---
title: Claude for Small Business
category: concept
summary: Anthropic-shipped vertical plugin installed directly into the Claude desktop app, pre-wired with **connectors** (QuickBooks / Xero / Stripe / PayPal / Square / HubSpot / Gmail) and **~30 pre-built skills** mapped to SMB jobs-to-be-done (Monday brief / call list / plan payroll / close month / handle complaint / run campaign / Friday brief / quarterly review / CRM maintenance / invoice chase + ~20 more); the `/smb-onboard` command is a [[skill-creator]]-shape meta-skill that customizes every skill in the pack to the user's business / industry / headcount / tools; the **first Anthropic-shipped vertical plugin** in this vault and the canonical "skills as packaged product" instantiation — confirms the [[claude-skills]] / [[plugin-marketplace]] / [[execution-layer]] roadmap is shipping as Anthropic-owned vertical plugins, not just community marketplaces
tags: [anthropic, claude, smb, small-business, plugin, vertical-plugin, claude-skills, connectors, mcp, quickbooks, xero, stripe, paypal, square, hubspot, gmail, smb-onboard, meta-skill, claude-for-small-business, vertical-ai, brad-bonanno]
sources: 1
updated: 2026-05-22
---

# Claude for Small Business

## What it is

A first-party [[anthropic]] plugin (announced May 2026) that installs into the Claude desktop app and ships with two bundled artifacts:

1. **Connectors** (MCP servers) pre-wired for: QuickBooks, Xero, Stripe, PayPal, Square, HubSpot, Gmail, and "the rest of the stack a small business actually runs on"
2. **~30 pre-built skills** mapped to the recurring SMB jobs-to-be-done

Distribution surface: **Claude desktop app**. Install time: **under three minutes** (per [[brad-bonanno]]).

## Why it matters for this wiki

**First Anthropic-shipped vertical plugin tracked in this vault.** Until this batch, Anthropic's product surface ([[brad-bonanno]] 13-product tour) was **horizontal** — Claude Code, Claude Skills, Claude Design, Claude Chat, MCP, Cowork, etc. all generic primitives that any vertical could compose. Claude for Small Business is the **first vertical-targeted, opinionated, pre-composed product** Anthropic has shipped.

Strategic implication: the [[execution-layer]] / [[plugin-marketplace]] / [[claude-skills]] roadmap is shipping **as Anthropic-owned vertical plugins**, not just as a marketplace for community plugins. Anthropic is verticalizing.

## The ~30 pre-built skills

Per [[brad-bonanno]]'s 2026-05-21 walkthrough — partial list (specifics gated to Brad's Small Business Skills Guide):

