---
title: FB Ads Digest — Competitor brands — 2026-05-26
category: source
summary: Twelfth competitor-ads farm batch — 6 new FB Ad Library entries (207 fetched, 201 dedup-skipped, 97%) after a 1-day gap from batch 11; **per-day rate (6.0 ads/day) matches batch 11's 6.0/day exactly** — second consecutive batch outside the 8-9 ads/day baseline (locked across batches 8+9+10), promoting the downward-drift hypothesis from "single-batch noise" to "two-point trend"; **all 6 ads are pure `{{product.brand}}` placeholders** — first all-placeholder batch in the farm where no static narrative ships from ANY source (tracked or noise); **[[ro]] RETURNS after 2-batch silence (10+11)** with 2 placeholders (started 2026-04-14, 2026-05-19) — 2nd non-cold-start multi-ad Ro batch, structurally identical to batch 8's 2-ad surge; **[[hims]] drops to 1 placeholder** (started 2026-05-22) — lowest-volume Hims batch in 12 batches outside silence batches (3+6); Wegovy 4-batch silent (9+10+11+12) extending the structurally-closed wave; **Hair Hybrids 2nd consecutive silence (11+12)** — approaching ≥3-batch threshold for "wave-closed" claim; **[[openai]] RETURNS after 1-batch silence** with 1 Cluster 2 expansion (started 2026-05-08, ID `852088814627491`) — Cluster 2 now at 14 ads / 18 days post-launch + Cluster 3 still stalled at 3 ads / 11 days post-launch; **[[anthropic]] silent batch 12** — only 1 batch since the batch-11 slow-cluster expansion, can't yet confirm pattern; **Eden Munoz returns as multi-batch noise repeat** (2 carousel ads, started 2026-03-06 — same dates as batch 3 + batch 7 surfacings, banda singer matched via "Eden" substring) — Eden Munoz joins the multi-batch verbatim-noise repeat tier (cloudn65, Lauren Brooks); **real-signal rate jumps to 67%** (4 of 6 — Hims + 2 Ro + 1 OpenAI) — highest signal rate in any batch since batch 7's 67% (the previous high)
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, all-placeholder-batch, downward-drift-confirmed, ro-returns-from-silence, hims-1-ad-low, wegovy-4-batch-silent, hair-hybrids-2nd-silence, openai-cluster2-expansion-continues, eden-munoz-multi-batch-noise, signal-rate-67]
sources: 1
source_path: raw/ads/digest-2026-05-26.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-26
updated: 2026-05-26
---

# FB Ads Digest — 2026-05-26

