---
title: Model Routing (Start With the Job, Not the Model)
category: concept
summary: [[nate-b-jones]]' practical **model-picker** framework (*Stop Wasting Money on the Wrong AI*, 11.1K views, 2026-07-02) — the prescriptive, per-job companion to his [[harness-over-model]] thesis; *"the common story is that the smartest model wins; the real question is which intelligence a specific job actually needs"* — so you **start with the job, not the model**, route familiar/repeatable work to a **cheap workhorse** ([[glm|GLM 5.2]]) and review it fast, keep a **frontier model** for when the *shape of the job is unclear* (*"[[claude-fable-5|Fable]]-style problems that need the strongest model"*), and hand specific jobs to **specialists** (images, video, live web, coding harnesses); the durable move is *"keep your context portable"* so *"no single model going away can stall your work"* — the [[context-wars]] posture stated as an operator habit.
tags: [nate-b-jones, framework, model-routing, model-picker, route-by-the-job, workhorse-model, daily-driver, frontier-model, specialists, portable-context, harness-over-model, glm, glm-5-2, claude-fable-5, opus-4-8, context-wars, substrate-economics, cost-control, model-selection]
sources: 1
updated: 2026-07-04
---

# Model Routing

## Definition

[[nate-b-jones]]' **practical model-picker** framework, from *Stop Wasting Money on the Wrong AI* (11.1K views, 2026-07-02, 14:17) in [[sources/youtube-digest-apify-2026-07-03]]. The framing problem: *"every AI model suddenly looks replaceable, and picking the right one has turned into a second job."* The reframe:

> *"The common story is that the smartest model wins. The real question is which intelligence a specific job actually needs."*

So the discipline is **route by the job, not the model** — match the *shape of the work* to the right class of model instead of defaulting to the highest-scoring one and overpaying, or drowning in model names.

This is the **prescriptive, per-job companion** to his [[harness-over-model]] framework: where harness-over-model made the *argument* (a stronger benchmark score does not make a model your daily driver), model-routing ships the *decision matrix*.

## The routing rules

| Route to | For which work | Notes |
|---|---|---|
| **Cheap workhorse** ([[glm|GLM 5.2]]) | Familiar, repeatable work | *"Route familiar work to cheaper models and review it fast"* (chapter 02:28). Distinct from your daily driver. |
| **Daily driver** | Everyday work where the harness matters | *"Your daily driver and why the harness matters"* (03:53) — a harness decision, not just a model choice. |
| **Frontier model** | When the **shape of the job is unclear** | *"When to pay for a frontier model"* (03:25) — pay up only for genuine uncertainty. |
| **Strongest model** ([[claude-fable-5|Fable]]) | *"Fable-style problems that need the strongest model"* | The hard 20% — reserve the top model for it (chapter 04:47). |
| **Specialists** | *"images, video, live web, and coding harnesses"* | Specific jobs where a purpose-built model beats a generalist. |

## The framing claim

> *"The models will keep changing, but if you route by the job and keep your context portable, no single model going away can stall your work."*

The load-bearing habit is **keep your context portable** — the operator-side statement of the [[context-wars]] / [[glm]]-last-mile thesis. If your work lives in a portable context (files, harness, skills) rather than trapped inside one vendor's model, model churn becomes a routing decision instead of a migration.

## The empirical posture

The chapters open on *"why picking an AI model suddenly got hard"* (00:00), lead with *"start with the job, not the model"* (01:42), and close on *"test any model on your own w[ork]"* (05:40). The prescription is to **test models on your own work** rather than trust benchmarks — the same don't-trust-the-leaderboard instinct behind [[harness-over-model]] and [[long-running-benchmarks]].

## Contrasts with

- [[harness-over-model]] — the *argument* this framework operationalizes. Harness-over-model says the score doesn't make a daily driver; model-routing says *here is the picker*.
- Benchmark-driven model selection — the thing it argues against: *"the smartest model wins"* is the story it replaces.

## Where it sits in the vault

- **The decision-matrix payoff of [[harness-over-model]]** — same author, sharpened from thesis into a per-job routing guide.
- **[[glm|GLM 5.2]] gets its canonical role**: the *cheap workhorse* for familiar, repeatable work — the demand-side use case for the model [[nate-herk]] proved routes into the [[claude-code]] harness ~5× cheaper than [[opus-4-8|Opus]].
- **A substrate-economics lever** — joins [[prompt-caching]], [[claude-subagents]], and [[glm]] in the 2026 "manage your token spend" cluster: down-route the familiar 80%, reserve frontier for the hard 20%.
- **[[context-wars]] as an operator habit** — *"keep your context portable"* is the personal-workflow instance of the own-the-context macro thesis.

## Why it matters for 3Ps

- **A billable deliverable shape** — a client-specific routing matrix ("which model for which job, harness-fit-weighted, cheap-workhorse for the familiar 80%") is the same consulting artifact as his [[capital-allocation-framework]] five levers or [[agent-metering]] four-question diagnostic.
- **Direct cost control** — routing the repeatable majority to a cheap workhorse and reviewing fast is a configurable, defensible optimization most clients won't build themselves.
- **De-risks vendor churn** — the *portable context* prescription is exactly the work of making a client resilient to any single model going away.

## Open questions

- **The full routing guide** — the specific per-job rules are gated to his Substack (`natesnewsletter.substack.com`).
- **How this differs from the [[harness-over-model]] routing table** — both ship a "which model when" matrix; the boundary between the two frameworks is one to watch as his cadence continues.
- **Where the cheap-workhorse line actually falls** — the "review it fast" caveat implies workhorse output needs checking; which work classes can't be down-routed at all?

## Used in

- [[sources/youtube-digest-apify-2026-07-03]] — vault entry point (Nate B Jones #1)
- [[nate-b-jones]] — author; the prescriptive picker for his [[harness-over-model]] thesis

## Related

- [[harness-over-model]] — the thesis this operationalizes into a decision matrix
- [[glm]] — the canonical *cheap workhorse* for familiar, repeatable work
- [[claude-fable-5]] — the *strongest model* reserved for the hardest problems
- [[opus-4-8]] — the frontier tier the workhorse undercuts
- [[context-wars]] — *"keep your context portable"* is this thesis as an operator habit
- [[prompt-caching]], [[claude-subagents]] — fellow substrate-economics / cost levers
- [[long-running-benchmarks]] — the shared don't-trust-the-benchmark, test-on-your-own-work posture
- [[reusable-agent-skeleton]]
