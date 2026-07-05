---
title: Design Skills (Claude Skills for Designers)
category: concept
summary: The **design vertical of [[claude-skills]]** — a coherent five-skill pipeline for designers named by [[griffin-wooldridge]] in *How to Use Claude Skills as a Designer* (**241K views**, 2026-03-09): **Frontend Design** (generate production front-end) → **Implement Design** (turn a design into working UI) → **Theme Factory** (systematic theming) → **Brand Guidelines** (enforce a brand system) → **Canvas Design** (lay out on a canvas). Four of the five map onto real first-party or community Claude skills (`frontend-design`, `brand-guidelines`, `canvas-design`, `theme-factory`). The highest-view single-vertical Skills video in the vault; the design-native counterpart to [[grace-leung]]'s marketing angle and distinct from [[claude-design]] (Anthropic's design *tool*).
tags: [design-skills, claude-skills, griffin-wooldridge, frontend-design, implement-design, theme-factory, brand-guidelines, canvas-design, designer-workflow, ux-design, product-design, claude-design, vertical-skills, high-view, skill-pipeline]
sources: 1
updated: 2026-07-05
---

# Design Skills (Claude Skills for Designers)

## What it is

The **design vertical of [[claude-skills]]** — a named, composable pipeline of five skills a working designer uses together inside one workflow, surfaced via [[griffin-wooldridge]]'s *How to Use Claude Skills as a Designer* (**241,333 views**, 2026-03-09, 9:30) in [[youtube-digest-apify-2026-07-05]]. This is the vault's **highest-view single-vertical Skills video** — the design-native counterpart to the generalist authoring/curation discourse and to [[grace-leung]]'s marketing angle.

Not to be confused with [[claude-design]] — that is Anthropic's design *tool* (generates design systems, decks, prototypes). **Design skills** are portable [[claude-skills|skill]] units a designer installs and runs.

## The five-skill pipeline

Griffin frames these as a workflow, not a menu — each stage hands off to the next:

| # | Skill | Job | Chapter | Source |
|---|---|---|---|---|
| 1 | **Frontend Design** | Generate production-grade front-end from a brief | 00:27 | `github.com/anthropics/claude-skills` (Anthropic first-party) |
| 2 | **Implement Design** | Turn an existing design into working UI code | 01:46 | `mcpservers.org/agent-skills/…` (community) |
| 3 | **Theme Factory** | Systematic theming / design-token generation | 03:17 | `mcpservers.org/agent-skills/…` |
| 4 | **Brand Guidelines** | Enforce a brand system across output | 04:09 | `mcpservers.org/agent-skills/…` |
| 5 | **Canvas Design** | Lay out / compose on a canvas | 05:36 | `mcpservers.org/agent-skills/…` |

Then **Create your own** (06:59, → [[skill-creator]]) and a **Demo** (08:11).

The pipeline reads as: **generate** (Frontend Design) → **implement** an existing design (Implement Design) → **theme** it (Theme Factory) → **constrain to brand** (Brand Guidelines) → **compose on canvas** (Canvas Design). Griffin's toolchain around them: Base44, Mobbin, Framer, Granola.

## Grounding — four of five are real installable skills

Four of the five map onto skills available in this environment, which grounds the video's claims in real artifacts rather than a curated wishlist:
- **Frontend Design** ↔ `frontend-design` (Anthropic first-party, anti-slop production frontend)
- **Brand Guidelines** ↔ `brand-guidelines`
- **Canvas Design** ↔ `canvas-design`
- **Theme Factory** ↔ `theme-factory`

Only **Implement Design** lacks an obvious first-party analog (community skill via `mcpservers.org`).

## Where it sits in the vault

- **The design cell of the [[claude-skills]] audience matrix** — alongside marketing ([[grace-leung]]), generalist curation ([[nate-herk]], [[brock-mesarich]]), authoring ([[chase-ai]], [[skill-creator]]), and beginner ([[tristen-obrien]], [[skill-leap-ai]]). Design was the missing vertical until this video.
- **A vertical-pipeline instance, not a curation list** — like [[skill-systems]] (composition) applied to a specific domain: five focused skills chained, not one mega-skill.
- **Distinct from [[claude-design]]** — the tool vs the skills; a designer might use both (the tool to generate, the skills to systematize).

## Why it matters for 3Ps

- **Vertical skill-pipelines are a productizable deliverable shape** — "here are the five skills your design team runs, wired to hand off to each other" is a concrete engagement artifact, more sellable than a generic "install these skills" list.
- **The design vertical is under-served** — most AI-creator Skills content is dev- or marketing-flavored; a design-team skill pipeline is a differentiation wedge.
- **241K views is demand proof** — the audience for domain-specific Skills pipelines is large and mainstream.

## Open questions

- **Are the community skills still current?** — the video is 2026-03-09; Implement Design / Theme Factory / Canvas Design may have moved or been superseded on `mcpservers.org`.
- **How much does the pipeline overlap with [[claude-design]]?** — where does the tool end and the skills begin in a real designer's workflow?
- **Is there a designer equivalent of [[skill-creator]]'s eval discipline?** — do design skills get acceptance-tested, or shipped on eyeball QA?

## Related

- [[griffin-wooldridge]] — the creator who named the pipeline (vault entry point)
- [[claude-skills]] — parent concept; this is its design vertical
- [[claude-design]] — Anthropic's design tool (distinct; the tool vs the skills)
- [[grace-leung]] — the marketing-vertical analog
- [[skill-systems]] — composition discipline; five chained skills is a domain instance
- [[skill-creator]] — the "create your own" underlying meta-skill

## Used in

- [[youtube-digest-apify-2026-07-05]] — [[griffin-wooldridge]]'s design-skills walkthrough (#2, 241K views) — vault entry point
