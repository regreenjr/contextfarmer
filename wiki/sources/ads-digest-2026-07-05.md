---
title: FB Ads Digest — Competitor brands — 2026-07-05
category: source
summary: Thirty-first competitor-ads farm batch — **2 new FB Ad Library entries** (190 fetched, 188 dedup-skipped = 98.9% dedup) at a **clean 1-day gap** from batch 30 (2026-07-04); **1 of 2 tracked-brand signal (50%)**. The lone signal ad is a **[[openai]] catalog placeholder** (carousel, ID `964016993098345`, started **2026-05-08** — a Cluster-2-window / Apr 30–May 8 re-surface via the catalog feed, headline `{{product.name}}` / body `{{product.brand}}`) — **OpenAI RETURNS from the batch-30 silence and REVERTS to catalog-only**; the batch-29 verbatim o3 Deep Research re-fire gets NO continuation across batches 30 (silent) + 31 (catalog-only) — 2 clean batches without recurrence lean the re-fire toward a **single re-fire** (the batch-9/batch-21/batch-27 one-off shape), but **dormant-not-closed** per the rule that broke in batch 29 → [[openai-narrative-ad-experiments]]; cumulative **84 OpenAI ads, still 4 with copy — 3 distinct creatives** (80/84 = 95% placeholder); lab-delta vs Anthropic 84/8 (~**10.5x — new widest in the farm**). The 1 noise ad is a genuinely new category — **Ophthalmology at BMJ Group** (image, ID `1486005956228016`, started 2026-04-30; *"Innovations in Ophthalmology: Integrating AI, Imaging, and Omics"* topic collection in BMJ Open Ophthalmology) — the farm's **first academic/medical-journal-publisher noise page** and a **non-substring AI-lab-adjacent** result (no tracked-brand substring; surfaced via the AI-lab search adjacency, the Microsoft-Cloud mechanism). **All 7 other tracked brands silent** — [[hims]] SILENT (2nd consecutive, 30+31; cumulative 131), [[ro]] SILENT — **Run 10 ENDS after a SINGLE batch (batch 30 only) — the FIRST single-batch Run in the farm**, breaking the emerging "2-batch run" hypothesis (Runs 8 + 9 both terminated at exactly 2 batches; cumulative 27), [[anthropic]] **20th consecutive silence (12-31), STRICT LOCK HOLDS** (Microsoft Cloud also absent for the 9th batch running 23-31; cumulative 8/0 copy), [[eden]] (TryEden) **18th consecutive silence (14-31); cumulative 1**. Cumulative **131 Hims / 84 OpenAI / 8 Anthropic / 27 Ro / 1 Eden**.
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, batch-31, clean-1-day-gap, signal-rate-50, openai-returns, openai-reverts-catalog-only, cluster-2-re-surface, o3-refire-single, o3-refire-no-continuation, openai-narrative-ad-experiments, widest-lab-delta, lab-delta-crosses-10x, hims-silent, hims-2nd-silence, ro-run-10-ends, ro-single-batch-run, two-batch-run-hypothesis-broken, anthropic-20th-silence, anthropic-strict-lock-holds, microsoft-cloud-absent, ai-lab-field-openai-only, eden-18th-silence, bmj-ophthalmology-noise, academic-publisher-noise, non-substring-noise, ai-lab-adjacent-noise, lab-paid-social-divergence]
sources: 1
source_path: raw/ads/digest-2026-07-05.md
source_date: 2026-07
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-07-05
updated: 2026-07-05
---

# FB Ads Digest — 2026-07-05

Thirty-first batch from the [[competitor-ads-farm]]. **2 new ads, 188 dedup-skipped** out of 190 fetched (**98.9% dedup**) at a **clean 1-day gap** from batch 30 (2026-07-04). Apify `facebook-ads-library-scraper` actor. **1 of 2 new ads is tracked-brand signal (50%)** — a lone [[openai]] catalog placeholder; the other is a genuinely new noise category (an academic medical-journal publisher).

## TL;DR

