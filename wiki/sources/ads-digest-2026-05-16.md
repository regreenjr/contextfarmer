---
title: FB Ads Digest — Competitor brands — 2026-05-16
category: source
summary: Seventh competitor-ads farm batch — 9 new FB Ad Library entries (208 fetched, 199 dedup-skipped, 95.7%) — signal returns with the highest real-signal rate (67%) in any batch since cold start; Hims surges from silence with TWO verbatim template re-launches in one batch (Wegovy GLP-1 verbatim across **4 batches / 10-day stability window** + Sex Rx + Climax Control verbatim across 2 batches) — mirrors the batch-5 multi-instance surge pattern and confirms inventory-cycle wave timing; **OpenAI silence was transient — 2 new May 8 cluster ads expand the cluster from 6 → 8**, decisively disproving batch 6's "fully dedup-cached" diagnosis (cluster is still rolling out, just slower pacing); **Ro signal returns** after 5 batches of silence — 1 new placeholder ad (started 2026-05-04) — bare-"Ro" filter produces signal for first time since batch 2; Anthropic stays silent for 2nd consecutive batch (3rd batch since 2026-05-11 launch); 2 noise ads — Sean Gracet Roset (NEW "Ro" substring noise, AI photo app) + Nissan of Hampton (Hampton substring noise) + Eden Munoz repeat (banda singer); brand-name filter still untuned, seventh consecutive batch
tags: [fb-ads, ad-library, competitor-ads, dedup, farm-tuning, signal-return, hims-surge, openai-cluster-expansion, ro-signal-return]
sources: 1
source_path: raw/ads/digest-2026-05-16.md
source_date: 2026-05
authors: [farmer-competitor-ads, apify-fb-ads-scraper]
ingested: 2026-05-16
updated: 2026-05-16
---

# FB Ads Digest — 2026-05-16

Seventh batch from the [[competitor-ads-farm]]. **9 new ads, 199 dedup-skipped** out of 208 fetched across 8 tracked brand keywords (Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine). Apify `facebook-ads-library-scraper` actor.

## TL;DR

- **Signal returns hard.** 6 of 9 new ads (67%) are tracked-brand — highest real-signal proportion of any batch since cold start. Seven-batch noise-rate trend: 65% → 82% → 50% → 69% → 77% → 100% → **33%**. Batch 7 reverses batch 6's 100%-noise outcome decisively.
- **Hims surges back from silence with TWO verbatim template re-launches.** Mirrors the batch-5 (2026-05-14) multi-instance surge pattern. Wegovy GLP-1 template now verbatim across **4 batches** (10-day stability window: 2026-05-06 → 2026-05-12 → 2026-05-14 → 2026-05-16). Sex Rx + Climax Control template now verbatim across **2 batches** (2026-05-14 → 2026-05-16). Plus 1 placeholder ad. Cumulative 53 Hims ads.
- **OpenAI silence was transient — May 8 cluster expands from 6 → 8 ads.** 2 new carousels (started 2026-05-08) **decisively disprove batch 6's "fully dedup-cached at 6" diagnosis.** The cluster is still rolling out, just at slower pacing than batches 3+4. Cumulative **33 OpenAI ads, 0 with copy** — five-batch active-cluster span (2026-05-08 launches spread across batches 3+4+7).
- **Ro signal returns after 5-batch silence.** 1 new placeholder ad (started 2026-05-04, ID `1542915227491027`). Cumulative **4 Ro ads**, all `{{product.brand}}` placeholders, still zero teardown-able copy. The bare-"Ro" filter produces signal for first time since batch 2 (2026-05-10).
- **Anthropic stays silent for 2nd consecutive batch** (3rd batch since the 2026-05-11 launch). Cumulative 6 ads across 2 windows holds; "standalone launch" hypothesis gains evidence over "slow cluster."
- **2 noise ads + 1 repeat noise page.** Sean Gracet Roset (NEW "Ro" substring noise — AI photo app, video format, "FREE APP" headline) + Nissan of Hampton (Hampton substring noise — used vehicles carousel) + Eden Munoz (banda singer placeholder, repeat from batch 3).
- **Brand-name filter still untuned — seventh consecutive batch.** Outstanding action item from 2026-05-06.

