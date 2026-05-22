---
title: MCP (Model Context Protocol)
category: concept
summary: Open standard from Anthropic for connecting LLMs to external data and tools; positioned in [[nate-b-jones]]' 6-layer agentic-scaffolding taxonomy ([[plugins]]) at layer 4; **in 2026-05-19 placed as Layer 1 of [[nate-b-jones]]' new [[agent-protocol-stack]]** (six protocols / three that matter: MCP + A2A + AG-UI) — answering the **"what can my agent access?"** question; also **reframed as a security boundary** (chapter 4:50 of #6) — MCP servers are the natural action-boundary instrumentation point, extending [[agent-security]]' judge-architecture pattern at the protocol layer; **also serves as the connector-distribution surface for [[claude-for-small-business]]** (QuickBooks/Xero/Stripe/HubSpot/Gmail connectors pre-bundled) — first explicit Anthropic-shipped MCP-connector kit
tags: [mcp, model-context-protocol, anthropic, claude-code, claude-skills, agentic, integration, printing-press, plugins, agent-protocol-stack, security-boundary, action-boundary, claude-for-small-business, connectors, a2a, ag-ui, six-protocols]
sources: 4
updated: 2026-05-22
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

## MCP as Layer 1 of [[agent-protocol-stack]] ([[nate-b-jones]] in [[youtube-digest-apify-2026-05-22]])

[[nate-b-jones]]'s 13th framework places MCP as **Layer 1 of the 6-protocol agent stack**:

| Protocol | Layer | Status | Sponsor |
|---|---|---|---|
| **MCP** | **Tool + data access** | **Settled** | [[anthropic]] |
| A2A | Agent-to-agent delegation | Settled | Google |
| AG-UI | Agent-to-human supervision | Settled | Google |
| A2UI / AP2 / x402 | UI / payment layers | Contested | Multiple |

MCP answers the first of the **three questions agents must answer**: *"what can I access?"*

**MCP as security boundary** (chapter 4:50 of [[nate-b-jones]] #6): MCP servers are the **natural action-boundary instrumentation point** — same reframe as Lindy's outbound-mail judge from [[nate-b-jones]] 2026-05-12. The judge sits at the MCP-server perimeter; MCP servers gate the action; the protocol carries the auditability surface. This is **the missing protocol-layer-level extension of [[agent-security]]'s judge architecture** — judges are deployed at MCP perimeters.

## MCP as connector-distribution surface ([[claude-for-small-business]] in [[youtube-digest-apify-2026-05-22]])

[[anthropic]]'s [[claude-for-small-business]] vertical plugin pre-bundles **MCP connectors** for QuickBooks / Xero / Stripe / PayPal / Square / HubSpot / Gmail. This is the **first explicit Anthropic-shipped MCP-connector kit** in this vault — confirms MCP-as-distribution-surface for vertical products.

The connector layer is **pluggable** — bundled connectors are defaults, not requirements (Xero swapped for QuickBooks etc post-install). Same pattern likely repeats for future Anthropic vertical plugins (Claude for Retail / Healthcare / Legal).

## Used in
- [[youtube-digest-apify-2026-05-03]] — Tim Berglund #9, [[anthropic]] #4, [[brad-bonanno]] #19
- [[youtube-digest-apify-2026-05-05]] — [[dubibubii]] #5 (5 MCP servers in curated list); [[nate-herk]] #3 (Higgsfield MCP-or-CLI)
- [[youtube-digest-apify-2026-05-10]] — [[nate-herk]] #1 (Printing Press as packaged CLI alternative); [[nate-b-jones]] #11 (MCP in 6-layer taxonomy)
- [[youtube-digest-apify-2026-05-22]] — [[nate-b-jones]] #6 (MCP as Layer 1 of [[agent-protocol-stack]] + security boundary) + [[brad-bonanno]] #7 ([[claude-for-small-business]] MCP connector kit)
- [[claude-code]], [[claude-skills]] — concept relationships
- [[printing-press]] — CLI-alternative packaged product
- [[plugins]] — taxonomy layer where MCP sits
- [[knowledge-layer]] — likely connector layer between Pinecone Nexus / Microsoft Fabric IQ and Claude Code
- [[voice-agents]] — cal.com integration likely via MCP
- [[context-farming]] — MCP is the connector layer
- [[anthropic]] — author
- (Planned) [[agent-skills-vs-mcp]] — direct comparison page
