---
title: FB Ads Digest — Competitor brands — 2026-05-12
category: source
summary: Fourth competitor-ads farm batch — 16 new FB Ad Library entries (207 fetched, 191 dedup-skipped); OpenAI ships 4 more dynamic-creative-only carousels (catalog-ads-only pattern QUADRUPLE-confirmed → 31 total ads, 0 narrative); Hims reuses the canonical Wegovy GLP-1 template in a fresh 2026-05-07 launch — first Hims ad since 2026-05-10 confirms the template is the standing creative, not a one-off; 11 of 16 ads (69%) are noise — including a SECOND non-substring-match noise pattern (Romance miniseries, 3 ads) reinforcing the 2026-05-11 Adobe Acrobat finding that the Apify actor surfaces unsolicited adjacent brands; Lauren Brooks long-form pet-allergy direct-response (4 ads) surfaces as a copy-pattern outlier — strong confession/long-narrative structural contrast to Hims' three-bullet template
tags: [fb-ads, ad-library, openai, hims, dtc, competitor-ads, catalog-ads, dedup, farm-tuning, long-form-copy]
sources: 1
source_path: raw/ads/digest-2026-05-12.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-12
updated: 2026-05-12
---

# FB Ads Digest — 2026-05-12

Fourth batch from the [[competitor-ads-farm]]. **16 new ads, 191 dedup-skipped** out of 207 fetched across 8 tracked brand keywords (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Volume back up modestly** — 16 new ads / 207 fetched / 92% dedup-skipped. After the 2026-05-11 thin batch (6 new) the farm picks back up but stays well below the 2026-05-06 cold-start volume. Steady-state is now visibly the 6-22 new ads/day band.
- **OpenAI catalog-ads-only QUADRUPLE-confirmed** — 4 more `{{product.name}}` / `{{product.brand}}` carousels, all started 2026-05-08 (same launch cluster as the 3 ads in batch 3). Cumulative: **31 OpenAI ads tracked across 4 batches, 0 with teardown-able copy.** The strategy is now the most-evidenced behavioral baseline in this vault.
- **Hims runs the Wegovy GLP-1 template fresh** — 1 new ad (started 2026-05-07, ID `3567971296700086`) reusing the canonical [[dtc-telehealth-ad-template]] three-bullet GLP-1 instantiation **verbatim** from the 2026-05-06 batch. First Hims ad since 2026-05-10 — confirms the template is the standing creative (not a stale-campaign artifact) and Hims A/B-tests inside structure rather than re-templating.
- **Signal-to-noise: ~31%** — 5 of 16 ads are tracked-brand (4 OpenAI + 1 Hims). 11 are noise (3 Romance miniseries + 4 Lauren Brooks + 1 BabylissPRO Barber + 1 Builders Protein Bars + 1 Hampton Roads Transit + 1 Blake Hampton). Noise-rate trend: 65% → 82% → 50% → **69%**.
- **NEW non-substring noise pattern: Romance miniseries (3 ads)** — bizarre serialized fiction app ad ("I rise from scavenger to king with alien tech") with no tracked-brand substring match. **Second non-substring noise after [[ads-digest-2026-05-11]]'s Adobe Acrobat.** The Apify actor returns unsolicited adjacent brands at a non-zero rate; substring filtering can never close the noise floor on its own.
- **Lauren Brooks long-form direct-response (4 ads)** — pet allergy long-form confession copy ("Please STOP buying allergy meds for your dog... $3400... NOTHING"). Substring root cause: "Brooks" contains "ro". Structurally interesting as a **contrast pattern** to Hims' three-bullet template — confession hook + price-anchored loss-aversion + chronological treatment-failure cascade + the WAS-supposed-to-help/ACTUALLY-failed reveal pattern. Filed as a copy-pattern observation even though Lauren Brooks isn't in the competitive set.
- **Brand-name filter still untuned** — fourth batch with the same outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-12.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 207 • New: 16 • Dedup-skipped: 191

## Tracked-brand creative inventory

### OpenAI (4 new ads) — catalog-ads-only QUADRUPLE-confirmed

All four ads:
- Format: carousel
- Title: `{{product.name}}`
- Body: `{{product.brand}}`
- Started: 2026-05-08 (all four — same launch cluster as batch 3's two May 8 ads)
- IDs: `984940781138942`, `1609127340383653`, `998103256504956`, `1413623514137961`

This is now the **fourth straight batch** of identical-template OpenAI catalog creative. The 2026-05-08 launch cluster previewed in batch 3 (2 ads) expands here to 6 total ads (2 from batch 3 + 4 here). The cluster is real, the template is unchanged from the Apr 2-21 wave.

> ⚠️ Pattern QUADRUPLE-confirmed: OpenAI's FB strategy is catalog-ads-only across four batches. **31 total OpenAI ads tracked, 0 with teardown-able copy.** Two distinct launch clusters (Apr 2-21 + Apr 30 / May 8 expanded), identical template both times. This is now the strongest behavioral baseline in this vault.

→ See [[entities/openai]] for cumulative inventory.

### Hims (1 new ad) — Wegovy GLP-1 template reuse

- Format: unknown (likely catalog-dynamic-creative-overlay)
- Title: (no headline)
- Started: 2026-05-07
- ID: `3567971296700086`

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

Followed by the canonical GLP-1 [[compounded-drug-disclaimer]] block and Wegovy/Novo Nordisk trademark attribution.

**This is the same GLP-1 template documented in [[ads-digest-2026-05-06]] for Wedge 1 (Wegovy partnership)** — same hook line, same three-bullet block (FDA-approved → $149/mo split → 100% online), same close ("Your goals. Your plan. Your pace.") and same disclaimer language. Hims is shipping the same creative skeleton with a fresh ad-library entry, which means:

1. **The template is the standing GLP-1 creative**, not a stale-2026-04 artifact
2. **A/B testing happens inside structure** (likely visual asset, headline overlay, or audience targeting) rather than via skeleton variation — consistent with the "skeleton ceiling + bullet substitution" pattern documented in [[dtc-telehealth-ad-template]]
3. **The Hims 3-wedge inventory now has 4 batches of evidence** — GLP-1 (this), Hair Hybrids (2026-05-06 + 2026-05-10), Sex Rx 4-SKU ladder (2026-05-06 baseline + Hard Mints in 2026-05-10)

→ See [[entities/hims]] for cumulative inventory.

### Ro, Anthropic, Henry Meds, Hampton Founders, DealMachine, Eden (0 new ads each)

Fourth consecutive batch with most tracked brands fully dedup-cached. The bare-"Ro" / "Eden" / "Hampton" / "DealMachine" searches continue to be misnamed against the actual primary FB Pages.

## False positives ("brand-name match" noise)

11 of 16 ads (69%) are off-target. Noise-rate trend across four batches: 65% → 82% → 50% → 69%. Mean noise rate ~67% — the steady-state baseline.

### Romance miniseries (3 ads) — **NEW non-substring noise pattern**

- **Page name:** *Romance miniseries* (or a near-variant; ad headline reads "I rise from scavenger to king with alien tech")
- Format: video
- Started: 2026-05-12 (3 distinct ad IDs: `3951954215105677`, `1664610538191815`, `2167571720696506`)
- Content: short-form serialized fiction app — Arthur Morgan/post-WW3/alien-tech/scavenger-to-king/"three wives"/"King of the Wasteland" plot. This is the [ReelShort / DramaBox / FlexTV] category — vertical micro-drama apps running heavy paid social

**None of the tracked brand keywords (Hims, Ro, Eden, Henry, Anthropic, OpenAI, Hampton, DealMachine) is a substring of "Romance miniseries."** Like the 2026-05-11 Adobe Acrobat surprise, this is a clean non-substring match — the Apify actor is returning unsolicited adjacent or suggested-brand results.

> ⚠️ Second non-substring noise pattern in two batches. This isn't a one-off — the Apify actor structurally returns adjacent ads alongside substring matches. Substring filtering alone will never close the noise floor; **page-ID allow-listing is the only structurally-safe filter.**

### Lauren Brooks (4 ads) — long-form pet-allergy direct-response

- **Page name:** *Lauren Brooks*
- Format: image
- Started: 2026-05-10 (4 distinct ad IDs: `866681182372751`, `1638394120715428`, `1476681847332400`, `2833357017001195`)
- Substring root cause: **"Brooks" contains "ro"** — same noise mechanism as Roads & Kingdoms, Roseionly, KaRoL G, Uproot Clean, BaBylissPRO

Although Lauren Brooks is firmly outside the competitive set, the **ad copy is a textbook long-form direct-response confession** worth filing as a contrast pattern. Skeleton:

1. **Pattern interrupt** (*"Please STOP buying allergy meds for your dog"*) + qualifier
2. **Insider authority claim** (*"I'm a dog groomer. Sixteen years."*)
3. **Emotional setup** (Henry the Cavalier King Charles, "soul pup", year-by-year deterioration)
4. **Concrete loss anchor** (*"In twelve months I spent $3400 dollars"*) + the *"I'm going to tell you what that bought me. NOTHING"* reveal
5. **Treatment-failure cascade** (Apoquel $156/mo → Cytopoint $189/2wk → Cyclosporine → Zenrelia) — each with specific dollar amounts, time-to-failure, and category-specific side effect (gums grew over teeth)
6. (truncated mid-Zenrelia — implied click-through reveals "the one thing")

This is the **opposite of Hims' compressed three-bullet template** — long-narrative, story-first, no bullets, no compliance block until far below the fold. Pairs with the [[entities/hampton-founders]] "narrative + proof" structure as another non-template format in the wider category. **Worth re-reading the ad in full when designing long-form creative for [[medvi-positioning]]'s GLP-1 funnel.**

### Other substring-match noise (4 ads)

- **BabylissPRO Barber** — *"Pro"* contains "ro". Already in noise inventory from 2026-05-10.
- **Builders Protein Bars** — *"Pro"* contains "ro". NEW page in noise inventory.
- **Hampton Roads Transit** — *"Hampton Roads"* substring. Already in noise inventory.
- **Blake Hampton** — *"Hampton"* substring. NEW page (likely a US realtor / personal brand).

## Cross-cutting patterns

### OpenAI's catalog-ads-only strategy — now the most-evidenced behavioral baseline in this vault

| Batch | Date | OpenAI ads | Format | Campaign cluster |
|---|---|---|---|---|
| 1 | 2026-05-06 | 21 | carousel | Apr 2-21 (initial wave) |
| 2 | 2026-05-10 | 3 | carousel | Apr 7 (subset of cluster 1) |
| 3 | 2026-05-11 | 3 | carousel | Apr 30 + May 8 (new cluster) |
| 4 | 2026-05-12 | 4 | carousel | May 8 (cluster 2 expanded) |
| **Total** | | **31** | **all carousel** | **2 launch clusters** |

Four batches. Two distinct launch clusters. 31 carousel ads. 0 with static narrative. There is no other behavioral pattern in this vault with comparable evidence depth — this is now the **OpenAI FB baseline assumption**.

The 2026-05-08 sub-cluster has expanded from 2 → 6 ads across batches 3+4, suggesting OpenAI is *still rolling out* this campaign rather than winding it down. If OpenAI ever ships static narrative creative on FB, it will require a noticed change of behavior, not a single counter-example.

→ [[entities/openai]] updated to reflect four-batch confirmation.

### Hims template stability — 4 batches in, the template hasn't evolved structurally

| Batch | Date | New Hims ads | Wedge changes |
|---|---|---|---|
| 1 | 2026-05-06 | 45 | GLP-1 / Hair Hybrids / Sex Rx 3-SKU initial inventory |
| 2 | 2026-05-10 | 2 | Hair Hybrids variant + Hard Mints (4th Sex Rx SKU, 4-bullet variant) |
| 3 | 2026-05-11 | 0 | (fully dedup-cached) |
| 4 | 2026-05-12 | 1 | GLP-1 template re-launch (verbatim) — **no structural change** |

Inside 6 days the only structural innovation has been Hard Mints' four-bullet variant for the high-objection ED non-responder category. Everything else is verbatim template reuse across launches. **Inside-structure A/B testing dominates over template variation** — this matches the 'mature compliance-anchored ad system' hypothesis.

→ [[entities/hims]] + [[concepts/dtc-telehealth-ad-template]] updated to note the 4th-batch verbatim re-launch.

### The four-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI ads | Hims ads | Real-signal % |
|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 31% |

Steady-state dedup is 92-97%. New-ad volume per batch in the 6-22 band. Real-signal proportion in the 18-50% band. **The farm is structurally noisy at ~67% mean — and substring filtering can never bring this number down because at least two of the four batches have surfaced non-substring noise.**

### Non-substring noise is now a recurring, not one-off, failure mode

Two of four batches have surfaced noise pages with **no tracked-brand substring match**:

- 2026-05-11: **Adobe Acrobat**
- 2026-05-12: **Romance miniseries** (3 ads — multiplier effect)

This rules out the "Adobe Acrobat was a one-time fluke" hypothesis. The Apify `facebook-ads-library-scraper` actor returns unsolicited adjacent / suggested-brand results at non-zero rate. Implication for filter design: **substring-allowlist is necessary but not sufficient; page-ID allow-listing is the only structurally-safe noise filter.**

## Open questions

- Is the 2026-05-08 OpenAI launch cluster pointing to a single product surface (Codex? ChatGPT for Business? Sora?) — worth one manual click-through to a few of the 6 cluster ads to confirm destination.
- Does the verbatim Hims Wegovy ad point to the same landing page as the 2026-05-06 batch's GLP-1 ads, or has the LP changed? (If LP changed, the verbatim ad copy is doing different work.)
- The "Romance miniseries" multiplier (3 ads in one batch from a single non-substring noise page) — is this a runaway path, or did the actor just return more of one campaign? Worth watching whether Romance miniseries dedup-prevents tomorrow.
- Lauren Brooks: is the long-form confession copy specific to pet supplement, or is it a category-portable template worth modeling for a future Medvi long-form ad?

## Related

- [[competitor-ads-farm]] — fourth batch from this farm; four-batch steady state now established
- [[hims]] — GLP-1 Wegovy template re-launched verbatim (4th batch evidence)
- [[openai]] — catalog-ads-only QUADRUPLE-confirmed across four batches (31 total ads)
- [[dtc-telehealth-ad-template]] — GLP-1 instantiation gets fresh evidence of structural stability
- [[ads-digest-2026-05-06]] — first batch (183 new, cold start)
- [[ads-digest-2026-05-10]] — second batch (22 new, Hims Hard Mints + OpenAI catalog confirmation #2)
- [[ads-digest-2026-05-11]] — third batch (6 new, 50% noise, OpenAI #3, Adobe Acrobat non-substring noise discovery)

## Appears in

- Fourth entry in `wiki/sources/` for the competitor-ads farm. Marks four-batch convergence with: (1) OpenAI catalog-ads-only quadruple-confirmation, (2) first verbatim Hims template re-launch evidencing inside-structure A/B as the standing pattern, (3) second non-substring noise event (Romance miniseries) confirming the Apify-actor adjacent-brand failure mode is recurring, (4) Lauren Brooks long-form confession copy as a filed-but-out-of-set contrast pattern.
