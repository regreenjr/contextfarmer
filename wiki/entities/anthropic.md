---
title: Anthropic
category: entity
summary: AI lab behind Claude / Claude Code / Claude Skills / MCP / Mythos / Skill Creator; 2026 strategy is layering Claude into other vendors' apps + rumored Atlassian acquisition + SpaceX compute partnership (2026-05) doubling Claude Code rate limits; 2026-05-06 FB ads batch shows zero static narrative copy; in 2026-05-10 Mythos AI code reviewer enters this vault via Mozilla's 271-vulnerability cycle; in 2026-05-11 named as a six-vendor agent-security responder alongside OpenAI/SAP/Pinecone/Salesforce/ServiceNow and Skill Creator gets first-hand walkthrough via Chase AI; **in 2026-05-13 passes [[openai]] in business adoption for the first time** (per Ramp/EconLab) — and within hours bumps Claude Code rate limits another **+50%** as a retention play; this is the **third Claude Code rate-limit increase in two weeks** (SpaceX deal doubled limits 2026-05-07 + 50% retention boost 2026-05-13 = roughly 3x baseline); 2026-05-14 ads batch surfaces **first new Anthropic ad since 2026-05-06** — placeholder carousel (started 2026-05-11) confirms catalog-ads-only AI-lab pattern across 2 distinct launch windows; 2026-05-15 batch returns 0 new ads — Anthropic **returns to silence** after the single 2026-05-11 carousel, no follow-up cluster yet (either one-off launch or slow-cluster pacing); **in 2026-05-15 ([[nate-b-jones]] [[agentic-implementation-layer]] framework) named alongside [[openai]] as axis-1 player in the four-axis squeeze — both labs explicitly standing up deployment companies rather than relying on partners**, capturing implementation revenue rather than just inference; this is the upstream cause of the [[free-sample-phase]] retention war (labs converting model-tier users into deployment-tier customers)
tags: [organization, ai-lab, anthropic, claude, claude-code, enterprise, ads, mythos, spacex, code-comprehensibility, skill-creator, agent-security, business-adoption, ramp-data, rate-limits, free-sample-phase, agentic-implementation-layer, deployment-company, axis-1, four-axis-squeeze]
sources: 8
updated: 2026-05-15
---

# Anthropic

## What it is
AI lab. Maker of the Claude model family, [[claude-code]], [[claude-skills]], and the [[mcp]] standard. Founded 2021 by ex-OpenAI researchers (Dario & Daniela Amodei et al). Headquartered in San Francisco.

## Why it matters for this wiki
The user's entire stack runs on Anthropic primitives: Claude Code (this vault), Claude Skills, MCP servers, sub-agents, Routines. Anthropic's product/strategy moves directly determine the substrate the 3Ps offering builds on. 2026 is shaping up as the year Anthropic transitions from "best coding model" to "enterprise infrastructure provider."

## 2026 strategy signals (from [[youtube-digest-apify-2026-05-03]])

