---
title: MCP (Model Context Protocol)
category: concept
summary: Open standard from Anthropic for connecting LLMs to external data and tools; in 2026, increasingly the right choice for agentic microservices, while local Claude Code work tilts toward Skills (or [[printing-press]] CLI alternatives); positioned in [[nate-b-jones]]' 6-layer agentic-scaffolding taxonomy ([[plugins]]) at layer 4; cross-curator favorites surfacing (Context7, Task Master, Playwright, Tavily, Codebase Memory)
tags: [mcp, model-context-protocol, anthropic, claude-code, claude-skills, agentic, integration, printing-press, plugins]
sources: 3
updated: 2026-05-10
---

# MCP (Model Context Protocol)

## Definition
**Model Context Protocol** — an open standard ([originally published by [[anthropic]]](https://modelcontextprotocol.io/)) for connecting LLMs to external data sources, tools, and APIs. Defines server/client protocol, capability discovery, transport (now `streamable HTTP`), and auth (`OAuth 2.1`). Implementations exist in multiple languages; ecosystem includes hundreds of community-maintained MCP servers (Slack, GitHub, GDrive, Postgres, Stripe, etc.).

## Origin
- **2024**: [[anthropic]] publishes the spec
- **2025-2026**: ecosystem growth; Tim Berglund's *Why MCP really is a big deal* lightboard (referenced in [[youtube-digest-apify-2026-05-03]] #9) becomes a canonical mainstream explainer

## Key claims (from [[youtube-digest-apify-2026-05-03]])

### What MCP gives you (Tim Berglund #9 + [[anthropic]] #4)
- Capability discovery — agents can introspect what a server offers
- Streamable HTTP transport — handles long-running tools cleanly
- OAuth 2.1 auth — production-grade security
- The Resource API has quietly declined; tools/prompts are the active surface

### MCP vs Skills (the canonical 2026 answer per Tim Berglund #9 + [[anthropic]] #4)
- **Skills** = local procedural knowledge; lighter weight; right for Claude Code tasks where the "skill" is "how to do this category of work"
- **MCP** = remote tool/data access; necessary for agentic microservices that can't be packaged as local procedure
- **Local coding agents** can lean on Skills + filesystem
- **Agentic microservices still very much need MCP** — Skills don't replace MCP for distributed/networked agent systems

### MCP in [[claude-code]] is double-edged
- **Cost**: MCP servers are token-expensive — they load capability schemas into context every session ([[brad-bonanno]] #19)
- **Fix**: replace MCP servers with CLI wrappers where the use case fits — get the tool access without the schema bloat
- This tension is the **canonical [[claude-code]] performance optimization** in 2026

### Strategic reframe ([[nate-b-jones]] #14)
- "MCP servers are not magic" — they're plumbing, not architecture
- The right architectural primitive is **interface principle**: many surfaces (editor, notes, browser, voice), one stack underneath
- MCP is part of the stack, not the stack itself

## Contrasts with
- **[[claude-skills]]** — see [[agent-skills-vs-mcp]] (planned comparison page); both are first-class; choice depends on whether work is local-procedure vs remote-microservice
- **CLI tools called from a skill** — emerging anti-pattern to MCP for token-cost reasons ([[brad-bonanno]] #19); CLI gives access without schema overhead
- **OpenAI function calling** — proprietary equivalent; MCP positioned as the open alternative

## Open questions / disagreements

- ⚠️ **MCP vs CLI** — [[brad-bonanno]] #19 advocates CLI replacements for cost; classic MCP advocacy treats this as an accident of immature tooling that will resolve. Open empirically.
- **MCP for non-Anthropic clients** — adoption outside Claude Code (GPT, Gemini, etc.) is happening but uneven; standard's openness vs proprietary ecosystems
- **Resource API decline** — Tim Berglund #9 notes this; what's the long-term replacement for "resource discovery" that isn't tool-based?
- **MCP marketplace** — none official yet; community-maintained registries; consolidation likely

## Why it matters for 3Ps

- **Substrate awareness**: every consulting deliverable that touches external systems will route through MCP or CLI-wrapped MCP
- **Cost framing**: clients optimizing Claude Code spend will need the MCP-vs-CLI conversation; high-leverage 3Ps content angle
- **MCP server inventory**: which MCP servers a client uses = direct map of their integration surface; useful diagnostic in any AI consulting engagement

## Curated MCP servers (2026-05 cross-curator surface)

[[dubibubii]]'s 33-tool curation in [[youtube-digest-apify-2026-05-05]] #5 surfaces a heavy MCP slate alongside Skills:

- **Context7** (`upstash/context7`) — library/docs MCP; this vault uses it
- **Task Master AI MCP** (`eyaltoledano/...`) — task orchestration
- **Playwright MCP** (`executeautomation/...`) — browser automation, also covered as a Skill in [[nate-herk]] #12
- **Tavily** (`tavily-ai/tavily-mcp`) — web search
- **Codebase Memory MCP** (`DeusData/codebase-...`) — code-context persistence

Cross-curator pattern: MCP picks are leaning toward **read-side servers** (docs, web search, codebase context) — exactly the surface where MCP's capability discovery + auth model justifies the schema-load cost vs CLI alternatives. The [[brad-bonanno]] CLI-replacement argument applies more to *write-side* MCP servers (Slack post, GitHub create-PR) where the action set is small and well-known.

Also notable: [[nate-herk]] #3's Higgsfield integration uses **MCP or CLI** (explicit either/or per the description), confirming the [[brad-bonanno]] either/or framing is now standard practice.

## CLI replacement shipped as packaged product ([[printing-press]] in [[youtube-digest-apify-2026-05-10]])

In [[youtube-digest-apify-2026-05-10]] #1, [[nate-herk]] (52.2K views) covers **Printing Press** — a catalog of CLIs + a builder that converts "almost anything" into a CLI an agent can use. The framing: *"if you've ever watched MCPs eat your tokens for breakfast, this is the better path."*

This is the **packaged-product evolution** of [[brad-bonanno]] #19's "replace MCP with CLI" optimization argument. Where Brad gave a methodology, Printing Press gives a tool that mechanizes the conversion.

Implication for this page: the **MCP-vs-CLI tension** has now shipped on both sides:
- **MCP-canonical side**: Anthropic's open spec + Tim Berglund's lightboard explainer
- **CLI-alternative side**: Brad's Context Audit + [[printing-press]]

Resolution per current best-practice: use MCP for **read-side, capability-discovery-heavy** servers (docs, search, codebase context); use CLIs (especially Printing Press CLIs) for **write-side, deterministic-action** tools (Slack post, GitHub create-PR, file ops). → See [[printing-press]].

## MCP positioned in 6-layer agentic-scaffolding taxonomy ([[nate-b-jones]] #11 in [[youtube-digest-apify-2026-05-10]])

[[nate-b-jones]] places MCP at **layer 4** of his 6-layer agentic-scaffolding map — between plugins (whole-workflow bundles) and hooks (deterministic events). Per his framing: MCPs and app connectors give "live access to where work lives." The "wrong-layer" failure mode here is **MCP for what should be a CLI / script** — a token-cost mistake that Printing Press is built to fix. → See [[plugins]].

## Used in
- [[youtube-digest-apify-2026-05-03]] — Tim Berglund #9, [[anthropic]] #4, [[brad-bonanno]] #19
- [[youtube-digest-apify-2026-05-05]] — [[dubibubii]] #5 (5 MCP servers in curated list); [[nate-herk]] #3 (Higgsfield MCP-or-CLI)
- [[youtube-digest-apify-2026-05-10]] — [[nate-herk]] #1 (Printing Press as packaged CLI alternative); [[nate-b-jones]] #11 (MCP in 6-layer taxonomy)
- [[claude-code]], [[claude-skills]] — concept relationships
- [[printing-press]] — CLI-alternative packaged product
- [[plugins]] — taxonomy layer where MCP sits
- [[knowledge-layer]] — likely connector layer between Pinecone Nexus / Microsoft Fabric IQ and Claude Code
- [[voice-agents]] — cal.com integration likely via MCP
- [[context-farming]] — MCP is the connector layer
- [[anthropic]] — author
- (Planned) [[agent-skills-vs-mcp]] — direct comparison page
