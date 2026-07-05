---
title: Claude Skills
category: concept
summary: Reusable procedural-knowledge units in Claude Code; the canonical packaging unit of 2026's AI-creator economy; in 2026-05-22 batch ships TWO Anthropic-shipped artifacts that change the category ([[ai-labs]] internal-skill reverse-engineering + [[anthropic]] [[claude-for-small-business]]); **in 2026-05-23 [[simon-scrapes]] ships [[self-improving-skills]]** (109.7K views — highest-views Claude-Skills-eval video in vault, exceeds [[chase-ai]] 107K) — the Karpathy-autoresearch-inspired **closed-loop optimization layer** above [[skill-creator]]'s single-shot eval; **in 2026-05-25 [[tristen-obrien]] fills the sub-7-min beginner-tier explainer rung** (5.3K views) — pizza-shop catering-quote skill build for non-technical SMB operators + consumer-facing skill-provenance security framing; cumulative skills-product evolution: authoring → curation → composition ([[skill-systems]]) → deployment ([[execution-layer]]) → distribution ([[plugin-marketplace]]) → meta-skills ([[skill-creator]] / Skillify / `/smb-onboard` / generation-first [[skill-forge]]) → vertical-plugin ([[claude-for-small-business]]) → closed-loop optimization ([[self-improving-skills]]) → beginner-tier explainer ([[tristen-obrien]] pizza-shop demo) → **cross-surface confirmation ([[kevin-stratvert]] / David DeWinter — same skill on Chat + Cowork + Claude Code; resolves the long-open "are skills Code-only?" question)** → **one-skill counter-thesis ([[alek]]'s [[skill-forge]] — "stop curating, generate on demand")**
tags: [claude-skills, claude-code, agentic, anthropic, skills-marketplace, skill-authoring, skill-authoring-lessons, gotchas-section, description-field, progressive-disclosure, stop-railroading, nine-categories, skill-systems, composition, cross-vendor, codex, plugins, hermes-agent, skill-creator, evals, capability-uplift, encoded-preference, daily-driver-curation, execution-layer, sub-plugins, pr-back-loop, team-deployment, anthropic-internal-skills, verify, skillify, tech-debt, batch, security-scan, frontend-designer, code-simplifier, commit-commands, claude-for-small-business, smb-onboard, vertical-plugin, meta-skills, ai-labs, self-improving-skills, closed-loop-optimization, binary-criteria, autoresearch-lineage, overnight-improvement, beginner-explainer, pizza-shop-demo, catering-quote, non-technical-smb, skill-provenance-security, sub-7-min-format, kevin-stratvert, chat-cowork-claude-code, cross-surface-skills, thread-reply-skill, david-dewinter, quickbooks, shared-folder-sharing, surface-portable, grill-me-skill, context-extraction, front-loading-context, feature-tier-list, skills-are-the-unlock, nate-herk, brock-mesarich, skill-forge, meta-skill, generation-first, one-skill, curation-counter-thesis, alek]
sources: 19
updated: 2026-07-05
---

# Claude Skills

Reusable procedural-knowledge units in [[claude-code]]. Each skill is a markdown file (typically with frontmatter + body + optional scripts/templates) that Claude invokes when its trigger conditions match. **The canonical official explainer** is [[anthropic]]'s *Claude Agent Skills Explained* (201K views, [[youtube-digest-apify-2026-05-03]] #4).

## What Skills are not (per [[anthropic]] #4)

- **Not CLAUDE.md** — CLAUDE.md is project-wide; skills are invoked situationally
- **Not MCP servers** — see [[mcp]]; skills are local procedural knowledge, MCP is remote tool/data access
- **Not sub-agents** — sub-agents are dispatched workers; skills are knowledge packages

The 2026 rule of thumb: **local procedure = Skill, remote service = MCP, dispatched specialist = sub-agent, project-wide context = CLAUDE.md.**

## Why it's a hot topic right now

[[youtube-digest-apify-2026-05-03]] surfaced **9 of 28** videos covering Skills directly:
- [[anthropic]] #4 — *Claude Agent Skills Explained* (201K, official explainer)
- [[code-with-beto]] #6 — *How to Create Good Agent Skills* (16K, authoring best practices)
- Confluent / Tim Berglund #9 — *Agent Skills or MCP in the era of Claude Code?* (175K, architecture)
- [[nate-herk]] #3 — *Build & Sell Claude Code Operating Systems* (86K, course-length)
- [[nate-herk]] #17 — *32 Tricks to Level Up Claude Code* (110K, includes skill tricks)
- [[nate-herk]] #25 — *I Tried 100+ Claude Code Skills. These 6 Are The Best* (47K, curation)
- [[grace-leung]] #1 — *Build Your Full AI Marketing Team (Agents + Claude Skills)* (222K, vertical app)
- Matt Maher #27 — *60 Seconds to Build a Claude Code Skill That Lasts Forever* (80K, intro)
- [[brad-bonanno]] #23 — *I Turned My Second Brain Into a Company Brain* (uses `/create-farmer` meta-skill)

Plus the prior digest [[youtube-digest-2026-05-03]] covered skills heavily.

The category has crossed from "early adopter only" to "explain-to-creators" mainstream awareness ([[greg-isenberg]]'s 266K-view explainer in the prior digest; [[anthropic]]'s 201K-view official explainer here).

## Authoring best practices ([[code-with-beto]] #6 + Anthropic #4)

1. **Don't write skills manually** — use Skill Creator (Anthropic-published meta-skill)
2. **Be concise** — skills load into context; bloat compounds
3. **Set degrees of freedom explicitly** — constrain skill behavior or it drifts
4. **Test different models** — skill behavior varies by model
5. **References folder** — supplemental material loaded only when needed (this vault uses `references/` and `.templates/`)
6. **Distribute via marketplace** — `claude-plugins-official`, community marketplaces, or per-team repo

## Deployment / team-scaling layer named — "Execution Layer" ([[brad-bonanno]] #1 in [[youtube-digest-apify-2026-05-14]])

[[brad-bonanno]]'s third-phase video names the **layer above Skills** that handles team deployment:

| Skills layer | Question | Canonical voice |
|---|---|---|
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] Skill Creator |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types) |
| Composition | How do skills chain into automations? | [[simon-scrapes]] (Skill Systems) |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |
| **Deployment / team-scaling** | **How does a team use Skills together?** | **[[brad-bonanno]] (Execution Layer)** |

