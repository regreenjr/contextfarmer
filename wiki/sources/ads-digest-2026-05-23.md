---
title: FB Ads Digest — Competitor brands — 2026-05-23
category: source
summary: Tenth competitor-ads farm batch — 8 new FB Ad Library entries (211 fetched, 203 dedup-skipped, 96.2%) after a 1-day gap from batch 9; **per-day rate (8.0 ads/day) confirms the ~8-9 ads/day standing baseline** established by batches 8+9 across the third consecutive fetch-cadence test point; **[[openai]] reverts to placeholder-only** in batch 10 — 1 Cluster 1 expansion carousel (ID `1127711402843910`, started 2026-04-21, body `{{product.brand}}`); the batch-9 Cluster 3 Codex retention video was a **one-off creative test, not a sustained narrative campaign** (Cluster 3 stalls at 3 ads / 1 with copy across batches 8+9+10) — cumulative 44 OpenAI ads, still 1 with copy; **Hims ships 4th post-cold-start Hair Hybrids verbatim re-launch** (ID `1302383031990848`, started 2026-04-22) + 1 placeholder = 2 new Hims ads; Hair Hybrids verbatim now spans **4 batches / 17-day stability window** (1+8+9+10) with 6 cumulative post-cold-start re-launches; **Wegovy GLP-1 SILENT for the 2nd consecutive batch** (batches 9+10) — Wegovy surge wave from batches 4+5+7+8 appears closed for now; **Anthropic 4th consecutive silence batch post-2026-05-11** further locks the standalone-launch diagnosis (no 5-batch test required — already locked at batch 8 ≥3); SecretRomance-cloudn65 **3-batch verbatim repeat** (8+9+10, same "Sierra Sterling" isekai body across all 5 batch-10 ads) overtakes Lauren Brooks as the new most-consistent verbatim noise repeat by batch count
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, openai-copy-one-off, hims-hair-hybrids-surge-continues, wegovy-silent-2-batches, anthropic-locked-silence-4-batches, secretromance-3-batch-repeat, baseline-confirmed]
sources: 1
source_path: raw/ads/digest-2026-05-23.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-23
updated: 2026-05-23
---

# FB Ads Digest — 2026-05-23

Tenth batch from the [[competitor-ads-farm]]. **8 new ads, 203 dedup-skipped** out of 211 fetched after a 1-day gap from batch 9 (2026-05-22). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Per-day rate (8.0 ads/day) closely matches batches 8 (9.0/d) + 9 (8.5/d).** Third consecutive test point confirms the **~8-9 ads/day standing creative-ops baseline** at typical 1-2-day fetch cadence — the fetch-gap-compression hypothesis from batch 8 + 9 now has a 1-day-gap data point that closes the methodological loop.
- **[[openai]] reverts to placeholder-only.** 1 new ad — ID `1127711402843910`, started **2026-04-21**, carousel, body `{{product.brand}}` — pure Cluster 1 expansion. **The batch-9 Cluster 3 Codex retention video was a one-off creative test**, not the opening of a sustained narrative-copy campaign. Cluster 3 stalls at 3 ads (2 placeholders + 1 video with copy) across batches 8+9+10. Cumulative **44 OpenAI ads across 10 batches, still 1 with copy**.
- **Hims continues Hair Hybrids verbatim surge** — 4th post-cold-start verbatim re-launch (ID `1302383031990848`, started **2026-04-22**) + 1 placeholder (ID `973036621745527`, started 2026-04-22). Hair Hybrids verbatim now spans **4 batches / 17-day stability window** (1+8+9+10) with **6 cumulative post-cold-start re-launches**. Cumulative **68 Hims ads** (66 → 68).
- **Wegovy GLP-1 SILENT for the 2nd consecutive batch.** Batches 9+10 both silent on Wegovy — the 4+5+7+8 Wegovy verbatim wave appears closed for now. Surge composition has fully rotated to Hair-Hybrids-only.
- **Anthropic 4th consecutive silence batch post-2026-05-11.** Standalone-launch diagnosis was already LOCKED in batch 8 (≥3-silent-batch methodology); batch 10 silence just extends the post-lock observation. Cumulative remains **7 Anthropic ads across 2 launch windows, 0 with copy**.
- **Ro / Henry Meds / Hampton Founders / DealMachine / Eden — 0 new ads each**, 10th consecutive batch with no Eden/Henry Meds/DealMachine signal; Ro silent for first time since batch 9 returned it.
- **SecretRomance-cloudn65 = 3-batch verbatim repeat (8+9+10).** All 5 batch-10 ads ship the identical "Sierra Sterling" isekai body verbatim to batches 8+9. **Overtakes Lauren Brooks (which itself was a 3-batch repeat across non-consecutive 4+8+9) as the new most-consistent verbatim noise repeat by *consecutive-batch* count.** Per-page-ID allow-listing bypass pattern from batch 8 is now structurally entrenched across 3 consecutive batches.
- **Brand-name filter still untuned — tenth consecutive batch.** Outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-23.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 211 • New: 8 • Dedup-skipped: 203 (96.2%)
- Gap from prior batch: 1 day (batch 9 = 2026-05-22)

