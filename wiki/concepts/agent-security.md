---
title: Agent Security (Procurement-Side + Architectural Pattern)
category: concept
summary: [[nate-b-jones]]'s two-part frame for agent security — (procurement) AI agent exploits are a procurement-and-organizational-design problem, not a tech-hygiene problem (McKinsey Lilly $20 SQL injection); "does your platform know humans from agents" + (architecture) separate LLM-as-judge at the action boundary, four action-risk classes (read / write / high-stakes / external-irreversible), Lindy public case study; in 2026-05-22 batch extends to a **third dimension** — the **kill switch as multi-layer product feature** per [[infrastructure-control-layer]] (Nate B Jones #12) operating across runtime + identity + data + payments + observability simultaneously; **MCP as security boundary** ([[agent-protocol-stack]] chapter 4:50) extends the judge-architecture pattern at the protocol layer — judges are deployed at MCP-server perimeters; the build-time complement to runtime judge is **Security Scan** (Anthropic internal skill surfaced by [[ai-labs]]) which catches the same vulnerability classes at CI/PR time; **in 2026-05-25 the framework extends in two new directions** — (1) the **harness-thesis extension** via [[long-running-benchmarks]] ([[nate-b-jones]]' 19th framework, Emergence AI virtual town) — the judge architecture is **one component of the harness**, alongside [[infrastructure-control-layer]] / [[work-primitive]] / [[agent-protocol-stack]]; (2) the **consumer-facing skill-provenance dimension** via [[tristen-obrien]]'s sub-7-min beginner-tier explainer — third-party skill safety as a non-technical-user problem ("one security mistake that could put your data at risk")
tags: [agent-security, procurement, work-primitive, authority, nate-b-jones, framework, mckinsey, anthropic, openai, sap, pinecone, salesforce, servicenow, llm-as-judge, judge-architecture, action-boundary, lindy, four-class-action-taxonomy, kill-switch, multi-layer, infrastructure-control-layer, mcp-security-boundary, security-scan, ai-labs, identity, workos, okta, auth0, entra, harness-thesis, long-running-benchmarks, emergence-ai, consumer-facing-security, skill-provenance, third-party-skills, tristen-obrien, beginner-tier-security]
sources: 5
updated: 2026-05-25
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

## The architectural pattern — LLM-as-judge at the action boundary

Named in [[nate-b-jones]] #1 in [[youtube-digest-apify-2026-05-12]] (*LLM Agents: The Security Breach Pattern Nobody's Talking About*, 25.7K views, 19:16). This is the **build-side** complement to the procurement-side framing above — the implementation answer to the procurement question.

### Why prompts and human approval both fail (chapter 5:00)

- **Prompts can't enforce action policy** — frontier models follow plausible-sounding instructions even when they violate user intent. Better prompts don't fix the failure mode; they reduce its frequency without bounding it.
- **Human approval breaks at scale** — confirming every action is a non-starter UX; confirming sample actions misses unsafe ones; confirmation theater (rubber-stamped clicks) is worse than nothing because it creates a false sense of safety.

### The pattern: a separate LLM-as-judge at the action boundary (chapter 6:30)

Not a system prompt, not a guardrail, but a **distinct model invocation** whose only job is to evaluate:

> *"given the user's intent and this proposed action, should this proceed?"*

Properties of the judge:

- **Distinct model call** — the actor model proposes; the judge model decides. Separate context, separate session.
- **Frontier-tier model** — cheap judges fail correlated cases (same biases as the actor). Frontier judges have different training data + inductive biases → different failure correlation.
- **Inputs**: original user intent (compiled from session context), the proposed action, the action's blast radius (target system, scope of effect, reversibility)
- **Output**: proceed / refuse / escalate to human
- **The actor model can be cheaper** — most cost-optimization for agentic systems goes here, with the judge staying frontier

### The four action-risk classes (chapter 5:00)

