---
title: Anthropic
category: entity
summary: AI lab behind Claude / Claude Code / Claude Skills / MCP / Mythos / Skill Creator; **2026-05-19 hires [[andrej-karpathy]]** — the LLM Wiki author crosses from [[openai]] (his co-founded lab) to Anthropic per [[nate-herk]]'s 105K-view coverage; **2026-05-21 ships [[claude-for-small-business]]** — first Anthropic vertical plugin (~30 pre-built skills + connectors for QuickBooks/Xero/Stripe/HubSpot/Gmail + `/smb-onboard` meta-skill); 2026 strategy now: layering Claude into other vendors' apps + rumored Atlassian acquisition + SpaceX compute partnership + business-adoption flip vs OpenAI (2026-05-13) + +50% retention rate-limit boost + Karpathy hire + first vertical plugin launch; 2026-05-11 named as a six-vendor agent-security responder; **in 2026-05-15 named alongside [[openai]] as axis-1 player in the four-axis squeeze ([[agentic-implementation-layer]])** — both labs standing up deployment companies; FB ads pattern: 6 cumulative ads across 2 distinct launch windows (5 in Mar 16 – Apr 8 + 1 standalone on 2026-05-11); 3 consecutive silence batches post-2026-05-11 LOCK the "standalone launch" diagnosis; paid-social cadence ~15% of OpenAI's despite the adoption flip
tags: [organization, ai-lab, anthropic, claude, claude-code, enterprise, ads, mythos, spacex, code-comprehensibility, skill-creator, agent-security, business-adoption, ramp-data, rate-limits, free-sample-phase, agentic-implementation-layer, deployment-company, axis-1, four-axis-squeeze, standalone-launch-locked, karpathy-hire, claude-for-small-business, vertical-plugin, smb-onboard, prompt-caching, opus-4.7]
sources: 11
updated: 2026-05-22
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

### 2026-05-19 — [[andrej-karpathy]] joins Anthropic (per [[nate-herk]] #3 in [[youtube-digest-apify-2026-05-22]])

**The major personnel event in this vault.** Karpathy — co-founder of [[openai]], author of the [[karpathy-llm-wiki]] gist, originator of "vibe coding" / "Software 3.0" / "agentic engineering" — joins Anthropic. Nate Herk's coverage is 105K views (highest-views news video in this vault) and frames the hire as **the convergence of two parallel architectures**: Karpathy's context-engineering + LLM Wiki + `/goal`-style autonomous loops were already where Claude Code was heading.

**Nate Herk's three predictions** (chapter 12:01 of Nate Herk #3):

1. **"App store for context"** — Anthropic ships a marketplace for context bundles (skills + wiki + farmers + memory). Aligns with [[plugin-marketplace]] ([[alex-mcfarland]]) and [[brad-bonanno]]'s skills-marketplace waitlist — **three-creator convergent prediction** for 2026-Q3.
2. **Education layer** — Eureka Labs pattern productized as Anthropic's pedagogical primitive. Extends [[skill-creator]] toward formal teaching artifacts.
3. **Claude Code becomes the canonical "context substrate"** — wiki + farmers + skills + agents + goal-loops unified, with Karpathy as named architect.

**Strategic significance for Anthropic**:

- **First major OpenAI → Anthropic senior crossing** tracked in this vault — first lab-to-lab co-founder-tier move
- Converts [[karpathy-llm-wiki]] and `karpathy/autoresearch` from external creator artifacts into **about-to-be-first-party Anthropic architecture**
- **"The wrapper is the product"** thesis (Nate Herk chapter 3:57) inverts the thin-wrapper critique — Claude Code + skills + wiki + memory is *the product*, the model is *the substrate*
- Validates the [[free-sample-phase]] retention war (axis-1 deployment-company strategy) — Karpathy's hire is the **product-leadership move** that complements the **business-adoption flip**
- Open: what's Karpathy's actual title/scope at Anthropic? Affects which Claude Code primitives he influences directly

### 2026-05-21 — Claude for Small Business launch (per [[brad-bonanno]] #7 in [[youtube-digest-apify-2026-05-22]])

**Anthropic ships its first vertical plugin** — [[claude-for-small-business]] — a desktop-app-installed plugin bundling:

- **Connectors** (MCP servers) pre-wired for: QuickBooks, Xero, Stripe, PayPal, Square, HubSpot, Gmail
- **~30 pre-built skills** mapped to SMB jobs-to-be-done (Monday brief / call list / plan payroll / close month / handle complaint / run campaign / Friday brief / quarterly review / CRM maintenance / invoice chase + ~20 more)
- **`/smb-onboard` meta-skill** — customizes every skill in the pack to the user's business / industry / headcount / tools (skill-creator-shape meta-skill)
- **Connector flexibility** — swap Xero for QuickBooks etc. post-install

**Strategic significance**:

