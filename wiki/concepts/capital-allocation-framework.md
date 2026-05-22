---
title: Capital Allocation Framework (Automate / Build / Buy / Hire / Wait)
category: concept
summary: [[nate-b-jones]]' 12th named framework — five-lever decision matrix for **per-workflow** AI investment (automate / build / buy / hire / wait); replaces the conventional "we need an AI strategy" consulting deliverable with **workflow-by-workflow capital allocation**; named alongside the **40% Gartner failure prediction** (most agentic AI projects fail because of misallocated lever), the **accounts-receivable example** (same workflow takes different levers at different companies), the **"do not automate what you cannot describe"** failure mode, the **"workflow operating loop"** primitive, and the **IBM AskHR case study**; pairs with [[chief-ai-officer]] as the **role-design** complement to the **career-side** CAIO framing (Nate Herk #4 same batch); decision-side companion to [[agentic-implementation-layer]] (where-value-lives) and [[agent-metering]] (how-pricing-works)
tags: [nate-b-jones, framework, capital-allocation, ai-investment, workflow, automate, build, buy, hire, wait, gartner, ibm-askhr, accounts-receivable, workflow-operating-loop, decision-framework, lever, chief-ai-officer, agentic-implementation-layer, agent-metering]
sources: 1
updated: 2026-05-22
---

# Capital Allocation Framework (Automate / Build / Buy / Hire / Wait)

## What it is

[[nate-b-jones]]' **12th named framework**, from *When to Automate, Build, Buy, Hire, or Wait on AI* (23.3K views, 2026-05-17, 27:46) in [[youtube-digest-apify-2026-05-22]]. A **five-lever decision matrix** for AI investment, applied **per workflow** rather than as a company-wide strategy.

**The framing claim**: *"What's really happening inside AI investment decisions at most companies? The common story is that you need an AI strategy — but the reality is more complicated. AI investment is a capital allocation problem, one workflow at a time."*

## The five levers

| Lever | Best for | Failure mode |
|---|---|---|
| **Automate** | Well-described, repeatable workflows with existing tools available | Automating what you can't describe (chapter 31:52) — the canonical failure |
| **Build** | When **company context** is the differentiator (proprietary domain logic) | Building what's already a commodity primitive |
| **Buy** | **Workflow-vendor** purchases (whole workflows, not primitives) | Buying primitives that should have been built; buying workflows that should have been hired |
| **Hire** | Workflow is critical, **purple unicorns don't exist** (chapter 24:56) | Trying to find one person who does everything; chasing the unicorn |
| **Wait** | Deliberate non-action when the workflow can't be reliably defined yet (chapter 29:36) | Confusing deliberate-wait with default-paralysis |

## Key surrounding claims

### "AI investment is really a workflow question" (chapter 6:49)

The conventional "we need an AI strategy" consulting frame is wrong. There is no single AI strategy — there are **as many lever decisions as there are workflows in the company**. The lever decision is downstream of the workflow, not the company.

### The 40% Gartner failure prediction (chapter 4:49)

Most agentic AI projects fail. The failure mode is almost always **misallocated lever** — building when buying was right, hiring when automating was right, automating when waiting was right. Right execution of the wrong lever still fails.

### The workflow operating loop (chapter 9:52)

Each workflow has an **operating loop**: trigger → inputs → action → outputs → feedback. Capital allocation requires being able to **describe the loop precisely**. Workflows whose loop you can't articulate **are not ready for automation** — the lever for them is **wait**.

### "Do not automate what you cannot describe" (chapter 31:52)

The single canonical failure mode. Premature automation of fuzzy workflows produces:
- Outputs that look right but aren't
- Hidden compounding errors that surface months later
- Maintenance debt as the workflow keeps drifting

### The accounts-receivable workflow example (chapter 7:39)

The **canonical case study** for "same workflow, different lever per company":

| Company shape | Lever | Why |
|---|---|---|
| 5-person SaaS startup | Buy (Stripe + automated dunning) | AR is mostly stable, no proprietary logic |
| 50-person services firm with custom payment terms | Build (custom AR agent) | Payment terms are company-specific differentiator |
| 500-person enterprise with complex collections | Hire (Head of Revenue Operations) + automate subroutines | Complexity demands judgment + delegation |
| Pre-revenue startup | Wait | Can't describe the workflow yet |

The workflow is the same; the lever depends on the **company shape + workflow stakes**.