Twelfth batch from the [[competitor-ads-farm]]. **6 new ads, 201 dedup-skipped** out of 207 fetched after a 1-day gap from batch 11 (2026-05-25). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Per-day rate (6.0 ads/day) EXACTLY matches batch 11's 6.0/day** — second consecutive point outside the 8-9 ads/day baseline locked across batches 8+9+10. Per the batch-11 open question, this **promotes the downward-drift hypothesis from "single-batch noise" to "two-point trend"** — the new baseline appears to be **~6 ads/day** rather than 8-9/day. One more batch needed to lock the new baseline at high confidence; batch 13's per-day rate will decide.
- **First all-`{{product.brand}}`-placeholder batch in the farm** — every one of the 6 new ads (4 tracked + 2 Eden Munoz noise) is pure dynamic-creative placeholder copy. No static narrative ships from any source this batch (tracked or noise). Both [[ro]] and [[hims]] and [[openai]] catalog feeds are surfacing only `{{product.brand}}` body text; Eden Munoz ships `{{product.brand}}` placeholders too (matching its batches 3+7 pattern).
- **[[ro]] RETURNS after 2-batch silence (10+11)** with **2 new placeholder ads** — IDs `4371300236471571` (started **2026-04-14**, same launch date as the cold-start Ro ad in batch 1 → cluster re-surfaces 6 weeks later) and `1354726933169121` (started **2026-05-19**, mid-May cluster). 2nd non-cold-start multi-ad Ro batch — structurally identical to batch 8's 2-ad surge. The Ro cluster is **NOT structurally closed** at the ≥3-batch silent threshold; instead the 2-batch silence was a trough between catalog re-surface events.
- **[[hims]] drops to 1 ad — lowest-volume Hims batch outside silence** (started 2026-05-22, ID `1296851655896170`, placeholder). **Wegovy now 4-batch silent (9+10+11+12)** extending the structurally-closed wave further. **Hair Hybrids 2nd consecutive silence (11+12)** — approaching the ≥3-batch threshold for wave-closure; batch 13 silence would lock the Hair Hybrids wave as closed alongside Wegovy. The 11+12 sequence is the **first 2-consecutive-batch all-placeholder Hims run** in the farm.
- **[[openai]] RETURNS after 1-batch silence (batch 11)** with **1 Cluster 2 expansion carousel** (ID `852088814627491`, started **2026-05-08**, placeholder). Cluster 2 (May 8) now at **14 ads / 18 days post-launch** — slowest-cadence period yet for Cluster 2 (was 12 ads / 15 days at batch 8 = 0.8 ads/day, now 14 ads / 18 days = 0.78 ads/day across batches 8→12, near-identical pacing). Cluster 3 (May 15) **STILL stalled at 3 ads / 1 with copy** after 11 days post-launch — 3 consecutive active OpenAI batches (10+11+12, wait, batch 11 was silent...) ok, 2 consecutive active batches (10+12) without a new Cluster 3 ad. The one-off creative test reading from batch 10 holds.
- **[[anthropic]] 0 new ads in batch 12** — only 1 batch since the batch-11 slow-cluster expansion (which broke the "standalone launch" lock). Can't yet confirm whether the 2026-05-11 cluster continues to expand or stalled at 2 ads. Cumulative 8 ads across 2 launch windows.
- **Henry Meds / Hampton Founders / DealMachine — 0 new ads each**, 12th consecutive batch with no signal.
- **Eden Munoz returns as multi-batch noise repeat** (2 carousel ads, both started **2026-03-06** — a NEW launch date distinct from batch 3's 2026-01-13 ad and batch 7's 2026-05-08 ad) — banda singer matched via "Eden" substring. Eden Munoz now appears in batches 3 + 7 + 12 = **3-batch non-consecutive repeat** with a 5-batch gap (8-11). Joins cloudn65 (4-batch consecutive) and Lauren Brooks (4-batch non-consecutive) as multi-batch verbatim-noise repeats. **Each surfacing has been from a different launch-date cluster** (Jan 13 / May 8 / Mar 6) — confirming Eden Munoz runs multiple distinct catalog campaigns across the tracked window.
- **Real-signal rate jumps to 67%** (4 of 6 tracked: 2 Ro + 1 Hims + 1 OpenAI; vs 2 of 6 noise: 2 Eden Munoz). Ties batch 7's 67% as the highest signal rate in any batch since cold start.
- **Brand-name filter still untuned — 12th consecutive batch.** Outstanding action item from 2026-05-06; ~3 weeks overdue.

## Source

