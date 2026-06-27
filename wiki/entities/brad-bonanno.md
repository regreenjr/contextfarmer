---
title: Brad Bonanno
category: entity
summary: AI & Automation YouTuber; coined/popularized "context farming" pattern that this vault uses; Skills marketplace builder; canonical "OpenClaw is dead, first-party Claude Code wins" voice; in 2026-05 ships the canonical 13-product "Learn Claude From Scratch" tour; in 2026-05-14 ships [[execution-layer]] (Phase 3); **in 2026-05-21 ships Phase 4** — first-creator-walkthrough coverage of [[anthropic]]'s newly-launched [[claude-for-small-business]] vertical plugin (~30 pre-built skills + connectors for QuickBooks/Xero/Stripe/HubSpot/Gmail + `/smb-onboard` meta-skill); his four-video trajectory sequence: context-farming (Phase 1) → 13-product tour (Phase 2) → execution layer (Phase 3) → **Anthropic-shipped vertical plugin coverage (Phase 4)**; CFSB likely preempts his own skills-marketplace roadmap but he covers it favorably — Brad continues to be the canonical creator-side commentator on Anthropic product launches
tags: [creator, youtube, claude-code, context-farming, second-brain, skills-marketplace, telegram, scheduled-tasks, auto-memory, claude-product-tour, execution-layer, sub-plugins, pr-back-loop, team-scaling, cross-vendor, claude-for-small-business, smb-onboard, anthropic-vertical-plugins, phase-4, mcp-connectors, content-ideas-skill, creator-growth, outlier-rating, comment-mining, anti-cannibalization, scrape-creators, for-you-page, event-driven-routines, cloud-routine, cal-com, make-com, sally, pre-call-research, apify, firecrawl, webhook, anticipation-gap]
sources: 8
updated: 2026-06-27
---

# Brad Bonanno

## What it is
Person + YouTube channel **Brad | AI & Automation**. Builder of the "AI Second Brain" / "Company Brain" / "context farming" pattern that this vault directly implements via the [[context-farming]] skill (`farmer/` configs in this repo).

## Why it matters for this wiki
**The user's vault uses Brad's pattern.** The `farmer` skill, the per-source farmer markdown configs, the auto-ingest into raw/ → wiki are direct instantiations of his Slack/Fireflies-fed Obsidian second brain. Tracking him = tracking the upstream evolution of the architecture this vault runs on.

## Key videos in [[youtube-digest-apify-2026-05-03]]

- #19 *I Stopped Hitting Claude Code Usage Limits (Here's How)* — 106K views, 2026-04-10. Releases free **Context Audit skill** that scans Claude Code setup, scores token bloat, recommends cuts. Canonical fix: replace MCP servers with CLIs, optimize CLAUDE.md, cut skill bloat, tune settings.json.
- #23 *I Turned My Second Brain Into a Company Brain (Now it reads Slack for me)* — 2.4K views (early), 2026-04-01. Shows full context-farming setup: Slack MCP + Fireflies + Obsidian + scheduled Claude Code routines. Includes a `/create-farmer` skill that builds and schedules new farmers automatically. **Free GitHub repo at `bradautomates/second...`** (truncated in source).

## Key video in [[youtube-digest-apify-2026-05-10]]

- #2 *How I'd Learn Claude From Scratch in 2026* — 3.5K views (early), 2026-05-07, 11:29. **Canonical 13-product tour** of Anthropic's surface area — the most comprehensive product inventory in this vault. Walks every product end-to-end:
  1. Claude Chat + artifacts
  2. Connectors + MCP (Gmail, Drive, Notion, Calendar, Slack)
  3. Projects (work organization)
  4. Claude Desktop + Cowork + Live Artifacts (local file read/edit)
  5. **Skills** ("the one feature that makes everything else dramatically better")
  6. Dispatch (mobile-to-desktop handoff)
  7. Word add-in
  8. PowerPoint add-in
  9. Excel add-in
  10. Chrome (browser automation)
  11. Design ([[claude-design]])
  12. Code ([[claude-code]] — "the most powerful version of all of it")
  13. Routines (scheduled recurring work)
- **Thesis**: paying users use ~2% of what Claude exposes. Most never touch Skills, Connectors, Cowork, Routines.
- **Skills as the unlock** — same framing [[ben-ai]] uses; Brad confirms it from the operator side, [[ben-ai]] from the authoring side
- **Skills Marketplace waitlist** at `brad-b.kit.com/f9a7349a1c` — same waitlist Brad has been driving since the earlier #19/#23 videos; he's been at it for months
- Useful as the **canonical Anthropic product surface inventory** for this vault — supplements the [[anthropic]] entity page

