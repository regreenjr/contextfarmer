---
title: FB Ads Digest — Competitor brands — 2026-07-04
category: source
summary: Thirtieth competitor-ads farm batch — **1 new FB Ad Library entry** (186 fetched, 185 dedup-skipped = 99.46% dedup, effectively tying batch 23/25 for the thinnest batch in the farm) at a **clean 1-day gap** from batch 29 (2026-07-03); **1 of 1 tracked-brand signal (100%)** — the FIRST 1-ad batch that is 100% signal rather than 100% noise (batch 23 = Aelfric Eden noise, batch 25 = Uproot Clean noise; batch 30 INVERTS them). The lone ad is a **[[ro]] catalog placeholder** (ID `1339969168063697`, started 2026-06-14, format unknown, body `{{product.brand}}`) — **Ro RETURNS from the 2-batch trough (28+29) — Run 10**; 1 ad / 1 day = 1.0/day, inside Ro's 0.5-1.0/day band; still catalog-only, **zero static narrative across 30 batches** (cumulative 27 Ro ads). **All 7 other tracked brands silent** — [[hims]] SILENT (first since batch 28; 29→30 reads surge→silence after batch 29's two-wedge return; cumulative 131), [[openai]] SILENT (its batch-29 verbatim o3 Deep Research re-fire gets NO new data — the "does the re-fire expand or is it a single re-fire" question carries to batch 31; cumulative 83, 4 with copy), [[anthropic]] **19th consecutive silence (12-30), STRICT LOCK HOLDS** (Microsoft Cloud also absent for the 8th batch running 23-30; cumulative 8, 0 with copy), [[eden]] (TryEden) **17th consecutive silence (14-30)** (cumulative 1). **0 noise ads** — the whole "Ro"/"Eden"/"Hampton" substring-noise corpus was dedup-cached, so the only thing that surfaced on this clean-1-day day was a single Ro catalog re-surface. Cumulative **131 Hims / 83 OpenAI / 8 Anthropic / 27 Ro / 1 Eden**
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, batch-30, clean-1-day-gap, thinnest-signal-batch, single-ad-batch, 100-percent-signal, first-100-percent-signal-thin-batch, zero-noise-batch, ro-run-10, ro-returns-from-trough, ro-catalog-cluster-cadence, hims-silent, surge-to-silence, openai-silent, o3-refire-no-data, anthropic-19th-silence, anthropic-strict-lock-holds, microsoft-cloud-absent, eden-17th-silence, lab-paid-social-divergence]
sources: 1
source_path: raw/ads/digest-2026-07-04.md
source_date: 2026-07
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-07-04
updated: 2026-07-04
---

# FB Ads Digest — 2026-07-04

Thirtieth batch from the [[competitor-ads-farm]]. **1 new ad, 185 dedup-skipped** out of 186 fetched (**99.46% dedup — effectively tying batch 23/25 for the thinnest batch in the farm**) at a **clean 1-day gap** from batch 29 (2026-07-03). Apify `facebook-ads-library-scraper` actor. **1 of 1 new ads is tracked-brand signal (100%)** — the lone ad is a Ro catalog placeholder. This is the **thinnest signal-bearing batch in the farm**: the third 1-ad batch (after batch 23 on 2026-06-26 and batch 25 on 2026-06-28), but the FIRST that is 100% signal rather than 100% noise — batch 30 **inverts** its two 1-ad predecessors.

## TL;DR

