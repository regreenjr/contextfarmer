---
title: FB Ads Digest — Competitor brands — 2026-06-26
category: source
summary: Twenty-third competitor-ads farm batch — **1 new FB Ad Library entry** (198 fetched, 197 dedup-skipped, 99.5% — the HIGHEST dedup rate and THINNEST new-ad batch in the farm) at a **clean 1-day gap** from batch 22 (2026-06-25); **0 of 1 tracked-brand signal (0%)** — the **3rd universal-tracked-brand-silence / 0%-signal batch** in the farm after batch 6 (2026-05-15) and batch 19 (2026-06-08), and the thinnest of the three (1 ad vs batch 6's 3 and batch 19's 2). **All 8 tracked brands silent.** The lone new ad is **Aelfric Eden UK** (UK streetwear brand, "Eden" substring noise — ID `1246605534224502`, started 2026-03-24, video, *"💸Biggest Savings of 2026💸 / Limited time only ⏰ Selling out fast"*), a recurring noise page (batches 5/8/16/21). **[[hims]] SILENT** after batch 22's 2 verbatim copy ads — the 22→23 clean-1-day sequence reads surge→silence (Hims' sharpest single-day swing since 18→19); first Hims silence since batch 19. **[[openai]] SILENT — the batch-21 o3 Deep Research one-off question gets NO new data this batch** (neither confirmed nor denied); cumulative **67 ads, still 2 with copy**. **[[ro]] SILENT — Run 8 ends after 2 consecutive active batches (21+22)**, back to trough; cumulative **23 ads**. **[[anthropic]] 12th consecutive silence (12-23) — STRICT LOCK HOLDS**; cumulative **8 ads, 0 with copy**. **[[eden]] (TryEden) 10th consecutive silence (14-23).** **Microsoft Cloud NOT present** — its 2-batch AI-lab-adjacent campaign (batches 21+22) gets no new data in this thin batch. Cumulative **122 Hims / 67 OpenAI / 8 Anthropic / 23 Ro / 1 Eden**
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, batch-23, clean-1-day-gap, thinnest-batch, highest-dedup-rate, universal-silence, zero-signal-batch, third-universal-silence, all-brands-silent, noise-only-batch, aelfric-eden-uk-noise, eden-substring-noise, hims-silent, surge-to-silence, openai-silent, o3-one-off-unresolved, ro-silent, ro-run-8-ends, anthropic-12th-silence, anthropic-strict-lock-holds, eden-10th-silence, microsoft-cloud-absent, lab-paid-social-divergence]
sources: 1
source_path: raw/ads/digest-2026-06-26.md
source_date: 2026-06
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-06-26
updated: 2026-06-26
---

# FB Ads Digest — 2026-06-26

