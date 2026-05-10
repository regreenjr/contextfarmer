---
title: Claude Skills
category: concept
summary: Reusable procedural-knowledge units in Claude Code; the canonical packaging unit of 2026's AI-creator economy; curation videos hit ~80-135K views; skill-authoring has a 229K-view voice (Ben AI); composition discipline ("Skill Systems") named by Simon Scrapes; Skills also exist on OpenAI Codex (cross-vendor primitive); in 2026-05-10 [[nate-b-jones]] places Skills inside a 6-layer agentic-scaffolding taxonomy ([[plugins]]) and [[brad-bonanno]] names Skills as "the unlock" in his 13-product Anthropic tour
tags: [claude-skills, claude-code, agentic, anthropic, skills-marketplace, skill-authoring, skill-systems, composition, cross-vendor, codex, plugins, hermes-agent]
sources: 7
updated: 2026-05-10
---

# Claude Skills

Reusable procedural-knowledge units in [[claude-code]]. Each skill is a markdown file (typically with frontmatter + body + optional scripts/templates) that Claude invokes when its trigger conditions match. **The canonical official explainer** is [[anthropic]]'s *Claude Agent Skills Explained* (201K views, [[youtube-digest-apify-2026-05-03]] #4).

## What Skills are not (per [[anthropic]] #4)

- **Not CLAUDE.md** — CLAUDE.md is project-wide; skills are invoked situationally
- **Not MCP servers** — see [[mcp]]; skills are local procedural knowledge, MCP is remote tool/data access
- **Not sub-agents** — sub-agents are dispatched workers; skills are knowledge packages

The 2026 rule of thumb: **local procedure = Skill, remote service = MCP, dispatched specialist = sub-agent, project-wide context = CLAUDE.md.**

## Why it's a hot topic right now

[[youtube-digest-apify-2026-05-03]] surfaced **9 of 28** videos covering Skills directly:
- [[anthropic]] #4 — *Claude Agent Skills Explained* (201K, official explainer)
- [[code-with-beto]] #6 — *How to Create Good Agent Skills* (16K, authoring best practices)
- Confluent / Tim Berglund #9 — *Agent Skills or MCP in the era of Claude Code?* (175K, architecture)
- [[nate-herk]] #3 — *Build & Sell Claude Code Operating Systems* (86K, course-length)
- [[nate-herk]] #17 — *32 Tricks to Level Up Claude Code* (110K, includes skill tricks)
- [[nate-herk]] #25 — *I Tried 100+ Claude Code Skills. These 6 Are The Best* (47K, curation)
- [[grace-leung]] #1 — *Build Your Full AI Marketing Team (Agents + Claude Skills)* (222K, vertical app)
- Matt Maher #27 — *60 Seconds to Build a Claude Code Skill That Lasts Forever* (80K, intro)
- [[brad-bonanno]] #23 — *I Turned My Second Brain Into a Company Brain* (uses `/create-farmer` meta-skill)

Plus the prior digest [[youtube-digest-2026-05-03]] covered skills heavily.

The category has crossed from "early adopter only" to "explain-to-creators" mainstream awareness ([[greg-isenberg]]'s 266K-view explainer in the prior digest; [[anthropic]]'s 201K-view official explainer here).

## Authoring best practices ([[code-with-beto]] #6 + Anthropic #4)

1. **Don't write skills manually** — use Skill Creator (Anthropic-published meta-skill)
2. **Be concise** — skills load into context; bloat compounds
3. **Set degrees of freedom explicitly** — constrain skill behavior or it drifts
4. **Test different models** — skill behavior varies by model
5. **References folder** — supplemental material loaded only when needed (this vault uses `references/` and `.templates/`)
6. **Distribute via marketplace** — `claude-plugins-official`, community marketplaces, or per-team repo

## Composition discipline named — "Skill Systems" ([[simon-scrapes]] #3 in [[youtube-digest-apify-2026-05-06]])

[[simon-scrapes]] introduces the **composition layer** as a named discipline:

- **Mega-skill anti-pattern** — the natural failure mode of "one skill per business process"; skills become bloated, brittle, and resist reuse
- **Skill Systems = modular skills chained** — narrow scope per skill, well-defined I/O, orchestration at a higher layer (slash commands, sub-agents, Routines); skills compose like Unix tools
- **Reuse is the test** — a properly modular skill ("send invoice", "draft email") plugs into 5+ end-to-end automations

This fills the **missing rung** in the Skills discourse:

| Layer | Question | Voices |
|---|---|---|
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] Skill Creator |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types) |
| **Composition** | **How do skills chain into automations?** | **[[simon-scrapes]] (Skill Systems)** |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

Plausible explanation for [[dubibubii]]'s "500K skills, 95% useless" claim: most marketplace skills are mega-skills built without composition discipline. Skill Systems framing predicts a market shift toward components-not-solutions. → See [[skill-systems]].

