---
title: FB Ads Digest — Competitor brands — 2026-05-20
category: source
summary: Eighth competitor-ads farm batch — 36 new FB Ad Library entries (213 fetched, 177 dedup-skipped, 83%) after a 4-day gap from batch 7; highest-volume tracked-brand signal since cold start (17 of 36 ads = 47% signal) — **Hims runs a THREE-wedge verbatim surge** in one batch (Wegovy GLP-1 verbatim #5 across 2 ads + Hair Hybrids verbatim re-launch across 2 ads + 4 placeholders); Wegovy GLP-1 template now verbatim across **5 batches / 14-day stability window** (longest single-template-stability window in the vault); Hair Hybrids template re-launches verbatim for first time since cold start (2026-05-06); **OpenAI ships 7 new ads — May 8 cluster expands 8 → 12 (cluster-2 disprovingly still rolling out 12 days post-launch) + 2 new 2026-05-15 ads (cluster 3 opens) + 1 new 2026-05-11 ad** — biggest single-batch OpenAI volume since cold start; **Ro ships 2 ads in one batch — first non-cold-start multi-ad Ro batch**, breaking the 4-batches-of-≤1-ad pattern (still placeholder-only); **Anthropic 0 new ads — 3rd consecutive silence locks the "2026-05-11 standalone launch" diagnosis** per the batch-7 ≥3-silent-batch methodology; 19 noise ads dominated by repeats (Uproot Clean ×4, Aelfric Eden ×3, Lauren Brooks ×2, SecretRomance/Romance ×2 cloud variants) + 6 new noise pages (Hero FinCorp, Hampton Roads Honda Dealers, Carolina Freightways, Rough Country, Cholesterol Support Group, Eden Books); brand-name filter still untuned, eighth consecutive batch
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, hims-three-wedge-surge, openai-cluster-3-opens, ro-multi-ad-batch, anthropic-standalone-locked, wegovy-5-batch-stability]
sources: 1
source_path: raw/ads/digest-2026-05-20.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-20
updated: 2026-05-20
---

# FB Ads Digest — 2026-05-20

Eighth batch from the [[competitor-ads-farm]]. **36 new ads, 177 dedup-skipped** out of 213 fetched after a 4-day gap from batch 7 (2026-05-16). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Highest-volume signal batch since cold start.** 17 of 36 new ads (47%) are tracked-brand — biggest absolute signal volume in any post-cold-start batch. Eight-batch noise-rate trend: 65% → 82% → 50% → 69% → 77% → 100% → 33% → **53%**. The 4-day fetch gap explains the larger batch (typical 1-day gap = 9-22 ads; 4-day gap = 36 ads).
- **Hims runs a THREE-wedge verbatim surge in one batch** — first time three wedges ship verbatim re-launches together. Wegovy GLP-1 verbatim across **5 batches / 14-day stability window** (2 ads in this batch) + Hair Hybrids verbatim re-launch across 2 ads (first Hair Hybrids verbatim re-launch since cold start) + 4 placeholders. Cumulative **61 Hims ads**.
- **Wegovy GLP-1 stability window extends to 14 days.** Longest single-template-stability window in the vault — verbatim across batches 1+4+5+7+8.
- **Hair Hybrids verbatim re-launches for first time post-cold-start.** Adds a **second wedge** to the verbatim-stability evidence beyond Wegovy/Sex Rx — three wedges now confirmed as verbatim-stable.
- **OpenAI ships 7 new ads — biggest single-batch OpenAI volume since cold start.** May 8 cluster (cluster 2) expands **8 → 12** (4 new ads, disproving any remaining "cluster-2 exhausted" claims 12 days post-launch). **Cluster 3 opens** with 2 new 2026-05-15 ads — first OpenAI launch outside Apr 2-21 + Apr 30/May 8 windows. 1 new 2026-05-11 ad sits between cluster 2 and cluster 3. Cumulative **40 OpenAI ads, 0 with copy.**
- **Ro ships 2 ads in one batch — first non-cold-start multi-ad Ro batch.** Breaks the 4-batches-of-≤1-ad pattern (batches 2, 5, 7). Both still placeholder-only (started 2026-05-14 and 2026-05-08). Cumulative **6 Ro ads, all placeholders.**
- **Anthropic 0 new ads — 3rd consecutive silence locks the "2026-05-11 standalone launch" diagnosis.** Per the batch-7 ≥3-silent-batch methodology, the 2026-05-11 ad is now confirmed as a standalone launch, not the opening of a slow cluster. Cumulative **6 Anthropic ads across 2 launch windows** (5 in Mar 16 – Apr 8 + 1 standalone on 2026-05-11).
- **19 noise ads dominated by repeats** — Uproot Clean (4-batch repeat: 2+4+5+8), Aelfric Eden (3-batch repeat: 1+5+8), Lauren Brooks (2-batch repeat: 4+8), Herb'N Eden (2-batch repeat: 5+8). + 2 SecretRomance cloud variants (`cloudn57` + `cloudn65`, 2 ads each — "Romance" contains "Ro" substring) revive the [[ads-digest-2026-05-12]] Romance-miniseries noise pattern.
- **6 new noise pages** — Hero FinCorp ("Ro" inside "Hero"), Hampton Roads Honda Dealers (Hampton substring), Carolina Freightways Inc. ("Ro" inside "Carolina"), Rough Country ("Ro" inside "Rough"), Cholesterol Support Group ("Ro" inside "Cholesterol"), Eden Books (Eden substring — 10th distinct "Eden" noise brand).
- **Brand-name filter still untuned — eighth consecutive batch.** Outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-20.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 213 • New: 36 • Dedup-skipped: 177 (83%)
- Gap from prior batch: 4 days (batch 7 = 2026-05-16)

