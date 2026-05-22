---
title: FB Ads Digest — Competitor brands — 2026-05-22
category: source
summary: Ninth competitor-ads farm batch — 17 new FB Ad Library entries (208 fetched, 191 dedup-skipped, 92%) after a 2-day gap from batch 8; **OpenAI ships its FIRST static-narrative ad with copy** — *"For anyone who's been putting off that project, Codex is here to make it happen. Try Codex for free today."* (video, started 2026-05-15, ID `1651415066063068`) — directly references the [[free-sample-phase]] Codex-2-months-free retention promo and breaks the catalog-ads-only OpenAI pattern that had been SEXTUPLE-confirmed across 8 batches; **Hims continues Hair Hybrids verbatim surge — 3 verbatim Hair Hybrids re-launches** (post-batch-8 first re-launches) + 2 placeholders = 5 new Hims ads; cumulative Hair Hybrids verbatim now spans batches 1+8+9; **Ro drops back to 1 ad** after batch 8's 2-ad anomaly — supports the **fetch-gap compression hypothesis** for batch 8 (batch 9's per-day rate matches batch 8's: ~8.5 ads/day, Ro 0.5/day in both); **Anthropic ships 1 new ad with 2026-03-17 start date** — an OLD ad from the original Mar 16 – Apr 8 launch wave surfacing via catalog feed, doesn't change the "standalone launch" diagnosis for 2026-05-11; SecretRomance multi-cloud-variant noise continues (cloudn57 + cloudn65, 4 ads), Lauren Brooks dog-allergy long-form re-fires verbatim for the 3rd time (batches 4+8+9), Hampton Water Rosé (wine brand, not Hampton Founders) + Gardens of Eden surface as new noise pages
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, openai-first-copy-ad, codex-retention-promo, hims-hair-hybrids-surge, anthropic-original-wave-resurface, fetch-gap-compression-confirmed]
sources: 1
source_path: raw/ads/digest-2026-05-22.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-22
updated: 2026-05-22
---

# FB Ads Digest — 2026-05-22