- **The thinnest signal-bearing batch in the farm — 1 new ad, 100% tracked-brand signal.** The prior two 1-ad batches (23 + 25) were both 0%-signal noise-only days (Aelfric Eden UK, Uproot Clean). Batch 30 flips that: the single ad that surfaced past the 99.46% dedup wall is a genuine [[ro]] catalog placeholder, and **0 noise ads** drew in — the whole "Ro"/"Eden"/"Hampton" substring-noise corpus was dedup-cached, so the only thing new on this clean-1-day day was one Ro catalog re-surface.
- **[[ro]] RETURNS from the 2-batch trough (28+29) — Run 10.** 1 placeholder (ID `1339969168063697`, started 2026-06-14, format unknown, body `{{product.brand}}`). Run 9 (batches 26+27) ended in batch 28; the 28+29 trough sat inside Ro's ~3-batch mean trough band and ends here at 2 batches — exactly as Ro's irregular burst→trough→burst cadence predicts. 1 ad / 1 day = 1.0/day, top of Ro's 0.5-1.0/day band. Pattern unchanged: catalog-driven dynamic creative only, **zero static narrative across 30 batches**. Cumulative **27 Ro ads, ALL placeholder-only**.
- **[[hims]] SILENT — 29→30 reads surge→silence.** After batch 29's two-wedge return (the NEW Generic-Viagra Sex Rx SKU + a Hair Hybrids verbatim re-launch), Hims ships nothing — its first silence since batch 28. The 28→29→30 clean-1-day sequence reads silence → two-wedge return → silence; the wedge mix keeps rotating/troughing day-to-day. No wedge/SKU has ever retired across 30 batches (all dormant-not-closed). → [[dtc-telehealth-ad-template]], [[compounded-drug-disclaimer]] (no new template/disclaimer data this batch). Cumulative **131 ads**.
- **[[openai]] SILENT — the batch-29 o3 Deep Research re-fire gets NO new data.** No new OpenAI ad (copy or placeholder), so batch 30 neither expands nor closes the batch-29 verbatim o3 re-launch (the farm's first-ever copy-ad re-fire, which broke the batch-24 "confirmed one-off" call → [[openai-narrative-ad-experiments]]). The "does the re-fire expand into a sustained campaign or is it a single re-fire like each prior copy ad?" question carries to batch 31. Cumulative **83 ads, still 4 with copy — 3 distinct creatives** (79/83 = 95% placeholder); lab-delta vs Anthropic 83/8 (~10.4x).
- **[[anthropic]] 19th consecutive silence (12-30) on its own page — STRICT LOCK HOLDS.** No new Anthropic-page ad; the 2026-05-11 cluster remains confirmed-stalled at 2 ads (locked in batch 20). No earned-media / WSJ-custom-content candidate surfaced this batch. **Microsoft Cloud also absent for the 8th batch running (23-30)** — the sustained Microsoft AI campaign of batches 21+22 stays closed at 2 and the AI-lab paid-social field is OpenAI-only. Cumulative **8 ads, 0 with copy** — 100% placeholder across 30 batches; lab-delta vs OpenAI 8/83 (~10.4x).
- **[[eden]] (TryEden) 17th consecutive silence (14-30).** No new TryEden ad and — for once — no new "Eden"-substring noise brand either (the noise corpus was dedup-cached). Cumulative **1 Eden ad, placeholder-only**.

## Source

- Path: `raw/ads/digest-2026-07-04.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 186 • New: 1 • Dedup-skipped: 185 (99.46% — effectively ties batch 23/25 as thinnest)
- Gap from prior batch: **1 day** (batch 29 = 2026-07-03)

## Tracked-brand creative inventory

### [[ro]] — 1 new ad (Run 10)

- **1 placeholder** — ID `1339969168063697`, started 2026-06-14, format unknown, body `{{product.brand}}`. Returns from the 2-batch trough (28+29) — **Run 10** in Ro's irregular-burst cadence (Run 1 batches 1-2 / Run 2 batches 7-9 / Run 3 batch 12 / Run 4 batch 15 / Run 5 batch 16 / Run 6 batch 18 / Run 7 batch 20 / Run 8 batches 21-22 / Run 9 batches 26-27 / **Run 10 batch 30**). 1.0/day, inside Ro's 0.5-1.0/day band. Still catalog-only; zero static narrative across 30 batches. Cumulative **27 ads**.

### All other tracked brands — 0 new ads

- **[[hims]]** — silent (first since batch 28; 29→30 reads surge→silence after batch 29's two-wedge return). Cumulative **131 ads**.
- **[[openai]]** — silent; the batch-29 verbatim o3 Deep Research re-fire gets NO new data (expand-or-single-re-fire question carries to batch 31). Cumulative **83 ads, 4 with copy**.
- **[[anthropic]]** — silent; 19th consecutive (12-30); strict lock holds; Microsoft Cloud absent for the 8th batch running (23-30). Cumulative **8 ads, 0 with copy**.
- **[[eden]]** (TryEden) — silent; 17th consecutive (14-30). Cumulative **1 ad, placeholder**.
- **[[henry-meds]]** — never appeared (30th consecutive batch).
- **[[hampton-founders]]** — 0 new since 2026-05-06.
- **DealMachine** — never appeared (30th consecutive batch).

## "Noise" inventory — 0 of 1 ads (0%)

- **None.** For the first time in a 1-ad batch, the lone new ad is tracked-brand signal (Ro), not substring noise. The recurring "Ro" / "Eden" / "Hampton" noise pages (Uproot Clean, Eden & Om, Aelfric Eden, Hero FinCorp, etc.) were all dedup-cached — nothing new drew in. **Microsoft Cloud is absent** for the 8th batch running (23-30), confirming its batches-21+22 AI-lab-adjacent campaign stays closed at 2 creatives.

## Cross-cutting patterns

### The three 1-ad batches — signal vs noise

| # | Batch | Date | New | Dedup | Signal % | Lone ad |
|---|---|---|---|---|---|---|
| 1 | 23 | 2026-06-26 | 1 | 99.5% | 0% | Aelfric Eden UK noise |
| 2 | 25 | 2026-06-28 | 1 | 99.5% | 0% | Uproot Clean noise |
| 3 | **30** | **2026-07-04** | **1** | **99.46%** | **100%** | **Ro placeholder (Run 10 signal)** |

Batches 23 and 25 were universal-tracked-brand-silence / 0%-signal days where the single ad was substring noise. Batch 30 is the **inverse** — the same thinness (1 ad, ~99.5% dedup) but the lone ad is a genuine tracked-brand catalog re-surface and 0 noise drew in. So the thinnest days are NOT structurally identical: whether the one ad that clears the dedup wall is signal or noise is effectively a coin-flip on a near-empty day.

### Thirty-batch convergence (recent batches)

| Batch | Date | Fetched | New | Dedup | New % | OpenAI | Hims | Anthropic | Ro | Eden | Signal % |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 26 | 2026-06-30 | 185 | 9 | 176 | 4.9% | 3 | 3 | 0 | 1 | 0 | 77.8% |
| 27 | 2026-07-01 | 183 | 10 | 173 | 5.5% | 1 | 2 | 0 | 2 | 0 | 50% |
| 28 | 2026-07-02 | 191 | 5 | 186 | 2.6% | 4 | 0 | 0 | 0 | 0 | 80% |
| 29 | 2026-07-03 | 183 | 7 | 176 | 3.8% | 2 | 3 | 0 | 0 | 0 | 71.4% |
| **30** | **2026-07-04** | **186** | **1** | **185** | **0.5%** | **0** | **0** | **0** | **1** | **0** | **100%** |

(Full table in [[ads-digest-2026-06-09]] / [[ads-digest-2026-06-24]].) Batch 30 is the thinnest since batch 25 and the first 100%-signal batch since batch 28 (which was OpenAI-only) — but at a single ad, the "100%" is one Ro placeholder, not a signal surge.

### What did NOT happen this batch

- **No new OpenAI creative** — the batch-29 o3 re-fire expand-vs-single-re-fire question stays open for batch 31.
- **No new Hims wedge/SKU data** — the batch-29 Generic-Viagra Sex Rx SKU and Hair Hybrids trough both silent; no template or disclaimer diff-target shipped.
- **No new Microsoft Cloud creative** — absent for the 8th batch running (23-30); the batches-21+22 campaign stays closed at 2.
- **No new "Eden"-substring noise brand** — the noise corpus was fully dedup-cached (a rare zero-noise batch).

## Open questions

- **Does OpenAI's batch-29 verbatim o3 Deep Research re-fire expand into a sustained campaign, or is it a single re-fire?** Batch 30 adds no data; batch 31 carries the resolution → [[openai-narrative-ad-experiments]].
- **Does Ro's Run 10 continue into a 2nd consecutive active batch (batch 31)?** Runs 8 and 9 both terminated at exactly 2 batches — a 3rd consecutive-active would break the "2-batch run" hypothesis; a batch-31 silence would confirm a single-batch Run 10.
- **Is Anthropic's own-page silence permanent or pre-launch?** 19 consecutive batches; any future ad = a NEW launch window.
- **Does Hims return next batch (confirming the daily surge→silence→surge rotation)?** Batch 29→30 surge→silence; batch 31 tests whether the trough is a single day.

## Related

- [[competitor-ads-farm]] — thirtieth batch; clean 1-day gap; thinnest signal-bearing batch in the farm (1 new ad, 100% signal, 0 noise); the 3rd 1-ad batch (after 23 + 25) but the FIRST that is 100% signal; Ro Run 10 returns from the 28+29 trough; Hims/OpenAI/Anthropic/Eden silent; Anthropic 19th silence (strict lock holds); Microsoft Cloud absent 8th batch running
- [[ro]] — 1 placeholder, Run 10 returns from the 2-batch trough (28+29); cumulative 27 ads, all placeholder
- [[hims]] — silent (first since batch 28; 29→30 surge→silence); cumulative 131 ads
- [[openai]] — silent; batch-29 o3 re-fire gets no new data (question carries to batch 31); cumulative 83 ads, 4 with copy
- [[anthropic]] — 0 new ads; 19th consecutive silence (12-30); strict lock holds; cumulative 8 ads
- [[eden]] — TryEden 17th consecutive silence (14-30); cumulative 1 Eden ad
- [[ads-digest-2026-07-03]] — twenty-ninth batch (the signal-side predecessor: OpenAI o3 re-fire breaks the one-off call, Hims new Generic-Viagra Sex Rx SKU)

## Appears in

- Thirtieth entry in `wiki/sources/` for the competitor-ads farm. **1 new ad, 100% tracked-brand signal (Ro)** at a clean 1-day gap — the **thinnest signal-bearing batch in the farm** (99.46% dedup) and the FIRST 1-ad batch that is 100% signal rather than 100% noise (INVERTS batch 23 + batch 25). Lone ad = a **[[ro]] catalog placeholder** (ID `1339969168063697`, started 2026-06-14, body `{{product.brand}}`) — **Ro Run 10 returns from the 2-batch trough (28+29)**. **All 7 other tracked brands silent** — [[hims]] silent (29→30 surge→silence), [[openai]] silent (batch-29 o3 re-fire gets no new data), [[anthropic]] 19th consecutive silence (12-30, strict lock holds), [[eden]] 17th consecutive silence (14-30). **0 noise ads; Microsoft Cloud absent 8th batch running (23-30).** Cumulative **131 Hims / 83 OpenAI / 8 Anthropic / 27 Ro / 1 Eden**.
</content>
</invoke>