## Tracked-brand creative inventory

### [[hims]] — 8 new ads (THREE-wedge verbatim surge — Wegovy + Hair Hybrids + 4 placeholders)

The largest single-batch Hims volume since cold start. Three wedges ship verbatim re-launches simultaneously.

**Ad #1 — Hair Hybrids verbatim re-launch (1st post-cold-start)**

- ID `2064207334519052`, started 2026-05-09, format unknown
- Body copy is **verbatim** to the 2026-05-06 canonical Hair Hybrids template:

> Don't wait — join the hundreds of thousands of guys who've found true results. Get a treatment recommendation today, 100% online.
>
> Why Hims?
> 🗓️Regrow in as few as 3-6 months
> 🧑🏻‍⚕️Doctor-trusted ingredients
> 📦Free shipping to your front door (if prescribed)

Followed by the canonical Hair Hybrids compounded-drug disclaimer block.

**Ad #2 — Wegovy GLP-1 verbatim re-launch (5th batch / 14-day stability window)**

- ID `1046013881316991`, started 2026-05-04, format unknown
- Body copy is **verbatim** to the 2026-05-06 canonical Wegovy GLP-1 template (same as batches 4, 5, 7).

**Ad #3 — Hair Hybrids verbatim re-launch (2nd in same batch)**