## Key video in [[youtube-digest-2026-05-03-r3]]

- #4 *These 3 Claude Code Features Just Killed OpenClaw (Setup Guide)* — 1.4K views (early), 2026-03-25, 20:48. Architecturally important — names three first-party Anthropic features that obsolete the OpenClaude open-source Telegram-Claude bridge:
  1. **Claude Code Channels** — first-party Telegram bot, no exposed ports / leaked API keys / sketchy OSS code on the host machine
  2. **Scheduled Tasks** — cron jobs via the `/loop` command (this vault uses it for farm scheduling — see `farmers/`)
  3. **Auto Memory** — persistent context across sessions (this vault uses it via `~/.claude/projects/.../memory/`, baked into root CLAUDE.md)
- Full setup demoed end-to-end: Telegram message → Claude reads files → runs SEO workflow → sends report attachments back → schedules cron jobs. **No VPS, no Docker, no third-party wrappers.**
- **Telegram-tuned Claude.md** — shorter mobile-friendly responses, progress-update prompts so user is "never left on read", auto memory checks before every task, guardrails around `--dangerously-skip-permissions`. Free download: `brad-b.kit.com/be466ba5df`
- AI Strategy Call funnel: `cal.com/bradley-bonanno/ai-st...`

## Key video in [[youtube-digest-apify-2026-05-14]]

- #1 *Build an Execution Layer for Your Second Brain (Step by Step)* — 56 views (just-published), 2026-05-14, 7:27. **Phase 3** of his product trajectory: names what comes after the second brain. → New concept: [[execution-layer]].

**Core thesis**: "A second brain for your business isn't enough." Context on its own doesn't ship the work. The execution layer takes the brain's context and runs real playbooks/SOPs over it to return *finished work*.

**Concrete primitives**:

1. **Wire Skills by reference, not hard-code** — when the brain updates, skills inherit ("referencing beats hard-coding")
2. **Private team marketplace from free GitHub template** — `github.com/bradautomates/comp...` (truncated); "spin up in under five minutes"
3. **One-command skill addition** — "Add your existing skills with one command"
4. **Sub-plugins for vertical functions** — sales, ops, customer success as separate sub-plugins as the team grows
5. **PR-back loop** — every correction becomes a permanent upgrade across the whole company → "the new hire who joined yesterday is running on the back of every lesson your team has ever taught the skill"

**Cross-vendor framing** (chapter 4:01 *Why This Works Across Every AI Tool*) — same shape as [[codex]] / [[hermes-agent]] substrate-symmetry but at the marketplace layer. The IP is portable.

**Skills Marketplace waitlist** (`brad-b.kit.com/f9a7349a1c`) now promoted in **three videos in five weeks** — same waitlist, three positioning angles. Suggests near-term launch.

## Key video in [[youtube-digest-apify-2026-05-22]]

- #7 *Why You Need Claude for Small Business* — 831 views (just-published), 2026-05-21, 6:52. **Phase 4** of his product trajectory: first-creator-walkthrough coverage of [[anthropic]]'s newly-shipped vertical plugin → New concept: [[claude-for-small-business]].

**The Anthropic launch**: [[claude-for-small-business]] is the **first Anthropic-shipped vertical plugin** — installed directly into the Claude desktop app, pre-wired with:

- **Connectors** ([[mcp]] servers) for QuickBooks / Xero / Stripe / PayPal / Square / HubSpot / Gmail
- **~30 pre-built skills** (Monday brief / call list / plan payroll / close month / handle complaint / run campaign / Friday brief / quarterly review / CRM maintenance / invoice chase + 20 more)
- **`/smb-onboard` meta-skill** — customizes every skill to the user's business / industry / headcount / tools (skill-creator-shape)

**Brad's framing**: install in under 3 minutes; `/smb-onboard` rewrites skills; connector flexibility (swap Xero for QuickBooks etc); live demos of Monday brief synthesizing financials+deals+calendar + call list ranking top 5 leads + CRM maintenance logging meetings to HubSpot + invoice chase skipping paid customers.

**Distribution funnel**:
- **Small Business Skills Guide** lead magnet (`brad-b.kit.com/bb4f80fd45`)
- **AI Strategy Call** (`cal.com/bradley-bonanno/ai-st...`)

**Strategic significance**:

1. **Competitive coexistence positioning** — CFSB likely **preempts Brad's own skills-marketplace waitlist** (which he's been promoting across Phases 1-3), but Brad covers it favorably and retains his role as the **execution-layer educator**. The marketplace waitlist's strategic value compresses; the educational/training value extends
2. **Phase 4 = creator covering Anthropic-shipped products** — Brad's role evolves from "build your own skills marketplace" (Phase 3) to "use Anthropic's pre-built skills marketplace" (Phase 4). The creator-side response to verticalization is **packaging the Anthropic product** + selling tuning/customization services
3. **`/smb-onboard` as meta-skill** validates the [[execution-layer]] PR-back-loop thesis at Anthropic scale — Anthropic builds the customization-by-onboarding meta-skill; community-side ([[brad-bonanno]] / [[alex-mcfarland]]) ships the corrections-back-as-permanent-upgrades pattern around it
4. **Cumulative four-phase trajectory** confirms Brad as the **highest-priority creator-watch** for vault architecture evolution

## Key video in [[youtube-digest-apify-2026-06-03]]

- #1 *I Hit 10k Subs in 3 Months with Claude Code (steal this)* — 174 views (just-published), 2026-06-03, 8:20. **The creator-growth axis** of his product trajectory: a free Claude skill (`/content-ideas`) he credits with growing his channel **0 → 10K subs in 3 months including three 90K+ view videos**. → New concept: [[content-ideas-skill]].

**The skill** (free, `github.com/bradautomates/cont...`; runs in [[claude-code]], Claude Chat, Cursor, Codex):

1. **Custom "For You page"** across YouTube/IG/X/TikTok — only highest-performing posts from tracked creators
2. **Outlier rating** — scores posts by how far they beat *that creator's own average*, not absolute views (size-normalized)
3. **Comment mining** (2:19) — reads comments on every post to find angles the post didn't cover ("the real edge")
4. **Anti-cannibalization** (3:13) — scrapes your own channel each run so it never repeats your back-catalog
5. **Auto-memory taste layer** — 👍/👎 trains it to sound like you, not "an AI trend report"

Data via **Scrape Creators** (`scrapecreators.com`); funnel to AI Strategy Call (`cal.com/bradley-bonanno/ai-st...`).

**Strategic significance**:

1. **A new axis, not a Phase-5 of the business-execution arc** — Phases 1-4 were business architecture (context farming → product tour → execution layer → CFSB). `/content-ideas` is **creator-growth tooling** — the same skill-author and free-lead-magnet playbook applied to his *own* channel growth. The skill *is* the lead magnet.
2. **A content-ideation farmer** — same supply-chain shape as [[context-farming]] (scheduled external-context pulls), but the destination is a ranked idea list, not a wiki. Confirms Brad keeps shipping farming-shaped skills.
3. **Self-improvement via encoded preference** — auto-memory thumbs-tuning is the *subjective-taste* cousin of [[self-improving-skills]]' *objective* binary-criteria loop.
4. **Outlier rating is a portable primitive** — "beat the creator's own average" is a cleaner content-selection signal than absolute views; worth porting into the vault's YouTube farmer.

## Key videos in [[youtube-digest-apify-2026-06-24]]

**Two videos — both [[ai-operating-system]] coverage from his operator-not-coder angle:**

- #8 *Claude Code RUNS My Business (13 WORKFLOWS)* — 1,551 views, 2026-06-22, 13:53. He runs his **entire business out of [[claude-code]]** across **13 workflows** spanning the full funnel — *"finding customers, marketing to them, closing them, delivering the work that gets them to stay, and the leverage layer that underpins all of it."* The pitch: *"a whole team's worth of work without hiring anyone."* Free guide with the exact build steps (`brad-b.kit.com`). The **breadth-tour of his own AIOS** — the operator's-eye companion to [[nate-herk]]'s framework-driven [[ai-operating-system]] (Four C's) and the execution-layer payoff of his own Phases 1-4. The 13 named workflows are gated to the guide.

- #10 *The AI Setup I Use to Run EVERYTHING (in one app)* — 13,018 views, 2026-06-12, 7:28. *"I love Claude, but the desktop app is slow, throws errors, locks you in a sandbox, and won't even let you edit the files you're working on. I haven't opened it in months."* He runs his whole workday out of **VS Code** with three pieces: **Claude + Codex in the side panel** (the extension, not terminal or chat — clean UI, multiple sessions, model switching, long-running tasks), the **working file open in the middle for live co-editing** *"without burning tokens on tiny changes,"* and his **whole OS folder on the left** (content, research, sales, custom skills, the rules that tell it who you are). PDFs/Word/Excel/PPTX/images/markdown render natively. **The VS-Code-as-AIOS-shell pattern** — a concrete editor-choice for the [[ai-operating-system]] he and [[nate-herk]] both teach, and a notable break from the Claude desktop app.

