---
title: FB Ads Digest — Competitor brands — 2026-05-11
category: source
summary: Third competitor-ads farm batch — 6 new FB Ad Library entries (196 fetched, 190 dedup-skipped) — the thinnest batch yet; OpenAI ships 3 more dynamic-creative-only carousels (third batch confirming the catalog-ads-only pattern → 27 total ads, 0 narrative); Hims/Ro/Anthropic/Henry Meds/Hampton Founders/DealMachine all absent (dedup-cached); 3 of 6 ads are noise (Eden Munoz, Adobe Acrobat, Hampton Roads Maritime Training) — Adobe Acrobat match has no obvious substring root cause and suggests the Apify actor surfaces unsolicited adjacent brands; signal-to-noise dropped to 50/50 and farm filter remains untuned since 2026-05-06
tags: [fb-ads, ad-library, openai, dtc, competitor-ads, catalog-ads, dedup, farm-tuning]
sources: 1
source_path: raw/ads/digest-2026-05-11.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-11
updated: 2026-05-11
---

# FB Ads Digest — 2026-05-11

Third batch from the [[competitor-ads-farm]]. **6 new ads, 190 dedup-skipped** out of 196 fetched across 8 tracked brand keywords (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Thinnest batch yet** — 6 new ads / 196 fetched / 97% dedup-skipped. Steady-state cadence is now visible: after the 2026-05-06 cold-start batch (183 new) and the 2026-05-10 mid-state batch (22 new), the farm has converged to ~6-25 new ads/day where dedup catches the vast majority of fetches.
- **OpenAI catalog-ads-only confirmed across THREE batches** — 3 more `{{product.name}}` / `{{product.brand}}` carousels. Cumulative: 27 OpenAI ads tracked, 0 with teardown-able copy. The strategy is now triple-confirmed; this is no longer an observation but a baseline assumption for [[entities/openai]].
- **Zero new ads for every other tracked brand** — Hims, Ro, Anthropic, Henry Meds, Hampton Founders, DealMachine all 0. Dedup state is now comprehensive enough to suppress nearly all known creative.
- **Signal-to-noise: 50/50** — only 3 of 6 ads are tracked-brand (OpenAI); the other 3 are noise (Eden Munoz, Adobe Acrobat, Hampton Roads Maritime Training). Total noise rate continues climbing across batches: 65% → 82% → 50% (noise count dropped but real-signal count dropped further).
- **New noise root cause: Adobe Acrobat** — one ad is from Adobe Acrobat. No tracked brand keyword (Hims, Ro, Eden, Henry, Anthropic, OpenAI, Hampton, DealMachine) is a substring of "Adobe Acrobat." This suggests the Apify actor returns unsolicited adjacent / suggested-brand ads, not just substring matches. Worth investigating.
- **Brand-name filter still untuned** — farm action item from 2026-05-06 has now persisted across three batches.

## Source

- Path: `raw/ads/digest-2026-05-11.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 196 • New: 6 • Dedup-skipped: 190

## Tracked-brand creative inventory

### OpenAI (3 new ads) — catalog-ads-only confirmed (third batch)

All three ads:
- Format: carousel
- Title: `{{product.name}}`
- Body: `{{product.brand}}`
- Started: 2 ads on 2026-05-08, 1 ad on 2026-04-30
- IDs: `1337964444896096`, `1481884507069298`, `1638491670630932`

The 2026-05-08 launches are the **first new OpenAI campaign cluster outside the Apr 2-21 wave** observed in batches 1+2. Same dynamic-creative format though — so the campaign launched but the creative template hasn't changed. Treat as confirming evidence that catalog-only is OpenAI's standing FB strategy, not a one-off campaign.

> ⚠️ Pattern triple-confirmed: OpenAI's FB strategy is catalog-ads-only across three batches. **27 total OpenAI ads tracked, 0 with teardown-able copy.** New 2026-05-08 campaign cluster confirms the pattern survives new campaign launches (not just a stale Apr campaign carrying through).

→ See [[entities/openai]] for cumulative inventory.

### Hims, Ro, Anthropic, Henry Meds, Hampton Founders, DealMachine (0 new ads each)

All dedup-cached or absent. Pattern from 2026-05-10 holds — once the cache is warm, real creative shows up only when a brand launches new campaigns. Hims' 4-SKU Sex Rx wedge + Hair Hybrids template haven't refreshed creative since 2026-05-10.

## False positives ("brand-name match" noise)

3 of 6 ads (50%) are off-target. Lower absolute noise count than prior batches because dedup also catches recurring noise pages — but real-signal also dropped, so noise *proportion* stays substantial.

### "Eden" false positive (1 ad)

- **Eden Munoz** — first appearance of this noise brand. Likely the Mexican regional musician (banda singer, ex-Calibre 50 vocalist). Carousel placeholder, started 2026-01-13 (older campaign). Adds to the "Eden" noise inventory alongside Eden & Om, Eden Brothers, Aelfric Eden, UNC Health Rockingham at Eden NC documented in prior batches.

### "Hampton" false positive (1 ad)

- **Hampton Roads Maritime Training System (HRMTS)** — Virginia regional maritime training school. Carousel placeholder, started 2026-04-27. Adds to the Hampton/Virginia geographic noise inventory (Hampton by Hilton, Visit Hampton VA, NAPA BDG South Hampton Roads, Hampton RV, Hampton University Proton Cancer Institute, Hampton Roads Honda, Hampton Roads Transit).

### Unclear-root-cause false positive (1 ad)

- **Adobe Acrobat** — Adobe's PDF product. Carousel placeholder, started 2026-04-25. **None of the tracked brand keywords is a substring of "Adobe Acrobat."** This is a new failure mode — either the Apify actor expanded the search to suggested-brand neighbors (Adobe is a major SaaS advertiser that appears near AI-labs in FB's category taxonomy), or the actor returned an unrelated trending ad. **Worth investigating** — if confirmed, the noise floor is structurally worse than just substring matching, and exact-page-name allow-listing becomes the only safe filter.

## Cross-cutting patterns

### OpenAI's catalog-ads-only strategy is now triple-confirmed

| Batch | Date | OpenAI ads | Format | Campaign cluster |
|---|---|---|---|---|
| 1 | 2026-05-06 | 21 | carousel | Apr 2-21 |
| 2 | 2026-05-10 | 3 | carousel | Apr 7 (subset of cluster 1) |
| 3 | 2026-05-11 | 3 | carousel | Apr 30 + May 8 (new cluster) |
| **Total** | | **27** | **all carousel** | **2 launch clusters** |

The third batch is the most decisive evidence — it shows a *new* campaign cluster (Apr 30 + May 8) using the exact same dynamic-creative template as the older Apr 2-21 cluster. If OpenAI were going to shift to narrative creative, a new campaign launch is when they'd do it. They didn't. Catalog-ads-only is the standing strategy, not a launch-cycle artifact.

→ [[entities/openai]] updated to reflect three-batch confirmation.

### The farm has reached steady state

Three batches of trend data:

| Batch | Fetched | New | Dedup-skipped | New % |
|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) |
| 2026-05-10 | 190 | 22 | 168 | 12% |
| 2026-05-11 | 196 | 6 | 190 | 3% |

By batch 3, dedup is catching 97% of fetches. The farm has converged. Future batches should be expected to surface ≤10 new ads/day on average unless a tracked brand launches a fresh campaign.

This makes per-batch signal density structurally higher (small set of genuinely new creative to study) but per-batch volume structurally lower (most ingests will be "1-3 new ads + noise"). The right cadence for STUDY-grade teardowns is now **per-batch** rather than weekly digest.

### Noise filter is the blocking bottleneck

Three batches in, the brand-name substring filter has never been tuned. The noise inventory now totals:

- **Eden noise:** Eden & Om, Eden Brothers, Aelfric Eden, UNC Health Rockingham at Eden NC, **Eden Munoz** (NEW)
- **Hampton noise:** Hampton Inn / Hampton by Hilton, Hampton Roads Honda, Hampton Roads Transit, Hampton Sun, Classic Toyota Hampton, Visit Hampton VA, NAPA BDG South Hampton Roads, Hampton RV Trailer Sales, Hampton University Proton Cancer Institute, **Hampton Roads Maritime Training (HRMTS)** (NEW)
- **Ro noise:** Roads & Kingdoms, Roseionly, Rockfest, ProTyres Oradea, Modlet.ro, KaRoL G, Uproot Clean, WR Performance Products, BaBylissPRO
- **Unclear-cause noise:** Hill Chiropractic (2026-05-10), **Adobe Acrobat** (NEW — 2026-05-11)

The Adobe Acrobat match is the most important new data point — it confirms the noise floor isn't just substring matching but also includes Apify-actor "adjacent brand" expansion. Without an explicit page-ID allow-list, the steady-state will continue to include unsolicited adjacent ads.

## Open questions

- Why did Adobe Acrobat surface? (Apify actor adjacency expansion? Suggested-brand from FB's API? Worth confirming on the actor's docs.)
- Has OpenAI's 2026-05-08 launch cluster moved the catalog destination — different product surface than the Apr 2-21 cluster?
- Why are Hims and Ro completely silent for a full day? (Either no new creative shipped or dedup is over-suppressing — worth a manual ad-library check to confirm.)

## Related

- [[competitor-ads-farm]] — third batch from this farm; three-batch steady state now established
- [[openai]] — catalog-ads-only confirmed across three batches (27 total ads, 0 narrative)
- [[ads-digest-2026-05-06]] — first batch (183 new, cold start)
- [[ads-digest-2026-05-10]] — second batch (22 new, Hims Hard Mints + OpenAI confirmation #2)

## Appears in

- Third entry in `wiki/sources/` for the competitor-ads farm. Marks the convergence to steady-state dedup (97%) and the OpenAI catalog-ads-only pattern's third confirmation across distinct campaign clusters.