- ID `728317760309201`, started 2026-04-22, format unknown
- Body copy is **verbatim** to the 2026-05-06 Hair Hybrids template (same wording as Ad #1).

**Ad #4 — Wegovy GLP-1 verbatim re-launch (2nd in same batch)**

- ID `1002990665415931`, started 2026-05-11, format unknown
- Body copy is **verbatim** to the 2026-05-06 canonical Wegovy GLP-1 template.

**Ads #5-8 — Placeholder (`{{product.brand}}` body)**

- IDs `864218772620911` (started 2026-05-11), `1286410240326521` (started 2026-05-04), `1742743447107513` (started 2026-05-05), `848302227664919` (started 2026-05-05) — all pure dynamic-creative placeholders.

**Wegovy GLP-1 verbatim instances (5-batch / 14-day stability window):**

| Batch | Date | Ad ID(s) | Started |
|---|---|---|---|
| 1 | 2026-05-06 | (initial wave) | early Apr 2026 |
| 4 | 2026-05-12 | `3567971296700086` | 2026-05-07 |
| 5 | 2026-05-14 | `956466943766183` | 2026-05-04 |
| 7 | 2026-05-16 | `1693764951776930` | 2026-05-13 |
| **8** | **2026-05-20** | **`1046013881316991` + `1002990665415931`** | **2026-05-04, 2026-05-11** |

**14-day verbatim-stability window — longest in the vault.** Hims has now run identical Wegovy body copy across 6 separate ad-library entries with launch dates spanning 2026-05-04 → 2026-05-13.

**Hair Hybrids verbatim instances (post-cold-start re-launches):**

| Batch | Date | Ad ID(s) | Started |
|---|---|---|---|
| 1 | 2026-05-06 | (initial 10+ wave) | early Apr 2026 |
| **8** | **2026-05-20** | **`2064207334519052` + `728317760309201`** | **2026-05-09, 2026-04-22** |

**First Hair Hybrids verbatim re-launch since cold start.** Adds a **second wedge to verbatim-stability evidence** beyond Wegovy/Sex Rx — Hims' template-stability pattern now confirmed across **three wedges** (GLP-1, hair, sex Rx).

**Three-wedge verbatim surge** is a step-change in surge magnitude:

| Batch | Date | Wedges in surge | New Hims ads | Wave state |
|---|---|---|---|---|
| 5 | 2026-05-14 | 2 (Wegovy + Sex Rx Climax Control) | 2 | Surge |
| 6 | 2026-05-15 | 0 | 0 | Trough |
| 7 | 2026-05-16 | 2 (Wegovy + Sex Rx Climax Control) | 3 (incl. 1 placeholder) | Surge |
| **8** | **2026-05-20** | **3 (Wegovy + Hair Hybrids + 4 placeholders)** | **8** | **Surge — three-wedge** |

The 5→6→7→8 sequence (surge → trough → surge → surge) extends the alternating cadence with a **second consecutive surge** at higher magnitude — open whether this is a 4-day-gap artifact (8 = compressed batches 8+9+10+11) or a genuine multi-wedge surge intensification.

### [[openai]] — 7 new ads (May 8 cluster 8 → 12, NEW cluster 3 opens with 2026-05-15 ads, 1 bridge 2026-05-11 ad)

Largest single-batch OpenAI volume since cold start.

From the digest:

- **Cluster 2 expansion (May 8)**: 4 new ads — IDs `988979626997856`, `1975636119722763`, `1318816936847050`, `1661069165042692`, all started 2026-05-08
- **Cluster 3 opens (May 15)**: 2 new ads — IDs `1521901416110521`, `1572670471096756`, both started 2026-05-15
- **Bridge ad (May 11)**: 1 new ad — ID `4242069169438254`, started 2026-05-11

All 7 are carousels with `{{product.name}}` / `{{product.brand}}` placeholders.

**Cluster-2 (May 8) timeline now spans 12 days from launch:**

| Batch | Date | New May 8 ads | Cumulative cluster-2 ads |
|---|---|---|---|
| 3 | 2026-05-11 | 2 | 2 |
| 4 | 2026-05-12 | 4 | 6 |
| 5 | 2026-05-14 | 0 | 6 |
| 6 | 2026-05-15 | 0 | 6 |
| 7 | 2026-05-16 | 2 | 8 |
| **8** | **2026-05-20** | **4** | **12** |

Cluster 2 (May 8) is at **12 ads across 5 active batches** — 12 days post-launch and still rolling out. Confirms the batch-7 conclusion: **cluster pacing is variable and "fully dedup-cached" claims need ≥3 silent batches**. Cluster 2 is now the most-evidenced single-launch cluster in the vault.

**Cluster 3 opens (2026-05-15) — first OpenAI launch outside the Apr 2-21 + Apr 30/May 8 windows:**

- 2 new ads with 2026-05-15 launch dates — first cluster 3 signal
- Plus 1 ad with 2026-05-11 start date (sits between cluster 2's May 8 and cluster 3's May 15 — open whether bridge or its own micro-cluster)

**Three distinct OpenAI launch windows now tracked:**

1. **Cluster 1**: Apr 2-21 (24 ads via batches 1+2)
2. **Cluster 2**: Apr 30 / May 8 (12 ads via batches 3+4+7+8)
3. **Cluster 3**: 2026-05-15 (2 ads opening, batch 8) — possibly + 1 May 11 bridge

Cumulative **40 OpenAI ads across 8 batches, 0 with teardown-able copy.** Catalog-ads-only AI-lab pattern SEXTUPLE-confirmed across 6 active batches (1, 2, 3, 4, 7, 8) with silence in 2 batches (5, 6).

### [[ro]] — 2 new ads (first multi-ad non-cold-start batch — breaks ≤1-ad pattern)

From the digest:

- ID `2277114206027622`, started 2026-05-14, format unknown, body `{{product.brand}}`
- ID `2238568280301485`, started 2026-05-08, format unknown, body `{{product.brand}}`

**First non-cold-start multi-ad Ro batch.** All four previous Ro signal-bearing batches shipped ≤1 ad each (1+2+1=4 across batches 1, 2, 7; batch 2 had 2 but spread across two start dates from the cold-start backlog).

**Cumulative Ro tracking (6 ads across 8 batches):**

| Batch | Date | New Ro ads | Cumulative |
|---|---|---|---|
| 1 | 2026-05-06 | 1 | 1 (started 2026-04-14) |
| 2 | 2026-05-10 | 2 | 3 (started 2026-05-04, 2026-04-28) |
| 3-6 | various | 0 | 3 (4-batch silence #1) |
| 7 | 2026-05-16 | 1 | 4 (started 2026-05-04) |
| **8** | **2026-05-20** | **2** | **6 (started 2026-05-14, 2026-05-08)** |

**All 6 Ro ads ship `{{product.brand}}` placeholder body text — zero static narrative across 8 batches.** Pattern persists across the longest window in the farm; the bare-"Ro" page name continues to run sparse catalog-driven dynamic creative. Batch 8's 2-ad volume is the first signal that Ro may be picking up catalog cadence (or the 4-day fetch gap simply captured 2 days of Ro ad-shipping that single-day fetches would have spread across 2 batches).

### [[anthropic]] — 0 new ads (3rd consecutive silence — "standalone launch" diagnosis LOCKED)

No new Anthropic ads. Cumulative remains **6 ads across 2 distinct launch windows** (Mar 16 – Apr 8 + 2026-05-11):

| Batch | Date | New Anthropic ads | Notes |
|---|---|---|---|
| 1 | 2026-05-06 | 5 | Initial wave |
| 2-4 | 2026-05-10 to 2026-05-12 | 0 | Silence trough (3 batches) |
| 5 | 2026-05-14 | 1 | 2026-05-11 launch (new window) |
| 6 | 2026-05-15 | 0 | Silence #1 post-2026-05-11 |
| 7 | 2026-05-16 | 0 | Silence #2 post-2026-05-11 |
| **8** | **2026-05-20** | **0** | **Silence #3 post-2026-05-11 — LOCKS diagnosis** |

**Per the batch-7 ≥3-silent-batch methodology, the 2026-05-11 ad is now confirmed as a standalone launch, not the opening of a slow cluster.** Three consecutive silent batches with a 4-day fetch gap on batch 8 (which would have surfaced new Anthropic ads if they existed) is decisive.

**Anthropic pattern**: 5 ads (Mar 16 – Apr 8 wave) + 1 ad (standalone 2026-05-11) — both windows now classified as discrete launches, not rolling clusters. Distinctly less aggressive than OpenAI's 40-ad volume across the same period (6 vs 40 — Anthropic is 15% of OpenAI's FB-ad volume).

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (8th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (8th consecutive batch)
- **Eden (telehealth)** — never appeared (8th consecutive batch); bare-"Eden" filter continues to produce only noise

## False positives ("brand-name match" noise) — 19 of 36 ads (53%)

19 noise ads across 12 distinct noise pages — highest noise volume by absolute count since cold start (though only ~53% noise *rate*).

### Multi-fire repeat noise pages (8 ads, 4 pages)

1. **Uproot Clean** (1 ad, video, started 2026-05-18) — **4-batch repeat** (also batches 2, 4, 5). Long-form pet-odor washing-machine biofilm copy. Now the most-recurring noise page in the farm by batch count.
2. **Aelfric Eden** (2 ads, carousel, started 2026-04-27 + 2026-02-27) — **3-batch repeat** (also batches 1, 5). Streetwear fashion, 15-30% OFF clearance.
3. **Lauren Brooks** (2 ads, image, both started 2026-05-18) — **2-batch repeat** (also batch 4). "Please STOP buying allergy meds for your dog" long-form pet-allergy direct-response copy — exact same body text re-shipped as in batch 4.
4. **Herb'N Eden** (2 ads, video, started 2024-10-18 + 2026-02-22) — **2-batch repeat** (also batch 5). Natural skincare/soap free-sample lead-magnet.

### New "Romance" noise category surfacing (4 ads, 2 cloud variants)

5. **SecretRomance-cloudn57** (2 ads, video, both started 2026-05-18) — "Ro" inside "Romance"; serialized fiction ("Sierra's Second Chance" magical-zoo isekai narrative). Different cloud-variant of the same Romance-miniseries noise category surfaced in [[ads-digest-2026-05-12]] (which had 3 Romance ads).
6. **SecretRomance-cloudn65** (2 ads, video, both started 2026-05-18) — same body copy as cloudn57 but different page ID. Suggests Romance-app advertiser runs **multiple cloud-suffix sub-pages** (cloudn57 + cloudn65 + likely many more) — per-ad-ID dedup catches single ad refresh but a multi-sub-page operator can launder fresh ads indefinitely.

### New noise pages (7 ads, 6 distinct pages)

7. **Hero FinCorp** (1 ad, carousel, started 2026-04-15) — "Ro" inside "Hero"; Indian financial services dynamic-feed catalog placeholder. First "Hero" surname/brand-prefix noise.
8. **Hampton Roads Honda Dealers** (2 ads, carousel, both around 2026-05-01) — exact "Hampton" substring (regional Virginia auto dealer). **14th distinct Hampton regional-business noise page** (after the batch-7 Nissan of Hampton 13th).
9. **Carolina Freightways Inc.** (2 ads, image + carousel, both started 2025-10-24) — "Ro" inside "Ca-Ro-lina"; trucking owner-operator job ad ($4,800-$5,200/week, 3,100+ miles, Florida-North Carolina lanes). Old October 2025 launch dates suggest this ad has been running 7+ months and just surfaced via Apify backfill.
10. **Rough Country** (1 ad, carousel, started 2026-04-24) — "Ro" inside "Rough"; truck lift kits (2024+ Tacoma).
11. **Cholesterol Support Group** (1 ad, image, started 2026-05-06) — "Ro" inside "Cholesterol"; long-form ICU-nurse statins-skepticism narrative ("I've been administering statins for 19 years, but last month I refused to take one myself"). Same long-form direct-response structure as Lauren Brooks pet-allergy and Cholesterol/statins variant (post-failure-cascade narrative; here it's "watching my husband die slowly" trope).
12. **Eden Books** (1 ad, image, started 2023-09-15) — exact "Eden" substring; online romance bookstore. **10th distinct "Eden" noise brand** (after batch-6 Eden Plastic Surgery Miami as 9th). Old September 2023 launch date — long-tail ad surfacing via Apify backfill.

### Cumulative noise-corpus updates

- **Hampton regional-business noise pages**: now 14 distinct (added Hampton Roads Honda Dealers)
- **"Eden" noise brands**: now 10 distinct (added Eden Books)
- **"Ro"/"ro"-substring noise**: continues to expand structurally — Hero FinCorp, Carolina Freightways, Rough Country, Cholesterol Support Group are 4 new sub-patterns this batch (surname-prefix "Hero", state-name "Carolina", common adjective "Rough", anatomical-noun "Cholesterol")
- **Romance/"Ro" sub-category**: re-confirmed across batches 4+8 with multi-cloud-variant operator pattern (SecretRomance-cloudn57 + cloudn65) — first noise category to demonstrate **per-page-ID-allow-listing bypass via sub-page proliferation**

## Cross-cutting patterns

### Eight-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Ro | Real-signal % |
|---|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | 1 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | 2 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 0 | 23% |
| 2026-05-15 | 203 | 3 | 200 | 1.5% | 0 | 0 | 0 | 0 | 0% |
| 2026-05-16 | 208 | 9 | 199 | 4% | 2 | 3 | 0 | 1 | 67% |
| **2026-05-20** | **213** | **36** | **177** | **17%** | **7** | **8** | **0** | **2** | **47%** |

The 4-day fetch gap inflated the new-ad volume to 36 (vs typical 3-22 / mean ~13 for 1-day gaps). Dedup-skipped percentage dropped to 83% (vs typical 92-98.5%) — confirms dedup density tracks fetch-gap inversely. Real-signal proportion 47% — second-highest batch since cold start (only batch 7's 67% is higher). Absolute signal volume of **17 tracked-brand ads is a new high-water mark for the farm** (prior high was 71 in cold-start batch 1).

### Hims surge magnification across the 5→6→7→8 sequence

Hims' four-batch surge-trough-surge-surge pattern now shows escalating magnitude in surge batches:

| Batch | Date | New Hims ads | Wedges in surge | Wave state |
|---|---|---|---|---|
| 5 | 2026-05-14 | 2 | 2 (Wegovy + Sex Rx) | Surge — two-wedge |
| 6 | 2026-05-15 | 0 | 0 | Trough |
| 7 | 2026-05-16 | 3 (incl. 1 placeholder) | 2 (Wegovy + Sex Rx) | Surge — two-wedge |
| **8** | **2026-05-20** | **8 (incl. 4 placeholders)** | **3 (Wegovy + Hair Hybrids + placeholder cluster)** | **Surge — three-wedge** |

Two readings:

1. **4-day fetch-gap compression** — batch 8 absorbed what would have been batches 8+9+10+11 under a 1-day cadence; the 3-wedge surge is actually 3-4 separate 1-wedge surges compressed into one fetch window
2. **Genuine surge intensification** — Hims' creative inventory is ramping up across more wedges simultaneously; the 5→7→8 sequence shows surge magnitudes of 2 → 3 → 8 (+ wedge counts 2 → 2 → 3)

Distinguishing requires either a 1-day-gap fetch on 2026-05-21 (to test compression hypothesis) or the next batch coming in at typical 1-day cadence with thin Hims volume (to confirm batch 8 absorbed 4 days of inventory).

### Wegovy GLP-1 stability window — 14 days / 5 batches

The Wegovy template's verbatim-stability window is now the longest single-template-stability window tracked in this vault:

- 5 batches active (1, 4, 5, 7, 8)
- 6 distinct ad-library entries with verbatim body copy
- 14-day stability window (2026-05-06 → 2026-05-20)
- Includes 2 verbatim re-launches in a single batch (batch 8)

**Implication for [[medvi-positioning]] and [[concepts/dtc-telehealth-ad-template]]**: the Wegovy template is now the most stable single creative artifact in the competitive corpus. Mirroring it (with disclaimer + price-split variations) is the safest baseline for Medvi's GLP-1 wedge. Inside-bullet A/B testing remains the standing creative-test surface.

### OpenAI cluster 3 opens — first launch outside Apr 2-21 + Apr 30/May 8 windows

Three distinct launch windows for OpenAI in 8 batches:

1. **Cluster 1 (Apr 2-21)** — 24 ads, batches 1+2, single campaign wave
2. **Cluster 2 (Apr 30 / May 8)** — 12 ads, batches 3+4+7+8, 12 days post-launch and still rolling out
3. **Cluster 3 (2026-05-15)** — 2 ads opening, batch 8 — possibly + 1 May 11 bridge ad

Cluster cadence is ~10-14 days between cluster opens (Apr 30 → May 8 within cluster 2 was a sub-cluster; cluster 3's May 15 is ~7 days after cluster 2's May 8). If the May 15 launches are cluster 3's start, batch 9-10 should surface 4-6 more May 15 ads (matching cluster 2's batch-3 opening). If cluster 3 stays at 2 ads, the pacing is decelerating.

### Anthropic standalone launch confirmed

Per the batch-7 ≥3-silent-batch methodology, the 2026-05-11 ad is now decisively confirmed as a standalone launch:

- 3 consecutive silent batches post-launch (batches 6, 7, 8)
- 4-day fetch gap on batch 8 would have captured any new Anthropic ads in 2026-05-17, 2026-05-18, 2026-05-19, 2026-05-20 — none surfaced
- Cumulative pattern: 5 ads (Mar 16 – Apr 8 wave) + 1 ad (standalone 2026-05-11) = sparse, well-spaced standalone launches

Distinctly different from OpenAI's continuous cluster expansion. **Anthropic's FB ad volume is 15% of OpenAI's across the same window (6 vs 40 ads).** Despite Anthropic passing OpenAI in *business adoption* (2026-05-13 Ramp/EconLab flip — see [[free-sample-phase]]), OpenAI's *paid social cadence* remains an order of magnitude more aggressive.

### Multi-cloud-variant noise: SecretRomance is the first per-page-ID-allow-listing bypass pattern

SecretRomance ships ads under multiple cloud-suffix page IDs (`cloudn57`, `cloudn65`, almost certainly more) with identical body copy. Implications:

1. **Per-page-ID allow-listing** (the action item from [[competitor-ads-farm]]) **doesn't fully close the noise floor** for operators who run multi-sub-page advertising
2. **Per-ad-ID dedup is insufficient** even when sub-pages share body copy — each cloud-variant has distinct ad IDs that pass through dedup
3. **Content-based dedup** (hash the body copy, not the ad ID) would close this failure mode — but introduces false positives for legitimate verbatim re-launches like Hims' Wegovy template

The Romance category is now the first noise pattern in the farm to require **architectural** filtering changes, not just configuration tuning.

## Open questions

- **Is batch 8's 36-ad volume a 4-day-gap compression artifact, or a genuine surge?** A 1-day-cadence batch 9 (2026-05-21) with thin Hims/OpenAI signal would confirm compression. A thick batch 9 would confirm intensification.
- **Will OpenAI cluster 3 (May 15) expand in batches 9-10 like cluster 2 did, or stay at 2 ads?** Cluster pacing is variable enough that either is plausible.
- **Does the Hims three-wedge surge become the new surge baseline, or revert to two-wedge in batch 9?** Three-wedge requires Hair Hybrids verbatim re-launches at the same cadence as Wegovy/Sex Rx — open whether Hair Hybrids was a one-time re-launch or joins the rotating verbatim-stability set.
- **Will Anthropic's next launch be another standalone (3rd window) or finally open a cluster?** Six ads in 8 batches across 2 windows is the established sparse pattern.
- **Is the SecretRomance multi-cloud-variant noise pattern an outlier, or do other noise operators run sub-page proliferation?** If multiple, content-based dedup becomes the only structural fix.
- **Why old launch dates (2023-09 Eden Books, 2025-10 Carolina Freightways, 2024-10 Herb'N Eden) surfacing now?** Apify catalog-feed sampling appears to backfill long-tail ads at non-zero rate — open whether this is a one-time event or recurring.

## Related

- [[competitor-ads-farm]] — eighth batch from this farm; highest absolute signal volume since cold start (17 tracked-brand ads); 4-day fetch gap inflated batch size to 36 new ads
- [[hims]] — 8 new ads (THREE-wedge verbatim surge: Wegovy verbatim #5+#6, Hair Hybrids verbatim #1+#2 post-cold-start, 4 placeholders); cumulative 61 ads
- [[ro]] — 2 new ads (first multi-ad non-cold-start batch); cumulative 6 ads, all placeholders across 8 batches
- [[openai]] — 7 new ads (May 8 cluster 8 → 12, NEW cluster 3 opens with 2 May 15 ads, 1 May 11 bridge); cumulative 40 ads across 3 launch windows
- [[anthropic]] — 0 new ads (3rd consecutive silence post-2026-05-11 LOCKS "standalone launch" diagnosis per batch-7 ≥3-silent-batch methodology); cumulative 6 ads across 2 launch windows
- [[concepts/dtc-telehealth-ad-template]] — Wegovy verbatim now 5 batches / 14-day stability; Hair Hybrids verbatim re-launches for first time post-cold-start; three wedges now confirmed verbatim-stable
- [[concepts/compounded-drug-disclaimer]] — Hair Hybrids disclaimer ships verbatim for first time post-cold-start; Wegovy disclaimer ships verbatim for 5th time (14-day stability)
- [[ads-digest-2026-05-06]] — first batch (cold-start canonical wave; Wegovy + Hair Hybrids + Sex Rx templates established)
- [[ads-digest-2026-05-10]] — second batch (Hard Mints introduction, OpenAI catalog confirmation)
- [[ads-digest-2026-05-11]] — third batch (OpenAI May 8 cluster opens)
- [[ads-digest-2026-05-12]] — fourth batch (Wegovy verbatim #1, Romance-miniseries first noise appearance)
- [[ads-digest-2026-05-14]] — fifth batch (Hims two-wedge surge #1)
- [[ads-digest-2026-05-15]] — sixth batch (universal silence)
- [[ads-digest-2026-05-16]] — seventh batch (Hims two-wedge surge #2 + ≥3-silent-batch methodology established)

## Appears in

- Eighth entry in `wiki/sources/` for the competitor-ads farm. **Highest absolute signal volume since cold start (17 tracked-brand ads).** Hims three-wedge verbatim surge (Wegovy + Hair Hybrids + placeholders) is the largest single-batch wedge count. Wegovy GLP-1 verbatim across 5 batches / 14-day stability window is the longest single-template-stability window in the vault. OpenAI cluster 3 opens with 2026-05-15 launches. Anthropic 3rd consecutive silence locks the standalone-launch diagnosis per the batch-7 methodology. SecretRomance multi-cloud-variant noise is the first per-page-ID-allow-listing bypass pattern, suggesting content-based dedup may eventually be required.
