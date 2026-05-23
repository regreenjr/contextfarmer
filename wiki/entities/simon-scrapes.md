---
title: Simon Scrapes
category: entity
summary: AI-automation YouTuber; coined/popularized the **[[skill-systems]]** framework — modular, focused Claude Skills chained into end-to-end automations as the alternative to "mega-skill" bloat; in 2026-05-23 batch his second framework **[[self-improving-skills]]** (109.7K views — vault's highest-views Claude-Skills-eval video, exceeds [[chase-ai]]'s 107K Skill Creator walkthrough) — Karpathy-autoresearch-inspired autonomous overnight loop that tests / scores / refines skills via **binary criteria**, the **closed-loop optimization extension** of [[skill-creator]]; **graduates from mid-tier to mainstream-creator territory** with this video; Skool community at `skool.com/scrapes`; **framework pair** ([[skill-systems]] composition + [[self-improving-skills]] optimization) makes Simon a durable claude-skills-tier voice across two disciplines
tags: [creator, youtube, claude-code, claude-skills, skill-systems, self-improving-skills, ai-automation, skool, karpathy-autoresearch, autonomous-loop, binary-criteria, closed-loop-optimization, eval-loop, overnight-improvement, mainstream-creator]
sources: 2
updated: 2026-05-23
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

- [[youtube-digest-apify-2026-05-06]] #3 *THIS Gives Claude Skills a Massive Upgrade (It's Easy!)* (30.5K views, 2026-04-30, 12:56) — [[skill-systems]] framework
- [[youtube-digest-apify-2026-05-23]] #3 *Build Self-Improving Claude Code Skills. The Results Are Crazy.* (**109.7K views**, 2026-03-13, 11:02) — [[self-improving-skills]] framework (Karpathy-autoresearch-inspired autonomous loop + binary criteria + overnight convergence)

**Tier graduation**: prior video was mid-tier (30.5K); 2026-05-23 video crosses mainstream-creator territory at 109.7K (exceeds [[chase-ai]]'s 107K Skill Creator first-hand walkthrough). The [[skill-systems]] + [[self-improving-skills]] framework pair is now a **durable IP foundation** for his channel.

## New in [[youtube-digest-apify-2026-05-23]]

### #3 [[self-improving-skills]] — autonomous overnight loop (his 2nd framework)

His **closed-loop optimization extension** of [[skill-creator]]. Where Skill Creator runs a single-shot acceptance test (plain-language evals + blind A/B), self-improving skills runs an **autonomous overnight loop** that converges the skill against **binary criteria**.

**The framing claim**: *"What if your Claude Code skills could improve themselves overnight while you sleep?"*

**The loop pattern**:
1. Run skill against test inputs
2. Score against binary criteria (pass/fail per criterion)
3. If failures: generate skill revision
4. Run revised skill against same tests
5. Compare scores
6. Keep revision if improved; discard if worse
7. Repeat until convergence

**Binary criteria as the unlock** — pass/fail bypasses subjective quality judgments. The criterion list becomes the skill's contract. Same shape as [[ai-question-method]]'s Principle 2 (*ask what good looks like*) operationalized at the skill-eval tier.

**The Karpathy lineage** — Simon's pattern explicitly references **[[andrej-karpathy]]'s `autoresearch` concept**. Video published 2026-03-13 (pre-Karpathy-Anthropic-hire) — the pattern was Karpathy-inspired *external creator content* at publish time; post-hire (2026-05-19) it's about-to-be-first-party Anthropic architecture.

**Where it fits in the [[claude-skills]] eval stack**:

| Tool | Loop shape | Time horizon |
|---|---|---|
| Hand authoring | Manual eval, manual revision | Minutes per cycle |
| [[skill-creator]] | Single-shot A/B eval | One run |
| **[[self-improving-skills]] (this)** | **Autonomous loop with binary criteria** | **Overnight — N iterations** |
| Future (predicted) | Skill marketplace with auto-improvement | Continuous |

**Strategic significance**:

1. **109.7K views — highest-views Claude-Skills-eval video in vault** (exceeds [[chase-ai]] 107K). Confirms closed-loop framing has stronger mainstream pull than single-shot eval.
2. **Sister framework to [[project-room-workflow]]** ([[nate-b-jones]] in same batch) — both target "before-the-work artifact" patterns. Simon's binary criteria + Nate's missing-context list both encode success criteria explicitly before the agent runs.
3. **Confirms [[karpathy-llm-wiki]] / autoresearch lineage as Claude-Code-compatible** — predates Karpathy-Anthropic hire by 2 months but the pattern survives the transition.
4. **Closes the [[claude-skills]] optimization gap** — every shipped skill can now be eval-converged before going to marketplace.
5. **Confirms the "automate" lever in [[capital-allocation-framework]]** — skill optimization itself can be automated once you can describe the binary criteria.

→ New concept: [[self-improving-skills]]. Major updates: [[skill-creator]] (closed-loop extension), [[karpathy-llm-wiki]] (autoresearch lineage), [[claude-skills]] (new eval-tier voice).

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
- [[self-improving-skills]] — concept he originated/popularized (2nd framework)
- [[skill-creator]] — single-shot eval; self-improving-skills is the closed-loop extension
- [[claude-skills]] — parent concept; Simon Scrapes now occupies both composition + evals strata
- [[claude-code]] — substrate
- [[code-with-beto]], [[ben-ai]] — adjacent voices in the authoring stratum
- [[nate-herk]], [[brock-mesarich]], [[dubibubii]] — adjacent voices in the curation stratum
- [[ai-consulting]] — Skill Systems is the natural artifact for productizing consulting deliverables
- [[karpathy-llm-wiki]] — self-improving-skills inherits the autoresearch lineage
- [[andrej-karpathy]] — autoresearch author; self-improving-skills is the skill-tier instantiation
- [[chase-ai]] — fellow evals-tier voice ([[skill-creator]] walkthrough)
- [[project-room-workflow]] — sister "before-the-work artifact" framework from [[nate-b-jones]] in same batch
- [[ai-question-method]] — Principle 2 ("ask what good looks like") is the human practice this operationalizes
- [[capital-allocation-framework]] — "automate" lever at the skill-eval tier
- [[anthropic]] — post-Karpathy-hire, autoresearch becomes first-party-future

## Appears in

- [[youtube-digest-apify-2026-05-06]] — first appearance; #3 introduces Skill Systems framework
- [[youtube-digest-apify-2026-05-23]] — second appearance; #3 introduces Self-Improving Skills framework (109.7K views, tier graduation)