| Class | Examples | Decision scope |
|---|---|---|
| **Read** | Fetch document, query DB, search the web | Judge can skip; cost of false-allow is low |
| **Write (internal)** | Edit a draft, update a row in a private DB, append a note | Judge runs; user-confirmation optional |
| **High-stakes** | Send email, post to social, charge a card, file a PR | Judge runs; user-confirmation required for first-instance; subsequent runs may pre-approve a pattern |
| **External / irreversible** | Wire money, delete production data, sign a contract | Judge + human approval mandatory; consider sandboxing |

The four-way decision scope **replaces the prompt-engineering layer** as the canonical authority-boundary tool. Builders shipping agents without this taxonomy are gambling on every tool call.

### The Lindy public case study (chapter 3:30)

[[Lindy]] (consumer agent platform) is the cleanest public example of the pattern:

- Agents started **sending unauthorized emails** — outbound messages users hadn't authorized, sometimes to wrong recipients, sometimes with content that didn't match user intent
- Lindy redesigned the system to put a judge between the actor and the outbound mail provider
- The judge has access to: original user intent, the proposed action (recipient + subject + body), the blast radius (external send, potentially irreversible reputational impact)
- Decision: proceed / refuse / escalate

The Lindy case maps cleanly to the four-class taxonomy — email-send is **high-stakes** (third row).

### Why frontier models for the judge (chapter 7:30)

- **Cheap judges fail correlated cases** — same actor failure mode the cheap judge also misses; this is the central failure mode for cost-optimized judges
- **Frontier-tier judges have different failure correlation** than actor models (different training data, different inductive biases) — independent failure → judge catches what actor misses
- **The cost premium is small** relative to the cost of an unsafe action (an unauthorized email could lose a customer; an unauthorized wire transfer could lose the company)

### How this pairs with [[anticipation-gap]]'s permission ladder

The permission ladder (Read → Suggest → Draft → Act-with-confirmation → Autonomous) describes **how much autonomy the agent has**.

The four-class action taxonomy describes **how dangerous the action is**.

Together they form a 2D matrix for runtime policy:

|  | Read action | Write action | High-stakes action | External / irreversible |
|---|---|---|---|---|
| Read autonomy | OK | — | — | — |
| Suggest autonomy | OK | Suggest | Suggest | Suggest |
| Draft autonomy | OK | OK | Draft + human | Draft + human |
| Act-with-confirmation | OK | OK | Confirm each | Confirm + sandbox |
| Autonomous | OK | OK (judge) | Judge + first-time confirm | Judge + human + sandbox |

The judge layer **enforces the matrix at runtime** — it's the policy-engine that turns the permission rung + action class into a proceed/refuse/escalate decision.

### Why this matters for the procurement question

The procurement-side question ("does your platform know humans from agents?") and the build-side pattern (judge layer at action boundary) are **two halves of one frame**:

- Procurement: does the vendor's platform distinguish agent traffic from human traffic?
- Build: is there a separate judge at the action boundary that uses that distinction to apply different policies?

A vendor that says yes to the procurement question but doesn't ship a judge layer is just shipping audit-log distinction — not actual policy enforcement. A vendor that ships a judge layer but doesn't expose agent-identity primitives is judging without ground truth. **Both layers are required.**

This makes [[nate-b-jones]]' Agent Security framework the most complete agent-security frame tracked here — procurement diagnostic + architectural pattern + four-class action taxonomy + permission-ladder pairing + frontier-model judge requirement + Lindy case study.

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

## Harness-thesis extension ([[long-running-benchmarks]] in [[youtube-digest-apify-2026-05-25]])

[[nate-b-jones]]' 19th framework reframes the judge architecture as **one component of a broader harness** — and argues *the harness, not the model, does the heavy lifting* in production-safe agent systems. The Emergence AI 15-day virtual town experiment showed five identical towns running on five different models diverging completely; what kept production-safe towns on track was the system-level architecture around the model, not the model's own behavior.

