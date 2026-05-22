---
title: YouTube Digest (Apify) — AI creators + Claude topics — 2026-05-22
category: source
summary: 12-video farm batch (32 fetched, 20 dedup-skipped) — **the biggest news batch since cold start**: (1) [[andrej-karpathy]] joins [[anthropic]] (105K-view [[nate-herk]] coverage) — the LLM Wiki author crosses to the lab whose product line he's been parallel-tracking; (2) [[anthropic]] ships **Claude for Small Business** — a [[brad-bonanno]] walkthrough of the new plugin with ~30 pre-built skills + connectors for QuickBooks/Xero/Stripe/HubSpot/Gmail (new concept [[claude-for-small-business]]); (3) [[eric-tech]] (new entity) ships a **/wiki skill that automates LLM Wiki ingest from YouTube/Gmail/Slack on a cron** — direct vault-architecture analog; (4) [[ai-labs]] (new entity) reverse-engineers Anthropic team's internal Claude Code skills (verify / skillify / tech-debt / security-scan) at 36K views — first canonical "what Anthropic actually uses internally" coverage; (5) [[nate-b-jones]] ships **four more frameworks** — capital allocation (build/buy/hire/wait/automate), 6-layer agent protocol stack ([[agent-protocol-stack]]: MCP/A2A/AG-UI/A2UI/AP2/x402), prove-it economy / truth layer ([[prove-it-economy]]), AI Question Method ([[ai-question-method]]), 5 infrastructure giants ([[infrastructure-control-layer]]: runtime/identity/data/payments/observability/kill-switch) — extends his framework cadence to **15 named frameworks**; (6) [[nate-herk]] ships the CAIO career framing ([[chief-ai-officer]]), prompt caching deep dive ([[prompt-caching]]), and Claude-Code↔Codex cross-substrate compatibility (3-layer mental model)
source_path: raw/youtube/digest-2026-05-22.md
source_date: 2026-05
authors: [AI LABS, Nate Herk, Nate B Jones, Brad Bonanno, Eric Tech]
ingested: 2026-05-22
tags: [youtube, digest, apify, karpathy-anthropic, claude-for-small-business, wiki-skill, anthropic-internal-skills, capital-allocation, agent-protocol-stack, mcp, a2a, ag-ui, a2ui, ap2, x402, prove-it-economy, truth-layer, ai-question-method, chief-ai-officer, caio, prompt-caching, infrastructure-control-layer, runtime, identity, data, payments, observability, kill-switch, codex-claude-code-compatibility, opus-4.7, gpt-5.5]
sources: 1
updated: 2026-05-22
---

# YouTube Digest (Apify) — 2026-05-22

## Source meta

- **Farmer**: `ai-creators-youtube`
- **Fetcher**: Apify `streamers/youtube-scraper`
- **Total fetched**: 32 videos
- **Dedup-skipped**: 20 (already seen)
- **New videos**: 12 (highest single-batch count since [[youtube-digest-apify-2026-05-10]])
- **Creators**: [[nate-herk]] (4), [[nate-b-jones]] (5), [[brad-bonanno]] (1), [[ai-labs]] (1 — new), [[eric-tech]] (1 — new)

## Videos

| # | Title | Channel | Views | Date | Duration |
|---|---|---|---|---|---|
| 1 | Claude Code's Creator Uses These Claude Skills Every Single Day | AI LABS | 36,260 | 2026-04-03 | 12:17 |
| 2 | How to Use Your Claude Code Projects in Codex in 5 Mins | Nate Herk | 24,577 | 2026-05-18 | 8:39 |
| 3 | What Karpathy Joining Anthropic Actually Means For Claude | Nate Herk | 105,462 | 2026-05-19 | 16:24 |
| 4 | The AI Career Opportunity Nobody is Talking About in 2026 | Nate Herk | 53,598 | 2026-05-17 | 19:13 |
| 5 | When to Automate, Build, Buy, Hire, or Wait on AI | Nate B Jones | 23,253 | 2026-05-17 | 27:46 |
| 6 | Google Spent a Year Stitching MCP, A2A, AG-UI Together. I/O Today. | Nate B Jones | 37,727 | 2026-05-19 | 20:42 |
| 7 | Why You Need Claude for Small Business | Brad Bonanno | 831 | 2026-05-21 | 6:52 |
| 8 | Karpathy's LLM Wiki + This Skill = Game Changer | Eric Tech | 3,391 | 2026-05-20 | 16:19 |
| 9 | Give Me 10 Mins and I'll Save You Millions of Claude Tokens | Nate Herk | 17,126 | 2026-05-21 | 10:43 |
| 10 | The Prove-It Economy is Here \| Most Marketers Aren't Ready | Nate B Jones | 56,099 | 2026-05-18 | 22:23 |
| 11 | Opus 4.7 and OpenAI 5.5 Made Your Prompting Style Obsolete. | Nate B Jones | 52,651 | 2026-05-21 | 25:03 |
| 12 | These 5 Infrastructure Giants Secretly Rule AI | Nate B Jones | 20,179 | 2026-05-20 | 20:19 |

## Per-video highlights

### #1 AI LABS — *Claude Code's Creator Uses These Claude Skills Every Single Day*

**36K views, 2026-04-03, 12:17. → New entity: [[ai-labs]]. Updates [[claude-skills]], [[claude-code]].**

The **first canonical "what Anthropic actually uses internally" coverage** in this vault. AI LABS reverse-engineered internal skills from Anthropic team posts + open-source repos + leaked source code references. Three categories surfaced:

**Anthropic-released open-source plugins** (in `claude-plugins-official`):
- **Frontend Designer Plugin** — helps AI avoid generic aesthetics in UI generation
- **Code Simplifier** — refactoring + dead-code elimination
- **Commit Commands** — automated commit-message generation

**Reverse-engineered internal-team skills** (behind CLI flags, not publicly published):
- **Verify** — automated testing harness ([[skill-creator]]-adjacent meta-skill)
- **Skillify** — converts a working session into a reusable skill ([[skill-creator]]-shape)
- **Tech Debt** — end-of-session cleanup of incomplete work
- **Batch** — parallelizes migrations across isolated git worktrees
- **Security Scan** — input-validation / auth / injection-risk vulnerability checks

**Strategic significance**:

1. **First "Anthropic uses Claude differently than you" coverage** — confirms internal Anthropic devs run a richer skill stack than what's shipped publicly. Same shape as Skill Creator's 2026-05-11 Anthropic-release (a meta-skill they were already using internally).
2. **Verify + Skillify + Tech Debt are all meta-skill-shape** — extending the [[skill-creator]] category. Meta-skills (skills that operate on other skills or sessions) are now a tracked category.
3. **Security Scan** is the agent-side complement to [[agent-security]] — a build-time scanner that catches the same vulnerability classes [[nate-b-jones]]' McKinsey Lilly example exposed.
4. **The Batch skill maps cleanly to [[deployment-framework]] Method 1** — `/loop`-shape parallelization, but with worktree isolation as the canonical container.
5. AI LABS' **`ailabspro.io`** community is the distribution surface; **sponsorships at ailabs.services**.

