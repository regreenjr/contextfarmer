---
title: Execution Layer
category: concept
summary: [[brad-bonanno]]'s 2026-05-14 framework — the second layer above a "second brain" that takes business context and runs real playbooks/SOPs to return *finished work*; sits above [[karpathy-llm-wiki]] / [[knowledge-layer]] / [[context-farming]] (all knowledge/context layers) and below the orchestration layer; concrete primitives are skills wired to the brain via reference (not hard-code), private team marketplace from a free GitHub template, sub-plugins for sales/ops/CS as the team grows, and a PR-back loop where every correction becomes a permanent upgrade across the company; "the new hire who joined yesterday is running on the back of every lesson your team has ever taught the skill"; in 2026-05-16 [[alex-mcfarland]]'s [[plugin-marketplace]] surfaces as the **build-walkthrough counterpart** to this deployment-pattern framework — Alex's video predates Brad's by 2 months (2026-03-16 vs 2026-05-14), suggesting Brad's [[execution-layer]] codified what Alex was already shipping
tags: [execution-layer, second-brain, company-brain, skills-marketplace, sub-plugins, pr-back-loop, brad-bonanno, claude-skills, context-farming, team-scaling, cross-vendor, plugin-marketplace, alex-mcfarland]
sources: 2
updated: 2026-05-16
---

# Execution Layer

## Definition

A second software layer that sits **above** an AI second brain and **runs the actual work**. The second brain holds context (sources, history, docs, decisions); the execution layer holds *playbooks, SOPs, and skills* that operate on that context to return finished work.

