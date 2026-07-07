---
title: FB Ads Digest — Competitor brands — 2026-07-07
category: source
summary: Thirty-third competitor-ads farm batch — **6 new FB Ad Library entries** (197 fetched, 191 dedup-skipped = 97.0% dedup) at a **clean 1-day gap** from batch 32 (2026-07-06); **only 2 of 6 tracked-brand signal (33.3%)** — the batch-32 three-brand rebound (Hims + OpenAI + Ro) does NOT sustain; batch 33 falls back to a **collision-heavy, catalog-only, ZERO-fresh-creative trough**. **THE HEADLINE — the farm surfaces its FIRST-EVER "Henry" brand-name collision: [[henry-meds]]'s search term matches "Dr. Henry Brown," a board-certified urologist running a long-form direct-response BPH/enlarged-prostate funnel** (2 ads, IDs `1507753507282847` carousel placeholder + `1339093435097279` image, both started 2026-07-06 — *"If you're taking Flomax or Tamsulosin… you're on a ticking clock… I'm Dr. Henry Brown. Board-certified urologist… 19 years… TURP, HoLEP…"* — urologist-authority + catheter/surgery fear + pharma-villain framing, the batch-8 Cholesterol-Support-Group / Lauren-Brooks long-form-DR shape). It is a **false positive** — [[henry-meds]] itself is still absent for the 33rd consecutive batch — and it confirms the batch-1 "brand-name filter too permissive" known issue on a NEW axis: "Henry" is as loose as "Ro"/"Eden"/"Hampton." **[[hims]] ships 1 catalog placeholder — the Wegovy wave does NOT sustain** (ID `966576545958808` started 2026-05-13, body `{{product.brand}}`, a ~2-month-old May-window re-surface, no copy); batch-32's Wegovy re-open reads as a **single-batch re-surface, dormant-not-closed** (batch-32 open question resolved). **[[openai]] ships 1 catalog placeholder** (carousel `{{product.name}}`/`{{product.brand}}`, ID `945993881573821` started 2026-05-08 — the oldest Cluster-2 / May-8 window re-surfacing) — **no new copy ad, so the batch-29 o3 Deep Research re-fire gets NO continuation for the 4th clean batch running (30+31+32+33)**, leaning further toward a single re-fire → [[openai-narrative-ad-experiments]]; cumulative **88 ads, still 4 with copy — 3 distinct creatives** (84/88 = 95.5% placeholder); lab-delta vs Anthropic 88/8 (**11.0x — new widest in the farm**). **[[ro]] SILENT — Run 11 ends at a single batch** (batch 32 only). **[[anthropic]] 22nd consecutive silence (12-33), STRICT LOCK HOLDS** (Microsoft Cloud absent 11th batch running 23-33). **[[eden]] (TryEden) 20th consecutive silence (14-33)**. **2 Hampton-substring noise pages — Hampton City Schools** (new first-fire; school-nurse recruitment) + **Hampton Roads Honda Dealers** (REPEAT, first fired batch 8). Cumulative **134 Hims / 88 OpenAI / 8 Anthropic / 29 Ro / 1 Eden**.
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, batch-33, clean-1-day-gap, signal-rate-33, low-signal-batch, rebound-does-not-sustain, catalog-only-signal, zero-fresh-creative, brand-name-collision, henry-collision-first, henry-brown-urologist, prostate-bph-ad, long-form-dr-medical, urologist-authority, pharma-villain-framing, henry-meds-still-absent, hampton-collision, hampton-city-schools, hampton-roads-honda-repeat, brand-filter-too-permissive, hims-placeholder-only, wegovy-does-not-sustain, wegovy-single-batch-resurface, dormant-not-closed, dtc-telehealth-ad-template, compounded-drug-disclaimer, openai-catalog-only, may-window-resurface, o3-refire-no-continuation-4th-batch, openai-narrative-ad-experiments, widest-lab-delta, lab-delta-11x, ro-silent, ro-run-11-single-batch, anthropic-22nd-silence, anthropic-strict-lock-holds, microsoft-cloud-absent, ai-lab-field-openai-only, eden-20th-silence]
sources: 1
source_path: raw/ads/digest-2026-07-07.md
source_date: 2026-07
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-07-07
updated: 2026-07-07
---

