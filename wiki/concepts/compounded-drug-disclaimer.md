---
title: Compounded Drug Disclaimer
category: concept
summary: The canonical 2026 boilerplate language used by DTC telehealth advertisers (Hims, Ro, Henry Meds, Medvi) on FB/IG ads for compounded GLP-1, ED, hair-loss, and other compounded prescriptions; pioneered/standardized by Hims; 2026-05-10 adds a fifth Hims variant for chewable compounded products ("Hard Mints"); 2026-05-23 batch 10 extended Hair Hybrids disclaimer to 4-batch / 17-day stability window with 6 cumulative post-cold-start re-launches; batches 11+12 shipped zero disclaimer language (all-placeholder Hims run); **2026-05-28 batch 13 ships the Hair Hybrids disclaimer verbatim for the 7th time post-cold-start** (ID `1502428521462699` started 2026-05-14) — **BREAKS the 2-batch Hair Hybrids disclaimer silence (11+12)** so the wave does NOT close — **Hair Hybrids disclaimer wave remains OPEN** (the 11+12 silence was a single 2-batch trough); **Wegovy disclaimer remains structurally CLOSED** — now 5-batch silent (9+10+11+12+13); the canonical boilerplate language is unchanged across the silent batches (Hims simply stopped/resumed shipping ads carrying disclaimer language) — safe-baseline template stable for Medvi diff-targets
tags: [compounded-drugs, fda, compliance, ad-disclaimer, dtc, telehealth, hims, glp-1, hair-hybrids, surge-composition-rotation, hair-hybrids-disclaimer-returns, wegovy-disclaimer-wave-closed]
sources: 9
updated: 2026-05-28
---

# Compounded Drug Disclaimer

## What it is

The standardized disclaimer language placed at the bottom of DTC telehealth FB/IG ads for **compounded prescription drugs** — drugs prepared by a compounding pharmacy from bulk active ingredients rather than supplied as a manufacturer-branded product. The disclaimer is structurally required by:

1. **FDA framing** — compounded drugs are not FDA-approved (only the active ingredients are); ads must avoid implying FDA endorsement
2. **FTC truthfulness rules** — claims of efficacy must be qualified
3. **State pharmacy board scrutiny** — escalating in 2024-2026 as compounded-GLP-1 (semaglutide, tirzepatide) volume exploded post-shortage

## Canonical template (Hims, 2026-05)

From [[hims]]'s active 2026-05-06 ads ([[ads-digest-2026-05-06]]):

### Compounded GLP-1 / Sex Rx variant

> [Product name] is a compounded drug product. The FDA does not approve or verify compounded drugs for safety, effectiveness, or quality. This prescription product requires an online consultation with a healthcare provider who will determine if a prescription is appropriate. Restrictions apply. See website for full details and important safety information.

### Compounded hair-loss variant ("Hair Hybrids")

> Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs.
>
> *Individual results may vary. Based on separate individual studies of oral and topical minoxidil and finasteride.
>
> Prescription products require an online consultation with a healthcare provider who will determine if a prescription is appropriate. Restrictions apply. See website for full details and important safety information.

### Compounded chewable variant ("Hard Mints", added 2026-05-10)

From [[ads-digest-2026-05-10]]:

> Hard Mints is a chewable compounded product and has not been approved by the FDA. The FDA does not verify the safety or effectiveness of compounded drugs. Prescription products require an online consultation with a healthcare provider who will determine if a prescription is appropriate. Restrictions apply. See website for full details and important safety information.

Notable rewording vs the canonical pill variant:
- *"is a chewable compounded product"* (specifies form factor) vs *"is a compounded drug product"*
- *"has not been approved by the FDA"* (passive completed action) vs *"FDA does not approve or verify"* (active ongoing stance)
- *"FDA does not verify the safety or effectiveness"* drops "or quality" from the standard triad

Same legal substance, different phrasing. Suggests Hims runs **A/B variants of the disclaimer language itself** — likely behind a creative-test framework with legal sign-off on each phrasing variant. Worth considering when drafting [[medvi-positioning]] disclaimers: pick one phrasing and stick to it, or test variants within the legal-approved set.

## Required structural elements

A compliant compounded-drug disclaimer in DTC telehealth ads (per the Hims template) must include:

1. **Compounded acknowledgment** — "[Product] is a compounded drug product"
2. **FDA non-approval** — "FDA does not approve or verify compounded drugs for safety, effectiveness, or quality"
3. **Prescription requirement gate** — "requires an online consultation with a healthcare provider who will determine if a prescription is appropriate"
4. **Restrictions clause** — "Restrictions apply"
5. **Safety-info pointer** — "See website for full details and important safety information"
6. **Efficacy hedge (when efficacy claims appear)** — "Individual results may vary"
7. **Study disclosure (when study data referenced)** — "Based on separate individual studies of [ingredients]" — note: Hims' template uses "separate individual studies" specifically because the *combination* compounded product has no combined-form study; only individual-ingredient studies exist

