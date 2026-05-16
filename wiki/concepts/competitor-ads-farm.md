---
title: Competitor Ads Farm
category: concept
summary: Daily Apify FB Ad Library scraper farm tracking 8 brands across two competitive sets — AI consulting/3Ps positioning (Anthropic, OpenAI, Hampton, DealMachine) and GLP-1 telehealth/Medvi (Hims, Ro, Eden, Henry Meds); 6:00 AM Pacific cron; seven batches in (2026-05-06 → 2026-05-16) the dedup pipeline is at steady state (92-98.5% dedup-skipped, 3-22 new ads/day); brand-name substring filter still untuned across all seven batches; two batches have surfaced non-substring noise (Adobe Acrobat 2026-05-11, Romance miniseries 2026-05-12) confirming the Apify actor returns unsolicited adjacent brands at non-zero rate — page-ID allow-listing is the only structurally-safe filter; 2026-05-14 batch surfaces a concentrated "Eden" substring noise cluster (9 ads / 5 unrelated brands); 2026-05-15 batch marks two firsts — first 100%-noise batch (0 of 3 ads tracked-brand) and first universal-silence batch (all 8 tracked anchors return 0 new ads); **2026-05-16 batch reverses batch 6 decisively** — 67% real-signal rate (highest since cold start), Hims surges back with TWO verbatim re-launches mirroring batch 5 (Wegovy GLP-1 verbatim across 4 batches / 10-day stability window + Sex Rx + Climax Control verbatim 2 batches), **OpenAI's May 8 cluster expands 6 → 8 disproving batch 6's "fully dedup-cached" diagnosis** (updated diagnostic methodology: ≥3 silent batches needed for cache-completion claims), Ro signal returns after 5-batch silence (4th placeholder-only ad)
tags: [farm, competitor-ads, fb-ads, apify, dtc, telehealth, hims, glp-1, ai-consulting, surge-trough-cadence, cluster-pacing]
sources: 7
updated: 2026-05-16
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

### Batch 4 — 2026-05-12

From [[ads-digest-2026-05-12]]:

- **207 fetched / 16 new / 191 dedup-skipped** — volume bumps back up from batch 3's thin 6, but stays well below cold-start scale; 92% dedup-skipped consistent with steady state
- **[[openai]] catalog-ads-only QUADRUPLE-confirmed** — 4 more carousels (all 2026-05-08, expanding the cluster 2 from 2 → 6 ads across batches 3+4). **31 total OpenAI ads, 0 narrative.** Strongest behavioral baseline in this vault.
- **[[hims]] re-launches Wegovy GLP-1 verbatim** — 1 new ad (started 2026-05-07, ID `3567971296700086`) reusing the canonical [[dtc-telehealth-ad-template]] GLP-1 instantiation **word-for-word** from batch 1. First Hims ad since 2026-05-10 — confirms GLP-1 template is the standing creative and Hims A/B-tests inside structure, not across structure.
- **Ro, Anthropic, Henry Meds, Hampton Founders, DealMachine, Eden — 0 new ads each** — fourth consecutive batch
- **Signal-to-noise: 31%** — 5 of 16 ads are tracked (4 OpenAI + 1 Hims); 11 are noise. Noise-rate trend: 65% → 82% → 50% → 69% (mean ~67%)
- **NEW non-substring noise: Romance miniseries (3 ads)** — short-form serialized fiction app ("I rise from scavenger to king with alien tech"), no tracked-brand substring match. **Second non-substring noise event in two consecutive batches** after Adobe Acrobat (2026-05-11). The Apify actor returns unsolicited adjacent results at non-zero rate; substring filtering can NEVER close the noise floor.
- **Lauren Brooks long-form pet-allergy direct-response (4 ads)** — substring root cause "Brooks" contains "ro"; filed as a copy-pattern contrast to Hims' three-bullet template (confession + price anchor + treatment-failure cascade)

### Batch 5 — 2026-05-14

From [[ads-digest-2026-05-14]]:

