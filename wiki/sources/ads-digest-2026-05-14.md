---
title: FB Ads Digest — Competitor brands — 2026-05-14
category: source
summary: Fifth competitor-ads farm batch — 13 new FB Ad Library entries (202 fetched, 189 dedup-skipped, 94%); Hims runs **two verbatim template re-launches in one batch** (Sex Rx + Climax Control from the 2026-05-06 template + Wegovy GLP-1 from the same template) — Wegovy template now verbatim across 3 batches (2026-05-06 → 2026-05-12 → 2026-05-14, 8-day stability window); Anthropic ships **first new ad since 2026-05-06** (placeholder carousel started 2026-05-11) — confirms catalog-ads-only pattern continues for Anthropic too; OpenAI returns **0 new ads for the first time in 5 batches** — May 8 cluster appears fully dedup-cached; 10 of 13 ads (77%) are noise dominated by an "Eden" substring cluster (Evereden + Herb'N Eden + Eden Brothers + Aelfric Eden + Edens Garden Essential Oils — 9 ads from 5 distinct unrelated brands); Uproot Clean returns as a 5th-batch repeat noise page; brand-name filter still untuned, fifth consecutive batch
tags: [fb-ads, ad-library, hims, anthropic, dtc, competitor-ads, catalog-ads, dedup, farm-tuning, template-stability, eden-noise-cluster]
sources: 1
source_path: raw/ads/digest-2026-05-14.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-14
updated: 2026-05-14
---

# FB Ads Digest — 2026-05-14

Fifth batch from the [[competitor-ads-farm]]. **13 new ads, 189 dedup-skipped** out of 202 fetched across 8 tracked brand keywords (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Volume back down from batch 4** — 13 new / 202 fetched / 94% dedup-skipped. Five-batch steady state firmly established in the **6-22 new ads/day** band.
- **Hims runs TWO verbatim template re-launches in a single batch** — Sex Rx + Climax Control (started 2026-04-21, ID `3275837862576962`) AND Wegovy GLP-1 (started 2026-05-04, ID `956466943766183`). Both are word-for-word re-runs of the 2026-05-06 templates. The Wegovy template is now verbatim across **3 batches** (2026-05-06, 2026-05-12, 2026-05-14) — an 8-day verbatim-stability window. The "inside-structure A/B dominates over template variation" hypothesis from batch 4 is now multi-instance confirmed.
- **Anthropic ships first new ad since 2026-05-06** — 1 carousel ad, headline `{{product.name}}`, body `{{product.brand}}`, started 2026-05-11 (ID `1521217572752360`). Same dynamic-creative-only pattern as the original 5 ads from batch 1. **6 total Anthropic ads tracked, 0 with teardown-able copy** — the catalog-ads-only AI-lab pattern is now confirmed for Anthropic across two distinct launch windows (Mar 16 – Apr 8 + 2026-05-11), not just OpenAI.
- **OpenAI returns 0 new ads for the first time in 5 batches** — the May 8 cluster (which expanded to 6 ads across batches 3+4) appears fully dedup-cached now. Cumulative remains **31 OpenAI ads tracked, 0 with copy**. First batch where the OpenAI catalog stream is silent.
- **Signal-to-noise: 23%** — 3 of 13 ads tracked-brand (2 Hims + 1 Anthropic). 10 are noise dominated by an **"Eden" substring cluster of 5 distinct unrelated brands**: Evereden (1) + Herb'N Eden (2) + Eden Brothers (4) + Aelfric Eden (1) + Edens Garden Essential Oils (1) = 9 noise ads. Plus Uproot Clean (1, repeat from batches 2+4). Noise-rate trend: 65% → 82% → 50% → 69% → **77%**. Mean ~69%.
- **Eden Brothers re-fires as repeat-noise multiplier** — same noise page as batch 1 (4 ads in batch 1, now 4 more in batch 5) — first noise page to multi-fire across non-consecutive batches. The dedup state is per-ad-ID, so the same noise page can keep emitting fresh creative.
- **Brand-name filter still untuned** — fifth batch with the same outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-14.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 202 • New: 13 • Dedup-skipped: 189

## Tracked-brand creative inventory

### Hims (2 new ads) — TWO verbatim template re-launches in one batch

#### Hims #1 — Sex Rx + Climax Control (verbatim 2026-05-06 template)

- Format: unknown (likely catalog-dynamic-creative-overlay)
- Title: (no headline)
- Started: 2026-04-21
- ID: `3275837862576962`

**Body text (verbatim):**

> The 2-in-1 pill to get harder, and go longer. Sex Rx + Climax Control combines tadalafil shown to result in more satisfying erections and help men last longer, plus PE treatment. Get started today—100% online with a free consultation.
>
> Why Hims?
> 🤩Daily pill options for spontaneous sex
> 🧑‍⚕️Prescribed by licensed providers
> 📦100% online, free discreet shipping
>
> [compounded-drug disclaimer block]

This is the **same Sex Rx + Climax Control template documented in [[ads-digest-2026-05-06]]** for Wedge 3 SKU #2 — same hook line ("The 2-in-1 pill to get harder, and go longer"), same three-bullet block, same emoji selection (🤩 / 🧑‍⚕️ / 📦), same 100%-online closer. The compounded-drug disclaimer block matches the canonical [[compounded-drug-disclaimer]] pill variant verbatim.

#### Hims #2 — Wegovy GLP-1 (third verbatim re-launch)

- Format: unknown
- Title: (no headline)
- Started: 2026-05-04
- ID: `956466943766183`

**Body text (verbatim):**

> Get Wegovy® with Hims, plus access to provider-led care, tailored treatment plans, and ongoing support designed around your lifestyle.
>
> Why Hims?
> ✅ FDA-approved GLP-1 pill and pens available
> ✅ Medication as low as $149/mo—membership fee of $39 for first month, $149 thereafter
> ✅ 100% online
>
> Your goals. Your plan. Your pace.
>
> See if you qualify today.

This is the **third verbatim re-launch** of the canonical Wegovy GLP-1 template. The template now has verbatim instances in:

| Batch | Date | Ad ID | Started |
|---|---|---|---|
| 1 | 2026-05-06 | (per [[ads-digest-2026-05-06]]) | (early Apr launch wave) |
| 4 | 2026-05-12 | `3567971296700086` | 2026-05-07 |
| 5 | 2026-05-14 | `956466943766183` | 2026-05-04 |

**8-day verbatim-stability window.** No structural change across three Wegovy ads spanning 8 days of launch dates.

> ⚠️ Two verbatim template re-launches in a single batch is the most-evidenced confirmation of the [[dtc-telehealth-ad-template]] template-stability hypothesis to date. Hims has now demonstrated **multi-instance template re-use within the same batch** — meaning the standing creative inventory for Wedge 1 (GLP-1) and Wedge 3 (Sex Rx Climax Control) ships the *same* skeleton across multiple ad-library entries simultaneously. Inside-structure A/B testing (visual asset, headline overlay, audience targeting) is the only variation surface; the body copy is locked.

→ See [[entities/hims]] for cumulative inventory.

### Anthropic (1 new ad) — first new ad since 2026-05-06; placeholder pattern continues

- Format: carousel
- Title: `{{product.name}}`
- Body: `{{product.brand}}`
- Started: 2026-05-11
- ID: `1521217572752360`

**Significance:** First new Anthropic FB ad in 5 batches (since the original 5 ads from batch 1, all started Mar 16 – Apr 8, 2026). The new ad started **2026-05-11 — three days before this batch fetched** — so it represents a fresh launch, not a backlog catch-up.

**Pattern:** Identical to the 2026-05-06 Anthropic ads — pure dynamic-creative-only carousel with `{{product.name}}` headlines and `{{product.brand}}` bodies. **Zero static narrative copy.** Same as the [[openai]] catalog-ads-only pattern.

**Cumulative Anthropic ad inventory: 6 total across two distinct launch windows (Mar 16 – Apr 8 wave + 2026-05-11), 0 with teardown-able copy.** The catalog-ads-only AI-lab pattern is now confirmed across two launch windows for Anthropic — not just OpenAI's four-batch evidence. Both AI labs ship only catalog/product-feed-driven dynamic creative on FB.

→ See [[entities/anthropic]] for cumulative inventory.

### OpenAI, Ro, Henry Meds, Hampton Founders, DealMachine, Eden (0 new ads each)

**OpenAI 0 new ads is the headline absence.** Cluster 2 (May 8) was actively expanding from 2 → 6 ads across batches 3+4. Now silent for the first time in 5 batches. Either:
- The May 8 cluster has fully dedup-cached against the 6 known ads
- OpenAI has paused the cluster
- A new cluster will appear in the next 1-2 batches

Cumulative OpenAI: still **31 ads tracked, 0 with copy.** No template change to evaluate.

Ro fifth-batch silence continues — bare-"Ro" filter remains net-negative across 5 batches now.

## False positives ("brand-name match" noise)

10 of 13 ads (77%) are off-target. Noise-rate trend across five batches: 65% → 82% → 50% → 69% → **77%**. Mean ~69% — squarely on the established baseline.

### "Eden" substring cluster — 9 ads from 5 distinct unrelated brands (NEW pattern)

The single most concentrated noise pattern across all five batches. The bare-"Eden" search (intended for the GLP-1 telehealth Eden) is structurally unable to disambiguate from:

| Page | Category | Ad count | Substring root |
|---|---|---|---|
| Evereden | kid/baby skincare | 1 | "Eden" inside "Evereden" |
| Herb'N Eden | natural handmade soaps | 2 | exact "Eden" substring |
| Eden Brothers | flower bulbs / seeds | 4 | exact "Eden" substring (REPEAT from batch 1) |
| Aelfric Eden | fashion / hoodies | 1 | exact "Eden" substring (REPEAT from batch 1) |
| Edens Garden Essential Oils | essential oils | 1 | exact "Eden" substring |

**5 distinct unrelated brands generating 9 noise ads in a single batch.** The "Eden" substring noise floor is structurally larger than other tracked brands' substring noise floors because "Eden" is both (a) a common English first name and (b) a common DTC-brand prefix/suffix in skincare/wellness/fashion.

**Eden Brothers (4 ads) re-fires across non-consecutive batches** — same noise page as batch 1 (which had 14 ads). First noise page to multi-fire across non-consecutive batches in this farm. Per-ad-ID dedup means the same page can keep emitting fresh creative; this is a recurring failure mode for high-volume noise pages.

> ⚠️ **The "Eden" substring noise cluster is structurally large.** The bare-"Eden" filter, like the bare-"Ro" filter, is now demonstrably net-negative — 0 telehealth-Eden signal across 5 batches, dozens of unrelated noise ads. Page-ID allow-listing for the actual telehealth Eden is the only structurally-safe filter.

### Uproot Clean (1 ad) — repeat noise page (3rd batch appearance)

- Page: *Uproot Clean*
- Format: video
- Started: 2026-05-01
- Substring root cause: "ro" inside "Uproot"
- Long-form direct-response copy: pet-odor / washing-machine-biofilm / WMT008 product, 60-day money-back guarantee, "100K pet parents" social proof

**Third batch appearance** (also in 2026-05-10 and 2026-05-12). Like Lauren Brooks (4 ads in batch 4), the copy is structurally interesting as a long-form direct-response contrast pattern to Hims' three-bullet template — *biofilm science explanation + checklist (No scrubbing / No outdated tricks / No rewashing) + 60-day guarantee + social proof + direct-CTA URL*. Filed as a copy-pattern observation even though Uproot Clean isn't in the competitive set.

## Cross-cutting patterns

### Hims template stability — 5 batches in, multi-instance verbatim re-use within a single batch

| Batch | Date | New Hims ads | Wedge instances | Structural change |
|---|---|---|---|---|
| 1 | 2026-05-06 | 45 | All 3 wedges (GLP-1 / Hair / Sex Rx 3-SKU initial inventory) | Initial template inventory |
| 2 | 2026-05-10 | 2 | Hair + Sex Rx (Hard Mints — 4-bullet variant) | First and only structural innovation: 4-bullet variant for high-objection ED non-responder category |
| 3 | 2026-05-11 | 0 | (fully dedup-cached) | — |
| 4 | 2026-05-12 | 1 | GLP-1 (verbatim re-launch #1) | None |
| 5 | 2026-05-14 | 2 | **GLP-1 (verbatim re-launch #2) + Sex Rx Climax Control (verbatim re-launch)** | None |

**The multi-instance verbatim re-use pattern in batch 5 is the strongest single-batch confirmation to date.** Two distinct wedges, both shipping the *same* templates as their 2026-05-06 originals, in the same batch. Inside-structure A/B testing (likely visual asset, headline overlay, audience targeting, disclaimer-wording variants per [[compounded-drug-disclaimer]]) is the only variation surface; **body copy is locked across all batches except for the Hard Mints four-bullet structural innovation in 2026-05-10.**

### Anthropic catalog-ads-only — confirmed across two distinct launch windows

| Window | Ads | Started dates |
|---|---|---|
| 1 (initial wave) | 5 | Mar 16 – Apr 8, 2026 |
| 2 (this batch) | 1 | 2026-05-11 |
| **Total** | **6** | **2 distinct windows** |

A single new ad in a fresh launch window with the **same template** rules out "the original 5 ads were a one-time test" — Anthropic, like OpenAI, ships only catalog-driven dynamic creative on FB. **The "both AI labs ship catalog-ads-only" pattern is now multi-window confirmed for both vendors.**

### OpenAI cumulative remains at 31 ads (0 new this batch)

| Batch | Date | OpenAI ads | Cumulative |
|---|---|---|---|
| 1 | 2026-05-06 | 21 | 21 |
| 2 | 2026-05-10 | 3 | 24 |
| 3 | 2026-05-11 | 3 | 27 |
| 4 | 2026-05-12 | 4 | 31 |
| 5 | 2026-05-14 | **0** | **31** |

First OpenAI silence in the farm. Worth watching whether batch 6 surfaces a new cluster or extends the silence.

### Five-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Real-signal % |
|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 23% |

Steady-state dedup is **92-97%**. New-ad volume per batch in the **6-22 band** (mean ~12). Real-signal proportion in the **18-50% band** (mean ~31%). Mean noise rate ~69%. Five-batch convergence is now decisive.

### Non-substring noise — none in batch 5

Batch 5 produced **no new non-substring noise events**. Every noise page in this batch traces to a tracked-brand substring (mostly "Eden", one "ro" via Uproot Clean). The Adobe Acrobat (batch 3) + Romance miniseries (batch 4) non-substring events remain at 2 of 5 batches (40%) — non-zero but not constant.

The "Eden" substring noise cluster (9 ads / 5 brands in batch 5 alone) is the dominant noise source for batch 5 — a substring-cluster pattern, not a non-substring pattern. Page-ID allow-listing remains the structurally-safe fix; substring filtering with smarter exclusions for "Eden Brothers / Aelfric Eden / Evereden / Edens Garden / Herb'N Eden" would partially close batch 5's noise but not the non-substring failure mode from batches 3+4.

## Open questions

- **Is OpenAI silence in batch 5 transient or structural?** If silent again in batches 6-7, the May 8 cluster is fully cached. If a new cluster appears in batches 6-7, the catalog-ads-only strategy is still actively expanding.
- **Is Anthropic's 2026-05-11 ad pointing to the same surface as the original 5?** Worth one manual click-through to identify the destination (claude.ai? Code? API? Enterprise?). If the destination has changed, the catalog-ads strategy is being repointed at a new product surface.
- **The verbatim multi-wedge re-launch in batch 5** — is this a coincidence (two ads happened to ship the same week) or a coordinated re-launch (Hims pushes verbatim re-runs across multiple wedges in waves)? Worth checking the next 2-3 batches for whether multi-wedge re-launches cluster temporally.
- **Is "Eden Brothers" multi-fire across batches 1+5 (skipping 2+3+4) a sign of seasonal-campaign cadence** (gardening = spring planting season)? Their batch 1 ads were also dahlia-tuber spring-planting creative.
- **Uproot Clean (3 of 5 batches)** — is the long-form biofilm copy a tested-and-converting template worth modeling for any [[medvi-positioning]] long-form ad?

## Related

- [[competitor-ads-farm]] — fifth batch from this farm; five-batch steady state firmly established
- [[hims]] — TWO verbatim template re-launches in one batch (Sex Rx Climax Control + Wegovy GLP-1)
- [[anthropic]] — first new ad since 2026-05-06; catalog-ads-only confirmed across 2 launch windows
- [[openai]] — 0 new ads for the first time in 5 batches; cumulative still 31
- [[dtc-telehealth-ad-template]] — multi-instance verbatim re-use within a single batch is the strongest stability confirmation to date
- [[compounded-drug-disclaimer]] — both Hims ads use canonical pill variants
- [[ads-digest-2026-05-06]] — first batch (183 new, cold start)
- [[ads-digest-2026-05-10]] — second batch (22 new, Hard Mints + OpenAI catalog confirmation #2)
- [[ads-digest-2026-05-11]] — third batch (6 new, 50% noise, OpenAI #3, Adobe Acrobat non-substring noise discovery)
- [[ads-digest-2026-05-12]] — fourth batch (16 new, 69% noise, OpenAI #4, first verbatim Hims re-launch + Romance miniseries non-substring noise)

## Appears in

- Fifth entry in `wiki/sources/` for the competitor-ads farm. Marks five-batch convergence with: (1) two simultaneous verbatim Hims template re-launches confirming the multi-instance template-reuse hypothesis, (2) Wegovy template now verbatim across 3 batches (8-day stability window), (3) Anthropic catalog-ads-only pattern confirmed across 2 distinct launch windows (matching OpenAI's 2-cluster pattern), (4) first OpenAI silence since farm cold-start, (5) "Eden" substring noise cluster (9 ads / 5 unrelated brands) as the dominant noise pattern of this batch, (6) first noise page to multi-fire across non-consecutive batches (Eden Brothers, batches 1+5).
