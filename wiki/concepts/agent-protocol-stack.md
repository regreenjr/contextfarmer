---
title: Agent Protocol Stack (Six Protocols / Three That Matter)
category: concept
summary: [[nate-b-jones]]' 13th named framework — a six-protocol agent-infrastructure-stack taxonomy with three settled layers ([[mcp]] for tool+data access, **A2A** for agent-to-agent delegation, **AG-UI** for agent-to-human supervision surface) plus three contested layers (A2UI, AP2, x402); positions [[mcp]] inside its larger six-protocol context for the first time in this vault; names the **three questions agents must answer** (what can I access / who can I delegate to / how do humans supervise me) and the **six questions to ask before you build**; pairs with [[agentic-commerce]] six-layer taxonomy (same vault-author, overlapping vendor map on AP2/x402) and **forms one layer in [[nate-b-jones]]' full 4-layer enterprise-AI stack** with [[infrastructure-control-layer]] (substrate) / [[agentic-implementation-layer]] (value) / [[agent-metering]] (pricing)
tags: [nate-b-jones, framework, agent-protocols, mcp, a2a, ag-ui, a2ui, ap2, x402, anthropic, google, stripe, agent-card, delegation, supervision-surface, security-boundary, anticipation-gap, agentic-commerce, infrastructure-control-layer]
sources: 1
updated: 2026-05-22
---

# Agent Protocol Stack (Six Protocols / Three That Matter)

## What it is

[[nate-b-jones]]' **13th named framework**, from *Google Spent a Year Stitching MCP, A2A, AG-UI Together. I/O Today.* (37.7K views, 2026-05-19, 20:42) in [[youtube-digest-apify-2026-05-22]]. A **six-protocol taxonomy** for the agent-infrastructure-stack with explicit "three that matter" + "three contested" partition.

**The framing claim**: *"The common story is that Google I/O is about the demos — but the more interesting story is the protocol stack being built underneath them. Six protocols, three of which form the actual agent stack."*

## The six-protocol taxonomy

| Protocol | Layer | Status | Sponsor |
|---|---|---|---|
| **[[mcp]]** | Tool + data access | **Settled** — production-ready | [[anthropic]] |
| **A2A** | Agent-to-agent delegation | **Settled** — production-ready | Google |
| **AG-UI** | Agent-to-human control / supervision | **Settled** — production-ready | Google |
| **A2UI** | Agent-to-UI driving | Contested | Multiple |
| **AP2** | Payment authorization (mandate mechanic) | Contested | Google |
| **x402** | HTTP-native machine-to-machine micropayments | Contested | Stripe |

## The three questions agents must answer (chapter 1:18)

The **diagnostic substructure** for understanding which protocols matter for any agent:

1. **What can I access?** → [[mcp]] answers
2. **Who can I delegate to?** → A2A answers
3. **How do humans supervise me?** → AG-UI answers

These three settled protocols form the **operational backbone**. The other three are **contested commercial layers** — camps fighting over who owns payment + UI surface.

## Each settled protocol

### [[mcp]] — tool and data layer (chapter 2:35)

The settled tool/data access protocol. Per [[nate-b-jones]]' new framing (chapter 4:50): **MCP is a security boundary**. MCP servers *are* the natural action-boundary instrumentation point — same reframe as Lindy's outbound-mail judge from [[nate-b-jones]] 2026-05-12 (the [[agent-security]] judge-architecture pattern). The judge sits at the MCP-server perimeter; MCP servers gate the action; the protocol carries the auditability surface.

### A2A — delegation layer (chapter 6:20)

Agent-to-agent delegation. **First A2A coverage in this vault.** The core primitive is the **agent card** (chapter 8:15) — a manifest declaring an agent's capabilities + SLA + authority surface. Other agents discover, verify, and delegate via the card. Same shape as MCP's manifest, but for delegation rather than tool-access.

Google-sponsored. Confirms Google's "stitching MCP+A2A+AG-UI" thesis — Google is **assembling the protocol stack** rather than competing with Anthropic on the model layer.

### AG-UI — human control layer (chapter 9:40)

The **supervision surface protocol**. **First AG-UI coverage in this vault.** Per Nate (chapter 11:55): *"Agents that don't expose supervision surfaces are unsupervisable; supervisability is a product feature, not a config option."*

AG-UI closes the gap [[anticipation-gap]] identified — consumer AI lacked a supervision surface; AG-UI is the **protocol-level candidate** for that surface across products.

The permission ladder ([[anticipation-gap]]) is the user-side framework; AG-UI is the protocol-side implementation.

## Each contested protocol

### A2UI — agent driving a UI

Distinct from AG-UI (human driving an agent). A2UI is the protocol for agents to **drive UIs as their action surface**. Contested because the camp split is between:
- "Agents should call APIs, not click buttons" (API-first camp)
- "Agents need UI drive for the long tail of un-API'd surfaces" (UI-first camp)

Resolution likely depends on which side ships first at scale.