- **[[openai]] RETURNS from the batch-30 silence with 1 catalog placeholder — REVERTS to catalog-only.** Carousel, ID `964016993098345`, started **2026-05-08**, headline `{{product.name}}` / body `{{product.brand}}` — a **Cluster-2-window (Apr 30 – May 8) re-surface** via the catalog feed (the ~8-week-old window still emitting previously-unseen ads, the batch-25/28 shape). No new copy ad. Cumulative **84 ads, still 4 with copy — 3 distinct creatives** (80/84 = 95% placeholder); lab-delta vs Anthropic 84/8 (~**10.5x — new widest in the farm**).
- **The batch-29 verbatim o3 Deep Research re-fire gets NO continuation — 2 clean batches without recurrence lean it toward a single re-fire.** Batch 29 re-launched the o3 / Boston Children's + Harvard narrative verbatim under a new ad ID (the farm's first-ever copy-ad re-fire); batches 30 (silent) + 31 (catalog-only, no copy) add no sibling or repeat, so the re-fire looks like a **single re-fire** — the batch-9 Codex / batch-21 o3 / batch-27 ChatGPT one-off shape — rather than a sustained campaign. Per the "**no creative is closed, only dormant**" rule that broke the batch-24 one-off call in batch 29, this stays **provisional / dormant-not-closed**. → [[openai-narrative-ad-experiments]].
- **[[ro]] SILENT — Run 10 ENDS after a SINGLE batch (batch 30 only) — the FIRST single-batch Run in the farm.** Batch 30's lone Ro placeholder (Run 10) does not continue into batch 31, so Run 10 = 1 batch. This **breaks the emerging "2-batch run" hypothesis** — Runs 8 (batches 21+22) and 9 (batches 26+27) had both terminated at exactly 2 batches, and batch 30's page flagged "does Run 10 continue into a 2nd consecutive active batch?" as the open question. Answer: **no** — Ro's burst lengths are irregular (1–3 batches), not a fixed 2. Back in the burst→trough cadence. Cumulative **27 ads, ALL placeholder-only**.
- **[[hims]] SILENT — 2nd consecutive (30+31).** After batch 29's two-wedge return (the new Generic-Viagra Sex Rx SKU + a Hair Hybrids verbatim re-launch), Hims ships nothing for the 2nd batch running (30+31). No wedge/SKU has ever retired across 31 batches (all dormant-not-closed). → [[dtc-telehealth-ad-template]], [[compounded-drug-disclaimer]] (no new template/disclaimer data this batch). Cumulative **131 ads**.
- **[[anthropic]] 20th consecutive silence (12-31) on its own page — STRICT LOCK HOLDS.** No new Anthropic-page ad; the 2026-05-11 cluster stays confirmed-stalled at 2 (locked in batch 20). **Microsoft Cloud also absent for the 9th batch running (23-31)** — the batches-21+22 sustained Microsoft AI campaign stays closed at 2, and the AI-lab paid-social field is OpenAI-only. Cumulative **8 ads, 0 with copy** — 100% placeholder across 31 batches; lab-delta vs OpenAI 8/84 (~10.5x).
- **[[eden]] (TryEden) 18th consecutive silence (14-31).** No new TryEden ad. Cumulative **1 Eden ad, placeholder-only**.
- **1 noise ad (50%) — a genuinely new category.** **Ophthalmology at BMJ Group** (image, ID `1486005956228016`, started 2026-04-30) runs *"Innovations in Ophthalmology: Integrating AI, Imaging, and Omics — Read the published articles in BMJ Open Ophthalmology"* — a topic-collection promo from the medical-journal publisher **BMJ Group**. The farm's **first academic / medical-journal-publisher noise page**, and a **non-substring** result (no tracked-brand substring at all) — surfaced via the AI-lab search adjacency, the same mechanism as Microsoft Cloud's AI-lab-adjacent noise (and Adobe Acrobat / Romance miniseries earlier). Notably it is a *legitimate AI-in-medicine credibility* ad, the structural opposite of the DTC substring-noise corpus.

## Source