### Layering inside other vendors' apps
- **Microsoft is testing Claude against its own Copilot** ([[nate-b-jones]] #16) — implies Microsoft sees Claude as competitive enough on coding tasks to evaluate as a Copilot backend
- **Salesforce Headless 360** ([[nate-b-jones]] #2) — Claude showing up inside Salesforce flows
- **Perplexity Personal Computer** — another surface

The framing per [[nate-b-jones]]: Anthropic's strategy is *layering* (be the model inside other vendors' UX) more than *destination* (own the chat surface).

### Acquisition rumor
- **Anthropic might buy Atlassian for $40B** ([[nate-b-jones]] #8, 2026-05-02) — would put Anthropic on top of Jira/Confluence, the canonical enterprise issue-tracker substrate that's becoming [[agent-substrate]]
- Strategic logic: agents need durable state, ownership, permissions, history — exactly what issue trackers were built for

### Product surface area
- **[[claude-code]]** — CLI/agent tool; the dominant developer-facing surface
- **[[claude-skills]]** — reusable procedural-knowledge units; "Agent Skills Explained" (#4) is the official explainer (201K views)
- **[[mcp]]** — the open standard for tool/data integration
- **[[claude-design]]** — Anthropic's design tool (covered in [[nate-herk]] #18)
- Skill marketplace — Anthropic-distributed via `claude-plugins-official`

## 2026-05-10 product surface expansions

### SpaceX compute partnership (per [[nate-herk]] #9 in [[youtube-digest-apify-2026-05-10]])

87.7K-view coverage in days — the highest-views entry in the 2026-05-10 batch:

- **Doubled Claude Code's 5-hour rate limits**
- **Killed the peak-hours throttle**
- **Raised API rate limits across the board**
- **SpaceX compute partnership** — non-Big-Three compute supplier; strategic diversification

Implications:
- The [[brad-bonanno]] context-bloat / token-rationing optimization argument loses some urgency; raw allowance has gone up
- [[claude-code]] operational headroom roughly doubled overnight
- For 3Ps: clients on Claude Code Plus/Pro got cheaper-to-run stacks without action — useful talking point

### Anthropic Mythos (per [[nate-b-jones]] #12 in [[youtube-digest-apify-2026-05-10]])

First appearance of **Mythos** — Anthropic's AI code-review tool — in this vault. [[mozilla]] pointed Mythos at Firefox and shipped fixes for **271 vulnerabilities in a single release cycle**.

Strategic significance:
- If Mythos becomes the canonical AI code reviewer, Anthropic captures another **infrastructure layer** (above the model, below the application) — same shape as their [[mcp]] play
- "A good human engineer wrote this" is becoming a much weaker security claim ([[code-comprehensibility]])
- Open: is Mythos public-facing, internal Anthropic, or something else? Worth verification
- Adds AI security tooling to Anthropic's surface area beyond pure model + Code

### Skill Creator first-hand walkthrough (per [[chase-ai]] #2 in [[youtube-digest-apify-2026-05-11]])

107K-view canonical first-hand demo of [[skill-creator]] — Anthropic's meta-skill that tests, benchmarks, and optimizes other skills using:

- **Plain-language evals** (no test harness scaffolding required)
- **Blind A/B testing** (skilled vs unskilled baseline on same input)
- **Description-field optimization** (iterates the skill's invocation-trigger description)

Strategic significance:
- Continues the **infrastructure-for-AI-builders** pattern (Skill Creator + Mythos + Anthropic SDK + claude-plugins-official) — Anthropic is increasingly shipping tools *for the people building on its substrate*, not just for end-users
- Cements [[claude-skills]] as **testable software** — skills get an acceptance test, like unit-tested code; the [[dubibubii]] "500K skills, 95% useless" claim becomes empirically falsifiable
- [[chase-ai]] also names the **two-types skill split** (capability uplift vs encoded preference) — the eval-target categorization Anthropic's own authoring guide didn't ship

### Agent-security responder (per [[nate-b-jones]] #1 in [[youtube-digest-apify-2026-05-11]])

In the McKinsey "Lilly" agent-exploit aftermath, Anthropic shipped a response in the same week as five other vendors:

| Vendor | Likely response shape |
|---|---|
| [[anthropic]] | Agent-aware identity primitives in [[claude-code]] / [[mcp]] |
| [[openai]] | Codex / API agent-auth surface |
| SAP | Authority-moat reinforcement |
| [[pinecone]] | Knowledge-layer access control (Nexus authorization) |
| Salesforce | Agentforce identity model |
| ServiceNow | Agent-aware ITSM approval gates |

The six-vendor convergence-in-one-week is the same shape as the [[knowledge-layer]] convergence ([[pinecone]] / Microsoft / Google in 4 weeks). Sub-month convergence cadence is now the new normal for major architectural shifts.

The buyer-side question this addresses: **"does your platform know humans from agents?"** Anthropic's response shape is presumably distinct agent identity primitives in Claude Code / MCP — transcript pull on #1 needed for specifics. → See [[agent-security]].

### Business-adoption flip + Claude Code +50% retention boost (per [[nate-herk]] #5 in [[youtube-digest-apify-2026-05-14]])

The biggest single-event Anthropic update in this vault:

- **2026-05-13: [[anthropic]] passes [[openai]] in business adoption for the first time** — per a Ramp / EconLab article (`econlab.substack.com/p/anthro...`)
- **Within hours: Claude Code rate limits bumped +50%** as a retention offer
- **Simultaneously: [[openai]] ships [[codex]] free for 2 months** — the symmetric retention move from the dethroned leader

Strategic significance:

1. **First adoption-rankings flip in the LLM era** — Anthropic was behind OpenAI on every meaningful adoption metric prior to this. Closest historical analog: AWS overtaking other clouds 2015-2020.
2. **The +50% boost is the *third* Claude Code rate-limit increase in two weeks**:
   - 2026-05-07: SpaceX deal **doubled** 5-hour rate limits ([[nate-herk]] #9 in [[youtube-digest-apify-2026-05-10]])
   - 2026-05-13: Additional **+50% retention boost** (this update)
   - **Total: ~3x baseline** in two weeks
3. **The [[brad-bonanno]] context-bloat optimization argument** is now substantially less urgent at 3x baseline. [[printing-press]] / CLI-replaces-MCP token-cost arguments still apply at scale but with reduced floor-level urgency.
4. **3Ps client implication**: cost projections for Claude Code Plus/Pro engagements just got better. Useful talking point for any current/active client conversations.
5. **[[free-sample-phase]] frame**: per [[nate-herk]] #5, the retention war is *the substrate-economics phase before the inevitable pricing reset*. Both labs are using free-tier expansion to capture training data + lock-in switching cost. → See [[free-sample-phase]].

**Open**: how durable is the adoption flip? Need 2-3 months of additional Ramp data to confirm consolidation vs flip-flop.

### Deployment-company axis (per [[nate-b-jones]] #2 in [[youtube-digest-apify-2026-05-15]])

In Nate's [[agentic-implementation-layer]] framework (32.2K views, 2026-05-14, 25:52), Anthropic is named alongside [[openai]] as **axis-1** of the four-axis squeeze on generic enterprise AI:

> **Anthropic and OpenAI stand up deployment companies** (chapter 4:55) — both labs explicitly building / acquiring deployment-tier organizations rather than relying on partners.

**Strategic significance**:

1. **The +50% Claude Code retention boost (above) is now causally legible** — labs are converting model-tier users into deployment-tier customers. The [[free-sample-phase]] retention war is the *downstream* visible effect of the *upstream* deployment-company strategy.
2. **Partner-channel margin compression** — Anthropic going direct on deployment compresses the resell margin for partners (consultancies, integrators, white-label deployers). This is the structural reason axis-2 ("consultancies moving up the stack" — confirmed by [[ramin-imani]] from inside MBB) is happening *now*.
3. **3Ps positioning implication** — implementation-layer specialists need to either (a) plug into the lab-direct deployment channel or (b) stay above it on the 5 durable primitives ([[skill-systems]] / [[retrieval-contract]] / authority / evals / audit trails). Generic Claude Code consultancy gets compressed.
4. **Open**: which specific deployment company is Anthropic standing up? Branded "Claude Solutions" / "Anthropic Enterprise" / unnamed acquisition? Transcript pull on the video would help. Could also be the [[anthropic]]-rumored Atlassian acquisition viewed through a new lens — Atlassian *is* a deployment substrate for the Jira/Confluence install base.

→ See [[agentic-implementation-layer]] for the full four-axis framework.

### Canonical product-surface inventory (per [[brad-bonanno]] #2 in [[youtube-digest-apify-2026-05-10]])

[[brad-bonanno]]'s 13-product tour is the most comprehensive Anthropic-surface walk in this vault:

1. Claude Chat + artifacts
2. Connectors + MCP
3. Projects
4. Claude Desktop + Cowork + Live Artifacts
5. Skills
6. Dispatch (mobile-to-desktop handoff)
7. Word add-in
8. PowerPoint add-in
9. Excel add-in
10. Chrome (browser automation)
11. Design
12. Code
13. Routines

Brad's thesis: paying users use ~2% of what Claude exposes. Useful baseline for any 3Ps client onboarding — most clients will be touching 2-3 of these and unaware of the other 10.

## FB ads pattern — catalog-ads-only confirmed across 2 launch windows

### 2026-05-06 batch (5 ads — initial wave)

From [[ads-digest-2026-05-06]] — 5 active Anthropic ads, all carousel format with `{{product.name}}` headlines and `{{product.brand}}` body text. **Zero static narrative copy.** Started Mar 16 - Apr 8, 2026.

Same pattern as [[openai]] in the same batch (21 ads, all dynamic-creative-only). Both AI labs in 2026-05-06 ship **only catalog/product-feed-driven dynamic creative** — opposite of DTC competitors like [[hims]] who pair catalog ads with static narrative wedges. Hypothesis: AI labs treat narrative work as PR/launches, and reserve paid social for catalog re-targeting against existing intent.

### 2026-05-14 batch (1 new ad — second launch window)

From [[ads-digest-2026-05-14]] — 1 new ad after **5 batches of silence** (no new Anthropic ads since 2026-05-06). Carousel format, `{{product.name}}` headline, `{{product.brand}}` body, started **2026-05-11** (3 days before fetch — fresh launch, not backlog catch-up). ID `1521217572752360`.

**Cumulative: 6 Anthropic ads across 2 distinct launch windows (Mar 16 – Apr 8 + 2026-05-11), 0 with teardown-able copy.** The catalog-ads-only AI-lab pattern is now confirmed across **two windows** for Anthropic — matching OpenAI's 2-cluster pattern. A fresh launch in a new window with the same template rules out "the original 5 were a one-time test."

> ⚠️ Both AI labs (Anthropic + OpenAI) ship only catalog-driven dynamic creative on FB across multiple launch windows. The pattern is now **multi-window confirmed for both vendors** — not just OpenAI's four-batch single-vendor evidence. Both pair catalog ads with PR/launches for narrative work and reserve paid social for catalog re-targeting against existing intent.

Open: which surface is the 2026-05-11 ad pointing to? Same destination as the original 5 (claude.ai / Code / API / Enterprise), or has the catalog been repointed at a new product surface (Skills marketplace? Mythos? Claude Design? post-business-adoption-flip enterprise push)?

## Official channel activity

- 2025-11-26: *Claude Agent Skills Explained* (201K views) — canonical 3-minute explainer for Skills vs CLAUDE.md vs MCP vs sub-agents
- (Anthropic's official YouTube cadence appears low; high impact when they post)

## Related
- [[claude-code]], [[claude-skills]], [[mcp]], [[claude-design]] — products
- [[andrej-karpathy]] — not at Anthropic but his frameworks (LLM Wiki, agentic engineering) shape the ecosystem Anthropic ships into
- [[agent-substrate]] — the strategic frame that explains the Atlassian rumor
- [[agentic-commerce]] — Anthropic likely a player here too
- [[free-sample-phase]] — substrate-economics framing for the 2026-05-13 retention war (downstream visible effect)
- [[agentic-implementation-layer]] — axis-1 deployment-company strategy (upstream cause of the retention war)
- [[openai]] — direct competitor; lost business-adoption lead on 2026-05-13; same axis-1 deployment-company move

## Appears in
- [[youtube-digest-apify-2026-05-03]] — official Skills explainer + 4 derivative analyst videos
- [[ads-digest-2026-05-06]] — 5 catalog-driven carousel ads (no static narrative)
- [[youtube-digest-apify-2026-05-10]] — SpaceX deal coverage, Mythos surface entry, 13-product tour
- [[youtube-digest-apify-2026-05-11]] — Skill Creator first-hand walkthrough ([[chase-ai]]); agent-security responder ([[nate-b-jones]])
- [[youtube-digest-apify-2026-05-14]] — business-adoption flip vs OpenAI; +50% Claude Code rate-limit retention boost ([[nate-herk]] #5); [[brad-bonanno]] execution-layer Phase 3 (#1)
- [[youtube-digest-apify-2026-05-15]] — axis-1 deployment-company in [[agentic-implementation-layer]] framework ([[nate-b-jones]] #2)
- [[ads-digest-2026-05-14]] — first new Anthropic ad since 2026-05-06 (placeholder carousel, started 2026-05-11) — catalog-ads-only confirmed across 2 distinct launch windows
- [[ads-digest-2026-05-15]] — 0 new Anthropic ads — returns to silence after the single 2026-05-11 carousel (universal-silence batch across all 8 tracked anchors); cumulative remains 6 ads across 2 launch windows; open whether batch 7+ continues the slow-cluster (additional ads from the 2026-05-11+ window expand catalog feed) or confirms the 2026-05-11 ad as a standalone launch
- [[claude-code]], [[claude-skills]], [[code-comprehensibility]], [[skill-creator]], [[agent-security]], [[free-sample-phase]], [[agentic-implementation-layer]] — concept pages

## Open questions
- Is the Atlassian rumor priced into Anthropic strategy, or speculative? (Watch for confirmation/denial)
- What does the next official Anthropic YouTube post cover? (Cadence is low but each post is high-signal)
- Are Skills going to ship in non-Code surfaces (Claude.ai, mobile)? (Currently Code-only)
- Is there an official Skills marketplace coming, or will GitHub-distributed remain canonical?
- **Mythos status** — public-facing product? internal tool? pricing? rollout scope?
- **SpaceX compute deal scope** — capacity terms, exclusivity, duration? Does this signal Anthropic preparing for major capacity demands (Claude Code 3? Enterprise Mythos rollout?)
- **13-product surface coherence** — which of Brad's 13 products are Anthropic actively investing in vs maintaining?
- **Adoption flip durability** — does the 2026-05-13 Ramp data point hold across 2-3 months? Single-data-point reversal vs structural shift unknown
- **What's the next retention move after +50% limits?** — likely a Claude Code Pro/Max price reduction, an expanded free tier, or new productivity primitive (Auto Skills?)
- **Codex 2-months-free competitive impact** — does Anthropic respond with a similar promo, or rely on the rate-limit lead as the standing offer?
