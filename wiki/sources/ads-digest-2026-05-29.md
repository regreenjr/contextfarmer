---
title: FB Ads Digest — Competitor brands — 2026-05-29
category: source
summary: Fourteenth competitor-ads farm batch — 5 new FB Ad Library entries (205 fetched, 200 dedup-skipped, 97.6%) after a 1-day gap from batch 13; **[[hims]] runs a GENUINE THREE-WEDGE surge — all three creative wedges ship verbatim static copy in one 1-day-gap batch** (Wegovy GLP-1 + Sex Rx + Hair Hybrids), the first non-compression three-wedge batch in the farm (batch 8's three-wedge surge was a confirmed 4-day-gap compression artifact); **Wegovy verbatim wave REOPENS after being declared "structurally CLOSED"** — the canonical GLP-1 template returns (ID `2051858468695624` started 2026-05-21, full copy) after 5 consecutive silent batches (9+10+11+12+13), BREAKING the batch-11 ≥3-batch wave-closure diagnosis — the 2nd "locked/closed" call broken in the farm (after Anthropic's batch-11 standalone-launch break); **Sex Rx wedge RETURNS after silence since batch 7** — Sex Rx + Testosterone Support SKU (ID `1018544387271890` started 2026-05-20, full copy), first Sex Rx ad in 13 days and first Testosterone Support SKU re-launch since batch 2; **Hair Hybrids continues** — 2 verbatim re-launches #8+#9 (IDs `945711041650935` started 2026-05-05 + `26975341935442255` started 2026-05-21), wave spans 1+8+9+10+13+14; **methodology lesson: "structurally closed at ≥3-batch silence" is false-positive-prone for Hims wedges — closure should be downgraded to "dormant," waves reopen even after 5-batch silence**; per-day rate (5.0 ads/day) recovers above batch 13's 4.0/day, driven entirely by the Hims three-wedge surge (Hims 4.0/day); only 1 noise ad (Evereden kid skincare, "Eden" substring); **real-signal rate 80% (4 of 5) — new farm high-water mark** (beats batch 7/12's 67%); OpenAI / Anthropic (3rd consecutive silence 12+13+14) / Ro (2-batch trough) / Eden-TryEden (1-batch after first signal) / Henry Meds / Hampton / DealMachine all silent
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, hims, three-wedge-surge, genuine-three-wedge, wegovy-wave-reopens, closure-call-broken, sex-rx-returns, hair-hybrids-continues, testosterone-support-sku, signal-rate-80, anthropic-3rd-silence, ro-2-batch-trough, evereden-noise]
sources: 1
source_path: raw/ads/digest-2026-05-29.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-29
updated: 2026-05-29
---

# FB Ads Digest — 2026-05-29