- Path: `raw/ads/digest-2026-07-05.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 190 • New: 2 • Dedup-skipped: 188 (98.9%)
- Gap from prior batch: **1 day** (batch 30 = 2026-07-04)

## Tracked-brand creative inventory

### [[openai]] — 1 new ad (returns from silence, catalog-only)

- **1 carousel placeholder** — ID `964016993098345`, started **2026-05-08**, headline `{{product.name}}` / body `{{product.brand}}`. A **Cluster-2-window (Apr 30 – May 8) re-surface** — the ~8-week-old window still emitting previously-unseen ads via the catalog feed (the batch-25/28 re-surface shape). RETURNS from the batch-30 silence; reverts to catalog-only. No new copy ad — the batch-29 o3 re-fire gets no continuation (see TL;DR). Cumulative **84 ads, 4 with copy — 3 distinct creatives** (80/84 = 95% placeholder).

### All other tracked brands — 0 new ads

- **[[ro]]** — silent; **Run 10 ends after a single batch (batch 30 only)** — the first single-batch Run in the farm, breaking the "2-batch run" hypothesis (Runs 8 + 9 both = 2 batches). Cumulative **27 ads**.
- **[[hims]]** — silent; 2nd consecutive (30+31; 29→30→31 reads two-wedge return → silence → silence). Cumulative **131 ads**.
- **[[anthropic]]** — silent; 20th consecutive (12-31); strict lock holds; Microsoft Cloud absent for the 9th batch running (23-31). Cumulative **8 ads, 0 with copy**.
- **[[eden]]** (TryEden) — silent; 18th consecutive (14-31). Cumulative **1 ad, placeholder**.
- **[[henry-meds]]** — never appeared (31st consecutive batch).
- **[[hampton-founders]]** — 0 new since 2026-05-06.
- **DealMachine** — never appeared (31st consecutive batch).

## "Noise" inventory — 1 of 2 ads (50%)

- **Ophthalmology at BMJ Group** (image, ID `1486005956228016`, started 2026-04-30) — *"'Innovations in Ophthalmology: Integrating AI, Imaging, and Omics' — Read the published articles in BMJ Open Ophthalmology."* A topic-collection promo from **BMJ Group**, the UK medical-journal publisher. **First academic / medical-journal-publisher noise page in the farm**, and a **non-substring** match (contains none of the 8 tracked brand names) — the third confirmed non-substring adjacent-noise category after Adobe Acrobat (batch 3) and Romance miniseries (batch 4), and the first that is explicitly **AI-themed**, surfaced via the AI-lab search adjacency exactly like Microsoft Cloud. Not a DTC advertiser — a high-trust B2B/academic credibility ad, the structural opposite of the DTC substring-noise corpus (Uproot Clean / Aelfric Eden / Rosabella / etc.).

## Cross-cutting patterns

### Ro run lengths — the "2-batch run" hypothesis breaks

| Run | Batches | Length | Terminated by |
|---|---|---|---|
| 8 | 21–22 | 2 | batch 23 silence |
| 9 | 26–27 | 2 | batch 28 silence |
| **10** | **30** | **1** | **batch 31 silence** |

Batch 28's page floated an emerging "2-batch run" length (Runs 8 + 9 both terminated at exactly 2 consecutive active batches), and batch 30's page carried "does Run 10 continue into batch 31?" as its open question. Batch 31's Ro silence **resolves it: no** — Run 10 is a single batch, so Ro's burst lengths are **irregular (1–3 batches), not a fixed 2**. The catalog-feed cadence is bursty and un-periodic; the "2-batch run" was a two-point coincidence.

### OpenAI's copy ads — four one-offs, one re-fire, still no sustained narrative campaign

| # | Batch | Product surface | Motion | Recurrence |
|---|---|---|---|---|
| 1 | 9 (05-22) | Codex | product-trial one-liner | never |
| 2 | 21 (06-24) | o3 Deep Research | scientific-credibility | re-fired verbatim batch 29 |
| 3 | 27 (07-01) | ChatGPT (SMB) | customer testimonial | never |
| — | 29 (07-03) | o3 Deep Research | **verbatim re-fire** of #2 | no continuation (30 + 31) |

Across 31 batches OpenAI runs a persistent catalog-placeholder base (80 of 84 ads) with **sporadic single-shot narrative experiments across different product surfaces / personas**, none yet sustained into a multi-ad campaign. The batch-29 o3 re-fire — the farm's only copy-ad recurrence — shows **no continuation across batches 30 + 31**, so even the re-fire reads as a single event (dormant-not-closed). → [[openai-narrative-ad-experiments]].

### Thirty-one-batch convergence (recent batches)

| Batch | Date | Fetched | New | Dedup | New % | OpenAI | Hims | Anthropic | Ro | Eden | Signal % |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 27 | 2026-07-01 | 183 | 10 | 173 | 5.5% | 1 | 2 | 0 | 2 | 0 | 50% |
| 28 | 2026-07-02 | 191 | 5 | 186 | 2.6% | 4 | 0 | 0 | 0 | 0 | 80% |
| 29 | 2026-07-03 | 183 | 7 | 176 | 3.8% | 2 | 3 | 0 | 0 | 0 | 71.4% |
| 30 | 2026-07-04 | 186 | 1 | 185 | 0.5% | 0 | 0 | 0 | 1 | 0 | 100% |
| **31** | **2026-07-05** | **190** | **2** | **188** | **1.1%** | **1** | **0** | **0** | **0** | **0** | **50%** |

(Full table in [[ads-digest-2026-06-09]] / [[ads-digest-2026-06-24]].) Batch 31's lone signal ad is one OpenAI catalog re-surface; the other new ad is the first academic-publisher noise page.

### What did NOT happen this batch

- **No new OpenAI copy ad** — the batch-29 o3 re-fire gets no continuation across batches 30 + 31 (single-re-fire reading strengthens, but dormant-not-closed).
- **No new Hims wedge/SKU data** — the batch-29 Generic-Viagra Sex Rx SKU and Hair Hybrids trough both silent for the 2nd batch running; no template or disclaimer diff-target shipped.
- **No new Microsoft Cloud creative** — absent for the 9th batch running (23-31); the batches-21+22 campaign stays closed at 2.
- **No Ro continuation** — Run 10 ends at a single batch (breaks the "2-batch run" hypothesis).

## Open questions

- **Is the batch-29 o3 re-fire a single re-fire or a slow-repeating flight?** Batches 30 + 31 add no recurrence — leaning single-re-fire, but the batch-29 precedent means any future recurrence is possible (dormant-not-closed) → [[openai-narrative-ad-experiments]].
- **When does Ro's next run (Run 11) fire, and how long?** Run 10 was a single batch; with irregular 1–3-batch bursts and ~1–3-batch troughs, the next burst timing is now the only Ro signal to watch.
- **Is Anthropic's own-page silence permanent or pre-launch?** 20 consecutive batches; any future ad = a new launch window.
- **Does the BMJ / academic-publisher AI-adjacent noise recur, or is it a one-off adjacency artifact?** First academic-journal publisher in the farm's noise corpus.

## Related

- [[competitor-ads-farm]] — thirty-first batch; clean 1-day gap; 2 new ads, 50% signal; OpenAI returns from silence with 1 catalog re-surface (reverts to catalog-only); o3 re-fire gets no continuation (leans single re-fire); Ro Run 10 ends at a single batch (breaks the 2-batch-run hypothesis); Hims 2nd silence; Anthropic 20th silence (strict lock holds); Microsoft Cloud absent 9th batch running; first academic-publisher noise page (BMJ Group ophthalmology)
- [[openai]] — 1 catalog placeholder (Cluster-2 re-surface, started 2026-05-08); returns from batch-30 silence, catalog-only; o3 re-fire gets no continuation; cumulative 84 ads, 4 with copy
- [[openai-narrative-ad-experiments]] — the four narrative copy ads (Codex / o3 / ChatGPT / o3 re-fire) atop OpenAI's catalog base; the re-fire gets no continuation across batches 30 + 31
- [[ro]] — silent; Run 10 ends at a single batch (first single-batch Run; breaks the 2-batch-run hypothesis); cumulative 27 ads, all placeholder
- [[hims]] — silent, 2nd consecutive (30+31); cumulative 131 ads
- [[anthropic]] — 0 new ads; 20th consecutive silence (12-31); strict lock holds; Microsoft Cloud absent 9th batch running; cumulative 8 ads
- [[eden]] — TryEden 18th consecutive silence (14-31); cumulative 1 Eden ad
- [[ads-digest-2026-07-04]] — thirtieth batch (the predecessor: the thinnest signal-bearing batch, Ro Run 10 opens, OpenAI silent)

## Appears in

- Thirty-first entry in `wiki/sources/` for the competitor-ads farm. **2 new ads, 50% tracked-brand signal** at a clean 1-day gap (98.9% dedup). The lone signal ad is a **[[openai]] catalog placeholder** (carousel, ID `964016993098345`, started 2026-05-08 — a Cluster-2-window re-surface) — **OpenAI returns from batch-30 silence and reverts to catalog-only**; the batch-29 verbatim o3 Deep Research re-fire gets **no continuation** across batches 30 + 31 (leans single re-fire, dormant-not-closed). The 1 noise ad is the farm's **first academic/medical-journal-publisher page** — **Ophthalmology at BMJ Group** (AI-in-medicine topic collection, non-substring AI-lab-adjacent). **All 7 other tracked brands silent** — [[hims]] 2nd-consecutive silence, [[ro]] silent with **Run 10 ending at a single batch (breaks the 2-batch-run hypothesis)**, [[anthropic]] 20th consecutive silence (strict lock holds; Microsoft Cloud absent 9th batch running), [[eden]] 18th consecutive silence. Cumulative **131 Hims / 84 OpenAI / 8 Anthropic / 27 Ro / 1 Eden**.