Key concrete primitives at the deployment layer:

- **Skills wired by reference, not hard-code** — when the brain updates, skills inherit (same shape as the wiki's `[[wikilink]]` over inline citation)
- **Private team marketplace** from Brad's free GitHub template (`github.com/bradautomates/comp...`)
- **Sub-plugins for vertical functions** — sales, ops, customer success — composable bundles of skills per org function
- **PR-back loop** — every correction at the leaf becomes a permanent upgrade across the company: *"the new hire who joined yesterday is running on the back of every lesson your team has ever taught the skill, and the quality lottery is gone"*

The PR-back loop is the **same shape as the wiki's update flow** — corrections propagate upstream. Comparable to `/wiki-ingest` → entity update → index regen.

**Cross-vendor framing** (chapter 4:01): the execution-layer pattern works on [[codex]] and [[hermes-agent]] too — the marketplace + sub-plugin + PR-back primitives are vendor-agnostic at the deployment layer.

→ See [[execution-layer]] for the full framework.

## Composition discipline named — "Skill Systems" ([[simon-scrapes]] #3 in [[youtube-digest-apify-2026-05-06]])

[[simon-scrapes]] introduces the **composition layer** as a named discipline:

- **Mega-skill anti-pattern** — the natural failure mode of "one skill per business process"; skills become bloated, brittle, and resist reuse
- **Skill Systems = modular skills chained** — narrow scope per skill, well-defined I/O, orchestration at a higher layer (slash commands, sub-agents, Routines); skills compose like Unix tools
- **Reuse is the test** — a properly modular skill ("send invoice", "draft email") plugs into 5+ end-to-end automations

This fills the **missing rung** in the Skills discourse:

| Layer | Question | Voices |
|---|---|---|
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] Skill Creator |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types) |
| **Composition** | **How do skills chain into automations?** | **[[simon-scrapes]] (Skill Systems)** |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

Plausible explanation for [[dubibubii]]'s "500K skills, 95% useless" claim: most marketplace skills are mega-skills built without composition discipline. Skill Systems framing predicts a market shift toward components-not-solutions. → See [[skill-systems]].

## Skills as a cross-vendor primitive ([[nate-herk]] #2 in [[youtube-digest-apify-2026-05-06]])

[[nate-herk]]'s 1hr Codex full-course confirms **Skills exist on [[codex]]** (OpenAI's coding-agent CLI) too — the same procedural-knowledge primitive this vault has tracked as Anthropic-canon is now cross-vendor. The 26:44 chapter is "Building Reusable Skills."

Implications:
- The architectural concepts in this page **port** to non-Anthropic substrates
- "Skills" as a name is settling; once two competing CLIs ship the same primitive name, the abstraction is mature
- **Open**: are Codex Skills file-format-compatible with Claude Skills, or just conceptually parallel? Marketplace dynamics depend on the answer.
- **Open**: how does the [[brad-bonanno]] context-bloat optimization translate to Codex's metered API model vs Claude's flat-fee?

This page stays Anthropic-canon-focused; cross-link to [[codex]] for parallel-primitive details.