→ See [[ai-labs]] entity page and [[claude-skills]] update for internal-skill inventory.

### #2 Nate Herk — *How to Use Your Claude Code Projects in Codex in 5 Mins*

**24.6K views, 2026-05-18, 8:39. → Updates [[codex]], [[nate-herk]], [[claude-code]].**

Cross-substrate compatibility tutorial — how to make a Claude Code project readable by [[codex]] (and vice versa) without duplicating files. Names the **3-layer mental model** for cross-vendor work:

| Layer | Claude Code artifact | Codex artifact | Compatible? |
|---|---|---|---|
| **Instructions** | `CLAUDE.md` | `AGENTS.md` | Yes — same content, different filename |
| **Skills** | `skills/` directory | `skills/` directory | Yes — same format |
| **Agents** | `agents/` directory | `agents/` directory | Mostly compatible — minor schema deltas |

**Chapter map**:
- 0:00 Intro
- 0:29 Claude vs Codex File Structure
- 3:05 Skills & Agents Compared
- 4:17 **The 3-Layer Mental Model**
- 5:13 Convert Any Project Fast
- 6:23 Using Both Together
- 8:11 Final Thoughts

**Strategic significance**:

1. **Confirms the [[free-sample-phase]] thesis** in concrete portability terms — "use both at once" is the canonical defensive strategy
2. **The 3-layer model is a portable architectural primitive** — applies symmetrically to [[hermes-agent]] / [[claude-code]] / [[codex]] (all use the same instructions/skills/agents triple)
3. **Cross-substrate symmetry now confirmed at the *project filesystem* level**, not just the *primitive* level — earlier symmetry claims ([[nate-herk]] Codex full course) were per-feature; this video shows entire projects copy-paste between substrates
4. **First conversion prompt published** for Claude Code → Codex auto-migration — extends the substrate-portability playbook

### #3 Nate Herk — *What Karpathy Joining Anthropic Actually Means For Claude*

**105K views, 2026-05-19, 16:24. → Major updates [[andrej-karpathy]], [[anthropic]], [[karpathy-llm-wiki]], [[claude-code]].**

**THE major news of this batch.** [[andrej-karpathy]] — co-founder of [[openai]], author of the [[karpathy-llm-wiki]] gist — **joins [[anthropic]]**. The 105K-view headline coverage from a 708K-sub channel makes this the highest-views video in the batch and the highest-views *news* video tracked in this vault.

**Chapter map**:
- 0:00 Karpathy Joins Anthropic
- 1:04 Who Is Karpathy
- 2:01 Anthropic's Momentum
- 3:57 The Wrapper Is the Product
- 6:25 LLM Wiki and Your Data Moat
- 8:52 AutoResearch and /Goal Loops
- 10:47 The Education Clue
- 12:01 **3 Predictions for Claude Code**
- 16:12 Final Thoughts

**The why-it-makes-sense thesis** (chapters 3:57-8:52):

Karpathy's recent work — context engineering, the LLM Wiki, `/goal`-style autonomous loops — **lines up almost perfectly with Claude Code's existing product surface**. He's been parallel-shipping the architecture Anthropic was already on. Joining unifies the two trajectories.

**The three predictions** (chapter 12:01):