## Skills as a cross-vendor primitive ([[nate-herk]] #2 in [[youtube-digest-apify-2026-05-06]])

[[nate-herk]]'s 1hr Codex full-course confirms **Skills exist on [[codex]]** (OpenAI's coding-agent CLI) too — the same procedural-knowledge primitive this vault has tracked as Anthropic-canon is now cross-vendor. The 26:44 chapter is "Building Reusable Skills."

Implications:
- The architectural concepts in this page **port** to non-Anthropic substrates
- "Skills" as a name is settling; once two competing CLIs ship the same primitive name, the abstraction is mature
- **Open**: are Codex Skills file-format-compatible with Claude Skills, or just conceptually parallel? Marketplace dynamics depend on the answer.
- **Open**: how does the [[brad-bonanno]] context-bloat optimization translate to Codex's metered API model vs Claude's flat-fee?

This page stays Anthropic-canon-focused; cross-link to [[codex]] for parallel-primitive details.

## Skills positioned in 6-layer agentic-scaffolding taxonomy ([[nate-b-jones]] #11 in [[youtube-digest-apify-2026-05-10]])

[[nate-b-jones]] names a 6-layer map of agentic scaffolding — see [[plugins]] for the full taxonomy. Skills sit at **layer 2**, between prompts (one-offs) and plugins (team-installable workflow bundles).

| Layer | Role | When to use |
|---|---|---|
| 1. Prompts | One-offs, exploration | Repeated workflows? — promote to skill |
| **2. Skills** | **House-style encoded across any LLM** | **Team-shared bundle? — promote to plugin** |
| 3. Plugins | Whole workflows your team can install | Smaller scope? — demote to skill |
| 4. MCPs / connectors | Live access to where work lives | Token-sensitive? — see [[printing-press]] |
| 5. Hooks | Deterministic events the model shouldn't handle | — |
| 6. Scripts | Deterministic logic the model shouldn't handle | — |

This is the **categorical map** above the existing authoring/composition/curation stack. Together:

| Layer | Question | Voices |
|---|---|---|
| **Taxonomy** | **What types of scaffolding exist?** | **[[nate-b-jones]] ([[plugins]])** |
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] Skill Creator |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types) |
| Composition | How do skills chain into automations? | [[simon-scrapes]] ([[skill-systems]]) |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

40% of operators' AI time is wasted putting work in the wrong layer (per [[nate-b-jones]] #11 title) — typically using a skill for what should be a plugin (over-stuffed) or a prompt for what should be a skill (re-tokens every use).

## Skills as "the unlock" ([[brad-bonanno]] #2 in [[youtube-digest-apify-2026-05-10]])

[[brad-bonanno]]'s 13-product Anthropic tour names Skills as **"the one feature that makes everything else dramatically better the moment you teach Claude how you actually want things done."**

Two voices, two frames, same conclusion:
- **[[ben-ai]]** (229K-view authoring frame): Skills are how you write one thing well
- **[[brad-bonanno]]** (operator frame): Skills are what unlocks the other 11 Anthropic products

