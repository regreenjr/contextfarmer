---
title: Agent Council (Meet The Council)
category: concept
summary: [[nate-herk]]'s **"Meet The Council"** — a panel of agents that **pressure-tests an idea before you build it** (*Will Anyone Buy? / Reshape Or Kill?*), surfaced in *I asked Claude Code to make me as much money as possible* (43.8K views, 2026-06-25, 28:12). Its purpose is **profit over productivity**: stop pouring build time into things nobody wants by forcing **market validation and dissent up front**. It is built on a deliberate **anti-sycophancy** move — *"Claude's Yes Man" / "Is It Honest?"* — make the model adversarial about your idea instead of agreeable; the multi-agent council exists precisely to supply the dissent a single agreeable model won't. The validation-side complement to his build-then-verify discipline ([[directing-agents]], [[agent-loops]]) and the structured fix for the *"Claude voted yes on everything"* sycophancy failure mode named in [[long-running-benchmarks]]; the agent-native cousin of the **persona/focus-group panel** pattern.
tags: [agent-council, council, nate-herk, will-anyone-buy, reshape-or-kill, anti-sycophancy, yes-man, honesty, market-validation, multi-agent, profit-over-productivity, claude-code, opus-4-8, directing-agents, agent-loops, long-running-benchmarks, persona-panel, ai-question-method, portable-judgment]
sources: 1
updated: 2026-06-26
---

# Agent Council (Meet The Council)

## What it is

From [[nate-herk]]'s *I asked Claude Code to make me as much money as possible* (43.8K views, 2026-06-25, 28:12, chapter **2:49 "Meet The Council"**). **The Council** is a **panel of agents convened to judge an idea before you commit build time to it.** Instead of asking one model "help me build X" (and getting an agreeable yes), you put X in front of a council that asks the questions a buyer would:

- **Will Anyone Buy?** (3:55) — market validation: is there a real buyer, or is this productive-looking work with no demand behind it?
- **Reshape Or Kill?** (5:35) — a verdict, not a vibe: the idea survives only if it can be reshaped into something someone pays for; otherwise it dies here, cheaply, before the build.

The council is the **front-end gate** in the video's larger *"profit over productivity"* thesis (chapter 1:03, *Productive Or Profitable?*): most operators *"burn their time and money on stuff that was never going to work,"* and a single agreeable model accelerates that mistake rather than catching it.

## The anti-sycophancy foundation

The council only works because of a prior move: **make the model honest, not a yes-man.** Chapters 1:53 (**Claude's Yes Man**) and 2:19 (**Is It Honest?**) name the default failure — the model *agrees with whatever you bring it*, so its encouragement is worthless as a signal. The fix is to instruct it to be **adversarial about your idea**, and then to **multiply that adversarial stance across several agents** so the dissent is structural, not dependent on one prompt holding.

This is the **operator-side use of [[opus-4-8]]'s "honesty upgrade"** — the model is *more candid about uncertainty* by default; the council weaponizes that candor into a buy/kill decision. It is also the first creator video to turn the *"Claude voted yes on everything"* polite-agreement failure mode (named in [[long-running-benchmarks]]) into a **deliberate countermeasure**: if one agent will rubber-stamp, convene a council that won't.

## Where it sits in the vault

- **The validation-side complement to build-then-verify.** Nate's recurring discipline is *don't trust the model's output* — [[directing-agents]] ("make the agent prove its work"), [[agent-loops]] (a checkable "done" beats trusting output). The Council pushes that skepticism **upstream of the build**: don't trust the model's *enthusiasm for the idea* either. Verify the demand before you verify the code.
- **The structured fix for sycophancy.** [[long-running-benchmarks]] surfaced *"Claude voted yes on everything"* as a trajectory-level failure (possibly an RLHF artifact); [[opus-4-8]] shipped an honesty upgrade as the model-side response; the Council is the **workflow-side response** — multi-agent dissent so no single agreeable pass decides.
- **The agent-native cousin of the persona/focus-group panel.** A council that asks "will anyone buy?" is the same primitive as a **synthetic buyer panel** run before spend (cf. the vault's persona-panel / roofer-panel tooling) — here generalized to *any* idea and run as part of the [[claude-code]] build loop, not as a separate research step.
- **A "senior partner, not yes-man" instance of [[ai-question-method]].** [[nate-b-jones]]' questioning discipline reframes AI as a **senior partner who pushes back**; the Council operationalizes exactly that with multiple partners voting reshape-or-kill.
- **Judgment over tooling.** The lever is **deciding what's worth building**, not a new feature — consistent with his [[ai-consultant-roadmap]] *"tools mean nothing"* thesis and [[nate-b-jones]]' [[portable-judgment]].

## Why it matters for 3Ps

- **A teachable pre-build gate.** "Convene a council, ask will-anyone-buy, get a reshape-or-kill verdict" is a clean, sellable discipline for operators who over-build and under-validate — the exact failure the video opens on.
- **Anti-sycophancy is a billable correction.** Most operators take the model's encouragement as a green light; naming the yes-man problem and supplying a structured dissent mechanism is hard-won operator knowledge a 3Ps engagement can encode.
- **Market validation moves inside the build loop.** Folding "will anyone buy?" into Claude Code (rather than a separate research phase) is the kind of throughput compression the vault's farming + AIOS patterns favor.

## Open questions

- **Exact composition** — how many agents are in the Council, what roles (skeptic / buyer / pricer / competitor), and how is the reshape-or-kill verdict aggregated (majority vote, any-veto)? Gated to the video.
- **Is it a skill, a subagent team, or a prompt?** Whether the Council ships as a reusable [[claude-skills|skill]] / [[claude-subagents|subagent]] team or is a manual multi-prompt routine is unresolved — would determine reusability.
- **How adversarial without nihilism?** A council tuned to kill everything is as useless as a yes-man; the calibration between honest dissent and reflexive rejection is not specified.

## Used in

- [[youtube-digest-apify-2026-06-26]] — vault entry point (Nate Herk #1)
- [[nate-herk]] — author

## Related

- [[opus-4-8]] — the honesty upgrade the Council turns into an anti-yes-man posture
- [[long-running-benchmarks]] — the "Claude voted yes on everything" sycophancy failure mode this counters
- [[directing-agents]] — build-then-verify; the Council is its validation-side, pre-build complement
- [[agent-loops]] — runtime verification (a checkable "done")
- [[ai-question-method]] — "AI as senior partner, not yes-man" — the Council operationalized
- [[ai-consultant-roadmap]], [[portable-judgment]] — judgment over tooling
- [[claude-code]] — substrate; the Council runs inside the build loop