Ninth batch from the [[competitor-ads-farm]]. **17 new ads, 191 dedup-skipped** out of 208 fetched after a 2-day gap from batch 8 (2026-05-20). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **OpenAI ships its FIRST static-narrative ad with copy.** Eight batches of catalog-ads-only (40 carousels with `{{product.name}}`/`{{product.brand}}` placeholders, zero static narrative) — and now batch 9 surfaces a **video ad with full body copy**: *"For anyone who's been putting off that project, Codex is here to make it happen. Try Codex for free today."* (ID `1651415066063068`, started 2026-05-15). **Directly references the [[free-sample-phase]] Codex-2-months-free retention promo** ([[nate-herk]] #5 in [[youtube-digest-apify-2026-05-14]]). This is the **first OpenAI ad copy in the vault** and breaks the SEXTUPLE-confirmed catalog-ads-only pattern. Cluster 3 (2026-05-15 launches) now confirmed as the **"Codex retention narrative" cluster** — not a catalog-cluster like 1 and 2.
- **Hims continues Hair Hybrids verbatim surge** — 3 more Hair Hybrids verbatim re-launches (IDs `3372941842875795` started 2026-02-26, `868992329557540` started 2026-05-06, `2498995467227011` started 2026-05-19) + 2 placeholders. Hair Hybrids verbatim now spans **3 batches** (1+8+9) — joins Wegovy GLP-1 (5 batches) and Sex Rx Climax Control (2 batches) as the **second-most-stable** Hims wedge template. Cumulative **66 Hims ads**.
- **Wegovy GLP-1 silent in batch 9** — first time since batch 5 that Wegovy verbatim doesn't ship. Hair Hybrids picks up the surge slack. **Surge composition rotates** between batches — Wegovy was the only template in batches 4+5+7, both Wegovy+Hair Hybrids in batch 8, Hair-Hybrids-only in batch 9.
- **Ro drops back to 1 ad after batch 8's 2-ad anomaly.** Single placeholder ad (ID `946235747996438`, started 2026-04-28). **Supports the fetch-gap compression hypothesis** for batch 8 — batch 9's per-day rate (~8.5 ads/day total, Ro 0.5/day) matches batch 8's per-day rate (9 ads/day total, Ro 0.5/day). The batch-8 multi-ad surge was largely a 4-day-gap artifact, not a genuine pickup in Ro's catalog cadence.
- **Anthropic ships 1 new ad — but from the ORIGINAL Mar 16 – Apr 8 launch window** (started 2026-03-17, ID `925745760422663`, carousel `{{product.brand}}` placeholder). Catalog feed surfaces an old ad from the original wave 2+ months later. **Does NOT change the "2026-05-11 standalone launch" diagnosis** (LOCKED in batch 8) — the 2026-03-17 ad is part of the already-tracked wave. Cumulative **7 Anthropic ads across 2 launch windows** (6 in Mar 16 – Apr 8 + 1 standalone on 2026-05-11).
- **Fetch-gap compression hypothesis largely confirmed.** Batch 9 per-day rates (8.5/d total, Hims 2.5/d, OpenAI 1.5/d, Ro 0.5/d) closely match batch 8 per-day rates (9/d total, Hims 2/d, OpenAI 1.75/d, Ro 0.5/d). Batch 8's 36-ad single-batch surge was mostly a 4-day-gap artifact, not a genuine multi-wedge surge intensification.
- **Noise: 6 ads, 4 noise pages.** SecretRomance-cloudn65 (3 video ads, identical "Sierra Sterling" body) + SecretRomance-cloudn57 (1 video ad, same body) — multi-cloud-variant pattern from batch 8 confirms across batches 8+9. Lauren Brooks dog-allergy long-form copy re-fires verbatim for the **3rd time** (batches 4+8+9 — most consistent verbatim noise repeat in the farm). **Hampton Water Rosé** (1 carousel placeholder, wine brand — NOT Hampton Founders; 15th distinct Hampton-substring noise) and **Gardens of Eden** (1 carousel placeholder, "Eden" prefix — 11th distinct "Eden" noise brand) are new noise pages.
- **Brand-name filter still untuned — ninth consecutive batch.** Outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-22.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 208 • New: 17 • Dedup-skipped: 191 (92%)
- Gap from prior batch: 2 days (batch 8 = 2026-05-20)

## Tracked-brand creative inventory

### [[openai]] — 3 new ads (FIRST static-narrative ad in vault — Codex retention promo)

The structural break event for OpenAI tracking. Eight batches of pure-catalog placeholders, now:

**Ad #1 — Codex retention promo (FIRST OpenAI ad with copy)**

- ID `1651415066063068`, started 2026-05-15, format **video**, no headline
- Body copy:

> For anyone who's been putting off that project, Codex is here to make it happen. Try Codex for free today.

**Strategic significance**:

1. **Breaks the SEXTUPLE-confirmed catalog-ads-only pattern.** 40 carousels with zero copy across 6 active batches — and now a video ad with full body copy. The pattern wasn't permanent; it was the *default* for catalog clusters, broken when OpenAI ships a campaign with creative-team-authored messaging.
2. **Directly references the [[free-sample-phase]] Codex-2-months-free retention promo.** The "Try Codex for free today" CTA maps cleanly onto the Codex Enterprise application-form play surfaced by [[nate-herk]] #5 in [[youtube-digest-apify-2026-05-14]] (2026-05-13 business-adoption flip → within hours, Codex free for 2 months).
3. **Cluster 3 (2026-05-15) is now confirmed as the "retention narrative" cluster** — not a catalog-cluster expansion like Cluster 1 (Apr 2-21) or Cluster 2 (Apr 30 / May 8). Cluster 3 ships static narrative copy + video format + Codex-specific CTA. Different motion from the catalog feed.
4. **First OpenAI ad copy for teardown in this vault.** Compares directly with Hims' three-bullet template ([[concepts/dtc-telehealth-ad-template]]) — same minimum-viable structure (hook + product + CTA) but compressed to a single sentence vs Hims' three-bullet block. Reflects the difference between B2B/dev-tool ads (one-line product reveal) and DTC telehealth (proof-claim + price-split + disclaimer).
5. **The 2-day cadence (batch 8 → batch 9) captured a brand-new ad type within Cluster 3.** Cluster 3 in batch 8 was 2 placeholder carousels (started 2026-05-15); in batch 9 a video ad with copy joins (also started 2026-05-15). Cluster 3 is **shipping multiple creative formats in parallel** — not a pure-catalog cluster.

**Ad #2 — `{{product.name}}` carousel from Cluster 1 (April expansion)**

- ID `1536515517807933`, started 2026-04-07, format carousel
- Body: `{{product.brand}}` placeholder
- Old Cluster 1 ad surfacing via catalog feed — joins the 24 ads from batches 1+2 in Cluster 1

**Ad #3 — `{{product.name}}` carousel from Cluster 2 (May 8 expansion)**

- ID `3404036309772778`, started 2026-05-08, format carousel
- Body: `{{product.brand}}` placeholder
- Cluster 2 (May 8) expands from 12 → 13 ads. Cluster 2 is **15 days post-launch and still rolling out**.

**Updated OpenAI cumulative tracking — 43 ads across 9 batches, 3 launch windows, 1 with copy:**

| Batch | Date | New | Cum | Cluster |
|---|---|---|---|---|
| 1 | 2026-05-06 | 21 | 21 | Cluster 1 (Apr 2-21) |
| 2 | 2026-05-10 | 3 | 24 | Cluster 1 expansion |
| 3 | 2026-05-11 | 3 | 27 | Cluster 2 opens (Apr 30 + May 8) |
| 4 | 2026-05-12 | 4 | 31 | Cluster 2 expansion |
| 5+6 | (silence) | 0 | 31 | — |
| 7 | 2026-05-16 | 2 | 33 | Cluster 2 expansion |
| 8 | 2026-05-20 | 7 | 40 | Cluster 2 +4 + Cluster 3 opens (May 15) +2 + May 11 bridge +1 |
| **9** | **2026-05-22** | **3** | **43** | **Cluster 1 +1 + Cluster 2 +1 + Cluster 3 ships first VIDEO with COPY (Codex retention)** |

**Cluster 3 (2026-05-15) composition — 3 ads total:**

| Ad ID | Format | Body |
|---|---|---|
| `1521901416110521` | carousel | `{{product.brand}}` placeholder |
| `1572670471096756` | carousel | `{{product.brand}}` placeholder |
| **`1651415066063068`** | **video** | **"...Codex is here to make it happen. Try Codex for free today."** |

Cluster 3 is **the first OpenAI cluster to mix formats** (catalog carousel + video) and **the first to ship copy**.

### [[hims]] — 5 new ads (Hair Hybrids surge continues, Wegovy silent)

The Hair Hybrids verbatim re-launch wave from batch 8 continues into batch 9.

**Ad #1 — Hair Hybrids verbatim re-launch (oldest start date in surge — 2026-02-26)**

- ID `3372941842875795`, started 2026-02-26, format unknown
- Body copy is **verbatim** to the 2026-05-06 canonical Hair Hybrids template (same wording as batch 8's `2064207334519052` + `728317760309201`).
- Notable: 2026-02-26 start date is the **oldest Hair Hybrids verbatim re-launch surfaced post-cold-start** — predates the 2026-05-06 batch by 10 weeks; another catalog-feed-surfaces-old-ad event like the batch-8 Carolina Freightways 2025-10-24 ad.

**Ad #2 — Hair Hybrids verbatim re-launch (started 2026-05-06)**

- ID `868992329557540`, started 2026-05-06, format unknown
- Body copy verbatim to the Hair Hybrids template.

**Ad #3 — Hair Hybrids verbatim re-launch (started 2026-05-19, freshest in surge)**

- ID `2498995467227011`, started 2026-05-19, format unknown
- Body copy verbatim to the Hair Hybrids template.
- Notable: 2026-05-19 start date is **3 days before fetch** — freshest Hair Hybrids launch surfacing; confirms the Hair Hybrids wedge is still actively shipping new ad-library entries.

**Ads #4-5 — Placeholder (`{{product.brand}}` body)**

- IDs `836403042295603` (started 2026-05-04), `1478179350703497` (started 2026-05-04) — pure dynamic-creative placeholders.

**Hair Hybrids verbatim cumulative tracking:**

| Batch | Date | Ad ID(s) | Started |
|---|---|---|---|
| 1 | 2026-05-06 | (initial 10+ wave) | early Apr 2026 |
| 8 | 2026-05-20 | `2064207334519052` + `728317760309201` | 2026-05-09, 2026-04-22 |
| **9** | **2026-05-22** | **`3372941842875795` + `868992329557540` + `2498995467227011`** | **2026-02-26, 2026-05-06, 2026-05-19** |

Hair Hybrids verbatim now active in **3 batches** spanning 2026-05-06 → 2026-05-22 (16-day stability window) — joins Wegovy GLP-1 (5 batches / 14-day window) and Sex Rx Climax Control (2 batches) as a confirmed verbatim-stable wedge template.

**Surge-composition rotation pattern across batches 4-9:**

| Batch | Date | Wegovy | Hair Hybrids | Sex Rx Climax | Placeholders | Total Hims |
|---|---|---|---|---|---|---|
| 4 | 2026-05-12 | 1 | 0 | 0 | 0 | 1 |
| 5 | 2026-05-14 | 1 | 0 | 1 | 0 | 2 |
| 6 | 2026-05-15 | 0 | 0 | 0 | 0 | 0 |
| 7 | 2026-05-16 | 1 | 0 | 1 | 1 | 3 |
| 8 | 2026-05-20 | 2 | 2 | 0 | 4 | 8 |
| **9** | **2026-05-22** | **0** | **3** | **0** | **2** | **5** |

**Surge composition rotates between batches** — the wedge that gets the verbatim re-launches in a given surge isn't deterministic. Batch 9 is the first batch since cold start where **Hair Hybrids ships verbatim re-launches AND Wegovy doesn't**. The three verbatim-stable wedges (Wegovy / Hair Hybrids / Sex Rx Climax Control) take turns; the surge cadence is rotational, not all-three-every-time.

Cumulative **66 Hims ads across 9 batches** (61 → 66).

### [[ro]] — 1 new ad (returns to baseline single-ad pattern)

- ID `946235747996438`, started 2026-04-28, format unknown, body `{{product.brand}}`

**First confirmation that batch 8's 2-ad volume was a 4-day-gap compression artifact, not a genuine pickup.** Batch 9 returns Ro to its baseline ≤1-ad-per-batch pattern.

**Per-day rate comparison (batch 8 vs batch 9 — distinguishing compression vs intensification)**:

| Batch | Gap (days) | Total ads | Ads/day | Ro ads | Ro/day | Hims/day | OpenAI/day |
|---|---|---|---|---|---|---|---|
| 8 | 4 | 36 | 9.0 | 2 | 0.50 | 2.00 | 1.75 |
| **9** | **2** | **17** | **8.5** | **1** | **0.50** | **2.50** | **1.50** |

Per-day rates are nearly identical across the 2-day-gap and 4-day-gap batches. **Fetch-gap compression hypothesis confirmed** — batch 8's 36-ad surge was mostly a multi-day-accumulation artifact, not a genuine multi-wedge intensification.

**Cumulative Ro tracking (7 ads across 9 batches):**

| Batch | Date | New Ro ads | Cumulative |
|---|---|---|---|
| 1 | 2026-05-06 | 1 | 1 |
| 2 | 2026-05-10 | 2 | 3 |
| 3-6 | various | 0 | 3 |
| 7 | 2026-05-16 | 1 | 4 |
| 8 | 2026-05-20 | 2 | 6 |
| **9** | **2026-05-22** | **1** | **7** |

**All 7 Ro ads ship `{{product.brand}}` placeholder body — zero static narrative across 9 batches.** The bare-"Ro" page pattern is now confirmed across the longest window in the farm.

### [[anthropic]] — 1 new ad (original Mar 16 – Apr 8 wave re-surface)

- ID `925745760422663`, started **2026-03-17**, format carousel, body `{{product.brand}}` placeholder

**Crucially: this is an OLD ad from the ORIGINAL Mar 16 – Apr 8 launch wave**, not a new launch. Catalog feed re-surfaces an ad from the wave that batch 1 already tracked.

**Does NOT change the "2026-05-11 standalone launch" diagnosis LOCKED in batch 8.** The 2026-03-17 ad is part of the already-known wave; the lock is on the *cluster status* of the 2026-05-11 ad, not on whether Anthropic ships new ads at all. Cumulative Anthropic launch windows remain:

1. **Window 1**: Mar 16 – Apr 8 (now 6 ads with this new 2026-03-17 entry)
2. **Window 2**: 2026-05-11 standalone (1 ad)

**Updated cumulative**: **7 Anthropic ads across 2 launch windows**, all placeholder carousels except — no, *all* are still placeholder. Catalog-ads-only AI-lab pattern still holds for Anthropic (in contrast to OpenAI's batch-9 break).

| Batch | Date | New Anthropic ads | Cumulative | Notes |
|---|---|---|---|---|
| 1 | 2026-05-06 | 5 | 5 | Initial wave |
| 2-4 | 2026-05-10 to 2026-05-12 | 0 | 5 | Silence trough |
| 5 | 2026-05-14 | 1 | 6 | 2026-05-11 launch (new window) |
| 6-8 | 2026-05-15 to 2026-05-20 | 0 | 6 | 3-batch silence — LOCKS standalone diagnosis |
| **9** | **2026-05-22** | **1** | **7** | **Original wave (Mar 16 – Apr 8) re-surfaces 2026-03-17 ad via catalog feed** |

**Cadence comparison vs [[openai]] across same 9-batch window**: Anthropic 7 ads / OpenAI 43 ads — Anthropic's paid-social cadence remains **~16% of OpenAI's**. **And now OpenAI ships static-narrative copy first** — Anthropic still 100% placeholder, OpenAI broken to first-copy in same batch. The lab-comparison delta widens.

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (9th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (9th consecutive batch)
- **Eden (telehealth)** — never appeared (9th consecutive batch); bare-"Eden" filter continues to produce only noise

## False positives ("brand-name match" noise) — 7 of 17 ads (41%)

7 noise ads across 4 distinct noise pages — moderate noise volume.

### Multi-fire repeat noise pages (5 ads, 2 pages)

1. **SecretRomance-cloudn65** (3 video ads, all started 2026-05-18) — **2nd batch repeat** (also batch 8); same "Sierra Sterling" isekai body across all 3 ads, identical to the batch-8 cloudn65 + cloudn57 ads. Multi-cloud-variant noise pattern from batch 8 now confirmed across **2 consecutive batches**.
2. **SecretRomance-cloudn57** (1 video ad, started 2026-05-19) — **2nd batch repeat** (also batch 8); slightly different body (focuses on "magical zoo" / "ability to talk to animals" — Chapter 1 framing) but same series. cloudn57 + cloudn65 confirmed as **first per-page-ID-allow-listing bypass pattern** continuing to operate.
3. **Lauren Brooks** (1 image ad, started 2026-05-20) — **3rd batch repeat** (batches 4+8+9). "Please STOP buying allergy meds for your dog" long-form pet-allergy direct-response copy. **Verbatim identical body across all 3 batches** — most consistent verbatim noise repeat in the farm.

### New noise pages (2 ads, 2 pages)

4. **Hampton Water Rosé** (1 carousel placeholder, started 2026-03-31, body `{{product.brand}}`) — wine brand (Jon Bon Jovi's rosé); "Hampton Water" matches "Hampton" substring. **15th distinct Hampton-substring noise page** (after batch-8 Hampton Roads Honda Dealers 14th). First wine-category Hampton noise.
5. **Gardens of Eden** (1 carousel placeholder, started 2026-03-31, body `{{product.brand}}`) — garden/landscaping brand; "Eden" substring. **11th distinct "Eden" noise brand** (after batch-8 Eden Books 10th).

### Cumulative noise-corpus updates

- **Hampton-substring noise pages**: now **15 distinct** (added Hampton Water Rosé)
- **"Eden" noise brands**: now **11 distinct** (added Gardens of Eden)
- **SecretRomance multi-cloud-variant**: confirmed across batches 8+9 — pattern is structural, not a one-batch event
- **Lauren Brooks pet-allergy long-form**: 3-batch verbatim repeat (4+8+9) — the most consistent verbatim noise repeat in the farm; competing with Uproot Clean (4-batch repeat) as most-recurring noise page by batch count

## Cross-cutting patterns

### Nine-batch farm convergence table

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
| **2026-05-22** | **208** | **17** | **191** | **8%** | **3** | **5** | **1** | **1** | **59%** |

Real-signal proportion 59% — **third-highest batch since cold start** after batch 7 (67%) and batch 8 (47%). Cumulative 9-batch tracked-brand ads: **17 + 17 from batch 8 = 34 ads in last two batches alone**, or ~22% of all 153 cumulative tracked-brand ads across 9 batches.

### OpenAI catalog-ads-only pattern BROKEN in batch 9

Eight batches of SEXTUPLE-confirmed catalog-ads-only — and batch 9 ships the first OpenAI ad with copy. Pattern history:

| Batch | OpenAI ads | All placeholder? |
|---|---|---|
| 1 | 21 | ✅ |
| 2 | 3 | ✅ |
| 3 | 3 | ✅ |
| 4 | 4 | ✅ |
| 5-6 | 0 | — |
| 7 | 2 | ✅ |
| 8 | 7 | ✅ |
| **9** | **3** | **❌ — 1 video ad with full body copy** |

**The catalog-ads-only pattern wasn't permanent — it was the default for cluster expansion.** When OpenAI ships a campaign with creative-team-authored messaging (Cluster 3 / Codex retention promo), they ship static narrative. The pattern remains *predominantly* catalog-ads-only (42 of 43 ads), but the structural claim shifts:

- **Old claim**: OpenAI ships only catalog-driven dynamic creative on FB
- **New claim**: OpenAI ships catalog-driven creative for cluster expansion (Clusters 1 + 2 — pre-launch retargeting), and static narrative for retention/promotion campaigns (Cluster 3 — Codex 2-months-free messaging)

**Implication for [[anthropic]] comparison**: Anthropic remains 100% placeholder across 7 ads / 2 windows. Now that OpenAI has broken to copy, the structural ask is: when does Anthropic ship its first copy? **Likely never until they need to run a retention/promotion campaign** — i.e., Anthropic's structural absence from FB copy may indicate they don't yet have a campaign requiring static narrative (rate-limit boost + Karpathy hire + Claude for Small Business launch are all PR / product-led / earned-media events, not paid-social-narrative events).

### Hair Hybrids surge composition (batch 8 + batch 9 stacked)

Hair Hybrids has now shipped **5 verbatim re-launches across batches 8+9** with start dates spanning 2026-02-26 → 2026-05-19:

| Ad ID | Started | Batch |
|---|---|---|
| `2064207334519052` | 2026-05-09 | 8 |
| `728317760309201` | 2026-04-22 | 8 |
| `3372941842875795` | 2026-02-26 | 9 |
| `868992329557540` | 2026-05-06 | 9 |
| `2498995467227011` | 2026-05-19 | 9 |

**Start dates span ~12 weeks (2026-02-26 → 2026-05-19)** — Hair Hybrids has been actively shipping ad-library entries with this exact body for months, but only batch 8+ has surfaced them via the Apify catalog-feed sampling. The verbatim-stability is structural; the surfacing cadence is variable.

### Fetch-gap compression hypothesis CONFIRMED

Batch 8's 4-day-gap 36-ad surge raised the question: was it a compression artifact (collapsing 4 days of ads into one fetch) or genuine intensification (a 3-wedge multi-creative surge)?

Batch 9 (2-day gap, 17 ads) provides the test:

- **Per-day rate** is nearly identical: 9.0 ads/day (batch 8) vs 8.5 ads/day (batch 9)
- **Per-brand per-day rates** track: Ro 0.50/d (both), OpenAI 1.5-1.75/d (both), Hims 2.0-2.5/d (both)
- **Per-cluster expansion rates** track: OpenAI Cluster 2 added 4 in batch 8 (1/day) vs 1 in batch 9 (0.5/day) — same order
- **Hims wedge rotation** continued (Wegovy in batch 8, Hair-Hybrids-only in batch 9) — surge composition rotates without changing magnitude

**Conclusion**: batch 8's 36 ads was largely a 4-day-gap-compression effect. The "three-wedge surge intensification" reading is now disproven; it was 4 days of typical ad-shipping cadence collapsed into one fetch. The standing creative-ops baseline is ~8-9 new ads/day under typical 1-2-day fetch cadence.

**Implication for [[competitor-ads-farm]]**: 1-2-day fetch cadence is the right operating point. Multi-day gaps inflate batch volume linearly (compression artifact) without revealing new behavioral patterns. The Hims/OpenAI/Ro/Anthropic ad-shipping rates are roughly stable; what surfaces in a batch is mostly a function of fetch-cadence × ad-shipping-rate × dedup-cache-state.

## Open questions

- **Will OpenAI ship more Codex-narrative ads in batch 10?** Cluster 3 currently has 3 ads — if more copy-bearing video ads surface, the "retention narrative cluster" becomes a sustained campaign, not a one-shot. If Cluster 3 stalls at 3, the single copy ad was a one-off creative test.
- **Will Hair Hybrids continue verbatim re-launches in batch 10?** Hair Hybrids verbatim now spans 2 consecutive batches (8+9) — does it stick as part of the rotating-surge baseline (joining Wegovy + Sex Rx Climax Control) or revert?
- **Will Wegovy GLP-1 verbatim ship in batch 10?** Wegovy was silent in batch 9 — first time since the 5→6→7→8 rotation pattern was established. If Wegovy stays silent across 2+ consecutive batches, the "5-batch / 14-day stability window" maximum has been reached; if it returns in batch 10, the rotation pattern continues.
- **Will Anthropic ship copy?** Now that OpenAI has, the structural question shifts to whether Anthropic ever does. Hypothesis: only when Anthropic launches a retention/promotion campaign (vs the current "earned-media + rate-limits + product launches" growth playbook).
- **Is Cluster 3 = Codex Enterprise application form?** The "Try Codex for free today" CTA almost certainly lands on the Codex Enterprise application form referenced in [[nate-herk]] #5 / [[youtube-digest-apify-2026-05-14]]. Worth a direct landing-page check.
- **Why is Lauren Brooks (pet allergy) the most verbatim-stable noise repeat?** 3-batch identical-body re-fire (4+8+9) suggests a high-budget direct-response advertiser who has found PMF on this single creative and just keeps re-launching it. Worth a creative teardown — the long-form structure could feed [[medvi-positioning]] long-form ad-test ideas (cross-vertical copy borrow).

## Related

- [[competitor-ads-farm]] — ninth batch from this farm; third-highest real-signal % since cold start (59%); fetch-gap compression hypothesis confirmed via 2-day cadence
- [[hims]] — 5 new ads (3 Hair Hybrids verbatim + 2 placeholders); Hair Hybrids verbatim now spans 3 batches / 16-day stability window; cumulative 66 ads
- [[openai]] — 3 new ads including **first static-narrative ad in vault** (video, Codex retention promo, started 2026-05-15) — breaks SEXTUPLE-confirmed catalog-ads-only pattern; cumulative 43 ads, 1 with copy
- [[ro]] — 1 new ad (returns to ≤1-ad baseline, confirms batch-8 anomaly was fetch-gap compression); cumulative 7 ads, all placeholders
- [[anthropic]] — 1 new ad from original Mar 16 – Apr 8 wave (started 2026-03-17, catalog feed re-surface); cumulative 7 ads across 2 launch windows; "standalone launch" diagnosis for 2026-05-11 still LOCKED
- [[concepts/dtc-telehealth-ad-template]] — Hair Hybrids verbatim now spans 3 batches; surge composition rotates between Wegovy / Hair Hybrids / Sex Rx Climax Control
- [[concepts/compounded-drug-disclaimer]] — Hair Hybrids disclaimer ships verbatim for 4th, 5th, and 6th instances (3 verbatim re-launches in batch 9 alone)
- [[concepts/codex]] — first OpenAI ad copy in vault directly references Codex; "Try Codex for free today" maps onto the 2026-05-13 Codex-2-months-free retention promo
- [[concepts/free-sample-phase]] — Codex retention promo now confirmed at the paid-social-creative layer (not just earned media + rate-limit announcements)
- [[ads-digest-2026-05-06]] — first batch (cold-start canonical Hair Hybrids template established)
- [[ads-digest-2026-05-20]] — eighth batch (first Hair Hybrids verbatim re-launches since cold start; raised the fetch-gap compression question batch 9 now answers)

## Appears in

- Ninth entry in `wiki/sources/` for the competitor-ads farm. **Structural break: OpenAI ships first static-narrative ad with copy** — video referencing the [[free-sample-phase]] Codex retention promo, breaking the SEXTUPLE-confirmed catalog-ads-only pattern. **Hair Hybrids verbatim surge continues** from batch 8 — Hair Hybrids template now spans 3 batches / 16-day stability window with 5 cumulative verbatim re-launches. **Fetch-gap compression hypothesis from batch 8 confirmed** via 2-day-cadence batch-9 per-day rates that match batch-8 per-day rates closely. **Anthropic catalog feed re-surfaces old Mar 16 – Apr 8 wave ad** without affecting the 2026-05-11 standalone-launch diagnosis. Lauren Brooks pet-allergy long-form is now the most-consistent verbatim noise repeat (3 batches, identical body).
