---
title: FB Ads Digest — Competitor brands — 2026-07-06
category: source
summary: Thirty-second competitor-ads farm batch — **8 new FB Ad Library entries** (190 fetched, 182 dedup-skipped = 95.8% dedup) at a **clean 1-day gap** from batch 31 (2026-07-05); **7 of 8 tracked-brand signal (87.5%)** — a **three-tracked-brand-active REBOUND (Hims + OpenAI + Ro)**, the FIRST 3-brand-active batch since batch 27 (2026-07-01) and the largest new-ad batch since batch 27, inverting the thin batches 30 (1 ad) + 31 (2 ads). **THE HEADLINE — [[hims]] RETURNS from the 2-batch silence (30+31) with 2 Wegovy GLP-1 verbatim ads — the Wegovy wave REOPENS after 9 dormant batches** (last shipped batch 22, 2026-06-25; IDs `1696425734973229` started **2026-07-02** — among the freshest Hims start dates in the farm, 4 days pre-fetch — + `1553105592929442` started 2026-06-26; both verbatim the canonical branded-Wegovy template + $149/mo-medication + $39/$149 membership footnote + Novo-Nordisk non-affiliation). It is a **Wegovy-ONLY return** (no Hair Hybrids, no Sex Rx) — BREAKING the batch-20/24/26/27 pattern where Hims returned from silence with Hair-Hybrids-only; the wedge mix rotates and Wegovy's 9-batch dormancy (23-31) is the 2nd-longest wedge dormancy in the farm after Hard Mints' 19-batch record (dormant-not-closed) → [[dtc-telehealth-ad-template]], [[compounded-drug-disclaimer]]. **[[openai]] ships 3 catalog placeholders** (carousel `{{product.name}}`/`{{product.brand}}`, June-window re-surfaces started 2026-06-10 + 2026-06-25 ×2) — no new copy ad, so the batch-29 verbatim o3 Deep Research re-fire gets NO continuation for the 3rd clean batch running (30+31+32), further leaning it toward a single re-fire → [[openai-narrative-ad-experiments]]; cumulative **87 ads, still 4 with copy — 3 distinct creatives** (83/87 = 95% placeholder); lab-delta vs Anthropic 87/8 (~**10.9x — new widest in the farm**). **[[ro]] RETURNS — Run 11, 2 placeholders** (IDs `1038345515301469` started 2026-06-20 + `1311245460513025` started 2026-06-01, both `{{product.brand}}`) after Run 10's single batch (30) + batch-31 silence; still catalog-only, zero static narrative across 32 batches (cumulative 29). **[[anthropic]] 21st consecutive silence (12-32), STRICT LOCK HOLDS** (Microsoft Cloud absent 10th batch running 23-32; cumulative 8, 0 with copy). **[[eden]] (TryEden) 19th consecutive silence (14-32)** (cumulative 1). **1 noise ad (12.5%) — Uproot Clean July 4th "Buy 2 Get 2 Free" BOGO** ("Ro" inside "Up**ro**ot", ~10th appearance — the most-recurring noise page in the farm), its long-form-DR pet-odor/3-enzyme BOGO variant (batches 2+4 shape) not the batch-25 washer-cleaner/NASA SKU. Cumulative **133 Hims / 87 OpenAI / 8 Anthropic / 29 Ro / 1 Eden**.
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, batch-32, clean-1-day-gap, signal-rate-87, three-brand-active, three-brand-rebound, first-three-brand-since-batch-27, hims-returns, hims-wegovy-reopens, wegovy-only-return, wegovy-9-batch-dormancy, wedge-mix-rotates, dormant-not-closed, dtc-telehealth-ad-template, compounded-drug-disclaimer, wegovy-disclaimer-reopens, openai-catalog-only, openai-june-window-resurface, o3-refire-no-continuation, o3-refire-single, openai-narrative-ad-experiments, widest-lab-delta, lab-delta-10-9x, ro-returns, ro-run-11, ro-placeholder-only, anthropic-21st-silence, anthropic-strict-lock-holds, microsoft-cloud-absent, ai-lab-field-openai-only, eden-19th-silence, uproot-clean-returns, most-recurring-noise-page, uproot-july4-bogo, ro-substring-noise, holiday-creative]
sources: 1
source_path: raw/ads/digest-2026-07-06.md
source_date: 2026-07
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-07-06
updated: 2026-07-06
---

# FB Ads Digest — 2026-07-06

