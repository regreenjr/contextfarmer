---
name: competitor-ads
description: Pull competitor ads from Meta Ad Library (Facebook/Instagram) for AI consulting + GLP-1 telehealth positioning. Cloud-routine-friendly via Apify.
fetcher: apify
fetcher_script: ~/.claude/skills/farmer/scripts/apify_fb_ads.py
fetcher_args:
  brands:
    # 3Ps / AI consulting space
    - "Anthropic"
    - "OpenAI"
    - "Hampton"
    - "DealMachine"
    # GLP-1 telehealth (Medvi competitive set)
    - "Hims"
    - "Ro"
    - "Eden"
    - "Henry Meds"
  max_per_brand: 8
  country: US
raw_path: "raw/ads/digest-{date}.md"
json_sidecar_path: "raw/ads/digest-{date}.json"
state_path: "farmers/state/competitor-ads.json"
ingest: auto
ingest_skip_if_zero_new: true
dedup_by: state-file              # tracks ad_archive_id per ad
last_run: 2026-05-05
schedule_cron: "0 6 * * *"        # 6:00 AM Pacific (30 min after YouTube to avoid wiki-lock contention)
auto_commit: true
requires_env: [APIFY_TOKEN]
---

# Competitor Ads Farmer (Apify FB Ad Library)

## Purpose

Two competitive sets feeding two different products:

1. **AI consulting / 3Ps positioning** — Anthropic, OpenAI (anchor brands);
   Hampton, DealMachine (peer/adjacent). Feeds copy decisions for landing pages,
   Skool community pitch, sales pages.

2. **GLP-1 telehealth (Medvi)** — Hims, Ro, Eden, Henry Meds. Direct competitor
   creative + claims + compliance language. Feeds the Meta Ads agent's creative
   test backlog and Medvi positioning doc.

## How it works

Uses the `apify/facebook-ads-scraper` actor (9.6M runs, official Apify). Hits
the Meta Ad Library search URL for each brand, returns active ads with full
metadata: `adArchiveID` (dedup key), `pageName`, `snapshot.body.text` (primary
copy), `snapshot.title` (headline), creative format (image/video/carousel),
start/end dates, platforms, reach estimates.

Brand-name filter post-fetch drops third-party ads that mention a brand keyword
(e.g. random pages running ads about "Hims hair loss"). Only ads where the page
name contains the search brand are kept.

## Required env

```bash
export APIFY_TOKEN=apify_api_xxxxx
```

Same token as the YouTube farm and `x-monitor`.

## Output

```
~/Obsidian/Wiki/raw/ads/
├── digest-2026-05-05.md       # markdown digest grouped by brand
├── digest-2026-05-05.json     # JSON sidecar with normalized ad data
└── ...

~/Obsidian/Wiki/farmers/state/competitor-ads.json   # seen ad IDs (capped 2000)
```

## Three phases (mirroring YouTube farm)

1. **Phase 1 — Apify fetch:** pull active ads, dedup against state, write digest, commit + push
2. **Phase 2 — Headless `claude -p /wiki-ingest`:** only if new ads > 0; creates/updates entity (brand) pages and concept pages (e.g. "compounded GLP-1 disclaimers"), commits + pushes
3. **Phase 3 — Slack notify:** always — STUDY/NOTE/PASS verdict per ad with LLM-generated 1-sentence summary + reasoning

## Slack verdict scale

- **STUDY** — novel angle, hook, format, or claim worth tearing down for inspiration
- **NOTE** — useful reference but familiar pattern; file for context
- **PASS** — generic, recycled, dynamic-creative placeholders, FDA disclaimers only

Most ads will be NOTE or PASS — STUDY is reserved for genuinely interesting
creative.

## Notes

- Most days will dedup heavily (ad libraries update slowly). That's fine — the
  value is catching the day a new ad drops.
- For Medvi-related ads, the wiki ingestor flags compliance-relevant claims
  (FDA, "results may vary", BMI/eligibility) with `> ⚠️ Compliance:` callouts.
- This farm pairs with the Meta Ads agent project — the wiki becomes a feature
  library the agent draws from when generating new creative.