### IBM AskHR case study (chapter 12:00)

The canonical **automate-lever-done-right** case study. AskHR is IBM's internal HR-agent; well-described workflow (employee asks HR question → routed to authoritative source → response), high volume, low ambiguity. **Automating was the right lever; IBM picked it correctly and shipped at scale**.

### "Build" when company context demands it (chapter 17:13)

Build is the **right** lever when **company-specific context is the differentiator**. Examples: pricing logic with custom tiers, customer-segment-specific workflows, proprietary content-moderation rules. **Wrong** when the workflow is commodity (don't build a CRM, don't build a customer-support copilot from scratch).

### "Buy primitives vs workflows" (chapter 21:36)

The Buy lever splits into two distinct purchase shapes:
- **Primitives** — building blocks (Stripe, Twilio, OpenAI API). Buy these when you'll compose them yourself.
- **Whole workflows** — vendor-shipped end-to-end ([[claude-for-small-business]], Agentforce). Buy these when you don't want to compose.

Buying a primitive when you needed a whole workflow → maintenance burden. Buying a whole workflow when you needed primitives → vendor lock-in + customization limits.

### Hire without chasing the purple unicorn (chapter 24:56)

Hiring for AI workflows fails when companies try to find **one person who** designs the workflow + implements the agent + maintains the integration + handles compliance. **That person doesn't exist** at scale. The right shape: hire the **workflow owner** + automation engineer + buy the rest.

### "Right people in the room" (chapter 3:33)

The lever decision can't be made by IT or the CFO alone. Minimum-viable decision team:
- **Workflow owner** (knows the operating loop)
- **Automation engineer** (knows the tooling)
- **Procurement** (knows the contracts)

Same shape as [[agent-security]]' "developers at the procurement table" argument from [[nate-b-jones]]' 2026-05-10 framework.

## The investment matrix (chapter 34:01)

Per Nate's mention of "the investment matrix and four quadrants" — a 2x2 placeholder structure (axes gated to transcript pull). Likely shape: **workflow well-described (yes/no)** × **company-context-differentiated (yes/no)** → quadrant recommends the right lever.

## Strategic significance

1. **12th [[nate-b-jones]] framework** — extends framework cadence to roughly one named diagnostic per video
2. **Decision-side companion** to [[agentic-implementation-layer]] (where-value-lives) and [[agent-metering]] (how-pricing-works) — together: three frameworks describing the **same enterprise-AI investment cycle from three angles**
3. **The "workflow not strategy" thesis is the anti-AI-strategy positioning** — replaces conventional "AI strategy" consulting deliverables with workflow-by-workflow audits
4. **Pairs with [[chief-ai-officer]]** (Nate Herk #4 same batch) — CAIO framing tells you *which role does this*; capital-allocation framing tells you *what the role does on day one*
5. **Directly portable to 3Ps consulting deliverables** — workflow audit + per-workflow lever recommendation is a **one-day engagement shape**, same as [[plugins]] taxonomy audit and [[agent-metering]] four-question diagnostic
6. **"Do not automate what you cannot describe"** is the cleanest premature-automation guardrail in the vault — pairs with [[anticipation-gap]] consumer-side framing

## Related

- [[nate-b-jones]] — author; 12th framework
- [[chief-ai-officer]] — career-side complement
- [[agentic-implementation-layer]] — where-value-lives counterpart
- [[agent-metering]] — pricing-mechanism counterpart
- [[plugins]] — taxonomy audit counterpart (same one-day deliverable shape)
- [[agent-security]] — procurement-table counterpart (same "right people in the room" argument)
- [[anticipation-gap]] — premature-automation guardrail counterpart
- [[claude-for-small-business]] — example of the "buy whole workflow" lever from this batch
- [[ai-consulting]] — buy-vs-build-vs-hire reframe

## Used in

- [[youtube-digest-apify-2026-05-22]] — primary citation ([[nate-b-jones]] #5)

## Open questions

- The investment matrix's actual 2x2 axes (chapter 34:01) — transcript pull needed
- How does the framework handle **multi-workflow** strategic decisions (e.g., "what platform should we standardize on")? Workflow-by-workflow may not scale to platform choices.
- IBM AskHR case study specifics — what was the actual scale + ROI + timeline?
- Other case studies named beyond accounts-receivable + IBM AskHR (truncated at chapter 38:12)
- Does Nate publish a workflow-audit template downstream (Substack)?
