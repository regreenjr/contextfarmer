---
title: Claude Skills
category: concept
summary: Reusable procedural-knowledge units in Claude Code; the canonical packaging unit of 2026's AI-creator economy; in 2026-05-22 batch ships TWO Anthropic-shipped artifacts that change the category: (1) **[[ai-labs]] reverse-engineers the internal Anthropic skill stack** — Anthropic-released public plugins (Frontend Designer / Code Simplifier / Commit Commands) + internal team skills behind CLI flags (Verify / Skillify / Tech Debt / Batch / Security Scan); and (2) **[[anthropic]] ships [[claude-for-small-business]]** — first vertical-plugin product with ~30 pre-built skills + connectors + `/smb-onboard` meta-skill; cumulative skills-product evolution: authoring → curation → composition ([[skill-systems]]) → deployment ([[execution-layer]]) → distribution ([[plugin-marketplace]]) → meta-skills ([[skill-creator]] / Skillify / `/smb-onboard`) → vertical-plugin ([[claude-for-small-business]])
tags: [claude-skills, claude-code, agentic, anthropic, skills-marketplace, skill-authoring, skill-systems, composition, cross-vendor, codex, plugins, hermes-agent, skill-creator, evals, capability-uplift, encoded-preference, daily-driver-curation, execution-layer, sub-plugins, pr-back-loop, team-deployment, anthropic-internal-skills, verify, skillify, tech-debt, batch, security-scan, frontend-designer, code-simplifier, commit-commands, claude-for-small-business, smb-onboard, vertical-plugin, meta-skills, ai-labs]
sources: 11
updated: 2026-05-22
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
- **Design** ([[claude-design]] integration via skills)
- **Development** ([[code-with-beto]]'s AI Tattoo App, $100 MRR demo)

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
- **Cross-platform skills** — Skills are Code-only today; will they work in Claude.ai chat surface?

## Related pages

- [[claude-code]] — substrate
- [[codex]] — sibling substrate; Skills now cross-vendor
- [[skill-systems]] — composition layer; the missing rung between authoring and curation
- [[mcp]] — sibling primitive; see [[agent-skills-vs-mcp]] (planned comparison)
- [[voice-agents]] — newest application surface; voice-agent skill bundles likely next
- [[anthropic]] — vendor
- [[karpathy-llm-wiki]] — this vault's skills implement this pattern; `karpathy/autoresearch` is a related Karpathy skill surfaced via [[dubibubii]]
- [[context-farming]] — depends on farmer skills
- [[youtube-digest-apify-2026-05-03]], [[youtube-digest-2026-05-03]], [[youtube-digest-2026-05-03-r3]], [[youtube-digest-apify-2026-05-04]], [[youtube-digest-apify-2026-05-05]], [[youtube-digest-apify-2026-05-06]], [[youtube-digest-apify-2026-05-10]], [[youtube-digest-apify-2026-05-11]], [[youtube-digest-apify-2026-05-12]], [[youtube-digest-apify-2026-05-14]]
- [[plugins]] — categorical taxonomy layer above Skills (where Skills sit in the broader scaffolding map)
- [[hermes-agent]] — sibling substrate that ships its own Skills primitive
- [[skill-creator]] — evaluation tool / meta-skill
- [[execution-layer]] — deployment / team-scaling layer above Skills ([[brad-bonanno]] 2026-05-14)
- Creators: [[code-with-beto]], [[nate-herk]], [[grace-leung]], [[brad-bonanno]], [[anthropic]], [[brock-mesarich]], [[ben-ai]], [[dubibubii]], [[simon-scrapes]], [[nate-b-jones]], [[chase-ai]], [[zinho-automates]]