## Skills positioned in 6-layer agentic-scaffolding taxonomy ([[nate-b-jones]] #11 in [[youtube-digest-apify-2026-05-10]])

[[nate-b-jones]] names a 6-layer map of agentic scaffolding — see [[plugins]] for the full taxonomy. Skills sit at **layer 2**, between prompts (one-offs) and plugins (team-installable workflow bundles).

| Layer | Role | When to use |
|---|---|---|
| 1. Prompts | One-offs, exploration | Repeated workflows? — promote to skill |
| **2. Skills** | **House-style encoded across any LLM** | **Team-shared bundle? — promote to plugin** |
| 3. Plugins | Whole workflows your team can install | Smaller scope? — demote to skill |
| 4. MCPs / connectors | Live access to where work lives | Token-sensitive? — see [[printing-press]] |
| 5. Hooks | Deterministic events the model shouldn't handle | — |
| 6. Scripts | Deterministic logic the model shouldn't handle | — |

This is the **categorical map** above the existing authoring/composition/curation stack. Together:

| Layer | Question | Voices |
|---|---|---|
| **Taxonomy** | **What types of scaffolding exist?** | **[[nate-b-jones]] ([[plugins]])** |
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] Skill Creator |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types) |
| Composition | How do skills chain into automations? | [[simon-scrapes]] ([[skill-systems]]) |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

40% of operators' AI time is wasted putting work in the wrong layer (per [[nate-b-jones]] #11 title) — typically using a skill for what should be a plugin (over-stuffed) or a prompt for what should be a skill (re-tokens every use).

## Skill Creator first-hand walkthrough + two-types eval split ([[chase-ai]] #2 in [[youtube-digest-apify-2026-05-11]])

107K-view canonical first-hand demo of [[skill-creator]] — Anthropic's meta-skill that tests, benchmarks, and optimizes skills using:

- **Plain-language evals** (no test harness scaffolding required)
- **Blind A/B testing** (skilled vs unskilled baseline on same input)
- **Description-field optimization** (iterates invocation-trigger description)

This resolves the **authoring-evaluation gap** the Skills discourse has had structurally since launch — prior to Skill Creator, "is my skill any good?" was vibes-based. Now skills are **testable software**.

### The two-types skill split

[[chase-ai]]'s framework names the eval-target categorization:

| Type | Definition | Eval metric | Example |
|---|---|---|---|
| **Capability uplift** | Adds an ability the model couldn't do well | Task pass rate (skilled vs unskilled) | New domain reasoning template, tool-orchestration pattern |
| **Encoded preference** | Bends the model toward a style/convention it could already approximate | Output distribution match (skilled output looks more like target) | Brand voice, format spec, house style |

This is **the missing eval rung** in the existing stack:

| Layer | Question | Voices |
|---|---|---|
| Taxonomy | What types of scaffolding exist? | [[nate-b-jones]] ([[plugins]]) |
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] authoring guide |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types), [[chase-ai]] (capability vs preference) |
| **Evaluation** | **Does my skill actually work?** | **[[skill-creator]] + [[chase-ai]] two-types split** |
| Composition | How do skills chain into automations? | [[simon-scrapes]] ([[skill-systems]]) |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

For 3Ps client deliverables: every shipped skill should be **labeled with its type at authoring time** — the eval target and acceptance criteria flow from the label. Skill Creator runs become the **acceptance test** for "is the deliverable done?".

→ See [[skill-creator]] for full coverage. Updates: [[anthropic]] (Skill Creator surface), [[claude-code]] (Skill Creator workflow integration).

## Skills as "the unlock" ([[brad-bonanno]] #2 in [[youtube-digest-apify-2026-05-10]])

[[brad-bonanno]]'s 13-product Anthropic tour names Skills as **"the one feature that makes everything else dramatically better the moment you teach Claude how you actually want things done."**

Two voices, two frames, same conclusion:
- **[[ben-ai]]** (229K-view authoring frame): Skills are how you write one thing well
- **[[brad-bonanno]]** (operator frame): Skills are what unlocks the other 11 Anthropic products

