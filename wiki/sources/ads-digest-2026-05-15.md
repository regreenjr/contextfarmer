---
title: FB Ads Digest — Competitor brands — 2026-05-15
category: source
summary: Sixth competitor-ads farm batch — 3 new FB Ad Library entries (203 fetched, 200 dedup-skipped, 98.5%) — thinnest meaningful signal batch since cold start AND **first 100%-noise batch** (0 of 3 tracked-brand); all six tracked anchors (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton Founders, DealMachine) return 0 new ads — Hims goes silent for the second time in 6 batches (first since batch 3 2026-05-11), OpenAI extends silence to 2 consecutive batches (May 8 cluster confirmed fully dedup-cached), Anthropic falls silent again after the single 2026-05-11 carousel; the 3 new ads are: **Eden Plastic Surgery Miami (2 ads — NEW sixth distinct "Eden" substring brand)** — Miami cosmetic-surgery clinic running long-form testimonial copy for the EVELift® facelift; **Heirloom Roses (1 ad)** — gardening carousel matched via "Ro" inside "Roses" (first time a plural "Roses" surfaces as substring root cause); brand-name filter still untuned, sixth consecutive batch
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, all-noise-batch, eden-noise-cluster, ro-noise-cluster, silence-batch]
sources: 1
source_path: raw/ads/digest-2026-05-15.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-15
updated: 2026-05-15
---

# FB Ads Digest — 2026-05-15

