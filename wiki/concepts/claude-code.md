---
title: Claude Code
category: concept
summary: Anthropic's CLI/agent tool; April 2026 "Claude Code 2.0" landed; primary substrate for Skills, MCP, sub-agents, Routines, hooks, Channels (Telegram), Scheduled Tasks, Auto Memory; canonical AI-creator topic of 2026; Saraev's 4hr course (1.56M views) is the flagship educational reference; in 2026-05 Codex (OpenAI) confirmed as parallel substrate with overlapping primitives
tags: [claude-code, anthropic, agentic, cli, claude-skills, mcp, routines, telegram, scheduled-tasks, auto-memory, voice-agents, antigravity, codex, cross-vendor]
sources: 6
updated: 2026-05-06
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

## Patterns added in [[youtube-digest-2026-05-03-r3]]

- **First-party obsoleting wrapper-OSS** ([[brad-bonanno]] #4) — Channels + Scheduled Tasks + Auto Memory replace the OpenClaude open-source Telegram bridge. Pattern: Anthropic ships first-party features ~6 months after a hot OSS wrapper appears, and the OSS goes dormant. Implications for skill builders — anything you build on top of unstable OSS gets obsoleted; build on Anthropic primitives or accept rewrite cost.
- **Mobile-first Claude.md** ([[brad-bonanno]] #4) — short responses, progress updates, auto-memory checks, permission guardrails. Codifies a "phone audience" prompt-engineering style different from desktop Claude Code.
- **Skill-stack architectural templates** ([[grace-leung]] #2 in r3) — vertical skill libraries (Brand Voice → Brand Design System → Campaign Planning → Carousel Design → Animated Motion → Campaign Manager Agent) are publishable as architectural templates, not just demos
- **PhD-research framing** ([[tommy-chryst]] #1 in r3) — Claude Code-hosted [[karpathy-llm-wiki]] is now positioned as a "ChatGPT deep research alternative" by sub-15K-view creators

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
- [[youtube-digest-apify-2026-05-03]], [[youtube-digest-2026-05-03]], [[youtube-digest-2026-05-03-r3]], [[youtube-digest-apify-2026-05-04]], [[youtube-digest-apify-2026-05-05]], [[youtube-digest-apify-2026-05-06]] — primary source digests
- Creators: [[nate-herk]], [[brad-bonanno]], [[code-with-beto]], [[grace-leung]], [[jack-roberts]], [[greg-isenberg]], [[nate-b-jones]], [[andrej-karpathy]], [[tommy-chryst]], [[brock-mesarich]], [[nick-saraev]], [[ben-ai]], [[dubibubii]], [[simon-scrapes]]