Twenty-third batch from the [[competitor-ads-farm]]. **1 new ad, 197 dedup-skipped** out of 198 fetched (**99.5% dedup — the highest dedup rate in the farm**, beating batch 6's 98.5%) at a **clean 1-day gap** from batch 22 (2026-06-25). Apify `facebook-ads-library-scraper` actor. **0 of 1 new ads is tracked-brand signal (0%)** — the lone ad is "Eden"-substring noise. This is the **3rd universal-tracked-brand-silence / 0%-signal batch** in the farm (after batch 6 on 2026-05-15 and batch 19 on 2026-06-08), and the **thinnest absolute batch ever** (1 new ad).

## TL;DR

- **All 8 tracked brands silent — the 3rd universal-silence / 0%-signal batch (after batch 6 and batch 19).** No Hims, OpenAI, Ro, Anthropic, Eden (TryEden), Henry Meds, Hampton, or DealMachine ad surfaced. At a clean 1-day gap this is a genuine daily trough, not a fetch-gap artifact — the farm sometimes produces a near-empty day, and 99.5% dedup says virtually everything fetched was already seen.
- **[[hims]] SILENT — 22→23 reads surge→silence.** After batch 22 shipped 2 verbatim copy ads (Wegovy + Sex Rx Climax Control), Hims ships nothing — its sharpest single-day swing since 18→19 (4 copy → 0) and first Hims silence since batch 19. Reads as a normal inventory-cycle trough in the surge-trough alternation, not a structural shift; no Hims wedge or SKU has ever retired across 23 batches. → [[dtc-telehealth-ad-template]], [[compounded-drug-disclaimer]] (no new template/disclaimer data this batch). Cumulative **122 ads**.
- **[[openai]] SILENT — the batch-21 o3 Deep Research one-off question gets NO new data.** No new OpenAI ad (copy or placeholder), so batch 23 neither confirms nor denies whether the batch-21 o3 Deep Research narrative (ID `869733176204909`, started 2026-06-18) was a one-off like the batch-9 Codex promo. The "watch batches 23-24" call from batch 22 carries forward to batch 24. Cumulative **67 ads, still 2 with copy** (65/67 = 97% placeholder); lab-delta vs Anthropic 67/8 (~8.4x).
- **[[ro]] SILENT — Run 8 ends after 2 consecutive active batches (21+22).** The rare consecutive-active Ro streak (batches 21+22) closes; Ro returns to its irregular burst→trough cadence. Cumulative **23 ads, all placeholder**, zero static narrative across 23 batches.
- **[[anthropic]] 12th consecutive silence (12-23) on its own page — STRICT LOCK HOLDS.** No new Anthropic-page ad; the 2026-05-11 cluster remains confirmed-stalled at 2 ads (locked in batch 20). No earned-media / WSJ-custom-content candidate surfaced this batch. Cumulative **8 ads, 0 with copy** — 100% placeholder across 23 batches.
- **[[eden]] (TryEden) 10th consecutive silence (14-23).** No new TryEden ad — ten silent batches and Eden's cadence still isn't established. Cumulative **1 Eden ad, placeholder-only**.
- **1 noise ad (100% of the batch) — Aelfric Eden UK.** UK streetwear brand (*"💸Biggest Savings of 2026💸 / Limited time only ⏰ Selling out fast — grab yours."*, video, ID `1246605534224502`, started 2026-03-24) — pure "Eden" substring noise and a recurring page (batches 5/8/16/21). **Microsoft Cloud is absent** this batch, so its 2-batch AI-lab-adjacent paid-social campaign (batches 21+22) gets no new data.

## Source

- Path: `raw/ads/digest-2026-06-26.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 198 • New: 1 • Dedup-skipped: 197 (99.5% — highest in the farm)
- Gap from prior batch: **1 day** (batch 22 = 2026-06-25)

## Tracked-brand creative inventory

### All tracked brands — 0 new ads

- **[[hims]]** — silent (first silence since batch 19; 22→23 reads surge→silence after 2 copy ads). Cumulative **122 ads**.
- **[[openai]]** — silent; o3 Deep Research one-off question unresolved (no new data). Cumulative **67 ads, 2 with copy**.
- **[[ro]]** — silent; Run 8 ends after 2 consecutive active batches (21+22). Cumulative **23 ads, all placeholder**.
- **[[anthropic]]** — silent; 12th consecutive (12-23); strict lock holds. Cumulative **8 ads, 0 with copy**.
- **[[eden]]** (TryEden) — silent; 10th consecutive (14-23). Cumulative **1 ad, placeholder**.
- **[[henry-meds]]** — never appeared (23rd consecutive batch).
- **[[hampton-founders]]** — 0 new since 2026-05-06.
- **DealMachine** — never appeared (23rd consecutive batch).

## "Noise" inventory — 1 of 1 ads (100%)

- **Aelfric Eden UK** — UK streetwear/fashion brand, *"💸Biggest Savings of 2026💸 / Limited time only ⏰ Selling out fast — grab yours."* (video, ID `1246605534224502`, started 2026-03-24). Pure "Eden" substring noise; a recurring noise page (batches 5 + 8 + 16 + 21, now batch 23 — across regional "Aelfric Eden" / "Aelfric Eden UK" / "Aelfric Eden EU" page variants). Not a tracked brand and not telehealth-relevant.

## Cross-cutting patterns

### Twenty-three-batch farm convergence table (recent batches)

| Batch | Date | Fetched | New | Dedup | New % | OpenAI | Hims | Anthropic | Ro | Eden | Signal % |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 19 | 2026-06-08 | 200 | 2 | 198 | 1.0% | 0 | 0 | 0 | 0 | 0 | 0% |
| 20 | 2026-06-09 | 210 | 14 | 196 | 6.7% | 4 | 4 | 0 | 2 | 0 | 71.4% |
| 21 | 2026-06-24 | 202 | 49 | 153 | 24.3% | 12 | 13 | 0 | 3 | 0 | 57.1% |
| 22 | 2026-06-25 | 200 | 6 | 194 | 3.0% | 1 | 2 | 0 | 1 | 0 | 66.7% |
| **23** | **2026-06-26** | **198** | **1** | **197** | **0.5%** | **0** | **0** | **0** | **0** | **0** | **0%** |

(Full table in [[ads-digest-2026-06-09]] / [[ads-digest-2026-06-24]].) Batch 23 is the **thinnest batch in the farm** (1 new ad, 99.5% dedup) and the **3rd 0%-signal batch** — a clean-1-day daily trough.

### The three universal-silence batches

| # | Batch | Date | New | Notes |
|---|---|---|---|---|
| 1 | 6 | 2026-05-15 | 3 | First 100%-noise / universal-silence batch; thinnest at the time |
| 2 | 19 | 2026-06-08 | 2 | 2nd; both noise; surfaced the Rx Pros [[glp1-price-undercut]] ad as noise |
| 3 | **23** | **2026-06-26** | **1** | **3rd; thinnest ever; lone ad = Aelfric Eden UK noise; follows a 22→23 surge→silence swing** |

The universal-silence batches recur at an irregular ~13-batch interval (6 → 19 → 23) and consistently coincide with Hims troughing after a copy-ad batch — batch 22 (Hims 2 copy) → batch 23 (silence) mirrors batch 18 (Hims 4 copy) → batch 19 (silence).

### What did NOT happen this batch

- **No new OpenAI creative** — the o3 Deep Research one-off vs sustained-campaign question stays open for batch 24.
- **No new Microsoft Cloud creative** — the 2-batch AI-lab-adjacent campaign (21+22) gets no confirmation or extension.
- **No Hims wedge/SKU data** — Wegovy / Hair Hybrids / Sex Rx / Hard Mints all silent; no template or disclaimer diff-target shipped.

## Open questions

- **Is OpenAI's o3 Deep Research ad a one-off (like the Codex promo) or the start of a sustained brand-proof campaign?** Batch 23 adds no data; batch 24 now carries the resolution.
- **Does Microsoft sustain its AI-lab-adjacent paid-social campaign past 2 batches?** Absent in batch 23 — watch whether it returns.
- **Does Hims return next batch (confirming the surge→silence→surge daily cadence)?** Batch 22→23 surge→silence; batch 24 tests whether the trough is a single day.
- **Is Anthropic's own-page silence permanent or pre-launch?** 12 consecutive batches; any future ad = a NEW launch window.

## Related

- [[competitor-ads-farm]] — twenty-third batch; clean 1-day gap; thinnest batch in the farm (1 new ad, 99.5% dedup); 3rd universal-silence / 0%-signal batch (after batch 6 + batch 19); all 8 tracked brands silent; Hims surge→silence; OpenAI o3 question unresolved; Ro Run 8 ends; Anthropic 12th silence (strict lock holds); Eden 10th silence; Microsoft Cloud absent
- [[hims]] — silent (first since batch 19; 22→23 surge→silence after 2 copy ads); cumulative 122 ads
- [[openai]] — silent; o3 Deep Research one-off question unresolved (no new data); cumulative 67 ads, 2 with copy
- [[ro]] — silent; Run 8 ends after 2 consecutive active batches; cumulative 23 ads, all placeholder
- [[anthropic]] — 0 new ads; 12th consecutive silence (12-23); strict lock holds; cumulative 8 ads
- [[eden]] — TryEden 10th consecutive silence (14-23); cumulative 1 Eden ad
- [[ads-digest-2026-06-25]] — twenty-second batch (the surge-side predecessor: Hims 2 copy ads, OpenAI reverts to catalog-only, Microsoft 2nd creative)

## Appears in

- Twenty-third entry in `wiki/sources/` for the competitor-ads farm. **1 new ad, 0 tracked-brand signal (0%)** at a clean 1-day gap — the **thinnest batch in the farm** (99.5% dedup, highest ever) and the **3rd universal-tracked-brand-silence batch** (after batch 6 + batch 19). **All 8 tracked brands silent.** Lone ad = **Aelfric Eden UK** noise (*"💸Biggest Savings of 2026💸"*, recurring "Eden"-substring page). **[[hims]] silent** (22→23 surge→silence after 2 copy ads). **[[openai]] silent** (o3 Deep Research one-off question unresolved). **[[ro]] silent** (Run 8 ends after 2 consecutive active batches). **[[anthropic]] 12th consecutive silence (12-23), strict lock holds.** **[[eden]] 10th consecutive silence (14-23).** **Microsoft Cloud absent.** Cumulative **122 Hims / 67 OpenAI / 8 Anthropic / 23 Ro / 1 Eden**.
</content>
</invoke>
