---
title: Printing Press
category: concept
summary: A catalog of CLIs + a builder that converts "almost anything" into a CLI an agent can use efficiently; the packaged-product evolution of [[brad-bonanno]]'s "replace MCP with CLI" token-cost optimization argument; covered by [[nate-herk]] (52K views) — the most-viewed video in [[youtube-digest-apify-2026-05-10]] except #9 (session limits)
tags: [printing-press, cli, mcp, agent-tooling, claude-code, token-cost, claude-code-optimization]
sources: 1
updated: 2026-05-10
---

# Printing Press

## Definition

A **CLI catalog + builder** for AI agents — `printingpress.dev`, with companion repos at `github.com/mvanhorn/cli-print...` and `github.com/mvanhorn/printing-...`.

Two products in one:
1. **A catalog of ready-to-use CLIs** that agents can call directly (no MCP server required)
2. **A builder** that converts "almost anything into a CLI in minutes" — turning APIs, web tools, or undocumented surfaces into agent-callable command-line tools

Surfaced in this vault via [[youtube-digest-apify-2026-05-10]] #1 ([[nate-herk]] *This is The Most Powerful Tool to Give to Claude Code*, 52.2K views).

## The thesis

[[nate-herk]]'s framing: *"If you've ever watched MCPs eat your tokens for breakfast, this video shows why CLIs are the better path for agent setups."*

This is the **packaged-product evolution** of [[brad-bonanno]]'s [[mcp]]-vs-CLI argument from #19 in [[youtube-digest-apify-2026-05-03]]. The argument is the same; what's new is that someone built a tool that makes the conversion mechanical.

## CLI vs API vs MCP (the framing chapter at 1:35)

Three substrate options for agent tool access, with different cost/capability tradeoffs:

| Dimension | API | MCP | CLI |
|---|---|---|---|
| **Token cost per session** | Variable (depends on payload) | High (schema loaded every session) | **Low** (only invoked when called) |
| **Capability discovery** | Manual (read docs) | Automatic via MCP protocol | Manual (`--help` if exposed) |
| **Auth** | Per-API; varies | OAuth 2.1 standardized | Whatever the CLI does |
| **Execution model** | Network call | MCP server roundtrip | Local subprocess |
| **Best for** | Programmatic apps | Agentic microservices, well-defined tool catalogs | **Sites without APIs, token-sensitive setups** |

## Why CLIs win for token economics

- **MCP servers load capability schemas into every session** — even if you never call the tool, you pay the schema-load cost
- **CLIs are zero-cost when not invoked** — the agent only pays tokens for the actual command output
- **For a typical Claude Code stack with 10+ MCP servers**, schema bloat is the dominant per-session token cost (per [[brad-bonanno]] #19)
- **Replacing the worst MCP servers with CLI equivalents** routinely cuts session token cost by 30-60%

## Why CLIs win for sites without APIs (chapter at 7:48)

- Many tools have web UIs but no public API
- Browser automation (Playwright) gives access but is heavy
- A CLI wrapper around a scrape-and-action script gives the agent **API-like access without the API**
- Printing Press makes this conversion mechanical (the "build your own CLI in minutes" loop at 9:48)

## Sharing CLIs with your team (chapter at 11:45)

Distribution mechanic implied; specifics gated to transcript. Likely options:
- **Git-shared CLIs** — team repo of CLIs, installed via the Printing Press tool
- **Private catalog** — Printing Press as a marketplace with team-private CLI listings
- **Open catalog contributions** — public CLI listings in the canonical Printing Press catalog

If the distribution mechanic is well-built, Printing Press becomes a **competitive layer to MCP marketplaces** — the cost-optimized alternative for tool access.

## Where Printing Press fits in the [[plugins]] taxonomy

[[nate-b-jones]] #11 in the same digest names a 6-layer agentic-scaffolding map. Printing Press hits two layers:

- **Skills** — Printing Press CLIs are typically invoked from a Skill that knows when/why to call which CLI
- **MCPs (replaced)** — Printing Press is the *alternative* to deploying an MCP server for a given tool

The strategic positioning: Printing Press is **MCP for the cost-conscious tier** of the agentic-scaffolding stack.

## Implications for this vault

1. **Run a Context Audit on this vault** — identify the highest-cost MCP servers in `~/.claude/` and check whether Printing Press has CLI equivalents
2. **The `claude_ai_*` MCP servers** (Gmail, Calendar, Drive) are likely high-cost candidates — check whether Printing Press has Google Workspace CLIs
3. **The `firebase`, `supabase` MCPs** — heavy schema loads; may be CLI-replaceable
4. **`telegram` MCP** — already has rich official Bot API CLIs; potentially replaceable

## Why it matters for 3Ps

1. **Token-cost optimization is now a packaged deliverable** — clients ask "how do we cut Claude Code costs"; Printing Press is the answer with a tool, not just a methodology
2. **Concrete deliverable structure** — "audit your MCP servers, swap top 3 for Printing Press CLIs" is a 1-day engagement with measurable cost savings
3. **Cross-vendor argument** — Printing Press CLIs work for [[claude-code]], [[codex]], and [[hermes-agent]] — the optimization is substrate-agnostic
4. **Content angle** — comparing token costs of MCP vs CLI for canonical tools (Gmail, Slack, GitHub) is publishable benchmark content

## Open questions

- **Pricing** — is Printing Press free, freemium, or paid?
- **Catalog size** — how many CLIs ship out-of-the-box?
- **Build quality** — does the "anything to CLI" conversion produce robust CLIs or brittle wrappers?
- **Update / maintenance** — when target sites change, do Printing Press CLIs auto-update?
- **vs `mcp-cli-bridge` patterns** — is Printing Press the dominant tool, or one of several? Worth a search for alternatives.
- **Compatibility** — does Printing Press work with [[claude-code]] only, or also [[codex]] and [[hermes-agent]]?

## Related pages

- [[mcp]] — the substrate Printing Press optimizes against
- [[claude-code]] — primary deployment substrate
- [[claude-skills]] — orchestration layer that calls Printing Press CLIs
- [[plugins]] — the broader 6-layer scaffolding taxonomy
- [[brad-bonanno]] — earlier voice on the CLI-replaces-MCP argument
- [[nate-herk]] — primary creator covering Printing Press
- [[youtube-digest-apify-2026-05-10]] — primary citation