1. **An "app store for context"** — Anthropic ships a marketplace for context bundles (skills + wiki + farmers + memory). Pairs with [[plugin-marketplace]] ([[alex-mcfarland]] 2026-03-16) and [[brad-bonanno]]'s skills-marketplace waitlist. **The Claude Code context-bundle marketplace is now a multi-creator prediction.**
2. **An education layer for packaging your own workflows** — Eureka Labs ([[andrej-karpathy]]'s company) provides the pedagogical pattern; Anthropic productizes it. Extension of [[skill-creator]] toward formal teaching artifacts.
3. **Claude Code becomes the canonical "context substrate"** — wiki + farmers + skills + agents + goal-loops as the unified primitive, with Karpathy as the named architect.

**"LLM Wiki and Your Data Moat" (chapter 6:25)** — Nate Herk's framing claim: in a world of commoditized models, **the wiki is the moat**. Your structured-context vault is the only thing competitors can't replicate by switching providers. Pairs with [[brad-bonanno]]'s [[execution-layer]] and [[free-sample-phase]] economics.

**Strategic significance**:

1. **Highest-views news coverage in vault** — confirms the hire is a category-defining event for the Claude ecosystem
2. **[[karpathy-llm-wiki]] is now an Anthropic-internal pattern** — the vault is no longer "implementing a Karpathy gist," it's implementing **what's about to become first-party Anthropic architecture**
3. **The "wrapper is the product" framing** (chapter 3:57) inverts the usual "thin wrapper" criticism — the wrapper (Claude Code + skills + wiki) is *exactly the product*; the model is the substrate
4. **Predictions 1 + 2 align with [[brad-bonanno]] Phase-3 [[execution-layer]] + [[alex-mcfarland]] [[plugin-marketplace]]** — three creators converging on the same near-term Anthropic roadmap. The marketplace + education trajectory is now **the consensus 2026-Q3 product forecast** across vault-tracked creators.
5. **`/goal` and AutoResearch as the same primitive** (chapter 8:52) — Karpathy's `autoresearch` skill is reframed as a `/goal`-loop ancestor; Anthropic ships the production form

→ Major updates to [[andrej-karpathy]] (now an Anthropic employee), [[anthropic]] (Karpathy joins), [[karpathy-llm-wiki]] (no longer external to Anthropic).

### #4 Nate Herk — *The AI Career Opportunity Nobody is Talking About in 2026*

**53.6K views, 2026-05-17, 19:13. → New concept: [[chief-ai-officer]]. Updates [[nate-herk]], [[ai-consulting]].**

The **counter-narrative to "start an AI agency"** — names the **Chief AI Officer (CAIO)** wave as the bigger, quieter opportunity for non-developer operators.

**Chapter map**:
- 0:00 Intro
- 1:15 **The CAIO Stat**
- 3:59 The Adoption Gap
- 7:26 **Two Paths**
- 10:05 What Matters Most
- 12:12 The Data Behind The Reframe
- 15:40 The Regulated Industry Edge
- 18:14 Final Thoughts

**The framing claim**: *"Everyone is told to start an AI automation agency. But the bigger, quieter shift is the Chief AI Officer wave — and it fits way more people."*

**The IBM survey unlock** — 2,000 CEOs surveyed (newsroom.ibm.com link in description), revealing:
- **CAIO role demand surging** (specific number gated to transcript pull)
- **61-point gap** between *who can use AI* and *who actually does* — the operational implementation gap
- **Regulated industries** (healthcare / financial services / legal) have the biggest CAIO opportunity because compliance + AI deployment maps onto existing chief-officer roles cleanly

**The two paths into the seat** (chapter 7:26):

| Path | For who | Time-to-seat |
|---|---|---|
| **Path 1 — Inside-the-firm operator** | Current senior managers, BUs heads, COOs | Faster — leverage existing authority + budget |
| **Path 2 — Fractional / external CAIO** | Consultants, ex-operators, fractional-CXO veterans | Slower — needs portfolio + signaling |

**"Playing to your strengths matters more than chasing the loudest trend"** (chapter 10:05) — the counter-thesis to [[ai-consulting]]'s solo-agency wedge. For operators who don't want to start a business, the CAIO seat is a higher-leverage on-ramp.

**Strategic significance**:

1. **First chief-AI-officer career framing** in this vault — extends the [[ai-consulting]] coverage to a sister category. Where [[nicole-mccain]] / [[ramin-imani]] / [[mark-kashef]] cover solo-consulting wedges, CAIO is the **employee-seat wedge** for the same skill set.
2. **Confirms axis-2 of [[agentic-implementation-layer]] from inside the firm** — Nate's CAIO framing is the practitioner-side complement to Nate B Jones' "consultancies moving up the stack" thesis. Both videos see the same enterprise-AI demand from different vantage points.
3. **The 61-point adoption gap is a new canonical stat** — pairs with the "2% of Claude features used" claim from [[brad-bonanno]]'s 13-product tour. Both are evidence of the **operational implementation gap** that 3Ps targets.
4. **Regulated-industries edge** (chapter 15:40) is the 3Ps wedge for compliance-bound verticals (healthcare, fintech, legal) — same audience as the user's competitor-ads farm tracking telehealth GLP-1 brands.

→ New concept: [[chief-ai-officer]].

### #5 Nate B Jones — *When to Automate, Build, Buy, Hire, or Wait on AI*

**23.3K views, 2026-05-17, 27:46. → New concept: [[capital-allocation-framework]]. Updates [[nate-b-jones]] (12th framework), [[agentic-implementation-layer]].**

His **12th named framework** — the **capital allocation matrix** for AI workflows. Where [[agentic-implementation-layer]] tells you *where the value lives* and [[agent-metering]] tells you *how the meter ticks*, this framework tells you *which lever to pull on each workflow*.

**Chapter map**:
- 00:00 Why AI investment is a capital allocation problem
- 03:33 You need the right people in the room
- 04:49 The Gartner 40 percent failure prediction
- 06:49 AI investment is really a workflow question
- 07:39 The accounts receivable workflow example
- 09:52 Defining the workflow operating loop
- 11:11 **The five levers**: automate, build, buy, hire, wait
- 12:00 Automation and the IBM AskHR case
- 17:13 Build: when company context demands it
- 21:36 Buy: primitives versus whole workflow vendors
- 24:56 Hiring without chasing the purple unicorn
- 29:36 When waiting is the right deliberate choice
- 31:52 Do not automate what you cannot describe
- 34:01 The investment matrix and four quadrants
- 38:12 (truncated)

**The five levers** (chapter 11:11):

| Lever | Best for | Failure mode |
|---|---|---|
| **Automate** | Well-described, repeatable workflows with existing tools | Automating what you can't describe (chapter 31:52) |
| **Build** | When **company context** is the differentiator (proprietary domain logic) | Building what's already a commodity primitive |
| **Buy** | Workflow-vendor purchases (full workflow, not primitives) | Buying primitives that should have been built; buying workflows that should have been hired |
| **Hire** | When workflow is critical but **purple unicorns don't exist** | Trying to find one person who does everything |
| **Wait** | Deliberate non-action when the workflow can't be reliably defined yet | Confusing deliberate-wait with default-paralysis |

**"Do not automate what you cannot describe"** (chapter 31:52) — the canonical failure mode. Pairs with [[anticipation-gap]]'s "the labs aren't going to fix this for you" insight: if you can't describe the workflow's operating loop (chapter 9:52), automation is premature.

**The Gartner 40% failure prediction** (chapter 4:49) — most agentic AI projects fail, and the failure mode is **misallocated lever** (build when buy was right, hire when automate was right, automate when wait was right).

**The accounts-receivable example** (chapter 7:39) — recurring workflow that maps cleanly onto each of the five levers depending on company size + AR volume + customer mix. The same workflow takes different lever choices at different companies — **the lever follows the company, not the workflow type**.

**"You need the right people in the room"** (chapter 3:33) — the lever decision can't be made by IT or the CFO alone; needs **workflow owner + automation engineer + procurement** at minimum. Same shape as [[agent-security]]'s "developers at the procurement table" argument from [[nate-b-jones]]' 2026-05-10 framework.

**Strategic significance**:

1. **12th [[nate-b-jones]] framework** — the **decision-side companion** to [[agentic-implementation-layer]] (where-value-lives) and [[agent-metering]] (how-pricing-works). Together: three frameworks describing the same enterprise-AI investment cycle from three angles
2. **The five-lever taxonomy is the cleanest "how do I actually decide" framework** in this vault — directly portable to 3Ps client engagement structure
3. **"Workflow not strategy" framing** is the **anti-AI-strategy thesis** — replaces the conventional "we need an AI strategy" consulting deliverable with workflow-by-workflow capital allocation
4. **The IBM AskHR case study** (chapter 12:00) — first IBM-internal-AI case study in the vault; pairs with the IBM CEO survey [[nate-herk]] used in #4
5. **Pairs perfectly with [[chief-ai-officer]]** — Nate Herk #4 says "you might want the CAIO seat"; Nate B Jones #5 says "here's what the CAIO actually does day-one." Two videos in the same batch defining the same role from career-side + role-design-side

→ New concept: [[capital-allocation-framework]].

### #6 Nate B Jones — *Google Spent a Year Stitching MCP, A2A, AG-UI Together. I/O Today.*

**37.7K views, 2026-05-19, 20:42. → New concept: [[agent-protocol-stack]]. Updates [[mcp]], [[agentic-commerce]], [[nate-b-jones]] (13th framework).**

His **13th framework** — the **6-layer agent-protocol-stack taxonomy**. Extends [[mcp]]'s prior solo coverage into a complete **agent-stack-protocol map** with the three protocols that *actually matter* highlighted.

**Chapter map**:
- 00:00 Six protocols, three that matter
- 01:18 The three questions agents must answer
- 02:35 **MCP: the tool and data layer**
- 04:50 Why MCP is a security boundary
- 06:20 **A2A: the delegation layer**
- 08:15 The agent card as operating contract
- 09:40 **AG-UI: the human control layer**
- 11:55 Why agents need supervision surfaces
- 13:30 A2UI, AP2, and x402: the contested layers
- 15:10 AP2 and the mandate mechanic
- 16:35 Stripe and customer-obsessed payment design
- 18:00 **Six questions to ask before you build**
- 19:45 What to watch at Google I/O

**The six-protocol taxonomy** (the master framework):

| Protocol | Layer | Status | Sponsor |
|---|---|---|---|
| **MCP** | Tool + data access | **Settled** — production-ready | [[anthropic]] |
| **A2A** | Agent-to-agent delegation | **Settled** — production-ready | Google |
| **AG-UI** | Agent-to-human control surface | **Settled** — production-ready | Google |
| **A2UI** | Agent-to-UI (contested) | Contested | Multiple |
| **AP2** | Payment authorization | Contested — fights with [[agentic-commerce]] AP2 | Google (different from commerce AP2?) |
| **x402** | Machine-to-machine payment rails | Contested | Stripe |

**The three questions agents must answer** (chapter 1:18) — the diagnostic substructure:

1. **What can I access?** → MCP answers this
2. **Who can I delegate to?** → A2A answers this
3. **How do humans supervise me?** → AG-UI answers this

These three settled protocols form the **operational backbone**. The other three (A2UI, AP2, x402) are **contested commercial layers** — the camps fighting over who owns the payment/UI surface.

**MCP as security boundary** (chapter 4:50) — extends [[agent-security]]'s judge-architecture pattern: MCP servers *are* the natural action-boundary instrumentation point. Same reframe as Lindy's outbound-mail judge from [[nate-b-jones]] 2026-05-12.

**The agent card as operating contract** (chapter 8:15) — A2A's metadata primitive. An agent publishes its capabilities/SLA/authority surface; other agents can discover + verify + delegate. Same shape as MCP's manifest, but for delegation rather than tool-access.

**"Why agents need supervision surfaces"** (chapter 11:55) — the AG-UI thesis. Agents that don't expose supervision surfaces are unsupervisable; **supervisability is a product feature, not a config option**. Extends [[anticipation-gap]]'s permission-ladder framework with a protocol-level layer.

**The six questions to ask before you build** (chapter 18:00) — the **builder-side diagnostic**:

1. What tool/data does my agent need? → MCP
2. Does it need to delegate? → A2A
3. How will humans intervene? → AG-UI
4. Does it need to drive a UI? → A2UI (contested)
5. Does it pay? → AP2 (contested)
6. Does it pay other agents? → x402 (contested)

**Strategic significance**:

1. **13th framework from [[nate-b-jones]]** — second framework specifically on agent infrastructure (after [[agentic-commerce]] 6-layer taxonomy from 2026-05-12). The two taxonomies overlap on AP2 and x402, but cover different surfaces (commerce = payment specifically; protocol stack = full agent operation).
2. **First A2A + AG-UI coverage** in this vault — these are now tracked alongside [[mcp]] as canonical protocol-layer primitives
3. **The "three that matter" filter is opinion-shaped** — Nate is explicitly betting MCP+A2A+AG-UI win and the contested-layer fights resolve to one winner each. This is a **testable prediction** for future digests
4. **AG-UI fills the gap [[anticipation-gap]] identified** — Nate B Jones' 2026-05-05 framing identified that consumer AI lacked a supervision surface; AG-UI is the protocol candidate for closing that gap
5. **Pairs with [[agentic-commerce]] from 2026-05-12** — agent-protocol-stack and agentic-commerce-taxonomy form a **complete agent-infrastructure-protocol map** across operations + commerce

→ New concept: [[agent-protocol-stack]]. Major update: [[mcp]] (placed in 6-protocol context).

### #7 Brad Bonanno — *Why You Need Claude for Small Business*

**831 views (just published), 2026-05-21, 6:52. → New concept: [[claude-for-small-business]]. Updates [[brad-bonanno]], [[anthropic]], [[claude-skills]].**

**Anthropic just shipped Claude for Small Business** — a plugin installed directly into the Claude desktop app, pre-wired with connectors (QuickBooks / Xero / Stripe / PayPal / Square / HubSpot / Gmail) and ~30 pre-built skills mapped to SMB jobs-to-be-done.

**The pre-built skills** (the SMB skill catalog):

| Skill | What it does |
|---|---|
| **Monday brief** | Synthesizes financials + settlements + deals + calendar into a one-page plan |
| **Call list** | Ranks top 5 leads worth calling today |
| **Plan payroll** | Per-pay-period scheduling/calculation |
| **Close month** | Books closing automation |
| **Handle complaint** | Customer-complaint workflow |
| **Run campaign** | Marketing-campaign launch |
| **Friday brief** | End-of-week roll-up |
| **Quarterly review** | QBR generation |
| **CRM maintenance** | Auto-logs meetings to HubSpot |
| **Invoice chase** | Tone-matched follow-ups, skips paid customers |
| (~20 more) | (specifics gated to transcript / Brad's small business skills guide) |

**The `/smb-onboard` command** — customizes every skill in the pack to the user's business, industry, headcount, and tools. **Same shape as a [[skill-creator]]-style meta-skill**: the onboarding command **rewrites the skills to fit the company**.

**Connector flexibility** — if the stack isn't covered out-of-box (e.g., Xero vs QuickBooks), connectors can be swapped post-install.

**Brad's distribution funnel**:
- **Small Business Skills Guide** lead magnet (`brad-b.kit.com/bb4f80fd45`)
- **AI Strategy Call** (`cal.com/bradley-bonanno/ai-st...`)

**Strategic significance**:

1. **First Anthropic-shipped vertical plugin** tracked in this vault — Claude for Small Business is a packaged, opinionated, vertical-targeted artifact (vs the prior horizontal Claude Code surface)
2. **30 pre-built skills = the canonical "skills as product" instantiation** — confirms the [[claude-skills]] / [[plugin-marketplace]] / [[execution-layer]] roadmap is shipping as **Anthropic-owned vertical plugins**, not just user-built marketplaces
3. **Direct competitor to [[brad-bonanno]]'s skills-marketplace roadmap** — Anthropic is shipping the SMB-focused private marketplace ahead of Brad's similar launch. Brad's video reads as **competitive-coexistence positioning** (he covers it favorably + retains his role as the "execution layer" educator)
4. **Pairs with [[chief-ai-officer]]** — CAIO for mid-market enterprise, Claude for Small Business for sub-CAIO businesses. Same demand curve, two product wedges
5. **`/smb-onboard` is a [[skill-creator]]-shape meta-skill** — confirms meta-skills are now an **Anthropic-shipped product category** (not just a community pattern)
6. **Phase 4 of [[brad-bonanno]]'s trajectory?** — context farming (Phase 1) → 13-product tour (Phase 2) → execution layer (Phase 3) → **Anthropic-shipped vertical plugin coverage (Phase 4)**. Brad continues to be the canonical creator-side commentator on Anthropic product launches.

→ New concept: [[claude-for-small-business]]. Major updates: [[anthropic]] (vertical plugin launch), [[brad-bonanno]] (Phase 4 of trajectory), [[claude-skills]] (Anthropic-shipped 30-skill SMB pack).

### #8 Eric Tech — *Karpathy's LLM Wiki + This Skill = Game Changer*

**3.4K views, 2026-05-20, 16:19. → New entity: [[eric-tech]]. Updates [[karpathy-llm-wiki]], [[context-farming]].**

**Direct vault-architecture analog.** Eric Tech (small-tier creator) ships a `/wiki` skill that **automates the entire LLM Wiki ingest workflow on a cron**, pulling from YouTube + Gmail + Slack + any data source into an Obsidian vault. **This is the same pattern this vault runs.**

**Chapter map**:
- 0:00 Intro
- 1:50 The Workflow
- 4:26 **Wiki Skill**
- 5:24 Interview Phase
- 6:35 Folder Structure
- 8:34 **Farmer Agents**
- 10:53 Run Wiki Farm
- 13:18 Final Demo
- 14:23 **Schedule Cron**
- 15:24 Wrap Up

**Key claims**:
- **"Karpathy's LLM Wiki is the smartest way to use AI for research — but it has one problem: you still have to manually feed it every single source"** → exact problem this vault's `farmer` skill solves
- **`/wiki` skill** wraps the whole setup (init + ingest + lint) into one command
- **Farmer subagents** ingest multiple sources in parallel — **this vault uses identical naming** (`farmers/<name>.md` configs)
- **Scheduling as a cron job** — same pattern as this vault's daily ai-creators-youtube farm
- **Distribution**: `skool.com/erictech` Skool community (paid — skill + 100+ templates + weekly Claude Code masterclasses)

**Strategic significance**:

1. **First creator-shipped parallel of this vault's architecture** — Eric's `/wiki` skill + farmer subagents + cron-scheduling triple **is the same primitive triple** this vault implements. Convergent evolution from two independent creators (Eric in mid-May 2026 + this vault since 2026-05-03).
2. **bookzero.ai callout** (`bookzero.ai — AI-powered bookkeeping built entirely with Claude Code`) is the **first Claude-Code-built SaaS product** tracked in this vault. Pairs with [[claude-for-small-business]]'s bookkeeping focus — bookzero is the standalone SaaS Eric appears to have built; Claude for Small Business is Anthropic's plugin alternative.
3. **Differentiation pressure on the vault**: this video's existence means **"I built an LLM Wiki + farmers + cron" is no longer differentiating** — the [[karpathy-llm-wiki]] adoption-tier signal has now reached the **operational-pattern-ships-as-skill** tier. The vault's differentiation now lives in:
   - What's *in* the wiki (3Ps + GTM + competitive intel content)
   - Quality of the farmers
   - Cross-references / synthesis depth
   - Multi-source farming (YouTube + ads + future channels)
4. **Adoption-tier signal**: Eric is small-channel (3.4K views) but ships paid Skool community — **the pattern is now a mid-tier commercial product**, not just a hobbyist artifact
5. **Direct cross-reference target** — Eric's `/wiki` skill is the **closest creator-shipped analog** to this vault's `/wiki-ingest`, `/wiki-query`, `/wiki-lint` triple

→ New entity: [[eric-tech]]. Major update: [[karpathy-llm-wiki]] (skill-shipped automation), [[context-farming]] (parallel implementation).

### #9 Nate Herk — *Give Me 10 Mins and I'll Save You Millions of Claude Tokens*

**17.1K views, 2026-05-21, 10:43. → New concept: [[prompt-caching]]. Updates [[nate-herk]], [[claude-code]], [[free-sample-phase]].**

Deep-dive on **prompt caching** — the substrate-economics primitive that "saves 300M+ tokens a week without you doing anything." References **Thariq's article** (`x.com/trq212/status/202457413...`) as the canonical authoritative source.

**Chapter map**:
- 0:00 91 Million Tokens Saved
- 0:32 What Caching Actually Costs
- 1:14 Why Anthropic Cares About Hit Rate
- 2:16 How the Cache Grows Each Turn
- 5:00 Cache TTL Confusion
- 6:14 **Three Habits to Stop Burning Tokens**
- 7:43 What Breaks the Cache
- 9:15 Free Token Dashboard
- 10:05 Final Thoughts

**Key claims**:

- **Anthropic charges for cache writes** (slightly above standard input) but **cache reads are 90% cheaper** than fresh inference — the hit rate is the only metric that matters
- **The cache grows each turn** — every turn appends to the prefix, so the cache prefix gets longer the deeper you go in a session
- **Cache TTL** — confusion around 5-minute default; can extend but at higher write cost
- **Three habits to protect session limits** (chapter 6:14):
  1. Keep instructions stable across turns — don't rewrite CLAUDE.md mid-session
  2. Append, don't insert — inserting earlier in the prefix invalidates everything after
  3. Use long-context less aggressively when caching matters — TTL renewal on small turns is cheaper
- **What breaks the cache** (chapter 7:43):
  - Changes to system prompt or CLAUDE.md
  - File rearrangement that changes order of inputs
  - Tool/skill definition changes mid-session
- **Free Token Dashboard + Session Handoff Skill** — gated to his Skool community

**Strategic significance**:

1. **First explicit prompt-caching deep dive** in this vault — substrate-economics primitive at the same level as [[free-sample-phase]] (which captures the macro-economics; caching captures the per-session economics)
2. **The hit-rate metric is the canonical instrumentation surface** — pairs with [[brad-bonanno]]'s Context Audit skill (token-bloat scanner) as the two diagnostic tools every Claude Code power user needs
3. **"Why Anthropic cares about hit rate"** (chapter 1:14) — explicit signal that **Anthropic's pricing model rewards cache hits** (and therefore rewards user behavior that builds caches). Pairs with [[agent-metering]]'s "the meter is changing" thesis from a substrate-economics angle.
4. **The three habits map cleanly onto vault practice**:
   - Stable CLAUDE.md (this vault: schema-frozen)
   - Append-only (this vault: log.md append-only)
   - TTL renewal pattern (this vault: scheduled farms hit cache repeatedly)
5. **Thariq's article reference** suggests an upstream authoritative source worth ingesting separately

→ New concept: [[prompt-caching]]. Updates: [[claude-code]] (caching economics).

### #10 Nate B Jones — *The Prove-It Economy is Here | Most Marketers Aren't Ready*

**56.1K views, 2026-05-18, 22:23. → New concept: [[prove-it-economy]]. Updates [[nate-b-jones]] (14th framework), [[gtm-2026]].**

His **14th named framework** — the **prove-it economy / truth-layer** — the marketing-side reframe for the AI-agent intermediation era.

**Chapter map**:
- 00:00 **The attention economy is ending**
- 01:15 Why AI is now the first place buyers ask
- 02:45 The sound system no marketer earned
- 04:30 Back-office automation is table stakes
- 06:00 **The truth layer marketers have to own**
- 09:30 The prove-it economy for individuals
- 12:00 Two ways to purchase: AI interpretation vs. brand loyalty
- 14:00 Why human memory is more precious now
- 16:30 AI-washing creates trust debt
- 18:30 What to look for in a marketing role in 2026
- 20:30 Why opinions matter more in the age of agents

**The framing claim**: *"The common story is that AI makes marketing faster. The reality is that the entire internet economy is moving from attention to interpretation, and most marketers are still optimizing for the wrong one."*

**Two-internet economy** (chapter 12:00):

| Old internet | New internet |
|---|---|
| Buyer reads ads → forms opinion → purchases | AI agent interprets brand → recommends → buyer purchases through agent |
| Marketing optimizes attention | Marketing optimizes interpretation |
| Emotional copy wins | Provable claims win |
| Brand loyalty as moat | Brand loyalty + interpretation accuracy as moat |

**The truth layer** (chapter 6:00):

Marketers now have to **own the truth layer** their LLM interlocutors read:
- Website (the canonical brand source LLMs cite)
- Pricing pages (verifiable, structured)
- Docs (where capability claims get tested)
- (these become the **inputs to AI agents**, which are now between buyers and brands)

**AI-washing creates trust debt** (chapter 16:30) — companies and candidates who **claim AI-native positioning without evidence** get destroyed when agents fact-check. The same pattern at company-level (brands) and individual-level (candidates on LinkedIn).

**Human memory is more precious** (chapter 14:00) — counter-intuitive: as agents commoditize the interpretation layer, **emotional/social/relationship memory** becomes the human moat. Marketers should invest in **memory in humans** (community, brand affinity) and **clarity for agents** (truth layer), not automation of either.

**Strategic significance**:

1. **14th [[nate-b-jones]] framework** — second-only marketing/GTM-side framework (after the [[gtm-2026]] coverage from 2026-05-03 batch). Extends the framework cadence to cover **marketing as a tracked dimension**, not just enterprise/strategy
2. **The truth layer is the marketing-side complement to [[retrieval-contract]]** — where retrieval contract names what an *agent* declares before retrieval, truth layer names what a *brand* must declare before agents retrieve. Together they form a **publisher-side / consumer-side** pair on the same surface
3. **"AI-washing creates trust debt"** is a portable claim for [[ai-consulting]] — the same dynamic exists for consultants claiming AI-native expertise without artifacts
4. **The two-internet split confirms [[anticipation-gap]]'s thesis** at the commerce-flow level — old internet is attention-economy (proactive marketer); new internet is interpretation-economy (proactive agent)
5. **Audience: 2026 marketing roles** — extends [[chief-ai-officer]]'s CAIO framing to CMO/marketing-leader hiring. The two-internet frame is **what a 2026 marketing-leader interview should be testing for**

→ New concept: [[prove-it-economy]]. Updates: [[gtm-2026]] (truth-layer wedge).

### #11 Nate B Jones — *Opus 4.7 and OpenAI 5.5 Made Your Prompting Style Obsolete.*

**52.7K views, 2026-05-21, 25:03. → New concept: [[ai-question-method]]. Updates [[nate-b-jones]] (15th framework), [[claude-code]].**

His **15th named framework** — the **AI Question Method** — the questioning-discipline replacement for prompt engineering in the Opus 4.7 / GPT 5.5 era.

**Chapter map**:
- 00:00 **Prompt engineering is now table stakes**
- 01:24 Why agents are 100x more powerful in 2026
- 02:48 **Introducing the AI Question Method**
- 04:05 **AI as senior partner, not junior teammate**
- 06:20 Why most people are still prompting like it's 2025
- 08:10 Defining agents vs. agentic pipelines
- 10:05 **Principle 1: The flashlight intent**
- 12:30 Conveying perspective and edges in your questions
- 14:45 **Principle 2: Asking what good looks like**
- 16:20 The PRFAQ example with Prime Video
- 19:10 **Principle 3: Wrestling with data and opinions**
- 21:30 The MRR product-led growth example
- 23:45 Why memory and quick-start guides matter

**The framing claim**: *"Prompt engineering is dead, you can just ask AI for what you want — except no. The reality is that anyone running heavy knowledge work with weak questions gets shallow output from powerful agents. Operators who learn to ask sharp layered questions unlock real leverage."*

**The three principles** (chapters 10:05-21:30):

| Principle | What it is | Example |
|---|---|---|
| **1. Flashlight intent** | Convey perspective + edges of what you're investigating, not just the question | "I'm trying to understand X **because I'm deciding Y**" |
| **2. Ask what good looks like** | Specify the artifact's success criteria before generation | Prime Video PRFAQ example (chapter 16:20) |
| **3. Wrestle with data and opinions** | Force the AI to take positions and defend them, not just summarize | MRR / product-led growth example (chapter 21:30) |

**"AI as senior partner, not junior teammate"** (chapter 4:05) — the canonical reframe. Junior-teammate prompting (give instructions, expect compliance) wastes 2026-era agent capability. Senior-partner questioning (frame the problem, request judgment) unlocks the leverage.

**The PRFAQ example** (chapter 16:20) — Prime Video. Asking "write a PRFAQ for X" gets a generic artifact. Asking "if you were the PM at Prime Video deciding to ship X, what's the PRFAQ you'd write — and what are the three places it would be wrong?" gets a **defensible artifact with named risk surface**.

**The MRR example** (chapter 21:30) — product-led growth. "How do I grow MRR?" gets surface-level. "Wrestle with the trade-off between PLG conversion velocity and ACV — where do most B2B PLG companies misallocate?" gets an opinionated, actionable artifact.

**Why memory and quick-start guides matter** (chapter 23:45) — the **vault-side complement**. Once you ask sharp questions, the answers need a place to compound. Memory layers (Claude Auto Memory, wiki, LLM Wiki) are how the senior-partner relationship accumulates context across sessions.

**Strategic significance**:

1. **15th [[nate-b-jones]] framework** — sustained framework-per-video cadence now at **15 frameworks in 18 days** (T/C/L/D 2026-05-04 → AI Question Method 2026-05-21)
2. **The "senior partner, not junior teammate" reframe is portable to 3Ps client positioning** — same shift consultants need to make with AI-augmented clients
3. **The three principles are diagnostic-ready** — like [[nate-b-jones]]' prior frameworks, AI Question Method has 3 questions that double as an audit
4. **Pairs with [[karpathy-llm-wiki]] + [[prompt-caching]]** — the question-discipline (Nate) + memory layer (Karpathy/wiki) + cache-economics (Nate Herk #9) form a **complete senior-partner-workflow stack**
5. **Confirms the [[free-sample-phase]] economics** — Opus 4.7 / GPT 5.5 capability jump means **questioning skill is the differentiator**, not model access. The free-sample-phase doesn't matter if questions stay weak.

→ New concept: [[ai-question-method]]. Updates: [[claude-code]] (Opus 4.7 capability shift).

### #12 Nate B Jones — *These 5 Infrastructure Giants Secretly Rule AI*

**20.2K views, 2026-05-20, 20:19. → New concept: [[infrastructure-control-layer]]. Updates [[nate-b-jones]] (16th framework), [[agent-security]].**

His **16th named framework** — the **5 infrastructure control points** that actually determine whether agents reach production. The **substrate-control-layer complement** to [[agentic-implementation-layer]] (where-value-lives) and [[agent-protocol-stack]] (which-protocols-matter).

**Chapter map**:
- 00:00 The companies that actually decide if your agent ships
- 01:20 Compute matters but compute isn't the whole story
- 02:40 The agent layer underneath the protocols
- 03:30 **Runtime as a control point**: Cloudflare, AWS, Vercel
- 05:40 Why runtime belongs at the top of your control map
- 06:30 **Identity for agents**: Auth0, Okta, WorkOS, Entra
- 08:50 Delegated authority and why fuzzy authority is dangerous
- 10:30 **The data control point**: Snowflake, Databricks, BigQuery
- 13:00 **Payments and institutional trust**: Stripe and the card networks
- 16:00 **Observability**: why logging isn't enough for agent runs
- 18:00 **The kill switch** is a multi-layer product feature
- 19:20 **The seven questions to map any agent workflow**

**The five control points** (the master taxonomy):

| Control point | Vendors | Decision question | Failure mode |
|---|---|---|---|
| **Runtime** | Cloudflare, AWS, Vercel | Where does the agent run? | Wrong-runtime = wrong scaling/latency/cost profile |
| **Identity** | Auth0, Okta, WorkOS, Entra (Microsoft) | Who is the agent acting as? | Fuzzy authority (chapter 8:50) — same vulnerability class as Lindy/McKinsey Lilly |
| **Data** | Snowflake, Databricks, BigQuery | What governed data can the agent see? | Ungoverned RAG = data leak surface |
| **Payments** | Stripe, Visa, Mastercard | Who can the agent pay (and how much)? | Pairs with [[agentic-commerce]] AP2/x402 |
| **Observability** | Datadog, Honeycomb, etc. | What did the agent actually do? | Logging ≠ observability (chapter 16:00) |

**The kill switch as multi-layer product feature** (chapter 18:00):

A single kill switch isn't enough. The kill switch lives at:
- **Runtime** (kill the process)
- **Identity** (revoke agent's token)
- **Data** (revoke read access)
- **Payments** (block agent's payment instrument)
- **Observability** (still need to know what happened pre-kill)

**"The seven questions to map any agent workflow"** (chapter 19:20) — the **builder-side diagnostic**. Combined with the [[agent-protocol-stack]] six-question diagnostic and [[capital-allocation-framework]] five-lever diagnostic, [[nate-b-jones]] has now shipped **three workflow-diagnostic question-sets in five days**.

**"The agent layer underneath the protocols"** (chapter 2:40) — explicit positioning: the infrastructure control layer sits **below** [[agent-protocol-stack]] (MCP/A2A/AG-UI) and **below** [[agentic-implementation-layer]] (where-value-lives). Together: **a complete agent-infrastructure stack** with named vendors at each layer.

**Strategic significance**:

1. **16th framework from [[nate-b-jones]]** — extends framework cadence to 16-in-19-days
2. **The full agent-infrastructure-stack now mapped** across 4 [[nate-b-jones]] frameworks: [[infrastructure-control-layer]] (substrate) + [[agent-protocol-stack]] (protocols) + [[agentic-implementation-layer]] (value) + [[agent-metering]] (pricing). All four ship in **8 days** (2026-05-14 to 2026-05-20)
3. **Identity layer is the new procurement frontier** — extends [[agent-security]]'s "does your platform know humans from agents" with vendor-specific answers (Auth0 / WorkOS / Entra)
4. **Cloudflare / Modal / Trigger.dev / AWS Bedrock all overlap as "runtime"** — confirms [[deployment-framework]] Method 3 maps onto the runtime-layer in this taxonomy. Modal/Trigger.dev (small) + Cloudflare/AWS/Vercel (giant) split the runtime space at different sizes
5. **"Logging isn't observability for agents"** (chapter 16:00) — extends [[agent-security]] judge-architecture pattern: the judge's *decisions* need to be observable, not just the actor's *outputs*

→ New concept: [[infrastructure-control-layer]]. Major updates: [[agent-security]] (kill switch is multi-layer), [[agentic-commerce]] (payments-layer overlap).

## Cross-batch patterns

### The single biggest news batch since cold start

| Event | Source | Strategic weight |
|---|---|---|
| **[[andrej-karpathy]] joins [[anthropic]]** | [[nate-herk]] #3 (105K views) | Highest — the LLM Wiki author crosses to the lab whose product line he was parallel-tracking |
| **[[anthropic]] ships [[claude-for-small-business]]** | [[brad-bonanno]] #7 | High — first Anthropic-shipped vertical plugin; SMB-targeted 30-skill pack |
| **[[ai-labs]] (new) ships internal-skill reverse-engineering** | AI LABS #1 (36K views) | Medium-high — first canonical "what Anthropic uses internally" coverage |
| **[[eric-tech]] (new) ships /wiki skill** | Eric Tech #8 (3.4K views) | Medium — first creator-shipped parallel of this vault's exact architecture |
| **[[nate-b-jones]] ships 4 more frameworks** | #5/#6/#10/#11/#12 | High — extends framework cadence to 16 |

### Nate B Jones extends framework cadence to 16

Now: **16 named frameworks in 19 days** (T/C/L/D 2026-05-04 → infrastructure control layer 2026-05-20). The five new frameworks in this batch:

| # | Framework | Layer | Diagnostic question |
|---|---|---|---|
| 12 | [[capital-allocation-framework]] | Decision | Which lever? (automate/build/buy/hire/wait) |
| 13 | [[agent-protocol-stack]] | Protocols | Which protocol layer does this need? |
| 14 | [[prove-it-economy]] | Marketing/GTM | Are you optimizing for attention or interpretation? |
| 15 | [[ai-question-method]] | Questioning skill | Are you prompting or questioning? |
| 16 | [[infrastructure-control-layer]] | Substrate vendors | Which 5 control points does your agent touch? |

**The full agent-infrastructure stack from [[nate-b-jones]] in 8 days (2026-05-14 to 2026-05-22)**:

| Layer | Framework | Vendors named |
|---|---|---|
| **Infrastructure** | [[infrastructure-control-layer]] | Cloudflare/AWS/Vercel + Auth0/Okta/WorkOS + Snowflake/Databricks + Stripe + observability |
| **Protocols** | [[agent-protocol-stack]] | MCP / A2A / AG-UI + A2UI / AP2 / x402 |
| **Implementation/value** | [[agentic-implementation-layer]] | Anthropic/OpenAI + McKinsey/BCG/Bain/Deloitte + Salesforce/ServiceNow/SAP + PE |
| **Pricing** | [[agent-metering]] | Salesforce Flex Credits + Microsoft Copilot credits + ServiceNow Action Fabric + SAP API policy |
| **Decision** | [[capital-allocation-framework]] | (cross-cuts all four layers — which lever per workflow) |

This is the **single most comprehensive 4-layer enterprise-AI stack map** in the vault, all from one creator in 8 days.

### Nate Herk extends framework production to 4 frameworks per batch

Nate Herk now sits at **15 videos tracked across 9 digests**, with 4 videos in this batch alone. His operational-side framework count now:

| Framework | Date |
|---|---|
| [[free-sample-phase]] | 2026-05-13 |
| [[claude-code-levels]] | 2026-05-12 |
| [[deployment-framework]] | 2026-05-15 |
| 3-layer Claude Code ↔ Codex mental model (#2) | 2026-05-18 |
| [[chief-ai-officer]] career framing (#4) | 2026-05-17 |
| [[prompt-caching]] habits (#9) | 2026-05-21 |

Six operational/career frameworks in 10 days. **Nate Herk + Nate B Jones now publish a combined 22 named frameworks in 19 days** — the single biggest creator-side framework production cycle tracked in this vault.

### Karpathy-Anthropic convergence locks several prior threads

The Karpathy hire (Nate Herk #3) **closes several previously-open threads**:

| Prior thread | How Karpathy hire closes it |
|---|---|
| `karpathy/autoresearch` vs LLM Wiki gist ([[andrej-karpathy]] open Q) | Both become Anthropic-internal — productized as Claude Code primitives |
| Whether `karpathy/autoresearch` is the production form of LLM Wiki ([[karpathy-llm-wiki]] open Q) | Will be answered by Anthropic's product roadmap, not external creator coverage |
| Predictions for Claude Code 2026-Q3 ([[free-sample-phase]] follow-up) | Nate Herk's 3 predictions (chapter 12:01) supersede prior speculation — context-marketplace + education-layer + unified context-substrate |
| [[brad-bonanno]] skills-marketplace roadmap | Anthropic-shipped vertical plugins ([[claude-for-small-business]]) may preempt Brad's marketplace |

### The vault's architecture is now upstream-validated

Two videos in this batch independently validate the vault's architecture:

1. **[[nate-herk]] #3** — "LLM Wiki and Your Data Moat" (chapter 6:25) — explicit claim that **the wiki is the moat**. The vault's existence is the moat.
2. **[[eric-tech]] #8** — ships the **same primitive triple** (`/wiki` skill + farmer subagents + cron-scheduling) the vault implements. Convergent evolution = strong correctness signal.

Combined: **the vault is on the canonical pattern**, but **the pattern is no longer differentiating**. Differentiation must come from **content quality** + **multi-source farming** + **synthesis depth** (see [[karpathy-llm-wiki]] update).

## Pages created or updated

### Created
- `wiki/sources/youtube-digest-apify-2026-05-22.md` *(this page)*
- `wiki/entities/eric-tech.md` *(new entity)*
- `wiki/entities/ai-labs.md` *(new entity)*
- `wiki/concepts/claude-for-small-business.md`
- `wiki/concepts/capital-allocation-framework.md`
- `wiki/concepts/agent-protocol-stack.md`
- `wiki/concepts/chief-ai-officer.md`
- `wiki/concepts/prove-it-economy.md`
- `wiki/concepts/ai-question-method.md`
- `wiki/concepts/prompt-caching.md`
- `wiki/concepts/infrastructure-control-layer.md`

### Updated
- `wiki/entities/andrej-karpathy.md` — joins Anthropic (major rewrite)
- `wiki/entities/anthropic.md` — Karpathy hire + Claude for Small Business launch
- `wiki/entities/nate-herk.md` — 4 more videos (12 → 16 tracked), CAIO/caching/Codex
- `wiki/entities/nate-b-jones.md` — 5 more videos (15 → 20 tracked), 5 more frameworks (11 → 16)
- `wiki/entities/brad-bonanno.md` — Phase 4 (Claude for Small Business coverage)
- `wiki/concepts/karpathy-llm-wiki.md` — Eric Tech's parallel + Anthropic-internal future
- `wiki/concepts/claude-code.md` — Karpathy hire context + Opus 4.7 + caching economics
- `wiki/concepts/claude-skills.md` — Anthropic internal-skill inventory + 30-skill SMB pack
- `wiki/concepts/codex.md` — 3-layer cross-substrate compatibility
- `wiki/concepts/mcp.md` — placed in 6-protocol agent-protocol-stack
- `wiki/concepts/agentic-commerce.md` — AP2/x402 in protocol-stack context
- `wiki/concepts/agent-security.md` — kill switch as multi-layer feature
- `wiki/concepts/agentic-implementation-layer.md` — protocol stack as deployment substrate
- `wiki/concepts/gtm-2026.md` — prove-it economy / truth layer addition
- `wiki/concepts/context-farming.md` — Eric Tech parallel

## Related pages

- [[andrej-karpathy]] — joins Anthropic
- [[anthropic]] — Karpathy hire + Claude for Small Business launch
- [[claude-for-small-business]] — new Anthropic vertical plugin
- [[capital-allocation-framework]] — 5 levers (Nate B Jones #5)
- [[agent-protocol-stack]] — 6 protocols (Nate B Jones #6)
- [[chief-ai-officer]] — CAIO career path (Nate Herk #4)
- [[prove-it-economy]] — truth-layer marketing reframe (Nate B Jones #10)
- [[ai-question-method]] — senior-partner questioning (Nate B Jones #11)
- [[prompt-caching]] — substrate-economics deep dive (Nate Herk #9)
- [[infrastructure-control-layer]] — 5 control points (Nate B Jones #12)
- [[eric-tech]] — new entity, /wiki skill
- [[ai-labs]] — new entity, Anthropic internal-skill reverse-engineering
- [[karpathy-llm-wiki]] — Karpathy hire makes pattern Anthropic-internal-future
- [[free-sample-phase]] — context-marketplace prediction extends this
- [[plugin-marketplace]] — Claude for Small Business preempts this layer
- [[execution-layer]] — Brad's Phase-3 framework
- [[agentic-implementation-layer]] — protocol-stack + infrastructure layer = full enterprise stack
- [[agent-metering]] — pricing-side complement
- [[deployment-framework]] — Method 3 maps onto runtime-layer in [[infrastructure-control-layer]]
- [[agent-security]] — kill switch multi-layer extension
- [[mcp]] — now layer 1 of [[agent-protocol-stack]]
- [[agentic-commerce]] — AP2/x402 overlap with protocol stack
- [[claude-code]] — Karpathy + Opus 4.7 + caching primitives
- [[codex]] — 3-layer cross-substrate compatibility
- [[claude-skills]] — internal-skill inventory + 30-skill SMB pack
- [[ai-consulting]] — CAIO sister category