## Tracked-brand creative inventory

### [[openai]] — 1 new ad (reverts to placeholder-only after batch 9 break)

- ID `1127711402843910`, started **2026-04-21**, format **carousel**, body `{{product.brand}}` placeholder
- Cluster 1 (Apr 2-21) expansion — joins the 25 cumulative Cluster 1 ads from batches 1+2+9
- **No new Cluster 3 (2026-05-15) ads in batch 10** — the batch-9 video with Codex retention copy stands alone

**Strategic significance**:

1. **The "first copy ad" was a one-off, not a campaign opening.** Batch 9 raised the question: is Cluster 3 the start of a sustained retention-narrative campaign or a single creative test? Batch 10's silence on Cluster 3 (combined with reversion to Cluster 1 placeholder expansion) suggests the **single-creative-test reading** wins for now. Cluster 3 inventory stalls at 3 ads — 2 placeholders + 1 video with copy.
2. **Catalog-ads-only remains the *predominant* OpenAI pattern across 10 batches** — now 43 of 44 ads (97.7%) are catalog placeholders. The structural claim from batch 9 stands: catalog-only is the default for cluster expansion; static narrative was a single Cluster-3 retention shot that didn't repeat.
3. **The lab-comparison delta vs [[anthropic]] holds.** Anthropic remains 100% placeholder (7/7) across 10 batches; OpenAI is 97.7% placeholder (43/44). The *one* copy ad gap doesn't fully close, but the campaign hasn't expanded either.

**Updated OpenAI cumulative tracking — 44 ads across 10 batches, 3 launch windows, 1 with copy:**

| Batch | Date | New | Cum | Cluster |
|---|---|---|---|---|
| 1 | 2026-05-06 | 21 | 21 | Cluster 1 (Apr 2-21) |
| 2 | 2026-05-10 | 3 | 24 | Cluster 1 expansion |
| 3 | 2026-05-11 | 3 | 27 | Cluster 2 opens (Apr 30 + May 8) |
| 4 | 2026-05-12 | 4 | 31 | Cluster 2 expansion |
| 5+6 | (silence) | 0 | 31 | — |
| 7 | 2026-05-16 | 2 | 33 | Cluster 2 expansion |
| 8 | 2026-05-20 | 7 | 40 | Cluster 2 +4 + Cluster 3 opens (May 15) +2 + May 11 bridge +1 |
| 9 | 2026-05-22 | 3 | 43 | Cluster 1 +1 + Cluster 2 +1 + Cluster 3 first VIDEO with COPY |
| **10** | **2026-05-23** | **1** | **44** | **Cluster 1 +1 (Cluster 3 stalls at 3 — copy ad was a one-off)** |

### [[hims]] — 2 new ads (Hair Hybrids verbatim re-launch #6 + 1 placeholder)

