---
title: Agent Security (Procurement-Side)
category: concept
summary: [[nate-b-jones]]'s frame that AI agent exploits are a procurement-and-organizational-design problem, not a tech-hygiene problem — McKinsey's "Lilly" platform was exploited via $20 SQL injection through 22 of 200 unauthenticated endpoints, but the deeper failure was buying agent software with traditional SaaS procurement (legal → security → IT → implementation) instead of putting developers at the table before signing; the canonical buyer-side diagnostic is "does your platform know humans from agents"
tags: [agent-security, procurement, work-primitive, authority, nate-b-jones, framework, mckinsey, anthropic, openai, sap, pinecone, salesforce, servicenow]
sources: 1
updated: 2026-05-11
---

# Agent Security (Procurement-Side)

## Definition

[[nate-b-jones]]'s **procurement-side framework** for AI agent security, named in [[youtube-digest-apify-2026-05-11]] #1 (*Anthropic And OpenAI Just Admitted The Model Isn't Enough*, 53.6K views).

Core thesis: **agent exploits are a procurement and organizational-design failure, not a tech-hygiene failure.** The cheapest move for any buyer is bringing developers to the procurement table *before* signing a contract — because **implementation IS the strategy in the agent era**.

This is the **buyer-side complement to [[work-primitive]]**: where Work Primitive asks *can the agent reach + understand + commit?* (post-buy substrate diagnostic), Agent Security asks *can the platform tell when it's an agent doing it, and apply different policies?* (pre-buy procurement diagnostic).

## The unlock event — McKinsey's Lilly platform

Per [[nate-b-jones]] #1:

- **McKinsey's "Lilly" AI platform** was exploited via **a $20 SQL injection** — an attack mostly extinct from 2026's standard SaaS attack surface
- The attacker reached one entry point, then escalated through **22 of 200 endpoints that were left unauthenticated** (chapter 4:22)
- Common narrative: "carelessness — they forgot auth"
- [[nate-b-jones]]' reframe: **22 unauthenticated endpoints out of 200 is a pattern, not a mistake** — it signals a culture/process gap, not a one-off oversight

The depth of the framing: SQL injection in 2026 is structurally implausible for a well-procured platform. It exists here because the procurement process didn't put eyes on the implementation surface until it was too late.

## The procurement-sequence claim

Chapter 6:10 of #1, *Why agents break the old procurement sequence*:

**Traditional SaaS procurement**:
```
Legal → Security → IT → eventually-Implementation
```
Implementation sits *downstream* of strategy. The procurement decision is made before anyone implements anything.

**Why this breaks for agents**:
- A single agent run *touches* multiple downstream systems (chapter 8:45)
- The implementation surface becomes the security surface
- Pre-implementation evaluation can't see what the agent will actually do
- Endpoint inventory ≠ behavior inventory

**The reframe**:
- **Implementation IS the strategy** in the agent era (chapter 10:30)
- The cheapest move is bringing developers to the procurement table *before* signing
- Buying agent software without developer input is the new equivalent of buying SaaS without security review in 2010

## Vendor responses — six-way convergence

Chapter 12:15 of #1, *Anthropic, OpenAI, SAP, Pinecone, Salesforce, ServiceNow respond*:

All six vendors pitched their answer to the same underlying problem in the same week:

| Vendor | Likely response shape |
|---|---|
| [[anthropic]] | Agent-aware identity primitives in [[claude-code]] / [[mcp]] |
| [[openai]] | Codex / API agent-auth surface |
| SAP | Authority-moat reinforcement (consistent with [[work-primitive]] tracking) |
| [[pinecone]] | Knowledge-layer access control (Nexus authorization model) |
| Salesforce | Agentforce identity model |
| ServiceNow | Agent-aware ITSM workflow approval gates |