## Source

- Path: `raw/ads/digest-2026-05-16.md`
- Fetcher: Apify FB Ad Library scraper (`facebook-ads-library-scraper`)
- Brands tracked: Hims, Ro, Eden, Henry Meds, Anthropic, OpenAI, Hampton, DealMachine
- Country filter: US
- Total fetched: 208 • New: 9 • Dedup-skipped: 199 (95.7%)

## Tracked-brand creative inventory

### [[hims]] — 3 new ads (Wegovy verbatim #4 + Sex Rx Climax Control verbatim #2 + 1 placeholder)

**Ad #1 — Wegovy GLP-1 verbatim re-launch (4th batch / 10-day stability window)**

- ID `1693764951776930`, started 2026-05-13, format unknown
- Body copy is **verbatim** to the 2026-05-06 canonical Wegovy GLP-1 template:

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

Followed by the standard $149/mo + $39 membership pricing disclosure and the FDA-approved-Wegovy disclaimer block.

**Wegovy GLP-1 verbatim instances (4-batch stability window):**

| Batch | Date | Ad ID | Started |
|---|---|---|---|
| 1 | 2026-05-06 | (initial wave) | early Apr 2026 |
| 4 | 2026-05-12 | `3567971296700086` | 2026-05-07 |
| 5 | 2026-05-14 | `956466943766183` | 2026-05-04 |
| **7** | **2026-05-16** | **`1693764951776930`** | **2026-05-13** |

**10-day verbatim-stability window.** Hims has now run identical body copy across 4 separate ad-library entries with launch dates spanning 2026-05-04 → 2026-05-13. Inside-structure A/B testing remains the standing pattern; the skeleton hasn't moved since 2026-05-06.

**Ad #2 — Placeholder (`{{product.brand}}` body)**

- ID `1316424053726023`, started 2026-04-08, format unknown
- Pure dynamic-creative placeholder, no static narrative
- This is the **5th Hims placeholder ad** tracked across 7 batches (batches 1, 5, 6, 7 — though most of the original batch 1's 26 placeholders weren't individually documented). The catalog-driven dynamic-creative half of Hims' two-track strategy continues to ship fresh entries alongside the static-narrative templates.

**Ad #3 — Sex Rx + Climax Control verbatim re-launch (2nd batch)**

- ID `1683250979537135`, started 2026-04-30, format unknown
- Body copy is **verbatim** to the 2026-05-06 canonical Sex Rx + Climax Control template:

> The 2-in-1 pill to get harder, and go longer. Sex Rx + Climax Control combines tadalafil shown to result in more satisfying erections and help men last longer, plus PE treatment. Get started today—100% online with a free consultation.
>
> Why Hims?
> 🤩Daily pill options for spontaneous sex
> 🧑‍⚕️Prescribed by licensed providers
> 📦100% online, free discreet shipping

Followed by the canonical compounded-drug disclaimer block.

**Sex Rx + Climax Control verbatim instances (2-batch stability window):**

| Batch | Date | Ad ID | Started |
|---|---|---|---|
| 5 | 2026-05-14 | `3275837862576962` | 2026-04-21 |
| **7** | **2026-05-16** | **`1683250979537135`** | **2026-04-30** |

**Two-wedge surge confirms inventory-cycle wave hypothesis.** Batch 7 mirrors batch 5's structural pattern — Hims runs verbatim re-launches across two distinct wedges (Wegovy GLP-1 + Sex Rx Climax Control) in the same batch. The post-batch-6 silence trough is now confirmed as a **timing artifact between waves**, not a structural shift. Standing pattern: surge batches ship 2-3 verbatim re-launches across multiple wedges; trough batches (3, 6) ship 0; alternating cadence is the steady state.

### [[openai]] — 2 new ads (May 8 cluster expands from 6 → 8)

From the digest:

- **Ad #1**: ID `1554270183093992`, started 2026-05-08, carousel, `{{product.name}}` / `{{product.brand}}` placeholders
- **Ad #2**: ID `1999764597582322`, started 2026-05-08, carousel, `{{product.name}}` / `{{product.brand}}` placeholders

