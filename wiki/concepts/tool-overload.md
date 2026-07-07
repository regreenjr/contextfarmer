---
title: Tool Overload (The ~50-Tool Selection Ceiling)
category: concept
summary: [[tech-with-tim]]'s empirical curation thesis (*The Only Claude Code Plugins You Actually Need*, 5.2K views, 2026-07-06) — *"once Claude can see more than about **50 tools** at once, it starts picking the wrong ones, and your agent actually gets **worse, not better**"*; the failure mode is **tool-selection quality**, not just token cost, so the discipline is to **curate down to the tools that earn their spot** ([[plugins|plugins]] + [[mcp|MCP]] servers) rather than install everything; gives the vault its first explicit **tool-count-as-a-cost** argument — the empirical floor under [[nate-b-jones]]' *"wasting 40% on the wrong layer"* ([[plugins]]) and the selection-quality companion to [[brad-bonanno]]'s MCP-token-cost / CLI-replacement thesis ([[mcp]], [[printing-press]])
tags: [tool-overload, tech-with-tim, plugins, mcp, plugin-curation, fifty-tool-ceiling, tool-selection, context-pollution, claude-code, curation, tigerdata, github-mcp, context7, figma, frontend-design, cost-lever, selection-degradation]
sources: 1
updated: 2026-07-07
---

# Tool Overload

## Definition

[[tech-with-tim]]'s **tool-count-as-a-cost** thesis, from *The Only Claude Code Plugins You Actually Need* ([[youtube-digest-apify-2026-07-07]] #3, 5.2K views, 2026-07-06, 21:54):

> *"Everyone tells you to install as many Claude Code plugins and MCP servers as possible. Here's the problem: once Claude can see more than about **50 tools** at once, it starts picking the wrong ones — and your agent actually gets **worse, not better**."*

The core claim is a **selection-degradation ceiling**: loading more tools into an agent's context does not monotonically increase capability. Past a threshold (~50 tools, per Tim), too many similar options crowd the model's tool-selection decision, and accuracy *drops*. The prescribed discipline is to **curate down to the tools that genuinely earn their spot**, not to maximize the count.

## The failure mode — selection quality, not just tokens

This is distinct from the two cost arguments already in the vault:

| Argument | Cost paid | Source |
|---|---|---|
| **MCP token cost** — every MCP server loads its capability schema into context each session | Tokens / context budget | [[brad-bonanno]] ([[mcp]]), [[printing-press]] |
| **Wrong-layer waste** — putting work in a prompt when it should be a skill/plugin/hook | Operator time (~40%) | [[nate-b-jones]] ([[plugins]]) |
| **Tool overload** (this page) — too many tools crowd the *selection* decision | **Answer quality** — the agent picks the wrong tool | [[tech-with-tim]] |

The failure here shows up as **wrong-tool-picked**, a quality regression, not just a slower/pricier run. It's why "install everything" is actively harmful, not merely wasteful.

## The curated slate (the earn-their-spot set)

Tim's shortlist after going through the whole plugin marketplace + MCP ecosystem:

- **TigerData MCP** — database control from inside Claude (the sponsor)
- **GitHub MCP** — `github/github-mcp-server`
- **Context7** — `upstash/context7` library/docs MCP (this vault uses it)
- **Figma** — `claude.com/plugins/figma`
- **Frontend Design** — Anthropic first-party `anthropics/claude-code/plugins/frontend-design`

The slate is deliberately **short and read/build-side heavy** — the inverse of the maximalist-curation tier ([[dubibubii]]'s 33 tools).

## Where it sits in the vault

- **The empirical floor under [[plugins]]** — [[nate-b-jones]]' 6-layer taxonomy explains *which layer* work belongs in; tool-overload explains *how many* live tools you can afford before selection breaks. Together: right layer, bounded count.
- **A selection-quality lever alongside the cost levers** — joins [[mcp]] token-cost, [[printing-press]] CLI-replacement, [[prompt-caching]], and [[model-routing]] in the 2026 "keep your agent lean" cluster, but it's the only one whose payoff is *answer correctness* rather than *spend*.
- **Curation reframed** — the established "best skills / best MCPs" curation tier ([[nate-herk]], [[brock-mesarich]], [[zinho-automates]]) picks on *taste*; tool-overload adds a *hard ceiling* reason to prune: keeping a bad tool installed doesn't just waste tokens, it degrades every unrelated task's tool-pick.

## Why it matters for 3Ps

- **An audit deliverable** — "your Claude Code has 70 tools loaded; 45 of them are hurting selection accuracy" is a concrete, measurable engagement output (sibling to the [[plugins]] wrong-layer audit).
- **A default-config recommendation** — a curated ~5-10 tool baseline per client role is a defensible, low-friction optimization most teams won't discover themselves.
- **Content hook** — *"more tools made your agent worse"* is a counter-intuitive, sticky headline for the same audience the [[plugins]] "40% wasted" line targets.

## Open questions

- **Is the ~50 number a hard limit or a soft threshold?** Tim asserts it; whether it's a context-window artifact, a model-specific ceiling, or a general "too many similar options" effect is unverified against Anthropic docs.
- **Does the ceiling scale with the model / context window?** Larger context ≠ better tool selection necessarily; worth testing across Haiku / Opus 4.8 / [[claude-fable-5|Fable 5]].
- **Interaction with [[claude-subagents]]** — does delegating to subagents (each with a narrow tool set) sidestep the ceiling by keeping any single context under it?
- **Interaction with progressive tool disclosure** — if a harness only surfaces relevant tools per task, is the ceiling ever hit in practice?

## Related

- [[tech-with-tim]] — author
- [[plugins]] — the taxonomy this thesis prunes
- [[mcp]] — half the overload surface; the token-cost sibling argument
- [[printing-press]] — CLI-over-MCP packaged product; token-cost cousin
- [[claude-subagents]] — the delegation pattern that may sidestep the ceiling
- [[model-routing]] — fellow "keep the agent lean" discipline (model side vs tool side)
- [[claude-code]] — substrate where the ceiling bites
- [[dubibubii]] — the maximalist-curation counterpoint