## Why the structure matters

The Hims template is the **safe template** because each clause maps to an FTC/FDA risk:

- "FDA does not approve" — pre-empts misleading-endorsement claims
- "Provider will determine if appropriate" — pre-empts unauthorized-prescribing claims
- "Restrictions apply" — pre-empts blanket-availability claims
- "Individual results" — pre-empts uniform-efficacy claims
- "Separate individual studies" — pre-empts combined-product-efficacy claims when only individual-ingredient evidence exists

DTC telehealth ads that omit any of these are vulnerable to FTC consent-decree action (multiple 2024-2025 cases) and state pharmacy board complaints.

## Branded-trademark non-affiliation pattern

When a compounded ad mentions a branded equivalent (Viagra®, Cialis®, Wegovy®, Zepbound®), the disclaimer adds a **non-affiliation clause**:

> All trademarks are the property of their respective owners. Use of Cialis® and Viagra® do not imply endorsement or affiliation with Hims, Inc.

For Wegovy®/Zepbound®/KwikPen®/Foundayo™:

> Wegovy® is a registered trademark of Novo Nordisk A/S. Zepbound®, KwikPen®, and Foundayo™ are registered trademarks of Eli Lilly and Company. Hims & Hers Health, Inc. is not affiliated with or endorsed by Eli Lilly and Company.

Required because:
- Branded-trademark mention could imply affiliation/endorsement
- Compounded products are *not* the branded product (semaglutide ≠ Wegovy®)

## Why this matters for [[medvi-positioning]]

Medvi competes directly in compounded GLP-1 and other compounded telehealth categories. Mirroring the Hims disclaimer template (or a stricter variant) is **table stakes for FB/IG ad approval**, not a nice-to-have:

- Meta's ad-library moderation flags missing FDA-disclosure language on prescription-drug ads
- State pharmacy board complaints typically cite the absence of these specific clauses
- The Hims template represents 8+ years of FTC-tested DTC-pharma legal review

Medvi creative should default to the Hims template and only deviate with explicit legal sign-off.

## Related

- [[hims]] — canonical reference template
- [[ro]], [[henry-meds]] — peer competitors using mirrored language
- [[concepts/dtc-telehealth-ad-template]] — the three-bullet structural pattern that pairs with this disclaimer
- (Future) [[medvi-positioning]] — the page this concept feeds into
- [[ads-digest-2026-05-06]] — first source documenting the template

## Appears in

