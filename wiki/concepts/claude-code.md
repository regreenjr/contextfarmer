---
title: Claude Code
category: concept
summary: Anthropic's CLI/agent tool; primary substrate for Skills, MCP, sub-agents, Routines, hooks, Channels, Scheduled Tasks, Auto Memory; in 2026-05 [[codex]] and [[hermes-agent]] confirmed as parallel substrates; SpaceX deal + retention boost = ~3x baseline rate limits; new primitives in 2026-05: Agent View + /goal command (multi-agent), Claude Agent SDK, Managed Agents & Hooks; **2026-05-19 [[andrej-karpathy]] joins [[anthropic]]** — LLM Wiki + autoresearch + /goal-loop primitives become first-party Anthropic architecture; **2026-05-21 Opus 4.7 + GPT 5.5 capability jump** makes prompt engineering "table stakes" per [[ai-question-method]]; **in 2026-05-23 batch the Opus-4.7 capability set extends further** via [[project-room-workflow]] (folder-tree-walking) + [[self-improving-skills]] (closed-loop optimization); **in 2026-05-25 batch the Emergence AI 15-day virtual town experiment surfaces a Claude-specific failure mode** — [[long-running-benchmarks]] ([[nate-b-jones]]' 19th framework) names *Claude voted yes on everything* as a "polite agreement" failure mode in trajectory-level eval (potentially RLHF-target artifact); **also 2026-05-25 [[tristen-obrien]]'s 5.3K sub-7-min explainer extends the beginner-tier creator funnel** below [[chase-ai]]/[[ben-ai]]/[[anthropic]]'s 100K+ tier — pizza-shop catering quote demo as canonical SMB-operator skill build; **in 2026-05-28 batch (1) [[document-truth-layer]] ([[nate-b-jones]]' 23rd framework) adds the Office-file-reliability discipline** (four-stage pipeline + hostile-reviewer pass for AI-built decks/models/Word docs) and **(2) [[nate-herk]]'s 100-hour [[claude-code-vs-codex]] shootout** ships the first substrate *performance* comparison (vs prior architectural-symmetry coverage), plus [[kevin-stratvert]] confirms skills run cross-surface (Chat + Cowork + Code)
tags: [claude-code, anthropic, agentic, cli, claude-skills, mcp, routines, telegram, scheduled-tasks, auto-memory, voice-agents, antigravity, codex, hermes-agent, printing-press, plugins, cross-vendor, skill-creator, agent-security, agent-view, goal-command, multi-agent, claude-code-levels, execution-layer, free-sample-phase, business-adoption, rate-limits, deployment-framework, claude-agent-sdk, managed-agents, hooks, modal, trigger-dev, karpathy-anthropic, opus-4.7, ai-question-method, claude-for-small-business, prompt-caching, data-moat, context-marketplace, three-time-scales, project-room-workflow, self-improving-skills, files-as-canvas, folder-tree-walking, binary-criteria, sullivan-cromwell, autoresearch-lineage, long-running-benchmarks, claude-town, polite-agreement, emergence-ai, harness-thesis, tristen-obrien, beginner-tier-explainer, pizza-shop-demo, document-truth-layer, hostile-reviewer, office-files, claude-code-vs-codex, head-to-head, performance-shootout, cross-surface-skills, kevin-stratvert, dynamic-workflows, complexity-ladder, goal-vs-workflow, depth-vs-width, ultracode, deep-research, orchestration, grill-me-skill, context-extraction, feature-tier-list, skills-are-the-unlock, harness-over-model, workflows-command]
sources: 17
updated: 2026-06-05
---

# Claude Code

[[anthropic]]'s CLI + agentic tool. The substrate that hosts [[claude-skills]], [[mcp]] integrations, sub-agents, hooks, and (as of April 2026) Routines (scheduled tasks).

## Versions

- **Claude Code 2.0** — released ~April 2026. Headline framing in the wild: *"automate anything"* ([[jack-roberts]] coverage in [[youtube-digest-2026-05-03]]).

## Core primitives

- **Skills** — see [[claude-skills]]
- **MCP** — see [[mcp]]; lets Claude Code talk to external services
- **Sub-agents** — dispatched specialized agents (e.g. [[wiki-ingestor]])
- **Hooks** — event-driven shell commands configured via settings.json
- **Routines** — scheduled cloud-running agents (April 2026); the scheduling primitive for [[context-farming]]
- **Channels** (Telegram, etc.) — first-party messaging surfaces; per [[brad-bonanno]] in [[youtube-digest-2026-05-03-r3]] #4, Channels obsoletes the OpenClaude open-source Telegram-Claude bridge
- **Scheduled Tasks** (`/loop` command) — cron-style scheduling without VPS or Docker; the substrate behind this vault's farmer scheduling
- **Auto Memory** — persistent file-based memory at `~/.claude/projects/.../memory/`; types: user, feedback, project, reference (per the user's global CLAUDE.md auto-memory section)
- **Slash commands** — user-invocable skill bindings (e.g. `/wiki-ingest`)
- **Plugins / marketplaces** — `claude-plugins-official` and community marketplaces; install path for skills like `skill-creator`, `superpowers`, `frontend-design`, etc. ([[nate-herk]] #25 in [[youtube-digest-apify-2026-05-03]])
- **Agent View** (2026-05-12) — multi-session orchestration from a single terminal tab; replaces external terminal-multiplexers for multi-agent setups; covered by [[nate-herk]] #2 in [[youtube-digest-apify-2026-05-12]]
- **/goal command** (2026-05-12) — long-running agent primitive that pairs with Agent View; persistent goal across multiple work cycles; third time-cadence primitive alongside `/loop` (scheduled) and Routines (cloud-scheduled)
- **/rewind** (surfaced 2026-05-12 via [[nate-herk]] #6 *Every Level of Claude*) — session-state rollback primitive; companion to Auto Memory's forward-persistence; Level 4 in [[claude-code-levels]]
- **Shift Tab Twice** (surfaced 2026-05-12 via [[nate-herk]] #6) — likely a Plan Mode toggle or alternate UI mode; Level 4 primitive; specifics gated to transcript
- **Claude Agent SDK** (surfaced 2026-05-15 via [[nate-herk]] [[deployment-framework]] chapter 15:52) — the SDK that lets you build Claude agents **outside the Claude Code CLI**; the unlock for packaged-product Claude agents (Claude as library, not CLI); pairs with [[codex]]' SDK as cross-vendor SDK-tier convergence; first surfacing in this vault
- **Managed Agents & Hooks** (surfaced 2026-05-15 via [[nate-herk]] [[deployment-framework]] chapter 19:18) — Anthropic-hosted always-on agents with event-triggered hooks; deployment-tier equivalent of `claude-plugins-official` for running agents (not just installing skills); closes the gap between Routines (scheduled) and external runtime (event-driven)
- **Opus 4.7** (substrate model, 2026-05) — frontier-tier capability jump that triggers the **questioning-discipline-replaces-prompt-engineering** shift per [[ai-question-method]] ([[nate-b-jones]] #11 in [[youtube-digest-apify-2026-05-22]]); 2026-era frontier models have **senior-partner capability**; junior-teammate prompting wastes the capability
- **Prompt caching** — [[prompt-caching]] mechanics (cache reads ~90% cheaper than fresh inference, ~5min TTL default, hit rate as canonical metric); the **per-session substrate-economics primitive** sitting alongside [[free-sample-phase]] (macro) and [[agent-metering]] (renewal). [[nate-herk]]'s 2026-05-21 deep dive in [[youtube-digest-apify-2026-05-22]] (#9, 17K views) names three habits: stable instructions / append-don't-insert / TTL-aware long-context use. References Thariq's article (`x.com/trq212/...`) as canonical authority
- **Dynamic workflows** (added in the [[opus-4-8]] era; surfaced 2026-05-30 via [[nate-herk]] in [[youtube-digest-apify-2026-06-02]]) — a **deterministic multi-agent orchestration** layer that scripts how subagents run (fan-out / pipeline / verify); the **top rung of the orchestration complexity ladder** (skills → subagents → agent teams → dynamic workflows) and the most token-expensive primitive (*"one prompt burned through half my $200 monthly plan"*). `/goal` vs workflow = **depth vs width**. → See [[dynamic-workflows]]
- **Ultracode mode** (surfaced 2026-05-30 via [[nate-herk]] #3) — **first vault surfacing**. A higher-power Claude Code mode flagged as a session-limit risk ("don't accidentally torch your session limit"); appears to escalate effort/orchestration aggressiveness. Specifics gated to transcript.
- **/deep-research** (surfaced 2026-05-30 via [[nate-herk]] #3) — **first vault surfacing**. A research-oriented high-cost mode (likely the Claude Code analog of the deep-research harness pattern). Specifics gated to transcript.

## Surface area in the YouTube creator space

### Tier 1 (1M+ subs / mainstream)
- Tech With Tim — *The Ultimate Claude Code Guide* (umbrella tutorials)
- Sequoia Capital — hosted [[andrej-karpathy]] *Vibe Coding to Agentic Engineering* (550K views, biggest video in [[youtube-digest-apify-2026-05-03]])
- [[nick-saraev]] — *Claude Code Full Course (4 HOURS)* — **1.56M views**, the highest-view educational Claude Code video tracked here ([[youtube-digest-apify-2026-05-05]] #4)

### Tier 2 (200K-1M)
- [[nate-herk]] — opinionated stacks ("Claude Code Operating Systems", 2hr course); skill curation; Karpathy wiki implementation
- [[jack-roberts]] — version coverage, mainstream awareness
- [[greg-isenberg]] — mainstream-creator explainers
- [[anthropic]] official channel — *Claude Agent Skills Explained* (201K)

### Tier 3 (50K-200K)
- [[grace-leung]] — vertical-specific (marketing) practitioner content
- [[brad-bonanno]] — context-farming, second-brain, usage-limit optimization
- [[code-with-beto]] — skill authoring best practices
- [[brock-mesarich]] — non-technical-audience skill curation; single-plugin bundle distribution (134.9K views on his 15-skill bundle, [[youtube-digest-apify-2026-05-04]])
- Confluent Developer (Tim Berglund) — Skills vs MCP architectural framings
- [[nate-b-jones]] — analyst/strategy framings

### Tier 4 (<50K)
- Matt Maher — quick skill-builder demos
- [[tonbi-onchain-ai-garage]] — wiki implementation
- (vertical-specific creators emerging)

## Key 2026 patterns observed in [[youtube-digest-apify-2026-05-03]]

- **"Operating Systems"** framing ([[nate-herk]] #3) — opinionated stacks (Three Ms + Four Cs) bundling Skills, Routines, dashboards, LLM Wiki, Slack/email/calendar
- **Skill curation videos** (#25 *I Tried 100+ Claude Code Skills*) — too many skills exist for users to evaluate; curation is its own format
- **Skill-builder meta-skills** — Skill Creator (Anthropic), `/create-farmer` ([[brad-bonanno]]), generic patterns
- **Karpathy LLM Wiki implementations** — 5 videos this digest implementing the [[karpathy-llm-wiki]] pattern in Claude Code
- **Context bloat optimization** ([[brad-bonanno]] #19) — replace MCP with CLI, optimize CLAUDE.md, cut skill bloat, settings.json tuning
- **Playwright integration** ([[nate-herk]] #12) — browser automation as a skill
- **Tricks/hacks compilation videos** ([[nate-herk]] #17 *32 Tricks*) — the topic is mature enough for "shortcut" content

## Patterns added in [[youtube-digest-apify-2026-05-05]]

- **Voice agents as Claude Code build target** ([[nate-herk]] #6) — see [[voice-agents]]. ElevenLabs Agents API + cal.com + Claude Code Plan Mode. The "build by description" pattern now extends to voice/phone surfaces; voice was the holdout vertical that still required dashboards.
- **Creative agency on Claude** ([[nate-herk]] #3) — Higgsfield via MCP/CLI + Marketing Studio + hyper-motion + image-to-ad + Google Sheet tracker + Routines. Companion to [[grace-leung]]'s marketing-team build; extends [[claude-design]] into video/ads.
- **Antigravity as recommended host IDE** ([[nick-saraev]] #4) — Saraev's 1.56M-view course recommends Gemini's IDE as the host for Claude Code work. Cross-vendor stack signal — host-IDE choice is no longer Cursor-default.
- **Skill-authoring as a 229K-view discipline** ([[ben-ai]] #7) — "3 Types of Skills" + "Skill Building Prompt Framework"; the highest-view authoring (vs curation) voice is now non-Anthropic, competing with the official Skill Creator meta-skill.
- **`karpathy/autoresearch` surfaces** ([[dubibubii]] #5) — separate Karpathy project from the LLM Wiki gist; possibly the production form of the [[karpathy-llm-wiki]] pattern. Open question.
- **Cross-curator consensus skills emerging** — Frontend Design + Superpowers + Context7 surface in three+ curation videos ([[nate-herk]] #25, [[brock-mesarich]], [[dubibubii]] #5). A small "must-install" core is forming.

## Patterns added in [[youtube-digest-apify-2026-05-06]]

- **Codex confirmed as parallel substrate** ([[nate-herk]] #2, *Master 97% of Codex in 1 Hour*) — the first major Codex educational entry from a top-tier Claude-ecosystem creator. Codex CLI ships **Plan Mode**, **Skills**, **weekly automations**, **browser-use** — the same primitive set as Claude Code. Architectural concepts in this page **port** to OpenAI's coding-agent CLI; the vault's IP is vendor-agnostic at the spec level. Open: format compatibility of Skills across substrates; MCP support in Codex. → See [[codex]].
- **Skill Systems composition layer named** ([[simon-scrapes]] #3) — the missing rung between *authoring* (one skill) and *curation* (which to install) is now explicitly named: modular skills chained into end-to-end automations vs the "mega-skill" anti-pattern. Direct architectural artifact for productizing consulting deliverables. → See [[skill-systems]].
- **Anticipation gap + permission ladder** ([[nate-b-jones]] #1) — agent-side diagnostic that names *why* coding agents (Claude Code, Codex) crossed the agent-usefulness threshold while consumer agents haven't: clean verification (tests, compilers) closes the anticipation gap. The **read → suggest → draft → act-with-confirmation → autonomous** ladder applies to Claude Code skill/sub-agent/routine permission design. → See [[anticipation-gap]].

## Patterns added in [[youtube-digest-apify-2026-05-10]]

- **Session limits doubled (Anthropic-SpaceX compute deal)** ([[nate-herk]] #9, 87.7K views — highest-views entry in the batch) — Anthropic doubled Claude Code's 5-hour rate limits, killed peak-hours throttle, raised API limits across the board. The [[brad-bonanno]] context-bloat optimization argument loses some urgency; raw allowance roughly doubled overnight. → See [[anthropic]] update.
- **CLI as packaged-product alternative to MCP** ([[nate-herk]] #1, 52.2K views) — [[printing-press]] is a catalog of CLIs + a builder that converts "almost anything" into a CLI. The packaged evolution of [[brad-bonanno]]'s "replace MCP with CLI" optimization. *"MCPs eat your tokens for breakfast"* is the framing. CLI is the right substrate for: token-sensitive setups, sites without APIs, deterministic actions where MCP schema-load is overhead. → See [[printing-press]].
- **Hermes Agent as parallel substrate** ([[nate-herk]] #5, 21.4K views; [[corey-ganim]] #3, 3.3K views) — [[hermes-agent]] is the **third tracked substrate** after Claude Code and [[codex]]. VPS-deployed always-on agent with Five Pillars (skills, cron, Telegram, GitHub backup, multi-agent scaling). Codex backend, Hostinger VPS, Telegram-first surface. Substantively different deployment topology from Claude Code (local session-based). The two may be complementary use cases, not strict competitors. → See [[hermes-agent]].
- **Plugins-as-mech-suit taxonomy** ([[nate-b-jones]] #11, 31.1K views) — explicit 6-layer agentic-scaffolding map: prompts, skills, **plugins**, MCPs, hooks, scripts. Plugins are bigger than MCPs; the app-store analogy undersells them. The taxonomy layer **above** [[skill-systems]] (composition) and [[claude-skills]] (units). Operators waste 40% of their time by putting work in the wrong layer. → See [[plugins]].
- **Work Primitive (access/meaning/authority)** ([[nate-b-jones]] #7, 27.6K views) — the substrate-side framework. *Why* coding agents arrived first: software has unusually rich work semantics (compilers, ASTs, types, tests). Computer use is the universal adapter for the messy middle, not the strategic primitive. → See [[work-primitive]].
- **OpenClaw reframed as runtime abstraction** ([[nate-b-jones]] #8, 53.3K views) — major reframe; OpenClaw is **becoming infrastructure** below the model layer that lets work survive model/vendor churn. Open question whether [[brad-bonanno]]'s "OpenClaw is dead" view (wrapper killed by first-party features) and Nate B Jones' "OpenClaw is runtime" view are both correct (different use cases) or one wins. → Likely needs an [[openclaw]] entity page.
- **Brad's 13-product Anthropic surface tour** ([[brad-bonanno]] #2, 3.5K views) — canonical Anthropic product-surface inventory: Chat, Connectors, Projects, Cowork, Skills, Dispatch, Word/PowerPoint/Excel add-ins, Chrome, Design, Code, Routines. Thesis: paying users use ~2% of what Claude exposes. → See [[anthropic]] update.
- **Code comprehensibility as security property** ([[nate-b-jones]] #12, 29.8K views) — first AI-as-security-tool entry in this vault. Anthropic's Mythos pointed at Mozilla Firefox shipped 271 vulnerability fixes in one cycle. → See [[code-comprehensibility]].
- **Knowledge layer commercially shipped** ([[the-ai-automators]] #4, 18.6K views) — Pinecone Nexus, Microsoft Fabric IQ, Google Knowledge Catalog all ship the [[karpathy-llm-wiki]] architecture in roughly four weeks. Validation that the patterns this vault tracks are **enterprise-software-shipped**, not hobbyist-only. → See [[knowledge-layer]].

## Patterns added in [[youtube-digest-apify-2026-05-11]]

- **Skill Creator first-hand walkthrough** ([[chase-ai]] #2, 107.3K views) — Anthropic's [[skill-creator]] meta-skill, previously referenced in this vault without first-hand coverage, finally gets an end-to-end demo: plain-language evals + blind A/B testing + description-field optimization. Skills become **testable software** rather than prose snippets. The two-types skill split (capability uplift vs encoded preference) gives each skill type a clean eval target. → See [[skill-creator]].
- **Agent-security responder position** ([[nate-b-jones]] #1, 53.6K views) — following the McKinsey "Lilly" exploit ($20 SQL injection through 22 of 200 unauthenticated endpoints), Claude Code is positioned in the six-vendor agent-security responder set ([[anthropic]] / [[openai]] / SAP / [[pinecone]] / Salesforce / ServiceNow). The buyer-side question — "does your platform know humans from agents?" — applies to any agent-touching surface, including Claude Code's MCP / Skill / sub-agent dispatch surfaces. Anthropic's response shape is presumably distinct agent identity primitives in Claude Code / MCP. → See [[agent-security]].

## Patterns added in [[youtube-digest-apify-2026-05-12]]

- **Agent View + /goal command first-party multi-agent orchestration** ([[nate-herk]] #2, 21.4K views) — same-day walkthrough of Claude Code's newest first-party primitive: multiple sessions managed from a single terminal tab, plus the new `/goal` command for long-running agents. Closes the multi-agent orchestration gap previously filled by external tooling (tmux, terminal-multiplexers) or [[hermes-agent]]'s VPS topology. Open: how Agent View's `/goal` interacts with the existing `/loop` (scheduled) and Routines (cloud-scheduled) primitives — likely complementary as the three time-cadence primitives. Partial overlap with [[hermes-agent]]'s "multi-agent scaling" pillar; may weaken Hermes' value proposition for simpler local-multi-agent setups. → New primitive in Core primitives table.
- **Agent-security architectural pattern (LLM-as-judge at the action boundary)** ([[nate-b-jones]] #1, 25.7K views) — second consecutive video on agent-security, this time the build-side pattern. Architectural answer to the previous batch's procurement-side question. **A separate frontier-model judge** decides proceed/refuse/escalate at each action, based on user intent + proposed action + blast radius. **Four action-risk classes** (read / write / high-stakes / external-irreversible) get different decision scopes. **Lindy** is the public case study (unauthorized-emails incident). For Claude Code: the canonical judge architecture for multi-agent setups (now natively supported via Agent View) and high-stakes Skills/MCP/sub-agent dispatches. → See [[agent-security]] (architectural pattern section).

## Patterns added in [[youtube-digest-apify-2026-05-14]]

- **+50% rate-limit retention boost** ([[nate-herk]] #5, 48.4K views) — same-week after [[anthropic]] passes [[openai]] in business adoption per Ramp/EconLab. Total Claude Code rate-limit increase across two weeks is **~3x baseline** (SpaceX deal 2x on 2026-05-07 + retention boost +50% on 2026-05-13). Substantively changes the [[brad-bonanno]] context-bloat optimization urgency and the cost basis for 3Ps client engagements. → See [[anthropic]] update + [[free-sample-phase]] framing for the strategic context.
- **Five-level mastery framework** ([[nate-herk]] #6, 73.4K views — his highest-viewed video in this batch) — *Every Level of Claude Explained in 21 Minutes*. First explicit progression framework for Claude Code in this vault:
  - **Level 1** — entry-level CLI use
  - **Level 2** — hidden artifacts + Office takeover (Word/PowerPoint/Excel add-ins)
  - **Level 3** — "Figma killer?" ([[claude-design]])
  - **Level 4** — Shift Tab Twice + `/rewind` (advanced session control; `/rewind` is a previously-untracked primitive)
  - **Level 5** — "five parallel sessions while they sleep" (Agent View + `/goal` + Routines + Channels)
  - Credibility anchor: "400 hours inside Claude"
  - The **depth-tour** companion to [[brad-bonanno]]'s 13-product **breadth-tour**
  - → See [[claude-code-levels]].
- **Execution layer (Phase 3 deployment)** ([[brad-bonanno]] #1, 56 views — just-published) — *Build an Execution Layer for Your Second Brain*. Phase 3 of Brad's trajectory: context-farming (Phase 1) → 13-product tour (Phase 2) → execution layer (Phase 3). Names the deployment / team-scaling layer above [[skill-systems]] composition:
  - Skills wired by reference, not hard-code
  - Private team marketplace from free GitHub template
  - Sub-plugins for sales / ops / customer success
  - PR-back loop (every correction = permanent company-wide upgrade)
  - **Cross-vendor framing** at chapter 4:01 — works on [[codex]] / [[hermes-agent]] too
  - → See [[execution-layer]].
- **`/rewind` is a new primitive** — Level 4 in [[claude-code-levels]] names `/rewind` as a session-state-rollback primitive (chapter 13:54). Not previously tracked. Possibly ships alongside Auto Memory; verifying via [[nate-herk]] transcript when available.
- **Shift Tab Twice** ([[nate-herk]] #6 chapter 10:40) — likely a Plan Mode toggle or alternate session UI; specifics gated to transcript.
- **[[free-sample-phase]] substrate-economics** ([[nate-herk]] #5) — names the moment when both Anthropic and OpenAI ship retention promos within hours of an adoption flip. The recommended operator play: build flexibly enough to swap substrates when pricing resets. Same insurance thesis as [[skill-systems]] / [[printing-press]] but at the *economics* layer rather than the architecture layer. → See [[free-sample-phase]].

## Patterns added in [[youtube-digest-apify-2026-05-16]]

- **[[deployment-framework]] — three-method runtime classifier** ([[nate-herk]] #1, 16.6K views) — first explicit framework for where Claude Code automations should run: Method 1 `/loop` (in-session), Method 2 Routines / Scheduled Tasks (Anthropic-hosted cloud cron), Method 3 Modal / Trigger.dev (external serverless runtime). Decision axis is "where it runs" + "how agentic it needs to be." The three methods form a buy-up funnel — Anthropic captures users at Method 1 (free), retains via Method 2 (subscription-included), and is happy to lose Method 3 to specialized runtimes (still pays for inference). → See [[deployment-framework]].
- **Claude Agent SDK** ([[nate-herk]] #1 chapter 15:52) — **first vault surfacing**. The SDK that lets you build Claude agents **outside the Claude Code CLI** — packaged-product agents (Claude as library, not CLI tool). Strategic implication: this is Anthropic's developer-facing primitive for axis-1 ([[agentic-implementation-layer]]) deployment-tier strategy. Pairs with [[codex]]' SDK pricing (referenced in [[nate-herk]]'s description via "Theo's video on SDK pricing") as cross-vendor SDK-tier convergence.
- **Managed Agents & Hooks** ([[nate-herk]] #1 chapter 19:18) — **first vault surfacing**. Anthropic-hosted always-on agents with event-triggered hooks; deployment-tier equivalent of `claude-plugins-official` for running agents (not just installing skills). Closes the gap between Routines (scheduled) and external runtime (event-driven). Likely positioning: this is Anthropic's answer to "what if I want a Cloud-hosted always-on Claude agent with event triggers" — closing the gap that Modal / Trigger.dev currently fills.
- **Modal + Trigger.dev as external-runtime vendors** ([[nate-herk]] #1 chapter 13:00) — first explicit naming of external serverless runtimes for Claude work. Both surface for the first time in this vault. Tracking candidates for any 3Ps client engagement that needs long-running or GPU-bound Claude work.

## Patterns added in [[youtube-digest-2026-05-03-r3]]

- **First-party obsoleting wrapper-OSS** ([[brad-bonanno]] #4) — Channels + Scheduled Tasks + Auto Memory replace the OpenClaude open-source Telegram bridge. Pattern: Anthropic ships first-party features ~6 months after a hot OSS wrapper appears, and the OSS goes dormant. Implications for skill builders — anything you build on top of unstable OSS gets obsoleted; build on Anthropic primitives or accept rewrite cost.
- **Mobile-first Claude.md** ([[brad-bonanno]] #4) — short responses, progress updates, auto-memory checks, permission guardrails. Codifies a "phone audience" prompt-engineering style different from desktop Claude Code.
- **Skill-stack architectural templates** ([[grace-leung]] #2 in r3) — vertical skill libraries (Brand Voice → Brand Design System → Campaign Planning → Carousel Design → Animated Motion → Campaign Manager Agent) are publishable as architectural templates, not just demos
- **PhD-research framing** ([[tommy-chryst]] #1 in r3) — Claude Code-hosted [[karpathy-llm-wiki]] is now positioned as a "ChatGPT deep research alternative" by sub-15K-view creators

## Patterns added in [[youtube-digest-apify-2026-05-28]]

- **[[document-truth-layer]] — reliable AI-built Office files** ([[nate-b-jones]] #1, 16.8K views) — the document-reliability discipline for building PowerPoint/Excel/Word with agents: four-stage pipeline (**sources → structure → creation → verification**) + a **hostile-reviewer prompt** (separate adversarial AI pass that finds the undefendable claim) + the **task risk gradient** (where AI is highest vs lowest risk on a document task). *"A prompt asks for output, a workflow defines trust."* Pairs with Anthropic's `pptx`/`xlsx`/`docx` skills (which generate the artifact — this framework *audits* it) and is the deliverable-boundary analog of [[agent-security]]'s LLM-as-judge. → See [[document-truth-layer]].
- **First substrate performance shootout** ([[nate-herk]] #5, 46.2K views) — *100 Hours Testing Claude Code vs ChatGPT Codex.* Same prompts, same builds, scored head-to-head across report generation / landing page / dashboard + pricing. The first *performance* (not architectural-symmetry) comparison of Claude Code vs [[codex]] in the vault; empirically tests the [[free-sample-phase]] thesis. Chapter arc ("Codex fights back") implies Codex overperformed Claude-default priors; verdict gated to transcript. → See [[claude-code-vs-codex]].
- **Skills confirmed cross-surface** ([[kevin-stratvert]] #4, 9.5K views) — the same skill runs across **Chat + Cowork + Claude Code**; in Claude Code skills live as folders on disk in `.claude/skills`, but the *same* skill is portable to Chat and Cowork. Resolves the long-open "are skills Code-only?" question. → See [[claude-skills]] cross-surface section + [[kevin-stratvert]].

## Patterns added in [[youtube-digest-apify-2026-06-02]]

- **Dynamic workflows — the orchestration-tier capstone** ([[nate-herk]] #3, 57.6K views) — *Claude Code Dynamic Workflows Clearly Explained.* The first vault coverage of [[opus-4-8]]'s **dynamic workflows** primitive: deterministic multi-agent orchestration that scripts fan-out / pipeline / verify. Key disambiguation tools: the **complexity ladder** (skills → subagents → agent teams → dynamic workflows — don't climb to the top by default) and **/goal vs workflow = depth vs width** (`/goal` goes deep on one thread; a workflow goes wide across many fanned-out agents). The headline risk is **token cost** — *"one prompt burned through half my $200 monthly plan"* — making workflows the substrate-economics frontier of Claude Code (pairs with [[prompt-caching]] + [[agent-metering]] + [[free-sample-phase]]). Plausibly a **Level 6** above [[claude-code-levels]]' Level 5. → See [[dynamic-workflows]].
- **Ultracode mode + /deep-research — first vault surfacing** ([[nate-herk]] #3 chapters 14:08 + 15:25) — two "hidden" higher-cost Claude Code modes Nate covers so viewers "don't accidentally torch your session limit." `ultracode` appears to escalate effort/orchestration aggressiveness; `/deep-research` is a research-oriented high-cost mode (likely the Claude Code build of the deep-research harness pattern). Both gated to transcript for exact mechanics. → See [[dynamic-workflows]].

## Patterns added in [[youtube-digest-apify-2026-06-05]]

- **Every-feature D→S tier ranking — #1 is Skills** ([[nate-herk]] #3, 40.3K views) — *I Tested Every Claude Code Feature, These 12 Are the Best.* The first **full feature-surface ranking** in the vault, scored from 500+ hours by *impact on day-to-day knowledge work and automation* (explicit caveat: an automation/knowledge-work lens, not heavy software engineering). Tiers D → C → B → A (honorable mentions) → top-12 countdown → **#1: [[claude-skills]]** (chapter 17:52). The third independent "Skills are the unlock" confirmation (with [[brad-bonanno]] + [[ben-ai]]). The full D→S placements are gated to the video; only #1 = Skills is confirmed in the digest. The feature-*inventory* companion to [[claude-code-levels]]' mastery *progression*. → See [[claude-skills]].
- **grill-me — the context-extraction front-end** ([[nate-herk]] #2, 36.8K views) — *The Skill That 10x'd My Claude Code Projects.* A free skill that runs *on* Claude Code and **interviews you to extract process knowledge into a doc**, checkpointing after each answer; *"the hardest part isn't the prompts, it's getting everything out of your head and into the system."* Front-loading context gets a skill to ~90% on the first try vs 30 iterations. → New concept: [[grill-me-skill]].
- **The harness-skeptic read on [[opus-4-8]]** ([[nate-b-jones]] #1, 34.3K views) — *Opus 4.8 Scored 81. Your Workflow Doesn't Care.* Argues the [[claude-code]] **harness** (orchestration, effort controls, [[dynamic-workflows]]) matters more than the model score: reasoning effort became **unpredictable** on 4.8, **max effort can make long-running work worse** (Vending-Bench), and the [[codex]] harness beat a higher-scoring model on real work. The `/workflows` command "reveals agent design." → New concept: [[harness-over-model]].

## Why it matters for 3Ps

Claude Code is the substrate for the entire 3Ps consulting offering. The wiki itself runs on Claude Code (Skills, sub-agents, slash commands, Routines). Tracking ecosystem shifts here = direct input to:
- Service offerings (what to teach)
- Tooling decisions (what to build)
- Content angles (what's mainstream vs. early)

## Open questions

- What did Claude Code 2.0 specifically add over 1.x? (Pull [[jack-roberts]] transcript)
- How are Skills + Routines + sub-agents + MCP *combined* in mature stacks? ([[nate-herk]]'s 2-hour AIOS course is the canonical reference)
- Plugin marketplace consolidation — Anthropic-official vs community-distributed; will Anthropic ship a paid marketplace?
- Token-cost optimization is now a skill ([[brad-bonanno]] #19 + Context Audit skill); is this temporary (will Anthropic fix it) or permanent (architecture issue)?

## Related pages

- [[claude-skills]] — primary primitive
- [[skill-systems]] — composition discipline above Claude Skills
- [[mcp]] — connector layer
- [[codex]] — sibling cross-vendor substrate (OpenAI)
- [[anticipation-gap]] — why coding agents crossed the agent-usefulness threshold
- [[voice-agents]] — newest build target on the substrate
- [[karpathy-llm-wiki]] — knowledge architecture pattern
- [[context-farming]] — automation pattern
- [[claude-design]] — sibling Anthropic product
- [[anthropic]] — vendor
- [[youtube-digest-apify-2026-05-03]], [[youtube-digest-2026-05-03]], [[youtube-digest-2026-05-03-r3]], [[youtube-digest-apify-2026-05-04]], [[youtube-digest-apify-2026-05-05]], [[youtube-digest-apify-2026-05-06]], [[youtube-digest-apify-2026-05-10]], [[youtube-digest-apify-2026-05-11]], [[youtube-digest-apify-2026-05-12]], [[youtube-digest-apify-2026-05-14]], [[youtube-digest-apify-2026-05-16]], [[youtube-digest-apify-2026-05-28]] — primary source digests
- [[hermes-agent]] — sibling parallel substrate (VPS-deployed, always-on)
- [[printing-press]] — CLI alternative tooling for token-cost optimization
- [[plugins]] — taxonomy layer above Skills
- [[work-primitive]] — substrate-side agent-readiness framework
- [[code-comprehensibility]] — codebase-side framework (Anthropic Mythos)
- [[knowledge-layer]] — commercial shipping of [[karpathy-llm-wiki]] architecture
- [[skill-creator]] — Anthropic meta-skill that benchmarks skills
- [[agent-security]] — procurement-side diagnostic; Claude Code is in the six-vendor responder set
- [[claude-code-levels]] — five-level mastery framework ([[nate-herk]] 2026-05-12)
- [[execution-layer]] — Phase 3 deployment / team-scaling pattern ([[brad-bonanno]] 2026-05-14)
- [[free-sample-phase]] — substrate-economics framing for the 2026-05-13 retention war
- [[deployment-framework]] — three-method runtime classifier + Claude Agent SDK + Managed Agents & Hooks ([[nate-herk]] 2026-05-15)
- [[plugin-marketplace]] — GitHub-hosted distribution-layer pattern ([[alex-mcfarland]] 2026-03-16, resurfaced 2026-05-16)
- [[document-truth-layer]] — Office-file-reliability discipline + hostile-reviewer pass ([[nate-b-jones]] 2026-05-27)
- [[claude-code-vs-codex]] — 100-hour substrate performance shootout ([[nate-herk]] 2026-05-26)
- [[dynamic-workflows]] — the [[opus-4-8]]-era orchestration capstone (complexity ladder + depth-vs-width + token cost + ultracode + /deep-research; [[nate-herk]] 2026-05-30)
- [[opus-4-8]] — the model generation that added dynamic workflows
- [[grill-me-skill]] — context-extraction front-end skill ([[nate-herk]] 2026-06-04)
- [[harness-over-model]] — the harness-skeptic read on 4.8; /workflows reveals agent design ([[nate-b-jones]] 2026-06-03)
- [[youtube-digest-apify-2026-06-02]] — dynamic-workflows primary source
- [[youtube-digest-apify-2026-06-05]] — feature tier-list + grill-me + harness-over-model
- Creators: [[nate-herk]], [[brad-bonanno]], [[code-with-beto]], [[grace-leung]], [[jack-roberts]], [[greg-isenberg]], [[nate-b-jones]], [[andrej-karpathy]], [[tommy-chryst]], [[brock-mesarich]], [[nick-saraev]], [[ben-ai]], [[dubibubii]], [[simon-scrapes]], [[corey-ganim]], [[the-ai-automators]], [[ai-academy]], [[chase-ai]], [[zinho-automates]], [[alex-mcfarland]], [[tristen-obrien]], [[kevin-stratvert]]
