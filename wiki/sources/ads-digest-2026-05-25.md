---
title: FB Ads Digest — Competitor brands — 2026-05-25
category: source
summary: Eleventh competitor-ads farm batch — 12 new FB Ad Library entries (213 fetched, 201 dedup-skipped, 94.4%) after a 2-day gap from batch 10; per-day rate (6.0 ads/day) drops modestly below the 8-9 ads/day baseline locked across batches 8+9+10 — first per-day-rate point outside the locked band; **Hims ships 2 placeholders, NO Hair Hybrids verbatim** (first Hair Hybrids silence after 3-consecutive-batch run 8+9+10) — Wegovy GLP-1 now **3rd consecutive silence batch (9+10+11)** crossing the ≥3-batch methodology threshold so the **Wegovy verbatim wave is now structurally CLOSED**; **Anthropic ships 1 new ad started 2026-05-11** (ID `1522847336238984`) — **BREAKS the "standalone launch" diagnosis** that batch 8 had LOCKED — the 2026-05-11 cluster is actually a slow-rolling 2-ad cluster with 14-day gap between ads (batch 5 surfacing + batch 11 surfacing) and 5 consecutive silent batches in between (6-10); **OpenAI 0 new ads — first OpenAI silence since batch 6** (5-batch active streak broken); **Ro 2nd consecutive silence (10+11)** parallels Wegovy 3-batch silence; SecretRomance-cloudn65 **4-consecutive-batch repeat (8+9+10+11)** extends the most-consistent verbatim noise repeat by another batch; cloudn57 **returns after batch-10 absence** (3-batch repeat 8+9+11 with 1-batch gap); Lauren Brooks **4-batch non-consecutive repeat** (4+8+9+11); **3 new first-fire noise pages** end the batch-10 zero-new-noise-pages anomaly — Eyebrow pencil (Vietnamese cosmetics, "Eyeb**ro**w" substring), Cholesterol Relief Community (NEW long-form barbershop Alzheimer's narrative, "Choleste**ro**l" substring, distinct from batch-8 Cholesterol Support Group), Robinhood ("**Ro**binhood" substring)
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, hims-hair-hybrids-silent, wegovy-wave-closed, anthropic-standalone-lock-broken, anthropic-slow-cluster-revealed, openai-silence-break, ro-2-batch-silent, secretromance-4-consecutive-batches, lauren-brooks-4-batch-repeat, new-noise-pages-resumed]
sources: 1
source_path: raw/ads/digest-2026-05-25.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-25
updated: 2026-05-25
---

# FB Ads Digest — 2026-05-25

