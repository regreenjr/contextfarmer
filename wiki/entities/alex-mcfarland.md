---
title: Alex McFarland
category: entity
summary: Mid-tier AI YouTuber (3.2K views on the plugin-marketplace video) + Substack operator; first creator in this vault to ship a focused **private Claude plugin marketplace build walkthrough** — the GitHub-hosted distribution layer that sits between [[claude-skills]] (units) and [[execution-layer]] (team deployment); covers marketplace.json + plugin folder structure + skill grouping + public-vs-private GitHub setup + one-command install across team/devices; his "Plugin Marketplace Builder Skill" is a [[skill-creator]]-shape meta-skill (a skill that builds the marketplace from your existing skill folder); audience: solopreneurs running Claude across multiple machines, team leads, freelancers building skill libraries for clients
tags: [creator, youtube, substack, claude-code, claude-skills, plugin-marketplace, cowork, meta-skill, distribution-layer, builder-skill, ai-consulting]
sources: 1
updated: 2026-05-16
---

# Alex McFarland

## What it is

Person + YouTube channel **Alex McFarland**. Substack newsletter at `alexmcfarland.substack.com`. Tier-3 AI creator (~3.2K views on his plugin-marketplace video, 2026-03-16 publish). His content angle is **build-pattern walkthroughs for Claude Code productization** — particularly the marketplace and distribution layers.

## Why he matters for this wiki

He ships the **first focused build-walkthrough for a private Claude plugin marketplace** tracked in this vault. The pattern he walks through is the **distribution-layer primitive** missing from prior vault coverage:

- [[claude-skills]] = unit of capability
- [[skill-systems]] = composition of units into workflows ([[simon-scrapes]])
- [[plugins]] = scaffolding-layer taxonomy ([[nate-b-jones]])
- **[[plugin-marketplace]] = GitHub-hosted distribution of plugins to a team or across machines (Alex McFarland — THIS PAGE)**
- [[execution-layer]] = team-operational deployment of the marketplace ([[brad-bonanno]])

His marketplace pattern is the **first concrete artifact-level walkthrough** for what [[brad-bonanno]]'s [[execution-layer]] describes architecturally. Brad and Alex describe the same primitive from two angles:

| Angle | Author | What it gives |
|---|---|---|
| **Build walkthrough** | [[alex-mcfarland]] (this page) | The concrete file structure, builder-skill, GitHub setup steps |
| **Deployment pattern** | [[brad-bonanno]] [[execution-layer]] | The architectural role + sub-plugins + PR-back loop + cross-vendor framing |

Alex's video predates Brad's by 2 months (2026-03-16 vs 2026-05-14) — possibly he was implementing what Brad later formalized.

## Key video in [[youtube-digest-apify-2026-05-16]]

- #3 *You Need a Private Claude Plugin Marketplace (Cowork)* — 3.2K views, 2026-03-16, 25:47

**The marketplace artifact** he walks through:

| Component | Purpose |
|---|---|
| `marketplace.json` | Manifest declaring the marketplace's plugins |
| `plugins/` directory | Each plugin is a folder grouping related skills |
| `skills/` inside each plugin | The actual skill units ([[claude-skills]]) |
| GitHub-hosted repo (public OR private) | One-command install across team/devices |
| **Plugin Marketplace Builder Skill** | The skill that *builds* the marketplace from your existing skill folder |

**The build flow** (chapters 7:00-12:00):

1. Install the Plugin Marketplace Builder Skill (free download from his Substack)
2. Open Claude Code in your skills folder
3. Launch the builder — it reads existing skills, asks for grouping decisions, generates marketplace structure
4. GitHub setup — accounts, authentication, first-timer onboarding (chapter 9:30)
5. Skill grouping and plugin organization (chapter 10:30)
6. Name the repo; pick public vs private (chapter 12:00)
7. Install on any other machine via one command

**Cowork as consumption surface** (chapter 6:15) — despite the video title's "Cowork" tag, the build happens in **Claude Code**. Cowork is where the marketplace gets installed *to* (consumption); Claude Code is where the marketplace is *built* (construction). Same construction/consumption separation pattern Anthropic ships across its product surface.

## Audience positioning

From his description (emphasis added):

> "This is for **solopreneurs running Claude across multiple machines**, **team leads managing shared workflows**, **freelancers building skill libraries for clients**, and **anyone who wants a professional plugin system without touching code**."

Four distinct user segments:

