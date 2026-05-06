---
title: Hims
category: entity
summary: Hims & Hers Health — public DTC telehealth (NYSE:HIMS); 2026 creative engine spans three wedges (GLP-1 / hair-loss / Sex Rx) with 45 active FB ads in this vault's first competitor-ads batch; pioneers the compounded-drug-disclaimer + "$149/mo + $39 membership" pricing template
tags: [organization, dtc, telehealth, glp-1, compounded-drugs, hair-loss, sex-rx, competitor, hims]
sources: 1
updated: 2026-05-06
---

# Hims

## What it is

Hims & Hers Health, Inc. (NYSE: HIMS) — DTC telehealth platform. Founded 2017 (Andrew Dudum). Started as men's hair-loss + ED (Hims), expanded to women's wellness (Hers) and now broadly into weight loss / mental health / dermatology / primary care. 100%-online consultation → prescription → ship-to-door model.

## Why it matters for this wiki

Hims is the **direct competitor benchmark for [[medvi-positioning]]** — same business model, same compounded-GLP-1 / compounded-ED / compounded-hair playbook, far more advertising volume. The compete-page + creative-test backlog draws from Hims first.

Hims is also the **canonical 2026 case study** for compounded-drug DTC advertising: every wedge ships the same FDA-compounded-drug disclaimer boilerplate, and the pricing-page architecture (medication vs membership billed separately) is the structural template the rest of the category copies.

## Three creative wedges (2026-05)

From [[ads-digest-2026-05-06]] — 45 active ads, three product wedges:

### Wedge 1 — GLP-1 weight loss (FDA-approved Wegovy® partnership)

- **Product:** Wegovy® (Novo Nordisk) — FDA-approved, real GLP-1, prescribed by Hims providers
- **Pricing:** $149/mo medication + $39 first-month membership / $149 membership thereafter (steady-state ≈ $298/mo)
- **Headline claim:** *"Lose up to 25% of your body weight* with clinically proven options, including the new Wegovy® High Dose Pen"*
- **Disclaimer pattern:** Wegovy®/Zepbound®/KwikPen®/Foundayo™ trademarks attributed to Novo Nordisk / Eli Lilly with explicit non-affiliation disclaimers
- **Ad volume in 2026-05-06 batch:** ≥6 active variations
- **Notable:** Hims cites the actual Wegovy 7.2mg 72-week study (31.2% of adults achieved ≥25% weight loss; average 18.7%) — strong clinical-evidence framing vs compounded-only competitors

### Wedge 2 — Hair-loss "Hair Hybrids" (compounded oral + topical)

- **Product:** Hair Hybrids — compounded oral and topical minoxidil + finasteride combinations
- **Headline claim:** *"Don't wait — join the hundreds of thousands of guys who've found true results"* + *"Regrow in as few as 3-6 months"*
- **Disclaimer:** *"Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs."* + *"Individual results may vary. Based on separate individual studies of oral and topical minoxidil and finasteride."*
- **Ad volume in 2026-05-06 batch:** ≥10 active variations — the highest-volume wedge

### Wedge 3 — Sex Rx (compounded ED + climax + testosterone)

Three SKU variants, all compounded:

1. **3-in-1 Pill** — sildenafil + tadalafil + B12. *"Same active ingredients as Viagra® and Cialis®"* (with non-affiliation disclaimer for both trademarks)
2. **Sex Rx + Climax Control** — tadalafil + PE treatment. *"The 2-in-1 pill to get harder, and go longer."*
3. **Sex Rx + Testosterone Support** — tadalafil + zinc + L-arginine + B12 + B6. *"🔥New Sex Rx + Testosterone Support 🔥"*

All three include the standard compounded-drug FDA disclaimer.

## Creative-format observation

Of 45 Hims ads in the 2026-05-06 batch:
- 44 have `Format: unknown` in Apify metadata (likely catalog-driven dynamic creative)
- 26 have body text *only* `{{product.brand}}` — pure dynamic-creative placeholder, no static narrative
- 19 have static narrative copy — the templates documented above

Pattern: Hims runs **catalog-driven dynamic creative** for the bulk of ad volume, and a small set of static-narrative templates for the message work.

## Recurring copy patterns

Across all three wedges, Hims uses a **three-bullet structure** with a category-specific fourth-bullet substitution:

```
[Hook line]

Why Hims?
🏅 [Outcome / equivalence claim]
🧑‍⚕️ [Provider trust signal]  
📦 Free shipping (+ "discreet delivery" for Sex Rx only)

[Disclaimer]
```

→ See [[concepts/dtc-telehealth-ad-template]].

## Pricing structure (the "headline split")

Every Hims GLP-1 ad headlines *"Medication as low as $149/mo"* — but the membership is billed separately ($39 first month, $149 thereafter). Effective steady-state cost ≈ **$298/mo**. The headline-price split is the structural pricing trick of compounded/branded-GLP-1 DTC in 2026.

## Compliance language

Hims uses the canonical 2026 compounded-drug disclaimer template documented at [[concepts/compounded-drug-disclaimer]]. Variants by category:

- **Compounded GLP-1 / Sex Rx products:** *"[Product] is a compounded drug product. The FDA does not approve or verify compounded drugs for safety, effectiveness, or quality. This prescription product requires an online consultation with a healthcare provider who will determine if a prescription is appropriate. Restrictions apply. See website for full details and important safety information."*
- **Hair Hybrids:** *"Hair Hybrids are compounded products. FDA does not approve nor verify the safety, effectiveness, or quality of compounded drugs."*

## Related

- [[ro]] — direct competitor (Roman Health), included in same farm
- [[henry-meds]] — direct competitor (compounded GLP-1), included in same farm
- [[concepts/compounded-drug-disclaimer]] — Hims' template is the canonical reference
- [[concepts/dtc-telehealth-ad-template]] — three-bullet structural pattern
- [[ads-digest-2026-05-06]] — first source documenting Hims creative
- (Future) [[medvi-positioning]] — direct compete page when ingested

## Appears in

- [[sources/ads-digest-2026-05-06]] — 45 ads across three wedges

## Open questions

- What's Hims' compounded-GLP-1 SKU? (Wegovy is the FDA-approved partnership; do they also sell compounded semaglutide / tirzepatide for non-Wegovy-eligible patients?)
- Is the steady-state $298/mo a feature-page disclosure or buried at checkout? (Affects compete-page angle.)
- Why so many `{{product.brand}}` placeholder ads — is the catalog feed misconfigured or intentional dynamic creative?
- Does Hims run separate FB Page for women's brand (Hers)? (None appeared in this batch.)