- **202 fetched / 13 new / 189 dedup-skipped (94%)** — fifth batch, dedup at steady-state band
- **[[hims]] runs TWO verbatim template re-launches in one batch** — Sex Rx + Climax Control (started 2026-04-21, ID `3275837862576962`) AND Wegovy GLP-1 (started 2026-05-04, ID `956466943766183`). Wegovy template now verbatim across **3 batches** (2026-05-06 → 2026-05-12 → 2026-05-14, 8-day stability window). Multi-instance verbatim re-use within a single batch is the strongest single-batch confirmation of [[dtc-telehealth-ad-template]] stability to date.
- **[[anthropic]] ships first new ad since 2026-05-06** — 1 carousel ad (ID `1521217572752360`, started 2026-05-11) — same `{{product.name}}` / `{{product.brand}}` placeholder pattern. **Cumulative: 6 Anthropic ads across 2 distinct launch windows**, 0 with copy. Catalog-ads-only AI-lab pattern now confirmed across 2 windows for Anthropic — matching OpenAI's 2-cluster pattern.
- **[[openai]] returns 0 new ads — first OpenAI silence in 5 batches**. May 8 cluster (which expanded 2 → 6 across batches 3+4) appears fully dedup-cached. Cumulative remains **31 ads, 0 with copy.**
- **[[ro]], Henry Meds, Hampton Founders, DealMachine, Eden — 0 new ads each** — fifth consecutive batch
- **Signal-to-noise: 23%** (3 of 13 tracked) — noise-rate trend: 65% → 82% → 50% → 69% → **77%** (mean ~69%)
- **"Eden" substring noise cluster (9 ads / 5 unrelated brands)** — Evereden (1), Herb'N Eden (2), Eden Brothers (4), Aelfric Eden (1), Edens Garden Essential Oils (1). Most concentrated noise cluster across all 5 batches. The "Eden" search is structurally unable to disambiguate from skincare/wellness/fashion brands using "Eden" as a prefix/suffix.
- **Eden Brothers re-fires across non-consecutive batches** (4 ads in batch 1, 4 more in batch 5) — first noise page to multi-fire across non-consecutive batches in this farm. Per-ad-ID dedup means same noise page can keep emitting fresh creative.
- **Uproot Clean (3-batch repeat noise page)** — also appeared in batches 2+4. Long-form direct-response biofilm copy structurally interesting as contrast pattern to Hims template.
- **No new non-substring noise in batch 5** — every noise page traces to a tracked-brand substring. Non-substring noise events stay at 2 of 5 batches (40%).

### Batch 6 — 2026-05-15

From [[ads-digest-2026-05-15]]:

- **203 fetched / 3 new / 200 dedup-skipped (98.5%)** — sixth batch; **thinnest signal batch since cold start** and **highest dedup rate** of any batch
- **First 100%-noise batch.** 0 of 3 new ads tracked-brand. Six-batch noise-rate trend: 65% → 82% → 50% → 69% → 77% → **100%**
- **First universal-silence batch.** All 8 tracked anchors (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton Founders, DealMachine) ship 0 new ads
- **[[openai]] silence promotes from transient (batch 5) to confirmed.** Two consecutive silent batches eliminate the single-batch-timing hypothesis; **May 8 cluster confirmed fully dedup-cached at 6 ads**. Cumulative remains 31 ads, 0 with copy
- **[[hims]] goes silent for the second time in 6 batches** (first since batch 3 2026-05-11). Reads as inventory-cycle timing trough following batch 5's two-wedge multi-instance surge — not a structural shift
- **[[anthropic]] returns to silence** after the single 2026-05-11 carousel in batch 5. Cumulative 6 ads across 2 windows; open whether batch 7+ continues the slow-cluster or confirms 2026-05-11 as a standalone launch
- **Eden Plastic Surgery Miami (2 ads) — 9th distinct "Eden" substring brand** surfaced via this farm. Miami cosmetic-surgery clinic, long-form testimonial copy for the EVELift® facelift. Cumulative bare-"Eden" noise corpus: ~31 noise ads, 0 signal ads across 6 batches — most decisively net-negative tracked-brand filter
- **Heirloom Roses (1 carousel ad) — first plural-noun substring root cause.** "Ro" prefix in "Roses" confirms the bare-"Ro" filter's noise floor is structurally unbounded — virtually any English text containing "ro" as letter sequence can match, including common pluralizations
- **No new non-substring noise events** — every batch-6 ad traces to a tracked-brand substring. Non-substring noise events remain at 2 of 6 batches (33%)

### Batch 7 — 2026-05-16

From [[ads-digest-2026-05-16]]:

- **208 fetched / 9 new / 199 dedup-skipped (95.7%)** — seventh batch, dedup at steady-state band
- **Highest real-signal rate of any post-cold-start batch — 67%** (6 of 9 ads tracked-brand). Reverses batch 6's 100%-noise decisively.
- **[[hims]] surges back with 3 new ads — TWO verbatim template re-launches mirroring batch 5.** Wegovy GLP-1 template verbatim #4 (ID `1693764951776930`, started 2026-05-13) — now spans **4 batches / 10-day stability window**. Sex Rx + Climax Control verbatim #2 (ID `1683250979537135`, started 2026-04-30) — now spans 2 batches. Plus 1 placeholder ad. The 5→6→7 sequence (surge → trough → surge) is the **cleanest evidence yet for an alternating surge-trough wave cadence** with multi-wedge simultaneous re-launches in surge batches.
- **[[openai]] May 8 cluster expands 6 → 8** — 2 new May 8 carousels (IDs `1554270183093992` + `1999764597582322`) **decisively disprove batch 6's "fully dedup-cached at 6 ads" diagnosis.** Cluster is still rolling out at variable pacing (4-ad burst → 0 → 0 → 2-ad trickle). Updated diagnostic methodology: **≥3 silent batches needed for high-confidence cache-completion claims, not 2**. Cumulative 33 OpenAI ads.
- **[[ro]] signal returns after 5-batch silence** — 1 new placeholder ad (ID `1542915227491027`, started 2026-05-04). 4 cumulative Ro ads across 7 batches, ALL `{{product.brand}}` placeholders. Pattern confirmed across the longest window in the farm: bare-"Ro" page runs sparse catalog-driven dynamic creative only.
- **[[anthropic]] 0 new ads — 2nd consecutive silence batch post-2026-05-11.** "Standalone launch" hypothesis strengthens over "slow cluster" for the 2026-05-11 ad.
- **Signal-to-noise: 67%** (6 of 9 tracked) — noise-rate trend: 65% → 82% → 50% → 69% → 77% → 100% → **33%** (new mean ~68%)
- **3 noise ads**: Sean Gracet Roset (AI photo app — NEW "Ro" substring root in "Roset" surname); Nissan of Hampton (13th distinct Hampton regional-business noise page); Eden Munoz repeat (banda singer, also batch 3 — **3rd "Eden" noise page to multi-fire** across non-consecutive batches after Eden Brothers + Aelfric Eden)
- **No new non-substring noise events** — every batch-7 noise ad traces to a tracked-brand substring. Non-substring noise events stay at 2 of 7 batches (29%).

### Seven-batch convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Ro | Real-signal % |
|---|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | 1 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | 2 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 0 | 23% |
| 2026-05-15 | 203 | 3 | 200 | 1.5% | 0 | 0 | 0 | 0 | 0% |
| **2026-05-16** | **208** | **9** | **199** | **4%** | **2** | **3** | **0** | **1** | **67%** |

The farm is at steady state. Future batches should average **3-22 new ads/day with 92-98.5% dedup**. Real-signal proportion in the **0-67% band** (new mean ~32%), mean noise rate ~68%. Per-batch teardown cadence remains the right discipline; *interesting* new creative will continue to concentrate in launch-cycle batches. Batch 7's 67% signal rate is now the new high-water mark — driven by simultaneous Hims surge + OpenAI cluster expansion + Ro signal return hitting the same fetch window. Hims' surge-trough alternating cadence (batches 5→6→7) suggests interesting creative will concentrate in every-other-batch surge windows.

## Known issue: brand-name filter is too permissive

The farmer config promises a post-fetch filter that *"drops third-party ads that mention a brand keyword (e.g. random pages running ads about 'Hims hair loss'). Only ads where the page name contains the search brand are kept."*

The 2026-05-06 digest shows the filter **kept** ads from third-party pages whose **page name** contains the keyword as a substring — so:

- "Eden" matched **Eden Brothers** (gardening, 14 ads), **Eden & Om** (bamboo sheets, 13), **Aelfric Eden** (fashion), **UNC Health Rockingham at Eden NC**, etc. — none are the GLP-1-telehealth Eden
- "Hampton" matched dozens of regional businesses (Hampton Inn, Hampton Roads Honda, Hampton Roads Transit, Hampton Sun, Classic Toyota Hampton, etc.) — none are Hampton Founders
- "Ro" matched Roads & Kingdoms, Roseionly, Rockfest, ProTyres Oradea, Modlet.ro, dozens more — none are Roman Health

**Noise rate by batch: ~65% (2026-05-06) → ~82% (2026-05-10) → 50% (2026-05-11) → 69% (2026-05-12) → 77% (2026-05-14) → 100% (2026-05-15) → 33% (2026-05-16).** Mean ~68%. Without filter tuning, the steady-state noise mix stays meaningfully present in every batch — batch 6's 100%-noise outcome is the established worst-case and batch 7's 33% is the post-cold-start best-case data point.