- Path: `raw/ads/digest-2026-05-26.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 207 • New: 6 • Dedup-skipped: 201 (97%)
- Gap from prior batch: 1 day (batch 11 = 2026-05-25)

## Tracked-brand creative inventory

### [[ro]] — 2 new ads (RETURNS after 2-batch silence; 2nd non-cold-start multi-ad batch)

**Ad #1 — Placeholder (`{{product.brand}}` body)**

- ID `4371300236471571`, started **2026-04-14**, format unknown — pure dynamic-creative placeholder
- **Same launch date as the cold-start Ro ad in batch 1** (`1848240979175501`, started 2026-04-14) — same 2026-04-14 launch window catalog re-surfaces ~6 weeks later

**Ad #2 — Placeholder (`{{product.brand}}` body)**

- ID `1354726933169121`, started **2026-05-19**, format unknown — pure dynamic-creative placeholder
- New mid-May cluster (closest start-date neighbors: batch 8's `2277114206027622` started 2026-05-14 + `2238568280301485` started 2026-05-08)

**Strategic significance**:

1. **Ro's 2-batch silence (10+11) was NOT wave closure — it was a trough between catalog re-surface events.** Cumulative pattern: active batches (1+2+7+8+9+12) → silent batches (3-6 + 10-11). Ro's catalog feed surfaces ads in irregular bursts rather than continuous cadence.
2. **Structurally identical to batch 8's 2-ad surge** — both batches deliver 2 placeholder ads with mixed launch dates spanning 2-6 weeks back. Pattern: Ro's catalog dynamic-creative cycles through ~3-5 distinct launch-date templates with non-fixed dedup-cache TTL.
3. **The 2026-04-14 launch window now confirmed as the canonical Ro template** — surfaces in batch 1 + batch 12 = 6+ weeks of catalog activity. Likely the steady-state Ro template that the placeholder catalog feed indexes.
4. **Per-day rate (1.0 Ro/day in batch 12) doubles the 0.5/day rate from batches 8+9** — Ro's cadence in batch 12 matches Hims (1.0/day) for the first time. Worth watching whether this is single-batch fluctuation or a structural pickup.

**Updated Ro cumulative tracking — 9 ads across 12 batches, ALL placeholders, 4 distinct active runs:**

| Batch | Date | New | Cum | Notes |
|---|---|---|---|---|
| 1 | 2026-05-06 | 1 | 1 | 2026-04-14 launch (cold-start) |
| 2 | 2026-05-10 | 2 | 3 | 2026-05-04, 2026-04-28 |
| 3-6 | (silent) | 0 | 3 | 4-batch trough |
| 7 | 2026-05-16 | 1 | 4 | 2026-05-04 re-surface |
| 8 | 2026-05-20 | 2 | 6 | 2026-05-14, 2026-05-08 |
| 9 | 2026-05-22 | 1 | 7 | 2026-04-28 re-surface |
| 10-11 | (silent) | 0 | 7 | 2-batch trough |
| **12** | **2026-05-26** | **2** | **9** | **2026-04-14 re-surface + 2026-05-19 new** |

### [[hims]] — 1 new ad (lowest-volume Hims batch outside silence; Wegovy 4-batch silent / Hair Hybrids 2nd silence)

**Ad #1 — Placeholder (`{{product.brand}}` body)**

- ID `1296851655896170`, started **2026-05-22**, format unknown — pure dynamic-creative placeholder

**No Wegovy verbatim re-launches in batch 12** — Wegovy now silent for batches 9+10+11+12 = **4-batch silent streak**, extending the structurally-closed wave from batch 11's ≥3-batch threshold (the wave is closed; this is just continued confirmation).

**No Hair Hybrids verbatim re-launches in batch 12** — Hair Hybrids now silent for batches 11+12 = **2-batch silent streak**, approaching but not at the ≥3-batch wave-closure threshold. Batch 13 silence would lock Hair Hybrids as closed.

**Surge-composition rotation pattern across batches 4-12:**

| Batch | Date | Wegovy | Hair Hybrids | Sex Rx | Placeholders | Total Hims |
|---|---|---|---|---|---|---|
| 4 | 2026-05-12 | 1 | 0 | 0 | 0 | 1 |
| 5 | 2026-05-14 | 1 | 0 | 1 | 0 | 2 |
| 6 | 2026-05-15 | 0 | 0 | 0 | 0 | 0 |
| 7 | 2026-05-16 | 1 | 0 | 1 | 1 | 3 |
| 8 | 2026-05-20 | 2 | 2 | 0 | 4 | 8 |
| 9 | 2026-05-22 | 0 | 3 | 0 | 2 | 5 |
| 10 | 2026-05-23 | 0 | 1 | 0 | 1 | 2 |
| 11 | 2026-05-25 | 0 | 0 | 0 | 2 | 2 |
| **12** | **2026-05-26** | **0** | **0** | **0** | **1** | **1** |

**Batch 11+12 is the first 2-consecutive-batch all-placeholder Hims run** in the farm — no verbatim template re-launches across any of the three wedges across 2 consecutive batches. Per-day rate (1.0/day) matches batch 11's 1.0/day — Hims's per-day rate has structurally dropped from the 2.0-2.5/day baseline locked across batches 8+9+10.

Cumulative **71 Hims ads across 12 batches** (70 → 71).

### [[openai]] — 1 new ad (RETURNS after batch-11 silence; Cluster 2 expansion continues 18 days post-launch)

**Ad #1 — Placeholder (`{{product.brand}}` body, carousel)**

- ID `852088814627491`, started **2026-05-08**, format carousel — pure dynamic-creative placeholder
- **Cluster 2 (May 8) expansion** — Cluster 2 now at 14 ads / 18 days post-launch

**Cluster 2 pacing across batches:**

| Batch | Date | Cluster 2 ads (cum) | Days post-launch | Ads/day |
|---|---|---|---|---|
| 3 | 2026-05-11 | 2 | 3 | 0.67 |
| 4 | 2026-05-12 | 6 | 4 | 1.50 |
| 7 | 2026-05-16 | 8 | 8 | 1.00 |
| 8 | 2026-05-20 | 12 | 12 | 1.00 |
| 9 | 2026-05-22 | 13 | 14 | 0.93 |
| 10 | 2026-05-23 | 13 | 15 | 0.87 |
| 11 | 2026-05-25 | 13 | 17 | 0.76 |
| **12** | **2026-05-26** | **14** | **18** | **0.78** |

Cluster 2 cadence settles at ~0.75-0.78 ads/day across 18 days — the longest-running cluster in OpenAI's tracked window. Cluster pacing has slowed from 1.0/day (batches 7-8) to 0.78/day (batch 12) but **remains active 18 days post-launch** with no signs of closure.

**Cluster 3 (May 15) remains stalled at 3 ads / 1 with copy** — 11 days post-launch, no new Cluster 3 ads across batches 10+11+12. The one-off creative test reading from batch 10 holds: OpenAI tested static narrative once at Cluster 3 launch but didn't scale it.

Cumulative **45 OpenAI ads across 12 batches, still 1 with copy** — unchanged copy-gap delta vs batch 11.

### [[anthropic]] — 0 new ads (batch 12 silence after batch-11 slow-cluster expansion)

No new Anthropic ads in batch 12. Only 1 batch has passed since the batch-11 slow-cluster expansion that broke the "standalone launch" diagnosis. Can't yet confirm whether the 2026-05-11 cluster continues to expand at the 14-day cadence (next expected expansion: ~2026-06-08 if the cadence holds) or stalled at 2 ads.

Cumulative **8 Anthropic ads across 12 batches, 0 with copy** — unchanged from batch 11.

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (12th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (12th consecutive batch)
- **Eden (telehealth)** — never appeared (12th consecutive batch); bare-"Eden" filter surfaced Eden Munoz banda-singer noise instead

## False positives ("brand-name match" noise) — 2 of 6 ads (33%)

Noise rate drops sharply from batch 11's 75% to 33% — driven by zero new first-fire noise pages and only one returning noise page (Eden Munoz). The all-placeholder format also strips out the long-form-narrative noise category that batch 11 had (Cholesterol Relief Community, Eyebrow pencil).

### Multi-fire repeat noise pages (2 ads, 1 page)

1. **Eden Munoz** (2 carousel ads, both started **2026-03-06**) — **3-batch non-consecutive repeat** (appears in batches 3 + 7 + 12, with 5-batch gap from batch 8 to 11). Same banda singer page matched via bare-"Eden" substring; both ads use `{{product.brand}}` placeholder body matching the catalog dynamic-creative format. **Each surfacing is from a different launch-date cluster**: batch 3 = started 2026-01-13, batch 7 = started 2026-05-08, batch 12 = started 2026-03-06 — confirming the page runs multiple distinct catalog campaigns. Joins SecretRomance-cloudn65 (4-consecutive-batch repeat) and Lauren Brooks (4-batch non-consecutive repeat) as the multi-batch verbatim-noise repeat tier. **Eden Munoz is the most-recurring "Eden" substring noise page** — most of the 11 "Eden" noise brands appeared in single batches, while Eden Munoz now has 3-batch recurrence.

### Cumulative noise-corpus updates

- **"Eden" noise brands**: still **11 distinct** (Eden Munoz already counted as #1 from batch 3)
- **Hampton-substring noise pages**: still **15 distinct** (unchanged across batches 9+10+11+12 — Hampton noise corpus appears stable)
- **"Ro" noise brands**: unchanged this batch (no new first-fire "Ro" noise — first batch since batch 10 with no new "Ro" noise page)
- **SecretRomance multi-cloud-variant**: silent in batch 12 (after 4-consecutive-batch run 8+9+10+11) — first SecretRomance silence batch since cold start
- **Lauren Brooks pet-allergy long-form**: silent in batch 12 (after 4-batch non-consecutive run 4+8+9+11) — both highest-recurrence verbatim noise pages silent simultaneously
- **Non-substring noise events**: still 2 of 12 batches (16.7%) — Adobe Acrobat (batch 3) + Romance miniseries (batch 4); no new non-substring noise this batch

## Cross-cutting patterns

### Twelve-batch farm convergence table

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
| 2026-05-25 | 213 | 12 | 201 | 5.6% | 0 | 2 | 1 | 0 | 25% |
| **2026-05-26** | **207** | **6** | **201** | **2.9%** | **1** | **1** | **0** | **2** | **67%** |

Real-signal proportion 67% — ties batch 7's 67% as the highest signal rate in any batch since cold start. The all-placeholder format strips out the long-form narrative noise category that typically drives noise rate up.

### Per-day rate downward-drift hypothesis PROMOTED to two-point trend

Batch 12's 6.0 ads/day **exactly matches** batch 11's 6.0/day — second consecutive point outside the 8-9 ads/day band locked across batches 8+9+10. Per the batch-11 open question, this promotes the hypothesis from "single-batch noise" to **"two-point trend"** — the new per-day baseline appears to be **~6 ads/day** rather than 8-9/day.

**Per-day rate test across 5 fetch-gap conditions:**

| Batch | Gap (days) | Total ads | Ads/day | Hims/day | OpenAI/day | Ro/day |
|---|---|---|---|---|---|---|
| 8 | 4 | 36 | 9.0 | 2.00 | 1.75 | 0.50 |
| 9 | 2 | 17 | 8.5 | 2.50 | 1.50 | 0.50 |
| 10 | 1 | 8 | 8.0 | 2.00 | 1.00 | 0 |
| 11 | 2 | 12 | 6.0 | 1.00 | 0 | 0 |
| **12** | **1** | **6** | **6.0** | **1.00** | **1.0** | **2.0** |

**Possible causes for the structural drop:**

1. **Hims verbatim-template waves closing in sequence** — Wegovy wave closed at batch 11 (≥3-batch silent); Hair Hybrids now 2-batch silent. The 8+9+10 surge composition has fully rotated to placeholder-only across batches 11+12. Hims's contribution to the overall per-day rate dropped from 2.0-2.5/day (batches 8-10) to 1.0/day (batches 11-12).
2. **OpenAI Cluster 2 cadence slowing** — Cluster 2 expansion dropped from 1.0/day (batches 7-8) to 0.78/day (batch 12). Cluster 3 stalled. OpenAI's contribution to the per-day rate dropped from 1.0-1.75/day (batches 8-10) to ~0.5/day (batches 11-12 average).
3. **Cumulative inventory-cycle trough** — multiple tracked brands simultaneously in lower-cadence phases.

If batch 13 also clusters at 6.0/day, the new baseline can be locked at high confidence; if it returns to 8-9/day, the downward drift is single-trough rather than structural.

### All-placeholder batch — first in the farm

Batch 12 is the **first batch in the farm where ALL ads (tracked + noise) are pure `{{product.brand}}` placeholders**. No static narrative shipped from any source. Notable interpretations:

1. **Confirms the catalog dynamic-creative format is the dominant ad surface for the farm's tracked brands** — when verbatim-template waves close (Wegovy + Hair Hybrids) and one-off narrative tests don't expand (OpenAI Cluster 3), what's left is catalog dynamic creative.
2. **Stripping out long-form narrative noise** — batch 11's biggest noise contributors (Cholesterol Relief Community, Eyebrow pencil) didn't return. The Apify actor's dedup cache is holding most long-form narrative noise.
3. **The all-placeholder pattern is brittle for teardown analysis** — when 100% of ads are `{{product.brand}}`, there's no copy to analyze. The farm's value-per-batch in batch 12 is structural (cadence patterns, cluster expansion) not content-based (no new teardown-able messaging).

### Hair Hybrids 2nd consecutive silence (11+12) — wave-closure threshold approached

Hair Hybrids verbatim re-launches across batches 1+8+9+10 (3-consecutive-batch run 8+9+10), then silent 11+12. Batch 13 silence would lock the Hair Hybrids wave as structurally closed at the ≥3-batch threshold — mirroring Wegovy's 9+10+11 closure pattern.

**Hair Hybrids vs Wegovy wave-closing comparison:**

| Wave | Surge batches | Surge span | Silent batches | Status at batch 12 |
|---|---|---|---|---|
| Wegovy | 4+5+7+8 (5-batch / 14-day stability) | 14 days | 9+10+11+12 (4-batch silent) | **CLOSED** at ≥3-batch threshold (batch 11) |
| Hair Hybrids | 1+8+9+10 (4-batch / 17-day stability) | 17 days | 11+12 (2-batch silent) | **APPROACHING** — needs batch 13 silence to close |

Hair Hybrids had a **slightly longer stability window than Wegovy** (17 days vs 14 days) before silence. If both close, all three Hims wedges (Wegovy GLP-1 + Hair Hybrids + Sex Rx) have moved into placeholder-only mode by mid-2026-05. **Sex Rx + Climax Control** wave also closed (last seen batch 7).

### Eden Munoz multi-batch verbatim-noise repeat (3-batch non-consecutive)

Eden Munoz now appears in batches 3 + 7 + 12 with a 5-batch gap from batch 8 to 11. **Joins the multi-batch verbatim-noise repeat tier** alongside SecretRomance-cloudn65 (4-consecutive-batch 8-11) and Lauren Brooks (4-batch non-consecutive 4+8+9+11). All three carry distinct cadence patterns:

- **cloudn65**: high-frequency consecutive (4-batch consecutive) → silent batch 12 (first silence)
- **Lauren Brooks**: high-frequency non-consecutive (4-batch with 1-batch gaps)
- **Eden Munoz**: low-frequency non-consecutive (3-batch with 4-5-batch gaps)

The cadence-pattern diversity confirms the bare-substring noise corpus contains multiple distinct ad-operator cadences — content-based dedup wouldn't be sufficient; per-page-ID allow-listing or substring-tuning is needed.

### Ro cluster cadence — 4 distinct active runs across 12 batches

Ro's catalog feed pattern: irregular bursts of 1-2 ads, separated by 1-4-batch troughs:

- **Run 1** (batches 1+2): 3 ads
- **Trough** (batches 3-6): 4-batch silence
- **Run 2** (batches 7+8+9): 4 ads
- **Trough** (batches 10-11): 2-batch silence
- **Run 3** (batch 12): 2 ads — current

Mean run length: ~2 batches, mean trough length: ~3 batches. The 2-batch silence (10+11) was within the typical range — not a wave-closure signal. The cluster-vs-wave distinction matters: Ro's catalog feed cycles rather than rises/falls.

## Open questions

- **Will the 6.0 ads/day rate lock as the new baseline?** Batch 13 will decide — if it clusters around 6/day, the new baseline is locked; if it returns to 8-9/day, the 2-batch drop was a structural-but-temporary trough.
- **Will Hair Hybrids return in batch 13 or stay silent?** Batch 13 silence would lock the Hair Hybrids wave as closed at the ≥3-batch threshold; ≥1 return ad keeps the wave open.
- **Does the 2026-05-11 Anthropic cluster expand to a 3rd ad?** If batch 13+ surfaces another 2026-05-11 ad, the slow-cluster reading holds; if Anthropic stays silent for 5+ batches, the cluster may have stalled at 2 ads.
- **Does OpenAI Cluster 3 ever expand?** 11 days post-launch with no new ads across batches 10+11+12 — the one-off creative test reading is now well-established but not yet permanent.
- **Will Ro's catalog cadence pick up to 1.0/day baseline or revert to 0.5/day?** Batch 12's 2-ad surge (1.0/day) doubles the batches 8+9 0.5/day rate; one more active batch needed to determine pattern.
- **Will Eden Munoz return in batch 13 or stay silent for another 4-5-batch trough?** The 3-batch non-consecutive repeat pattern (batches 3+7+12) implies the next expected surface is batch ~16-17 if the cadence holds.
- **Does the all-placeholder batch pattern become standing?** If batches 13+ also ship 100% placeholder ads, the farm's value shifts entirely to cluster-cadence pattern detection (vs content teardown).

## Related

- [[competitor-ads-farm]] — twelfth batch from this farm; 67% real-signal rate (ties batch 7's high); 6.0 ads/day per-day rate matches batch 11's 6.0 (two-point downward-drift trend)
- [[hims]] — 1 new ad (placeholder), lowest-volume Hims batch outside silence; Wegovy 4-batch silent; Hair Hybrids 2nd silence approaching wave-closure threshold; first 2-consecutive-batch all-placeholder Hims run; cumulative 71 ads
- [[openai]] — 1 new ad, RETURNS from batch-11 silence; Cluster 2 expansion continues 18 days post-launch (14 ads, 0.78/day); Cluster 3 still stalled at 3 ads / 1 with copy; cumulative 45 ads
- [[ro]] — 2 new ads (both placeholders), RETURNS after 2-batch silence (10+11); 2nd non-cold-start multi-ad batch; 2026-04-14 launch window confirmed as canonical Ro template (6+ weeks of catalog activity); cumulative 9 ads across 12 batches
- [[anthropic]] — 0 new ads; 1 batch since batch-11 slow-cluster expansion; can't yet confirm whether 2026-05-11 cluster continues; cumulative 8 ads across 2 launch windows
- [[concepts/dtc-telehealth-ad-template]] — Hair Hybrids 2nd consecutive silence; Wegovy 4-batch silent; first 2-consecutive-batch all-placeholder Hims run
- [[concepts/compounded-drug-disclaimer]] — both Hair Hybrids + Wegovy disclaimers silent for 2nd consecutive batch
- [[ads-digest-2026-05-23]] — tenth batch (per-day rate baseline LOCKED at 8-9/day)
- [[ads-digest-2026-05-25]] — eleventh batch (first per-day point at 6.0/day; downward drift hypothesis OPEN)

## Appears in

- Twelfth entry in `wiki/sources/` for the competitor-ads farm. **Per-day rate downward-drift hypothesis PROMOTED** from "single-batch noise" to "two-point trend" — batch 12's 6.0/day exactly matches batch 11's 6.0/day, both below the 8-9 baseline locked across batches 8+9+10. **First all-`{{product.brand}}`-placeholder batch in the farm** — every ad (tracked + noise) is pure dynamic creative. **Ro RETURNS after 2-batch silence with 2-ad surge** (2nd non-cold-start multi-ad batch); 2026-04-14 launch window confirmed as canonical Ro template (6+ weeks active). **Hims drops to 1 ad** (lowest outside silence batches 3+6); Wegovy 4-batch silent; Hair Hybrids 2nd silence approaching wave-closure threshold. **OpenAI returns from batch-11 silence** with Cluster 2 expansion (14 ads / 18 days at 0.78/day); Cluster 3 still stalled at 3 ads / 11 days post-launch. **Anthropic silent batch 12** — can't yet confirm slow-cluster continuation. **Eden Munoz joins multi-batch verbatim-noise repeat tier** (3-batch non-consecutive 3+7+12). Real-signal rate jumps to 67% — ties batch 7's high; the all-placeholder format strips long-form narrative noise.