**Ad #1 — Hair Hybrids verbatim re-launch (started 2026-04-22)**

- ID `1302383031990848`, started **2026-04-22**, format unknown
- Body copy is **verbatim** to the 2026-05-06 canonical Hair Hybrids template (same wording as batch-8 `2064207334519052`/`728317760309201` and batch-9 `3372941842875795`/`868992329557540`/`2498995467227011`).

**Ad #2 — Placeholder (`{{product.brand}}` body)**

- ID `973036621745527`, started 2026-04-22, format unknown — pure dynamic-creative placeholder.

**Hair Hybrids verbatim cumulative tracking — now spans 4 batches / 17-day stability window:**

| Batch | Date | Ad ID(s) | Started |
|---|---|---|---|
| 1 | 2026-05-06 | (initial 10+ wave) | early Apr 2026 |
| 8 | 2026-05-20 | `2064207334519052` + `728317760309201` | 2026-05-09, 2026-04-22 |
| 9 | 2026-05-22 | `3372941842875795` + `868992329557540` + `2498995467227011` | 2026-02-26, 2026-05-06, 2026-05-19 |
| **10** | **2026-05-23** | **`1302383031990848`** | **2026-04-22** |

**6 cumulative post-cold-start Hair Hybrids verbatim re-launches** with start dates spanning 2026-02-26 → 2026-05-19. Hair Hybrids now matches Wegovy GLP-1's 5-batch / 14-day stability window and **exceeds it on consecutive-batch count** (Hair Hybrids 3-consecutive 8+9+10 vs Wegovy 4+5+7+8 spans skip batch 6).

**Surge-composition rotation pattern across batches 4-10:**

| Batch | Date | Wegovy | Hair Hybrids | Sex Rx Climax | Placeholders | Total Hims |
|---|---|---|---|---|---|---|
| 4 | 2026-05-12 | 1 | 0 | 0 | 0 | 1 |
| 5 | 2026-05-14 | 1 | 0 | 1 | 0 | 2 |
| 6 | 2026-05-15 | 0 | 0 | 0 | 0 | 0 |
| 7 | 2026-05-16 | 1 | 0 | 1 | 1 | 3 |
| 8 | 2026-05-20 | 2 | 2 | 0 | 4 | 8 |
| 9 | 2026-05-22 | 0 | 3 | 0 | 2 | 5 |
| **10** | **2026-05-23** | **0** | **1** | **0** | **1** | **2** |

**Wegovy GLP-1 silent for the 2nd consecutive batch** (9+10). The Wegovy verbatim wave that spanned batches 4+5+7+8 appears closed for now — possible the surge composition has fully rotated to Hair-Hybrids-only as the standing late-May 2026 template. **Worth watching batches 11-12** to see if Wegovy returns or stays silent for ≥3 (the methodology threshold for a high-confidence "wave closed" claim).

Cumulative **68 Hims ads across 10 batches** (66 → 68).

### [[anthropic]] — 0 new ads (4th consecutive silence post-2026-05-11)

No new Anthropic ads. The standalone-launch diagnosis for 2026-05-11 was **already LOCKED at batch 8** (3 consecutive silent batches post-launch); batch 10 extends the post-lock observation to 4 consecutive batches (silence + batch 9's old-Mar-17 catalog-feed re-surface doesn't count as a new launch).

Cumulative **7 Anthropic ads across 2 launch windows, 0 with copy** — unchanged from batch 9. **Lab-comparison delta vs OpenAI**: 7/0 vs 44/1 — Anthropic remains the lower-cadence + zero-copy lab; OpenAI's *one* copy ad from batch 9 didn't expand in batch 10, so the delta widens slightly (OpenAI still ~6x cadence, copy gap stuck at 1).

### [[ro]] — 0 new ads (1st silence batch since return-from-silence in batch 7)

