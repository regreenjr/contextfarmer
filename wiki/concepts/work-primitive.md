---
title: Work Primitive (Access / Meaning / Authority)
category: concept
summary: [[nate-b-jones]]'s three-layer framework for diagnosing agent-readiness in any product or platform — access (can the agent reach it), meaning (does the agent understand what the action means), authority (can the agent commit it); explains why coding agents arrived first (rich work semantics), why Salesforce-headless works and SAP-blocking doesn't, and reframes "computer use" as the messy-middle adapter rather than the strategic primitive; in 2026-05-11 the authority layer gains a humans-vs-agents sub-diagnostic via the sibling [[agent-security]] framework
tags: [work-primitive, semantic-work, agent-readiness, access, meaning, authority, salesforce, sap, perplexity, computer-use, nate-b-jones, framework, agent-security]
sources: 2
updated: 2026-05-11
---

# Work Primitive

## Definition

[[nate-b-jones]]'s **three-layer agent-readiness framework**, named in [[youtube-digest-apify-2026-05-10]] #7 (*The Work Primitive: What Every AI Product Leader Gets Wrong*, 27.6K views).

The three layers under any agent-platform interaction:

1. **Access** — can the agent *reach* the surface? (Computer use, browser automation, MCP, native API)
2. **Meaning** — does the agent know *what the action means*? (Domain semantics, downstream effects, business intent)
3. **Authority** — does the agent have *permission to commit*? (Approval, governance, audit trail)

Visible work the model does (clicking buttons) is at the **access** layer. Strategic moats live at **meaning** and **authority**.

## Core claims

- **Computer use is a distraction from the strategic layer** — visible AI clicks distract from the question of who defines what the click means
- **The richer the work-semantics layer, the better an agent works on top** — software development has unusually rich semantics (compilers, ASTs, types, tests, lint), which is **why coding agents arrived first**
- **Use the richest interface available** — when MCP exposes meaning, MCP > computer use; when nothing exposes meaning, computer use is the universal adapter
- **Computer use is the universal adapter for the messy middle** — works on everything because it operates at the access layer; lacks meaning by construction
- **Salesforce going headless is exposing meaning to agents** — strategic
- **SAP blocking agents is protecting the authority moat** — also strategic, opposite direction
- **Perplexity's strategy** (search → browser → personal computer) is a **march up the meaning hierarchy** — they're not adding access, they're building meaning around the surfaces they reach
- **Leaders asking "can the agent act?" are asking the wrong question** — the right question is "does the product know what that action means?"

## Why coding agents arrived first

| Layer | What software development has |
|---|---|
| **Access** | Filesystem, git, terminal — fully programmable |
| **Meaning** | Compilers, type systems, ASTs, lint, tests — *machine-checkable semantics* |
| **Authority** | Code review, CI gates, branch protection — *codified approval flows* |

Compare to consumer life:
- **Access** — patchwork (some APIs, lots of UI)
- **Meaning** — taste, social norms, situational judgment — *no machine-checkable semantics*
- **Authority** — implicit, contextual — *no codified approval flow*

This is **the same diagnosis** [[nate-b-jones]] used in his [[anticipation-gap]] frame — coding agents crossed the agent-usefulness threshold because verification (meaning + authority) is clean. Work Primitive generalizes the explanation: it's not just verification — it's all three layers being mature.

## Strategic test cases

### Salesforce going headless
- **Access**: SaaS APIs already exposed
- **Meaning**: object model (Account, Opportunity, Lead) is a rich semantic layer
- **Authority**: SOC2 + custom permission model; can be agent-delegated
- **Verdict**: agent-ready; Salesforce's head*less* move *exposes* the meaning layer to agents

### SAP blocking agents
- **Access**: SAP could expose APIs but chooses not to
- **Meaning**: deeply rich (decades of ERP semantics) but proprietary
- **Authority**: tightly governance-controlled
- **Verdict**: agent-ready *technically*, but SAP's strategic move is to *withhold* the meaning layer to preserve authority moat