For 3Ps client conversations: **Skills are the highest-leverage primitive** in the Claude product surface. If a client uses Claude without Skills, they're at ~2% of the platform's value (per Brad's framing).

## Skill-authoring discipline goes mainstream ([[ben-ai]] #7)

[[ben-ai]]'s *How to build Claude Skills Better than 99% of People* in [[youtube-digest-apify-2026-05-05]] is **229.7K views** — ~14x [[code-with-beto]]'s 16K and ~5x [[nate-herk]] #25's 47K. The highest-view authoring voice is now non-Anthropic, with his own framework competing with Anthropic's official Skill Creator:

- **3 Types of Skills** (chapter at 08:00) — *new framework*; types not yet enumerated
- **Skills vs Plugins** distinction (chapter at 06:20)
- **Planning & Context Engineering** as authoring discipline
- **Skill Building Prompt Framework** — meta-prompt for skill authoring

This puts authoring (not just curation) in mainstream-creator territory. The *Skill Creator vs Ben AI's Prompt Framework* fork is now real; transcript ingest needed to resolve specifics.

## Curation problem and emerging solutions

- **"Best of N skills" videos** are now an established format — implies skill abundance has outpaced user evaluation capacity. Four distinct curation philosophies are visible:
  - **Best-of-N from large sample** — [[nate-herk]] #25 ("6 of 100+ tested"), 47K views
  - **Curated essentials bundle** — [[brock-mesarich]] ("15 I can't live without"), 134.9K views — non-technical audience preference for "tell me what to install" over "here's how I evaluated"
  - **Mixed Skills + MCPs + repos** — [[dubibubii]] ("33 you actually need"), 78.9K views ([[youtube-digest-apify-2026-05-05]] #5) — broader stack-curation, not pure Skills
  - **Daily-driver / frequency-of-use** — [[zinho-automates]] ("9 I use every single day"), 13.6K views ([[youtube-digest-apify-2026-05-12]] #4) — smallest-N, frequency-based selection, "steal them" lower-friction onboarding framing for new users
- **Market-size claim** ([[dubibubii]] #5): *"500,000 skills on the market right now, and 95% are completely useless."* First explicit number for the Skills ecosystem; if accurate, the curation-video format will only get more important.
- **Cross-curator consensus is forming** — Frontend Design + Superpowers + Context7 surface in three+ curation videos ([[nate-herk]] #25, [[brock-mesarich]], [[dubibubii]] #5). A small "must-install" core is emerging that 3Ps and others can use as a baseline client recommendation.
- **Skill marketplaces** are emerging:
  - `claude-plugins-official` (Anthropic-distributed)
  - Community marketplaces (e.g., `mksglu/context-mode`, `thedotmack/claude-mem`)
  - [[brad-bonanno]] is building a verified-skills marketplace (waitlist mentioned in #19, #23)
- **Single-plugin bundle distribution** ([[brock-mesarich]]) — packaging multiple skills as one plugin install; lowers friction for non-technical users vs per-skill installs. Different distribution philosophy from `claude-plugins-official`'s per-skill model.
- **Curation videos as discovery layer** — until marketplace ratings exist, creator curation is the de facto signal

## Anthropic-internal skill inventory ([[ai-labs]] in [[youtube-digest-apify-2026-05-22]])

[[ai-labs]]'s 36K-view *Claude Code's Creator Uses These Claude Skills Every Single Day* (2026-04-03) is the **first canonical "what Anthropic uses internally" coverage** in this vault. Two categories surfaced:

### Anthropic-released open-source plugins (`claude-plugins-official`)

| Plugin | Purpose |
|---|---|
| **Frontend Designer** | Avoids generic aesthetics in UI generation |
| **Code Simplifier** | Refactoring + dead-code elimination |
| **Commit Commands** | Automated commit-message generation |

### Reverse-engineered internal-team skills (behind CLI flags)

| Skill | Purpose | Meta-skill? |
|---|---|---|
| **Verify** | Automated testing harness | Yes |
| **Skillify** | Converts a working session into a reusable skill | Yes |
| **Tech Debt** | End-of-session cleanup of incomplete work | Sort-of |
| **Batch** | Parallelizes migrations across isolated git worktrees | No |
| **Security Scan** | Input-validation / auth / injection-risk checks | No |

The **meta-skill cluster** (Verify + Skillify + Tech Debt) extends the [[skill-creator]] category — meta-skills are now an explicit tracked category in this vault (Skill Creator + Skillify + `/smb-onboard` + [[alex-mcfarland]]'s Plugin Marketplace Builder + [[brad-bonanno]]'s `/create-farmer` are all meta-skill-shape).

The **Security Scan** skill is the build-time complement to [[agent-security]] runtime judge architecture. The **Batch** skill maps onto [[deployment-framework]] Method 1 with worktree isolation as the parallelism primitive.

**Pattern**: AI LABS surfaced "Skillify" before Anthropic released Skill Creator publicly (2026-04-03 vs 2026-05-11) — **community surfaces internal Anthropic skills ~6 weeks before official release**. Useful early-warning signal for upcoming primitives.

## Beginner-tier sub-7-min explainer ([[tristen-obrien]] in [[youtube-digest-apify-2026-05-25]])

[[tristen-obrien]]'s 5.3K-view *Claude Skills Explained Simply (Master in 7 Minutes)* (2026-05-24, 6:59) fills the **sub-7-min beginner-tier explainer rung** below [[anthropic]]'s 201K official explainer, [[chase-ai]]'s 107K Skill Creator walkthrough, and [[ben-ai]]'s 229K authoring video. The four-tier explainer funnel is now mapped:

| Tier | Creator | Audience | Length |
|---|---|---|---|
| Official | [[anthropic]] (201K) | Ecosystem broadly | Long-form |
| Developer walkthrough | [[chase-ai]] (107K Skill Creator) | Developers + skill authors | Tutorial |
| Authoring framework | [[ben-ai]] (229K) | Skill builders | Educational |
| **Sub-7-min beginner** | **[[tristen-obrien]] (5.3K)** | **Non-developer SMB operators** | **Express** |

The **Pizza Shop Catering Quote demo** (chapter 2:52) is the canonical live-built skill for the beginner tier — takes a messy customer email and produces a branded PDF quote (likely using Anthropic's `pdf` skill on the back end) + a ready-to-send reply email. Directly portable to plumbing, HVAC, landscaping, catering, photography — the trade-service vertical set this vault tracks via adjacent skills.

**"Not Every Skill Is Safe"** (chapter 5:09) is the new wrinkle — Tristen flags the **third-party-skill security risk** for non-technical users (*"one security mistake that could put your data at risk"*). This is the **consumer-facing surface** of [[agent-security]] — which to date has been enterprise procurement + LLM-as-judge architecture. Beginner-tier users now have to think about skill provenance, code execution permissions, and data exposure.

→ See [[tristen-obrien]] for full coverage. Updates: [[agent-security]] (consumer-facing skill-provenance dimension).

## Cross-surface confirmation — Chat + Cowork + Claude Code ([[kevin-stratvert]] in [[youtube-digest-apify-2026-05-28]])

[[kevin-stratvert]]'s 9.5K-view *Claude Skills Tutorial (2026): Chat, Cowork, and Claude Code* (2026-05-27, hosted by David DeWinter, sponsored by Intuit/QuickBooks) is the **first vault coverage of the same skill running across all three Claude surfaces** — and it **resolves the standing open question** below: *"Skills are Code-only today; will they work in the Claude.ai chat surface?"* → **yes**. Skills are now confirmed portable on **both axes**: surface (Chat ↔ Cowork ↔ Code, this video) and vendor ([[codex]]).

| Surface | How skills appear | Audience |
|---|---|---|
| **Chat** (`claude.ai`) | Invoked situationally in conversation | Broadest / non-technical |
| **Cowork** (`claude.com/download`) | Run on a local folder with business context | Operators with local files |
| **Claude Code** | Folders on disk in `.claude/skills` | Developers |

Notable details:
- **Built a "Thread Reply" skill from scratch *with test cases that grade the skill before you save it*** — the [[skill-creator]] eval discipline, surfaced for a non-developer audience (same democratization move as [[tristen-obrien]]'s pizza-shop demo, but cross-surface).
- **Four ways to share a skill**, including a **synced shared folder** so a sub-team runs the same skill *without a Team/Enterprise plan* — the lowest-friction team-distribution method tracked (below [[plugin-marketplace]] GitHub-hosting and [[execution-layer]] private marketplaces).
- **Office-productivity-tutorial tier** — first skills coverage from a mainstream business-software channel, reached through a QuickBooks sponsor (same SMB-operator audience as [[claude-for-small-business]]).

This adds a **fifth tier** to the explainer funnel — the office-productivity-tutorial lane — and the **cross-surface** dimension the prior single-surface explainers lacked.

→ See [[kevin-stratvert]] for full coverage.

## Context-extraction front-end — grill-me + Skills ranked #1 of all Claude Code features (2026-06-05)

Two [[nate-herk]] videos in [[youtube-digest-apify-2026-06-05]] reinforce Skills from opposite ends.

**#2 *The Skill That 10x'd My Claude Code Projects* (36.8K views)** ships a free **context-extraction skill** → new concept [[grill-me-skill]]. It inverts the usual direction — *"the skill relentlessly interviews you about a process and writes it back to a knowledge doc"* — and names the real bottleneck in skill quality: *"the hardest part isn't the prompts, it's getting everything out of your head and into the system."* Claim: front-loading context this way gets a skill to **~90% on the first try instead of 30 iterations.** This adds a **front-of-pipeline** rung the Skills stack lacked — *extract context* sits before *author* / *eval* ([[skill-creator]]) / *optimize* ([[self-improving-skills]]). → See [[grill-me-skill]].

**#3 *I Tested Every Claude Code Feature, These 12 Are the Best* (40.3K views)** ranks every [[claude-code]] feature D→S tier from 500+ hours — and **#1 is Skills** (chapter 17:52). This is the **third independent "Skills are the unlock" confirmation** in the vault, joining [[brad-bonanno]]'s "the one feature that makes everything else dramatically better" and [[ben-ai]]'s 229K authoring video. From a creator who tested *every* feature, Skills top the list. → See [[claude-code]] for the full tier-list coverage.

## First-party authoring playbook — Anthropic's *Lessons from building Claude Skills* ([[brock-mesarich]] in [[youtube-digest-apify-2026-06-06]])

[[brock-mesarich]]'s 11.3K-view walkthrough surfaces Anthropic's official article **"Lessons from building Claude Skills"** (`claude.com/blog/lessons-from-...`) → new concept [[skill-authoring-lessons]] — the **first-party authoring discipline** for Skills, the "how to write one well" companion to Anthropic's 201K "what skills are" explainer.

The high-signal points:

- **9 categories of skills** — Anthropic's internal taxonomy of skill *kinds* (more granular than [[ben-ai]]'s "3 Types").
- **The gotchas section is "the highest-signal part of any skill"** — edge cases + failure modes earn the skill's keep more than the happy path. The new canonical authoring rule: **failure modes first**.
- **Write descriptions for the model, not humans** — the `description` field is the invocation lever, written for the model's firing decision. First-party confirmation of what [[chase-ai]] / [[skill-creator]] surfaced via description-field optimization.
- **Progressive disclosure via the file system** — keep the body lean, load supplemental files (good-vs-avoid examples) only when needed. The filesystem *is* the context-management mechanism (this vault's `references/` / `.templates/`).
- **Stop railroading Claude** — don't over-constrain a capable model; give it goal + guardrails, not a step-by-step script (the senior-partner-not-junior-teammate instinct at the skill layer).
- **Start small, iterate** — anti-mega-skill discipline, from Anthropic directly (matches [[skill-systems]]).

This **first-party-validates three patterns** the vault inferred from creators: description-field-as-invocation-lever, progressive-disclosure-via-files, and start-small-not-mega-skill. The explainer funnel now has an **authoring-discipline article at its first-party top**. → See [[skill-authoring-lessons]]. Updates: [[skill-creator]] (description-field + don't-railroad), [[anthropic]].

## Vertical-plugin product instantiation ([[claude-for-small-business]] in [[youtube-digest-apify-2026-05-22]])

[[anthropic]] ships **the first vertical plugin** on 2026-05-21 — [[claude-for-small-business]] bundles ~30 pre-built skills + connectors + the `/smb-onboard` meta-skill. This is the **canonical "skills as packaged product" instantiation** — confirms the [[execution-layer]] / [[plugin-marketplace]] roadmap is shipping as **Anthropic-owned vertical plugins**, not just community marketplaces.

Predictable sibling launches: Claude for Retail, Claude for Healthcare, Claude for Legal.

## Top-rated skills surfaced (per [[nate-herk]] #25)

```
/plugin install skill-creator@claude-plugins-official
/plugin install superpowers@claude-plugins-official
npx get-shit-done-cc --claude --global
/plugin marketplace add mksglu/context-mode
/plugin install context-mode@context-mode
/plugin marketplace add thedotmack/claude-mem
/plugin install claude-mem
/plugin install frontend-design@claude-plugins-official
```
6 highlighted out of 100+ tested. Heuristic appears to be "boring + frequent" — the "simple, boring skills are the ones that actually sell" framing.

## Vertical applications

- **Marketing** ([[grace-leung]] #1) — 5-agent marketing team + 12 skills covering research/write/design/analyze, Notion task board integration, remote control via phone
- **Marketing skill-stack architecture** ([[grace-leung]] #2 in [[youtube-digest-2026-05-03-r3]]) — Brand Voice → Brand Design System → Campaign Planning → Carousel Design → Animated Motion → Campaign Manager Agent. Publishable as a reusable architectural template, not just a tutorial.
- **Knowledge management** ([[brad-bonanno]] #23, this vault) — context farmers + wiki ingest skills
- **Design** ([[design-skills]] — [[griffin-wooldridge]]'s five-skill pipeline: Frontend Design → Implement Design → Theme Factory → Brand Guidelines → Canvas Design, 241K views; plus [[claude-design]] integration)
- **Development** ([[code-with-beto]]'s AI Tattoo App, $100 MRR demo)

## The cross-vendor portability gap + the consumer surface (2026-06-24)

Two [[youtube-digest-apify-2026-06-24]] videos push the Skills story in opposite directions — toward a portability *problem* and toward a wider *surface*:

- **[[open-skills]] ([[nate-b-jones]], his 30th framework, 24.8K views)** names the gap prior coverage hadn't: **Anthropic shipped *surface* portability (Chat/Cowork/Code, per [[kevin-stratvert]]) but skills still don't travel across *vendors*** — Claude Code, [[codex]], and Cursor each trap their own. Jones reframes scattered per-tool prompts as **procedural debt** and argues a **real skill ≠ a clever prompt** (it *verifies* and *composes* — "skills as primitives, runbooks as compositions"). His **Open Skills** project proposes a neutral, portable format. The cross-vendor sharpening of [[nate-herk]]'s `CLAUDE.md`↔`AGENTS.md` 3-layer model: instructions are symmetric; the *skill* layer is where portability breaks. → [[open-skills]].
- **[[justyn-the-ai-guy]] (*How To Install Skills On Claude Desktop*, 99.1K back-catalog views)** confirms Skills have fully crossed onto the **consumer Claude Desktop surface** — *"Skills are a super power, but they're not just for Claude Code users"* — and surfaces the **skills.sh** community directory. A mainstream-tier datapoint that Skills are now non-developer territory.

## Generation-first meta-skill + the "one skill, not a shelf" counter-thesis ([[alek]] in [[youtube-digest-apify-2026-07-01]])

[[alek]]'s *The BEST Claude Skill You've Never Seen Before* (4.3K views, 2026-06-30) pitches **[[skill-forge]]** — a meta-skill framed as *"the only skill you really need"* because it **builds any other skill from a described workflow**. Two things make it worth a hook here:

- **It's the vault's first *generation-first* meta-skill.** The meta-skill cluster ([[skill-creator]] = evaluation, Skillify = session-capture, `/smb-onboard` = vertical customization, `/create-farmer` = domain scaffolding) gains a "describe workflow → get skill" member. Skill Forge scaffolds; [[skill-creator]] proves; [[self-improving-skills]] converges — a clean generate → evaluate → optimize pipeline.
- **It inverts the curation debate.** Every prior curation voice argued *which N to install* ([[brock-mesarich]] 15 / [[dubibubii]] 33 / [[nate-herk]] 6-of-100+ / [[zinho-automates]] 9). Skill Forge argues **stop curating, generate on demand** — the meta-skill *replaces the shelf*. First explicit "one skill, not a library" position tracked here, and a direct answer to [[dubibubii]]'s "500K skills, 95% useless" (don't shop the 500K, forge the one). Open whether it holds — forged skills still need an acceptance test.

Also a **crossover-creator signal**: it reaches the vault via an e-commerce-adjacent channel (boilerplate Etsy/TikTok-shop disclaimer), extending the downmarket drift of [[tristen-obrien]] and [[justyn-the-ai-guy]]. → See [[skill-forge]], [[alek]].

## The design vertical — a five-skill pipeline for designers ([[griffin-wooldridge]] in [[youtube-digest-apify-2026-07-05]])

[[griffin-wooldridge]]'s *How to Use Claude Skills as a Designer* (**241K views**, 2026-03-09) is the **highest-view single-vertical Skills video** tracked in the vault and names a coherent **five-skill design pipeline** → new concept: [[design-skills]]. The five: **Frontend Design** (generate front-end, Anthropic first-party) → **Implement Design** (design → working UI) → **Theme Factory** (systematic theming) → **Brand Guidelines** (enforce brand) → **Canvas Design** (compose on canvas), then *create your own* ([[skill-creator]]).

Why it lands here: it's the **design cell of the Skills audience matrix** — the counterpart to [[grace-leung]]'s marketing vertical — and it's a **pipeline instance, not a curation list** (five focused skills chained, [[skill-systems]]-style, in one domain). Four of the five map onto real installable skills (`frontend-design`, `brand-guidelines`, `canvas-design`, `theme-factory`), grounding it beyond a wishlist. Distinct from [[claude-design]] (the tool vs the skills). → See [[design-skills]].

## Beginner build-from-scratch + skill-safety/provenance ([[skill-leap-ai]] in [[youtube-digest-apify-2026-07-05]])

[[skill-leap-ai]]'s *Ultimate Guide To Claude Skills* (29.5K views, 2026-06-29, 18:03) fills the **beginner build-from-scratch** rung — *"what Claude skills are, where to find them, how to turn them on, and how to build one from scratch with the Claude skill creator"* ([[skill-creator]] as the non-technical on-ramp). Named example skills: writing-style, deep-research auditor, CSV dashboard, content engine, on-brand presentation maker → jobs like scripts, PDF reports, dashboards, blog/LinkedIn posts, slides.

Its distinctive contribution is the **skill-safety / provenance** framing — *"some Claude skills from the internet can be risky, so I build my own and check the instructions before using them."* This is the **second explicit consumer-facing skill-provenance-security voice** in the vault (after [[tristen-obrien]]) — an emerging standing sub-thread as the marketplace fills with unvetted skills, complementary to the builder-side [[agent-security]] framing. → See [[skill-leap-ai]].

## Why it matters for 3Ps

Skills are the canonical artifact for packaging consulting expertise:
- Methodology → skill
- Onboarding flow → skill
- Repeated client deliverable → skill
- Course content → skill bundle

The 3Ps consulting offering should ship skills, not just teach them. **Productization angle**: branded skill library + marketplace listing as paid product.

## Open questions

- **Anthropic's marketplace plans** — official paid marketplace coming, or stays GitHub-distributed indefinitely?
- **Usage / ranking metrics** — no public "most installed skills" data yet; whoever publishes this becomes the de facto curator
- **Skill rot** — as Claude Code APIs evolve, how often do skills break? Lint-style health checks for skill compatibility?
- ~~**Cross-platform skills** — Skills are Code-only today; will they work in Claude.ai chat surface?~~ **Resolved 2026-05-28** ([[kevin-stratvert]]) — the same skill runs across Chat + Cowork + Claude Code. Skills are surface-portable. Open follow-up: does the *same file* run unchanged, or are there per-surface adaptations?

## Related pages

- [[claude-code]] — substrate
- [[codex]] — sibling substrate; Skills now cross-vendor
- [[skill-systems]] — composition layer; the missing rung between authoring and curation
- [[open-skills]] — cross-vendor portability framework; skills don't travel between Claude Code/Codex/Cursor; procedural debt; own portable procedures ([[nate-b-jones]] 2026-06-19)
- [[justyn-the-ai-guy]] — consumer Claude Desktop Skills install tutorial + skills.sh directory (99K back-catalog, 2026-06-24)
- [[mcp]] — sibling primitive; see [[agent-skills-vs-mcp]] (planned comparison)
- [[voice-agents]] — newest application surface; voice-agent skill bundles likely next
- [[anthropic]] — vendor
- [[karpathy-llm-wiki]] — this vault's skills implement this pattern; `karpathy/autoresearch` is a related Karpathy skill surfaced via [[dubibubii]]
- [[context-farming]] — depends on farmer skills
- [[youtube-digest-apify-2026-05-03]], [[youtube-digest-2026-05-03]], [[youtube-digest-2026-05-03-r3]], [[youtube-digest-apify-2026-05-04]], [[youtube-digest-apify-2026-05-05]], [[youtube-digest-apify-2026-05-06]], [[youtube-digest-apify-2026-05-10]], [[youtube-digest-apify-2026-05-11]], [[youtube-digest-apify-2026-05-12]], [[youtube-digest-apify-2026-05-14]], [[youtube-digest-apify-2026-05-22]], [[youtube-digest-apify-2026-05-23]], [[youtube-digest-apify-2026-05-25]], [[youtube-digest-apify-2026-05-28]], [[youtube-digest-apify-2026-06-05]], [[youtube-digest-apify-2026-06-06]], [[sources/youtube-digest-apify-2026-07-05]]
- [[design-skills]] — the design vertical; [[griffin-wooldridge]]'s five-skill pipeline (241K views, 2026-07-05)
- [[griffin-wooldridge]] — designer who named the [[design-skills]] pipeline
- [[skill-leap-ai]] — beginner build-from-scratch guide + skill-safety/provenance framing (2026-07-05)
- [[skill-authoring-lessons]] — Anthropic's first-party authoring playbook; gotchas-section + description-for-the-model + progressive disclosure ([[brock-mesarich]] 2026-06-05)
- [[grill-me-skill]] — context-extraction front-end; "the hardest part is getting it out of your head" ([[nate-herk]] 2026-06-04)
- [[tristen-obrien]] — beginner-tier sub-7-min explainer + pizza-shop catering-quote demo + consumer-facing skill-provenance security
- [[kevin-stratvert]] — cross-surface (Chat/Cowork/Code) tutorial + Thread Reply skill with test cases + synced-shared-folder team distribution
- [[plugins]] — categorical taxonomy layer above Skills (where Skills sit in the broader scaffolding map)
- [[hermes-agent]] — sibling substrate that ships its own Skills primitive
- [[skill-creator]] — evaluation tool / meta-skill
- [[skill-forge]] — generation-first meta-skill + "one skill, not a curated shelf" counter-thesis ([[alek]] 2026-06-30)
- [[alek]] — crossover creator who introduced [[skill-forge]]
- [[execution-layer]] — deployment / team-scaling layer above Skills ([[brad-bonanno]] 2026-05-14)
- Creators: [[code-with-beto]], [[nate-herk]], [[grace-leung]], [[brad-bonanno]], [[anthropic]], [[brock-mesarich]], [[ben-ai]], [[dubibubii]], [[simon-scrapes]], [[nate-b-jones]], [[chase-ai]], [[zinho-automates]], [[tristen-obrien]], [[kevin-stratvert]], [[griffin-wooldridge]], [[skill-leap-ai]]
- [[watch-skill]] — [[brad-bonanno]]'s free `/watch` skill gives [[claude-code]] video comprehension ([[sources/youtube-digest-apify-2026-07-03]])