**Strategic significance**: both videos are **execution-layer-in-practice** — not new architecture, but Brad showing his own working AIOS (13 funnel workflows + the VS Code shell that hosts them). #10's "I quit the Claude desktop app" stance is a pointed product critique and the clearest editor-substrate recommendation in the vault's AIOS coverage; #8's funnel-complete workflow set is the breadth-tour to [[nate-herk]]'s framework depth-tour. → Updates: [[ai-operating-system]] (13-workflow breadth + VS Code shell), [[claude-code]], [[codex]].

## Key video in [[youtube-digest-apify-2026-06-27]]

- #2 *I Automated Pre-Call Research with Claude Code (FULL BUILD)* — 249 views (just-published), 2026-06-26, 49:08. An **unedited live build** ("bugs and all") that takes the operator **completely out of the loop** → New concept: [[event-driven-routines]].

**The problem**: for months Brad ran a sales-research skill **by hand** on every booked call — *"I have to remember to type slash research every single time, and on a busy morning I forget."* The build fires the research **the instant a booking is made** so notes land on the calendar invite before he opens his laptop. The concrete operator-side close of [[nate-b-jones]]' [[anticipation-gap]] (the agent knows *when* to act because an event tells it).

**The agent ("Sally")** pulls the prospect's LinkedIn, work history, company size, recent news, open roles, and buying signals via:
- **Apify** — LinkedIn scraping + Google search
- **Firecrawl** — website + web search
- **Google Drive MCP** ([[mcp]]) — writes a private research doc
- **Google Calendar MCP** ([[mcp]]) — attaches the doc to the invite

**The load-bearing architecture decision**: *why a local routine isn't event-based enough, and when to reach for a Claude cloud routine vs a managed agent.* The trigger chain is `cal.com webhook → make.com (enriches the booking) → Claude cloud routine`. He lets Claude configure the cloud routine straight from the **Git-tracked AIOS repo** and sets **least-access permissions** on it.

**Strategic significance**: the **event-driven** complement to his prior AIOS coverage. Phases 1-4 + the 06-24 13-workflow/VS-Code instantiation showed a *manually-invoked* operator system; this is the first time he wires a workflow to **fire on an external event** rather than a slash command or a cron. The vault's farmers are **cron-scheduled** ([[context-farming]]); Brad's `webhook → middleware → cloud routine` chain is the **missing event-trigger primitive**. Skill download: `brad-b.kit.com/0b31eb2b33`. → New concept: [[event-driven-routines]]. Updates: [[ai-operating-system]] (cadence/connections made event-driven), [[claude-code]] (cloud routines + event triggers), [[mcp]], [[anticipation-gap]].

## The four-phase product trajectory

| Phase | Video | Concept | Vault implementation |
|---|---|---|---|
| **1** | [[youtube-digest-apify-2026-05-03]] #23 (*Company Brain*) | [[context-farming]] | `farmers/`, `/wiki-ingest`, raw/ → wiki/ |
| **2** | [[youtube-digest-apify-2026-05-10]] #2 (*Learn Claude From Scratch*) | 13-product surface tour (Anthropic inventory) | (Reference inventory in [[anthropic]] page) |
| **3** | [[youtube-digest-apify-2026-05-14]] #1 (*Execution Layer*) | [[execution-layer]] | **Not yet implemented** — productization layer above the vault |
| **4** | [[youtube-digest-apify-2026-05-22]] #7 (*Why You Need Claude for Small Business*) | [[claude-for-small-business]] | **Anthropic-shipped vertical plugin** — Brad covers Anthropic's product launch from the execution-layer educator role |

Brad has been incrementally describing the same product across these four videos. Phase 4 represents the **creator-side response to Anthropic verticalization** — package the Anthropic product + sell tuning/customization services on top.

## Pattern artifacts to harvest