For 3Ps client conversations: **Skills are the highest-leverage primitive** in the Claude product surface. If a client uses Claude without Skills, they're at ~2% of the platform's value (per Brad's framing).

## Skill-authoring discipline goes mainstream ([[ben-ai]] #7)

[[ben-ai]]'s *How to build Claude Skills Better than 99% of People* in [[youtube-digest-apify-2026-05-05]] is **229.7K views** — ~14x [[code-with-beto]]'s 16K and ~5x [[nate-herk]] #25's 47K. The highest-view authoring voice is now non-Anthropic, with his own framework competing with Anthropic's official Skill Creator:

- **3 Types of Skills** (chapter at 08:00) — *new framework*; types not yet enumerated
- **Skills vs Plugins** distinction (chapter at 06:20)
- **Planning & Context Engineering** as authoring discipline
- **Skill Building Prompt Framework** — meta-prompt for skill authoring

This puts authoring (not just curation) in mainstream-creator territory. The *Skill Creator vs Ben AI's Prompt Framework* fork is now real; transcript ingest needed to resolve specifics.

## Curation problem and emerging solutions

- **"Best of N skills" videos** are now an established format — implies skill abundance has outpaced user evaluation capacity. Three distinct curation philosophies are visible:
  - **Best-of-N from large sample** — [[nate-herk]] #25 ("6 of 100+ tested"), 47K views
  - **Curated essentials bundle** — [[brock-mesarich]] ("15 I can't live without"), 134.9K views — non-technical audience preference for "tell me what to install" over "here's how I evaluated"
  - **Mixed Skills + MCPs + repos** — [[dubibubii]] ("33 you actually need"), 78.9K views ([[youtube-digest-apify-2026-05-05]] #5) — broader stack-curation, not pure Skills
- **Market-size claim** ([[dubibubii]] #5): *"500,000 skills on the market right now, and 95% are completely useless."* First explicit number for the Skills ecosystem; if accurate, the curation-video format will only get more important.
- **Cross-curator consensus is forming** — Frontend Design + Superpowers + Context7 surface in three+ curation videos ([[nate-herk]] #25, [[brock-mesarich]], [[dubibubii]] #5). A small "must-install" core is emerging that 3Ps and others can use as a baseline client recommendation.
- **Skill marketplaces** are emerging:
  - `claude-plugins-official` (Anthropic-distributed)
  - Community marketplaces (e.g., `mksglu/context-mode`, `thedotmack/claude-mem`)
  - [[brad-bonanno]] is building a verified-skills marketplace (waitlist mentioned in #19, #23)
- **Single-plugin bundle distribution** ([[brock-mesarich]]) — packaging multiple skills as one plugin install; lowers friction for non-technical users vs per-skill installs. Different distribution philosophy from `claude-plugins-official`'s per-skill model.
- **Curation videos as discovery layer** — until marketplace ratings exist, creator curation is the de facto signal

## Top-rated skills surfaced (per [[nate-herk]] #25)

```
/plugin install skill-creator@claude-plugins-official
/plugin install superpowers@claude-plugins-official
npx get-shit-done-cc --claude --global
/plugin marketplace add mksglu/context-mode
/plugin install context-mode@context-mode
/plugin marketplace add thedotmack/claude-mem
/plugin install claude-mem
/plugin install frontend-design@claude-plugins-official
```
6 highlighted out of 100+ tested. Heuristic appears to be "boring + frequent" — the "simple, boring skills are the ones that actually sell" framing.

## Vertical applications

- **Marketing** ([[grace-leung]] #1) — 5-agent marketing team + 12 skills covering research/write/design/analyze, Notion task board integration, remote control via phone
- **Marketing skill-stack architecture** ([[grace-leung]] #2 in [[youtube-digest-2026-05-03-r3]]) — Brand Voice → Brand Design System → Campaign Planning → Carousel Design → Animated Motion → Campaign Manager Agent. Publishable as a reusable architectural template, not just a tutorial.
- **Knowledge management** ([[brad-bonanno]] #23, this vault) — context farmers + wiki ingest skills
- **Design** ([[claude-design]] integration via skills)
- **Development** ([[code-with-beto]]'s AI Tattoo App, $100 MRR demo)

## Why it matters for 3Ps

Skills are the canonical artifact for packaging consulting expertise:
- Methodology → skill
- Onboarding flow → skill
- Repeated client deliverable → skill
- Course content → skill bundle

The 3Ps consulting offering should ship skills, not just teach them. **Productization angle**: branded skill library + marketplace listing as paid product.

## Open questions

- **Anthropic's marketplace plans** — official paid marketplace coming, or stays GitHub-distributed indefinitely?
- **Usage / ranking metrics** — no public "most installed skills" data yet; whoever publishes this becomes the de facto curator
- **Skill rot** — as Claude Code APIs evolve, how often do skills break? Lint-style health checks for skill compatibility?
- **Cross-platform skills** — Skills are Code-only today; will they work in Claude.ai chat surface?

## Related pages

- [[claude-code]] — substrate
- [[codex]] — sibling substrate; Skills now cross-vendor
- [[skill-systems]] — composition layer; the missing rung between authoring and curation
- [[mcp]] — sibling primitive; see [[agent-skills-vs-mcp]] (planned comparison)
- [[voice-agents]] — newest application surface; voice-agent skill bundles likely next
- [[anthropic]] — vendor
- [[karpathy-llm-wiki]] — this vault's skills implement this pattern; `karpathy/autoresearch` is a related Karpathy skill surfaced via [[dubibubii]]
- [[context-farming]] — depends on farmer skills
- [[youtube-digest-apify-2026-05-03]], [[youtube-digest-2026-05-03]], [[youtube-digest-2026-05-03-r3]], [[youtube-digest-apify-2026-05-04]], [[youtube-digest-apify-2026-05-05]], [[youtube-digest-apify-2026-05-06]], [[youtube-digest-apify-2026-05-10]]
- [[plugins]] — categorical taxonomy layer above Skills (where Skills sit in the broader scaffolding map)
- [[hermes-agent]] — sibling substrate that ships its own Skills primitive
- Creators: [[code-with-beto]], [[nate-herk]], [[grace-leung]], [[brad-bonanno]], [[anthropic]], [[brock-mesarich]], [[ben-ai]], [[dubibubii]], [[simon-scrapes]], [[nate-b-jones]]