- [[sources/ads-digest-2026-05-06]] — 30+ Hims ads using the template (canonical variants)
- [[sources/ads-digest-2026-05-10]] — Hard Mints variant adds a fifth disclaimer phrasing for chewable compounded products
- [[sources/ads-digest-2026-05-16]] — Sex Rx + Climax Control disclaimer ships verbatim for the 2nd time (after batch 5) + Wegovy/FDA-approved disclaimer block ships verbatim for the 4th time (10-day stability window) — disclaimer language stability tracks parent template stability across the alternating surge-trough wave cadence
- [[sources/ads-digest-2026-05-20]] — Wegovy/FDA-approved disclaimer block ships **verbatim for the 5th time (14-day stability window — longest in the vault)** across 2 ad-library entries in the same batch + **Hair Hybrids disclaimer block ships verbatim re-launches for the first time post-cold-start** (2 ad-library entries) — disclaimer language stability now confirmed across **three wedges** (Wegovy/GLP-1 + Hair Hybrids + Sex Rx Climax Control); first time the Hair Hybrids "Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs" block surfaces in a non-cold-start batch
- [[sources/ads-digest-2026-05-22]] — **Hair Hybrids disclaimer ships verbatim 3 more times in one batch** (IDs `3372941842875795` started 2026-02-26 — oldest Hair Hybrids verbatim re-launch surfaced post-cold-start; `868992329557540` started 2026-05-06; `2498995467227011` started 2026-05-19). **5 cumulative post-cold-start Hair Hybrids disclaimer re-launches across batches 8+9 / 16-day stability window** spanning ~12 weeks of start dates. **Wegovy/FDA-approved disclaimer is SILENT in this batch** for the first time since the 4→5→7→8 verbatim rotation pattern was established — disclaimer language stability tracks **surge-composition rotation** between wedges (Hair-Hybrids-only in batch 9, Wegovy+Hair-Hybrids in batch 8, Wegovy-only in batches 4/5/7), not all-three-every-time
- [[sources/ads-digest-2026-05-23]] — **Hair Hybrids disclaimer ships verbatim for the 6th time** (ID `1302383031990848` started 2026-04-22). Hair Hybrids disclaimer now spans **4 batches / 17-day stability window** (1+8+9+10) with 6 cumulative post-cold-start re-launches; 3-consecutive-batch run (8+9+10) exceeds Wegovy on consecutive-batch count. **Wegovy/FDA-approved disclaimer 2nd consecutive silence batch (9+10)** — approaching but not at the ≥3-batch threshold.
- [[sources/ads-digest-2026-05-25]] — **ZERO Hair Hybrids disclaimer + ZERO Wegovy disclaimer** — first all-placeholder Hims batch since cold start (both ads ship `{{product.brand}}` placeholder body with no disclaimer block). **Hair Hybrids disclaimer FIRST SILENCE after the 3-consecutive-batch run (8+9+10)** — possible wave entering same closing pattern as Wegovy. **Wegovy disclaimer 3rd consecutive silence batch (9+10+11)** crosses the ≥3-batch methodology threshold — **Wegovy disclaimer language stability is structurally CLOSED**. Both wedges' verbatim disclaimer re-use simultaneously silent confirms disclaimer language stability tracks parent-template surge-composition; both surge waves may now be closing together. Open: does Hair Hybrids disclaimer return in batch 12+ (single-batch trough) or stay silent for 2+ more batches (wave-closing pattern matching Wegovy).
- [[sources/ads-digest-2026-05-26]] — **ZERO Hair Hybrids disclaimer + ZERO Wegovy disclaimer for the 2nd consecutive batch** — single Hims ad ships `{{product.brand}}` placeholder body with no disclaimer block (ID `1296851655896170` started 2026-05-22). **Batches 11+12 form the first 2-consecutive-batch all-placeholder Hims run** in the farm. **Wegovy disclaimer 4-batch silent (9+10+11+12)** extending the structurally-closed wave. **Hair Hybrids disclaimer 2nd consecutive silence (11+12)** — approaching the ≥3-batch wave-closure threshold; batch 13 silence would lock the Hair Hybrids disclaimer wave as structurally closed alongside Wegovy. The disclaimer-language stability pattern may be entering a quiet phase across all three Hims wedges (GLP-1 + Hair Hybrids + Sex Rx Climax Control all silent for verbatim re-use). **Open**: does Hair Hybrids disclaimer return in batch 13 (interpretation b — single-2-batch trough) or stay silent for 3+ batches (interpretation a — wave-closing pattern matching Wegovy's 4+5+7+8 → 9+10+11 silent shape). For Medvi creative: the canonical disclaimer template language remains stable (no edits to the boilerplate observed across the silent batches — Hims simply stopped shipping new ads carrying disclaimer language); the safe-baseline template is unchanged for Medvi ad-copy diff-targets.
- [[sources/ads-digest-2026-05-28]] — **Hair Hybrids disclaimer ships verbatim for the 7th time post-cold-start** (ID `1502428521462699` started 2026-05-14, full copy: *"Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs."* + *"Individual results may vary. Based on separate individual studies of oral and topical minoxidil and finasteride."* + prescription-gate + Restrictions + safety-info pointer). **BREAKS the 2-batch Hair Hybrids disclaimer silence (11+12)** — the wave does NOT reach the ≥3-batch wave-closure threshold, so the **Hair Hybrids disclaimer wave remains OPEN.** **Resolves the batch-11/12 open question in favor of interpretation (b): single 2-batch trough** — NOT wave-closing pattern matching Wegovy. **Wegovy disclaimer remains structurally CLOSED** — now 5-batch silent (9+10+11+12+13). Disclaimer-language stability tracks parent-template surge-composition: Hair Hybrids parent template returned this batch, so its disclaimer returned with it verbatim. **For Medvi creative**: the canonical boilerplate is confirmed unchanged across the 2-batch silence — Hims resumed shipping the identical disclaimer language with no edits; the safe-baseline template is stable for Medvi ad-copy diff-targets. **Note**: the 2 returning "Cholesterol" noise narratives this batch (Cholesterol Relief Community + Cholesterol Support Group) are statins-skepticism long-form confession ads — NOT compounded-drug telehealth — and carry no compounded-drug disclaimer (they're supplement / lifestyle direct-response, a different compliance regime).

## Open questions

- Do Henry Meds and Ro use exactly Hims' template or have material variations? (Need next batches to confirm.)
- Has the FTC issued any 2025-2026 guidance specifically on compounded GLP-1 advertising that would update the template?
- What's the equivalent disclaimer language for non-compounded telehealth (branded Wegovy, branded Cialis prescribed via telehealth) — does the "FDA does not approve" clause flip to something else?