1. **Context Audit skill** (free download, video #19) — worth installing and running on this vault
2. **`/create-farmer` skill** (video #23) — directly comparable to the user's existing `farmer` skill
3. **Skills marketplace waitlist** — `brad-b.kit.com/f9a7349a1c` — he's building a verified-skills marketplace; competitive/complementary product to study
4. **Full second-brain repo** at `github.com/bradautomates/seco...` — likely worth cloning and diffing against this vault's `farmer/` skill
5. **Telegram-tuned Claude.md** (free, video #4) — `brad-b.kit.com/be466ba5df` — diff against the user's `/telegram` skill setup for ergonomics improvements
6. **Execution-layer free template** (video #1 in 2026-05-14) — `github.com/bradautomates/comp...` — clone and diff against the vault's farmer + skills setup. Likely names sub-plugin scaffolding patterns the vault hasn't formalized.

## Architecture co-evolution

Brad's three videos surfaced so far (#19, #23, #4) collectively describe the **architecture this vault runs on**:

| Brad video | Concept | Vault implementation |
|---|---|---|
| #19 (Context Audit) | Token-cost optimization | (TODO: install Context Audit skill) |
| #23 (Company Brain) | [[context-farming]] | `farmers/`, `/wiki-ingest`, scheduled routines |
| #4 (OpenClaw is dead) | Telegram + `/loop` + Auto Memory | `/telegram` skill, `/loop`, `~/.claude/projects/.../memory/` |
| 2026-05-10 #2 (13-product tour) | Anthropic surface inventory | Reference doc in [[anthropic]] page |
| 2026-05-14 #1 (Execution Layer) | [[execution-layer]] | **Not yet implemented** — productization gap |

This makes him the **highest-priority creator-watch** for vault architecture evolution. New Brad videos likely → new vault primitives.

## Related
- [[context-farming]] — the canonical concept page (Phase 1)
- [[event-driven-routines]] — his event-triggered pre-call research build (2026-06-27); the event-trigger complement to cron-scheduled context-farming
- [[content-ideas-skill]] — his free content-ideation skill (creator-growth axis, 2026-06-03)
- [[self-improving-skills]] — `/content-ideas`' auto-memory tuning is the preference-side cousin
- [[execution-layer]] — his Phase 3 concept (productization above the brain)
- [[karpathy-llm-wiki]] — the architecture his pattern implements
- [[claude-code]] — substrate
- [[claude-skills]] — packaging unit
- [[skill-systems]] — composition discipline ([[simon-scrapes]]) that pairs with execution-layer at the workflow level
- [[mcp]] — his pattern depends on MCP for Slack/Fireflies access
- [[codex]], [[hermes-agent]] — cross-vendor parity per video #1's chapter 4:01

## Appears in
- [[youtube-digest-apify-2026-05-03]] — 2 high-signal videos (#19, #23)
- [[youtube-digest-2026-05-03-r3]] — video #4 (OpenClaw-killer features)
- [[youtube-digest-apify-2026-05-10]] — video #2 (Learn Claude From Scratch 13-product tour)
- [[youtube-digest-apify-2026-05-14]] — video #1 (Execution Layer — Phase 3)
- [[youtube-digest-apify-2026-05-22]] — video #7 (*Why You Need Claude for Small Business* — Phase 4)
- [[youtube-digest-apify-2026-06-03]] — video #1 (*I Hit 10k Subs in 3 Months* — `/content-ideas` skill, creator-growth axis)
- [[youtube-digest-apify-2026-06-24]] — videos #8 (*Claude Code RUNS My Business — 13 WORKFLOWS*) + #10 (*The AI Setup I Use to Run EVERYTHING* — VS Code as AIOS shell)
- [[youtube-digest-apify-2026-06-27]] — video #2 (*I Automated Pre-Call Research with Claude Code* — event-driven cloud routine, "Sally" pre-call research → [[event-driven-routines]])
- [[context-farming]] — primary citation
- [[claude-code]] — primary citation for Channels / Scheduled Tasks / Auto Memory features
- [[anthropic]] — most comprehensive product-surface tour
- [[execution-layer]] — primary author

## Why track him for 3Ps
- **Direct architectural influence** on this vault — anything he ships likely belongs here
- **Skills marketplace** is a strategic move worth watching; could become competitor or partner for any 3Ps skill product
- **His audience** = practitioners adopting context-farming patterns; same persona as 3Ps target customer

## Open questions
- What does his Skills marketplace actually offer? (Join waitlist for visibility)
- Is the `/create-farmer` skill open-source? Worth diffing against the user's existing implementation
- His business model — newsletter + AI strategy calls (`cal.com/bradley-bonanno/ai-st...`) — what's he selling?
- Cross-platform presence — X handle?