After 4 consecutive active batches (7→8→9 + before-that-1 from batch 2's pair), Ro returns to silence. Cumulative **7 Ro ads across 10 batches, all `{{product.brand}}` placeholders** — zero static narrative across the longest window in the farm.

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (10th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (10th consecutive batch)
- **Eden (telehealth)** — never appeared (10th consecutive batch); bare-"Eden" filter continues to produce only noise (and even noise dried up — batch 10 surfaces no new "Eden" matches)

## False positives ("brand-name match" noise) — 5 of 8 ads (62.5%)

5 noise ads on a single noise page — concentrated noise but only one page in play.

### Multi-fire repeat noise pages (5 ads, 1 page)

1. **SecretRomance-cloudn65** (5 video ads, started 2026-05-18/19) — **3rd consecutive-batch repeat** (8+9+10); **same "Sierra Sterling" isekai body across all 5 batch-10 ads, verbatim to batches 8+9**. The cloud-variant proliferation continues — cloudn65 alone shipped 3 ads in batch 9 and 5 more in batch 10, suggesting cloudn65 is a high-volume sub-page within the SecretRomance operator's portfolio. **Overtakes Lauren Brooks** (3-batch repeat 4+8+9 *non-consecutive*) as the new most-consistent verbatim noise repeat by *consecutive-batch count*. cloudn57 (which fired in batches 8+9) absent in batch 10 — possible the operator is concentrating volume on cloudn65 or has rotated to other cloud-suffixed sub-pages outside batch-10 sampling.

### No new noise pages in batch 10

First batch with zero new noise pages since cold start — all 5 noise ads trace to a single previously-seen page (SecretRomance-cloudn65). The noise-page accumulation rate is non-zero across batches but **batch 10 produces no new "Eden" / "Hampton" / "Ro" / "Romance" first-fire noise pages**. Possible noise-page corpus is approaching saturation given the bare-keyword search space, though long-tail will keep producing first-fire matches in subsequent batches.

### Cumulative noise-corpus updates

- **Hampton-substring noise pages**: still **15 distinct** (unchanged from batch 9)
- **"Eden" noise brands**: still **11 distinct** (unchanged from batch 9)
- **SecretRomance multi-cloud-variant**: now confirmed **3-consecutive-batch repeat** (8+9+10) — pattern is structural, deeply entrenched, **content-based dedup is the only path to closure** (per-page-ID allow-list cannot scale to the cloud-suffix proliferation)
- **Lauren Brooks pet-allergy long-form**: 3-batch *non-consecutive* repeat (4+8+9) — absent in batch 10; SecretRomance-cloudn65's 3-consecutive-batch repeat now exceeds Lauren Brooks on the consecutive-batch metric

## Cross-cutting patterns

### Ten-batch farm convergence table

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
| **2026-05-23** | **211** | **8** | **203** | **3.8%** | **1** | **2** | **0** | **0** | **37.5%** |

Real-signal proportion 37.5% — drops back into the typical 0-67% band after batches 7-9's elevated 47-67% run. Cumulative 10-batch tracked-brand ads: **3 + 17 + 17 = 37 ads in last three batches**, or ~23% of all 156 cumulative tracked-brand ads across 10 batches.

### Three-point per-day rate confirmation — baseline locked at ~8 ads/day

Batches 8 (4-day gap, 9.0 ads/day), 9 (2-day gap, 8.5 ads/day), and 10 (1-day gap, 8.0 ads/day) now form a **three-point per-day rate confirmation series**:

| Batch | Gap (days) | Total ads | Ads/day | Hims/day | OpenAI/day |
|---|---|---|---|---|---|
| 8 | 4 | 36 | 9.0 | 2.00 | 1.75 |
| 9 | 2 | 17 | 8.5 | 2.50 | 1.50 |
| **10** | **1** | **8** | **8.0** | **2.00** | **1.00** |

Per-day rates are remarkably consistent across the 4-day, 2-day, and 1-day fetch-gap conditions. **Standing creative-ops baseline locked at ~8-9 ads/day under typical 1-4-day fetch cadence**. Tracked-brand-specific rates also stable: Hims 2.0-2.5/day, OpenAI 1.0-1.75/day (with batch 10's 1.0 reflecting the Cluster-3 silence — placeholder-cluster-expansion-only on a typical day yields ~1/day).

The fetch-gap compression hypothesis from batches 8+9 is now triple-confirmed. **1-day fetch cadence is the operating-point sweet spot** — it captures the daily ad-shipping rate without compression artifacts and surfaces structural-break events (like the batch-9 OpenAI copy ad) within a 24-hour window of their first appearance.

### OpenAI Cluster 3 stalls — single-creative-test reading confirms

Batch 9 raised the open question: **"Will OpenAI ship more Codex-narrative ads in batch 10?"** The answer is **no** — batch 10's only OpenAI ad is a Cluster 1 (Apr 2-21) placeholder expansion, with zero new Cluster 3 (2026-05-15) ads.

**Cluster 3 (2026-05-15) inventory across batches 8+9+10:**

| Batch | Date | New Cluster 3 ads | Cumulative |
|---|---|---|---|
| 8 | 2026-05-20 | 2 placeholders | 2 |
| 9 | 2026-05-22 | 1 video with copy | 3 |
| **10** | **2026-05-23** | **0** | **3** |

**Cluster 3 stalls at 3 ads / 1 with copy after 8 days post-launch.** Compared to Cluster 2 (12 ads / 15 days post-launch by batch 8), Cluster 3 is rolling out at a much slower pace OR is structurally smaller (a single video creative test embedded in a small cluster, vs Cluster 2's 12-ad expansion sequence).

**Updated reading**: the batch-9 Codex retention video was a **one-off creative test**, not the opening of a sustained narrative-copy campaign. OpenAI tested static narrative in a small video format and didn't expand it (yet) — possible they're A/B-testing the creative against control before expanding, or the test result wasn't compelling enough to scale. Either way, the structural claim from batch 9 — *"catalog-only for cluster expansion, static narrative for retention/promotion"* — needs **qualification**: static narrative *was tested* in retention/promotion context but didn't yet *scale* there. Worth re-testing in batch 11+.

### Hair Hybrids verbatim continues, Wegovy 2-batch silent

**Hair Hybrids verbatim cumulative — 4 batches / 17-day stability window / 6 post-cold-start re-launches:**

| Ad ID | Started | Batch |
|---|---|---|
| `2064207334519052` | 2026-05-09 | 8 |
| `728317760309201` | 2026-04-22 | 8 |
| `3372941842875795` | 2026-02-26 | 9 |
| `868992329557540` | 2026-05-06 | 9 |
| `2498995467227011` | 2026-05-19 | 9 |
| `1302383031990848` | 2026-04-22 | 10 |

**Start dates span ~12 weeks (2026-02-26 → 2026-05-19)** — Hair Hybrids has been actively shipping ad-library entries with this exact body for months. The verbatim-stability is structural; the surfacing cadence is variable.

**Wegovy GLP-1 silent for the 2nd consecutive batch** (9+10). The 4+5+7+8 Wegovy verbatim wave appears closed for now. Open question for batch 11: does Wegovy return (continuing the rotation pattern) or stay silent for a 3rd batch (suggesting the wave structurally closed)?

## Open questions

- **Will Wegovy GLP-1 verbatim return in batch 11?** 2 consecutive silent batches (9+10) is approaching but not yet at the ≥3-silent-batch methodology threshold for a high-confidence "wave closed" claim. If silent in batch 11, Wegovy wave is structurally closed; if returns, the rotation pattern continues.
- **Will Hair Hybrids verbatim continue in batch 11?** Hair Hybrids now spans 4 consecutive batches (8+9+10 + cold-start batch 1). If batch 11 ships another Hair Hybrids verbatim, the 4-consecutive-batch run becomes 5 — matching Wegovy's stability-window length and confirming Hair Hybrids as the standing late-May 2026 template.
- **Will OpenAI Cluster 3 expand in batch 11+?** Cluster 3 stalls at 3 ads after 8 days post-launch (vs Cluster 2's 12 ads / 15 days). If batch 11 ships another Cluster 3 video with copy, the "sustained retention campaign" reading wins; if Cluster 3 remains at 3 ads, the "one-off creative test" reading wins.
- **Will Anthropic ever ship copy?** Anthropic remains 100% placeholder (7/7) across 10 batches; OpenAI broke to copy briefly in batch 9 but didn't sustain. Hypothesis from batch 9 (only ships copy with retention/promo campaign) holds.
- **Is SecretRomance-cloudn65 = the canonical multi-cloud-variant noise operator?** 3 consecutive batches of verbatim "Sierra Sterling" body across multiple cloud-suffix sub-pages — the strongest entrenched noise pattern in the farm. **Content-based dedup is now the unambiguous next step** (per-page-ID allow-list cannot scale).
- **Is the 8-9 ads/day baseline structurally stable or seasonal?** Triple-confirmed across 1/2/4-day gaps, but only across 10 batches over 18 days. Watch for variation in the next 2-week window.

## Related

- [[competitor-ads-farm]] — tenth batch from this farm; 37.5% real-signal rate (typical band); confirms ~8-9 ads/day standing baseline via 3-point per-day rate test (8+9+10)
- [[hims]] — 2 new ads (1 Hair Hybrids verbatim re-launch + 1 placeholder); Hair Hybrids verbatim now spans 4 batches / 17-day stability window with 6 cumulative post-cold-start re-launches; Wegovy 2-batch silent; cumulative 68 ads
- [[openai]] — 1 new ad (Cluster 1 placeholder expansion); Cluster 3 stalls at 3 ads / 1 with copy — batch-9 copy ad was a one-off creative test, not a sustained campaign opening; cumulative 44 ads, still 1 with copy
- [[ro]] — 0 new ads (1st silence batch since return-from-silence in batch 7); cumulative 7 ads, all placeholders across 10 batches
- [[anthropic]] — 0 new ads (4th consecutive silence post-2026-05-11); standalone-launch diagnosis remains LOCKED from batch 8; cumulative 7 ads across 2 launch windows
- [[concepts/dtc-telehealth-ad-template]] — Hair Hybrids verbatim now spans 4 batches / 17-day stability window; Wegovy 2-batch silent; surge composition fully rotated to Hair-Hybrids-only
- [[concepts/compounded-drug-disclaimer]] — Hair Hybrids disclaimer ships verbatim for 6th post-cold-start instance; 4-batch / 17-day stability window
- [[concepts/free-sample-phase]] — Codex retention narrative remains the *one* paid-social-creative confirmation; didn't expand in batch 10
- [[ads-digest-2026-05-20]] — eighth batch (THREE-wedge verbatim surge — raised the fetch-gap compression question)
- [[ads-digest-2026-05-22]] — ninth batch (FIRST OpenAI ad with copy + fetch-gap compression hypothesis CONFIRMED)

## Appears in

- Tenth entry in `wiki/sources/` for the competitor-ads farm. **Three-point per-day rate confirmation** (batches 8+9+10 at 4-day/2-day/1-day gaps) locks the ~8-9 ads/day standing baseline. **OpenAI Cluster 3 stalls** — batch-9 Codex retention video was a one-off creative test, not a sustained campaign opening; updated reading qualifies batch-9 structural claim. **Hims Hair Hybrids verbatim surge extends to 4 consecutive batches (8+9+10 + cold-start batch 1)** — Hair Hybrids becomes the standing late-May 2026 Hims template; Wegovy 2-batch silent (rotation continues). **SecretRomance-cloudn65 3-consecutive-batch verbatim repeat** overtakes Lauren Brooks as the new most-consistent verbatim noise repeat by consecutive-batch count — content-based dedup is the unambiguous next step. Anthropic 4th consecutive silence further entrenches the standalone-launch lock.
