---
title: Free Sample Phase
category: concept
summary: [[nate-herk]]'s 2026-05-13 framing for the substrate-economics moment in AI tooling — "the real product isn't the subscription, it's you"; when Anthropic passed OpenAI in business adoption (per Ramp/EconLab), within hours both labs dropped lock-in offers (Codex 2 months free, Claude Code +50% limits); the strategic play is to use it like crazy while building projects flexible enough to swap tools the day pricing resets; same industry pattern as cloud / mobile-OS / streaming wars; the substrate-economics counterpart to [[skill-systems]] / vendor-agnostic positioning at the architecture layer
tags: [free-sample-phase, anthropic, openai, codex, claude-code, lock-in, business-adoption, substrate-economics, vendor-agnostic, training-data, nate-herk, ramp, econlab]
sources: 1
updated: 2026-07-05
---

# Free Sample Phase

## Definition

The strategic phase in a contested AI-tooling market where **the vendor's product is not the subscription — it's the user**. Free tiers, rate-limit upgrades, and 2-month-free promos exist to **capture behavior data** that improves the model and locks in switching costs. The smart play is **maximizing free-tier usage while building tooling flexible enough to swap vendors on pricing resets.**

Named by [[nate-herk]] in *Anthropic Just Dethroned OpenAI. Here's What Happens Next.* (48.4K views, 2026-05-13, 7:43, [[youtube-digest-apify-2026-05-14]] #5).

## Origin / triggering event

Two simultaneous things in mid-2026-05:

1. **[[anthropic]] passed [[openai]] in business adoption for the first time** (per a Ramp/EconLab article cited in the video description — "Ramp article: `econlab.substack.com/p/anthro...`")
2. **Within hours of the Ramp data dropping, both labs ship retention offers**:
   - **[[codex]]**: 2 months free (description: "Free Codex application form: `openai.com/form/codex-enterpr...`" — Codex Enterprise)
   - **[[claude-code]]**: rate limits bumped by **50%**

## The five-chapter argument

| Chapter | Time | Claim |
|---|---|---|
| Anthropic Passes OpenAI | 0:00 | Business-adoption flip is the unlock event |
| The Free Sample Phase | 0:55 | What's happening: free samples → lock-in |
| **You're the Training Data** | 2:01 | Why: user behavior is the actual asset |
| The Industry Pattern | 4:18 | Where: cloud / mobile / streaming all did this |
| How to Actually Play It | 5:08 | What to do: use heavily, build to swap |
| Final Thoughts | 6:32 | (Closing) |

## Core claims

### "The real product isn't the subscription — it's you" (chapter 2:01)

The vendor's monetization model isn't the subscription fee. The fee is roughly cost-recovery. The **actual asset** is:

- **Training data** — every prompt, edit, and acceptance signal feeds the next model
- **Switching cost moat** — operators who've built workflows on Vendor A's quirks have a sunk cost in staying
- **Distribution lock-in** — usage of the tool generates content (videos, tutorials, skills) that locks the ecosystem to Vendor A

This frame inverts the user's mental model. The user thinks they're *paying* for the tool; they're actually *being monetized* for the tool. The free tier looks generous because the data is the product.

### "The Industry Pattern" (chapter 4:18)

[[nate-herk]] names this as a *recurring* pattern, not a 2026-only event. Likely analogues (specifics gated to video, but plausible):

| Era | Free sample phase | Lock-in result |
|---|---|---|
| Cloud (2010-2015) | AWS free tier, Azure free tier | Workloads migrate to one cloud, switching is expensive |
| Mobile OS (2007-2012) | iPhone subsidies, Android free | App ecosystems lock developer time |
| Streaming (2018-2022) | Free trials, multi-month promos | Catalog content + family-account inertia |
| **AI coding agents (2026)** | **Codex 2 months free, Claude Code +50% limits** | **Skill libraries + workflows + memory state lock to one vendor** |

### "How to Actually Play It" (chapter 5:08)

The recommended operator move:

> "Use it like crazy, but build projects flexible enough to swap tools the day pricing resets."

Two parts:

1. **Use heavily** — extract maximum value during the free-sample phase; the data the vendor gets is sunk anyway
2. **Build to swap** — keep the *architecture* vendor-agnostic so the day pricing resets (the inevitable monetization shift), migration is cheap

This is the **substrate-economics counterpart** to the architectural vendor-agnostic patterns this vault tracks:

| Layer | Vendor-agnostic principle | Voice |
|---|---|---|
| Architecture (Skills) | [[skill-systems]] — composition, modular | [[simon-scrapes]] |
| Architecture (CLI vs MCP) | [[printing-press]] — CLIs portable across substrates | [[nate-herk]] (separately) |
| Architecture (cross-vendor) | [[claude-skills]] / [[codex]] symmetry | Vault-level analysis |
| **Economics** | **[[free-sample-phase]] — build to swap when pricing resets** | **[[nate-herk]]** |

## Strategic significance

### First substrate-economics framework in this vault

The vault tracks architectural / behavioral / procurement / security / commerce frameworks. **This is the first economics-of-the-substrate framework** — names the *vendor business model* layer that determines when free tiers tighten.

Pairs with [[nate-b-jones]]'s [[openclaw]] runtime-reframe (2026-05-10) — same intuition ("model choice is not permanent, workflows that outlive providers win") arrived at from a different angle.

### Anthropic-passes-OpenAI is the singular flip event

The 2026-05-13 business-adoption flip is the **first time in the LLM era** that Anthropic was ahead. Prior to this, OpenAI led every meaningful adoption metric. The lock-in offers within hours confirm both labs see this as a **defendable / contestable** moment, not a permanent shift.