Fourteenth batch from the [[competitor-ads-farm]]. **5 new ads, 200 dedup-skipped** out of 205 fetched after a 1-day gap from batch 13 (2026-05-28). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **[[hims]] runs a GENUINE THREE-WEDGE surge — all three creative wedges ship verbatim static copy in one batch**: Wegovy GLP-1 (ID `2051858468695624`, started 2026-05-21) + Sex Rx + Testosterone Support (ID `1018544387271890`, started 2026-05-20) + Hair Hybrids ×2 (IDs `945711041650935` started 2026-05-05 + `26975341935442255` started 2026-05-21). **This is the first GENUINE three-wedge batch in the farm.** Batch 8's apparent three-wedge surge was a confirmed 4-day-gap *compression* artifact (collapsed 4 days of shipping into one batch). Batch 14 ships all three wedges with full static copy at a **1-day gap** — no compression — making it the cleanest evidence of a coordinated multi-wedge surge in the farm's history.
- **Wegovy verbatim wave REOPENS after being declared "structurally CLOSED."** The canonical GLP-1 template (*"Get Wegovy® with Hims, plus access to provider-led care..."* → ✅ FDA-approved GLP-1 pill and pens / ✅ Medication as low as $149/mo / ✅ 100% online) returns verbatim after **5 consecutive silent batches (9+10+11+12+13)**. The batch-11 diagnosis — "Wegovy verbatim wave structurally CLOSED at the ≥3-batch threshold" — is now **BROKEN**. This is the **2nd "locked/closed" call broken in the farm**, after Anthropic's batch-11 standalone-launch break. **Methodology lesson below.**
- **Sex Rx wedge RETURNS after silence since batch 7.** Sex Rx + Testosterone Support (the 3rd Sex Rx SKU, documented in batch 2) ships verbatim — first Sex Rx ad in **13 days** (last was Climax Control in batch 7, 2026-05-16) and **first Testosterone Support SKU re-launch since batch 2** (2026-05-10).
- **Hair Hybrids continues** — 2 verbatim re-launches (#8 + #9). Hair Hybrids verbatim now spans batches **1+8+9+10+13+14** with **9 cumulative post-cold-start re-launches**; it remains the standing late-May 2026 Hims template and is now joined by the reawakened Wegovy and Sex Rx wedges.
- **Per-day rate (5.0 ads/day) recovers above batch 13's 4.0/day** — but the recovery is entirely the Hims three-wedge surge (Hims 4.0/day vs batch 13's 1.0/day). Every other tracked brand is silent, so the farm-wide rate would be ~1.0/day without Hims.
- **Real-signal rate 80% (4 of 5) — new farm high-water mark** (beats the prior 67% high in batches 7 + 12). Only 1 noise ad this batch (Evereden), the cleanest signal-to-noise ratio since cold start.
- **OpenAI / Anthropic / Ro / Eden(TryEden) all silent.** Anthropic is now at its **3rd consecutive silence (12+13+14)** since the batch-11 slow-cluster expansion; Ro is at a **2-batch trough** (13+14); TryEden goes silent 1 batch after its first signal; OpenAI ships nothing after batch 13's possible Cluster-4 placeholder. Henry Meds / Hampton Founders / DealMachine — 14th consecutive batch with no signal.
- **Brand-name filter still untuned — 14th consecutive batch.** Outstanding since 2026-05-06. This batch is unusually clean (only 1 noise ad) but that reflects a thin noise draw, not a filter fix.

## Source

