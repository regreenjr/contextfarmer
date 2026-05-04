---
name: competitor-ads
description: Pull competitor ads (FB/LinkedIn ad library) for the AI consulting + GLP-1 telehealth + Meta-ads-agent positioning
fetcher_skill: competitive-ads-extractor
fetcher_args:
  brands:
    # 3Ps / AI consulting space
    - "Anthropic"
    - "OpenAI"
    - "Hampton"               # peer high-end community
    - "DealMachine"           # GTM-engineering adjacent
    # GLP-1 telehealth (Medvi competitive set)
    - "Hims"
    - "Ro"
    - "Eden"
    - "Henry Meds"
  platforms: ["facebook", "linkedin"]
  since: "{{ last_run }}"
  include_creative_urls: true
  include_copy: true
raw_path: raw/ads/{brand_slug}/{date}.md
ingest: auto
dedup_by: brand+date          # one entry per brand per day
last_run: 2026-05-03
schedule_cron: "0 7 * * *"
auto_commit: true
---

# Competitor Ads Farmer

## Purpose
Two distinct competitive sets feeding two different products:

1. **AI consulting / 3Ps positioning** — what messaging works for AI advisors
   right now (Anthropic, OpenAI as anchor brands; Hampton, DealMachine as peers).
   Feeds copy decisions for landing pages, Skool community pitch, sales pages.

2. **GLP-1 telehealth (Medvi)** — direct competitor ad creative + claims +
   compliance angles (Hims, Ro, Eden, Henry Meds). Feeds the Meta Ads agent's
   creative test backlog and the Medvi positioning doc.

## What the wiki should learn
- **Per brand:** active ad themes, claim patterns, creative format preferences
- **Cross-brand:** which messaging is converging vs. diverging in the category
- **Trend signals:** when a new brand enters or an old one shifts angle

## Notes
- Runs daily but ad libraries don't update that fast — most days will dedup.
  That's fine; the value is catching the day a new ad drops.
- For Medvi-related ads, the wiki should flag any compliance-relevant claims
  for review (FDA, "results may vary", BMI/eligibility language). Add a
  `> ⚠️ Compliance:` callout on those source pages.
- This farm pairs with the Meta Ads agent project — the wiki becomes the
  feature library the agent draws from when generating new creative.
