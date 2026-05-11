---
title: Competitor Ads Farm
category: concept
summary: Daily Apify FB Ad Library scraper farm tracking 8 brands across two competitive sets — AI consulting/3Ps positioning (Anthropic, OpenAI, Hampton, DealMachine) and GLP-1 telehealth/Medvi (Hims, Ro, Eden, Henry Meds); 6:00 AM Pacific cron; three batches in (2026-05-06, 2026-05-10, 2026-05-11) the dedup pipeline has reached steady state (196 fetched → 6 new in batch 3, 97% dedup-skipped); brand-name substring filter still untuned across all three batches and a new noise root cause (Adobe Acrobat — no substring match) suggests Apify actor surfaces unsolicited adjacent brands as well
tags: [farm, competitor-ads, fb-ads, apify, dtc, telehealth, hims, glp-1, ai-consulting]
sources: 3
updated: 2026-05-11
---

# Competitor Ads Farm

## What it is

The third farm in this vault (after `ai-creators-youtube` and `x-monitor`) — automated daily ingest of competitor ads from Meta Ad Library via Apify's `facebook-ads-library-scraper` actor. Mirrors the [[concepts/context-farming]] pattern but for paid-creative intelligence rather than YouTube/X organic content.

Config lives at `farmers/competitor-ads.md`. State (seen ad IDs, capped 2000) at `farmers/state/competitor-ads.json`. Schedule: `0 6 * * *` (6 AM Pacific, 30 min after the YouTube farm to avoid wiki-lock contention).

## Two competitive sets

### Set 1 — AI consulting / 3Ps positioning

- **[[anthropic]]** — anchor brand
- **[[openai]]** — anchor brand
- **[[hampton-founders]]** — peer/adjacent founder community
- **DealMachine** — peer/adjacent

Feeds copy decisions for landing pages, Skool community pitch, sales pages.

### Set 2 — GLP-1 telehealth (Medvi competitive set)

- **[[hims]]** — primary benchmark (highest creative volume in 2026-05-06 batch — 45 ads)
- **[[ro]]** — direct competitor
- **Eden** — direct competitor (telehealth — *not* the gardening / bedding / fashion brands the bare-keyword search returns)
- **[[henry-meds]]** — direct competitor (compounded-first)

Feeds the Meta Ads agent's creative test backlog and Medvi positioning.

## Architecture (three phases)

Mirrors the YouTube farm:

1. **Phase 1 — Apify fetch** — pull active ads, dedup against state, write digest to `raw/ads/digest-{date}.{md,json}`, commit + push
2. **Phase 2 — Headless `claude -p /wiki-ingest`** — only fires if new-ad count > 0; creates/updates entity (brand) pages and concept pages, commits + pushes
3. **Phase 3 — Slack notify** — STUDY/NOTE/PASS verdict per ad with LLM 1-sentence summary

## Slack verdict scale

- **STUDY** — novel angle, hook, format, or claim worth tearing down for inspiration
- **NOTE** — useful reference but familiar pattern; file for context
- **PASS** — generic, recycled, dynamic-creative placeholders, FDA disclaimers only

Most days: NOTE or PASS dominate. STUDY is reserved for genuinely novel creative.

## Batch findings

### Batch 1 — 2026-05-06

From [[ads-digest-2026-05-06]]:

- **187 fetched / 183 new / 4 dedup-skipped** — first batch so dedup state was empty
- **[[hims]] is the volume leader** — 45 ads, three creative wedges (GLP-1, hair-loss "Hair Hybrids", Sex Rx), pioneered the [[concepts/compounded-drug-disclaimer]] and [[concepts/dtc-telehealth-ad-template]] patterns documented in this vault
- **AI labs ship dynamic-creative-only** — OpenAI (21 ads) and Anthropic (5) both run pure catalog/product-feed carousels with `{{product.name}}` headlines and `{{product.brand}}` bodies, zero static narrative
- **[[hampton-founders]] is the only "Hampton" with relevant creative** — vetted founder peer-group community for $3M+ revenue founders
- **Ro / Henry Meds / DealMachine produced ~zero relevant creative** — Ro had 1 placeholder; Henry Meds and DealMachine missing entirely
- **~65% noise rate** from substring brand-name matches

### Batch 2 — 2026-05-10

From [[ads-digest-2026-05-10]]:

- **190 fetched / 22 new / 168 dedup-skipped** — dedup pipeline working as designed; dropped 168 already-seen ads
- **[[hims]] adds Hard Mints product** — 4th Sex Rx SKU (chewable compounded ED for non-responders to traditional pills); first four-bullet variant of the [[concepts/dtc-telehealth-ad-template]]
- **[[openai]] catalog-ads-only confirmed** — 3 more carousels in the same Apr 2-21 launch cluster; pattern is now stable across two batches (24 total ads, 0 narrative)
- **[[ro]] placeholder pattern persists** — 2 more `{{product.brand}}` placeholders; 3 total Ro ads tracked, 0 with teardown-able copy
- **Anthropic, Henry Meds, DealMachine, Hampton Founders — 0 new ads** — dedup-cached or absent
- **~82% noise rate** — proportionally worse than batch 1 because dedup removed real creative but the noise pages keep firing fresh creative substring-matches

### Batch 3 — 2026-05-11

From [[ads-digest-2026-05-11]]:

- **196 fetched / 6 new / 190 dedup-skipped** — thinnest batch yet; **97% dedup-skipped** marks convergence to steady state
- **[[openai]] catalog-ads-only TRIPLE-confirmed** — 3 more carousels from a **new Apr 30 + May 8 campaign cluster** (not the Apr 2-21 cluster from batches 1+2). Fresh launch → same template → confirms catalog-ads-only is the standing strategy, not a stale-campaign artifact. **27 total OpenAI ads tracked, 0 narrative.**
- **Hims, Ro, Anthropic, Henry Meds, Hampton Founders, DealMachine — 0 new ads** — every other tracked brand fully dedup-cached
- **Signal-to-noise: 50/50** — 3 of 6 ads are tracked (OpenAI), 3 are noise (Eden Munoz, Adobe Acrobat, Hampton Roads Maritime Training)
- **New noise root cause: Adobe Acrobat** — no tracked brand keyword is a substring of "Adobe Acrobat." Suggests the Apify actor returns unsolicited adjacent / suggested-brand ads, not just substring matches. **The noise floor is structurally worse than substring matching** — exact-page-name allow-listing is now the only safe filter.

### Three-batch convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI ads | Real-signal % |
|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 50% |

The farm has converged. Future batches should average ≤10 new ads/day unless a tracked brand launches new creative. Per-batch teardown cadence is now feasible (small set per day) but the *interesting* new creative will be concentrated in launch-cycle batches.

## Known issue: brand-name filter is too permissive

The farmer config promises a post-fetch filter that *"drops third-party ads that mention a brand keyword (e.g. random pages running ads about 'Hims hair loss'). Only ads where the page name contains the search brand are kept."*

The 2026-05-06 digest shows the filter **kept** ads from third-party pages whose **page name** contains the keyword as a substring — so:

- "Eden" matched **Eden Brothers** (gardening, 14 ads), **Eden & Om** (bamboo sheets, 13), **Aelfric Eden** (fashion), **UNC Health Rockingham at Eden NC**, etc. — none are the GLP-1-telehealth Eden
- "Hampton" matched dozens of regional businesses (Hampton Inn, Hampton Roads Honda, Hampton Roads Transit, Hampton Sun, Classic Toyota Hampton, etc.) — none are Hampton Founders
- "Ro" matched Roads & Kingdoms, Roseionly, Rockfest, ProTyres Oradea, Modlet.ro, dozens more — none are Roman Health

**Noise rate by batch: ~65% (2026-05-06) → ~82% (2026-05-10) → 50% (2026-05-11).** The proportion drops in batch 3 only because total ad volume collapsed (6 ads); absolute noise (3 noise ads) is in line with prior batches. Without filter tuning, the steady-state noise mix stays meaningfully present in every batch.

New noise brands surfaced in 2026-05-10: **KaRoL G** ("Ro" inside "KaRoL"), **Uproot Clean** ("Ro" inside "Uproot"), **BaBylissPRO** ("Ro" inside "Pro"), **Hampton by Hilton**, **Visit Hampton VA**, **NAPA BDG South Hampton Roads**, **Hampton RV Trailer Sales**, **Hampton University Proton Cancer Institute**, **Hill Chiropractic** (root cause unclear).

New noise brands surfaced in 2026-05-11: **Eden Munoz** (Mexican banda singer, "Eden" substring), **Hampton Roads Maritime Training System / HRMTS** (Virginia maritime school, "Hampton" substring), **Adobe Acrobat** (**no tracked-brand substring at all** — confirms the Apify actor returns unsolicited adjacent / suggested-brand results, not just substring matches).

### Action items

- → tune the [[competitor-ads-farm]] to use **exact page-name match** or **page-ID allow-listing** rather than substring match. **Outstanding from 2026-05-06; not addressed by 2026-05-10 or 2026-05-11.**
- → for short brand names ("Ro", "Eden", "Hampton"), maintain an explicit allow-list of the actual FB Page IDs
- → consider adding `Roman Health`, `Ro Body`, `Hampton Founders`, `Eden Body` to the search-brand list to catch the variant page names
- → investigate the "Hill Chiropractic" match in 2026-05-10 and **"Adobe Acrobat" in 2026-05-11** — neither has a tracked brand keyword as substring; the Apify actor is almost certainly returning unsolicited adjacent results. Implication: substring filter alone won't fix the noise floor; allow-listing is required.

## Why this farm exists

Two specific products feed from it:

1. **Medvi compete-page work** — Hims/Ro/Henry Meds creative becomes the diff-target for Medvi positioning (price split, disclaimer language, wedge messaging, ad-template structure)
2. **Meta Ads agent project** — the wiki becomes a feature library the agent draws from when generating new Medvi creative

## Related

- [[concepts/context-farming]] — parent pattern (scheduled context ingest)
- [[concepts/compounded-drug-disclaimer]] — first concept this farm fed into the wiki
- [[concepts/dtc-telehealth-ad-template]] — second concept this farm fed into the wiki
- [[hims]], [[ro]], [[henry-meds]], [[openai]], [[anthropic]], [[hampton-founders]] — entity pages this farm seeds
- [[ads-digest-2026-05-06]] — first source from this farm

## Appears in

- [[sources/ads-digest-2026-05-06]] — first batch (183 new ads, 65% noise)
- [[sources/ads-digest-2026-05-10]] — second batch (22 new ads, 82% noise — Hims Hard Mints + OpenAI catalog confirmation)
- [[sources/ads-digest-2026-05-11]] — third batch (6 new ads, 50% noise, 97% dedup-skipped — OpenAI catalog triple-confirmed via new campaign cluster; Adobe Acrobat noise reveals non-substring failure mode)

## Open questions

- Will Ro / Henry Meds appear in next batches once the brand-name filter is tuned?
- What's the right cadence for Slack verdict review — every batch (manual), weekly digest (delegated), or per-STUDY-only (alert)?
- Should compounded GLP-1 mentions trigger a `> ⚠️ Compliance:` callout on the entity page automatically? (Currently manual.)