This is the **same shape as the [[knowledge-layer]] convergence** ([[pinecone]] / Microsoft / Google all shipping in 4 weeks per [[youtube-digest-apify-2026-05-10]] #4) — when category leaders all ship the same product in the same week, that's a category, not coincidence.

**Convergence cadence is now sub-month for major architectural shifts.**

> Open: specific product names + scope of each vendor's response. Transcript pull on [[youtube-digest-apify-2026-05-11]] #1 would clarify. Worth tracking as each vendor publishes details.

## The substrate question — "does your platform know humans from agents"

Chapter 15:20 of #1, *Does your platform know humans from agents*:

The **single most actionable buyer-side question** [[nate-b-jones]] surfaces. Most current platforms treat agent traffic as if it were human user traffic:
- Same auth tokens
- Same session model
- Same audit trail
- Same rate limits
- Same permission scope

The actual buyer question for any agent-touching product: **"can your platform distinguish a human action from an agent action, and apply different policies?"** If the answer is no, the platform is *agent-naive* — every authority-layer guarantee is unreliable in an agent-mixed environment.

This is **the procurement-side equivalent of [[work-primitive]]'s authority layer**. Work Primitive asks if the platform *can* commit the action; Agent Security asks if the platform *knows who's asking*.

## Strategic test cases

| Scenario | Failure mode | Agent-aware response |
|---|---|---|
| Agent makes admin-tier API call using human's OAuth token | Audit log shows the human as actor; impossible to forensically separate agent action from human action | Distinct agent identity primitives; agents carry their own tokens; audit log distinguishes |
| Agent triggers rate-limit on behalf of human | Human gets locked out of their own account because the agent burned the quota | Per-agent rate limits separate from human user limits |
| Agent escalates privileges by chaining endpoints | The McKinsey Lilly pattern — 22 of 200 unauthenticated endpoints discovered through traversal | Endpoint inventory + agent-policy specification at procurement time |
| Agent acts on instructions from a prompt injection in user-supplied content | "Confused deputy" — agent acts on attacker's intent with user's authority | Intent/authority separation; per-action confirmation for high-impact operations |

## Where Agent Security integrates with [[nate-b-jones]]' framework stack

This is **[[nate-b-jones]]' 7th named framework**:

| Framework | Side | Diagnostic question |
|---|---|---|
| T/C/L/D | Worker | Which tasks survive AI? |
| Anticipation gap + permission ladder | User | When should the agent act? |
| Work Primitive | Substrate | Is the platform agent-ready? |
| Plugins as mech-suit | Builder | Where does each capability belong? |
| Code comprehensibility | Codebase | Is my code legible enough for AI to review? |
| OpenClaw runtime reframe | Stack | What survives model/vendor churn? |
| **Agent Security** | **Procurement** | **Does the platform know humans from agents — and can we tell before we sign?** |

This is [[nate-b-jones]]' **first procurement-focused** framework. Prior frameworks all targeted post-buy diagnostics. Agent Security targets the *buy* itself.

Together: **a complete agent-era audit covering worker → user → codebase → builder → substrate → stack → and now procurement**.

## Why coding agents arrived first (consistent with [[work-primitive]])

The agent-security analog of [[work-primitive]]'s coding-agent-first argument:

- Coding agents operate in environments with **rich identity primitives** (git, OS users, CI runners) — agent identity is naturally distinct from human identity
- Code-review/PR workflows have **codified approval flows** — the authority layer already knows what an agent commit looks like vs human commit
- The implementation surface is the security surface, and developers are already at the procurement table for dev tools

Consumer / enterprise SaaS has none of this — agent identity is bolted onto a human-user-only data model.

## Why this matters for 3Ps

1. **Cleanest procurement-conversation entry point yet.** "Does your platform know humans from agents?" is a single-sentence diagnostic that turns any AI vendor-evaluation conversation into a scoping exercise. Direct replacement for vague "AI readiness."
2. **"Implementation is the strategy" sharpens [[ai-consulting]] positioning.** The 3Ps offering can claim a seat at *procurement* discussions, not just post-buy implementation — higher-margin engagement scope.
3. **Six-vendor convergence is a content angle.** "Why Anthropic, OpenAI, SAP, Pinecone, Salesforce, and ServiceNow all shipped agent-security responses in the same week" is publishable thought leadership for enterprise buyers.
4. **The McKinsey Lilly case is a portable horror story.** $20 exploit + 22 unauthenticated endpoints + name-brand consultancy is the kind of detail that earns enterprise attention. Use sparingly so it doesn't lose impact.
5. **Pairs naturally with [[work-primitive]]** — the buyer-side / substrate-side pair becomes a 2x2 framework for any AI vendor evaluation: *can it tell humans from agents (procurement) × can the agent commit (substrate)*.
6. **Aligns with [[code-comprehensibility]]** for engineering-leader clients — both treat security as a property emergent from the meaning/identity layer, not bolted-on hygiene.

## Open questions

- **What did McKinsey actually publish about the Lilly postmortem?** Worth a search — the [[nate-b-jones]] framing may add interpretive layers not in the original.
- **Specific vendor products** — each of the six vendors' responses needs a concrete product name + scope. Worth ad-hoc tracking as they publish.
- **Standardization** — is there a vendor-neutral spec emerging for agent-vs-human identity (analogous to OAuth for auth, OIDC for identity)?
- **Detection — can a buyer test "does it know humans from agents" without vendor cooperation?** What's a buyer-side audit script?
- **Insurance angle** — cyber insurance treats AI agents how? Premium structure as a forcing function?
- **Regulatory angle** — does any regulator (FTC, EU AI Act, NYDFS) require human/agent distinction in production deployments?

## Related pages

- [[nate-b-jones]] — author; this is his 7th named framework
- [[work-primitive]] — sibling framework (substrate side); Agent Security is the procurement-side complement
- [[code-comprehensibility]] — sibling framework (codebase side); shared "meaning layer" foundation
- [[anticipation-gap]] — sibling framework (user side); permission ladder is the autonomy gradient that agent-aware platforms need to enforce
- [[anthropic]], [[openai]], [[pinecone]] — agent-security responders tracked in this vault
- [[ai-consulting]] — direct sales conversation framework
- [[claude-code]], [[claude-skills]] — coding-agent context where this is most-mature
- [[knowledge-layer]] — sibling sub-month convergence pattern
- [[youtube-digest-apify-2026-05-11]] — primary citation