### Perplexity's march
- **Search** — access layer (raw web access)
- **Browser** — adds meaning (page semantics, navigation, citation)
- **Personal computer** — adds meaning + authority (knows what user is working on, what they care about, what's allowed)

Each step climbs the hierarchy: more meaning, more authority, same access.

## Hierarchy of interfaces (per [[nate-b-jones]] #7)

In order of decreasing meaning richness:

1. **Native domain API with full semantics** — best
2. **MCP server with rich tool/resource model** — second-best
3. **Programmatic API with thin semantics** — adequate
4. **Browser automation with DOM understanding** — adapter-tier
5. **Computer use / pure UI replay** — last resort

**The rule**: use the richest interface available. Computer use is the messy-middle adapter, not the strategic primitive.

## Implications for agent design

| If meaning is... | Use... |
|---|---|
| Codified in the platform | Native API or MCP |
| Codified externally (docs, ontology) | API + retrieval over the codified meaning |
| In the user's head | Permission ladder ([[anticipation-gap]]); agent prompts user for meaning per-action |
| Not codified anywhere | Avoid agent automation; do the meaning work first |

## Authority-layer extension — humans-vs-agents sub-diagnostic (added 2026-05-11)

[[nate-b-jones]]' sibling [[agent-security]] framework (named in [[youtube-digest-apify-2026-05-11]] #1) adds a sharpening sub-diagnostic to the **authority layer**:

> **"Does your platform know humans from agents?"**

Most current platforms treat agent traffic as human traffic — same auth tokens, same session model, same audit trail, same rate limits. That's an **authority-layer leak**: the platform technically can commit the action, but can't distinguish *who is asking it to commit* (agent vs human). The McKinsey Lilly exploit ($20 SQL injection through 22 of 200 unauthenticated endpoints) is the canonical failure case.

Updated authority-layer diagnostic table:

| Authority question | Maturity level |
|---|---|
| Can the platform commit the action at all? | Authority-1: bare authority |
| Can the platform delegate the authority to an agent? | Authority-2: delegated authority |
| Can the platform tell *who* delegated — and apply different policies to agent vs human callers? | **Authority-3: agent-aware authority** ([[agent-security]]) |

This makes [[work-primitive]] **substrate-side post-buy** while [[agent-security]] is **substrate-side pre-buy** (procurement). The two questions chain: Work Primitive at evaluation, Agent Security at procurement.

## Where this framework integrates with this vault's frameworks

[[nate-b-jones]] is now the source of **seven complementary diagnostics**:

| Framework | Side | Question |
|---|---|---|
| T/C/L/D | Worker-side | Which of my tasks is durable? |
| Anticipation gap + permission ladder | User-side | When should the agent act, and how much autonomy? |
| **Work Primitive (access/meaning/authority)** | **Substrate-side (post-buy)** | **Is the platform agent-ready?** |
| Plugins as mech-suit | Builder-side | Where in my stack does each capability belong? |
| Code comprehensibility | Codebase-side | Is my code legible enough for AI review? |
| OpenClaw runtime reframe | Stack-side | What survives model/vendor churn? |
| **Agent Security** | **Procurement-side (pre-buy)** | **Does the platform know humans from agents?** |

Together: **a complete agent-readiness audit** for any organization — covering procurement, substrate, worker, user, builder, codebase, and stack.

## Why it matters for 3Ps

1. **Cleanest enterprise-buyer framework yet** — three answerable questions replace vague "AI readiness" with concrete diagnostics:
   - **Access**: can the agent reach your tools? (technical)
   - **Meaning**: does it understand your domain? (semantic)
   - **Authority**: are you comfortable letting it commit? (governance)
2. **Direct sales conversation tool** — for any pre-engagement discovery call, the three layers structure the conversation
3. **Vendor-evaluation framework** — when clients ask "should we build on Salesforce / SAP / Microsoft / Salesforce-Agentforce", the work-primitive lens gives a structured answer
4. **Content angle** — "the work primitive" reframe of "AI strategy" is publishable thought leadership for engineering leaders
5. **Pairs with [[agent-substrate]]** — Work Primitive explains *why* boring tools (Jira, Salesforce, ERPs) become more important: they own the meaning + authority layers

## Open questions

- Is "Work Primitive" the durable name for this framework, or will [[nate-b-jones]] iterate naming?
- Does it map cleanly onto industry analysts' (Forrester, Gartner) AI-readiness frameworks?
- Are there products explicitly addressing the meaning layer? (LangChain, Salesforce Agentforce, Microsoft Copilot Studio — partial)
- How do **multi-modal** agents (voice, vision) layer into access/meaning/authority?

## Related pages

- [[anticipation-gap]] — sibling [[nate-b-jones]] framework (user-side)
- [[plugins]] — sibling [[nate-b-jones]] framework (builder-side)
- [[code-comprehensibility]] — sibling [[nate-b-jones]] framework (codebase-side)
- [[agent-security]] — sibling [[nate-b-jones]] framework (procurement-side); sharpens the authority layer with humans-vs-agents sub-diagnostic
- [[agent-substrate]] — boring-tools-win thesis; Work Primitive explains *why*
- [[nate-b-jones]] — author
- [[mcp]] — meaning-layer mechanism
- [[claude-code]] — coding-agents-arrived-first proof case
- [[ai-consulting]] — direct sales-conversation framework
- [[gtm-2026]] — AI-era buyer framework
- [[youtube-digest-apify-2026-05-10]] — primary citation
- [[youtube-digest-apify-2026-05-11]] — authority-layer extension via [[agent-security]]