Thirty-second batch from the [[competitor-ads-farm]]. **8 new ads, 182 dedup-skipped** out of 190 fetched (**95.8% dedup**) at a **clean 1-day gap** from batch 31 (2026-07-05). Apify `facebook-ads-library-scraper` actor. **7 of 8 new ads are tracked-brand signal (87.5%)** — a **three-tracked-brand-active rebound** (Hims ×2 + OpenAI ×3 + Ro ×2); the lone noise ad is the farm's most-recurring noise page returning with a July-4th holiday creative.

## TL;DR

- **Three-tracked-brand-active REBOUND (Hims + OpenAI + Ro) — the first 3-brand-active batch since batch 27 (2026-07-01), and the largest new-ad batch since batch 27.** After batch 30 (1 ad, Ro-only) and batch 31 (2 ads, OpenAI-only + noise), batch 32 pops back to 8 ads / 87.5% signal with three tracked brands live simultaneously — the batch-26/27 three-brand shape (Hims + OpenAI + Ro) repeats. Not a structural surge, just the daily surge-trough oscillation swinging back up (the thin batches 30+31 were the trough).
- **[[hims]] RETURNS from the 2-batch silence (30+31) with 2 Wegovy GLP-1 verbatim ads — the Wegovy wave REOPENS after 9 dormant batches.** IDs `1696425734973229` started **2026-07-02** (among the freshest Hims start dates in the farm — 4 days pre-fetch) + `1553105592929442` started 2026-06-26; both verbatim the canonical branded-Wegovy template (*"Get Wegovy® with Hims, plus access to provider-led care… ✅ FDA-approved GLP-1 pill and pens available ✅ Medication as low as $149/mo—membership fee of $39 for first month, $149 thereafter ✅ 100% online. Your goals. Your plan. Your pace."*) with the expanded $149/mo-medication + $39/$149 membership pricing footnote + Novo-Nordisk non-affiliation clause. **Wegovy last shipped in batch 22 (2026-06-25)** — batches 23-31 were Hims-silent or Hair-Hybrids-only, so this is a **9-batch Wegovy dormancy** (2nd-longest wedge dormancy in the farm after Hard Mints' 19-batch record). It is a **Wegovy-ONLY return** — no Hair Hybrids, no Sex Rx — BREAKING the batch-20/24/26/27 "return from silence = Hair-Hybrids-only" pattern; the wedge mix rotates day-to-day and no wedge is guaranteed. Dormant-not-closed reaffirmed on the Wegovy wedge. → [[dtc-telehealth-ad-template]], [[compounded-drug-disclaimer]]. Cumulative **133 ads**.
- **[[openai]] ships 3 catalog placeholders — reverts/continues catalog-only; no new copy ad.** Carousels `{{product.name}}`/`{{product.brand}}`, June-window re-surfaces: ID `3876811359280748` started 2026-06-10 + IDs `2428506124326865` + `1302434362036427` both started 2026-06-25 (the 2026-06-25 window opened batch 26; 2026-06-10 is an established June window). No new launch window and no new narrative — so the **batch-29 verbatim o3 Deep Research re-fire gets NO continuation for the 3rd clean batch running (30 silent + 31 catalog-only + 32 catalog-only)**, further leaning it toward a **single re-fire** (the batch-9/21/27 one-off shape), but dormant-not-closed per the rule that broke in batch 29 → [[openai-narrative-ad-experiments]]. Cumulative **87 ads, still 4 with copy — 3 distinct creatives** (83/87 = 95% placeholder); lab-delta vs Anthropic 87/8 (~**10.9x — new widest in the farm**).
- **[[ro]] RETURNS — Run 11, 2 placeholders.** IDs `1038345515301469` started 2026-06-20 + `1311245460513025` started 2026-06-01, both `{{product.brand}}`. After Run 10 was a single batch (batch 30) and batch 31 was Ro-silent, Run 11 fires at batch 32 with 2 ads — the burst→trough→burst cadence continues (Ro's burst lengths remain irregular, 1-3 batches). Still catalog-driven dynamic creative only, **zero static narrative across 32 batches**. Cumulative **29 ads, ALL placeholder-only**.
- **[[anthropic]] 21st consecutive silence (12-32) on its own page — STRICT LOCK HOLDS.** No new Anthropic-page ad; the 2026-05-11 cluster stays confirmed-stalled at 2 (locked in batch 20). **Microsoft Cloud also absent for the 10th batch running (23-32)** — the batches-21+22 Microsoft AI campaign stays closed at 2, and the AI-lab paid-social field is OpenAI-only. Cumulative **8 ads, 0 with copy** — 100% placeholder across 32 batches; lab-delta vs OpenAI 8/87 (~10.9x).
- **[[eden]] (TryEden) 19th consecutive silence (14-32).** No new TryEden ad. Cumulative **1 Eden ad, placeholder-only**.
- **1 noise ad (12.5%) — Uproot Clean returns with a July-4th holiday creative.** **🇺🇸 July 4th Sale Is Live! — Buy 2 Get 2 Free + Free Gifts** (video, ID `1039332318426591`, started 2026-06-27): *"That smell coming off your 'clean' laundry? It's not your clothes. It's your washing machine… Our 3-enzyme formula dissolves it. One tablet every two weeks… 60 days to try it."* "Ro" inside "Up**ro**ot" — the **most-recurring noise page in the farm** (~10th appearance: batches 2/4/5/8/16/19/21/22/25 + 32). This is its **long-form-DR pet-odor / 3-enzyme BOGO variant** (the batches 2+4 shape), not the batch-25 washer-cleaner / NASA-enzyme SKU — and a timely holiday-sale creative.

## Source

- Path: `raw/ads/digest-2026-07-06.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 190 • New: 8 • Dedup-skipped: 182 (95.8%)
- Gap from prior batch: **1 day** (batch 31 = 2026-07-05)

## Tracked-brand creative inventory

### [[hims]] — 2 new ads (Wegovy wave REOPENS, Wegovy-only)

- **2 Wegovy GLP-1 verbatim copy ads** — IDs `1696425734973229` (started **2026-07-02**) + `1553105592929442` (started 2026-06-26), both format unknown, **identical verbatim copy**: the canonical branded-Wegovy skeleton (*"Get Wegovy® with Hims…"* + three ✅ bullets: FDA-approved GLP-1 pill & pens / medication as low as $149/mo + $39 first-month / $149 membership / 100% online + *"Your goals. Your plan. Your pace. See if you qualify today."*) followed by the expanded pricing footnote and the Novo-Nordisk trademark non-affiliation clause. **Wegovy REOPENS after 9 dormant batches** (last shipped batch 22, 2026-06-25). **Wegovy-only return** — Hair Hybrids + Sex Rx + Hard Mints all silent — breaking the batch-20/24/26/27 Hair-Hybrids-only return pattern. The 2026-07-02 start date is among the freshest Hims ad-launch dates in the farm (4 days pre-fetch). Dormant-not-closed on the Wegovy wedge. Cumulative **133 ads**.

### [[openai]] — 3 new ads (catalog-only)

- **3 carousel placeholders** — ID `3876811359280748` (started 2026-06-10) + IDs `2428506124326865` + `1302434362036427` (both started 2026-06-25), all headline `{{product.name}}` / body `{{product.brand}}`. June-window re-surfaces via the catalog feed (the 2026-06-25 window opened batch 26; 2026-06-10 is an established June window). No new launch window; no new copy ad — the batch-29 o3 re-fire gets no continuation for the 3rd clean batch running (see TL;DR). Cumulative **87 ads, 4 with copy — 3 distinct creatives** (83/87 = 95% placeholder).

### [[ro]] — 2 new ads (Run 11)

- **2 placeholders** — IDs `1038345515301469` (started 2026-06-20) + `1311245460513025` (started 2026-06-01), both body `{{product.brand}}`. Returns from the batch-31 silence — **Run 11** in Ro's irregular-burst cadence (Run 10 was the single batch 30; batch 31 silent; Run 11 = batch 32). Still catalog-only; zero static narrative across 32 batches. Cumulative **29 ads**.

### All other tracked brands — 0 new ads

- **[[anthropic]]** — silent; 21st consecutive (12-32); strict lock holds; Microsoft Cloud absent for the 10th batch running (23-32). Cumulative **8 ads, 0 with copy**.
- **[[eden]]** (TryEden) — silent; 19th consecutive (14-32). Cumulative **1 ad, placeholder**.
- **[[henry-meds]]** — never appeared (32nd consecutive batch).
- **[[hampton-founders]]** — 0 new since 2026-05-06.
- **DealMachine** — never appeared (32nd consecutive batch).

## "Noise" inventory — 1 of 8 ads (12.5%)

- **Uproot Clean** — washing-machine-cleaner DTC, video (ID `1039332318426591`, started 2026-06-27). July-4th holiday BOGO: *"🇺🇸 July 4th Sale Is Live! — And Your Washer Has Been Waiting For This. Buy 2 Get 2 FREE + Free Gifts. That smell coming off your 'clean' laundry? It's not your clothes. It's your washing machine. Pet oils and dander coat the drum and seal, feeding bacteria that survive every cycle… Our 3-enzyme formula dissolves it. One tablet every two weeks… 60 days to try it. Money back if it doesn't work."* CTA → `uprootclean.com/products/uproot-washing-machine-cleaner-pro`. "Ro" inside "Up**ro**ot" — the **most-recurring noise page in the farm** (~10th appearance across batches 2/4/5/8/16/19/21/22/25/32). This is its **long-form-DR pet-odor / 3-enzyme BOGO variant** (batches 2+4 shape), distinct from the batch-25 washer-cleaner / NASA-enzyme SKU — timed to the July-4th holiday.

## Cross-cutting patterns

### Hims wedge rotation — Wegovy-only return breaks the Hair-Hybrids-only pattern

Since batch 20, every Hims "return from silence" batch had shipped **Hair-Hybrids-only** copy (batches 20, 24, 26, 27), reinforcing Hair Hybrids as the standing trough-wedge. Batch 32 **inverts that**: Hims returns from the 30+31 silence with **Wegovy-only** copy (Hair Hybrids silent). Combined with the batch-18/22 lesson (wedge mix rotates day-to-day, no wedge guaranteed even at 1-day resolution), this confirms there is **no fixed "default return wedge"** — the return-wedge is itself part of the rotation. Wegovy's 9-batch dormancy (23-31) is the 2nd-longest wedge dormancy in the farm after Hard Mints' 19-batch record — another strong dormant-not-closed datapoint; no Hims wedge or SKU has retired across 32 batches.

### OpenAI's copy ads — four one-offs, one re-fire, still no continuation

| # | Batch | Product surface | Motion | Recurrence |
|---|---|---|---|---|
| 1 | 9 (05-22) | Codex | product-trial one-liner | never |
| 2 | 21 (06-24) | o3 Deep Research | scientific-credibility | re-fired verbatim batch 29 |
| 3 | 27 (07-01) | ChatGPT (SMB) | customer testimonial | never |
| — | 29 (07-03) | o3 Deep Research | **verbatim re-fire** of #2 | no continuation (30 + 31 + 32) |

Across 32 batches OpenAI runs a persistent catalog-placeholder base (83 of 87 ads = 95%) with **sporadic single-shot narrative experiments across different product surfaces / personas**, none yet sustained. The batch-29 o3 re-fire — the farm's only copy-ad recurrence — now shows **no continuation across batches 30 + 31 + 32** (3 clean batches), so the single-re-fire reading strengthens (dormant-not-closed). → [[openai-narrative-ad-experiments]].

### Thirty-two-batch convergence (recent batches)

| Batch | Date | Fetched | New | Dedup | New % | OpenAI | Hims | Anthropic | Ro | Eden | Signal % |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 28 | 2026-07-02 | 191 | 5 | 186 | 2.6% | 4 | 0 | 0 | 0 | 0 | 80% |
| 29 | 2026-07-03 | 183 | 7 | 176 | 3.8% | 2 | 3 | 0 | 0 | 0 | 71.4% |
| 30 | 2026-07-04 | 186 | 1 | 185 | 0.5% | 0 | 0 | 0 | 1 | 0 | 100% |
| 31 | 2026-07-05 | 190 | 2 | 188 | 1.1% | 1 | 0 | 0 | 0 | 0 | 50% |
| **32** | **2026-07-06** | **190** | **8** | **182** | **4.2%** | **3** | **2** | **0** | **2** | **0** | **87.5%** |

(Full table in [[ads-digest-2026-06-09]] / [[ads-digest-2026-06-24]].) Batch 32 is the largest and highest-signal batch since batch 27 — a three-brand rebound (Hims + OpenAI + Ro) out of the batch-30/31 thin trough.

### What did NOT happen this batch

- **No new OpenAI copy ad** — the batch-29 o3 re-fire gets no continuation for the 3rd clean batch running (30+31+32); single-re-fire reading strengthens (dormant-not-closed).
- **No new Hims Hair Hybrids / Sex Rx / Hard Mints data** — the return is Wegovy-only; Hair Hybrids (the usual return-wedge), Sex Rx, and Hard Mints all silent, all dormant-not-closed.
- **No new OpenAI launch window** — the 3 placeholders are all June-window (06-10 / 06-25) re-surfaces.
- **No new Microsoft Cloud creative** — absent for the 10th batch running (23-32); the batches-21+22 campaign stays closed at 2.
- **No disclaimer edit** — the Wegovy/Novo-Nordisk block ships verbatim after its dormancy; the boilerplate is still never edited, only its shipping cadence rotates.

## Open questions

- **Does the Wegovy wave continue into batch 33 (sustained flight) or drop back to trough (single-batch re-fire)?** Wegovy re-opened after 9 dormant batches; a batch-33 Wegovy ad would confirm a flight, silence would mark it a single re-surface day.
- **Is the batch-29 o3 re-fire a single re-fire or a slow-repeating flight?** Batches 30 + 31 + 32 add no recurrence — leaning single-re-fire, but dormant-not-closed → [[openai-narrative-ad-experiments]].
- **How long is Ro's Run 11?** Run 10 was a single batch; Runs 8 + 9 were 2 batches each — Ro's burst lengths are irregular (1-3), so batch 33 tests whether Run 11 extends or ends at 1.
- **Is Anthropic's own-page silence permanent or pre-launch?** 21 consecutive batches; any future ad = a new launch window.

## Related

- [[competitor-ads-farm]] — thirty-second batch; clean 1-day gap; 8 new ads, 87.5% signal; three-brand rebound (Hims + OpenAI + Ro), first since batch 27; Hims Wegovy wave REOPENS after 9 dormant batches (Wegovy-only return breaks the Hair-Hybrids-only pattern); OpenAI 3 catalog placeholders (o3 re-fire no continuation, 3rd clean batch); Ro Run 11; Anthropic 21st silence (strict lock holds); Microsoft Cloud absent 10th batch running; Uproot Clean July-4th BOGO (~10th appearance)
- [[hims]] — 2 Wegovy GLP-1 verbatim ads; Wegovy REOPENS after 9 dormant batches; Wegovy-only return; cumulative 133 ads
- [[dtc-telehealth-ad-template]] — the canonical Wegovy GLP-1 verbatim template ships again (Wegovy-only), verbatim after 9-batch dormancy
- [[compounded-drug-disclaimer]] — the Wegovy/Novo-Nordisk disclaimer + pricing footnote reopens verbatim after dormancy since batch 22
- [[openai]] — 3 catalog placeholders (June-window re-surfaces); o3 re-fire no continuation (3rd clean batch); cumulative 87 ads, 4 with copy; lab-delta ~10.9x
- [[openai-narrative-ad-experiments]] — the four narrative copy ads (Codex / o3 / ChatGPT / o3 re-fire); the re-fire gets no continuation across batches 30 + 31 + 32
- [[ro]] — 2 placeholders, Run 11; cumulative 29 ads, all placeholder
- [[anthropic]] — 0 new ads; 21st consecutive silence (12-32); strict lock holds; Microsoft Cloud absent 10th batch running; cumulative 8 ads
- [[eden]] — TryEden 19th consecutive silence (14-32); cumulative 1 Eden ad
- [[ads-digest-2026-07-05]] — thirty-first batch (the predecessor: OpenAI returns catalog-only, o3 re-fire no continuation, Ro Run 10 ends at a single batch, first BMJ academic-publisher noise)

## Appears in

- Thirty-second entry in `wiki/sources/` for the competitor-ads farm. **8 new ads, 87.5% tracked-brand signal** at a clean 1-day gap (95.8% dedup) — a **three-tracked-brand-active rebound** (Hims ×2 + OpenAI ×3 + Ro ×2), the first 3-brand-active batch since batch 27 and the largest batch since batch 27, inverting the thin batches 30 + 31. **THE HEADLINE — [[hims]] Wegovy GLP-1 verbatim wave REOPENS after 9 dormant batches** (2 ads, IDs `1696425734973229` started 2026-07-02 + `1553105592929442` started 2026-06-26) in a **Wegovy-ONLY return** that breaks the batch-20/24/26/27 Hair-Hybrids-only return pattern (wedge mix rotates; Wegovy's 9-batch dormancy 2nd-longest after Hard Mints' 19). **[[openai]] 3 catalog placeholders** (June-window re-surfaces; no new copy ad — o3 re-fire no continuation for the 3rd clean batch 30+31+32; cumulative 87 ads, 4 with copy, lab-delta ~10.9x). **[[ro]] Run 11, 2 placeholders** (cumulative 29). **[[anthropic]] 21st consecutive silence** (strict lock holds; Microsoft Cloud absent 10th batch running). **[[eden]] 19th consecutive silence.** 1 noise ad — **Uproot Clean July-4th BOGO** (~10th appearance, most-recurring noise page). Cumulative **133 Hims / 87 OpenAI / 8 Anthropic / 29 Ro / 1 Eden**.
</content>
</invoke>