New noise brands surfaced in 2026-05-10: **KaRoL G** ("Ro" inside "KaRoL"), **Uproot Clean** ("Ro" inside "Uproot"), **BaBylissPRO** ("Ro" inside "Pro"), **Hampton by Hilton**, **Visit Hampton VA**, **NAPA BDG South Hampton Roads**, **Hampton RV Trailer Sales**, **Hampton University Proton Cancer Institute**, **Hill Chiropractic** (root cause unclear).

New noise brands surfaced in 2026-05-11: **Eden Munoz** (Mexican banda singer, "Eden" substring), **Hampton Roads Maritime Training System / HRMTS** (Virginia maritime school, "Hampton" substring), **Adobe Acrobat** (**no tracked-brand substring at all** — confirms the Apify actor returns unsolicited adjacent / suggested-brand results, not just substring matches).

New noise brands surfaced in 2026-05-12: **Romance miniseries** (3 ads, **no tracked-brand substring** — second non-substring noise event), **Lauren Brooks** (4 ads, "Brooks" contains "ro"; long-form pet-allergy direct-response copy worth filing as a contrast pattern), **Builders Protein Bars** ("Pro" contains "ro"), **Blake Hampton** ("Hampton" substring).

New noise brands surfaced in 2026-05-14: **Evereden** ("Eden" inside "Evereden" — kid skincare, Harvard/Stanford doctor moms positioning), **Herb'N Eden** (2 ads, exact "Eden" substring — natural handmade soaps, $6 free-sample-pack lead-magnet copy), **Edens Garden Essential Oils** (exact "Eden" substring — essential oils). Also: **Eden Brothers** (4 ads — REPEAT noise page from batch 1; first noise page to multi-fire across non-consecutive batches), **Aelfric Eden** (REPEAT from batch 1 — fashion / hoodies $49 spring sale), **Uproot Clean** (REPEAT from batches 2+4 — pet-odor washing-machine biofilm long-form copy). The "Eden" substring noise cluster (9 ads / 5 unrelated brands) is the single most concentrated noise pattern across all 5 batches.

