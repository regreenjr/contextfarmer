---
title: FB Ads Digest — Competitor brands — 2026-06-05
category: source
summary: Sixteenth competitor-ads farm batch — 39 new FB Ad Library entries (199 fetched, 160 dedup-skipped, 80.4%) at a **6-day gap** from batch 15 (the largest gap since batch 8's 4-day) — so the headline volume is **gap-inflated**; **[[hims]] ships its biggest copy volume in the farm — 8 verbatim static-copy ads spanning ALL THREE wedges AND both Sex Rx SKUs** (Wegovy GLP-1 ×3 + Hair Hybrids ×2 + Sex Rx + Testosterone Support ×1 + Sex Rx + Climax Control ×2) + 10 placeholders = 18 Hims ads — but per-day-normalized this is **3.0 Hims/day, NOT an intensification** (matches the batch-8/9 ~2-2.5/day baseline, below batch 14's 4.0/day surge); the apparent "mega three-wedge surge" is 6 days of verbatim re-launches across all wedges surfaced in one fetch — the **clearest compression-artifact demonstration since batch 8**, and a refinement to the surge→trough cadence reading (varying fetch gaps make multi-wedge batches look like mega-surges); **Sex Rx + Climax Control RETURNS** (IDs `961821243380184` started 2026-04-29 + `1736502914453690` started 2026-06-04) after silence since batch 7 — both Sex Rx SKUs (Testosterone Support + Climax Control) now active in the same batch for the first time; **the 2026-06-04 Climax Control ad uses an "Introducing the 2-in-1 pill" intro-word A/B variant** vs the older "The 2-in-1 pill"; **Wegovy comes back with 3 verbatim re-launches** after its batch-15 collapse-to-placeholder (confirms "dormant not closed" yet again); **[[ro]] ships 5 placeholders — the largest Ro batch in the farm** (prior max 2; all `{{product.brand}}`, 0.83/day gap-normalized = normal Ro rate) — Run 5; **[[openai]] 2 placeholders, still catalog-only** (started 2026-05-08 Cluster 2 + a 2026-05-18 re-surface) — Cluster 4 (2026-05-22) does NOT expand this batch (holds at 2); cumulative 49 ads, still 1 with copy; **[[anthropic]] 5th consecutive silence (12-16) — now MEETS the ≥5-silent-batch threshold count, but the cadence-predicted next-ad date (~2026-06-08) has NOT yet passed**, so hold the stall call until past 06-08 (~batch 17); **[[eden]] (TryEden) 3rd consecutive silence (14+15+16)**; real-signal rate 64.1% (25 of 39) — high, behind only batch 14's 80% / batches 7+12's 67%; **14 noise ads, 12 "Ro" + 2 "Eden", with 7 NEW first-fire "Ro" pages in one batch** (largest single-batch "Ro" noise expansion — gap-inflated): From Head To Toe, **TRELEGY** (first major-pharma noise, GSK asthma, via "fu**ro**ate"), Diamond Cross Ranch, Lowe's, **Ross Fledderjohn** (first third-party affiliate ad promoting a TRACKED brand's product — OpenAI Codex/GPT-5.5 #ChatGPTPartner, on a personal page not OpenAI's), Range Rover, WR Performance Products + returning Cholesterol Support Group (both confession narratives) / Lauren Brooks / Uproot Clean / Gardens of Eden / Aelfric Eden + **Aelfric Eden UK** (2nd regional-page variant after batch-15's Aelfric Eden EU); Henry Meds / Hampton / DealMachine — 16th consecutive batch no signal; cumulative 96 Hims / 49 OpenAI / 8 Anthropic / 15 Ro / 1 Eden
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, hims, fetch-gap-compression-confirmed, six-day-gap, mega-three-wedge-compression, all-four-template-coverage, sex-rx-climax-control-returns, both-sex-rx-skus, wegovy-wave-continues, dormant-not-closed, ro-run-5, ro-largest-batch, openai-catalog-only, cluster-4-holds-at-2, anthropic-5th-silence, anthropic-threshold-met, eden-3rd-silence, signal-rate-64, ro-noise-expansion, trelegy-pharma-noise, ross-fledderjohn-affiliate, aelfric-eden-uk-regional-page]
sources: 1
source_path: raw/ads/digest-2026-06-05.md
source_date: 2026-06
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-06-05
updated: 2026-06-05
---

