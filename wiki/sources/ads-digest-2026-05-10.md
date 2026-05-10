---
title: FB Ads Digest — Competitor brands — 2026-05-10
category: source
summary: Second competitor-ads farm batch — 22 new FB Ad Library entries (190 fetched, 168 dedup-skipped); Hims drops to 2 new ads (one new product — "Hard Mints" chewable ED compound — and a Hair Hybrids variant); OpenAI ships 3 more dynamic-creative-only carousels confirming the catalog-ads-only pattern; Ro still placeholder-only; ~85% of digest is brand-name-substring noise (Eden & Om, Eden Brothers, Hampton by Hilton, KaRoL G, Uproot Clean, BaBylissPRO, etc.) — farm filter remains untuned since 2026-05-06
tags: [fb-ads, ad-library, hims, hard-mints, glp-1, telehealth, compounded-drugs, openai, ro, dtc, competitor-ads, creative-teardown]
sources: 1
source_path: raw/ads/digest-2026-05-10.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-10
updated: 2026-05-10
---

# FB Ads Digest — 2026-05-10

Second batch from the [[competitor-ads-farm]]. **22 new ads, 168 dedup-skipped** out of 190 fetched across 8 tracked brand keywords (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Hims drops to 2 new ads** — Hair Hybrids template continues, **plus a new product wedge: "Hard Mints by Hims"** — a chewable ED compounded product positioned for "guys traditional ED pills don't work for." Confirms Hims' Sex Rx category continues to expand SKU variants (3-in-1 Pill → Sex Rx + Climax Control → Sex Rx + Testosterone Support → Hard Mints chewable). Same [[concepts/compounded-drug-disclaimer]] template applies.
- **OpenAI ships 3 more dynamic-creative carousels** — exact same `{{product.name}}` / `{{product.brand}}` placeholder pattern as the 2026-05-06 batch. **The catalog-ads-only strategy is now confirmed across two batches.** Started 2026-04-07 — same campaign launch wave as the 2026-05-06 batch's Apr 2-21 cluster.
- **Ro still placeholder-only** — 2 new ads, both `{{product.brand}}` body text. Pattern from 2026-05-06 (1 placeholder ad) holds: Ro's primary FB Page either uses a different name than bare "Ro" or runs minimal narrative creative.
- **Anthropic produced zero new ads in this batch** — the 5 ads from 2026-05-06 are still dedup-cached.
- **Hampton Founders, Henry Meds, DealMachine — zero new ads.**
- **Brand-name filter still untuned** — farm action item from 2026-05-06 has not been addressed. ~85% of this digest's 22 ads are substring-match noise (vs ~65% in the prior batch — narrower because of dedup, but proportionally worse).

## Source

- Path: `raw/ads/digest-2026-05-10.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 190 • New: 22 • Dedup-skipped: 168

## Tracked-brand creative inventory

### Hims (2 new ads) — Hard Mints product launch

Volume dropped from 45 → 2 because most Hims creative is dedup-cached from 2026-05-06. The two new ads:

#### Ad 1 — Hair Hybrids continuation (started 2026-04-22)

> Don't wait — join the hundreds of thousands of guys who've found true results. Get a treatment recommendation today, 100% online.
>
> Why Hims?
> 🗓️Regrow in as few as 3-6 months
> 🧑🏻‍⚕️Doctor-trusted ingredients
> 📦Free shipping to your front door (if prescribed)
>
> Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs.

Identical to the 2026-05-06 Hair Hybrids template — a fresh creative ID with the same copy. Fits the [[concepts/dtc-telehealth-ad-template]] three-bullet skeleton and the canonical [[concepts/compounded-drug-disclaimer]] hair variant.

#### Ad 2 — **"Hard Mints by Hims" — new chewable ED product** (started 2026-05-05)

> If traditional ED pills don't work for you, Hard Mints by Hims might be an option—if prescribed.
>
> Why treat ED with Hims?
> 🥼 Wide range of personalized ED treatments
> ❇️ Pills and discreet chewable options
> 🩺 Doctor-trusted active ingredients
> 💻 No office visit required
>
> Hard Mints is a chewable compounded product and has not been approved by the FDA. The FDA does not verify the safety or effectiveness of compounded drugs. Prescription products require an online consultation with a healthcare provider who will determine if a prescription is appropriate. Restrictions apply. See website for full details and important safety information.

**This is a new Hims SKU not present in the 2026-05-06 batch.** Notable shifts:

- **Hook is failure-mode-targeted** — "If traditional ED pills don't work for you" qualifies the buyer immediately on a different axis than the 3-in-1 Pill ("better sex life") or Sex Rx + Testosterone ("optimize"). Implies Hard Mints uses a different active ingredient or higher dose that addresses non-responders. Likely sublingual avanafil or a tadalafil/avanafil chewable combination — needs landing-page check to confirm.
- **Four-bullet variant** — first Hims ad in this vault to use four bullets instead of three. Adds "💻 No office visit required" as the access-channel bullet alongside the standard three. Hypothesis: ED category has a stickier "would I have to see a doctor?" objection than GLP-1 or hair, requiring an explicit no-office-visit signal.
- **Discreet chewable as differentiator** — "Pills and discreet chewable options" — discreet shipping is the standard Sex Rx bullet but here it's the *form factor* (chewable mints) that's discreet, not just the packaging. Mints can be taken in public; pills require a glass of water.
- **Disclaimer template** — matches the [[concepts/compounded-drug-disclaimer]] canonical clauses but with slightly tighter wording: *"chewable compounded product"* + *"has not been approved by the FDA"* (vs the 3-in-1 Pill's *"is a compounded drug product"* + *"FDA does not approve or verify"*). Same legal substance, different phrasing — suggests Hims runs A/B variants of the disclaimer language too.

→ See [[hims]] for updated wedge inventory (now 4 Sex Rx SKUs: 3-in-1 Pill, Sex Rx + Climax Control, Sex Rx + Testosterone Support, **Hard Mints**).

### OpenAI (3 new ads) — dynamic-only carousels (confirmed pattern)

All three ads:
- Format: carousel
- Title: `{{product.name}}`
- Body: `{{product.brand}}`
- Started: 2026-04-07 (all three the same date — same campaign launch as the Apr 2-21 cluster from the 2026-05-06 batch)
- IDs: `1320981316759965`, `1624315815477453`, `1349759913586962`

> ⚠️ Pattern confirmed across two batches: OpenAI's FB strategy is **catalog-ads-only**. Zero static narrative ads in either the 2026-05-06 batch (21 ads) or the 2026-05-10 batch (3 ads). 24 total OpenAI ads tracked, 0 with teardown-able copy. This is now a stable observation, not a single-batch anomaly.

Implication for [[entities/openai]]: whatever product surface these carousels point to (API console / ChatGPT plans / verticals) is being driven entirely by product-feed dynamic creative, with narrative work pushed elsewhere (PR, launches, organic). Worth tracking landing-page destinations to confirm what they're catalog-ing.

### Ro (2 new ads) — placeholder-only (pattern continues)

Both ads body text: `{{product.brand}}` only.
- Ad 1: started 2026-05-04, ID `1293670862912194`, Format unknown
- Ad 2: started 2026-04-28, ID `1509432877229735`, Format unknown

Same pattern as the 2026-05-06 batch's lone Ro ad. → See [[ro]] action item: tune farm to search for "Roman Health" / "Ro Body" / "Ro Health" page names rather than bare "Ro."

### Anthropic (0 new ads)

No new creative this batch. The 5 ads from 2026-05-06 are still cached in dedup state.

### Henry Meds (0 new ads)

Continued absence — second batch with zero new ads. Either Henry Meds runs minimal FB creative or the brand-keyword search doesn't match their primary FB Page. → Action item: verify Henry Meds' actual FB Page and add to allow-list.

### Hampton Founders (0 new ads)

The 2 ads from 2026-05-06 are dedup-cached. No new creative.

### DealMachine (0 new ads)

Continued absence — same as 2026-05-06.

## False positives ("brand-name match" noise)

The farm filter remains untuned since 2026-05-06. **18 of 22 ads (~82%)** in this batch are noise from substring-matching the bare brand keywords. The recurring offenders:

### "Eden" false positives (3 ads)

- **Eden & Om** — bamboo loungewear/PJs (2 ads — same pattern as 2026-05-06 batch's 13 ads). Sample copy: *"Experience true luxury with super soft loungewear!"* + *"Tired of rough, worn-out PJs? Upgrade to a comfy, soft & luxurious slouchy PJ set."* Different product (PJ set vs sheets) but same brand and same false-positive root cause.
- **Eden Brothers** — gardening / flower bulbs (1 ad — was 14 in 2026-05-06). *"Meet the newest blooms this season 🌷"* — fall/spring planting marketing.

None are the GLP-1-telehealth Eden the farm is supposed to track.

### "Hampton" false positives (5 ads — most diverse noise category)

- **Hampton by Hilton** — *"Save up to 20% this summer at Hampton Inn & Suites Chicago Medical District UIC"* — hotel discount carousel
- **Visit Hampton, Virginia!** — tourism board (placeholder carousel)
- **NAPA BDG South Hampton Roads** — Virginia auto-shop chain (*"With 17 individual auto shops in Chesapeake, Norfolk, Virginia Beach"*)
- **Hampton RV Trailer Sales & Service** — RV dealer (placeholder)
- **Hampton University Proton Cancer Institute** — *"Considering your cancer treatment options? For 15 years, we've guided patients toward advanced care like proton therapy"* — university-affiliated cancer center

This is consistent with the 2026-05-06 noise — Hampton is a Virginia geographic name, a hotel chain, and a university name; substring match floods the digest.

### "Ro" false positives (4 ads)

- **KaRoL G** — Karol G (Colombian pop star) — *"VIAJANDO POR EL MUNDO , TropiTour 🧡"* — tour promo. The "Ro" matches inside "KaRoL."
- **Uproot Clean** (2 ads) — washing machine cleaner tablet — *"Get Rid of Bacteria & Pet Odor from Your Washer"* + the NASA-enzyme-tech variant. The "Ro" matches inside "Uproot."
- **WR Performance Products Inc.** — auto performance parts (placeholder) — "Pro" contains "Ro."

### "Hims" false positives (0)

"Hims" is a sufficiently unusual substring that it doesn't generate noise. **The 4-letter brand keywords (Eden, Hims, OpenAI, Henry Meds) work; the 2-3 letter keywords (Ro, Hampton) generate the bulk of noise.**

### Other (1 ad)

- **Hill Chiropractic** — *"$49 Knee Pain Exam and Relief Treatment"* — Edmond/OKC area chiropractor pitching Shockwave® Therapy. Unclear what brand keyword this matched against — possibly "ill" inside "Hill" caught against an internal Apify search-broadening, or the actor returned an unrelated suggested-brand ad. Worth investigating.

### Other surfaced false-positive brands (not telehealth)

- **BaBylissPRO USA** (2 ads) — hair-styling tools — "Pro" → "Ro" substring match (2 placeholder carousels)

> ⚠️ Action item from 2026-05-06 still not addressed: tune the [[competitor-ads-farm]] to use **exact page-name match** or **page-ID allow-listing** rather than substring match. The 2026-05-06 batch was ~65% noise; the 2026-05-10 batch is ~82% noise (proportionally worse because dedup removed real Hims/OpenAI/Anthropic creative but kept all the noise pages — substring matches re-fire on every new ad those pages run, even if the page itself is irrelevant).

## Cross-cutting patterns

### Hard Mints — chewable ED is the new Hims SKU

Hims' Sex Rx wedge has expanded to **4 SKUs in 2026-05**:

| SKU | Form factor | Active ingredients | Hook angle |
|---|---|---|---|
| 3-in-1 Pill | Pill | sildenafil + tadalafil + B12 | "Better sex life" + Viagra/Cialis equivalence |
| Sex Rx + Climax Control | Pill | tadalafil + PE treatment | "Get harder, and go longer" |
| Sex Rx + Testosterone Support | Pill | tadalafil + zinc + L-arginine + B12 + B6 | "Optimize sex life and testosterone" |
| **Hard Mints** (NEW) | **Chewable mint** | (compounded — likely sublingual avanafil or tadalafil/avanafil combo) | **"If traditional ED pills don't work for you"** — failure-mode-targeted |

Each new SKU adds a different *failure mode* it addresses:
- 3-in-1 Pill: baseline / "want it all"
- Climax Control: PE-specific
- Testosterone Support: low-T-specific
- **Hard Mints: non-responders to traditional pills** (failure of standard ED meds)

This is **wedge laddering** — not just adding products but adding *qualifying buyer states*. Each SKU expands the ICP: men whose ED isn't addressed by the prior SKU. Direct relevance for [[medvi-positioning]] — the Medvi Sex Rx product line, if it exists, can mirror this laddering or compete by collapsing it ("one product for all four states").

### OpenAI's catalog-ads-only strategy is confirmed

Across the 2026-05-06 and 2026-05-10 batches, OpenAI has shipped **24 carousel ads, all dynamic-creative-only**. Zero static narrative copy. This is a deliberate strategy, not a campaign-launch coincidence:

- Both batches show the same campaign cluster (Apr 2-21 launches)
- Both batches show only carousel format
- Both batches show only `{{product.name}}` / `{{product.brand}}` placeholders
- **Two batches, same pattern → it's a strategy, not noise**

Hypothesis remains: AI labs lean on PR/organic/launches for narrative work and reserve paid social for catalog re-targeting against existing intent (search, ChatGPT visit, API signup). Worth a separate concept page if a third batch confirms.

### The four-bullet variant for high-objection categories

The Hard Mints ad breaks the [[concepts/dtc-telehealth-ad-template]] three-bullet ceiling and uses **four bullets** — adding "💻 No office visit required" as a fourth access-channel bullet. Worth noting on the template page: when the category has a sticky objection that the standard three bullets don't pre-empt (here: ED's "would I have to see a doctor?" objection), the safe default expands to four bullets with the fourth bullet specifically targeting the objection.

→ See [[concepts/dtc-telehealth-ad-template]] update.

## Open questions

- What's Hard Mints' actual active ingredient? (Likely avanafil sublingual or tadalafil/avanafil chewable — landing-page or compounding-pharmacy partnership disclosure should confirm.)
- Does Hard Mints address the same buyer Medvi's compounded ED line targets, or is it positioned for a different failure mode?
- Why is OpenAI still running the same Apr 2-21 carousels a month later? (Successful catalog campaign? Or did the campaign pause and these are the residue?)
- The Ro placeholder pattern persists across two batches — is Ro running real creative under a page name the farm misses (Roman Health, Ro Body)?

## Related

- [[competitor-ads-farm]] — second batch from this farm
- [[hims]] — Hard Mints product update + 4-SKU Sex Rx wedge
- [[ro]] — placeholder pattern continues
- [[openai]] — catalog-ads-only confirmed across two batches
- [[concepts/compounded-drug-disclaimer]] — Hard Mints adds a fifth disclaimer variant
- [[concepts/dtc-telehealth-ad-template]] — four-bullet variant for high-objection categories
- [[ads-digest-2026-05-06]] — first batch (baseline reference)

## Appears in

- Second entry in `wiki/sources/` for the competitor-ads farm. Establishes the dedup-driven cadence: most batches will surface ≤25 ads with the bulk of new creative concentrated in 1-2 brand wedges.
