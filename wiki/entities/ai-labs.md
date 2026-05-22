---
title: AI LABS
category: entity
summary: Mid-tier AI YouTube channel (36K-view canonical video) + `ailabspro.io` community + `ailabs.services` sponsorship arm; first creator in this vault to publish a focused **"what Anthropic actually uses internally"** reverse-engineering — dug through Anthropic team posts + open-source repos + leaked source code references to surface internal Claude Code skills (Verify, Skillify, Tech Debt, Batch, Security Scan) behind CLI flags that aren't publicly published; complements [[chase-ai]] (Skill Creator first-hand walkthrough) and [[brad-bonanno]] (13-product breadth tour) as the **internal-skill-inventory voice** in the 2026-Q2 Claude ecosystem coverage trio
tags: [creator, youtube, ai-labs, claude-skills, anthropic-internal, reverse-engineering, skills-curation, ailabspro, meta-skills, verify, skillify, tech-debt, batch, security-scan, frontend-designer, code-simplifier, commit-commands]
sources: 1
updated: 2026-05-22
---

# AI LABS

## What it is

YouTube channel **AI LABS** + community at `ailabspro.io` + sponsorship arm at `ailabs.services`. Content focus: curation + reverse-engineering of Claude Code skills, with a deliberate "what the Anthropic team actually uses" angle.

## Why it matters for this wiki

**Their canonical video is the first "internal Anthropic skill inventory" coverage** tracked in this vault. The Claude ecosystem has plenty of "best 100 skills" curation content ([[brock-mesarich]], [[dubibubii]], [[nate-herk]] #25) and one canonical first-hand Skill Creator walkthrough ([[chase-ai]]). AI LABS occupies a third position: **reverse-engineering what Anthropic devs run on themselves**.

## Key video in [[youtube-digest-apify-2026-05-22]]

- **#1** *Claude Code's Creator Uses These Claude Skills Every Single Day* — 36.3K views, 2026-04-03, 12:17

**Source methodology** (their own framing): *"We dug through the Anthropic team's posts, open source repos, and the official plugin marketplace to pull out every skill and slash command the creators of Claude Code actually use. This video breaks down what is Claude Skills, how to add skills to Claude, and walks through the best Claude Skills available right now, plus internal ones you've never seen before."*

## Two categories surfaced

### Anthropic-released open-source plugins (in `claude-plugins-official`)

| Plugin | Purpose | GitHub link |
|---|---|---|
| **Frontend Designer Plugin** | Avoids generic aesthetics in UI generation; opinionated design-system enforcement | `github.com/anthropics/claude-...` |
| **Code Simplifier** | Refactoring + dead-code elimination | `github.com/anthropics/claude-...` |
| **Commit Commands** | Automated commit-message generation following conventional-commit format | `github.com/anthropics/claude-...` |

All three are **publicly published** by Anthropic in their `claude-plugins-official` GitHub org. They form the **Anthropic-blessed default skill kit** for new Claude Code installs.

### Reverse-engineered internal-team skills (behind CLI flags, not publicly published)

| Skill | What it does | Meta-skill shape? |
|---|---|---|
| **Verify** | Automated testing harness — runs tests against a skill or session output | Yes — operates on other skills |
| **Skillify** | Converts a working session into a reusable skill | Yes — produces skill artifacts |
| **Tech Debt** | End-of-session cleanup of incomplete work — pulls TODO/FIXME items, reconciles partial implementations | Sort-of — operates on session state |
| **Batch** | Parallelizes migrations across isolated git worktrees | No — operates on code, not skills |
| **Security Scan** | Input-validation / auth / injection-risk vulnerability checks | No — operates on code |

**The meta-skill cluster** (Verify + Skillify + Tech Debt) extends the [[skill-creator]] category. Combined with [[alex-mcfarland]]'s "Plugin Marketplace Builder Skill" and Anthropic's own [[skill-creator]] (2026-05-11), this is now a **tracked category** — skills that operate on other artifacts (other skills, sessions, marketplaces).

**The Security Scan skill** is the agent-side build-time complement to [[agent-security]]'s runtime judge-architecture pattern. Same vulnerability classes ([[nate-b-jones]]' McKinsey Lilly example) tackled from the **build/CI** side rather than the **runtime/action-boundary** side.