# FB Ads Digest — 2026-06-05

Sixteenth batch from the [[competitor-ads-farm]]. **39 new ads, 160 dedup-skipped** out of 199 fetched at a **6-day gap** from batch 15 (2026-05-30) — the largest fetch gap since batch 8's 4-day gap. Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **The 6-day gap means this batch is gap-inflated — read everything per-day-normalized.** 39 new ads / 6 days = **6.5 ads/day total** (back in the 8-9 baseline band once you account for the gap). Dedup rate 80.4% is the lowest since batch 8 (83%), exactly as expected for a long gap that accumulated more new ads. This is the **second-clearest compression event in the farm** after batch 8.
- **[[hims]] ships its biggest copy volume in the farm — 8 verbatim static-copy ads across ALL THREE wedges AND both Sex Rx SKUs** (+ 10 placeholders = 18 Hims ads). But **gap-normalized this is 3.0 Hims/day — NOT an intensification** (it matches the batch-8/9 ~2.0-2.5/day baseline and is *below* batch 14's 4.0/day true surge). The apparent "mega three-wedge surge" is **6 days of continuous verbatim re-launches across all wedges surfaced in one fetch.** This is the clearest demonstration since batch 8 that **varying fetch gaps make multi-wedge batches look like mega-surges** — a refinement to the surge→trough cadence reading.
- **All-template coverage in one batch — the broadest the farm has produced**: Wegovy GLP-1 verbatim ×3 + Hair Hybrids verbatim ×2 + Sex Rx + Testosterone Support ×1 + Sex Rx + Climax Control ×2. Four distinct SKU-templates, all three wedges.
- **Sex Rx + Climax Control RETURNS after silence since batch 7** (IDs `961821243380184` started 2026-04-29 + `1736502914453690` started 2026-06-04) — and **both Sex Rx SKUs (Testosterone Support + Climax Control) are active in the same batch for the first time.** Another "dormant not closed" confirmation: a wedge SKU silent for 9 batches re-fired verbatim. **The 2026-06-04 Climax Control ad opens with *"Introducing the 2-in-1 pill to get harder, and go longer"*** vs the older *"The 2-in-1 pill..."* — an **intro-word A/B variant** inside the otherwise-identical skeleton.
- **Wegovy comes back with 3 verbatim re-launches** (IDs `1515282093530826` started 2026-05-13 + `1293493396304066` started 2026-05-28 + `4320859921505418` started 2026-05-21) after its batch-15 collapse-to-placeholder — confirms "dormant not closed" again; the wave that reopened in batch 14 keeps running.
- **[[ro]] ships 5 placeholders — the largest Ro batch in the farm** (prior max 2 ads, batches 8+12). All `{{product.brand}}` placeholders. Gap-normalized = **0.83 Ro/day**, the normal Ro catalog rate — **Run 5** in Ro's irregular-burst cadence. Cumulative **15 Ro ads across 16 batches, ALL placeholder-only.**
- **[[openai]] 2 placeholders, still catalog-only** (IDs `2424816878031768` started 2026-05-08 [Cluster 2] + `1536018427862624` started 2026-05-18). **Cluster 4 (2026-05-22) does NOT expand this batch — holds at 2 ads.** Cumulative **49 ads across 16 batches, still 1 with copy** (48/49 = 98% placeholders).
- **[[anthropic]] 5th consecutive silence (12+13+14+15+16) — now MEETS the ≥5-silent-batch threshold count** from the batch-11 methodology revision. **BUT the cadence-predicted next-2026-05-11-cluster ad date is ~2026-06-08, which has NOT yet passed** (today is 2026-06-05) — so the silence reaches the threshold count but the prediction window is still open. **Hold the stall call until past 06-08 (~batch 17).** Cumulative **8 ads, 0 with copy.**
- **[[eden]] (TryEden) 3rd consecutive silence (14+15+16)** after the batch-13 first signal — cadence still unknown. The "Eden" filter this batch surfaced **Gardens of Eden + Aelfric Eden + Aelfric Eden UK** noise.
- **Real-signal rate 64.1% (25 of 39)** — high; behind only batch 14's 80% and batches 7+12's 67%. The 6-day gap accumulated mostly tracked-brand creative (Hims kept shipping copy across the window).
- **14 noise ads — 12 "Ro"-substring + 2 "Eden", with 7 NEW first-fire "Ro" pages in one batch** — the **largest single-batch "Ro" noise expansion in the farm**, consistent with the 6-day gap accumulating noise. Non-substring noise events stay at 2 of 16 batches (none this batch).
- **Brand-name filter still untuned — 16th consecutive batch.** Outstanding since 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-06-05.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 199 • New: 39 • Dedup-skipped: 160 (80.4%)
- Gap from prior batch: **6 days** (batch 15 = 2026-05-30)

## Tracked-brand creative inventory

### [[hims]] — 18 new ads (8 verbatim copy across all 3 wedges + both Sex Rx SKUs; 10 placeholders)

The biggest Hims copy batch in the farm — but a **6-day-gap compression artifact**, not a per-day intensification (3.0 Hims/day matches the ~2-2.5/day baseline).

**Wegovy GLP-1 verbatim — 3 re-launches** (canonical *"Get Wegovy® with Hims..."* → ✅ FDA-approved GLP-1 pill and pens / ✅ Medication as low as $149/mo / ✅ 100% online → *"Your goals. Your plan. Your pace."* + expanded $149/$39-membership pricing footnote + Wegovy®/Novo-Nordisk non-affiliation):

- ID `1515282093530826`, started **2026-05-13**
- ID `1293493396304066`, started **2026-05-28**
- ID `4320859921505418`, started **2026-05-21**

**Hair Hybrids verbatim — 2 re-launches** (*"Don't wait — join the hundreds of thousands of guys who've found true results..."* → 🗓️ Regrow in as few as 3-6 months / 🧑🏻‍⚕️ Doctor-trusted ingredients / 📦 Free shipping to your front door (if prescribed) + Hair Hybrids compounded disclaimer):

- ID `1346609827367645`, started **2026-06-02**
- ID `1554859919536031`, started **2026-06-02**

**Sex Rx + Testosterone Support verbatim — 1 re-launch** (*"🔥New Sex Rx + Testosterone Support 🔥"* → 🚀 tadalafil / 💪 zinc / 🍎 L-arginine + B12 + B6 + compounded disclaimer):

- ID `1258797639329555`, started **2026-05-05**

**Sex Rx + Climax Control verbatim — 2 re-launches (wedge RETURNS after silence since batch 7)** (*"...The 2-in-1 pill to get harder, and go longer. Sex Rx + Climax Control combines tadalafil... plus PE treatment..."* → 🤩 Daily pill options / 🧑‍⚕️ Prescribed by licensed providers / 📦 100% online, free discreet shipping + compounded disclaimer):

- ID `961821243380184`, started **2026-04-29** — opens *"The 2-in-1 pill to get harder..."*
- ID `1736502914453690`, started **2026-06-04** — opens **"Introducing the 2-in-1 pill to get harder..."** (intro-word A/B variant)

**10 placeholders** (`{{product.brand}}` body, no static narrative): IDs `837459935727504` (2026-06-02), `2033619974247251` (2026-06-02), `974929168727700` (2026-05-27), `1342601431075754` (2026-05-05), `1928444534459743` (2026-03-26), `867277673054466` (2026-04-09), `1995067031077817` (2026-04-03), `1719539692503467` (2026-05-19), `2134603420638323` (2026-04-09), `1181410460214080` (2025-12-09).

**Strategic significance**: This is the **broadest single-batch verbatim-template coverage in the farm** — all three wedges plus both Sex Rx SKUs (Testosterone Support *and* Climax Control). But the **6-day fetch gap is doing the work**: 18 Hims ads / 6 days = **3.0 Hims/day**, which is *below* batch 14's true 4.0/day one-day surge and consistent with the batch-8/9 ~2.0-2.5/day baseline. The apparent "mega surge" is **6 days of continuous verbatim re-launches across all wedges, compressed into one fetch.** This is the same lesson as batch 8 (4-day gap → apparent three-wedge surge that gap-normalized to baseline), now at a larger gap with even more dramatic apparent magnitude. **Refinement to the surge→trough cadence reading**: at varying fetch gaps, the surge/trough alternation is partly a *sampling artifact* — Hims ships ~3 ads/day mixing wedges + placeholders continuously, and a 1-day sample (batch 15 → 1 placeholder) vs a 6-day sample (batch 16 → 18 ads) produces wildly different apparent magnitudes from the same underlying rate. **Climax Control returning after 9 silent batches is the 3rd "dormant not closed" confirmation** (after Wegovy in batch 14 and the general methodology lesson) — no Hims wedge or SKU has been retired across 16 batches; all remain live [[medvi-positioning]] diff-targets. Cumulative **96 Hims ads across 16 batches.**

### [[ro]] — 5 new ads (largest Ro batch in the farm — Run 5)

All 5 are `{{product.brand}}` placeholders:

- ID `1518002113116670`, started 2026-05-29
- ID `1249902287216650`, started 2026-05-29
- ID `1427177692767852`, started 2026-05-29
- ID `992040536912236`, started 2026-06-01
- ID `2399728897171922`, started 2026-06-01

**Strategic significance**: Ro's largest single-batch volume in the farm (prior max 2 ads, batches 8+12) — but **gap-normalized to 0.83 Ro/day**, the normal Ro catalog rate (Ro has run 0.5-1.0/day across the farm). The 5-ad volume is a **6-day-gap compression**, structurally identical to every prior Ro signal: catalog-driven dynamic creative only, **zero static narrative across 16 batches.** This is **Run 5** in Ro's irregular-burst cadence (Run 1 batches 1-2 / Run 2 batches 7-9 / Run 3 batch 12 / Run 4 batch 15 / Run 5 batch 16). The substantive Ro creative (almost certainly on Roman Health / Ro Body / Ro Health pages) remains absent. Cumulative **15 Ro ads, ALL placeholder-only.**

### [[openai]] — 2 new ads (still catalog-only; Cluster 4 does not expand)

Both carousel `{{product.name}}` / `{{product.brand}}` placeholders:

- ID `2424816878031768`, started **2026-05-08** (Cluster 2 / May 8 expansion — 20+ days post-launch)
- ID `1536018427862624`, started **2026-05-18** (catalog re-surface between Cluster 3's 05-15 and Cluster 4's 05-22; ambiguous, not over-read)

**Strategic significance**: OpenAI reverts to placeholder-only after batch 15's Cluster-4 expansion. **Cluster 4 (2026-05-22) does NOT expand this batch — it holds at the 2 ads from batch 15** (no new 2026-05-22 ad in this 6-day window), so the "Cluster 4 opening" reading neither strengthens nor breaks. **Cluster 3 (2026-05-15) remains stalled at 3 ads / 1 with copy** (the one-off-creative-test reading is now very firm at 21 days post-launch). Cumulative **49 ads across 16 batches, still 1 with copy** (48/49 = 98% placeholders). Lab-comparison delta vs Anthropic in the same 16-batch window: OpenAI 49 / Anthropic 8 — OpenAI's paid-social cadence remains ~6x Anthropic's.

### [[anthropic]] — 0 new ads (5th consecutive silence 12-16; threshold count MET, prediction window still open)

No new Anthropic ads — **5th consecutive silent batch** since the batch-11 slow-cluster expansion (ad #2 of the 2026-05-11 cluster). This **now meets the ≥5-silent-batch threshold count** the batch-11 methodology revision set for claiming an Anthropic cluster stall. **However, the cluster's observed cadence (14 days between ads) predicts the next ad ~2026-06-08, which has not yet passed** (today is 2026-06-05). So the silence-count threshold is met but the prediction window is still open by 3 days. **Hold the stall call until past 06-08 (~batch 17).** Cumulative **8 ads, 0 with copy** — unchanged. Anthropic remains 100% placeholder (8/8) across 16 batches while OpenAI shipped its 1 copy ad in batch 9 (never expanded).

### [[eden]] (TryEden) — 0 new ads (3rd consecutive silence 14+15+16)

No new TryEden ads — **3rd consecutive silent batch** after the batch-13 first-signal placeholder. Three silent batches still don't establish Eden's cadence (irregular like [[ro]], or a single ad then dormant). The "Eden" filter this batch surfaced **Gardens of Eden + Aelfric Eden + Aelfric Eden UK** noise (see below). Whether TryEden ever ships static copy — the [[medvi-positioning]] diff-target — remains the open Eden question. Cumulative **1 Eden ad, placeholder-only.**

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (16th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (16th consecutive batch)

## False positives ("brand-name match" noise) — 14 of 39 ads (35.9%)

**12 "Ro"-substring + 2 "Eden"-substring.** Every noise ad traces to a tracked-brand substring — no non-substring noise this batch (those remain at 2 of 16 batches: Adobe Acrobat batch 3 + Romance miniseries batch 4). **7 NEW first-fire "Ro" pages drew in this batch — the largest single-batch "Ro" noise expansion in the farm**, consistent with the 6-day gap accumulating noise.

### NEW first-fire "Ro" pages (7)

1. **From Head To Toe** (1 video ad, started 2026-05-04) — *"The way I will always stan SPF + Korean-engineered beauty @eadem.co..."* SPF / Korean beauty influencer creative for eadem.co (Sunsuede). Substring root cause "F**ro**m" → bare-"Ro" filter. **First K-beauty / influencer-partner noise page.**
2. **TRELEGY** (1 ad, started 2026-01-05) — *"Discover how TRELEGY works to offer adults with asthma better breathing for 24 hours..."* GSK once-daily asthma inhaler. Substring root cause "fluticasone fu**ro**ate" (in the parenthetical generic name) → bare-"Ro" filter. **First major-pharma (GSK) noise page in the farm** — a legitimate FDA-regulated pharma brand surfaced only by the "ro" letter sequence in a drug compound name.
3. **Diamond Cross Ranch in Jackson Hole** (1 carousel ad, started 2026-04-01) — cowboy/western apparel, 100-year Jackson Hole heritage, "Handcrafted in the USA." Substring root cause "Diamond C**ro**ss" → "Cross". **First western-apparel / heritage-brand noise page.**
4. **Lowe's Home Improvement** (1 carousel ad, started 2026-05-28) — `{{product.brand}}` placeholder. Substring root cause "Imp**ro**vement" → bare-"Ro" filter. **First big-box-retail noise page.**
5. **Ross Fledderjohn** (1 video ad, started 2026-05-21) — *"OpenAI just dropped GPT-5.5 and Codex is the real story nobody's talking about... Try it out at chatgpt.com/codex @openai @openaidevs #ChatGPTPartner"*. Substring root cause "**Ro**ss" → bare-"Ro" filter. **The most notable noise ad of the batch — the first third-party AFFILIATE ad promoting a TRACKED brand's product (OpenAI Codex / GPT-5.5) but on a personal creator page, not OpenAI's official page.** A `#ChatGPTPartner` affiliate/partner-program creator. Content-interesting: it's first-party-product messaging (Codex computer-use, app-building, CRM/Slack/Gmail integration, "what used to take hours now takes under 5 minutes") delivered by an influencer rather than OpenAI — a paid-social surface OpenAI's *own* ad library doesn't capture. First affiliate/partner-program ad in the farm.
6. **Range Rover** (1 carousel ad, started 2026-04-02) — `{{product.name}}` placeholder. Substring root cause "Range **Ro**ver" → "Rover". **First luxury-auto noise page.**
7. **WR Performance Products Inc.** (1 video ad, started 2026-02-21) — *"OFF-ROAD OWNERS ALERT! Get 3 FREE bottles of Total Wash, the touchless cleaning solution for off-road vehicles & heavy machinery!"* Substring root cause "WR Performance P**ro**ducts" → "Products" (and "off-**ro**ad" in body). **First off-road-vehicle-care noise page** — same touchless-cleaning category as the recurring Uproot Clean noise.

### Returning "Ro" noise pages (3)

8. **Cholesterol Support Group** (2 image ads) — BOTH long-form *"Feel Like Yourself Again"* confession narratives: the Tamika/probate-paralegal/mother's-medication-list narrative (started 2026-05-27, ID `1010371368104811` — same as batch 15) AND the Laura/ICU-nurse-statins-skepticism narrative (started 2026-05-06, ID `26613934588269229` — the batch-8 narrative). The page ships **both** confession narratives in one batch — confirming **Cholesterol Support Group A/B-tests multiple long-form confession narratives under one page**. Returning (batches 8 → 13 → 15 → 16). Substring "Choleste**ro**l".
9. **Lauren Brooks** (1 image ad, started 2026-05-24) — the verbatim *"Please STOP buying allergy meds for your dog..."* Henry-the-Cavalier dog-allergy long-form confession. Returning (batches 4+8+9+11+16) — one of the highest-recurrence noise pages. Substring "B**ro**oks".
10. **Uproot Clean** (1 video ad, started 2026-05-11) — *"...NASA developed powerful enzyme technology... Uproot Washing Machine Cleaner Tabs."* Returning (batches 2+4+5+8+16) — **the most-recurring noise page in the farm by batch count (5 batches).** Substring "Up**ro**ot".

### "Eden" noise (2)

11. **Gardens of Eden** (1 carousel ad, `{{product.name}}` placeholder) — garden/landscaping brand. Returning (batch 9 = 11th distinct "Eden" noise brand). Substring exact "Eden".
12. **Aelfric Eden** (1 carousel ad, started 2026-04-03) — *"💥 Spring Collection just dropped. 💥 Fresh Drop — 20% Off..."* Fashion. Returning (batches 1+5+8+16). Substring exact "Eden".
13. **Aelfric Eden UK** (1 video ad, started 2026-03-24) — *"💸Biggest Savings of 2026💸 Limited time only..."* Fashion. **2nd regional-page variant** of Aelfric Eden (after **Aelfric Eden EU** in batch 15). The "Eden" noise-brand count stays at **11 distinct brands** but Aelfric Eden now has **3 distinct FB Pages** (main + EU + UK) — the regional-page-split pattern (cf. SecretRomance `cloudn57`/`cloudn65`) now confirmed across two consecutive batches and **must be enumerated in any page-ID allow/block-list.**

### Cumulative noise-corpus updates

- **"Ro" noise pages**: **+7 new first-fire pages** (From Head To Toe, TRELEGY, Diamond Cross Ranch, Lowe's Home Improvement, Ross Fledderjohn, Range Rover, WR Performance Products) — the largest single-batch "Ro" noise expansion in the farm (gap-inflated). Returning: Cholesterol Support Group (8+13+15+16), Lauren Brooks (4+8+9+11+16), Uproot Clean (2+4+5+8+16 — 5-batch record).
- **"Eden" noise brands**: still **11 distinct** — Aelfric Eden UK is a 2nd regional-page variant of the already-counted Aelfric Eden (after Aelfric Eden EU batch 15), not a new distinct brand; but it IS a new distinct FB Page (3 Aelfric Eden pages now seen: main + EU + UK).
- **"Hampton" noise**: no new pages this batch.
- **Non-substring noise events**: still 2 of 16 batches (12.5%) — none this batch.

## Cross-cutting patterns

### Sixteen-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Ro | Eden | Real-signal % |
|---|---|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | 1 | 0 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | 2 | 0 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 0 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 0 | 0 | 23% |
| 2026-05-15 | 203 | 3 | 200 | 1.5% | 0 | 0 | 0 | 0 | 0 | 0% |
| 2026-05-16 | 208 | 9 | 199 | 4% | 2 | 3 | 0 | 1 | 0 | 67% |
| 2026-05-20 | 213 | 36 | 177 | 17% | 7 | 8 | 0 | 2 | 0 | 47% |
| 2026-05-22 | 208 | 17 | 191 | 8% | 3 | 5 | 1 | 1 | 0 | 59% |
| 2026-05-23 | 211 | 8 | 203 | 4% | 1 | 2 | 0 | 0 | 0 | 37.5% |
| 2026-05-25 | 213 | 12 | 201 | 5.6% | 0 | 2 | 1 | 0 | 0 | 25% |
| 2026-05-26 | 207 | 6 | 201 | 2.9% | 1 | 1 | 0 | 2 | 0 | 67% |
| 2026-05-28 | 207 | 8 | 199 | 3.9% | 1 | 2 | 0 | 0 | 1 | 50% |
| 2026-05-29 | 205 | 5 | 200 | 2.4% | 0 | 4 | 0 | 0 | 0 | 80% |
| 2026-05-30 | 213 | 8 | 205 | 3.8% | 1 | 1 | 0 | 1 | 0 | 37.5% |
| **2026-06-05** | **199** | **39** | **160** | **19.6%** | **2** | **18** | **0** | **5** | **0** | **64.1%** |

Batch 16's 39-new / 80.4%-dedup is the **highest absolute new volume since batch 8** (36 new), reflecting the 6-day fetch gap. Real-signal rate (64.1%) is high — behind only batch 14's 80% and batches 7+12's 67% — because the gap accumulated mostly Hims copy creative.

### Per-day rate — gap-normalized, batch 16 is at baseline, NOT a surge

| Batch | Gap (days) | Total ads | Ads/day | Hims/day | OpenAI/day | Ro/day |
|---|---|---|---|---|---|---|
| 8 | 4 | 36 | 9.0 | 2.00 | 1.75 | 0.50 |
| 9 | 2 | 17 | 8.5 | 2.50 | 1.50 | 0.50 |
| 10 | 1 | 8 | 8.0 | 2.00 | 1.00 | 0 |
| 11 | 2 | 12 | 6.0 | 1.00 | 0 | 0 |
| 12 | 1 | 6 | 6.0 | 1.00 | 1.0 | 2.0 |
| 13 | 2 | 8 | 4.0 | 1.0 | 0.5 | 0 |
| 14 | 1 | 5 | 5.0 | 4.0 | 0 | 0 |
| 15 | 1 | 8 | 8.0 | 1.0 | 1.0 | 1.0 |
| **16** | **6** | **39** | **6.5** | **3.0** | **0.33** | **0.83** |

Batch 16's **6.5 ads/day total** sits in the 6-9/day band. The **3.0 Hims/day** is *below* batch 14's true 4.0/day one-day surge and consistent with the batch-8/9 ~2.0-2.5/day baseline — **the 8-copy-ad "mega three-wedge surge" is a 6-day-gap compression artifact, not an intensification.** Ro 0.83/day and OpenAI 0.33/day are both at normal catalog rates. **Methodological refinement**: the farm's surge→trough "cadence" is partly a *sampling artifact* of varying fetch gaps — Hims ships ~3 ads/day mixing wedges + placeholders continuously; a 1-day sample (batch 15 → 1 placeholder) vs a 6-day sample (batch 16 → 18 ads) produces order-of-magnitude-different apparent volumes from the same underlying rate. **All per-day comparisons must gap-normalize before reading surge/trough.**

## Open questions

- **Does Anthropic's 2026-05-11 cluster surface a 3rd ad past ~2026-06-08?** Batch 16 is the 5th silent batch (meets the threshold count) but the cadence-prediction window doesn't close until ~06-08 — batch 17 (past that date) decides between "slow-cluster continues" and "cluster stalled at 2 ads."
- **Does Hims sustain copy at a true ~3 ads/day on the next 1-day-gap batch, or revert to a thin placeholder trough?** Only a clean 1-day-gap batch 17 can distinguish a genuine elevated rate from the 6-day-gap compression seen here.
- **Does Sex Rx + Climax Control stay active now that it has returned, or go dormant again?** Both Sex Rx SKUs are live for the first time — watch whether they alternate or co-run.
- **Does OpenAI Cluster 4 (2026-05-22) expand to 3+ ads, or is it stalled at 2?** No 2026-05-22 ad in this 6-day window — the cluster neither expanded nor was confirmed closed.
- **Does TryEden surface a 2nd ad, and does it ever ship static copy?** Three silent batches (14+15+16) after the first signal — cadence still unknown.

## Related

- [[competitor-ads-farm]] — sixteenth batch from this farm; 6-day-gap compression; Hims biggest copy batch (8 verbatim across all 3 wedges + both Sex Rx SKUs) but 3.0/day baseline; Climax Control returns; Ro largest batch (Run 5); Anthropic 5th silence (threshold met, window open); 7 new "Ro" noise pages
- [[hims]] — 18 ads (8 verbatim copy + 10 placeholder); all 3 wedges + both Sex Rx SKUs; Climax Control returns after batch 7; gap-compression mega-surge; cumulative 96 ads
- [[ro]] — 5 placeholders (largest Ro batch — Run 5); cumulative 15 ads, all placeholder-only
- [[openai]] — 2 carousel placeholders; still catalog-only; Cluster 4 holds at 2; Cluster 3 stalled at 3/1; cumulative 49 ads, 1 with copy
- [[anthropic]] — 0 new ads; 5th consecutive silence (12-16); threshold count met but prediction window (~06-08) still open; cumulative 8 ads
- [[eden]] — TryEden 3rd consecutive silence (14+15+16); Gardens of Eden + Aelfric Eden + Aelfric Eden UK noise
- [[concepts/dtc-telehealth-ad-template]] — broadest single-batch verbatim coverage (all 3 wedges + both Sex Rx SKUs); Climax Control intro-word A/B variant; all templates dormant-not-closed diff-targets
- [[concepts/compounded-drug-disclaimer]] — all three wedge disclaimer blocks ship verbatim again; Climax Control compounded disclaimer returns
- [[ads-digest-2026-05-30]] — fifteenth batch (three-wedge surge does not sustain; broad-thin signal; OpenAI Cluster 4 reaches 2)

## Appears in

- Sixteenth entry in `wiki/sources/` for the competitor-ads farm. **6-day-gap batch (largest since batch 8) — gap-inflated; read per-day-normalized.** **[[hims]] ships its biggest copy volume in the farm — 8 verbatim static-copy ads across ALL THREE wedges AND both Sex Rx SKUs** (Wegovy ×3 + Hair Hybrids ×2 + Sex Rx Testosterone Support ×1 + Sex Rx Climax Control ×2) + 10 placeholders = 18 Hims ads — but **3.0 Hims/day gap-normalized = baseline, NOT an intensification** (the clearest compression-artifact demonstration since batch 8; a refinement to the surge→trough cadence reading — varying gaps make multi-wedge batches look like mega-surges). **Sex Rx + Climax Control RETURNS** after silence since batch 7 (both Sex Rx SKUs now active in one batch for the first time; the 2026-06-04 ad uses an "Introducing the 2-in-1 pill" intro-word A/B variant). **Wegovy back with 3 verbatim re-launches** after batch-15 collapse (dormant-not-closed again). **[[ro]] ships 5 placeholders — largest Ro batch (Run 5)**, 0.83/day gap-normalized = normal rate. **[[openai]] 2 placeholders, still catalog-only; Cluster 4 (2026-05-22) holds at 2; cumulative 49 ads, 1 with copy.** **[[anthropic]] 5th consecutive silence (12-16) — threshold count MET but cadence-prediction window (~06-08) still open; hold the stall call.** **[[eden]] (TryEden) 3rd consecutive silence (14+15+16).** Real-signal rate 64.1% (25 of 39). **14 noise ads — 12 "Ro" + 2 "Eden", with 7 NEW first-fire "Ro" pages** (largest single-batch "Ro" noise expansion): From Head To Toe, TRELEGY (first major-pharma noise, GSK, via "furoate"), Diamond Cross Ranch, Lowe's, Ross Fledderjohn (first third-party affiliate ad promoting a tracked brand — OpenAI Codex/GPT-5.5 #ChatGPTPartner on a personal page), Range Rover, WR Performance Products + returning Cholesterol Support Group (both confession narratives) / Lauren Brooks / Uproot Clean (5-batch record) / Gardens of Eden / Aelfric Eden + Aelfric Eden UK (2nd regional-page variant). Henry Meds / Hampton / DealMachine — 16th consecutive batch no signal. Cumulative 96 Hims / 49 OpenAI / 8 Anthropic / 15 Ro / 1 Eden ads.
