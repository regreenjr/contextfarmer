---
title: Claude Skills
category: concept
summary: Reusable procedural-knowledge units in Claude Code; the canonical packaging unit of 2026's AI-creator economy; "best of N skills" curation videos now mainstream
tags: [claude-skills, claude-code, agentic, anthropic, skills-marketplace]
sources: 4
updated: 2026-05-04
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

## Curation problem and emerging solutions

- **"Best of N skills" videos** ([[nate-herk]] #25, [[brock-mesarich]] in [[youtube-digest-apify-2026-05-04]]) are an emerging format — implies skill abundance has outpaced user evaluation capacity. Two distinct curation philosophies are visible:
  - **Best-of-N from large sample** — [[nate-herk]] #25 ("6 of 100+ tested"), 47K views
  - **Curated essentials bundle** — [[brock-mesarich]] ("15 I can't live without"), **134.9K views** — higher-view despite smaller channel; non-technical audience preference for "tell me what to install" over "here's how I evaluated"
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
- [[mcp]] — sibling primitive; see [[agent-skills-vs-mcp]] (planned comparison)
- [[anthropic]] — vendor
- [[karpathy-llm-wiki]] — this vault's skills implement this pattern
- [[context-farming]] — depends on farmer skills
- [[youtube-digest-apify-2026-05-03]], [[youtube-digest-2026-05-03]], [[youtube-digest-2026-05-03-r3]], [[youtube-digest-apify-2026-05-04]]
- Creators: [[code-with-beto]], [[nate-herk]], [[grace-leung]], [[brad-bonanno]], [[anthropic]], [[brock-mesarich]]