1. **First Anthropic-shipped vertical plugin** — Anthropic's product surface (Brad's 13-product tour) was previously horizontal. CFSB is the **first vertical-targeted, opinionated, pre-composed** product
2. **30 pre-built skills = canonical "skills as product" instantiation** — [[claude-skills]] / [[plugin-marketplace]] / [[execution-layer]] roadmap is shipping as **Anthropic-owned vertical plugins**, not just community marketplaces
3. **Competes with [[brad-bonanno]]'s own skills-marketplace roadmap** — Anthropic preempts Brad's similar vertical launch
4. **Pairs with [[chief-ai-officer]]** ([[nate-herk]] #4 same batch) — CFSB for SMBs (sub-200 employees), CAIO for mid-market. Same demand curve, two product wedges at different company sizes
5. **`/smb-onboard` confirms meta-skills as Anthropic-shipped product category** — not just a community pattern ([[skill-creator]] is meta-skill #1 from Anthropic; `/smb-onboard` is meta-skill #2)
6. **Open**: pricing model, sibling vertical-plugin roadmap (Claude for Retail / Healthcare / Legal), 30-skill open-source status

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

**Cumulative: 6 Anthropic ads across 2 distinct launch windows (Mar 16 – Apr 8 + 2026-05-11), 0 with teardown-able copy.** The catalog-ads-only AI-lab pattern is now confirmed across **two windows** for Anthropic — matching OpenAI's 2-cluster pattern.

### 2026-05-15 + 2026-05-16 + 2026-05-20 batches (3 consecutive silence batches — "standalone launch" diagnosis LOCKED)

From [[ads-digest-2026-05-15]], [[ads-digest-2026-05-16]], [[ads-digest-2026-05-20]] — **3 consecutive silent batches with 0 new Anthropic ads** post-2026-05-11.

**Per the batch-7 ≥3-silent-batch methodology, the 2026-05-11 ad is now confirmed as a standalone launch, not the opening of a slow cluster.** Batch 8's 4-day fetch gap would have captured any new Anthropic ads from 2026-05-17 → 2026-05-20 — none surfaced. Three consecutive silent batches with a 4-day gap on the third is decisive.

**Anthropic pattern**: 5 ads (Mar 16 – Apr 8 wave) + 1 ad (standalone 2026-05-11) = sparse, well-spaced standalone launches across 8 batches.

| Batch | Date | New Anthropic ads | Cumulative |
|---|---|---|---|
| 1 | 2026-05-06 | 5 | 5 |
| 2-4 | (silence trough) | 0 | 5 |
| 5 | 2026-05-14 | 1 | 6 |
| 6 | 2026-05-15 | 0 | 6 |
| 7 | 2026-05-16 | 0 | 6 |
| **8** | **2026-05-20** | **0** | **6 (LOCKED — standalone diagnosis confirmed)** |

**Cadence comparison vs [[openai]] across same 8-batch window**: Anthropic 6 ads / OpenAI 40 ads — Anthropic's paid-social cadence is **~15% of OpenAI's**. Despite Anthropic *passing* OpenAI in business adoption on 2026-05-13, OpenAI's *paid-social cadence* remains an order of magnitude more aggressive. Reads as: Anthropic relies on rate-limit boosts + PR + business-adoption momentum for growth, while OpenAI runs continuous paid-social catalog cadence (probably re-targeting against ChatGPT signup intent + API console traffic).

Open: which surface is the 2026-05-11 ad pointing to? Same destination as the original 5 (claude.ai / Code / API / Enterprise), or has the catalog been repointed at a new product surface (Skills marketplace? Mythos? Claude Design? post-business-adoption-flip enterprise push)?

## Official channel activity

- 2025-11-26: *Claude Agent Skills Explained* (201K views) — canonical 3-minute explainer for Skills vs CLAUDE.md vs MCP vs sub-agents
- (Anthropic's official YouTube cadence appears low; high impact when they post)

## Related
- [[claude-code]], [[claude-skills]], [[mcp]], [[claude-design]] — products
- [[andrej-karpathy]] — **joined Anthropic in 2026-05-19** (per [[nate-herk]] 105K-view coverage); his frameworks (LLM Wiki, agentic engineering, autoresearch, `/goal` loops) now becoming first-party Anthropic primitives
- [[claude-for-small-business]] — first vertical plugin (launched 2026-05-21)
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
- [[ads-digest-2026-05-16]] — **0 new Anthropic ads — 2nd consecutive silence batch post-2026-05-11.** "Standalone launch" hypothesis strengthens over "slow cluster"; one more silent batch (batch 8) would lock the diagnosis. Cumulative remains 6 ads across 2 launch windows (5 in Mar 16 – Apr 8 + 1 on 2026-05-11). Contrast with [[openai]]'s same-batch behavior — 2 new May 8 ads expand cluster 2 from 6 → 8, decisively disproving batch 6's "fully dedup-cached" diagnosis. Anthropic remains markedly sparser than OpenAI in FB-ad cadence (6 vs 33 cumulative ads across the same window)
- [[ads-digest-2026-05-20]] — **0 new Anthropic ads — 3rd consecutive silence batch post-2026-05-11 LOCKS the "standalone launch" diagnosis** per the batch-7 ≥3-silent-batch methodology. Batch 8's 4-day fetch gap would have captured any new ads in 2026-05-17 → 2026-05-20 — none surfaced. Cumulative remains 6 ads across 2 launch windows. Cadence vs [[openai]] in same 8-batch window: Anthropic 6 / OpenAI 40 — Anthropic's paid-social cadence is ~15% of OpenAI's despite the 2026-05-13 business-adoption flip. Anthropic's pattern is sparse standalone launches; OpenAI's is continuous cluster expansion.
- [[youtube-digest-apify-2026-05-22]] — **[[andrej-karpathy]] joins Anthropic** ([[nate-herk]] #3, 105K views) + **[[claude-for-small-business]] launch** ([[brad-bonanno]] #7) — first vertical plugin
- [[claude-code]], [[claude-skills]], [[code-comprehensibility]], [[skill-creator]], [[agent-security]], [[free-sample-phase]], [[agentic-implementation-layer]], [[claude-for-small-business]] — concept pages

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
