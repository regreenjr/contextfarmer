---
title: FB Ads Digest — Competitor brands — 2026-06-07
category: source
summary: Eighteenth competitor-ads farm batch — 6 new FB Ad Library entries (193 fetched, 187 dedup-skipped, 96.9%) at a **clean 1-day gap** from batch 17 — the **second clean 1-day-gap batch in a row, and it inverts batch 17's reading**; **[[hims]] runs a GENUINE THREE-WEDGE surge — the 2nd in the farm after batch 14** — 4 ads, ALL with verbatim static copy across three wedges: Wegovy GLP-1 verbatim (ID `1318231786944621` started 2026-06-05) — **Wegovy RETURNS after exactly ONE silent batch (17)** + Hair Hybrids verbatim ×2 (IDs `1006359278539108` started 2026-06-04 + `2795816404144725` started 2026-06-02) + **Sex Rx + Climax Control RETURNS** (ID `1533618474776489` started 2026-05-26, *"Introducing the 2-in-1 pill"* intro-word A/B variant) after exactly ONE silent batch (17); this is a **trough→surge alternation at the 1-day-gap resolution** — two consecutive clean 1-day batches give OPPOSITE pictures (batch 17 = 1 copy wedge / Hair-Hybrids-only vs batch 18 = 4 copy ads / 3 wedges), **REFINING the batch-17 "genuine copy rate ~1 copy ad/day, Hair-Hybrids-only baseline" reading — that baseline does NOT hold even at 1-day resolution; the wedge mix rotates day-to-day and Wegovy + Sex Rx are dormant-not-closed in the strongest possible sense (silent exactly 1 batch, back the next)**; Hims 4.0/day = 4.0 copy/day (the most copy-dense 1-day-gap Hims batch in the farm, edging batch 14's 4.0/3-copy); **[[ro]] RETURNS from batch-17 silence with 2 placeholders — Run 6** (IDs `1321326639352870` started 2026-06-05 + `1002278945590232` started 2026-06-01, both `{{product.brand}}`); **[[openai]] SILENT — first OpenAI silence since batch 14** (Cluster 4 holds at 2 for the 3rd consecutive batch; Cluster 3 stalled at 3/1, 23 days; cumulative 50 ads / 1 with copy); **[[anthropic]] 7th consecutive silence (12-18) — but the cadence-predicted next-ad date (~2026-06-08) STILL has NOT passed** (today is 2026-06-07, by 1 day) — **hold the stall call ONE more day; batch 19 (past 06-08) decides** between "slow-cluster continues" and "cluster stalled at 2"; **[[eden]] (TryEden) 5th consecutive silence (14-18)**; **0 noise ads — 100% real-signal rate (6 of 6), a NEW FARM HIGH** (beats batch 14's 80%); Henry Meds / Hampton / DealMachine — 18th consecutive batch no signal; cumulative 103 Hims / 50 OpenAI / 8 Anthropic / 17 Ro / 1 Eden
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, hims, one-day-gap, genuine-three-wedge, second-genuine-three-wedge, trough-to-surge-alternation, wegovy-wave-reopens, wegovy-returns-one-batch, sex-rx-climax-control-returns, climax-control-returns, both-sex-rx-skus-rotation, intro-word-ab-variant, dormant-not-closed, all-copy-hims-batch, hair-hybrids-verbatim, ro-returns, ro-run-6, openai-silent, anthropic-7th-silence, prediction-window-closes-06-08, eden-5th-silence, signal-rate-100, zero-noise, farm-high-signal]
sources: 1
source_path: raw/ads/digest-2026-06-07.md
source_date: 2026-06
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-06-07
updated: 2026-06-07
---

# FB Ads Digest — 2026-06-07