Eleventh batch from the [[competitor-ads-farm]]. **12 new ads, 201 dedup-skipped** out of 213 fetched after a 2-day gap from batch 10 (2026-05-23). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Per-day rate (6.0 ads/day) drops modestly below the 8-9 ads/day baseline** locked across batches 8+9+10. First per-day-rate point outside the previously-locked band — could be a single-batch fluctuation or the beginning of a downward drift; one more batch needed before recalibrating. Tracked-brand-specific rates: Hims 1.0/day (vs 2.0-2.5/day prior baseline), OpenAI 0/day (broke from 1.0-1.75/day), Ro 0/day (matches 0-0.5/day baseline).
- **Hims ships 2 ads — BOTH placeholders, NO Hair Hybrids verbatim, NO Wegovy.** IDs `1472790238030901` (started **2026-05-13**) and `26739814575700138` (started **2026-05-22**), both with `{{product.brand}}` body. **First Hair Hybrids silence after the 3-consecutive-batch run (8+9+10)** — possible the Hair Hybrids surge wave is now closing too, mirroring the Wegovy pattern. **Wegovy 3rd consecutive silence batch (9+10+11)** — at the ≥3-batch methodology threshold, the **Wegovy verbatim wave is now structurally CLOSED**.
- **Anthropic ships 1 new ad — and BREAKS the "standalone launch" lock from batch 8.** ID `1522847336238984`, started **2026-05-11**, carousel `{{product.brand}}` placeholder. The 2026-05-11 launch is **NOT standalone** — it's a slow-rolling 2-ad cluster with **14-day gap between ads** (1 ad in batch 5 surfacing 3 days post-launch + 1 ad in batch 11 surfacing 14 days post-launch) and **5 consecutive silent batches in between (6-10)**. Updated reading: Anthropic's catalog feed re-surfaces ads from the original 2026-05-11 launch on much-longer cadence than OpenAI's clusters (OpenAI cluster 2 expanded across 9 days; Anthropic 2026-05-11 cluster expanded across 14 days with 5 silent batches between ads).
- **OpenAI 0 new ads — first OpenAI silence since batch 6 (2026-05-15).** 5-batch active streak (batches 7-10) breaks. Cluster 3 (2026-05-15) remains stalled at 3 ads / 1 with copy across batches 8+9+10. The one-off creative test reading from batch 10 is further locked.
- **Ro 0 new ads — 2nd consecutive silence (10+11).** Parallels Wegovy 3-batch silence — both surge-trough patterns now silent simultaneously.
- **Henry Meds / Hampton Founders / DealMachine / Eden — 0 new ads each**, 11th consecutive batch with no signal.
- **3 new first-fire noise pages** end the batch-10 zero-new-noise-pages anomaly: **Eyebrow pencil** (Vietnamese cosmetics, "Eyeb**ro**w" substring), **Cholesterol Relief Community** (long-form barbershop Alzheimer's narrative — distinct page from batch-8 Cholesterol Support Group; "Choleste**ro**l" substring), **Robinhood** ("**Ro**binhood" substring — first financial-app noise page).
- **SecretRomance-cloudn65 4-consecutive-batch repeat (8+9+10+11)** extends the most-consistent verbatim noise repeat by another batch. **cloudn57 returns after batch-10 absence** (3-batch repeat 8+9+11 with 1-batch gap) — the multi-cloud-variant operator confirms continuous activity, just with cloud-suffix rotation within each batch.
- **Lauren Brooks 4-batch non-consecutive repeat (4+8+9+11)** — verbatim "Please STOP buying allergy meds for your dog" body re-fires for the 4th time after batch-10 absence. Joins SecretRomance-cloudn65 as the highest-recurrence noise pages by total batch count (both at 4).
- **Brand-name filter still untuned — 11th consecutive batch.** Outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-25.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 213 • New: 12 • Dedup-skipped: 201 (94.4%)
- Gap from prior batch: 2 days (batch 10 = 2026-05-23)

## Tracked-brand creative inventory

### [[anthropic]] — 1 new ad (BREAKS standalone-launch lock from batch 8)

- ID `1522847336238984`, started **2026-05-11**, format **carousel**, body `{{product.brand}}` placeholder
- Same launch window as the batch-5 Anthropic ad (ID `1521217572752360`, started 2026-05-11, also placeholder)
- 14-day gap between ad surfacings within the same launch window; 5 consecutive silent batches in between (6-10)

**Strategic significance**:

1. **The "standalone launch" diagnosis from batch 8 is BROKEN.** Per the batch-7 ≥3-silent-batch methodology, batches 6+7+8 of silence post-2026-05-11 LOCKED the standalone-launch claim. Batch 11 now produces a new ad from the *same* 2026-05-11 launch window — proving the 2026-05-11 launch is NOT standalone, but a **slow-rolling 2-ad cluster** on a 14-day expansion cadence.
2. **Anthropic's catalog feed cadence is structurally slower than OpenAI's.** OpenAI Cluster 2 (May 8) expanded from 2 → 12 ads across 9 days of batches 3+4+7+8. Anthropic's 2026-05-11 cluster expanded from 1 → 2 ads across 14 days with 5 silent batches in between. **Cluster-level pacing for Anthropic is ~4-5x slower than OpenAI's**, consistent with their broader ~6x cadence delta on cumulative ad volume.
3. **Methodology revision implied**: the ≥3-silent-batch threshold for "standalone launch" claims may need to be **extended to ≥5 silent batches at typical 1-2-day fetch cadence**, or qualified to "≥3 silent batches AND no new launch-window-matching catalog ad in batch N+3+." The current threshold was correct for batch-9's OpenAI Cluster 3 stall diagnosis but premature for Anthropic's slower cadence.
4. **Anthropic remains 100% placeholder (8/8) across 11 batches.** OpenAI shipped 1 copy ad in batch 9 (Cluster 3 video, didn't expand in batch 10); Anthropic has never shipped copy. Lab-comparison delta on copy gap is now 1/0 unexpanded ads — Anthropic still the lower-cadence + zero-copy lab.

**Updated Anthropic cumulative tracking — 8 ads across 11 batches, 2 launch windows, 0 with copy:**

| Batch | Date | New | Cum | Launch window |
|---|---|---|---|---|
| 1 | 2026-05-06 | 5 | 5 | Mar 16 – Apr 8 (initial wave, 5 ads) |
| 2-4 | (silence) | 0 | 5 | — |
| 5 | 2026-05-14 | 1 | 6 | 2026-05-11 cluster opens (ad #1) |
| 6-8 | (silence trough) | 0 | 6 | — |
| 9 | 2026-05-22 | 1 | 7 | Mar 16 – Apr 8 wave re-surfaces (2026-03-17 ad via catalog) |
| 10 | 2026-05-23 | 0 | 7 | — |
| **11** | **2026-05-25** | **1** | **8** | **2026-05-11 cluster expands (ad #2 — BREAKS standalone-launch lock)** |

### [[hims]] — 2 new ads (BOTH PLACEHOLDERS — Hair Hybrids first silence after 3-batch run)

**Ad #1 — Placeholder (`{{product.brand}}` body)**

- ID `1472790238030901`, started **2026-05-13**, format unknown — pure dynamic-creative placeholder

**Ad #2 — Placeholder (`{{product.brand}}` body)**

- ID `26739814575700138`, started **2026-05-22**, format unknown — pure dynamic-creative placeholder

**No Hair Hybrids verbatim re-launches in batch 11.** Hair Hybrids verbatim spans batches 1+8+9+10 (3-consecutive-batch run 8+9+10); batch 11 silence is the **first post-cold-start Hair Hybrids silence batch**. Possible interpretations:

1. **Hair Hybrids wave entering the rotation cycle the Wegovy wave just completed** — surge composition rotates between wedges; Wegovy went 4+5+7+8 → silent 9+10+11 (now structurally closed at ≥3-batch threshold); Hair Hybrids could follow the same pattern (8+9+10 surge → silent batch 11+).
2. **Single-batch noise** — Hair Hybrids may return in batch 12+ since the run was only 3 batches and the methodology threshold for "wave closed" is ≥3 silent batches.
3. **Surge composition fully rotated to placeholder-only** — both Wegovy AND Hair Hybrids silent in batch 11 with only 2 placeholder ads shipping. Either an inventory-cycle trough or a structural pivot away from verbatim-template re-launches.

**Wegovy GLP-1 now 3rd consecutive silence batch (9+10+11)** — at the ≥3-batch methodology threshold, the **Wegovy verbatim wave is structurally CLOSED**. The 4+5+7+8 Wegovy surge wave (5-batch / 14-day stability window with 6 cumulative post-cold-start re-launches) is now confirmed closed for the immediate term.

**Surge-composition rotation pattern across batches 4-11:**

| Batch | Date | Wegovy | Hair Hybrids | Sex Rx | Placeholders | Total Hims |
|---|---|---|---|---|---|---|
| 4 | 2026-05-12 | 1 | 0 | 0 | 0 | 1 |
| 5 | 2026-05-14 | 1 | 0 | 1 | 0 | 2 |
| 6 | 2026-05-15 | 0 | 0 | 0 | 0 | 0 |
| 7 | 2026-05-16 | 1 | 0 | 1 | 1 | 3 |
| 8 | 2026-05-20 | 2 | 2 | 0 | 4 | 8 |
| 9 | 2026-05-22 | 0 | 3 | 0 | 2 | 5 |
| 10 | 2026-05-23 | 0 | 1 | 0 | 1 | 2 |
| **11** | **2026-05-25** | **0** | **0** | **0** | **2** | **2** |

**Batch 11 is the first all-placeholder Hims batch** since cold start — no verbatim template re-launches across any of the three wedges. Per-day rate (1.0/day) drops below the 2.0-2.5/day baseline locked across batches 8+9+10.

Cumulative **70 Hims ads across 11 batches** (68 → 70).

### [[openai]] — 0 new ads (first OpenAI silence since batch 6 / 5-batch active streak breaks)

No new OpenAI ads. Active streak (batches 7-10) breaks at 4 consecutive active batches. Cluster 3 (2026-05-15) remains stalled at 3 ads / 1 with copy across batches 8+9+10+11 (now 10 days post-launch with no new Cluster 3 ads) — the **one-off creative test reading from batch 10 is further locked**.

Cumulative **44 OpenAI ads across 11 batches, still 1 with copy** — unchanged from batch 10.

### [[ro]] — 0 new ads (2nd consecutive silence batch — 10+11)

After 4 consecutive active batches (7+8+9 + occasional prior signal), Ro is now 2 consecutive silent batches (10+11). Approaching but not at the ≥3-silent-batch methodology threshold for a "Ro creative pause" claim. Cumulative **7 Ro ads across 11 batches, all `{{product.brand}}` placeholders** — zero static narrative across the longest tracked window in the farm.

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (11th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (11th consecutive batch)
- **Eden (telehealth)** — never appeared (11th consecutive batch); bare-"Eden" filter remained silent of even noise in batch 11

## False positives ("brand-name match" noise) — 9 of 12 ads (75%)

Noise rate jumps back to 75% from batch 10's 62.5% — driven primarily by 6 repeat-page ads (cloudn65 + cloudn57 + Lauren Brooks at 2 each) and 3 new first-fire noise pages.

### Multi-fire repeat noise pages (6 ads, 3 pages)

1. **SecretRomance-cloudn65** (2 video ads, started 2026-05-19/20) — **4-consecutive-batch repeat** (8+9+10+11); same "Sierra Sterling" isekai body verbatim across all 4 batches. The most-consistent verbatim noise repeat in the farm by consecutive-batch count. Volume dropped 5 → 2 ads from batch 10 to batch 11 (cloud-suffix rotation effect — see below).

2. **SecretRomance-cloudn57** (2 video ads, started 2026-05-19/21) — **3-batch non-consecutive repeat** (8+9+11 with 1-batch gap in batch 10). Returns after batch-10 absence with the same "Sierra inherited a magical zoo" intro variant (slightly different from cloudn65's "Sierra Sterling woke up" opener — though body converges to identical "Sierra Sterling" passage by paragraph 3). **The multi-cloud-variant operator confirms continuous activity, just with cloud-suffix rotation within each batch** — cloudn65 alone in batch 10 (5 ads), both cloudn57 + cloudn65 in batch 11 (2 each), suggesting the operator distributes daily volume across the cloud-suffix portfolio in non-fixed ratios.

3. **Lauren Brooks** (2 image ads, both started 2026-05-18) — **4-batch non-consecutive repeat** (4+8+9+11 with 1-batch gap in batch 10). Verbatim "Please STOP buying allergy meds for your dog" body re-fires for the 4th time. **Joins SecretRomance-cloudn65 as the highest-recurrence noise pages by total batch count** (both at 4). The Apoquel + Cytopoint + Cyclosporine + Zenrelia treatment-failure cascade copy is now the most-recurring single-creative noise pattern in the farm by total batches.

### New first-fire noise pages (3 ads, 3 pages) — batch-10 zero-new-noise anomaly ends

1. **Eyebrow pencil** (1 video ad, started 2026-05-05) — Vietnamese-language cosmetics direct-response copy (eye liner pen). Substring root cause: **"Eyeb*ro*w"** contains "ro". Ships entirely in Vietnamese with `https://www.giaudungplus.com` checkout link, "+ Bảo Hành Lỗi 1 Đổi 1 Trong Vòng 15 Ngày" (warranty/exchange copy), 50% discount promotion. First Vietnamese-language noise ad in the farm. Suggests the bare-"Ro" filter matches *substring within English text* as well as *substring within non-English text* — the noise floor extends across languages.

2. **Cholesterol Relief Community** (1 image ad, started 2026-05-23) — Long-form barbershop Alzheimer's narrative ("I have been cutting the same man's hair every three weeks for twenty-six years, and last March he sat down in my chair and asked me, very politely, what my name was"). Substring root cause: **"Choleste*ro*l"** contains "ro". **Distinct page from batch-8 Cholesterol Support Group** — same substring root cause ("Cholesterol"), different page name, different narrative structure (barbershop Alzheimer's vs ICU-nurse statins-skepticism). Filed as long-form direct-response copy contrast pattern alongside Lauren Brooks and Cholesterol Support Group — third "Cholesterol" substring noise page in the farm, second narrative-storytelling category.

3. **Robinhood** (1 carousel ad, started 2026-05-06) — Financial app, "Get a new perk with your Robinhood Gold membership ($5/mo.)" placeholder copy. Substring root cause: **"*Ro*binhood"**. First financial-app noise page in the farm matched via "Ro." Joins Hero FinCorp (batch 8, Indian financial services) as the second financial-services noise page — financial-app vertical now distinctly visible in the bare-"Ro" noise corpus.

### Cumulative noise-corpus updates

- **Hampton-substring noise pages**: still **15 distinct** (unchanged from batches 9+10)
- **"Eden" noise brands**: still **11 distinct** (unchanged from batches 9+10)
- **"Ro" noise brands**: +3 new this batch (Eyebrow pencil + Cholesterol Relief Community + Robinhood) — bare-"Ro" noise corpus continues to grow most aggressively
- **SecretRomance multi-cloud-variant**: now confirmed **4-consecutive-batch repeat** (cloudn65) + 3-batch non-consecutive repeat (cloudn57); content-based dedup remains the unambiguous next step
- **Lauren Brooks pet-allergy long-form**: 4-batch non-consecutive repeat (4+8+9+11) — joins cloudn65 as highest-recurrence by total batch count
- **Non-substring noise events**: still 2 of 11 batches (18.2%) — Adobe Acrobat (batch 3) + Romance miniseries (batch 4)

## Cross-cutting patterns

### Eleven-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Ro | Real-signal % |
|---|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | 1 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | 2 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 0 | 23% |
| 2026-05-15 | 203 | 3 | 200 | 1.5% | 0 | 0 | 0 | 0 | 0% |
| 2026-05-16 | 208 | 9 | 199 | 4% | 2 | 3 | 0 | 1 | 67% |
| 2026-05-20 | 213 | 36 | 177 | 17% | 7 | 8 | 0 | 2 | 47% |
| 2026-05-22 | 208 | 17 | 191 | 8% | 3 | 5 | 1 | 1 | 59% |
| 2026-05-23 | 211 | 8 | 203 | 4% | 1 | 2 | 0 | 0 | 37.5% |
| **2026-05-25** | **213** | **12** | **201** | **5.6%** | **0** | **2** | **1** | **0** | **25%** |

Real-signal proportion 25% — drops back toward the typical 0-67% band low end after batches 7-10's elevated 37.5-67% run. Cumulative 11-batch tracked-brand ads: **0 + 2 + 1 + 0 = 3 ads in batch 11**, or 1.9% of all 159 cumulative tracked-brand ads across 11 batches.

### Per-day rate drops modestly below the 8-9 ads/day baseline

Batch 11's 6.0 ads/day is the **first per-day-rate point outside the 8-9 ads/day band** locked across batches 8 (9.0/d), 9 (8.5/d), and 10 (8.0/d). Possible interpretations:

1. **Single-batch fluctuation** — 6.0/day is only ~25% below the 8/day floor; could be normal weekly cadence variation (batch 11 spans 2026-05-23 → 2026-05-25 which includes a weekend day).
2. **Downward drift** — the baseline could be shifting if tracked brands are entering inventory-cycle troughs simultaneously (Hims surge composition rotated, Wegovy wave closed, Hair Hybrids silent for first time, OpenAI between clusters, Ro 2-batch silent).
3. **Multi-brand simultaneous trough** — Wegovy 3-batch silent + Hair Hybrids 1-batch silent + OpenAI 1-batch silent + Ro 2-batch silent suggests batch 11 captured a coordinated trough across all four highest-volume tracked brands. Per-day rate would naturally drop during such a trough.

**Per-day rate test across 4 fetch-gap conditions:**

| Batch | Gap (days) | Total ads | Ads/day | Hims/day | OpenAI/day |
|---|---|---|---|---|---|
| 8 | 4 | 36 | 9.0 | 2.00 | 1.75 |
| 9 | 2 | 17 | 8.5 | 2.50 | 1.50 |
| 10 | 1 | 8 | 8.0 | 2.00 | 1.00 |
| **11** | **2** | **12** | **6.0** | **1.00** | **0** |

Worth watching batches 12-13 to see if the 6.0/day rate is single-batch noise or the start of a downward drift. If batches 12+13 return to 8-9/day, batch 11 was noise; if they cluster around 6/day, the baseline has shifted.

### Anthropic standalone-launch diagnosis BROKEN — 2026-05-11 cluster is slow-rolling

The most structurally significant batch-11 finding. Per the batch-8 diagnosis:

- Batch 5 (2026-05-14): 1 ad started 2026-05-11
- Batches 6-8: 3 consecutive silent batches → ≥3-batch methodology threshold met → **standalone launch claim LOCKED**

Batch 11 produces a new 2026-05-11 ad (ID `1522847336238984`). This proves the 2026-05-11 launch is **NOT standalone** — it's a slow-rolling 2-ad cluster on a 14-day expansion cadence.

**Updated Anthropic cluster pacing:**

- **Mar 16 – Apr 8 wave** (cluster 1): 5 ads in cold-start batch + 1 catalog re-surface in batch 9 = 6 ads across ~70 days. Active expansion across ~24 days (Mar 16 → Apr 8); catalog re-surface 5+ months later in batch 9.
- **2026-05-11 cluster** (cluster 2): 1 ad in batch 5 + 1 ad in batch 11 = 2 ads across 14 days. Active expansion across 14 days with 5 silent batches in between ad surfacings.

**OpenAI vs Anthropic cluster pacing comparison** (within the 11-batch window):

| Lab | Cluster | Ads | Active span | Silent batches between ads |
|---|---|---|---|---|
| OpenAI | Cluster 2 (May 8) | 13 | 15 days | 2-3 max |
| OpenAI | Cluster 3 (May 15) | 3 | 8 days, stalled | 2-3 max |
| Anthropic | Mar 16-Apr 8 | 6 | ~24 days active expansion | varies (incl. cold-start single batch) |
| Anthropic | 2026-05-11 | 2 | 14 days | 5 silent batches |

**Cluster-level pacing for Anthropic is ~4-5x slower than OpenAI's.** The ≥3-silent-batch methodology threshold for "standalone launch" claims correctly identified OpenAI's Cluster 3 stall (3 ads / 8 days post-launch / no new Cluster 3 ads for ≥3 batches = stalled) but **was premature for Anthropic's slower cadence**.

**Methodology revision implied**: extend the threshold to **≥5 silent batches at typical 1-2-day fetch cadence** for Anthropic, or qualify to "≥3 silent batches AND no new launch-window-matching catalog ad in batch N+3." Conservatively: the standalone-launch claim should require either ≥5 silent batches OR an explicit cluster-expansion ad later disproving it (whichever comes first).

### Wegovy GLP-1 wave structurally CLOSED (3-batch silent threshold met)

Per the methodology threshold, the Wegovy verbatim wave is now structurally closed:

| Batch | Date | Wegovy verbatim re-launches |
|---|---|---|
| 4 | 2026-05-12 | 1 |
| 5 | 2026-05-14 | 1 |
| 6 | 2026-05-15 | 0 |
| 7 | 2026-05-16 | 1 |
| 8 | 2026-05-20 | 2 |
| 9-11 | 2026-05-22 to 2026-05-25 | 0 (3-batch silent) |

**The 4+5+7+8 Wegovy verbatim wave** (5-batch / 14-day stability window with 6 cumulative post-cold-start re-launches) is now confirmed closed. Hair Hybrids took over as the standing template across batches 8+9+10 — but batch 11's Hair Hybrids silence raises the question of whether Hair Hybrids is now entering the same closing pattern.

### Hair Hybrids first silence after 3-consecutive-batch run

Batch 11 Hair Hybrids silence is the **first silence after the 8+9+10 surge** — possible interpretations:

1. **Wave-closing pattern starting** — same shape as Wegovy 4+5+7+8 surge → silent 9-11; if Hair Hybrids silent across batches 11+12+13 it'll match Wegovy's pattern and "wave closed" will be confirmed
2. **Single-batch trough** — Hair Hybrids may return in batch 12+ since the run was only 3 consecutive batches (vs Wegovy's 5-batch / 14-day stability window before silence)
3. **Surge composition entirely rotating away from verbatim** — both Wegovy AND Hair Hybrids silent simultaneously with only 2 placeholder ads shipping suggests the standing template-stability pattern from batches 8-10 may be ending

Worth watching batches 12-13 to distinguish.

### OpenAI first silence since batch 6 + 5-batch active streak breaks

OpenAI silence in batch 11 ends the 5-batch active streak (7+8+9+10). Cluster 3 (2026-05-15) further stalls at 3 ads / 1 with copy after 10 days post-launch. The one-off creative test reading from batch 10 strengthens — OpenAI tested static narrative in a single video at Cluster 3 launch but hasn't expanded it across 2 subsequent active batches (10+11) and now sits silent.

## Open questions

- **Is the 6.0 ads/day rate single-batch noise or a downward drift?** Batches 12-13 will distinguish. If they cluster around 8-9/day, batch 11 was noise; if around 6/day, baseline has shifted.
- **Will Hair Hybrids return in batch 12+?** Batch 11 was the first Hair Hybrids silence after the 3-consecutive-batch run. ≥3 silent batches needed to claim Hair Hybrids wave closed; ≥1 return ad in batches 12-13 keeps the wave open.
- **Will Anthropic continue the 2026-05-11 slow-cluster expansion?** If batch 12+ surfaces another 2026-05-11 ad, the slow-cluster reading is confirmed; if Anthropic returns to silence for 5+ batches, the 2026-05-11 cluster may have stalled at 2 ads.
- **What's the right methodology threshold for Anthropic standalone-launch claims?** Batch 11 disproved the ≥3-batch threshold for Anthropic. Conservative revision: ≥5 silent batches AND no new launch-window-matching catalog ad in the same period.
- **Does the OpenAI silence batch 11 mark a between-cluster pause or campaign exhaustion?** If a new OpenAI launch cluster opens in batches 12-13 (start date > 2026-05-15), campaign cadence continues; if silence persists 3+ batches, OpenAI may have paused FB catalog spend.
- **Is the SecretRomance cloud-suffix rotation predictable?** Cloudn65 was solo in batch 10, both cloudn65 + cloudn57 in batch 11. Watch batches 12+ for whether the operator runs both consistently or rotates.
- **Will the bare-"Ro" filter ever surface a new tracked-brand-relevant page?** 11 consecutive batches with no Roman Health / Ro Body / Ro Health page name surfacing. The filter tuning action item is now ~3 weeks overdue.

## Related

- [[competitor-ads-farm]] — eleventh batch from this farm; 25% real-signal rate (low end of typical band); 6.0 ads/day per-day rate drops below the 8-9 baseline locked by batches 8+9+10
- [[hims]] — 2 new ads (both placeholders, NO Hair Hybrids verbatim, NO Wegovy); first all-placeholder Hims batch since cold start; Hair Hybrids first silence after 3-batch run; Wegovy wave structurally CLOSED at 3-batch silent threshold; cumulative 70 ads
- [[openai]] — 0 new ads (first silence since batch 6 / 5-batch active streak breaks); Cluster 3 stalls at 3 ads / 1 with copy after 10 days post-launch; cumulative 44 ads, still 1 with copy
- [[anthropic]] — 1 new ad started 2026-05-11; **BREAKS the standalone-launch lock from batch 8**; 2026-05-11 is actually a slow-rolling 2-ad cluster with 14-day expansion cadence; methodology revision implied (≥5 silent batches for Anthropic standalone-launch claims); cumulative 8 ads across 2 windows
- [[ro]] — 0 new ads (2nd consecutive silence batch — 10+11); cumulative 7 ads, all placeholders across 11 batches
- [[concepts/dtc-telehealth-ad-template]] — Hair Hybrids first silence after 3-batch run; Wegovy wave structurally closed; batch 11 is first all-placeholder Hims batch since cold start
- [[concepts/compounded-drug-disclaimer]] — Hair Hybrids disclaimer silent for first time after 3-consecutive-batch run; Wegovy disclaimer 3-batch silent now confirmed wave closure
- [[concepts/free-sample-phase]] — Codex retention narrative stalled at 1 ad across batches 9+10+11; one-off creative test reading further locked
- [[ads-digest-2026-05-22]] — ninth batch (FIRST OpenAI ad with copy)
- [[ads-digest-2026-05-23]] — tenth batch (per-day rate baseline LOCKED at 8-9/day; batch-9 copy ad confirmed one-off)

## Appears in

- Eleventh entry in `wiki/sources/` for the competitor-ads farm. **Anthropic 2026-05-11 standalone-launch lock BROKEN** — proves cluster is slow-rolling 2-ad cluster on 14-day expansion cadence; methodology revision implied (Anthropic clusters need ≥5-batch threshold, not ≥3). **Wegovy verbatim wave structurally CLOSED** at 3-consecutive-silent-batch threshold (9+10+11). **Hair Hybrids first silence after 3-batch run (8+9+10)** — wave may be entering same closing pattern as Wegovy. **OpenAI first silence since batch 6** — Cluster 3 further stalled. **Per-day rate (6.0/day) drops below the 8-9/day baseline** locked by batches 8+9+10 — first per-day point outside the band; single-batch noise vs downward drift needs batches 12-13 to distinguish. **SecretRomance-cloudn65 4-consecutive-batch repeat** + Lauren Brooks 4-batch non-consecutive repeat = joint highest-recurrence noise pages. 3 new first-fire noise pages (Eyebrow pencil + Cholesterol Relief Community + Robinhood) end the batch-10 zero-new-noise anomaly.
