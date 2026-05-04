---
title: Claude Code
category: concept
summary: Anthropic's CLI/agent tool; April 2026 "Claude Code 2.0" landed; primary substrate for Skills, MCP, sub-agents, and Routines
tags: [claude-code, anthropic, agentic, cli]
sources: 1
updated: 2026-05-03
---

# Claude Code

Anthropic's CLI + agentic tool. The substrate that hosts Skills, MCP integrations, sub-agents, hooks, and (as of April 2026) Routines (scheduled tasks).

## Versions

- **Claude Code 2.0** — released ~April 2026. Headline framing in the wild: *"automate anything"* ([[jack-roberts]] coverage in [[youtube-digest-2026-05-03]]).

## Core primitives

- **Skills** — see [[claude-skills]]
- **MCP** — Model Context Protocol; lets Claude Code talk to external services
- **Sub-agents** — dispatched specialized agents (e.g. [[wiki-ingestor]])
- **Hooks** — event-driven shell commands configured via settings.json
- **Routines** — scheduled cloud-running agents (April 2026)
- **Slash commands** — user-invocable skill bindings (e.g. `/wiki-ingest`)

## Surface area in the YouTube creator space (per [[youtube-digest-2026-05-03]])

- Tier 1 (2M+ subs): Tech With Tim — *The Ultimate Claude Code Guide* (umbrella tutorials)
- Tier 2 (500K-1M): [[nate-herk]] — opinionated stacks ("Claude Code Operating Systems")
- Tier 2 (200K-500K): [[jack-roberts]], [[greg-isenberg]] — version coverage, mainstream awareness
- Tier 3 (100K-200K): [[grace-leung]] — vertical-specific (marketing) practitioner content

## Why it matters for 3Ps

Claude Code is the substrate for the entire 3Ps consulting offering. The wiki itself runs on Claude Code (Skills, sub-agents, slash commands). Tracking ecosystem shifts here = direct input to:
- Service offerings (what to teach)
- Tooling decisions (what to build)
- Content angles (what's mainstream vs. early)

## Open questions

- What did Claude Code 2.0 specifically add over 1.x? (Pull Jack Roberts' transcript)
- How are Skills + Routines + sub-agents *combined* in mature stacks? ([[nate-herk]]'s 2-hour course is the canonical reference candidate)

## Related pages

- [[claude-skills]]
- [[youtube-digest-2026-05-03]]
- [[nate-herk]], [[jack-roberts]], [[greg-isenberg]], [[grace-leung]]