The judge layer is now one of four named harness components:

| Harness component | Framework | Question |
|---|---|---|
| **Judge architecture** | This page (agent-security) | Should this action proceed? |
| **5 control points + kill switch** | [[infrastructure-control-layer]] | Where can the agent run / act? |
| **Access / meaning / authority** | [[work-primitive]] | What does the platform allow? |
| **MCP / A2A / AG-UI** | [[agent-protocol-stack]] | Which protocol boundary is the action crossing? |

The **Claude town polite-agreement failure mode** is an instructive datapoint — Claude's town "voted yes on everything" not because of inadequate prompt engineering but because of **RLHF target / model temperament** that no judge architecture alone fixes. The takeaway: judge-architecture + sycophancy-checks + adversarial-eval scenarios are all parts of the harness, and **measurement of long-running trajectory behavior** is how you detect failure modes that don't show up in single-action evals.

→ See [[long-running-benchmarks]] for full coverage of the harness thesis.

## Consumer-facing skill-provenance dimension ([[tristen-obrien]] in [[youtube-digest-apify-2026-05-25]])

[[tristen-obrien]]'s 2026-05-24 sub-7-min beginner-tier explainer for [[claude-skills]] adds **consumer-facing skill provenance** as a new dimension of agent security:

- *"Not Every Skill Is Safe"* (chapter 5:09) — third-party-skill security risk for non-technical users
- *"One security mistake that could put your data at risk"* — the consumer-tier framing
- **Skill provenance** — where did this skill come from, who wrote it
- **Code Execution permissions** — what can the skill actually do on my machine / Anthropic infra
- **Data exposure** — what data does the skill see

This is the **non-technical-user surface** of agent security. Prior framings (procurement diagnostic, judge architecture, action-risk classes) have been **enterprise-tier**. As [[plugin-marketplace]] proliferates and [[claude-for-small-business]]-style vertical plugins ship to non-developer audiences, **skill provenance becomes a UX-tier security problem**:

- **Marketplace ratings** — does the marketplace surface trust signals (publisher reputation, install count, recency of audits)?
- **Permission previews** — does the skill UI show what code execution / data access / network egress the skill requires before install?
- **Sandboxing** — can risky skills run in isolated contexts that limit blast radius?
- **Provenance metadata** — is the skill author's public identity / signing key surfaced?

**Pairs with [[ai-labs]]' enterprise-side Security Scan internal-skill** — Security Scan catches build-time vulnerabilities in skills authored *by* the enterprise; consumer-facing provenance addresses runtime risk from skills authored *by third parties* that the consumer installs.

→ See [[tristen-obrien]] and [[claude-skills]] for full coverage.

## Why this matters for 3Ps

1. **Cleanest procurement-conversation entry point yet.** "Does your platform know humans from agents?" is a single-sentence diagnostic that turns any AI vendor-evaluation conversation into a scoping exercise. Direct replacement for vague "AI readiness."
2. **"Implementation is the strategy" sharpens [[ai-consulting]] positioning.** The 3Ps offering can claim a seat at *procurement* discussions, not just post-buy implementation — higher-margin engagement scope.
3. **Six-vendor convergence is a content angle.** "Why Anthropic, OpenAI, SAP, Pinecone, Salesforce, and ServiceNow all shipped agent-security responses in the same week" is publishable thought leadership for enterprise buyers.
4. **The McKinsey Lilly + Lindy cases are portable horror stories.** $20 exploit + 22 unauthenticated endpoints + name-brand consultancy (McKinsey Lilly) and "agents started sending unauthorized emails" + named consumer-agent platform (Lindy) are the kind of details that earn enterprise attention. Use sparingly so they don't lose impact.
5. **Pairs naturally with [[work-primitive]]** — the buyer-side / substrate-side pair becomes a 2x2 framework for any AI vendor evaluation: *can it tell humans from agents (procurement) × can the agent commit (substrate)*.
6. **Aligns with [[code-comprehensibility]]** for engineering-leader clients — both treat security as a property emergent from the meaning/identity layer, not bolted-on hygiene.
7. **Judge-layer audit is a productizable consulting deliverable.** "We'll audit your agent system against the four action-risk classes and recommend a judge architecture." Concrete, scoped, defensible. Direct billable engagement scope.
8. **Four-class action taxonomy is a workshop artifact.** Same shape as T/C/L/D — a tag-your-actions exercise leadership teams can run in a 90-minute session. Maps every agent workflow to a risk class, drives architecture decisions.
9. **The permission-ladder × action-class matrix is a packaged framework.** 2D matrix → policy decisions. Concrete enough to be a slide; rich enough to be an engagement. The most defensible 3Ps-original artifact this vault could produce.

