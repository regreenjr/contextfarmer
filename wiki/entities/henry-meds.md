---
title: Henry Meds
category: entity
summary: DTC telehealth — compounded GLP-1 + hormone therapy + sleep specialist; tracked competitor for Medvi positioning; first competitor-ads farm batch (2026-05-06) returned zero new ads — stub entity
tags: [organization, dtc, telehealth, glp-1, compounded-drugs, competitor, henry-meds]
sources: 1
updated: 2026-07-07
---

# Henry Meds

## What it is

Henry Meds — DTC telehealth platform specializing in compounded prescriptions. Founded 2021 (Jacobi Anstruther). Distinct from [[hims]] / [[ro]] in being **compounded-first** rather than expanding into compounded from a branded base — most public for compounded GLP-1 (semaglutide / tirzepatide) at lower price points than Hims' Wegovy partnership, plus hormone therapy and sleep medications.

## Why it matters for this wiki

Henry Meds is the **price-anchor competitor** in compounded GLP-1 — typically advertising semaglutide at sub-$300/mo all-in (vs Hims' steady-state $298/mo *just for the Wegovy partnership*). Direct competitor to [[medvi-positioning]] on both pricing and product mix.

## 2026-05-06 batch presence

From [[ads-digest-2026-05-06]]:
- **0 new ads** — Henry Meds did not appear in the 183-ad batch

Possible reasons:
- Brand-keyword "Henry Meds" too specific — FB Page may be "Henry" or "Henry Inc."
- Ads paused / between flights
- Apify search-URL params not returning Henry Meds page

## Action items

- → check Henry Meds' actual FB Ad Library page directly to confirm whether they're running ads
- → if active, tune [[competitor-ads]] farm to use the correct page-name match
- → flag for next batch (2026-05-07) to verify whether absence is structural or transient

## 2026-07-07 batch — first "Henry" collision (Dr. Henry Brown, urologist)

From [[sources/ads-digest-2026-07-07]] (batch 33): the "Henry" search term produced its **first-ever match in 33 batches — and it's a false positive.** The scraper surfaced **"Dr. Henry Brown,"** a board-certified urologist running a long-form direct-response BPH / enlarged-prostate funnel (*"If you're taking Flomax or Tamsulosin… you're on a ticking clock… I'm Dr. Henry Brown. Board-certified urologist… 19 years… TURP, HoLEP…"*), matched on the bare first name — **not** the compounded-GLP-1 telehealth Henry Meds. **Henry Meds itself remains absent for the 33rd consecutive batch.** This confirms the "brand-keyword too specific / page-match too permissive" open question below on the "Henry" axis: the term is as net-negative as bare "Ro"/"Eden"/"Hampton." Fix = **page-ID allow-listing the real Henry Meds page** (once located) + blocklisting the "Henry Brown" collision page. → [[competitor-ads-farm]].

## Related

- [[hims]] — direct competitor, the volume leader; Hims' Wegovy partnership is the FDA-approved counter-position to Henry's compounded approach
- [[ro]] — direct competitor
- [[concepts/compounded-drug-disclaimer]] — Henry Meds is almost certainly the most volume-exposed compounded-GLP-1 advertiser in the category
- [[ads-digest-2026-05-06]] — flagged as missing-from-batch
- [[sources/ads-digest-2026-07-07]]

## Open questions

- Is Henry Meds' actual FB ad volume large (and the search missed) or genuinely paused?
- How does Henry Meds' compounded-GLP-1 pricing compare to Hims' Wegovy + Medvi's price point?
- What disclaimer language does Henry Meds use vs the [[concepts/compounded-drug-disclaimer]] template Hims uses?