| Skill | What it does |
|---|---|
| **Monday brief** | Synthesizes financials + settlements + deals + calendar into a one-page weekly plan |
| **Call list** | Ranks top 5 leads worth calling today (lead-scoring synthesis) |
| **Plan payroll** | Per-pay-period scheduling/calculation |
| **Close month** | Books closing automation |
| **Handle complaint** | Customer-complaint workflow with tone-matched response |
| **Run campaign** | Marketing-campaign launch with tracking setup |
| **Friday brief** | End-of-week roll-up |
| **Quarterly review** | QBR generation from financials + ops data |
| **CRM maintenance** | Auto-logs meetings to HubSpot (and equivalents) |
| **Invoice chase** | Tone-matched follow-ups; **skips customers who already paid** |
| (~20 more) | (specifics gated to transcript / Brad's Small Business Skills Guide) |

**Pattern**: each skill is **a recurring SMB owner task** — Monday brief is a weekly job, close month is monthly, QBR is quarterly. The skill cadence maps onto the **operator's natural calendar**.

## The `/smb-onboard` meta-skill

The most architecturally significant primitive in the bundle. `/smb-onboard` is a **[[skill-creator]]-shape meta-skill** — it doesn't *do* a task, it **rewrites every skill in the pack** to fit the user's:
- Business name + description
- Industry
- Headcount
- Tools (which connectors to wire vs swap)

After `/smb-onboard` runs, each skill in the 30-skill pack is customized — the Monday brief synthesizes from *the user's* HubSpot/QuickBooks/Calendar, not from a generic template; invoice chase uses *the user's* tone-of-voice patterns.

**Significance**:
- **Meta-skills are now an Anthropic-shipped product category**, not just a community pattern ([[skill-creator]], [[ai-labs]]' Skillify, [[alex-mcfarland]]'s Plugin Marketplace Builder)
- The onboarding flow is **the productized version** of the consulting "discovery → customize → deploy" cycle
- This is the **first Anthropic-shipped customization-by-onboarding meta-skill** — competitive pressure on every consulting deliverable that follows the same shape

## Connector flexibility

Per Brad: if the stack isn't covered out-of-box, **connectors can be swapped post-install** (e.g., Xero instead of QuickBooks). The connector layer is pluggable [[mcp]]-style — the bundled connectors are the **default kit**, not a hard requirement.

This is the **first explicit Anthropic-shipped MCP-connector kit** in this vault. Confirms MCP-as-distribution-surface for vertical products.

## Relationship to other vault concepts

### vs [[plugin-marketplace]] ([[alex-mcfarland]])

| Plugin Marketplace ([[alex-mcfarland]]) | Claude for Small Business |
|---|---|
| User-built, GitHub-hosted | Anthropic-built, desktop-app-installed |
| Empty marketplace structure ready for skills | Pre-loaded with 30 skills |
| Horizontal — works for any vertical | Vertical — SMB-specific |
| Free / Substack-gated | Anthropic-distributed |

**Both ship in 2026-Q2** within ~10 weeks of each other. Suggests Anthropic and community-builders are **converging on the same distribution layer** from opposite ends.

### vs [[execution-layer]] ([[brad-bonanno]])

[[brad-bonanno]]'s [[execution-layer]] is the **deployment-pattern framework** (skill marketplace + sub-plugins for sales/ops/CS + PR-back loop). Claude for Small Business is **Anthropic's vertical-plugin instantiation** of that pattern. Brad's framework predates the Anthropic product by 1 week.

Open question: does Anthropic's launch **preempt** [[brad-bonanno]]'s skills-marketplace roadmap, or does Brad pivot to **execution layer for sub-SMB or mid-market** verticals not yet covered by CFSB?

### vs [[ai-consulting]] / [[chief-ai-officer]]

CFSB **automates the most common 30 SMB workflows out of the box**. This compresses the **per-engagement value of [[ai-consulting]] for SMBs** — what used to be a multi-week customization engagement is now a `/smb-onboard` command.

3Ps positioning implication: **SMB consulting wedge gets compressed**. The remaining value lives in:
- Industries not covered by CFSB defaults (specialty verticals)
- Mid-market and above ([[chief-ai-officer]] territory)
- Custom skills beyond the 30-pack
- Tuning the meta-skill output (CFSB is opinionated; some SMBs want different opinions)

### vs [[claude-skills]]

CFSB is **the canonical "skills as packaged product" instantiation**. Where [[claude-skills]] has been a primitive + a curation/authoring conversation, CFSB demonstrates **what a finished skills product looks like** — 30 opinionated, pre-composed, pre-connected skills with onboarding.

This is the **pattern other vertical plugins will follow** — Claude for Retail / Claude for Legal / Claude for Healthcare are predictable future-batch products.

## Strategic significance

1. **First Anthropic vertical-plugin product** — confirms verticalization is the 2026-Q2 strategy. Validates the [[brad-bonanno]] Phase-3 [[execution-layer]] roadmap from inside Anthropic.
2. **The 30-skill pack is the canonical "skills product" reference implementation** — every future vault analysis of vertical-AI products will reference CFSB.
3. **`/smb-onboard` is the first Anthropic-shipped customization-by-onboarding meta-skill** — productizes the consulting "discovery → customize → deploy" cycle. Compresses SMB consulting wedge.
4. **MCP-connector pre-bundling** confirms MCP-as-distribution-surface for vertical products — connectors are the new "import templates from your tools" surface
5. **Pairs with [[chief-ai-officer]]** (Nate Herk #4 same batch) — CFSB for SMBs, CAIO for mid-market. Same demand curve, two product wedges at different company sizes.
6. **Open: will Anthropic ship sibling vertical plugins?** (Claude for Retail / Claude for Healthcare / Claude for Legal). The methodology is now demonstrated; the next launches are scaling questions.

## Used in

- [[youtube-digest-apify-2026-05-22]] — primary citation ([[brad-bonanno]] #7 walkthrough)
- [[brad-bonanno]] — Phase 4 of product trajectory (covering Anthropic-shipped vertical plugins)
- [[anthropic]] — first vertical-plugin launch
- [[claude-skills]] — 30-skill instantiation
- [[plugin-marketplace]] — Anthropic-shipped sibling
- [[execution-layer]] — deployment-pattern framework that CFSB instantiates
- [[skill-creator]] — `/smb-onboard` is a skill-creator-shape meta-skill
- [[mcp]] — connector layer
- [[ai-consulting]] — SMB consulting wedge gets compressed
- [[chief-ai-officer]] — sibling for mid-market

## Open questions

- **Full skill list** — what are the remaining ~20 skills?
- **Pricing** — is CFSB included in standard Claude subscriptions, or a paid add-on?
- **Connector roadmap** — which connectors are coming next (NetSuite, Salesforce SMB, Shopify, FreshBooks)?
- **`/smb-onboard` internals** — how does it actually rewrite the skills? Template substitution, full regeneration, or hybrid?
- **Sibling vertical plugins** — Claude for Retail / Claude for Legal / Claude for Healthcare in roadmap?
- **Open-source the 30-pack?** — Or is this Anthropic-proprietary?
- **Industry coverage in `/smb-onboard`** — which verticals are well-served vs poorly-served by the default opinionated skills?
