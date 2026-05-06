---
title: Skill Systems
category: concept
summary: Composition discipline for Claude Skills — modular, focused skills chained into end-to-end automations as the alternative to "mega-skill" bloat; named by Simon Scrapes; the missing layer between authoring (one skill) and curation (which skills to install)
tags: [skill-systems, claude-skills, claude-code, composition, mega-skill, simon-scrapes, agentic-systems]
sources: 1
updated: 2026-05-06
---

# Skill Systems

## Definition

A **Skill System** is a set of small, focused [[claude-skills]] composed into an end-to-end business automation. Each skill stays narrow (one process, well-defined inputs and outputs); orchestration lives at a higher layer; skills compose like Unix tools rather than collapsing into one monolithic skill that tries to do everything.

The alternative — building a single "mega-skill" that handles a whole business process end-to-end — is named explicitly as the anti-pattern. Mega-skills are bloated, brittle, hard to debug, and resist reuse across processes that share sub-steps.

## Origin

Coined by [[simon-scrapes]] in [[youtube-digest-apify-2026-05-06]] #3 *THIS Gives Claude Skills a Massive Upgrade (It's Easy!)*. Implicit in earlier authoring-discipline content ([[code-with-beto]]'s "be concise," [[anthropic]]'s Skill Creator philosophy) but Simon Scrapes is the first to give the failure mode an explicit name and frame composition as its own discipline.

## The Skills discourse stratification

Skill Systems sits at the **composition layer** of an emerging stack:

| Layer | Question | Voices |
|---|---|---|
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] Skill Creator |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types of Skills + Skill Building Prompt Framework) |
| **Composition** | **How do skills chain into end-to-end automations?** | **[[simon-scrapes]] (Skill Systems)** |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

The composition layer was the missing rung; once it's named, the whole stack has a complete maturity model.

## Key claims (from [[simon-scrapes]] #3)

- **Most downloaded Claude skills are built for a single task** — mismatch with how real work is structured (sequences of connected processes)
- **Mega-skill anti-pattern** — the natural reaction to single-task limitations is one giant skill that does everything; this is bloated, brittle, and hard to reuse
- **Skill Systems = modular skills chained** — narrow scope per skill, well-defined I/O, orchestration at a higher layer
- **Composition unlocks reuse** — a properly modular skill ("send invoice", "draft email") plugs into 5+ end-to-end automations across the business
- **Real business problems need composition** — single-skill solutions hit a ceiling beyond toy demos

## Design heuristics (synthesized from #3 + cross-references)

- **Each skill = one process** — if your skill has multiple distinct verbs, split it
- **Inputs and outputs over side-effects** — the more stateless the skill, the more composable
- **Orchestration is its own layer** — don't bake the chaining into the skills; the chaining lives in slash-commands, sub-agents, or routines that *call* the skills
- **Reuse is the test** — if a skill only fits one chain, it's still too coupled; refactor until it composes into ≥2 chains
- **Composition aligns with Unix philosophy** — small, sharp tools that combine

## Examples in this vault

The user's own vault implements a Skill System:

- **Farmer skills** (`farmer/<name>.md`) — fetch from one source
- **Wiki-ingest skill** — process raw input into wiki pages
- **Wiki-query skill** — answer questions from the vault
- **Wiki-lint skill** — health-check the vault
- **Update_index / append_log scripts** — orchestration glue

Each skill is narrow and reusable; the `/wiki-ingest` slash command + Routines compose them into the end-to-end automation. This is a textbook Skill System per Simon Scrapes' framing — and likely the cleanest reference example in the vault.

## Contrasts with

- **Mega-skill** — the anti-pattern. One skill, many responsibilities, low reuse. Bloated context load, brittle behavior. Per [[dubibubii]] #5 in [[youtube-digest-apify-2026-05-05]]: *"500,000 skills on the market right now, and 95% are completely useless"* — mega-skill bloat is plausibly one mechanism behind the 95% number.
- **Sub-agent dispatch** — sub-agents are *dispatched workers* with their own context; Skill Systems use shared-context orchestration. Different mechanism, partially overlapping use cases. Sub-agents win when each step needs context isolation; Skill Systems win when steps share state and a tight feedback loop.
- **MCP server bundles** — MCP servers expose tools at the protocol level; Skill Systems compose at the procedural-knowledge level. Both are composition primitives but at different layers.
- **"Bundle skills as one plugin install"** ([[brock-mesarich]] pattern in [[youtube-digest-apify-2026-05-04]]) — *distribution* composition, not *runtime* composition. Brock bundles for friction reduction; Skill Systems compose for end-to-end behavior. Compatible, not redundant.

## Open questions / disagreements

- **Where does orchestration live?** Slash commands, sub-agents, Routines, or external scripts? Simon Scrapes' answer is unclear from the description — the 12:56 video probably names a specific orchestration substrate. Transcript ingest needed.
- **Granularity** — how narrow is "narrow enough"? Is "send invoice" the right unit, or "format invoice line items" + "render PDF" + "email file"? Probably workload-dependent.
- **Failure isolation** — when one skill in a chain fails, does the system halt, retry, or skip? Skill Systems framing is for happy-path composition; failure modes need their own treatment.
- **Cross-vendor** — does Skill Systems composition work the same way on [[codex]] (which now also has Skills per [[nate-herk]] #2)? Likely yes, but not confirmed.
- **Marketplace implication** — if Skill Systems is the right mental model, marketplace skills should be *components* not *complete solutions*. Most current marketplace skills are pitched as complete solutions — Skill Systems framing predicts a market shift.

## Why it matters for 3Ps

- **The technical pattern for productizing 3Ps deliverables.** Each consulting deliverable (lead-research, content-cascade, invoice-organization) becomes a small chained skill stack — explicitly *not* a mega-skill. This is the architectural answer for "how do I package my IP for repeated client engagements without a rewrite per client."
- **3Ps reference architecture**: client-onboarding skill → context-farming skill → wiki-ingest skill → wiki-query skill — the pattern is generic. Each skill is a sellable component; the chain is the deliverable.
- **Content angle**: most of the [[ai-consulting]] creator landscape teaches *one skill at a time* (the curation tier) or *one giant skill* (the demo tier). Teaching *Skill Systems* — composition discipline — is underserved educational content with direct relevance to consultant clients.
- **Defensive moat for 3Ps IP**: a competitor who copies one of your skills gets one component; the value is in the system + orchestration. Composition is harder to copy than authoring.

## Used in

- [[youtube-digest-apify-2026-05-06]] — primary source ([[simon-scrapes]] #3)
- [[simon-scrapes]] — primary author
- [[claude-skills]] — parent concept
- [[claude-code]] — substrate
- [[codex]] — likely-portable concept (Codex now has Skills too)
- [[ai-consulting]] — Skill Systems is the natural unit of consulting IP
- [[context-farming]] — this vault's farmer setup is a working Skill System
