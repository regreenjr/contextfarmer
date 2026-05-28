---
title: Public AI Work (Apprenticeship Gap / Polanyi's Paradox)
category: concept
summary: [[nate-b-jones]]' 22nd named framework (2026-05-26, 18.8K views) — the **organizational-learning framework**: AI adoption is *not* a tooling problem you solve by buying licenses; your most valuable AI work is **invisible** (done in private DMs), and that invisibility widens an **apprenticeship gap** — juniors can't watch seniors use AI, so tacit knowledge never transmits (**Polanyi's paradox**: we know more than we can tell, and a prompt library can't capture it); unlock event is **Shopify's "River" agent running only in public Slack channels** (deliberately watchable); **tooling choices are frontier choices** (Slack public-channel-native vs Teams/Copilot DM-native shapes observability); the fix is **declared spaces + senior people willing to run real work where everyone can watch**; reframes [[context-farming]] / [[karpathy-llm-wiki]] as organizational apprenticeship infrastructure; org-design-side complement to his worker-side T/C/L/D and the [[agent-substrate]] thesis
tags: [public-ai-work, apprenticeship-gap, polanyi-paradox, tacit-knowledge, shopify, river-agent, slack-vs-teams, copilot, declared-spaces, senior-people, observable-work, organizational-learning, prompt-library-insufficient, tooling-is-frontier, nate-b-jones, agent-substrate]
sources: 1
updated: 2026-05-28
---

# Public AI Work (Apprenticeship Gap / Polanyi's Paradox)

[[nate-b-jones]]' **22nd named framework** — *Shopify CEO Reveals Their Secret AI Developer* ([[youtube-digest-apify-2026-05-28]] #2, 18.8K views, 2026-05-26, 16:24). The **organizational-learning framework** for why most companies get *faster* with AI but not *smarter*.

## The framing claim

> *"What's really happening inside companies that are actually getting smarter with AI, not just faster? The common story is that AI adoption is a tooling problem you solve by buying licenses, but the reality is more complicated."*

Adoption isn't a licensing problem — it's a **visibility** problem. *"Your most valuable AI work is invisible"* because it happens in private chats, so the organization never learns from it.

## The unlock event: Shopify's "River" agent (chapter 09:03)

Shopify's internal AI developer agent (**"River"**) is **deliberately constrained to run only in public Slack channels** — never in DMs. The design choice *makes the work watchable*: every prompt, correction, and result is observable by the whole team. That deliberate publicness is the framework's canonical positive example.

## The apprenticeship gap (chapter 05:46)

The structural failure mode:

- Senior people do their **best AI work in private DMs** (faster, less self-conscious, no audience)
- Juniors **can't watch** → can't learn the judgment, the corrections, the "when not to trust it"
- The gap between *who can use AI well* and *who is learning to* **widens** over time
- This is the inter-generational analog of the [[chief-ai-officer]] 61-point adoption gap — but *inside the team*, between senior and junior

Private AI fluency compounds privately; the org doesn't get smarter, only the individual does.

## Polanyi's paradox (chapter 07:30)

The reason a prompt library doesn't fix this (chapter 11:00, *"why a prompt library isn't enough"*):

- **Polanyi's paradox** — *"we know more than we can tell."* The way an expert *uses* AI (which output to trust, when to push back, how to frame the follow-up) is **tacit knowledge**.
- Tacit knowledge transmits by **observation**, not by documentation. A library of saved prompts captures the *artifact* but not the *judgment* that produced it.
- Therefore the only transmission mechanism is **watching the work happen** — which requires the work to be public.

## Tooling choices are frontier choices (chapter 04:45)

A sharp substrate claim: the collaboration tool you pick **shapes whether AI work is observable**.

| Substrate | Default surface | Observability |
|---|---|---|
| **Slack** | Public channels (River-native) | High — work is watchable by default |
| **Teams / Copilot** | DM + private threads | Low — work happens out of view |

Picking Slack vs Teams isn't just a UX preference — it's a **frontier choice** about whether your organization can run the apprenticeship loop at all. This extends the [[agent-substrate]] thesis (boring tools become strategic) to the *collaboration-tool* layer: the substrate determines organizational learning capacity.

## What public AI work looks like (chapters 09:03–15:00)

The actionable core:
- **Four parts of AI work to make visible** (specifics gated to transcript) — the prescriptive checklist.
- **Building a public AI workflow** (chapter 13:28) — operationalize the watchable loop.
- **Privacy, declared spaces, and senior people** (chapter 15:00) — regulated teams (healthcare, finance, legal) can *still* expose work safely via **declared/sanctioned channels** that meet compliance while staying watchable. The non-negotiable unlock: **senior people willing to run actual work where everyone can watch** — public AI work fails if leaders keep their best work private.

## Where it sits in [[nate-b-jones]]' framework stack

- **Org-design-side complement to T/C/L/D** (his 1st framework) — T/C/L/D diagnoses *which work survives AI* at the individual level; Public AI Work diagnoses *how the organization learns AI* at the team level.
- **Extends the [[agent-substrate]] thesis** — Slack-as-observable-substrate is a new instance of "boring tools become strategic in the agent era."
- **Trust/reliability pair with [[document-truth-layer]]** (his 23rd framework, same batch) — Document Truth Layer = trust in the *deliverable*; Public AI Work = trust + learning in the *organization*.
- **Reframes this vault's own architecture** — [[context-farming]] + [[karpathy-llm-wiki]] are, in effect, *public AI work infrastructure*: a watchable, append-only record (the `log.md` timeline, the cross-referenced wiki) of how the operator actually uses AI. The vault is the apprenticeship artifact the framework prescribes.

## Why it matters for 3Ps

- **A net-new consulting deliverable: the "public AI workflow" audit** — diagnose where a client's AI work is happening privately, map the apprenticeship gap, and design declared/watchable channels. Pairs with the T/C/L/D "tag your week" audit as a leadership-team intake artifact.
- **Substrate-selection advisory** — "tooling choices are frontier choices" makes Slack-vs-Teams a *strategic* question 3Ps can advise on, not just an IT preference.
- **Reframes the vault-as-deliverable pitch** — a 3Ps engagement can position the [[karpathy-llm-wiki]] + [[context-farming]] build as the client's **organizational apprenticeship layer**, not just a knowledge base.
- **Regulated-industry angle** — the declared-spaces mechanic is the compliance-safe path to public AI work for healthcare/finance/legal, the same verticals flagged as high-opportunity for [[chief-ai-officer]].

## Open questions

- **The four "parts to make visible"** — gated to the Substack post; transcript ingest needed for the exact checklist. Confirm no overlap with [[document-truth-layer]]'s four *stages*.
- **River agent specifics** — is "River" a named Shopify product, an internal codename, or Nate's framing? First Shopify-internal-agent reference in the vault; may warrant a Shopify entity stub if it recurs.
- **Does observability degrade speed?** — public work has an audience-cost (self-consciousness, slower iteration). The framework asserts the learning payoff dominates; empirically open.

## Related pages

- [[nate-b-jones]] — framework author (22nd named framework)
- [[youtube-digest-apify-2026-05-28]] — primary source
- [[document-truth-layer]] — same-batch trust/reliability framework (deliverable side)
- [[agent-substrate]] — boring-tools-become-strategic thesis, extended to the collaboration-tool layer
- [[chief-ai-officer]] — the 61-point org-wide adoption gap; Public AI Work names the *intra-team* version
- [[context-farming]], [[karpathy-llm-wiki]] — reframed as organizational apprenticeship infrastructure
- [[claude-code]] — substrate; Channels (Slack/Telegram) are the observable-work surfaces this framework cares about