This is structurally similar to:
- AWS vs Azure (cloud lead shifted 2015-2020)
- Google search vs Bing (search lead never shifted)
- iOS vs Android (mobile lead shifted by metric)

If the Anthropic lead consolidates, this becomes a "Lehman moment" for OpenAI's frontier-model leadership. If OpenAI claws it back, the free-sample-phase wars intensify.

### The Codex 2-months-free offer changes Codex economics

Earlier [[codex]] coverage framed it as the "underserved alternative substrate" (the lower-view Nate Herk Codex course was the entry signal). 2 months free **makes Codex a credible head-to-head substrate** for free-tier experimenters who would otherwise default to Claude Code on the "trying everything" path.

Implication: cross-vendor Skills / Plan Mode / Routines experimentation just got cheaper for the next 2 months. Expect more cross-vendor creator content in the 2026-07 timeframe.

### Claude Code +50% limits is the *third* limit increase in two weeks

Sequence:
- 2026-05-07: SpaceX deal **doubled** 5-hour rate limits ([[nate-herk]] #9 in [[youtube-digest-apify-2026-05-10]])
- 2026-05-13: Additional **+50%** retention boost (this video)

Total Claude Code rate-limit increase across two weeks: roughly **3x baseline**. Substantively changes:

- [[brad-bonanno]]'s context-bloat optimization argument (still useful, but less urgent at 3x baseline)
- 3Ps client cost projections (Claude Code Plus/Pro substantially cheaper to run per-task)
- Any user behavior gated on rate limits (e.g., multi-session parallel work per [[claude-code-levels]] Level 5)

## Why it matters for 3Ps

### Pricing-stability talking point

For any 3Ps client conversation that hinges on "will the pricing change," the [[free-sample-phase]] frame provides a **vendor-acknowledged answer**: yes, pricing will change. Build accordingly.

### Architecture choice rationale

The 3Ps deliverable should be **cross-vendor by default**. The [[skill-systems]] + [[printing-press]] + vendor-neutral [[claude-skills]] patterns are not theoretical purism — they're **insurance against the inevitable pricing reset.**

### Educational on-ramp arbitrage

While Codex is 2 months free, the cost differential for a multi-substrate consulting deliverable drops to near-zero. A 3Ps client engagement can include **both** Claude Code and Codex demonstrations at minimal incremental cost. The 2-month window is the on-ramp arbitrage.

### Distribution capture warning

The user's vault, skills, and farmer architecture **are themselves training data** that compounds Anthropic's lead. The vault doesn't have a quick way to *be* vendor-agnostic at the data layer — every farm tick deepens the Anthropic-specific implementation. The architectural cross-vendor patterns are the *output-layer* hedge, not a substrate-layer hedge.

Open question: should the vault explicitly run on [[codex]] periodically to maintain bidirectional substrate competence? Especially during the 2-months-free window?

## Contrasts with

- **[[anticipation-gap]]** — Nate B Jones' consumer-AI framework about *user invocation*; [[free-sample-phase]] is about *vendor economics*. Both describe substrate-side dynamics from different angles.
- **[[openclaw]]** runtime reframe ([[nate-b-jones]] #8 in [[youtube-digest-apify-2026-05-10]]) — same "workflows outlive providers" thesis, different scaffolding (runtime layer vs economic phase)
- **[[skill-systems]]** ([[simon-scrapes]]) — architectural vendor-agnosticism; [[free-sample-phase]] is economic vendor-agnosticism. Complementary.

## Open questions

- **When does the free-sample phase end?** — Nate Herk says "the day pricing resets," but doesn't predict when. Historical analogues (AWS, iOS) suggest 3-7 years; AI may compress to 18-24 months
- **What does a "pricing reset" look like in this market?** — Usage-based metering replacing flat-fee? Plan tier consolidation? Pulled free tiers? Watching for signals
- **Does the Anthropic-passes-OpenAI flip stick?** — Need 2-3 more months of Ramp data
- **Will the Codex 2-months-free actually convert to retained users?** — Empirical question; will resolve by 2026-08
- **Is "you're the training data" literal (model training) or behavioral (data leverage for product)?** — Anthropic's published policy on training-on-customer-data needs revisiting

## Why this concept page (not just an [[anthropic]] / [[openai]] update)

The framing transcends either vendor. It's a substrate-economics pattern. The same logic will apply to whoever ships AI coding agents in 2027 (Google? Meta? Open-source replicas?). Concept page level is the right home.

## Related pages

- [[anthropic]] — passed OpenAI in business adoption; +50% Claude Code limits
- [[openai]] — lost business-adoption lead; Codex 2 months free
- [[claude-code]] — primary affected substrate (rate-limit increase)
- [[codex]] — primary affected substrate (free promo)
- [[nate-herk]] — primary author; ninth Claude Code-ecosystem framework
- [[openclaw]] — adjacent runtime reframe ([[nate-b-jones]])
- [[skill-systems]], [[printing-press]] — architectural vendor-agnostic patterns
- [[free-sample-phase]] is the economic-layer companion
- [[youtube-digest-apify-2026-05-14]] — primary citation

## Used in

- [[youtube-digest-apify-2026-05-14]] — primary citation ([[nate-herk]] #5)
- [[anthropic]], [[openai]], [[claude-code]], [[codex]] — substantively affected pages
- [[ai-consulting]] — vendor-agnostic positioning rationale
- [[sources/youtube-digest-apify-2026-07-05]]