Sixth batch from the [[competitor-ads-farm]]. **3 new ads, 200 dedup-skipped** out of 203 fetched across 8 tracked brand keywords (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **First all-noise batch.** 0 of 3 new ads are tracked-brand. Six-batch noise-rate trend: 65% → 82% → 50% → 69% → 77% → **100%**. New batch-mean ~74%.
- **Thinnest signal batch since cold start.** 3 new ads / 203 fetched / 98.5% dedup-skipped — highest dedup rate of any batch. Volume drops below batch 3's 6 new ads.
- **Universal tracked-brand silence.** All 8 tracked anchors (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton Founders, DealMachine) ship 0 new ads. First batch with simultaneous silence across all tracked brands.
- **Hims goes silent for the second time** (first since batch 3 2026-05-11). The two-wedge verbatim re-launch surge of batch 5 (Sex Rx Climax Control + Wegovy GLP-1) appears to have exhausted the active creative inventory for one cycle. Standing inventory: 50 cumulative ads, no structural changes.
- **OpenAI extends silence to 2 consecutive batches.** May 8 cluster now confirmed **fully dedup-cached** — not transient single-batch absence as flagged in batch 5. Cumulative remains **31 ads, 0 with copy**. Either between launches or paused.
- **Anthropic returns to silence after single 2026-05-11 carousel.** No follow-up cluster yet. Cumulative remains 6 ads across 2 windows.
- **NEW noise brand: Eden Plastic Surgery Miami (2 ads)** — Miami cosmetic surgery clinic. Sixth distinct "Eden" substring brand surfaced via this farm (after Eden Brothers, Aelfric Eden, Evereden, Herb'N Eden, Edens Garden Essential Oils, Eden Munoz). The "Eden" substring noise corpus is now structurally larger than any other tracked-brand substring corpus.
- **NEW noise root cause: "Roses" pluralization.** Heirloom Roses (1 carousel ad) matches via "Ro" inside "Roses" — first time a plural-noun pluralization of "Ro" surfaces as substring root cause in this farm.
- **Brand-name filter still untuned — sixth consecutive batch.** Outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-15.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 203 • New: 3 • Dedup-skipped: 200 (98.5%)

## Tracked-brand creative inventory

### All brands (0 new ads)

For the first time in 6 batches, **all 8 tracked-brand anchors return 0 new ads**. The full silence list:

| Brand | New | Cumulative | Last new ad |
|---|---|---|---|
| [[hims]] | 0 | 50 | 2026-05-14 (Sex Rx Climax Control + Wegovy GLP-1, verbatim) |
| [[ro]] | 0 | 3 | 2026-05-10 (placeholder) |
| Eden (telehealth) | 0 | 0 | (never appeared) |
| [[henry-meds]] | 0 | 0 | (never appeared) |
| [[anthropic]] | 0 | 6 | 2026-05-14 (carousel placeholder, started 2026-05-11) |
| [[openai]] | 0 | 31 | 2026-05-12 (May 8 cluster expansion, 4 ads) |
| [[hampton-founders]] | 0 | (initial batch) | 2026-05-06 |
| DealMachine | 0 | 0 | (never appeared) |

**Hypothesis:** Batches 5 + 6 may form a complementary pair — batch 5 surged with 3 tracked-brand ads (Hims ×2 + Anthropic ×1) plus 9 Eden-cluster noise ads; batch 6 produces near-zero new volume across the board. The dedup pipeline is mature enough that batch-to-batch new-ad count is now dominated by *whether tracked brands shipped fresh creative in the prior 24-48hrs*, not by the actor's fetch volume (which stays in the 187-207 range every batch).

## False positives ("brand-name match" noise) — 100% of batch 6

All 3 new ads are off-target. Both noise root causes are substring matches against the bare "Eden" and "Ro" filters.

### Eden Plastic Surgery Miami (2 ads) — NEW sixth distinct "Eden" brand

A Miami-based cosmetic surgery clinic, **clearly not the GLP-1 telehealth Eden** the farm is meant to track. Two long-form video ads documenting patient transformations.

**Ad #1** (ID `1526702065958496`, video, started 2026-02-19): *"Pamela's Natural Refresh"* — 60-year-old patient from Oklahoma; testimonial-style narrative pitching the **EVELift®** facelift + Four Point Support necklift under local anesthesia + IV sedation, with hashtag block `#EVELift #FaceliftUnderLocal #NaturalResults #MinimalDowntime`.

**Ad #2** (ID `4036289083260183`, video, started 2026-02-19): *"You're 70 just for the next 2 hours"* — Donna from Atlanta; menu-driven copy listing **5 procedures in a single visit** (EVELift® + CO2 laser + stem cell therapy + under-eye volume + IPL chest rejuvenation) followed by a 9-emoji benefits checklist (Effortless Comfort / Safe & Effective / Transformative / Natural Results / Swift Recovery / Hassle-Free / Minimal Bruising / Unmatched Care + an Around-the-Clock Support sub-bullet) and direct phone + DM CTA.

**Substring root cause:** exact "Eden" in "Eden Plastic Surgery Miami." Same root cause as Eden Brothers / Aelfric Eden / Evereden / Herb'N Eden / Edens Garden Essential Oils / Eden Munoz.

**Cumulative "Eden" substring noise corpus across 6 batches:**

| Page | Category | Total ads | First seen | Repeats |
|---|---|---|---|---|
| Eden Brothers | flower bulbs / seeds | 8 | batch 1 | batches 1+5 |
| Aelfric Eden | fashion / hoodies | 2 | batch 1 | batches 1+5 |
| Eden & Om | bamboo sheets | 13 | batch 1 | single batch |
| UNC Health Rockingham at Eden NC | hospital | 1 | batch 1 | single batch |
| Eden Munoz | Mexican banda singer | 1 | batch 3 | single batch |
| Evereden | kid skincare | 1 | batch 5 | single batch |
| Herb'N Eden | natural soaps | 2 | batch 5 | single batch |
| Edens Garden Essential Oils | essential oils | 1 | batch 5 | single batch |
| **Eden Plastic Surgery Miami** | **cosmetic surgery** | **2** | **batch 6 (NEW)** | **single batch** |

**Nine distinct unrelated "Eden" brands across 6 batches.** Zero ads from the actual GLP-1 telehealth Eden across all 6 batches. The bare-"Eden" filter has produced ~31 noise ads and 0 signal ads — the most decisively net-negative tracked-brand filter in this farm.

> ⚠️ Copy-pattern observation worth filing: Eden Plastic Surgery Miami's "Donna" ad is a **9-emoji checklist long-form testimonial** — structurally similar in *form* (long bullet list) to Hims' three-bullet template but ~3x the bullet count and zero compliance language. Cosmetic-surgery DTC plays by different ad-library compliance rules than compounded-drug DTC; the longer bullet list is a category artifact, not a transferable copy lesson for [[medvi-positioning]]. Filed for record, not for emulation.

### Heirloom Roses (1 ad) — NEW noise root cause: "Roses" pluralization

A gardening carousel from page "Heirloom Roses" titled *"Climbing Rose Plants"* (ID `1205748091105679`, started 2026-01-19, carousel format). Body copy is engagement-bait: *"What climbing rose would you recommend to another gardener? Share your thoughts in the comments!"*

**Substring root cause:** exact "Ro" prefix in **"Roses"** — first time a plural noun pluralization of "Ro" surfaces as substring root cause in this farm. Prior "Ro" noise was rooted in proper nouns ("Roads & Kingdoms," "Roseionly," "KaRoL G," "Uproot," "BaBylissPRO," "Brooks") or compound brand names. Plural-noun substring expansion confirms the bare-"Ro" filter's noise floor is **structurally unbounded** — virtually any English text containing "ro" as letter sequence can match, including common pluralizations of one-syllable nouns.

**Cumulative "Ro" substring noise corpus across 6 batches** (partial list): Roads & Kingdoms, Roseionly, KaRoL G, Uproot Clean (× 3 batches), BaBylissPRO, Lauren Brooks (4 ads), Builders Protein Bars, Rockfest, ProTyres Oradea, Modlet.ro, **Heirloom Roses (batch 6 NEW)**. Plus the actual Ro signal: 3 placeholder ads across batches 1+2.

**Signal-to-noise across 6 batches for bare-"Ro": 3 placeholder ads of signal, 20+ noise ads** — confirming bare-"Ro" is decisively net-negative for the sixth consecutive batch.

## Cross-cutting patterns

### Six-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Real-signal % |
|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 23% |
| **2026-05-15** | **203** | **3** | **200** | **1.5%** | **0** | **0** | **0** | **0%** |

Steady-state dedup is **92-98.5%** (band widens with batch 6's record 98.5%). New-ad volume **3-22 band** (mean ~10.5). Real-signal proportion **0-50% band** (new mean ~26%). Mean noise rate ~74%. Six-batch convergence holds.

### Universal silence across tracked brands

This is the first batch with **zero new ads from any tracked brand**. Interpreting cautiously:

- Not a fetch-volume issue — 203 fetched is consistent with batches 1-5 (mean ~198, σ ~8)
- Not a dedup-pipeline error — 200 dedup-skipped is the highest count ever, suggesting the pipeline is correctly identifying recurring ads
- Most likely **a fresh-creative timing artifact** — batch 5 surged with two-wedge Hims re-launches + Anthropic carousel; if those covered the active inventory, the next 24-48hrs would naturally produce thin volume
- Watch batches 7-8 to see if the silence is single-batch (timing) or multi-batch (structural shift — campaign pauses, end-of-quarter ad freeze, etc.)

### OpenAI silence promotes from transient (batch 5) to confirmed (batch 6)

Batch 5 flagged OpenAI's 0-new-ads as ambiguous (May 8 cluster cached vs paused vs between-launch). **Batch 6's continued silence promotes the diagnosis to "May 8 cluster fully dedup-cached at 6 ads."** Two consecutive silent batches with no new May 8 IDs eliminates the "transient batch-timing artifact" hypothesis.

Open question for batches 7-8: does a new cluster (May 15+ launch dates) appear, or does OpenAI's FB catalog stream stay silent for the medium term? Either outcome reframes the catalog-ads-only behavioral baseline:
- New cluster → strategy is actively scaling
- Continued silence → strategy is on hold (potentially correlated with the 2026-05-13 [[free-sample-phase]] retention promo redirecting attention)

### Anthropic returns to silence

The 2026-05-14 batch surfaced 1 new Anthropic ad (started 2026-05-11) — interpreted at the time as the start of a new launch window. Batch 6 produces no follow-up ad. Two interpretations:

- **One-off ad** — the 2026-05-11 carousel was a standalone launch, not a cluster opener. Cumulative inventory stays at 6 ads across 2 narrow windows.
- **Slow cluster** — additional ads from the 2026-05-11+ window will appear in batches 7-8 as catalog feed expands.

Either way, the catalog-ads-only AI-lab pattern stands. The pacing question is when the next cluster shipt — not whether the strategy persists.

### Hims goes silent for the second time in 6 batches

Hims silence in batch 6 mirrors batch 3 (2026-05-11) — both follow batches that surged with verbatim template re-launches. Read as **inventory-exhaustion timing**, not structural shift. The standing creative inventory of [[dtc-telehealth-ad-template]] instantiations cycles in waves; once a wave ships (e.g., batch 5's two-wedge multi-instance re-launch), the next 24-48hrs naturally produce thin new-ad volume until the next wave begins.

Hims inventory standing patterns remain unchanged: 3 wedges, 4 Sex Rx SKUs, three-bullet template default + four-bullet variant for Hard Mints, Wegovy template verbatim-stable across 3 batches.

## Open questions

- **Will the universal-silence pattern persist or revert?** If batches 7-8 stay below 10 new ads with continued silence across all tracked brands, the farm is in genuine steady-state low-water-mark mode. If batches 7-8 surge to 15+ new ads, batch 6 was a timing trough.
- **Is the OpenAI silence structural?** Two batches of silence after a 4-batch active campaign warrants a manual check of the OpenAI FB ad library page in 1-2 weeks to confirm no new launches.
- **Should "Eden Plastic Surgery Miami" be excluded from "Eden" substring matches via blocklist?** It's the 9th distinct "Eden" brand surfaced; the bare-"Eden" filter has produced 31 noise ads and 0 signal ads across 6 batches. Page-ID blocklisting all 9 is closer to a full fix than further substring tuning.
- **Is the 100% noise rate a one-off or convergence point?** Batch 6 is the first 0%-signal batch. Mean signal rate across 6 batches drops to ~26% (from ~31% at batch 5). The signal-rate distribution has long tails; a single 0-signal batch is consistent with the mean if 2-3 future batches return to 30-50%.

## Related

- [[competitor-ads-farm]] — sixth batch from this farm; first 100%-noise batch
- [[hims]] — 0 new ads (2nd Hims silence batch in 6, first since 2026-05-11)
- [[anthropic]] — 0 new ads (returns to silence after single 2026-05-11 carousel in batch 5)
- [[openai]] — 0 new ads (silence promotes to confirmed: May 8 cluster fully dedup-cached)
- [[ro]] — 0 new ads (6th consecutive silence batch); Heirloom Roses adds "Roses" pluralization as new substring root cause
- [[ads-digest-2026-05-06]] — first batch (183 new, cold start)
- [[ads-digest-2026-05-10]] — second batch (22 new, Hard Mints + OpenAI catalog confirmation #2)
- [[ads-digest-2026-05-11]] — third batch (6 new, 50% noise, OpenAI #3, Adobe Acrobat non-substring noise discovery)
- [[ads-digest-2026-05-12]] — fourth batch (16 new, 69% noise, OpenAI #4, first verbatim Hims re-launch + Romance miniseries non-substring noise)
- [[ads-digest-2026-05-14]] — fifth batch (13 new, 77% noise, OpenAI silence #1 transient, Anthropic returns w/ 1 ad, Hims two-wedge verbatim re-launch surge)

## Appears in

- Sixth entry in `wiki/sources/` for the competitor-ads farm. Marks **two firsts**: (1) first 100%-noise batch (0 of 3 ads tracked-brand) and (2) first batch with universal silence across all 8 tracked anchors. Also adds two NEW substring noise brands — Eden Plastic Surgery Miami (9th "Eden" cluster member) and Heirloom Roses (first plural-noun "Roses" → "Ro" substring expansion). Promotes OpenAI's batch-5 silence from "transient" to "May 8 cluster fully dedup-cached" via two-batch confirmation.