| Segment | Use case | 3Ps relevance |
|---|---|---|
| Solopreneurs multi-machine | Sync skills across desktop/laptop/cloud | Direct match (vault user case) |
| Team leads | Shared team workflows | Direct match (3Ps client case) |
| **Freelancers building for clients** | **Skill library as deliverable** | **Highest match — canonical 3Ps deliverable** |
| Non-developer team leads | Professional plugin system without code | Beginner-tier extension |

The third segment — *freelancers building skill libraries for clients* — is **the canonical 3Ps consulting deliverable shape**. Alex names it explicitly.

## "Without touching code" positioning

Sits in the [[ai-consulting]] audience-tier ladder between:

- [[nicole-mccain]] (pre-revenue beginners, no business, no tech)
- **[[alex-mcfarland]] (team-lead-with-Claude-Code-account band, no-code marketplace)**
- [[brock-mesarich]] (15-skill plugin curator for non-techies)
- [[brad-bonanno]] (operator-level execution layer)
- [[nate-herk]] (developer-deep AIOS courses)

Alex's audience tier is **non-developer team-leads with Claude Code accounts** — the tier above pre-revenue beginners but below operator-level developers. This was previously an under-tracked tier in the vault's [[ai-consulting]] map.

## Distribution channels

- **YouTube** — Alex McFarland channel
- **Substack** — `alexmcfarland.substack.com` (primary funnel)
- **Free download** — Plugin Marketplace Builder Skill (gated to Substack signup, per video description block)
- **No paid product surfaced** in this video — appears to be a lead-magnet-into-newsletter funnel

## Meta-skill pattern

His **Plugin Marketplace Builder Skill** is a [[skill-creator]]-shape meta-skill — *a skill that builds other artifacts*. Same architectural shape as:

- Anthropic's [[skill-creator]] (skills that test skills)
- [[brad-bonanno]]'s `/create-farmer` (skills that create farms)
- Anthropic's CLAUDE.md generator (skills that bootstrap project schemas)

**Meta-skills are themselves becoming a tracked category** — at least four canonical examples now exist in the vault. This is worth a future synthesis page on **builder skills as a primitive category**.

## Why track him for 3Ps

1. **First plugin-marketplace build walkthrough** — fills the distribution-layer gap between skill authoring and team deployment
2. **Direct artifact-level walkthrough** — Brad's [[execution-layer]] gives the architecture; Alex gives the steps to build it
3. **Free builder skill** — worth downloading and diffing against [[brad-bonanno]]'s execution-layer template (likely overlap; possibly direct cross-pollination)
4. **Audience tier** — team-lead non-developer band that 3Ps may want to address with simpler engagements

## Recommended actions

- [ ] Sign up for `alexmcfarland.substack.com` and download the Plugin Marketplace Builder Skill
- [ ] Diff Alex's marketplace.json schema against [[brad-bonanno]]'s execution-layer template
- [ ] Inspect any public marketplaces he's shipped (chapter 3:45 mentions "Alex McFarland Plugins" — likely on GitHub)
- [ ] Test the build flow against the vault's existing `farmers/` and skill folders to see if the builder works on this corpus

## Open questions

- What does the marketplace.json schema actually contain? (Open issue: is there an Anthropic-blessed spec, or is this a creator-defined convention?)
- Does Alex have a paid product? Newsletter monetization is a known funnel pattern
- How does his audience overlap with [[brad-bonanno]]'s? Both target similar use cases but Alex predates Brad's execution-layer naming by 2 months
- Did Brad reference Alex's pattern in the execution-layer video, or did they converge independently?
- Skool/Discord/community presence?

## Related

- [[plugin-marketplace]] — primary concept he ships
- [[execution-layer]] — [[brad-bonanno]]'s deployment-pattern counterpart
- [[claude-skills]] — units distributed via marketplace
- [[plugins]] — taxonomy layer the marketplace distributes
- [[skill-creator]] — sibling meta-skill pattern (skill that builds other things)
- [[claude-code]] — construction surface for the marketplace
- [[ai-consulting]] — productization target ("freelancers building for clients" audience segment)
- [[brad-bonanno]] — closest creator analog (Brad's execution-layer = Alex's marketplace + sub-plugin scaffolding)
- [[brock-mesarich]] — sibling non-developer-tier creator

## Appears in

- [[youtube-digest-apify-2026-05-16]] — primary citation (video #3, plugin marketplace walkthrough)
- [[plugin-marketplace]] — primary author of the concept
