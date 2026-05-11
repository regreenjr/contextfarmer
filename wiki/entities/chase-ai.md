---
title: Chase AI
category: entity
summary: AI/Claude Code YouTuber + Skool community operator + consulting agency owner; first-hand walkthrough of Anthropic's Skill Creator (107K views, 2026-03) names the canonical two-types skill split — capability uplift vs encoded preference — that resolves the missing eval framework for [[claude-skills]]
tags: [creator, youtube, claude-code, claude-skills, skill-creator, skool, agency, chase-ai, ai-creator]
sources: 1
updated: 2026-05-11
---

# Chase AI

## What it is

Chase AI is a YouTube channel + Skool community + consulting agency, all under the brand. Three-tier funnel:

- **Free YouTube content** — Claude Code / Claude Skills tutorials and breakdowns
- **`skool.com/chase-ai-community`** — free community with AI resources
- **`skool.com/chase-ai`** — paid Skool: "Master Claude Code, Build Your Agency, Land Your First Client"
- **`chaseai.io`** — paid consulting bookings

The framing is **agency-builder** rather than pure-tutorial — the funnel converts toward "build an AI agency" outcomes vs [[nate-herk]]'s "operate Claude well" or [[brock-mesarich]]'s "make $80K/mo solo" framings.

## Why it matters for this wiki

[[chase-ai]] surfaces in this vault via [[youtube-digest-apify-2026-05-11]] #2 — the **canonical first-hand walkthrough of [[skill-creator]]**. Prior [[claude-skills]] coverage referenced Skill Creator existed ([[code-with-beto]] #6 + [[anthropic]] #4 in [[youtube-digest-apify-2026-05-03]]) but didn't demo it. [[chase-ai]] provides the end-to-end demo + a clean eval-framework synthesis.

The video is **107K views in ~9 weeks** — top-quartile for skill-authoring content (compare [[ben-ai]]'s 229K-view "How to build Claude Skills Better than 99%" and [[anthropic]]'s 201K official explainer).

## Key contributions

### The two-types skill split (from [[youtube-digest-apify-2026-05-11]] #2)

The cleanest **eval framework** for [[claude-skills]] surfaced in this vault. Skills split into two types, each evaluated differently:

| Type | What it does | How it evaluates | Example |
|---|---|---|---|
| **Capability uplift** | Adds an ability the model couldn't do well otherwise | Task pass rate (skilled vs unskilled) | New domain reasoning template, tool-orchestration pattern |
| **Encoded preference** | Bends the model toward a specific style or convention it could already approximate | Output distribution match (skilled output looks more like target than unskilled) | "Write in our brand voice", "format outputs to our spec" |

This is the **missing rung** in the existing [[claude-skills]] eval discourse — prior frames (Ben AI's "3 Types", Anthropic's authoring guide) named categories without specifying eval metrics. Capability vs preference makes the eval metric flow directly from the type.

### Skill Creator walkthrough

First end-to-end demo of Anthropic's [[skill-creator]] in this vault:

- **Evals in plain language** — no test harness scaffolding required
- **Blind A/B testing** — skilled vs unskilled run on same input, output compared blind
- **Description optimization** — Skill Creator iterates the skill's *description field* (used by Claude to decide invocation) to improve invocation accuracy
- **Workflow demo** — build-skill-from-scratch + run-an-eval, on-camera

Resolves the **authoring-evaluation gap** in [[claude-skills]] — prior to Skill Creator, skill authors had no standard way to benchmark their work. Post-Skill-Creator, skills become **testable software**, not prose snippets.

## Distribution & funnel architecture

Three-tier (free → community → paid):

| Tier | Surface | Cost | Outcome |
|---|---|---|---|
| Top | YouTube | Free | Audience build + Anthropic-product awareness |
| Mid | `skool.com/chase-ai-community` | Free | Lead capture + ongoing engagement |
| Paid community | `skool.com/chase-ai` | $$ | "Master Claude Code, Build Your Agency, Land Your First Client" |
| Service | `chaseai.io` | $$$ | Custom consulting / done-for-you work |

Classic AI-creator funnel — same shape as [[nick-saraev]]'s Maker School and [[brad-bonanno]]'s Skills Marketplace waitlist, but **agency-outcome-oriented** vs Saraev's course-outcome framing.

For 3Ps positioning: this is **a direct reference architecture** for the user's potential funnel. The "Land Your First Client" framing is more sales-explicit than the rest of the vault's tracked creators.

## Why track him for 3Ps

1. **Same product surface, more agency-coded framing** — useful comparison data for 3Ps positioning conversations
2. **Canonical [[skill-creator]] reference** — until Anthropic ships a definitive demo, [[chase-ai]] #2 is the canonical resource to cite/share
3. **The two-types eval split is portable** — directly usable as a 3Ps deliverable categorization scheme (every skill ships labeled with its eval target)
4. **Funnel design is studyable** — three-tier with explicit paid path is a clean template

## Open questions

- **Channel size** — exact subscriber count (estimated ~150K from view density, but unverified). Worth a transcript pull on the channel-info chapter if any video covers it.
- **Other content velocity** — is this a high-output channel? The 107K-view skill video suggests algorithmic success but not output cadence.
- **Skool pricing** — paid Skool tier cost not captured; useful market data for 3Ps comparable-pricing research.
- **Agency wins** — "Land Your First Client" framing implies there are documented case studies. Are these public?
- **Other Skill Creator videos** — has [[chase-ai]] done follow-ups on Skill Creator, or was this a one-shot?
- **Why did the farmer miss this for 9 weeks?** Video is 2026-03-04, was 107K views before this batch — the keyword set or channel filter wasn't catching "Chase AI" content. Worth a periodic audit of which top creators the farm is missing.

## Related

- [[claude-skills]] — primary topic; two-types eval framework is the page's missing rung
- [[skill-creator]] — primary tool covered
- [[anthropic]] — vendor of Skill Creator
- [[claude-code]] — substrate
- [[ben-ai]], [[code-with-beto]] — fellow skill-authoring voices (Chase is the third in this tier)
- [[nate-herk]], [[brock-mesarich]] — fellow skill-curator/tutorial voices but with different framings
- [[nick-saraev]] — fellow course/community operator with course-outcome (vs agency-outcome) framing

## Appears in

- [[youtube-digest-apify-2026-05-11]] — *Claude Code Skills Just Got a MASSIVE Upgrade* (#2, 107.3K views) — Skill Creator walkthrough + two-types eval framework