- Path: `raw/ads/digest-2026-05-29.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 205 • New: 5 • Dedup-skipped: 200 (97.6%)
- Gap from prior batch: 1 day (batch 13 = 2026-05-28)

## Tracked-brand creative inventory

### [[hims]] — 4 new ads (GENUINE THREE-WEDGE surge — Wegovy reopens + Sex Rx returns + Hair Hybrids continues)

**Ad #1 — Wegovy GLP-1 verbatim re-launch (FULL COPY) — WAVE REOPENS**

- ID `2051858468695624`, started **2026-05-21**, format unknown
- Body copy (verbatim to the canonical GLP-1 instantiation in [[concepts/dtc-telehealth-ad-template]]):

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

Plus the expanded pricing footnote (*"$149/mo price includes medication only... An active Hims Weight Loss Membership is required ($39 for the first month, auto-renews at $149/month thereafter)..."*) and the Wegovy®/Novo Nordisk non-affiliation disclaimer. This is the **first Wegovy GLP-1 ad since batch 8 (2026-05-20)** — Wegovy was silent across batches 9+10+11+12+13 (5 consecutive batches), at which point the wave was diagnosed "structurally CLOSED" (batch 11, ≥3-batch threshold). **The verbatim re-launch REOPENS the wave.** Note the ad's start date (2026-05-21) falls *inside* the silent window — a fresh ad launched during the "closed" period that only surfaced via catalog now (catalog re-surface lag).

**Ad #2 — Sex Rx + Testosterone Support verbatim re-launch (FULL COPY) — WEDGE RETURNS**

- ID `1018544387271890`, started **2026-05-20**, format unknown
- Body copy (verbatim to the Testosterone Support SKU documented in batch 2, see [[hims]] Wedge 3):

> 🔥New Sex Rx + Testosterone Support 🔥
> Daily 2-in-1 pill to optimize your sex life and testosterone, plus supplements to support overall health.
>
> 🚀Boost your sex life and achieve stronger erections thanks to tadalafil
> 💪Optimize testosterone thanks to zinc
> 🍎Support health and performance with L-arginine, Vitamin B12, and Vitamin B6
> ⌛Be ready for sex—every time, anytime

Plus the standard compounded-drug disclaimer (*"Sex Rx + Testosterone Support is a compounded drug product. The FDA does not approve or verify compounded drugs..."*). This is the **first Sex Rx ad in 13 days** (the last Sex Rx ad was the Climax Control SKU in batch 7, 2026-05-16). It is also the **first Testosterone Support SKU re-launch since batch 2 (2026-05-10)** — the Sex Rx wedge returns with the testosterone-laddering SKU (the low-T failure-mode variant), not the Climax Control SKU that ran in batches 5+7.

**Ad #3 — Hair Hybrids verbatim re-launch #8 (FULL COPY)**

- ID `945711041650935`, started **2026-05-05**, format unknown
- Body copy verbatim to the canonical Hair Hybrids template (same hook *"Don't wait — join the hundreds of thousands of guys..."* + 🗓️ Regrow in as few as 3-6 months / 🧑🏻‍⚕️ Doctor-trusted ingredients / 📦 Free shipping to your front door (if prescribed) + Hair Hybrids compounded disclaimer + "Individual results may vary / separate individual studies" block).

**Ad #4 — Hair Hybrids verbatim re-launch #9 (FULL COPY)**

- ID `26975341935442255`, started **2026-05-21**, format unknown
- Body copy **identical** to Ad #3 (same Hair Hybrids template, word-for-word). Two simultaneous verbatim Hair Hybrids instances in one batch — same inside-structure-A/B pattern seen in prior surge batches (different ad IDs / start dates, identical copy = audience or visual-asset A/B behind the same skeleton).

**Strategic significance**:

1. **GENUINE three-wedge surge — the first in the farm.** All three Hims creative wedges (GLP-1 + Sex Rx + hair-loss) ship verbatim static copy in the *same* batch, at a **1-day fetch gap** (no compression). Batch 8's superficially-similar three-wedge surge was later confirmed to be a 4-day-gap compression artifact (per-day rate matched the 2.0-2.5 Hims/day baseline once gap-normalized). Batch 14, at a clean 1-day gap, is the **cleanest evidence of a coordinated multi-wedge surge** the farm has produced. Hims's surge-trough cadence not only resumed (after the batches-11+12 placeholder trough and the thin batch 13) — it resumed with **all three wedges firing at once**.
2. **Wegovy wave REOPENS — the "structurally closed" diagnosis is BROKEN.** Wegovy went silent 9+10+11+12+13 (5 batches) and was declared structurally closed at batch 11. Batch 14's verbatim re-launch proves the wave was **dormant, not closed**. This is the 2nd "locked/closed" call broken in the farm (after the batch-11 Anthropic standalone-launch break). See methodology note below.
3. **Sex Rx returns after the longest single-wedge silence in the farm** (batch 7 → batch 14 = 13 days / 6 silent active batches for Sex Rx). The Sex Rx wedge rotated *out* across batches 8-13 and rotated *back in* at batch 14 — confirming surge composition rotates across *all three* wedges, not just the Wegovy↔Hair-Hybrids pair seen earlier.
4. **Inside-structure A/B still dominates — no template variation.** All four ads are verbatim re-launches of canonical templates. The only structural innovation in the farm's lifetime remains the 2026-05-10 Hard Mints four-bullet variant. Hims continues to test inside the skeletons, not across them.

**Updated Hair Hybrids verbatim instances (post-cold-start re-launches):**

| Batch | Date | Ad ID(s) | Started |
|---|---|---|---|
| 1 | 2026-05-06 | (initial 10+ wave) | early Apr 2026 |
| 8 | 2026-05-20 | `2064207334519052` + `728317760309201` | 2026-05-09, 2026-04-22 |
| 9 | 2026-05-22 | `3372941842875795` + `868992329557540` + `2498995467227011` | 2026-02-26, 2026-05-06, 2026-05-19 |
| 10 | 2026-05-23 | `1302383031990848` | 2026-04-22 |
| 11-12 | (silent) | — | — |
| 13 | 2026-05-28 | `1502428521462699` | 2026-05-14 |
| **14** | **2026-05-29** | **`945711041650935` + `26975341935442255`** | **2026-05-05, 2026-05-21** |

Hair Hybrids verbatim now spans batches **1+8+9+10+13+14** (2-batch trough at 11+12) — **9 cumulative post-cold-start re-launches**. Cumulative **77 Hims ads across 14 batches** (73 → 77).

### [[openai]] — 0 new ads (silent)

No new OpenAI ads in batch 14. The batch-13 possible Cluster-4 ad (2026-05-22 launch date) does **not** expand this batch — consistent with the "irregular catalog re-surface, not a new cluster" reading at 1 ad. Cluster 3 remains stalled at 3 ads / 1 with copy (14 days post-launch). Cumulative **46 OpenAI ads across 14 batches, still 1 with copy.**

### [[anthropic]] — 0 new ads (3rd consecutive silence 12+13+14)

No new Anthropic ads — **3rd consecutive silent batch (12+13+14)** since the batch-11 slow-cluster expansion. The 2026-05-11 cluster's observed cadence is 14 days between ads; the next ad would be expected ~2026-06-08, so 3 silent batches do **not** yet confirm a stall (the ≥5-silent-batch Anthropic threshold from the batch-11 revision implies silence through ~batch 16-17 to claim the cluster stalled at 2 ads). Cumulative **8 ads, 0 with copy** — unchanged.

### [[ro]] — 0 new ads (2-batch trough)

No new Ro ads — **2nd consecutive silence (13+14)** after batch-12's 2-ad return (Run 3). Within Ro's irregular-burst cadence (mean run ~2 batches, mean trough ~3 batches), a 2-batch trough is well within range and is not a wave-closure signal. Cumulative **9 Ro ads across 14 batches, ALL placeholder-only.**

### [[eden]] (TryEden) — 0 new ads (1-batch silence after first signal)

No new TryEden ads — a single silent batch after the batch-13 first-signal placeholder. One silent batch tells us nothing yet about Eden's cadence; whether TryEden surfaces again (and whether it ever ships static copy) remains the open Eden creative-intel question. Cumulative **1 Eden ad, placeholder-only.**

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (14th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (14th consecutive batch)

## False positives ("brand-name match" noise) — 1 of 5 ads (20%)

The cleanest noise ratio since cold start — only **1 noise ad** this batch (vs the 11-brand "Eden" / 15-brand "Hampton" / unbounded "Ro" noise corpora). This reflects a thin noise draw in a small 5-ad batch, not a filter fix (the filter remains untuned).

1. **Evereden** (1 video ad, started 2026-05-06) — kid skincare brand (*"Designed with kids in mind 🌈 ... Shop now and get 10% off your first order!"*). Substring root cause "Ever**eden**" → bare-"Eden" filter. **Already counted** in the 11-brand "Eden" noise corpus (first surfaced batch 5, 2026-05-14). A returning noise page, not a new one. Notable irony recurring from batch 13: the "Eden" search that now also catches the real TryEden telehealth signal continues to drag in unrelated "Eden"-substring brands — reinforcing that the right fix is **page-ID allow-listing TryEden + blocklisting the noise brands**, not dropping the search.

### Cumulative noise-corpus updates

- **"Eden" noise brands**: still **11 distinct** (Evereden already counted from batch 5; no new "Eden" noise brand this batch).
- **"Ro" / "Hampton" noise**: no new pages this batch (no Ro/Hampton-substring noise drew into this small batch).
- **Non-substring noise events**: still 2 of 14 batches (14.3%) — Adobe Acrobat (batch 3) + Romance miniseries (batch 4); none this batch.

## Cross-cutting patterns

### Fourteen-batch farm convergence table

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
| **2026-05-29** | **205** | **5** | **200** | **2.4%** | **0** | **4** | **0** | **0** | **0** | **80%** |

Batch 14 is the **highest real-signal-rate batch in the farm (80%)** — only 1 noise ad against 4 Hims ads. It is also the **most Hims-concentrated batch since cold start**: 4 of 5 new ads are Hims, and Hims is the *only* tracked brand with signal this batch.

### Per-day rate recovers — but it's a Hims-only recovery

Batch 14's **5.0 ads/day** (5 new / 1-day gap) recovers above batch 13's 4.0/day:

| Batch | Gap (days) | Total ads | Ads/day | Hims/day | OpenAI/day | Ro/day |
|---|---|---|---|---|---|---|
| 8 | 4 | 36 | 9.0 | 2.00 | 1.75 | 0.50 |
| 9 | 2 | 17 | 8.5 | 2.50 | 1.50 | 0.50 |
| 10 | 1 | 8 | 8.0 | 2.00 | 1.00 | 0 |
| 11 | 2 | 12 | 6.0 | 1.00 | 0 | 0 |
| 12 | 1 | 6 | 6.0 | 1.00 | 1.0 | 2.0 |
| 13 | 2 | 8 | 4.0 | 1.0 | 0.5 | 0 |
| **14** | **1** | **5** | **5.0** | **4.0** | **0** | **0** |

The recovery is **entirely Hims** — Hims jumps to 4.0/day (its highest 1-day-normalized rate in the farm, reflecting the three-wedge surge), while OpenAI / Ro / Anthropic / Eden are all at 0. Farm-wide rate *minus Hims* would be ~1.0/day (the lone Evereden noise ad). So the per-day rate downward-drift question (was the farm declining toward ~4/day, or just in a coordinated trough?) is **not** resolved by batch 14: the non-Hims brands are still in their troughs; Hims alone masked the drift this batch. The cleaner read is that **batch 14 is a Hims surge superimposed on a continuing multi-brand trough.**

### Methodology lesson — downgrade "structurally closed" to "dormant" for Hims wedges

The Wegovy wave's reopening is the **2nd time a "locked/closed" diagnosis has been broken** in the farm:

1. **Batch 11** — Anthropic's "2026-05-11 standalone launch" lock (set at batch 8 via the ≥3-silent-batch methodology) was broken when a 2nd cluster ad surfaced after 5 silent batches. → methodology revised to ≥5-batch threshold for Anthropic's slow cadence.
2. **Batch 14** — Hims's "Wegovy verbatim wave structurally CLOSED" diagnosis (set at batch 11 via the ≥3-silent-batch threshold) is broken when the Wegovy template returns verbatim after **5 silent batches** (9-13).

**Implication**: the "≥3-batch silence ⇒ structurally closed" rule is **false-positive-prone** for Hims's catalog-driven creative-ops. A wedge can go dormant for 5 batches (Wegovy) or 13 days (Sex Rx) and then re-fire verbatim. **The correct framing is "dormant," not "closed"** — Hims wedges cycle in and out of the surge composition on irregular multi-batch cadences, and any wedge silent for several batches should be treated as *between re-surface events* (the same reading that batch 13 confirmed for the Hair Hybrids 11+12 trough), not permanently retired. For [[medvi-positioning]], this means **all three Hims wedge templates remain live diff-targets** even when one or more is silent for a stretch — none has been retired across 14 batches.

## Open questions

- **Is batch 14 the start of a sustained three-wedge surge, or a single-batch coincidence of three re-surface events?** Batch 15 distinguishes — if all three wedges keep shipping, Hims has genuinely intensified; if it drops back to Hair-Hybrids-only or placeholder, batch 14 was a coincidental triple re-surface.
- **Does the non-Hims multi-brand trough continue?** OpenAI / Ro / Anthropic / TryEden are all silent. Batch 15's non-Hims volume tests whether the farm-wide per-day rate is genuinely declining (~4/day floor) or just in a coordinated trough that Hims masked this batch.
- **Does Anthropic's 2026-05-11 cluster surface a 3rd ad ~2026-06-08?** 3 silent batches (12+13+14) — the 14-day cadence predicts the next expansion ~2026-06-08; silence through ~batch 16-17 would confirm the cluster stalled at 2 ads.
- **Does TryEden surface again, and does it ever ship static copy?** One silent batch after the first signal tells us nothing about Eden's cadence yet.
- **Should the "wave closure" methodology be formally retired for Hims wedges?** Two broken closure calls (Anthropic, Wegovy) argue for replacing "closed" with a dormancy-half-life model.

## Related

- [[competitor-ads-farm]] — fourteenth batch from this farm; genuine three-wedge Hims surge; Wegovy wave reopens (closure call broken); per-day rate recovers Hims-only
- [[hims]] — 4 new ads; GENUINE three-wedge surge (Wegovy reopens + Sex Rx returns + Hair Hybrids ×2); cumulative 77 ads
- [[concepts/dtc-telehealth-ad-template]] — all three wedge instantiations ship verbatim in one batch (GLP-1 + Sex Rx Testosterone Support + Hair Hybrids); Wegovy reopens after closure
- [[concepts/compounded-drug-disclaimer]] — Wegovy + Sex Rx + Hair Hybrids disclaimer blocks all ship verbatim in one batch; Wegovy disclaimer wave reopens after 5-batch silence
- [[eden]] — TryEden silent 1 batch after first signal; Evereden noise (kid skincare, "Eden" substring) returns from batch 5
- [[openai]] — 0 new ads; possible Cluster-4 ad does not expand; cumulative 46 ads
- [[anthropic]] — 0 new ads; 3rd consecutive silence (12+13+14); cumulative 8 ads
- [[ro]] — 0 new ads; 2-batch trough (13+14); cumulative 9 ads
- [[ads-digest-2026-05-28]] — thirteenth batch (Eden first signal; Hair Hybrids returns wave open; per-day drift to 4.0/day)

## Appears in

- Fourteenth entry in `wiki/sources/` for the competitor-ads farm. **[[hims]] runs a GENUINE THREE-WEDGE surge** — all three creative wedges ship verbatim static copy in one 1-day-gap batch (Wegovy GLP-1 ID `2051858468695624` + Sex Rx Testosterone Support ID `1018544387271890` + Hair Hybrids ×2 IDs `945711041650935` + `26975341935442255`), the first non-compression three-wedge batch (batch 8's was a confirmed 4-day-gap compression artifact). **Wegovy verbatim wave REOPENS** after 5 silent batches (9-13) — BREAKS the batch-11 "structurally CLOSED" diagnosis, the 2nd broken closure call after Anthropic's batch-11 standalone-launch break. **Sex Rx wedge RETURNS** after silence since batch 7 (Testosterone Support SKU, first since batch 2). **Hair Hybrids continues** (re-launches #8+#9, wave spans 1+8+9+10+13+14, 9 cumulative re-launches). **Methodology lesson**: "structurally closed at ≥3-batch silence" is false-positive-prone for Hims wedges — downgrade to "dormant"; all three wedge templates remain live diff-targets. Per-day rate (5.0/day) recovers above batch 13's 4.0/day but Hims-only (4.0 Hims/day; all other brands silent). Real-signal rate **80% (4 of 5) — new farm high-water mark**. Only 1 noise ad (Evereden kid skincare, returning "Eden" substring). OpenAI / Anthropic (3rd consecutive silence) / Ro (2-batch trough) / TryEden (1-batch after first signal) / Henry / Hampton / DealMachine all silent. Cumulative 77 Hims / 46 OpenAI / 8 Anthropic / 9 Ro / 1 Eden ads.
