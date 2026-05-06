---
title: Simon Scrapes
category: entity
summary: AI-automation YouTuber; coined/popularized the "Skill Systems" framework — modular, focused Claude Skills chained into end-to-end automations as the alternative to "mega-skill" bloat; Skool community at skool.com/scrapes
tags: [creator, youtube, claude-code, claude-skills, skill-systems, ai-automation, skool]
sources: 1
updated: 2026-05-06
---

# Simon Scrapes

## What it is

YouTube channel **Simon Scrapes** — focuses on building agentic systems on [[claude-code]] for business automation. Distinguishing format: short (10-15min) videos that name a specific anti-pattern + frame the architectural fix. Distribution: paid Skool community at `skool.com/scrapes` ("Build agentic systems that run your business").

## Why it matters for this wiki

He's the **composition voice** in the [[claude-skills]] discourse. The category had two existing strata — *authoring* ([[code-with-beto]], [[ben-ai]], [[anthropic]] Skill Creator) and *curation* ([[nate-herk]], [[brock-mesarich]], [[dubibubii]]) — but no one had named **composition** as its own discipline. Simon Scrapes' **Skill Systems** framework fills that gap.

For a 3Ps vault tracking how consulting IP gets packaged, the composition layer is the high-leverage one: it's where reusable client deliverables actually live.

## Key claims (from [[youtube-digest-apify-2026-05-06]] #3, *THIS Gives Claude Skills a Massive Upgrade*)

- **Most downloaded skills are built for a single task** — but real work is a sequence of connected processes
- **Mega-skill anti-pattern** — the natural reaction to single-task skills is building one giant skill that does everything; this is bloated, brittle, and resists reuse
- **Skill Systems = modular skills chained** — keep each skill narrow, well-defined I/O; orchestrate at a higher layer; skills compose like Unix tools
- **Reusability is the payoff** — a properly modular skill ("send invoice", "draft email") plugs into 5+ end-to-end automations across the business
- **Real business problems need composition** — single-skill solutions hit a ceiling; the framework is for "agentic systems that run your business," not toy demos

→ See [[skill-systems]]

## Recent activity tracked

- [[youtube-digest-apify-2026-05-06]] #3 *THIS Gives Claude Skills a Massive Upgrade (It's Easy!)* (30.5K views, 2026-04-30, 12:56)

Single video so far in the vault. Notable that the video is from April 30 but only just slipped past dedup — implying he's not in the daily cycle of the highest-output creators yet, but the topic-quality is high.

## Distribution channels

- YouTube (primary): @simonscrapes
- Skool community: `skool.com/scrapes` — paid, "build agentic systems that run your business"
- Hashtags used: `#claudecodeskills #claudecodetutorial #claudecode` — Claude-Code-specific, not OpenAI/general

## Why track him for 3Ps

1. **Skill Systems framework is directly portable** into 3Ps client architecture — every consulting deliverable should be a Skill System, not a mega-skill. Naming and documenting this discipline is a 3Ps content angle.
2. **Composition layer is underserved** — the curation videos and the authoring videos both exist; the composition videos are early. First-mover content potential.
3. **Skool format suggests target audience** is the same operator persona as [[mark-kashef]] / [[nick-saraev]] / [[nate-herk]] — direct competitive set.

## Recommended actions

- [ ] Watch the full 12:56 video and pull the concrete Skill System example (likely a 2-4 skill chain for one business process)
- [ ] Check Skool community size, pricing, content slate as benchmark for 3Ps community pricing
- [ ] Diff his "Skill System" examples against the user's `farmer/` + wiki + skills setup — likely the user's vault already implements this pattern (farmer skill → wiki-ingest skill → query/lint skills) and could be the reference example

## Open questions

- What does a concrete Skill System look like in his framing? (Need transcript or watch-through)
- How does he distinguish a Skill System from a sub-agent orchestration? Is the boundary "shared context vs dispatched specialist"?
- Skool community size + pricing tier?
- Does he cover composition for non-Claude substrates (Codex, n8n)? Or is this Claude-Code-specific?
- Any cross-creator collaboration with the curation tier ([[nate-herk]], [[brock-mesarich]], [[dubibubii]])?

## Related

- [[skill-systems]] — concept he originated/popularized
- [[claude-skills]] — parent concept; Simon Scrapes occupies the composition stratum
- [[claude-code]] — substrate
- [[code-with-beto]], [[ben-ai]] — adjacent voices in the authoring stratum
- [[nate-herk]], [[brock-mesarich]], [[dubibubii]] — adjacent voices in the curation stratum
- [[ai-consulting]] — Skill Systems is the natural artifact for productizing consulting deliverables

## Appears in

- [[youtube-digest-apify-2026-05-06]] — first appearance; #3 introduces Skill Systems framework