**Both started 2026-05-08 — same launch cluster as batches 3+4** (Apr 30 + May 8 launches). Cluster 2 now contains **8 total ads** across batches 3+4+7:

| Batch | Date | New May 8 ads | Cumulative cluster-2 ads |
|---|---|---|---|
| 3 | 2026-05-11 | 2 | 2 |
| 4 | 2026-05-12 | 4 | 6 |
| 5 | 2026-05-14 | 0 | 6 (silence #1) |
| 6 | 2026-05-15 | 0 | 6 (silence #2 — "fully dedup-cached" hypothesis) |
| **7** | **2026-05-16** | **2** | **8 (silence diagnosis disproven)** |

**Decisively disproves batch 6's diagnosis.** Batch 6 concluded the May 8 cluster was "fully dedup-cached at 6 ads" based on two consecutive silent batches. Batch 7 ships 2 new ads with 2026-05-08 launch dates, meaning either:

1. The Apify actor's catalog-feed sampling is uneven across days (most likely — explains why some May 8 ads appeared in batches 3-4 and others took until batch 7 to surface)
2. OpenAI continued launching new ads with backdated 2026-05-08 timestamps (unlikely — ad-library start dates are immutable)
3. The cluster is much larger than 8 ads and is rolling out at slower pacing than the early-batch evidence suggested (also plausible)

**Implication for diagnostic methodology**: declaring a cluster "fully dedup-cached" after 2 silent batches was premature. Need ≥3 silent batches for high-confidence cache-completion claims. The right framing for OpenAI's pattern is now **"two distinct launch clusters (Apr 2-21 + Apr 30 / May 8 expanded); cluster 2 still rolling out 8+ days after launch, pacing variable."**

**Cumulative: 33 OpenAI ads across 7 batches, 0 with teardown-able copy.** Catalog-ads-only AI-lab pattern QUINTUPLE-confirmed across 5 active batches (1, 2, 3, 4, 7) with silence in 2 batches (5, 6).

### [[ro]] — 1 new ad (placeholder, breaks 5-batch silence)

From the digest:

- ID `1542915227491027`, started 2026-05-04, format unknown
- Body copy: `{{product.brand}}` — pure placeholder

**First Ro signal in 5 batches.** Last new Ro ad was batch 2 (2026-05-10). Cumulative Ro ads:

| Batch | Date | New Ro ads | Cumulative |
|---|---|---|---|
| 1 | 2026-05-06 | 1 | 1 (started 2026-04-14) |
| 2 | 2026-05-10 | 2 | 3 (started 2026-05-04, 2026-04-28) |
| 3 | 2026-05-11 | 0 | 3 |
| 4 | 2026-05-12 | 0 | 3 |
| 5 | 2026-05-14 | 0 | 3 |
| 6 | 2026-05-15 | 0 | 3 |
| **7** | **2026-05-16** | **1** | **4 (started 2026-05-04)** |

**All 4 Ro ads tracked across 7 batches are `{{product.brand}}` placeholders.** Pattern confirmed across the longest window in this farm — Ro's bare-"Ro" page name (or whichever page is matching) runs pure catalog-driven dynamic creative, never static narrative. The substantive Ro creative almost certainly lives on a different FB Page name not captured by the bare-"Ro" substring filter (Roman Health / Ro Body / Ro Health). The signal-return is **structurally identical to prior Ro signals** — no new teardown-able copy.

### [[anthropic]] — 0 new ads (2nd consecutive silence batch)

No new Anthropic ads. Cumulative remains **6 ads across 2 distinct launch windows** (Mar 16 – Apr 8 + 2026-05-11):

| Batch | Date | New Anthropic ads | Notes |
|---|---|---|---|
| 1 | 2026-05-06 | 5 | Initial wave |
| 2-4 | 2026-05-10 to 2026-05-12 | 0 | Silence trough |
| 5 | 2026-05-14 | 1 | 2026-05-11 launch (interpreted as new window) |
| 6 | 2026-05-15 | 0 | Silence #1 post-2026-05-11 |
| **7** | **2026-05-16** | **0** | **Silence #2 post-2026-05-11** |

**Two consecutive silent batches post-2026-05-11 strengthen the "standalone launch" hypothesis over "slow cluster."** The 2026-05-11 ad now reads as a single-entry launch, not the start of a cluster. Cumulative pattern: Anthropic runs **sparse, well-spaced** catalog launches (5 ads in window 1 + 1 ad in window 2), distinctly less aggressive than OpenAI's 8+1+21 = 30-ad volume across the same period.

### Other tracked brands — 0 new ads each

- **[[henry-meds]]** — never appeared (7th consecutive batch)
- **[[hampton-founders]]** — 0 new since 2026-05-06
- **DealMachine** — never appeared (7th consecutive batch)
- **Eden (telehealth)** — never appeared (7th consecutive batch); bare-"Eden" filter continues to produce only noise

## False positives ("brand-name match" noise) — 3 of 9 ads (33%)

Three noise pages this batch. Lowest noise rate since cold start.

### Sean Gracet Roset (1 ad) — NEW "Ro" substring noise

- ID `2042420463294529`, started 2026-04-14, format video
- Headline: *"FREE APP"*
- Body: *"Try the new AI photo trend now! Top 1 AI FREE App"*
- **Substring root cause:** "Ro" inside "Roset" (Sean Gracet Roset is presumably an AI app developer / creator brand)

**First AI/tech noise page matched via "Ro" substring.** Prior "Ro" noise was rooted in proper nouns (Roads & Kingdoms, KaRoL G, Lauren Brooks), compound brand names (Uproot Clean, BaBylissPRO, Builders Protein Bars), or plural nouns (Heirloom Roses). "Roset" as a personal/brand surname adds a new sub-pattern. Cross-substrate observation: the "AI photo trend" app category is at saturation (this is the second consumer-AI noise page matched via Apify after Adobe Acrobat in batch 3).

### Nissan of Hampton (1 ad) — Hampton substring noise

- ID `1951422105485988`, started 2026-04-03, format carousel
- Headline: *"{{vehicle.description}}"* — auto dealer dynamic-feed placeholder
- Body: *"💸 The ONE Place to Buy Used in Hampton Roads / 200+ affordable pre-owned vehicles / Nissan of Hampton is the Affordability Headquarters — where smart shoppers save big."*
- **Substring root cause:** exact "Hampton" in "Nissan of Hampton" / "Hampton Roads" (Virginia regional auto dealer)

**Adds to the cumulative Hampton noise corpus.** Prior Hampton noise pages: Hampton Inn, Hampton Roads Honda, Hampton Roads Transit, Hampton Sun, Classic Toyota Hampton, Hampton by Hilton, Visit Hampton VA, NAPA BDG South Hampton Roads, Hampton RV Trailer Sales, Hampton University Proton Cancer Institute, Hampton Roads Maritime Training System, Blake Hampton. **Nissan of Hampton is the 13th distinct Hampton regional-business noise page.** Pattern: every Hampton noise page is either a regional Virginia business or a Hilton sub-brand; none is the Hampton Founders peer-group community the farm intends to track.

### Eden Munoz (1 ad) — REPEAT noise page (also batch 3)

- ID `972253352461388`, started 2026-05-08, format carousel
- Body: `{{product.brand}}` — pure placeholder
- **Substring root cause:** exact "Eden" in "Eden Munoz" (Mexican banda singer; previously seen in [[ads-digest-2026-05-11]])

**Second batch this noise page surfaces** — confirms Eden Munoz is a multi-fire noise page (per-ad-ID dedup doesn't catch fresh creative from the same page). Cumulative "Eden" noise corpus tally updates: still 9 distinct brands, but multi-fire repeats are now Eden Brothers (×2 batches), Aelfric Eden (×2 batches), **Eden Munoz (×2 batches)**. Three "Eden" noise pages have multi-fired across non-consecutive batches.

## Cross-cutting patterns

### Seven-batch farm convergence table

| Batch | Fetched | New | Dedup-skipped | New % | OpenAI | Hims | Anthropic | Ro | Real-signal % |
|---|---|---|---|---|---|---|---|---|---|
| 2026-05-06 | 187 | 183 | 4 | 98% (cold start) | 21 | 45 | 5 | 1 | ~35% |
| 2026-05-10 | 190 | 22 | 168 | 12% | 3 | 2 | 0 | 2 | ~18% |
| 2026-05-11 | 196 | 6 | 190 | 3% | 3 | 0 | 0 | 0 | 50% |
| 2026-05-12 | 207 | 16 | 191 | 8% | 4 | 1 | 0 | 0 | 31% |
| 2026-05-14 | 202 | 13 | 189 | 6% | 0 | 2 | 1 | 0 | 23% |
| 2026-05-15 | 203 | 3 | 200 | 1.5% | 0 | 0 | 0 | 0 | 0% |
| **2026-05-16** | **208** | **9** | **199** | **4%** | **2** | **3** | **0** | **1** | **67%** |

Steady-state dedup is **92-98.5%** (band stays consistent at 95.7% this batch). New-ad volume **3-22 band** (mean ~10.6). Real-signal proportion **0-67% band** (new mean ~32%, mean noise rate ~68%). Batch 7's 67% signal rate is the highest of any batch since cold start — driven by the Hims surge (3) + OpenAI cluster expansion (2) + Ro signal return (1) hitting in the same fetch window.

### Hims surge-trough cadence confirmed

Hims' 7-batch creative-volume pattern now shows an **alternating surge-trough cadence**:

| Batch | New Hims ads | Wave state |
|---|---|---|
| 1 | 45 | Initial wave (cold start) |
| 2 | 2 | Trough |
| 3 | 0 | Trough |
| 4 | 1 | Light surge (Wegovy verbatim #1) |
| 5 | 2 | Surge (Wegovy verbatim #2 + Sex Rx Climax Control verbatim #1 — multi-wedge) |
| 6 | 0 | Trough |
| **7** | **3** | **Surge (Wegovy verbatim #3 + Sex Rx Climax Control verbatim #2 + 1 placeholder — multi-wedge mirrors batch 5)** |

The 5 → 6 → 7 sequence (surge → trough → surge) is the cleanest evidence yet that Hims' standing creative inventory cycles in waves — a wave ships 2-3 verbatim re-launches across multiple wedges, then 24-48hrs of trough, then the next wave. **Multi-wedge simultaneous re-launches in surge batches now confirmed across 2 of 2 surge batches (5 + 7).** This is the standing creative-operations pattern, not coincidence.

### OpenAI cluster pacing reframed

Batch 6 prematurely diagnosed the May 8 cluster as "fully dedup-cached at 6 ads." Batch 7's 2 new May 8 ads decisively disprove this. The corrected diagnostic methodology:

- **≥3 silent batches needed** for high-confidence cache-completion (not 2)
- **Cluster pacing is variable** — same campaign can have 4-ad-burst batches and 0-ad-trough batches between fresh entries
- **Catalog-feed sampling appears uneven** across the Apify actor's daily fetches — even if no new ads are launched, the actor may surface previously-unseen ads from the same launch date in later batches

**Updated cluster 2 timeline:** 8 ads (2026-04-30 + 2026-05-08 launches) across 4 active batches (3, 4, 7) with 2 silent batches in between (5, 6). Still open whether the cluster is fully exhausted at 8 ads or continues to expand in batches 8+.

### Ro placeholder pattern persists across longest window

Ro's 4-ad placeholder-only pattern is now confirmed across the full 7-batch window:

- All 4 ads ship `{{product.brand}}` body text (zero static narrative across 7 batches)
- 5-batch silence between batch 2 and batch 7 confirms Ro's bare-"Ro" page (whichever it is) runs sparse catalog creative — far less frequent than Hims or OpenAI
- The actual Ro narrative creative remains absent from this farm — strong evidence the bare-"Ro" filter is missing Ro's primary advertising FB Page name (Roman Health / Ro Body / Ro Health are the still-unfilter-tuned candidates)

### Hims placeholder ad joins the catalog-driven half

Batch 7's Hims placeholder ad (started 2026-04-08, ID `1316424053726023`) is the first individually-tracked Hims placeholder ad post-cold-start. Confirms Hims continues to ship **two parallel creative tracks**:

1. **Static-narrative template ads** — surge-trough cadence, verbatim re-launches, multi-wedge waves (Wegovy + Sex Rx + Hair Hybrids + Hard Mints)
2. **Catalog-driven placeholder ads** — `{{product.brand}}` body, dynamic-creative, presumably less attention-getting but higher-volume

The 26 batch-1 placeholders + 1 batch-7 placeholder establish Hims runs both tracks simultaneously — same dual-track strategy as Anthropic / OpenAI for the catalog half, but unique to Hims for the static-narrative half.

## Open questions

- **Is the OpenAI cluster 2 fully exhausted at 8 ads, or will batches 8+ surface more 2026-05-08 launches?** Batch 7's pacing-variability evidence makes either outcome plausible.
- **Will Hims' surge-trough cadence continue?** If batches 8+9 follow surge → trough → surge, the wave hypothesis upgrades from confirmed to systematic. If the next 3 batches are flat (all trough or all surge), the cadence is coincidence.
- **Is the 2026-05-11 Anthropic ad really standalone, or does a delayed cluster appear in batches 8+?** Two silent batches post-2026-05-11 favor "standalone"; one more silent batch (batch 8) would lock the diagnosis.
- **When does the bare-"Ro" filter break?** It's now produced 4 placeholder-only signal ads + 20+ noise ads across 7 batches. Page-ID allow-listing for Roman Health / Ro Body / Ro Health remains the unactioned fix.
- **Does batch 7's 67% signal rate represent a new high-water mark, or is it a single-batch outlier?** Three of seven batches now have ≥50% signal rate; four have ≤35%. Distribution has long tails on both ends.

## Related

- [[competitor-ads-farm]] — seventh batch from this farm; first batch with simultaneous surge from Hims (3 ads) + OpenAI cluster expansion (2 ads) + Ro signal return (1 ad)
- [[hims]] — 3 new ads (Wegovy verbatim #4, Sex Rx Climax Control verbatim #2, 1 placeholder); 2-wedge multi-instance verbatim surge mirroring batch 5
- [[ro]] — 1 new placeholder ad (breaks 5-batch silence, 4th Ro ad cumulative, all placeholders)
- [[openai]] — 2 new ads (May 8 cluster expands 6 → 8); disproves batch 6's "fully dedup-cached" diagnosis
- [[anthropic]] — 0 new ads (2nd consecutive silence batch post-2026-05-11; "standalone launch" hypothesis strengthens)
- [[concepts/dtc-telehealth-ad-template]] — Wegovy verbatim now 4 batches / 10-day stability; Sex Rx + Climax Control verbatim now 2 batches
- [[concepts/compounded-drug-disclaimer]] — Hims #3 disclaimer block ships verbatim across 2 batches with Sex Rx + Climax Control template
- [[ads-digest-2026-05-06]] — first batch (183 new, cold start, canonical Wegovy + Sex Rx Climax Control templates established)
- [[ads-digest-2026-05-10]] — second batch (22 new, Hard Mints + OpenAI catalog confirmation, last Ro signal before 5-batch silence)
- [[ads-digest-2026-05-11]] — third batch (6 new, Eden Munoz first appearance, OpenAI May 8 cluster opens with 2 ads)
- [[ads-digest-2026-05-12]] — fourth batch (16 new, Wegovy verbatim #1, OpenAI May 8 cluster expands to 6)
- [[ads-digest-2026-05-14]] — fifth batch (13 new, Hims two-wedge verbatim surge #1 — Wegovy + Sex Rx Climax Control)
- [[ads-digest-2026-05-15]] — sixth batch (3 new, 100% noise, universal silence, premature "OpenAI fully dedup-cached" diagnosis)

## Appears in

- Seventh entry in `wiki/sources/` for the competitor-ads farm. Reverses batch 6's universal-silence trough with the **highest real-signal rate (67%) in any post-cold-start batch**. Confirms Hims' surge-trough alternating cadence across 5 → 6 → 7 (surge → trough → surge with multi-wedge re-launches in both surge batches). Disproves batch 6's "OpenAI May 8 cluster fully dedup-cached at 6 ads" diagnosis (cluster now at 8 ads, still rolling out). Ro signal returns after 5-batch silence — fourth placeholder-only ad confirms the bare-"Ro" page name runs sparse catalog creative across the longest window in the farm. Wegovy GLP-1 verbatim template now spans 4 batches / 10-day stability window — strongest single-template stability evidence in the vault.