New noise brands surfaced in 2026-05-15: **Eden Plastic Surgery Miami** (2 video ads, exact "Eden" substring — Miami cosmetic surgery clinic, EVELift® facelift testimonial copy, **9th distinct "Eden" brand** surfaced via this farm), **Heirloom Roses** (1 carousel ad — "Ro" prefix in **"Roses"** — first time a plural-noun pluralization of "Ro" surfaces as substring root cause, confirming the bare-"Ro" filter's noise floor is structurally unbounded). Batch 6 has zero non-substring noise events.

New noise brands surfaced in 2026-05-16: **Sean Gracet Roset** (1 video ad — "Ro" inside "Roset" surname — first AI/tech consumer-app noise page matched via "Ro"; "FREE APP" headline + "Try the new AI photo trend now"); **Nissan of Hampton** (1 carousel ad — exact "Hampton" substring — 13th distinct Hampton regional-business noise page; Virginia used-vehicle dealer with `{{vehicle.description}}` dynamic-feed placeholder); **Eden Munoz REPEAT** (1 placeholder ad — 2nd appearance after batch 3; 3rd "Eden" noise page to multi-fire across non-consecutive batches after Eden Brothers + Aelfric Eden). Batch 7 has zero non-substring noise events.

### Non-substring noise is now confirmed recurring, not one-off

Two of four batches have surfaced noise pages with **no tracked-brand substring match**:

- 2026-05-11: **Adobe Acrobat** (1 ad)
- 2026-05-12: **Romance miniseries** (3 ads — multiplier effect)

This rules out the "Adobe Acrobat was a fluke" hypothesis. The Apify `facebook-ads-library-scraper` actor returns unsolicited adjacent / suggested-brand results at non-zero rate, with multi-ad volume per noise page. Implication: **substring-allowlist is necessary but not sufficient; page-ID allow-listing is the only structurally-safe noise filter.**

### Action items

- → tune the [[competitor-ads-farm]] to use **exact page-name match** or **page-ID allow-listing** rather than substring match. **Outstanding since 2026-05-06; not addressed by 2026-05-10, 2026-05-11, 2026-05-12, 2026-05-14, 2026-05-15, or 2026-05-16 (7 consecutive batches).**
- → for short brand names ("Ro", "Eden", "Hampton"), maintain an explicit allow-list of the actual FB Page IDs. **The bare-"Ro" filter is decisively net-negative across 5 batches** (3 placeholder Ro ads total, dozens of "ro"-substring noise ads). **The bare-"Eden" filter is now also decisively net-negative** — batch 5 alone surfaced 9 noise ads from 5 unrelated brands (Evereden / Herb'N Eden / Eden Brothers / Aelfric Eden / Edens Garden Essential Oils) with 0 telehealth-Eden signal across all 5 batches.
- → consider adding `Roman Health`, `Ro Body`, `Hampton Founders`, `Eden Body` to the search-brand list to catch the variant page names
- → investigate the "Hill Chiropractic" match (2026-05-10), **"Adobe Acrobat" (2026-05-11), and "Romance miniseries" (2026-05-12)** — none has a tracked brand keyword as substring; with two events in two consecutive batches, the Apify actor is **confirmed** to return unsolicited adjacent results. **Substring filter alone cannot close the noise floor; allow-listing is required.**
- → handle multi-fire noise pages — Eden Brothers (batches 1+5), Uproot Clean (batches 2+4+5), Aelfric Eden (batches 1+5) all show that per-ad-ID dedup is insufficient when a noise page keeps emitting fresh creative. Page-ID *blocklist* (in addition to allow-list) would close this failure mode for known recurring noise sources.

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
- [[sources/ads-digest-2026-05-12]] — fourth batch (16 new ads, 69% noise, 92% dedup-skipped — OpenAI catalog QUADRUPLE-confirmed via cluster 2 expansion; Hims Wegovy template re-launched verbatim (inside-structure A/B confirmed); Romance miniseries 3-ad multiplier as second non-substring noise event)
- [[sources/ads-digest-2026-05-14]] — fifth batch (13 new ads, 77% noise, 94% dedup-skipped — Hims runs TWO verbatim template re-launches in one batch (Sex Rx + Climax Control + Wegovy GLP-1, multi-instance template re-use within the same batch); Anthropic ships first new ad since 2026-05-06 (placeholder, started 2026-05-11) confirming catalog-ads-only across 2 launch windows; OpenAI 0 new ads (first silence in 5 batches); "Eden" substring noise cluster (9 ads / 5 unrelated brands — Evereden / Herb'N Eden / Eden Brothers / Aelfric Eden / Edens Garden); Eden Brothers as first noise page to multi-fire across non-consecutive batches)
- [[sources/ads-digest-2026-05-15]] — sixth batch (3 new ads, **100% noise**, 98.5% dedup-skipped — first all-noise batch and first universal-silence batch across all 8 tracked anchors; OpenAI silence promotes from transient (batch 5) to confirmed fully dedup-cached (batch 6); Hims second silence batch in 6 (post-surge inventory-cycle trough); Anthropic returns to silence after single 2026-05-11 carousel; Eden Plastic Surgery Miami adds 9th distinct "Eden" brand to cumulative noise corpus; Heirloom Roses adds first plural-noun "Roses" → "Ro" substring root cause)
- [[sources/ads-digest-2026-05-16]] — seventh batch (9 new ads, **67% signal — new high-water mark**, 95.7% dedup-skipped — Hims surges with 3 ads (Wegovy GLP-1 verbatim #4 spanning 4-batch / 10-day stability window + Sex Rx + Climax Control verbatim #2 + 1 placeholder), mirroring batch 5's two-wedge surge pattern; OpenAI's May 8 cluster expands 6 → 8 with 2 new ads, **decisively disproving batch 6's "fully dedup-cached" diagnosis** (updated diagnostic methodology: ≥3 silent batches needed for cache-completion); Ro signal returns after 5-batch silence (4th placeholder-only ad); Anthropic 2nd consecutive silence batch post-2026-05-11; 3 noise ads — Sean Gracet Roset (NEW "Roset" surname "Ro" substring root) + Nissan of Hampton (13th distinct Hampton regional-business noise) + Eden Munoz repeat (3rd "Eden" multi-fire page); the 5→6→7 surge→trough→surge sequence confirms Hims' alternating wave cadence as standing creative-ops pattern)

## Open questions

- Will Ro / Henry Meds appear in next batches once the brand-name filter is tuned?
- What's the right cadence for Slack verdict review — every batch (manual), weekly digest (delegated), or per-STUDY-only (alert)?
- Should compounded GLP-1 mentions trigger a `> ⚠️ Compliance:` callout on the entity page automatically? (Currently manual.)
