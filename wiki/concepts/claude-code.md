---
title: Claude Code
category: concept
summary: Anthropic's CLI/agent tool; April 2026 "Claude Code 2.0" landed; primary substrate for Skills, MCP, sub-agents, Routines, hooks; canonical AI-creator topic of 2026
tags: [claude-code, anthropic, agentic, cli, claude-skills, mcp, routines]
sources: 2
updated: 2026-05-03
---

# Claude Code

[[anthropic]]'s CLI + agentic tool. The substrate that hosts [[claude-skills]], [[mcp]] integrations, sub-agents, hooks, and (as of April 2026) Routines (scheduled tasks).

## Versions

- **Claude Code 2.0** — released ~April 2026. Headline framing in the wild: *"automate anything"* ([[jack-roberts]] coverage in [[youtube-digest-2026-05-03]]).

## Core primitives

- **Skills** — see [[claude-skills]]
- **MCP** — see [[mcp]]; lets Claude Code talk to external services
- **Sub-agents** — dispatched specialized agents (e.g. [[wiki-ingestor]])
- **Hooks** — event-driven shell commands configured via settings.json
- **Routines** — scheduled cloud-running agents (April 2026); the scheduling primitive for [[context-farming]]
- **Slash commands** — user-invocable skill bindings (e.g. `/wiki-ingest`)
- **Plugins / marketplaces** — `claude-plugins-official` and community marketplaces; install path for skills like `skill-creator`, `superpowers`, `frontend-design`, etc. ([[nate-herk]] #25 in [[youtube-digest-apify-2026-05-03]])

## Surface area in the YouTube creator space

### Tier 1 (1M+ subs / mainstream)
- Tech With Tim — *The Ultimate Claude Code Guide* (umbrella tutorials)
- Sequoia Capital — hosted [[andrej-karpathy]] *Vibe Coding to Agentic Engineering* (550K views, biggest video in [[youtube-digest-apify-2026-05-03]])

### Tier 2 (200K-1M)
- [[nate-herk]] — opinionated stacks ("Claude Code Operating Systems", 2hr course); skill curation; Karpathy wiki implementation
- [[jack-roberts]] — version coverage, mainstream awareness
- [[greg-isenberg]] — mainstream-creator explainers
- [[anthropic]] official channel — *Claude Agent Skills Explained* (201K)

### Tier 3 (50K-200K)
- [[grace-leung]] — vertical-specific (marketing) practitioner content
- [[brad-bonanno]] — context-farming, second-brain, usage-limit optimization
- [[code-with-beto]] — skill authoring best practices
- Confluent Developer (Tim Berglund) — Skills vs MCP architectural framings
- [[nate-b-jones]] — analyst/strategy framings

### Tier 4 (<50K)
- Matt Maher — quick skill-builder demos
- [[tonbi-onchain-ai-garage]] — wiki implementation
- (vertical-specific creators emerging)

## Key 2026 patterns observed in [[youtube-digest-apify-2026-05-03]]

- **"Operating Systems"** framing ([[nate-herk]] #3) — opinionated stacks (Three Ms + Four Cs) bundling Skills, Routines, dashboards, LLM Wiki, Slack/email/calendar
- **Skill curation videos** (#25 *I Tried 100+ Claude Code Skills*) — too many skills exist for users to evaluate; curation is its own format
- **Skill-builder meta-skills** — Skill Creator (Anthropic), `/create-farmer` ([[brad-bonanno]]), generic patterns
- **Karpathy LLM Wiki implementations** — 5 videos this digest implementing the [[karpathy-llm-wiki]] pattern in Claude Code
- **Context bloat optimization** ([[brad-bonanno]] #19) — replace MCP with CLI, optimize CLAUDE.md, cut skill bloat, settings.json tuning
- **Playwright integration** ([[nate-herk]] #12) — browser automation as a skill
- **Tricks/hacks compilation videos** ([[nate-herk]] #17 *32 Tricks*) — the topic is mature enough for "shortcut" content

## Why it matters for 3Ps

Claude Code is the substrate for the entire 3Ps consulting offering. The wiki itself runs on Claude Code (Skills, sub-agents, slash commands, Routines). Tracking ecosystem shifts here = direct input to:
- Service offerings (what to teach)
- Tooling decisions (what to build)
- Content angles (what's mainstream vs. early)

## Open questions

- What did Claude Code 2.0 specifically add over 1.x? (Pull [[jack-roberts]] transcript)
- How are Skills + Routines + sub-agents + MCP *combined* in mature stacks? ([[nate-herk]]'s 2-hour AIOS course is the canonical reference)
- Plugin marketplace consolidation — Anthropic-official vs community-distributed; will Anthropic ship a paid marketplace?
- Token-cost optimization is now a skill ([[brad-bonanno]] #19 + Context Audit skill); is this temporary (will Anthropic fix it) or permanent (architecture issue)?

## Related pages

- [[claude-skills]] — primary primitive
- [[mcp]] — connector layer
- [[karpathy-llm-wiki]] — knowledge architecture pattern
- [[context-farming]] — automation pattern
- [[claude-design]] — sibling Anthropic product
- [[anthropic]] — vendor
- [[youtube-digest-apify-2026-05-03]], [[youtube-digest-2026-05-03]] — primary source digests
- Creators: [[nate-herk]], [[brad-bonanno]], [[code-with-beto]], [[grace-leung]], [[jack-roberts]], [[greg-isenberg]], [[nate-b-jones]], [[andrej-karpathy]]