Named by [[brad-bonanno]] in *Build an Execution Layer for Your Second Brain (Step by Step)* (56 views, just-published 2026-05-14, [[youtube-digest-apify-2026-05-14]] #1).

## Origin

[[brad-bonanno]]'s product trajectory across three videos:

| Phase | Video | What it names | This vault implementation |
|---|---|---|---|
| 1 | [[youtube-digest-apify-2026-05-03]] #23 | [[context-farming]] (company brain) | `farmers/`, `/wiki-ingest`, raw/ → wiki/ |
| 2 | [[youtube-digest-apify-2026-05-10]] #2 | 13-product Anthropic surface tour | (Inventory reference) |
| 3 | **[[youtube-digest-apify-2026-05-14]] #1** | **Execution layer** | (Not yet implemented; this is the *productized output* of the wiki) |

The execution layer is the **productization layer above the wiki/farmer architecture** — what the user delivers to a team or client, not what the user maintains for themselves.

## The core claim (from [[brad-bonanno]] #1)

> "A second brain for your business isn't enough. Pointing Claude at a thousand interconnected docs gives it context, but context on its own doesn't ship the work. To actually run your business with AI you need a second layer: the execution layer. It takes everything your brain already knows about your company and runs your real playbooks and SOPs over the top to return finished work."

Architectural distinction:

| Layer | Holds | Reads | Writes |
|---|---|---|---|
| **Context layer** (second brain) | Sources, docs, decisions, history | Raw materials | Knowledge graph |
| **Execution layer** (this concept) | Playbooks, SOPs, skill definitions | Knowledge graph | **Finished work** |
| Orchestration layer (above) | Routing rules, triggers, schedules | Both layers | Activities + tasks |

## Concrete primitives ([[brad-bonanno]] #1)

### 1. Skills wired by reference, not hard-code

> "How to wire skills into the brain so context stays live (referencing beats hard-coding)"

Skills should *reference* the brain rather than embed context — when the brain updates, skills inherit. Same shape as the wiki's `[[wikilinks]]` over inline citation.

### 2. Private team marketplace from a free GitHub template

- "Spin up the marketplace from my free GitHub template in under five minutes"
- "Add your existing skills with one command"
- Free template at `github.com/bradautomates/comp...` (truncated — presumably `company-brain` or `company-execution`)

This is the **productization layer**. A single-operator skill set becomes a *team-distributable* skill marketplace via the template.

### 3. Sub-plugins for vertical functions

> "Scaffold sub-plugins for sales, ops and customer success as the team grows"

As the org scales, the marketplace decomposes into **vertical sub-plugins** — sales plugin, ops plugin, CS plugin. Each is its own composable set of skills. Same shape as [[skill-systems]] composition discipline, but at the *organizational* layer rather than the workflow layer.

### 4. The PR-back loop

The architectural innovation:

> "The PR-back loop turns every correction into a permanent upgrade across the whole company. By the end, the new hire who joined yesterday is running on the back of every lesson your team has ever taught the skill, and the quality lottery is gone."

How it works:
- A team member corrects a skill's output for their specific task
- The correction is committed as a PR against the team marketplace
- Future invocations of the same skill — for *any team member* — inherit the correction

This is **upstream propagation of leaf-level corrections** — same shape as `/wiki-ingest`'s entity-page update flow (a single new source updates all referencing pages).

## Why it matters

### Names a previously-implicit layer

Existing creator content covered:
- **Authoring** ([[code-with-beto]], [[ben-ai]], [[anthropic]] Skill Creator) — how to write one skill
- **Composition** ([[simon-scrapes]] [[skill-systems]]) — how to chain skills
- **Curation** ([[nate-herk]], [[brock-mesarich]], [[dubibubii]]) — which skills to install

[[brad-bonanno]] now names the **deployment / team-scaling** layer above all three. This is the missing operational rung between "I have a skill" and "my team uses skills."

### Maps cleanly onto 3Ps consulting deliverables

If the user's [[ai-consulting]] offering ships an "execution layer for your team":

- **Phase 1 deliverable**: implement context layer (wiki + farmer) — vault already does this
- **Phase 2 deliverable**: implement execution layer (skill marketplace + sub-plugins) — this concept names it
- **Phase 3 deliverable**: PR-back loop training (how the team makes the system improve) — operational handover

This is the **first clean three-phase consulting offer** that the [[ai-consulting]] wedge has produced in this vault.

### Validates the [[brad-bonanno]] product-evolution thesis

Three videos in five weeks, each adding the next layer. Brad's been incrementally describing **the same product** — a team-scalable second brain + execution layer + marketplace. The 2026-05 Skills Marketplace waitlist (`brad-b.kit.com/f9a7349a1c`, promoted across all three videos) likely launches as **a complete execution-layer system**, not just a skill marketplace.

### Cross-vendor framing

[[brad-bonanno]] explicitly says (chapter 4:01): *"Why This Works Across Every AI Tool."* The execution layer is vendor-agnostic — works on [[claude-code]], [[codex]], and likely [[hermes-agent]]. Same architectural symmetry as [[skill-systems]] / [[claude-skills]] / [[plugins]]. The IP is portable.

### The build-walkthrough counterpart ([[alex-mcfarland]] 2026-05-16)

[[alex-mcfarland]]'s [[plugin-marketplace]] (2026-03-16, resurfaced in [[youtube-digest-apify-2026-05-16]]) is the **build-walkthrough counterpart** to this concept's deployment-pattern framework:

| Angle | Author | What it gives | Date |
|---|---|---|---|
| **Deployment pattern** | [[brad-bonanno]] (this concept) | Architectural role + sub-plugins + PR-back loop + cross-vendor framing | 2026-05-14 |
| **Build walkthrough** | [[alex-mcfarland]] [[plugin-marketplace]] | Concrete `marketplace.json` + plugin folder structure + GitHub setup steps + builder-skill | 2026-03-16 |

Alex's video **predates Brad's by 2 months** — suggesting Alex was implementing what Brad later formalized. The two creators describe the same primitive from two angles: Brad gives the *architecture*, Alex gives the *build steps*. Together they form a complete plugin-marketplace stack.

[[brad-bonanno]]'s `github.com/bradautomates/comp...` template and [[alex-mcfarland]]'s "Plugin Marketplace Builder Skill" are presumably independent implementations of the same underlying primitive — worth diffing to see if there's a canonical schema emerging.

## Open questions

- **What's the actual artifact** of the free GitHub template? (Need to inspect repo to verify it implements what the description claims)
- **PR-back loop tooling** — manual git PRs, or is there a Brad-built automation that converts corrections to PRs?
- **Sub-plugin spec** — are sub-plugins just folder hierarchies of skills, or a different primitive?
- **Marketplace vs filesystem** — does the team marketplace require a hosted service (e.g. Anthropic Plugin Marketplace) or is it git/folder-based?
- **Sales-ops-CS taxonomy** — is this an arbitrary example, or a canonical org-shape the marketplace assumes?
- **Multi-tenant** — does the marketplace support multiple companies on one substrate (consulting use case) or is it single-org?

## Contrasts with

- **[[skill-systems]]** ([[simon-scrapes]]) — composition discipline *within* a workflow; execution layer is composition *across an organization*
- **[[claude-skills]]** unit — the building block; execution layer is the organizational deployment
- **[[plugins]]** taxonomy ([[nate-b-jones]]) — explains *where* a unit belongs; execution layer explains *how a team uses the units together*
- **[[context-farming]]** — feeds the second brain (input side); execution layer consumes the brain to produce work (output side)
- **Mega-skill anti-pattern** — execution layer explicitly avoids this via sub-plugin decomposition

## How it relates to this vault

This vault implements the **context layer** (Brad's Phase 1) thoroughly:
- `raw/` ingestion
- `wiki/` knowledge graph
- `/wiki-ingest`, `/wiki-query`, `/wiki-lint` operations

It does **not** implement the execution layer (Brad's Phase 3). The vault's skills (`/wiki-ingest`, `/wiki-query`) operate *on the brain* but don't yet have:

- A team marketplace
- Sub-plugin decomposition (the user is solo)
- A PR-back loop for skill corrections

**3Ps implication**: when productizing the vault for a client, the execution layer is the **net-new deliverable** above what the vault already does. The free template is worth cloning and diffing.

## Related pages

- [[brad-bonanno]] — primary author; this is his Phase 3
- [[alex-mcfarland]] — build-walkthrough counterpart ([[plugin-marketplace]])
- [[context-farming]] — his Phase 1 framework (input/context side)
- [[claude-skills]] — building blocks the execution layer composes
- [[skill-systems]] — composition discipline at the workflow layer
- [[plugins]] — taxonomy layer
- [[plugin-marketplace]] — distribution-layer artifact this concept deploys
- [[deployment-framework]] — runtime-selection sibling framework
- [[karpathy-llm-wiki]] — context layer architecture this builds on
- [[claude-code]] — primary substrate
- [[codex]], [[hermes-agent]] — cross-vendor compatibility per chapter 4:01
- [[ai-consulting]] — productization target for the [[brad-bonanno]] pattern
- [[youtube-digest-apify-2026-05-14]], [[youtube-digest-apify-2026-05-16]] — primary citations

## Used in

- [[youtube-digest-apify-2026-05-14]] — primary citation ([[brad-bonanno]] #1)
- [[youtube-digest-apify-2026-05-16]] — [[alex-mcfarland]] build-walkthrough counterpart
- [[brad-bonanno]], [[alex-mcfarland]] — primary authors
- [[ai-consulting]] — productization target
- [[claude-skills]] — deployment layer above authoring/composition/curation
- [[plugin-marketplace]] — sibling distribution-layer framework