Eighteenth batch from the [[competitor-ads-farm]]. **6 new ads, 187 dedup-skipped** out of 193 fetched at a **clean 1-day gap** from batch 17 (2026-06-06). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **The second clean 1-day-gap batch in a row — and it INVERTS batch 17.** Batch 17 (1-day gap) reverted to a Hair-Hybrids-only trough (1 copy ad) and the read was *"the genuine per-day copy rate is ~1 copy ad/day (Hair Hybrids standing trough-wedge); Wegovy + Sex Rx dormant."* **Batch 18 — also a clean 1-day gap — ships a GENUINE THREE-WEDGE surge: 4 Hims ads, ALL with verbatim copy, across Wegovy + Hair Hybrids ×2 + Sex Rx Climax Control.** Wegovy and Sex Rx, silent in batch 17, **returned after exactly ONE silent batch.** This is the **2nd genuine three-wedge batch in the farm after batch 14** (the only other clean-1-day-gap multi-wedge surge).
- **The refinement: the batch-17 "~1 copy ad/day, Hair-Hybrids-only baseline" does NOT hold even at 1-day resolution.** Two back-to-back clean 1-day-gap batches give opposite pictures (1 copy wedge vs 3 copy wedges). **The wedge mix rotates day-to-day** — batch 17's Hair-Hybrids-only was itself a 1-day trough, not a stable state. This is a **trough→surge alternation at the 1-day-gap resolution** (batch 17 trough → batch 18 surge), the same surge-trough alternating cadence the farm has tracked at coarser gaps, now visible at the finest resolution. **Wegovy + Sex Rx are "dormant, not closed" in the strongest possible sense: silent exactly 1 batch, back the next.**
- **[[hims]] — 4 ads, ALL verbatim copy (the most copy-dense 1-day-gap Hims batch in the farm).** Wegovy GLP-1 verbatim (ID `1318231786944621`, started **2026-06-05** — the day of batch 17's fetch) reusing the canonical *"Get Wegovy® with Hims..."* → ✅ FDA-approved GLP-1 pill and pens / ✅ Medication as low as $149/mo / ✅ 100% online skeleton; Hair Hybrids verbatim ×2 (IDs `1006359278539108` started 2026-06-04 + `2795816404144725` started 2026-06-02, identical copy); **Sex Rx + Climax Control verbatim** (ID `1533618474776489`, started **2026-05-26**) — *"Introducing the 2-in-1 pill to get harder, and go longer..."* — the **intro-word A/B variant** first seen on batch 16's 2026-06-04 ad. Hims 4.0/day = 4.0 copy/day (edges batch 14's 4.0-ads/3-copy surge). Cumulative **103 ads across 18 batches.**
- **[[ro]] RETURNS from batch-17 silence — Run 6.** 2 `{{product.brand}}` placeholders (IDs `1321326639352870` started 2026-06-05 + `1002278945590232` started 2026-06-01) — consistent with Ro's irregular-burst cadence (a silence is typically followed by a fresh catalog re-surface). Cumulative **17 Ro ads, ALL placeholder-only.**
- **[[openai]] SILENT — first OpenAI silence since batch 14.** No new ads at the 1-day gap. **Cluster 4 (2026-05-22) holds at 2 ads for the 3rd consecutive batch (16+17+18)**; Cluster 3 (2026-05-15) stalled at 3 ads / 1 with copy (23 days post-launch); Cluster 2 (May 8) silent. Cumulative **50 ads, still 1 with copy** (49/50 = 98% placeholders). Lab-delta vs Anthropic 50/8 (~6.25x).
- **[[anthropic]] 7th consecutive silence (12-18) — but the cadence-prediction window has STILL not closed.** The 2026-05-11-cluster's observed 14-day cadence predicts the next ad ~2026-06-08, which **has not yet passed** (today is 2026-06-07, by 1 day). The silence count overshoots the ≥5-silent-batch threshold by two, but the prediction window closes tomorrow. **Hold the stall call ONE more day; batch 19 (past 06-08) is the decider** between "slow-cluster continues" and "cluster stalled at 2 ads." Cumulative **8 ads, 0 with copy.**
- **[[eden]] (TryEden) 5th consecutive silence (14-18)** after the batch-13 first signal. No "Eden" noise ad surfaced this batch.
- **0 noise ads — 100% real-signal rate (6 of 6) — NEW FARM HIGH** (beats batch 14's 80%). Every ad traces to a tracked brand (Hims 4 + Ro 2). The cleanest signal batch in 18.
- **Brand-name filter still untuned — 18th consecutive batch.** Outstanding since 2026-05-06 (though it cost nothing this batch — zero noise surfaced).

## Source

- Path: `raw/ads/digest-2026-06-07.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 193 • New: 6 • Dedup-skipped: 187 (96.9%)
- Gap from prior batch: **1 day** (batch 17 = 2026-06-06)

## Tracked-brand creative inventory

### [[hims]] — 4 new ads (GENUINE three-wedge surge; ALL verbatim copy)

The second genuine three-wedge batch in the farm (after batch 14), at a clean 1-day gap — and it inverts batch 17's Hair-Hybrids-only trough one day later.

**Wegovy GLP-1 verbatim — 1 re-launch** (*"Get Wegovy® with Hims, plus access to provider-led care, tailored treatment plans, and ongoing support designed around your lifestyle."* → ✅ FDA-approved GLP-1 pill and pens available / ✅ Medication as low as $149/mo—membership fee of $39 for first month, $149 thereafter / ✅ 100% online + *"Your goals. Your plan. Your pace."* + the expanded $149/$39-membership pricing footnote + Wegovy® / Novo Nordisk non-affiliation clause):

- ID `1318231786944621`, started **2026-06-05** (the day of batch 17's fetch — Wegovy returns after exactly 1 silent batch)

**Hair Hybrids verbatim — 2 re-launches** (*"Don't wait — join the hundreds of thousands of guys who've found true results. Get a treatment recommendation today, 100% online."* → 🗓️ Regrow in as few as 3-6 months / 🧑🏻‍⚕️ Doctor-trusted ingredients / 📦 Free shipping to your front door (if prescribed) + Hair Hybrids compounded disclaimer):

- ID `1006359278539108`, started **2026-06-04**
- ID `2795816404144725`, started **2026-06-02** (identical copy)

**Sex Rx + Climax Control verbatim — 1 re-launch** (*"Introducing the 2-in-1 pill to get harder, and go longer. Sex Rx + Climax Control combines tadalafil shown to result in more satisfying erections and help men last longer, plus PE treatment. Get started today—100% online with a free consultation."* → 🤩 Daily pill options for spontaneous sex / 🧑‍⚕️ Prescribed by licensed providers / 📦 100% online, free discreet shipping + Climax Control compounded disclaimer):

- ID `1533618474776489`, started **2026-05-26** — **Climax Control RETURNS after exactly 1 silent batch (17)**; uses the *"Introducing the 2-in-1 pill..."* **intro-word A/B variant** first seen on batch 16's 2026-06-04 ad (vs the older *"The 2-in-1 pill..."*).

**Strategic significance**: This batch is the **second genuine three-wedge surge** in the farm (after batch 14), and it lands at a clean 1-day gap — so, like batch 14 and unlike batch 16, it carries **no compression artifact**. The analytic payoff is the **direct inversion of batch 17**: batch 17 (1-day gap) reverted to a Hair-Hybrids-only trough and the reading was *"genuine copy rate ~1 copy ad/day (Hair Hybrids standing trough-wedge); Wegovy + Sex Rx dormant."* Batch 18 (also 1-day gap) ships 4 copy ads across three wedges, with **Wegovy and Sex Rx Climax Control both returning after exactly ONE silent batch.** Two consecutive clean 1-day-gap batches therefore give **opposite pictures** (1 copy wedge vs 3 copy wedges).

The refinement to the batch-17 reading: **the "~1 copy ad/day, Hair-Hybrids-only baseline" does NOT hold even at the 1-day resolution.** The wedge mix rotates day-to-day — batch 17's Hair-Hybrids-only was itself a 1-day trough, not a stable state. This is the **surge-trough alternating cadence visible at the finest resolution** (batch 17 trough → batch 18 surge, same shape as 5→6→7, 14→15, just at consecutive single days). The methodological takeaways stack:

- **Batch 16 (6-day gap) demonstrated the *compression* artifact** (multi-day accumulation looks like a mega-surge).
- **Batch 17 (1-day gap) was read as the clean trough baseline** (Hair-Hybrids-only, ~1 copy/day).
- **Batch 18 (1-day gap) breaks that baseline** — the very next day produces a 3-wedge 4-copy surge. So even single-day samples swing between trough and surge; the surge→trough "cadence" is real but operates at the daily resolution, and **no single 1-day batch defines a stable per-day copy rate.**

**Wegovy + Sex Rx are "dormant, not closed" in the strongest sense yet observed** — silent exactly 1 batch (17), back the next (18). This is the cleanest confirmation of the batch-14 methodology lesson (downgrade "closed" to "dormant"): a wedge can go silent for a single fetch and re-fire verbatim immediately. **All three wedge templates remain live diff-targets**; no wedge or SKU retired across 18 batches. Cumulative **103 Hims ads.**

Note on copy density: all 4 Hims ads carry verbatim static copy — the **most copy-dense 1-day-gap Hims batch in the farm** (4.0 copy ads/day, edging batch 14's 4 ads / 4 copy across 3 wedges — same magnitude, different Sex Rx SKU: batch 14 ran Testosterone Support, batch 18 runs Climax Control, confirming surge composition rotates across SKUs within the Sex Rx wedge as well as across wedges).

### [[ro]] — 2 new ads (RETURNS from batch-17 silence — Run 6)

Two `{{product.brand}}` placeholders (catalog-driven dynamic creative, no static narrative):

- ID `1321326639352870`, started **2026-06-05**
- ID `1002278945590232`, started **2026-06-01**

**Strategic significance**: Ro returns from its single batch-17 silence (post-Run-5) with a fresh 2-placeholder catalog re-surface — **Run 6** in Ro's irregular-burst cadence (Run 1 batches 1-2 / Run 2 batches 7-9 / Run 3 batch 12 / Run 4 batch 15 / Run 5 batch 16 / Run 6 batch 18). The single silent batch (17) was a trough between catalog re-surface events, exactly as Ro's pattern predicts (a burst is typically followed by silence, then another burst). Pattern unchanged across 18 batches: **catalog-driven dynamic creative only, zero static narrative.** Cumulative **17 Ro ads, ALL placeholder-only.**

### [[openai]] — 0 new ads (SILENT; first OpenAI silence since batch 14)

No new OpenAI ads at the 1-day gap — the first OpenAI silence since batch 14 (batches 15+16+17 each shipped ≥1 placeholder). **Cluster 4 (2026-05-22) holds at 2 ads for the 3rd consecutive batch (16+17+18)** — the "Cluster 4 opening" reading neither strengthens nor breaks (a 3-batch non-expansion at 2 ads now leans slightly toward "stalled at 2 / irregular re-surface" over "genuine slow-rolling cluster"). **Cluster 3 (2026-05-15) remains stalled at 3 ads / 1 with copy** (23 days post-launch — one-off-creative-test reading extremely firm). Cluster 2 (May 8) silent. Cumulative **50 ads across 18 batches, still 1 with copy** (49/50 = 98% placeholders). Lab-comparison delta vs Anthropic in the same 18-batch window: OpenAI 50 / Anthropic 8 — ~6.25x.

### [[anthropic]] — 0 new ads (7th consecutive silence 12-18; prediction window closes 06-08)

No new Anthropic ads — **7th consecutive silent batch** since the batch-11 slow-cluster expansion. The silence count now overshoots the ≥5-silent-batch threshold by two, **BUT the 2026-05-11-cluster's observed 14-day cadence predicts the next ad ~2026-06-08, which has STILL not passed** (today is 2026-06-07, by exactly 1 day). The prediction window closes tomorrow. **Hold the stall call ONE more day; batch 19 (past 06-08) is the decider** between "slow-cluster continues at ~14-day cadence" and "cluster stalled at 2 ads." Cumulative **8 ads, 0 with copy** — unchanged; Anthropic remains 100% placeholder (8/8) across 18 batches while [[openai]] shipped its 1 copy ad in batch 9 (never expanded).

### [[eden]] (TryEden) — 0 new ads (5th consecutive silence 14-18)

No new TryEden ads — **5th consecutive silent batch** after the batch-13 first-signal placeholder. Five silent batches still don't establish Eden's cadence (irregular like [[ro]], or a single ad then dormant). No "Eden" noise ad surfaced this batch (the filter cost nothing). Whether TryEden ever ships static copy — the [[medvi-positioning]] diff-target — remains the open Eden question. Cumulative **1 Eden ad, placeholder-only.**

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (18th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (18th consecutive batch)

## False positives ("brand-name match" noise) — 0 of 6 ads (0%)

**Zero noise ads — the cleanest signal batch in the farm.** All 6 new ads trace to tracked brands (Hims 4 + Ro 2). 100% real-signal rate, a new farm high (beats batch 14's 80%). The bare-substring filter remains untuned (18th consecutive batch) but cost nothing this batch — no "Ro" / "Eden" / "Hampton" substring noise drew into the small 6-ad batch.

### Cumulative noise-corpus updates

- No new first-fire noise pages; no returning noise pages. Noise corpus unchanged from batch 17 (Aelfric Eden main + EU + UK; TRELEGY 2-condition GSK page; the "Ro" / "Eden" / "Hampton" substring brands enumerated in prior batches).
- **Non-substring noise events**: still 2 of 18 batches (11.1%) — none this batch.

## Cross-cutting patterns

### Eighteen-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Ro | Eden | Real-signal % |
|---|---|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | 1 | 0 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | 2 | 0 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 0 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 0 | 0 | 23% |
| 2026-05-15 | 203 | 3 | 200 | 1.5% | 0 | 0 | 0 | 0 | 0 | 0% |
| 2026-05-16 | 208 | 9 | 199 | 4% | 2 | 3 | 0 | 1 | 0 | 67% |
| 2026-05-20 | 213 | 36 | 177 | 17% | 7 | 8 | 0 | 2 | 0 | 47% |
| 2026-05-22 | 208 | 17 | 191 | 8% | 3 | 5 | 1 | 1 | 0 | 59% |
| 2026-05-23 | 211 | 8 | 203 | 4% | 1 | 2 | 0 | 0 | 0 | 37.5% |
| 2026-05-25 | 213 | 12 | 201 | 5.6% | 0 | 2 | 1 | 0 | 0 | 25% |
| 2026-05-26 | 207 | 6 | 201 | 2.9% | 1 | 1 | 0 | 2 | 0 | 67% |
| 2026-05-28 | 207 | 8 | 199 | 3.9% | 1 | 2 | 0 | 0 | 1 | 50% |
| 2026-05-29 | 205 | 5 | 200 | 2.4% | 0 | 4 | 0 | 0 | 0 | 80% |
| 2026-05-30 | 213 | 8 | 205 | 3.8% | 1 | 1 | 0 | 1 | 0 | 37.5% |
| 2026-06-05 | 199 | 39 | 160 | 19.6% | 2 | 18 | 0 | 5 | 0 | 64.1% |
| 2026-06-06 | 198 | 6 | 192 | 3.0% | 1 | 3 | 0 | 0 | 0 | 66.7% |
| **2026-06-07** | **193** | **6** | **187** | **3.1%** | **0** | **4** | **0** | **2** | **0** | **100%** |

Batch 18's 6-new / 96.9%-dedup sits in the thin steady-state band (same as batch 17), but with a **100% signal rate** — the highest in 18 batches, driven by the Hims three-wedge surge + Ro Run-6 return with zero noise drawing in.

### Per-day rate — two consecutive clean 1-day-gap batches, opposite shapes

| Batch | Gap (days) | Total ads | Ads/day | Hims/day (copy/day) | OpenAI/day | Ro/day |
|---|---|---|---|---|---|---|
| 14 | 1 | 5 | 5.0 | 4.0 (3.0) | 0 | 0 |
| 15 | 1 | 8 | 8.0 | 1.0 (0) | 1.0 | 1.0 |
| 16 | 6 | 39 | 6.5 | 3.0 (1.33) | 0.33 | 0.83 |
| 17 | 1 | 6 | 6.0 | 3.0 (1.0) | 1.0 | 0 |
| **18** | **1** | **6** | **6.0** | **4.0 (4.0)** | **0** | **2.0** |

Batches 17 and 18 are **both clean 1-day-gap batches** and both gap-normalize to ~3-4 Hims/day, but the **copy composition is opposite**: batch 17 = 1 copy ad (Hair-Hybrids-only), batch 18 = 4 copy ads (3 wedges). This is the cleanest demonstration that **the per-day copy rate is NOT stable at the 1-day resolution** — the wedge mix rotates day-to-day, so no single 1-day batch defines a baseline copy rate. The surge-trough alternation operates at the daily scale (batch 17 trough → batch 18 surge).

## Open questions

- **Does Anthropic's 2026-05-11 cluster surface a 3rd ad past 2026-06-08?** Batch 18 is the 7th silent batch (overshoots the threshold count by two) but the cadence-prediction window closes ~06-08 — batch 19 (past that date) finally decides between "slow-cluster continues" and "cluster stalled at 2 ads."
- **Is the Hims wedge mix genuinely day-to-day random, or is there a hidden rotation pattern?** Two consecutive clean 1-day batches gave Hair-Hybrids-only (17) then three-wedge (18). More clean 1-day batches would show whether the rotation is stochastic or follows a wedge-cycling schedule.
- **Does OpenAI Cluster 4 (2026-05-22) ever reach 3+ ads, or is it stalled at 2?** Held at 2 across batches 16+17+18 (3 consecutive non-expansions) — the "stalled at 2 / irregular re-surface" reading is now mildly favored.
- **Does TryEden surface a 2nd ad, and does it ever ship static copy?** Five silent batches (14-18) after the first signal — cadence still unknown.

## Related

- [[competitor-ads-farm]] — eighteenth batch; 2nd genuine three-wedge Hims surge (after batch 14) at a clean 1-day gap inverting batch 17's Hair-Hybrids-only trough; Ro Run 6; OpenAI/Anthropic/Eden silent; 100% signal rate (new farm high)
- [[hims]] — 4 ads, ALL verbatim copy across 3 wedges (Wegovy + Hair Hybrids ×2 + Sex Rx Climax Control); Wegovy + Climax Control return after exactly 1 silent batch; dormant-not-closed in the strongest sense; cumulative 103 ads
- [[ro]] — 2 placeholders, RETURNS from batch-17 silence (Run 6); cumulative 17 ads, all placeholder-only
- [[openai]] — 0 new ads (first silence since batch 14); Cluster 4 holds at 2 (3rd consecutive); Cluster 3 stalled at 3/1 (23 days); cumulative 50 ads, 1 with copy
- [[anthropic]] — 0 new ads; 7th consecutive silence (12-18); prediction window closes ~06-08; hold the stall call to batch 19; cumulative 8 ads
- [[eden]] — TryEden 5th consecutive silence (14-18); no Eden noise this batch
- [[concepts/dtc-telehealth-ad-template]] — 2nd genuine three-wedge batch ships all three wedge instantiations verbatim at a clean 1-day gap; refines the batch-17 "Hair-Hybrids-only baseline" (wedge mix rotates day-to-day)
- [[concepts/compounded-drug-disclaimer]] — Wegovy + Hair Hybrids + Sex Rx Climax Control disclaimer blocks all ship verbatim; Climax Control disclaimer returns after 1 silent batch
- [[ads-digest-2026-06-06]] — seventeenth batch (the clean 1-day-gap Hair-Hybrids-only trough this batch inverts)

## Appears in

- Eighteenth entry in `wiki/sources/` for the competitor-ads farm. **Clean 1-day-gap batch (6 new, 96.9% dedup) — the SECOND consecutive clean 1-day-gap batch, and it INVERTS batch 17.** **[[hims]] runs a GENUINE THREE-WEDGE surge — the 2nd in the farm after batch 14** — 4 ads, ALL with verbatim copy: Wegovy GLP-1 verbatim (ID `1318231786944621` started 2026-06-05) — **Wegovy RETURNS after exactly 1 silent batch (17)** + Hair Hybrids verbatim ×2 (IDs `1006359278539108` started 2026-06-04 + `2795816404144725` started 2026-06-02) + **Sex Rx + Climax Control RETURNS** (ID `1533618474776489` started 2026-05-26, *"Introducing the 2-in-1 pill"* intro-word A/B variant) after exactly 1 silent batch (17). This is a **trough→surge alternation at the 1-day-gap resolution** — two consecutive clean 1-day batches give opposite pictures (batch 17 = 1 copy wedge / Hair-Hybrids-only vs batch 18 = 4 copy ads / 3 wedges) — **REFINING the batch-17 "genuine copy rate ~1 copy ad/day, Hair-Hybrids-only baseline" reading: that baseline does NOT hold even at 1-day resolution; the wedge mix rotates day-to-day; Wegovy + Sex Rx are dormant-not-closed in the strongest sense (silent exactly 1 batch, back the next).** Hims 4.0 copy/day — the most copy-dense 1-day-gap Hims batch in the farm. **[[ro]] RETURNS from batch-17 silence with 2 placeholders — Run 6** (IDs `1321326639352870` + `1002278945590232`). **[[openai]] SILENT — first since batch 14; Cluster 4 holds at 2 (3rd consecutive); Cluster 3 stalled at 3/1 (23 days); cumulative 50 ads / 1 with copy; lab-delta vs Anthropic 50/8 (~6.25x).** **[[anthropic]] 7th consecutive silence (12-18) — prediction window (~06-08) closes tomorrow; hold the stall call to batch 19.** **[[eden]] (TryEden) 5th consecutive silence (14-18).** **0 noise ads — 100% real-signal rate (6 of 6), a NEW FARM HIGH.** Henry Meds / Hampton / DealMachine — 18th consecutive batch no signal. Cumulative 103 Hims / 50 OpenAI / 8 Anthropic / 17 Ro / 1 Eden ads.