**The Batch skill** maps onto [[deployment-framework]] Method 1 (`/loop` in-session) with **worktree isolation** as the parallelism primitive. Different from Modal/Trigger.dev (Method 3) — same parallelism goal but local rather than serverless.

## Distribution / monetization

- **YouTube** — `AI LABS` channel
- **ailabspro.io** — community + "Video code: V53" suggests there's an indexed video archive
- **ailabs.services** — sponsorship inquiries arm
- **No paid Skool / no obvious lead magnet** in this specific video description — funnel appears to be community-first, sponsorship-monetized

## Strategic significance

1. **First "internal Anthropic skill inventory" voice** in this vault — fills a gap between curation (best-of lists) and authoring (how to build skills). The "what Anthropic devs actually use" angle is **its own content category**.
2. **Confirms internal-vs-public skill split** at Anthropic — there's an unpublished tier of skills the team uses internally. Pattern is the same as Skill Creator's pre-release period (Anthropic used it for months before publishing in 2026-05-11).
3. **The reverse-engineered skills are 3Ps-deliverable candidates** — Verify + Skillify + Tech Debt + Security Scan are all generally applicable. 3Ps could build sanctioned versions of each as part of a client engagement.
4. **Meta-skills are now an explicit category** — Skill Creator + Skillify + Verify + Plugin Marketplace Builder + `/create-farmer` ([[brad-bonanno]]) all operate on other skills/sessions/artifacts. The category needs its own concept page in a future digest.
5. **2026-04-03 publish date predates the canonical Skill Creator release** — AI LABS surfaced "Skillify" (the same idea) **before** Anthropic publicly released Skill Creator on 2026-05-11. Pattern: **community surfaces internal Anthropic skills before official release** — useful early-warning signal for upcoming Anthropic primitives.

## Related

- [[claude-skills]] — primary topic
- [[claude-code]] — substrate
- [[skill-creator]] — public Anthropic version of Skillify
- [[agent-security]] — Security Scan is the build-time complement
- [[deployment-framework]] — Batch maps onto Method 1 worktree parallelism
- [[chase-ai]] — Skill Creator first-hand walkthrough; complementary "first-hand insider" voice
- [[brad-bonanno]] — 13-product breadth tour; complementary "comprehensive surface" voice
- [[brock-mesarich]], [[dubibubii]], [[nate-herk]] — curation-tier voices (vs AI LABS' reverse-engineering tier)
- [[plugin-marketplace]] — Anthropic's `claude-plugins-official` is the upstream distribution channel for the released plugins

## Appears in

- [[youtube-digest-apify-2026-05-22]] — primary source

## Why track them for 3Ps

- **Early-warning signal** for Anthropic-internal skills that will eventually go public — Skillify predicted Skill Creator by ~6 weeks
- **Internal-skill-inventory content angle** for 3Ps marketing — different from "best of" curation
- **Their `ailabspro.io` community** is a competitive benchmark for any 3Ps community product
- **Their reverse-engineering methodology** (posts + repos + leaked source) is the same research pattern 3Ps clients will eventually pay for

## Open questions

- **Are the reverse-engineered internal skills installable** by community-tier users, or just documented?
- **Channel sub count + cadence** — is this a single-creator channel or a team?
- **ailabspro.io membership model** — free / paid / hybrid?
- **Are there more reverse-engineered skills** beyond the 5 surfaced here? (Their "V53" video code suggests at least 52 prior videos worth of content)
- **Cross-platform presence** — X / LinkedIn / newsletter?
