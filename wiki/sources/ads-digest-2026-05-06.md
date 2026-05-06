---
title: FB Ads Digest — Competitor brands — 2026-05-06
category: source
summary: First competitor-ads farm batch — 183 new FB Ad Library entries across 8 tracked brands; Hims dominates with 45 ads spanning three creative wedges (GLP-1 + hair-loss "Hair Hybrids" + Sex Rx); OpenAI (21) and Anthropic (5) ship dynamic-creative carousels with no static copy; Hampton Founders runs "$3M+ founder peer group" community pitch; Ro/Henry Meds/DealMachine/Eden produce zero in-set creative this batch
tags: [fb-ads, ad-library, hims, glp-1, telehealth, compounded-drugs, openai, anthropic, hampton, dtc, competitor-ads, creative-teardown]
sources: 1
source_path: raw/ads/digest-2026-05-06.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-06
updated: 2026-05-06
---

# FB Ads Digest — 2026-05-06

First batch from the [[competitor-ads]] farm. **183 new ads, 4 dedup-skipped** across 8 tracked brand keywords (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Hims is the creative-volume leader.** 45 new ads, three clear wedges: GLP-1 weight-loss (Wegovy® with Hims at $149/mo + $39 first-month membership), hair-loss ("Hair Hybrids" compounded oral+topical minoxidil/finasteride), and Sex Rx (compounded "3-in-1 Pill," "Sex Rx + Climax Control," "Sex Rx + Testosterone Support"). Each wedge carries the same FDA-compounded-drug disclaimer boilerplate.
- **OpenAI & Anthropic ship dynamic-creative-only carousels.** 21 OpenAI + 5 Anthropic ads in this batch — every single one has `{{product.name}}` headlines and `{{product.brand}}` body text. No teardown-able copy; these are product-feed-driven dynamic ads against catalog items.
- **Hampton Founders is the only "Hampton" with relevant creative.** "Most founders making $3M+ have the same problem" — peer-group community pitch tied to the [[entities/y-combinator]]-adjacent founder-community thesis.
- **Brand-keyword false positives dominate the digest.** "Eden" matched Eden Brothers (gardening, 14 ads), Eden & Om (bamboo sheets, 13), Aelfric Eden (fashion), UNC Health Rockingham at Eden NC, etc. "Hampton" matched Hampton Inn, Hampton Roads Transit, dozens of regional businesses. **The farmer's brand-name filter isn't catching these** — the farmer config promises a post-fetch filter that drops third-party pages, but the digest shows it didn't fire. → flag for [[competitor-ads]] farm tuning.
- **Ro, Henry Meds, DealMachine produced zero relevant ads.** Ro had 1 placeholder-only ad. Henry Meds and DealMachine — no in-set creative.

## Source

- Path: `raw/ads/digest-2026-05-06.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 187 • New: 183 • Dedup-skipped: 4

## Tracked-brand creative inventory

### Hims (45 new ads) — the dominant creative engine

Three product wedges, recurring copy templates per wedge. All compounded products carry the FDA disclaimer.

#### Wedge 1 — GLP-1 weight loss (Wegovy® with Hims)

Recurring template (≥6 variations):

> Get Wegovy® with Hims, plus access to provider-led care, tailored treatment plans, and ongoing support designed around your lifestyle.
>
> Why Hims?
> ✅ FDA-approved GLP-1 pill and pens available
> ✅ Medication as low as $149/mo—membership fee of $39 for first month, $149 thereafter
> ✅ 100% online
>
> Your goals. Your plan. Your pace.

**Pricing structure:** $149/mo medication + $39 first-month membership / $149 membership thereafter — billed separately, "Membership is billed separately and does not include or guarantee a prescription."

One outlier ad escalates the claim: *"Lose up to 25% of your body weight* with clinically proven options, including the new Wegovy® High Dose Pen"* citing the Wegovy 7.2mg 72-week study (31.2% of adults achieved ≥25% weight loss; average 18.7%).

> ⚠️ Compliance: every Wegovy ad includes — *"Wegovy® is a registered trademark of Novo Nordisk A/S"* + *"Hims & Hers Health, Inc. is not affiliated with or endorsed by Eli Lilly and Company"* (when Zepbound®/KwikPen®/Foundayo™ are mentioned).

#### Wedge 2 — Hair-loss "Hair Hybrids" (compounded)

Recurring template (≥10 variations):

> Don't wait — join the hundreds of thousands of guys who've found true results. Get a treatment recommendation today, 100% online.
>
> Why Hims?
> 🗓️Regrow in as few as 3-6 months
> 🧑🏻‍⚕️Doctor-trusted ingredients
> 📦Free shipping to your front door (if prescribed)

> ⚠️ Compliance: *"Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs."* + *"Individual results may vary. Based on separate individual studies of oral and topical minoxidil and finasteride."*

#### Wedge 3 — Sex Rx (compounded)

Three product variants, all compounded:

1. **3-in-1 Pill** — sildenafil + tadalafil + B12. *"A better sex life just dropped: Meet the new 3-in-1 Pill by Hims."* Disclaimer: *"All trademarks are the property of their respective owners. Use of Cialis® and Viagra® do not imply endorsement or affiliation with Hims, Inc."*
2. **Sex Rx + Climax Control** — tadalafil + PE treatment. *"The 2-in-1 pill to get harder, and go longer."*
3. **Sex Rx + Testosterone Support** — tadalafil + zinc + L-arginine + B12 + B6. *"🔥New Sex Rx + Testosterone Support 🔥 Daily 2-in-1 pill to optimize your sex life and testosterone."*

All three carry the same compounded-drug FDA disclaimer.

#### Hims creative-format observation

44 of 45 Hims ads have `Format: unknown` and 26 have body text *only* `{{product.brand}}` (placeholder) — Hims appears to use catalog-driven dynamic ads heavily, with the static-copy variants above doing the heavy lifting on messaging.

### Ro (1 new ad)

Single ad, placeholder-only body (`{{product.brand}}`). No teardown-able creative this batch. Library URL: `facebook.com/ads/library/?id=1848240979175501` (started 2026-04-14).

### Henry Meds (0 new ads in batch)

No creative output captured. Either ads paused, dedup state already covers all active creative, or the brand-name search didn't match — flag for next batch.

### OpenAI (21 new ads) — dynamic-only carousels

Every single OpenAI ad in the batch is a carousel with title `{{product.name}}` and body `{{product.brand}}` — pure product-feed-driven dynamic creative. No tear-downable static copy. Suggests OpenAI's FB strategy here is **catalog ads** (likely API products / ChatGPT plans / ChatGPT-for-X SKUs) rather than narrative creative.

Started dates cluster Apr 2-21, 2026 — consistent with a single campaign launch.

### Anthropic (5 new ads) — dynamic-only carousels

Same pattern as OpenAI: 5 carousels, all `{{product.name}}` / `{{product.brand}}` placeholders. Started dates Mar 16 - Apr 8, 2026. No teardown signal.

> ⚠️ Pattern: Both OpenAI and Anthropic in this batch ship **only** dynamic-creative carousels with no static narrative ads. This is the opposite of Hims' approach. Hypothesis: AI labs are testing catalog/product-feed ads against API surface or plan SKUs, rather than running brand creative.

### Hampton Founders (2 new ads)

The relevant "Hampton" — Sam Parr's vetted founder community.

> Most founders making $3M+ have the same problem. They feel stuck often. And not always just on tactics. On the bigger stuff.
>
> Hampton is where 1,000+ vetted founders & CEOs meet monthly to talk about it. In small groups. With people in their city.
> Real conversations about co-founder splits, whether to sell, how to balance life and business.

This is the founder-peer-group ICP that overlaps with [[mark-kashef]]'s Early AIdopters and [[nick-saraev]]'s Maker School. ICP: $3M+ revenue founders. Channel: monthly small-group meetings, city-based. Hook: "stuck on the bigger stuff" — emotional/strategic, not tactical.

### DealMachine (0 new ads)

No creative output captured.

## False positives ("brand-name match" noise)

The farmer config promises *"Brand-name filter post-fetch drops third-party ads that mention a brand keyword (e.g. random pages running ads about 'Hims hair loss'). Only ads where the page name contains the search brand are kept."*

The digest shows ~120+ ads from third-party pages with the keyword in the page name (which technically matches the filter rule but isn't the intent). Examples:

- **Eden** false positives: Eden Brothers (gardening, 14 ads — biggest single bucket); Eden & Om (bamboo sheets, 13); Aelfric Eden (fashion); UNC Health Rockingham at Eden NC; Eden Lifestyle Boutique; Eden and Om; The Mystic Eden; Carolina Sheds (Eden NC location)
- **Hampton** false positives: Hampton Inn & Suites Clearwater Beach; Hampton Roads Honda/Transit/Moving/Hospice; Hampton Sun (sunless tanning); Hampton University Online; Classic Toyota Hampton; Audi/Genesis/Nissan of Hampton; Hampton Hopper (Hamptons shuttle); Hampton Food Market; Conner's Rooftop (in Hampton Hotel Fort Wayne); Rockfest Half Marathon Hampton NH; Jewels On Hampton; Spoon and Script by Emily Hampton; Kidtique Hampton; Hampton Sun
- **Ro** false positives: Roads and Kingdoms; Pasieki Rodziny Sadowskich; ProTyres Oradea; Sean Gracet Roset; Josh Ross J-RO; Roseionly home; Modlet.ro; Carobooks; Fenzy România; BazarulOnline.ro; Metropolitan Beauty Academy; Babylisspro Barber; YZPST; Prolube Oil; Vincero Collective; Zero9 Holsters; Southern Auto Group; Genesis of Hampton; Audi Hampton; Carol Henderson; Carolina Sheds; Herb'N Eden (matches "Eden" + "Hero" patterns?)

> ⚠️ Action item: tune the [[competitor-ads]] farm's brand-name filter to use exact-match or page-ID allow-listing rather than substring match. Current filter is too permissive — ~65% of this digest is noise.

## Cross-cutting patterns

### Compounded-drug disclaimer template (Hims)

The exact boilerplate Hims uses on every compounded-product ad:

> [Product name] is a compounded drug product. The FDA does not approve or verify compounded drugs for safety, effectiveness, or quality. This prescription product requires an online consultation with a healthcare provider who will determine if a prescription is appropriate. Restrictions apply. See website for full details and important safety information.

Variant for Hair Hybrids:

> Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs.

This is the canonical compliance-line for compounded GLP-1 / compounded ED / compounded hair products in 2026 telehealth advertising — and it's what [[medvi-positioning]] (when ingested) will need to mirror. → New concept: [[compounded-drug-disclaimer]].

### "100% online" + "free shipping" + "discreet delivery" — DTC telehealth template

Recurring three-bullet structure across Hims products:

```
🏅[Outcome / equivalence claim]
🧑‍⚕️[Provider trust signal]
📦Free shipping / discreet delivery
```

The "discreet delivery" framing only appears on Sex Rx — appears to be the conditional fourth bullet for stigma-bearing categories.

### Pricing trick: separate medication & membership

Hims' GLP-1 ads consistently say *"Medication as low as $149/mo"* but the membership is billed separately ($39 first month, $149 thereafter). Effective monthly cost is $149 + $149 = **$298/mo** (steady state) or **$188/mo** (first month). The headline price hides 50% of the cost. Worth noting for [[medvi-positioning]] and any compete-page work.

### Ad-format split

| Format | Count | Notes |
|---|---|---|
| unknown / dynamic | ~80 | mostly Hims + OpenAI + Anthropic catalog ads |
| video | ~50 | recurring Eden Brothers garden ads, Uproot Clean washer-bacteria ads, Herb'N Eden skincare |
| carousel | ~40 | mostly auto-dealership and OpenAI dynamic |
| image | ~13 | mostly Eden & Om bamboo sheets and stock e-comm |

## Open questions

- Why is the brand-name filter not catching obvious noise? (See action item above.)
- Are Henry Meds and DealMachine actually running ads but the search misses them, or have they paused FB? (Check Apify search-URL params.)
- Is OpenAI's catalog-only ad strategy a deliberate choice or a placeholder while they test? (Watch next batches for static creative.)
- Hims' steady-state $298/mo GLP-1 price — does Medvi need a price-anchor compete page calling this out?

## Related

- [[competitor-ads]] (when promoted to a concept page) — the farmer config
- [[hims]] (entity, this ingest creates) — most-active brand
- [[hampton-founders]] (entity, this ingest creates) — relevant Hampton
- [[compounded-drug-disclaimer]] (concept, this ingest creates) — boilerplate template
- [[dtc-telehealth-ad-template]] (concept, this ingest creates) — three-bullet pattern
- [[anthropic]] — entity, updated with FB ad-creative observation
- [[ro]], [[openai]], [[henry-meds]] (entities, this ingest creates as stubs)

## Appears in

- First entry in `wiki/sources/` for the competitor-ads farm. Sets the template for daily ad-digest ingests.