# FB Ads Digest — 2026-07-07

Thirty-third batch from the [[competitor-ads-farm]]. **6 new ads, 191 dedup-skipped** out of 197 fetched (**97.0% dedup**) at a **clean 1-day gap** from batch 32 (2026-07-06). Apify `facebook-ads-library-scraper` actor. **Only 2 of 6 new ads are tracked-brand signal (33.3%)** — both catalog placeholders re-surfacing old May windows (zero fresh tracked-brand creative). The other 4 ads (66.7%) are **brand-name-collision noise**, including the farm's **first-ever "Henry" false positive** (Dr. Henry Brown, urologist) — the sole substantive new creative in the batch belongs to a page that isn't a tracked competitor.

## TL;DR

- **The batch-32 three-brand rebound (Hims + OpenAI + Ro) does NOT sustain — batch 33 falls back to a low-signal, catalog-only, collision-heavy trough.** Signal drops 87.5% (batch 32) → 33.3% (batch 33). Volume is not thin (6 ads vs batches 30/31's 1/2), but the mix is collision-dominated: 2 tracked placeholders + 4 false-positive noise ads. **Zero fresh tracked-brand creative** — the freshest tracked ads are ~2-month-old May-window re-surfaces (Hims 2026-05-13, OpenAI 2026-05-08); the only NEW-dated creative in the whole batch (started 2026-07-06) is noise (Henry Brown).
- **THE HEADLINE — the farm's FIRST-EVER "Henry" brand-name collision: [[henry-meds]]'s search term matches "Dr. Henry Brown," a board-certified urologist.** 2 ads under the "Henry Brown" page (IDs `1507753507282847` carousel placeholder, started 2026-07-06 + `1339093435097279` image, started 2026-07-06). Ad 2 is a **long-form direct-response BPH / enlarged-prostate narrative**: *"If you're taking Flomax or Tamsulosin for your enlarged prostate, you're on a ticking clock — within a few years you'll rely on a catheter or need risky prostate surgery. I know this because I'm a urologist… I'm Dr. Henry Brown. Board-certified urologist… 19 years… Pharmaceutical companies have conditioned an entire generation of urologists… I perform prostate surgeries (TURP, HoLEP and more)…"* — **urologist-authority + catheter/surgery fear + pharma-villain framing**, the same long-form-DR shape as the batch-8 Cholesterol Support Group and Lauren Brooks pet-allergy specimens. This is a **false positive** ("Henry" prefix match, NOT the compounded-GLP-1 telehealth [[henry-meds]]) — the FIRST time the "Henry" term produced ANY match in 33 batches, and [[henry-meds]] itself is still absent for the 33rd consecutive batch. Confirms the batch-1 "brand-name filter too permissive" known issue on a **new axis** — "Henry" is as loose as "Ro"/"Eden"/"Hampton." → [[competitor-ads-farm]].
- **[[hims]] ships 1 catalog placeholder — the Wegovy wave does NOT sustain.** ID `966576545958808` (started **2026-05-13**), format unknown, body `{{product.brand}}` only — a ~2-month-old May-window re-surface, no copy. Batch 32's Wegovy GLP-1 verbatim wave (2 copy ads) gets **no batch-33 continuation** — so the batch-32 open question ("does Wegovy continue into batch 33 or drop back to trough?") resolves as **single-batch re-surface**: Wegovy re-opened for exactly one batch and is dormant again (dormant-not-closed, consistent with its 9-batch prior dormancy). Cumulative **134 ads**.
- **[[openai]] ships 1 catalog placeholder — catalog-only; no new copy ad.** Carousel `{{product.name}}` / `{{product.brand}}`, ID `945993881573821` (started **2026-05-08**) — the oldest **Cluster-2 / May-8 window** re-surfacing via the catalog feed (older than batch 32's June-window placeholders). No new launch window; no new narrative — the **batch-29 o3 Deep Research re-fire gets NO continuation for the 4th clean batch running (30 silent + 31 catalog + 32 catalog + 33 catalog)**, further strengthening the single-re-fire reading (dormant-not-closed) → [[openai-narrative-ad-experiments]]. Cumulative **88 ads, still 4 with copy — 3 distinct creatives** (84/88 = 95.5% placeholder); lab-delta vs Anthropic 88/8 (**11.0x — new widest in the farm**).
- **[[ro]] SILENT — Run 11 ends at a single batch.** No new Ro ad. Run 11 (batch 32's 2 placeholders) closes at 1 batch, mirroring Run 10 (also a single batch, batch 30). Ro's burst lengths remain irregular (1-3). Cumulative **29 ads, all placeholder-only**.
- **[[anthropic]] 22nd consecutive silence (12-33) on its own page — STRICT LOCK HOLDS.** No new Anthropic-page ad; the 2026-05-11 cluster stays confirmed-stalled at 2. **Microsoft Cloud absent for the 11th batch running (23-33)** — the AI-lab paid-social field stays OpenAI-only. Cumulative **8 ads, 0 with copy** (100% placeholder across 33 batches); lab-delta vs OpenAI 8/88 (~11.0x).
- **[[eden]] (TryEden) 20th consecutive silence (14-33).** No new TryEden ad. Cumulative **1 Eden ad, placeholder-only**.
- **2 Hampton-substring noise pages — a new first-fire + a repeat.** **Hampton City Schools** (1 image ad, ID `1035969922490319`, started 2026-07-06) — school-nurse recruitment (*"🩺 Now Hiring: School Nurses for the 2026–2027 School Year!"*), a **new first-fire Hampton-substring noise page** (Virginia school district, NOT [[hampton-founders]]). **Hampton Roads Honda Dealers** (1 carousel placeholder, ID `3106403162888025`, started 2026-05-01) — a **REPEAT Hampton noise page** (first fired batch 8 / 2026-05-20). Both confirm the "Hampton" filter remains decisively net-negative.

## Source

- Path: `raw/ads/digest-2026-07-07.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 197 • New: 6 • Dedup-skipped: 191 (97.0%)
- Gap from prior batch: **1 day** (batch 32 = 2026-07-06)

## Tracked-brand creative inventory — 2 of 6 (33.3%)

### [[hims]] — 1 new ad (catalog placeholder; Wegovy does NOT sustain)

- **1 catalog placeholder** — ID `966576545958808` (started **2026-05-13**), format unknown, body `{{product.brand}}` only. A ~2-month-old May-window re-surface via the catalog feed — no static copy. **The batch-32 Wegovy GLP-1 verbatim wave does not continue**; Hair Hybrids, Sex Rx, and Hard Mints all also silent. Batch 32's Wegovy re-open reads as a single-batch re-surface (dormant-not-closed). Cumulative **134 ads**.

### [[openai]] — 1 new ad (catalog placeholder; May-window re-surface)

- **1 carousel placeholder** — ID `945993881573821` (started **2026-05-08**), headline `{{product.name}}` / body `{{product.brand}}`. The oldest Cluster-2 / May-8 window re-surfacing (older than the June-window placeholders of batch 32). No new launch window; no new copy ad — the batch-29 o3 re-fire gets no continuation for the 4th clean batch running (see TL;DR). Cumulative **88 ads, 4 with copy — 3 distinct creatives** (84/88 = 95.5% placeholder).

### All other tracked brands — 0 new ads

- **[[ro]]** — silent; Run 11 ends at a single batch (batch 32 only). Cumulative **29 ads, all placeholder**.
- **[[anthropic]]** — silent; 22nd consecutive (12-33); strict lock holds; Microsoft Cloud absent for the 11th batch running (23-33). Cumulative **8 ads, 0 with copy**.
- **[[eden]]** (TryEden) — silent; 20th consecutive (14-33). Cumulative **1 ad, placeholder**.
- **[[henry-meds]]** — **still absent (33rd consecutive batch)** — the "Henry Brown" ads are a false-positive collision, not Henry Meds (see below).
- **[[hampton-founders]]** — 0 real ads since 2026-05-06; the "Hampton City Schools" + "Hampton Roads Honda" ads are false-positive collisions (see below).
- **DealMachine** — never appeared (33rd consecutive batch).

## "Noise" inventory — 4 of 6 ads (66.7%)

### "Henry" collision — Dr. Henry Brown (urologist) — 2 ads — FIRST "Henry" false positive in the farm

- **Henry Brown** — DTC men's-health / urology funnel, NOT [[henry-meds]]. Two ads under the "Henry Brown" FB page:
  - **Ad 1** — carousel placeholder, ID `1507753507282847` (started 2026-07-06), headline `{{product.name}}` / body `{{product.brand}}`.
  - **Ad 2** — image, ID `1339093435097279` (started 2026-07-06). **Long-form direct-response BPH / enlarged-prostate narrative** (headline *"Read if your prostate is enlarged…"*): *"If you're taking Flomax or Tamsulosin for your enlarged prostate, you're on a ticking clock — within a few years you'll rely on a catheter or need risky prostate surgery. I know this because I'm a urologist. It's not healing your prostate. It's actually your one-way ticket to a catheter and surgery… I'm Dr. Henry Brown. Board-certified urologist. I've been in practice for 19 years… Pharmaceutical companies have conditioned an entire generation of urologists — myself included — to believe Flomax and other drugs (Alfuzosin, Finasteride) are the only 'treatments'… Look, I perform prostate surgeries (TURP, HoLEP and more)…"* The copy runs the classic long-form-DR medical structure — **credentialed-authority opener + fear/urgency (catheter, surgery) + pharma-villain reframe + "proof below" curiosity gap** — the same shape the farm has filed before as noise-but-worth-studying (batch-8 Cholesterol Support Group ICU-nurse statins narrative; Lauren Brooks pet-allergy). This is the **first "Henry"-substring collision in 33 batches**: the "Henry Meds" search term matched a first-name-only page, and [[henry-meds]] itself remains absent. → [[competitor-ads-farm]] known-issue section.

### "Hampton" collision — 2 ads (1 new first-fire + 1 repeat)

- **Hampton City Schools** — image, ID `1035969922490319` (started 2026-07-06). **School-nurse recruitment** ad: *"🩺 Now Hiring: School Nurses for the 2026–2027 School Year! … Predictable schedule. Superior work-life balance. Meaningful community impacts. Apply or share…"* → `bit.ly/4u8F9w8`. A **new first-fire Hampton-substring noise page** (Virginia school district), NOT [[hampton-founders]].
- **Hampton Roads Honda Dealers** — carousel placeholder, ID `3106403162888025` (started 2026-05-01), body `{{product.brand}}`. A **REPEAT Hampton noise page** (first fired batch 8 / 2026-05-20, where it appeared as 2 carousel ads). Regional Honda dealer group; catalog dynamic-feed placeholder.

## Cross-cutting patterns

### The "Henry" collision — a new noise axis confirms the batch-1 filter problem

Across 33 batches the farm's "brand-name filter too permissive" issue has surfaced on the "Ro," "Eden," and "Hampton" terms (dozens of substring/adjacency false positives). Batch 33 adds the **"Henry" axis**: the first-ever match on the "Henry Meds" search term is a false positive — "Dr. Henry Brown," a urologist, matched on the bare first name. The tell is that [[henry-meds]] has **never** appeared as real signal in 33 batches, yet the term now emits noise — exactly the net-negative profile that made the bare-"Ro" and bare-"Hampton" filters liabilities. The fix is the same standing recommendation: **page-ID allow-listing the real Henry Meds page** (once located) + blocklisting the collision pages, not tightening the search into dropping a challenger. Notably, the collision ad is a **higher-intel creative than the batch's actual signal** — the same paradox seen in batch 19 (loose filter surfaces the best copy specimen *because* it's loose): the only substantive new creative this batch is the Henry Brown BPH funnel, while both tracked-brand ads are inert placeholders.

### Rebound → trough oscillation continues; signal is catalog-only

Batch 32's three-brand rebound (Hims Wegovy + OpenAI + Ro) does not carry into batch 33 — the daily surge/trough swing returns to a low-signal read. The distinctive feature of this trough is that it's **collision-heavy rather than thin**: 6 ads, but 4 are false positives and the 2 tracked ads are both old-window catalog placeholders. **Zero fresh tracked-brand creative shipped** — the freshest tracked start dates are 2026-05-13 (Hims) and 2026-05-08 (OpenAI), both ~2 months stale. No tracked brand ran new copy this batch.

### OpenAI's o3 re-fire — no continuation across four clean batches

The batch-29 verbatim o3 Deep Research re-fire — the farm's only copy-ad recurrence — now shows **no continuation across batches 30 + 31 + 32 + 33** (4 clean batches). No sibling o3 creatives, no new narrative on any surface. The single-re-fire reading (batch-9/21/27 one-off shape, imported to a re-fire) strengthens further, though dormant-not-closed per the rule that broke in batch 29. → [[openai-narrative-ad-experiments]].

### Thirty-three-batch convergence (recent batches)

| Batch | Date | Fetched | New | Dedup | New % | OpenAI | Hims | Anthropic | Ro | Eden | Signal % |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 29 | 2026-07-03 | 183 | 7 | 176 | 3.8% | 2 | 3 | 0 | 0 | 0 | 71.4% |
| 30 | 2026-07-04 | 186 | 1 | 185 | 0.5% | 0 | 0 | 0 | 1 | 0 | 100% |
| 31 | 2026-07-05 | 190 | 2 | 188 | 1.1% | 1 | 0 | 0 | 0 | 0 | 50% |
| 32 | 2026-07-06 | 190 | 8 | 182 | 4.2% | 3 | 2 | 0 | 2 | 0 | 87.5% |
| **33** | **2026-07-07** | **197** | **6** | **191** | **3.0%** | **1** | **1** | **0** | **0** | **0** | **33.3%** |

(Full table in [[ads-digest-2026-06-09]] / [[ads-digest-2026-06-24]].) Batch 33 inverts the batch-32 rebound — the lowest signal rate since batch 31, and the only recent batch whose noise is dominated by brand-name collisions rather than substring noise.

### What did NOT happen this batch

- **No new tracked-brand copy** — both Hims and OpenAI shipped only old-window catalog placeholders; no Wegovy / Hair Hybrids / Sex Rx / o3 / ChatGPT / Codex creative.
- **No Wegovy continuation** — batch 32's Wegovy re-open was a single-batch re-surface (dormant-not-closed).
- **No OpenAI copy ad** — the o3 re-fire gets no continuation for the 4th clean batch running (30+31+32+33).
- **No Ro ad** — Run 11 closes at a single batch.
- **No Anthropic / Microsoft Cloud creative** — 22nd Anthropic silence; Microsoft absent 11th batch running.
- **No real Henry Meds or Hampton Founders ad** — every "Henry"/"Hampton" match this batch is a false-positive collision.

## Open questions

- **Does the Wegovy wave stay closed, or was batch 32 the start of a slow flight?** Batch 33 adds no Wegovy copy — leaning single-batch re-surface, but dormant-not-closed → [[dtc-telehealth-ad-template]].
- **Is the batch-29 o3 re-fire a single re-fire or a slow-repeating flight?** Batches 30-33 add no recurrence (4 clean batches) — leaning single-re-fire, but dormant-not-closed → [[openai-narrative-ad-experiments]].
- **Will the "Henry Brown" collision recur (like Uproot / SecretRomance) or one-off?** First fire in batch 33; watch whether the urologist funnel keeps emitting fresh creative → [[competitor-ads-farm]].
- **Is Henry Meds genuinely un-advertised, or is the search-term/page-name mismatch hiding real signal?** 33 batches, zero real Henry Meds ads, now a "Henry" collision — the page-ID allow-list fix is overdue → [[henry-meds]].
- **Is Anthropic's own-page silence permanent or pre-launch?** 22 consecutive batches; any future ad = a new launch window.

## Related

- [[competitor-ads-farm]] — thirty-third batch; clean 1-day gap; 6 new ads, 33.3% signal; the batch-32 three-brand rebound does NOT sustain — a collision-heavy, catalog-only, zero-fresh-creative trough; **FIRST-EVER "Henry" brand-name collision** (Dr. Henry Brown, urologist, long-form BPH DR funnel — NOT Henry Meds); Hims + OpenAI both placeholder-only May-window re-surfaces; o3 re-fire no continuation (4th clean batch); Ro Run 11 ends at 1 batch; Anthropic 22nd silence; Eden 20th silence; Hampton City Schools (new) + Hampton Roads Honda (repeat) noise
- [[henry-meds]] — the "Henry Brown" urologist ads are a false-positive collision on the "Henry" search term; Henry Meds itself still absent (33rd consecutive batch)
- [[hampton-founders]] — the "Hampton City Schools" + "Hampton Roads Honda" ads are false-positive collisions on the "Hampton" term; no real Hampton Founders ad since 2026-05-06
- [[hims]] — 1 catalog placeholder (2026-05-13 May-window re-surface); Wegovy does NOT sustain (single-batch re-surface); cumulative 134 ads
- [[openai]] — 1 catalog placeholder (2026-05-08 Cluster-2 re-surface); no new copy; o3 re-fire no continuation (4th clean batch); cumulative 88 ads, 4 with copy; lab-delta 11.0x
- [[openai-narrative-ad-experiments]] — the o3 re-fire gets no continuation across batches 30-33 (4 clean batches); single-re-fire reading strengthens
- [[dtc-telehealth-ad-template]] — no template copy shipped this batch (Hims placeholder-only); Wegovy dormant again
- [[compounded-drug-disclaimer]] — no disclaimer copy shipped this batch (Hims placeholder-only)
- [[anthropic]] — 0 new ads; 22nd consecutive silence (12-33); strict lock holds; Microsoft Cloud absent 11th batch running; cumulative 8 ads
- [[eden]] — TryEden 20th consecutive silence (14-33); cumulative 1 Eden ad
- [[ro]] — 0 new ads; Run 11 ends at a single batch; cumulative 29 ads, all placeholder
- [[ads-digest-2026-07-06]] — thirty-second batch (the predecessor: three-brand rebound, Hims Wegovy wave reopens, OpenAI 3 catalog placeholders, Ro Run 11 opens, Uproot July-4th BOGO)

## Appears in

- Thirty-third entry in `wiki/sources/` for the competitor-ads farm. **6 new ads, 33.3% tracked-brand signal** at a clean 1-day gap (97.0% dedup) — the batch-32 three-brand rebound does NOT sustain; batch 33 is a **collision-heavy, catalog-only, ZERO-fresh-creative trough** (2 tracked placeholders + 4 false-positive noise ads). **THE HEADLINE — the farm's FIRST-EVER "Henry" brand-name collision: [[henry-meds]]'s term matches "Dr. Henry Brown," a board-certified urologist running a long-form direct-response BPH/enlarged-prostate funnel** (IDs `1507753507282847` + `1339093435097279`, both started 2026-07-06) — a false positive (Henry Meds still absent, 33rd batch) that confirms the batch-1 filter problem on a new axis. **[[hims]] 1 catalog placeholder** (2026-05-13 May-window re-surface — Wegovy wave does NOT sustain, single-batch re-surface). **[[openai]] 1 catalog placeholder** (2026-05-08 Cluster-2 re-surface — no new copy; o3 re-fire no continuation for the 4th clean batch 30+31+32+33; cumulative 88 ads, 4 with copy, lab-delta 11.0x). **[[ro]] SILENT** (Run 11 ends at 1 batch). **[[anthropic]] 22nd consecutive silence** (strict lock holds; Microsoft Cloud absent 11th batch running). **[[eden]] 20th consecutive silence.** 2 Hampton-substring noise ads — **Hampton City Schools** (new first-fire, school-nurse recruitment) + **Hampton Roads Honda Dealers** (repeat, first fired batch 8). Cumulative **134 Hims / 88 OpenAI / 8 Anthropic / 29 Ro / 1 Eden**.
</content>
</invoke>