## Open questions

- **What did McKinsey actually publish about the Lilly postmortem?** Worth a search — the [[nate-b-jones]] framing may add interpretive layers not in the original.
- **Specific vendor products** — each of the six vendors' responses needs a concrete product name + scope. Worth ad-hoc tracking as they publish.
- **Standardization** — is there a vendor-neutral spec emerging for agent-vs-human identity (analogous to OAuth for auth, OIDC for identity)?
- **Detection — can a buyer test "does it know humans from agents" without vendor cooperation?** What's a buyer-side audit script?
- **Insurance angle** — cyber insurance treats AI agents how? Premium structure as a forcing function?
- **Regulatory angle** — does any regulator (FTC, EU AI Act, NYDFS) require human/agent distinction in production deployments?
- **Lindy postmortem specifics** — what did Lindy actually publish about the unauthorized-emails incident? Their judge architecture's exact shape?
- **Judge-layer reference implementations** — does Anthropic ship a reference judge skill or Mythos-style tool? Does Codex have parity?
- **Judge cost ceiling** — at what action-volume does a frontier judge become economically prohibitive? Are there hybrid patterns (cheap pre-judge + frontier escalation judge)?
- **Multi-turn judge state** — the judge sees user intent + proposed action. Does it see prior judge decisions, or is each invocation stateless? What's the right design for stateful judges?
- **Adversarial judge** — can a prompt-injection attacker that owns the actor's context also poison the judge's intent compilation? What's the isolation boundary?

## Related pages

- [[nate-b-jones]] — author; this is his 7th named framework (with the 2026-05-12 architectural pattern extension)
- [[work-primitive]] — sibling framework (substrate side); Agent Security is the procurement-side complement
- [[code-comprehensibility]] — sibling framework (codebase side); shared "meaning layer" foundation
- [[anticipation-gap]] — sibling framework (user side); permission ladder pairs with four-class action taxonomy as the 2D runtime policy matrix
- [[anthropic]], [[openai]], [[pinecone]] — agent-security responders tracked in this vault
- [[lindy]] — public case study for the judge-architecture pattern (unauthorized-emails incident)
- [[ai-consulting]] — direct sales conversation framework
- [[claude-code]], [[claude-skills]] — coding-agent context where this is most-mature
- [[knowledge-layer]] — sibling sub-month convergence pattern
- [[youtube-digest-apify-2026-05-11]] — primary citation (procurement diagnostic)
- [[youtube-digest-apify-2026-05-12]] — second citation (architectural pattern + judge layer + four-class action taxonomy)
- [[youtube-digest-apify-2026-05-22]] — third citation (kill switch as multi-layer feature in [[infrastructure-control-layer]])
- [[youtube-digest-apify-2026-05-25]] — fourth + fifth citations (harness-thesis extension via [[long-running-benchmarks]] + consumer-facing skill-provenance via [[tristen-obrien]])
- [[long-running-benchmarks]] — judge architecture is one component of the broader harness
- [[tristen-obrien]] — consumer-facing skill-provenance dimension