### AP2 — payment authorization (chapter 15:10)

**The mandate mechanic.** AP2 is Google's protocol for an agent's **signed payment authorization** — a permission slip the agent carries from the user. Distinct from x402 (the rails); AP2 is the **authorization layer above the rails**.

Overlaps with the AP2 named in [[agentic-commerce]] (same Google protocol; [[nate-b-jones]] now covers it twice across two framework videos).

### x402 — machine-to-machine rails (chapter 16:35)

Stripe-sponsored. **HTTP-native micropayments** for agent-to-agent flows. The "Stripe and customer-obsessed payment design" callout (chapter 16:35) signals Stripe positioning x402 as the **agent-payment standard** the way they positioned APIs as the developer-payment standard a decade ago.

Per [[agentic-commerce]] framework: x402 is **Layer 5** (machine-to-machine rails) of the six-layer commerce taxonomy.

## The six questions to ask before you build (chapter 18:00)

The **builder-side diagnostic**:

1. What tool/data does my agent need? → [[mcp]]
2. Does it need to delegate? → A2A
3. How will humans intervene? → AG-UI
4. Does it need to drive a UI? → A2UI (contested)
5. Does it pay? → AP2 (contested)
6. Does it pay other agents? → x402 (contested)

Pairs with [[capital-allocation-framework]]'s five-lever decision matrix and [[infrastructure-control-layer]]'s seven questions — [[nate-b-jones]] now ships **three workflow-diagnostic question-sets** in this batch alone (capital allocation, agent protocols, infrastructure).

## Position in the full [[nate-b-jones]] stack

| Layer | Framework | Primary question |
|---|---|---|
| **Infrastructure** | [[infrastructure-control-layer]] | Which 5 control points does my agent touch? |
| **Protocols** | **[[agent-protocol-stack]]** | **Which 6 protocols + 3 questions?** |
| **Value capture** | [[agentic-implementation-layer]] | Where do the trillion dollars live (4-axis squeeze)? |
| **Pricing** | [[agent-metering]] | How does the meter tick (5-vendor metering shapes)? |
| **Decision** | [[capital-allocation-framework]] | Which lever per workflow (automate/build/buy/hire/wait)? |

This is the **complete enterprise-AI agent stack** in [[nate-b-jones]]' framework cadence — all five layers shipped within **8 days** (2026-05-14 → 2026-05-20).

## Strategic significance

1. **13th [[nate-b-jones]] framework** — extends framework cadence to one-per-video baseline
2. **First A2A + AG-UI coverage** in this vault — two new protocol primitives tracked alongside [[mcp]]
3. **The "three that matter" filter is an opinion bet** — Nate is explicitly betting MCP+A2A+AG-UI win and the contested layers resolve to single winners. This is a **testable prediction** for future digests
4. **Pairs with [[agentic-commerce]] 6-layer taxonomy** — overlap on AP2 and x402 means [[nate-b-jones]] is **double-covering the commerce protocols** from operations + commerce angles. Triangulation signal — these protocols matter at multiple stack layers
5. **MCP-as-security-boundary** (chapter 4:50) is the **first explicit security-boundary reframe of MCP** in the vault — extends [[agent-security]]' judge-architecture pattern at the protocol layer
6. **AG-UI is the [[anticipation-gap]] protocol-level answer** — Nate's 2026-05-05 framing identified consumer AI's missing supervision surface; AG-UI is the protocol candidate

## Related

- [[nate-b-jones]] — author; 13th framework
- [[mcp]] — layer 1 of this stack
- [[agentic-commerce]] — 6-layer taxonomy with AP2/x402 overlap
- [[agent-security]] — MCP-as-security-boundary reframe extends judge pattern
- [[anticipation-gap]] — AG-UI is the protocol-side answer to the supervision-surface gap
- [[infrastructure-control-layer]] — substrate-layer counterpart in the full stack
- [[agentic-implementation-layer]] — value-capture-layer counterpart
- [[agent-metering]] — pricing-layer counterpart
- [[capital-allocation-framework]] — decision-layer counterpart
- [[claude-code]] — primary [[mcp]] substrate

## Used in

- [[youtube-digest-apify-2026-05-22]] — primary citation ([[nate-b-jones]] #6)

## Open questions

- **What happens at Google I/O** (chapter 19:45 *What to watch at Google I/O*) — the video predates the event by a few days; Google's actual launches reshape this taxonomy
- **A2A adoption outside Google** — does Anthropic adopt A2A or ship a competitor?
- **A2UI vs AG-UI in practice** — are they the same protocol from different sides, or genuinely separate?
- **AP2 in [[agent-protocol-stack]] vs AP2 in [[agentic-commerce]]** — same Google protocol, different stack-position framing. Worth resolving the overlap.
- **Agent card** — does it have a standardized schema yet? What does a published agent card look like?
- **Will Anthropic publish their own delegation protocol** instead of adopting A2A? (Critical for [[claude-code]]'s multi-agent roadmap)
