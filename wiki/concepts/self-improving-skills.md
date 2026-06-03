---
title: Self-Improving Claude Code Skills (Autonomous Loop)
category: concept
summary: [[simon-scrapes]]'s 109.7K-view 2026-03-13 framework (vault entry-point #2 for Simon) — Karpathy-autoresearch-inspired **autonomous overnight loop** that tests, scores, and refines Claude Code skills based on **binary criteria**, ensuring skills get more reliable with every iteration; the **closed-loop optimization extension** of [[skill-creator]] (which runs a single-shot acceptance test) — together they form the complete authoring → evals → optimization pipeline; positioned as the **skill-tier instantiation of [[andrej-karpathy]]'s `autoresearch`** primitive (now [[anthropic]]-internal after his 2026-05-19 hire); binary criteria as the unlock (pass/fail bypasses subjective quality judgments — same shape as [[ai-question-method]]' "ask what good looks like" Principle 2); highest-views Claude-Skills-eval video in the vault (exceeds [[chase-ai]]'s 107K Skill Creator walkthrough); confirms the closed-loop framing has stronger mainstream pull than single-shot evaluation
tags: [self-improving-skills, skill-creator, skill-evals, karpathy-autoresearch, claude-skills, claude-code, autonomous-loop, binary-criteria, overnight-improvement, closed-loop-optimization, eval-loop, ab-test, convergence, simon-scrapes, skill-systems, capability-uplift, encoded-preference, anthropic-internal, autoresearch-lineage, content-ideas-skill, auto-memory, preference-tuning, brad-bonanno]
sources: 2
updated: 2026-06-03
---

# Self-Improving Claude Code Skills

## What it is

An **autonomous overnight loop** that tests, scores, and refines [[claude-code]] skills based on **binary criteria** — pass/fail per criterion — so skills get more reliable with every iteration without human-in-the-loop. The pattern takes inspiration from [[andrej-karpathy]]'s `autoresearch` concept and applies it specifically to the [[claude-skills]] tier.

Source: [[simon-scrapes]] *Build Self-Improving Claude Code Skills. The Results Are Crazy.* (109.7K views, 2026-03-13, 11:02), surfaced via [[youtube-digest-apify-2026-05-23]].

## The framing claim

*"What if your Claude Code skills could improve themselves overnight while you sleep?"*

The default skill-author workflow is **manual**: write skill → run skill → eyeball output → revise → repeat. The default Skill Creator workflow is **single-shot**: run plain-language eval + blind A/B once. Self-improving skills replace both with an **autonomous loop**: write skill + binary criteria → loop runs overnight → converged version in the morning.

## The autonomous loop

The canonical pattern:

```
1. Run skill against test inputs
2. Score against binary criteria (pass/fail per criterion)
3. If failures exist: generate skill revision
4. Run revised skill against same test inputs
5. Compare new score vs old score
6. Keep revision if improved; discard if same/worse
7. Repeat until convergence (or budget exhausted)
```

The loop is **convergent**, not greedy — it only accepts revisions that improve the score, so it can't degrade beyond the starting state.

## Binary criteria as the unlock

**Pass/fail per criterion** is the architectural unlock that makes the loop work:

- Subjective quality ("is this good?") can't be scored consistently — the loop diverges or randomly walks
- Binary criteria ("does the output include X?" "is the output under Y tokens?" "does the format match Z?") **can be scored deterministically**
- The criterion list becomes the **skill's contract** — what the skill is *supposed* to produce
- The loop optimizes for **contract satisfaction**, not vague quality

Same shape as [[ai-question-method]]'s Principle 2 (*ask what good looks like*) — but operationalized at the **skill-eval tier**. Where [[ai-question-method]] is a *human* practice (specify success criteria before generation), self-improving skills is the *machine* practice (encode success criteria as binary checks, run the loop).

## The Karpathy lineage

Simon's pattern explicitly references **[[andrej-karpathy]]'s `autoresearch` concept**. The lineage:

| Artifact | What it is | Tier |
|---|---|---|
| **`karpathy/autoresearch`** | Open-ended research-agent skill (gist + repo) | Research workflows |
| **Self-improving skills (this)** | Bounded skill-tier improvement with binary scoring | Skill authoring |
| **`/goal` (predicted)** | [[nate-herk]] 2026-05-19 framed autoresearch as `/goal`-loop ancestor | Long-running agents |

Simon published this video on **2026-03-13 — pre-Karpathy-Anthropic-hire (2026-05-19)**. The pattern was Karpathy-inspired *external creator content* at publish time; post-hire it's **about-to-be-first-party Anthropic architecture** (per [[karpathy-llm-wiki]]).

The 109.7K-view audience reach **predates the hire** — meaning the autoresearch-style autonomous-loop framing has mainstream pull *independent of* the Anthropic momentum. The hire only amplifies it.

## Where it fits in the [[claude-skills]] eval stack

Updated stack:

| Layer | Voice / tool | Loop shape |
|---|---|---|
| Authoring | [[code-with-beto]] / [[ben-ai]] | None — manual write |
| Authoring framework | [[ben-ai]] (3 Types) / [[chase-ai]] (capability vs preference) | None — taxonomy |
| Acceptance test | [[skill-creator]] | **Single-shot eval** — plain-language criteria + blind A/B |
| **Closed-loop optimization** | **[[self-improving-skills]] (this)** | **Autonomous loop** — binary criteria + N iterations |
| Composition | [[simon-scrapes]] ([[skill-systems]]) | None — chaining |
| Curation | [[nate-herk]] / [[brock-mesarich]] / [[dubibubii]] | None — selection |

The vault now has a **complete pre-ship pipeline**:
1. Author the skill (Ben/Beto guidance)
2. Type the skill (Ben/Chase's capability-vs-preference label)
3. Run acceptance test ([[skill-creator]])
4. Run closed-loop optimization (this — until convergence)
5. Compose into Skill System ([[skill-systems]])
6. Curate / ship

Each layer adds a discipline. Self-improving skills closes the last optimization gap.

## Comparison with [[skill-creator]]

| | [[skill-creator]] | [[self-improving-skills]] |
|---|---|---|
| **Loop shape** | Single run | Convergent autonomous loop |
| **Eval format** | Plain-language criteria + blind A/B | Binary criteria (pass/fail per criterion) |
| **Output** | Pass/fail signal | Improved skill |
| **Time horizon** | One run | Overnight / N iterations |
| **Human in loop** | Author writes criteria + reviews result | Author writes criteria; loop runs unsupervised |
| **Use case** | "Does my skill work?" | "Can my skill be made to work better?" |

The two are **complementary, not redundant**. Skill Creator is the acceptance test; self-improving skills is the optimization loop. The full pipeline runs **Skill Creator first** (verify the skill changes behavior in the right direction at all), then **self-improving skills** (converge it to as-good-as-it-can-get given the criteria).

## Comparison with hand-tuning

| | Manual revision | Self-improving skills |
|---|---|---|
| Time cost per iteration | 5-30 min (author thinking + rewriting) | seconds (LLM-generated revision) |
| Iterations per night | 0-1 (humans sleep) | N (loop runs while you sleep) |
| Quality at convergence | Plateaus at author's skill ceiling | Plateaus at frontier model's revision ceiling |
| Cost | Author time | Token cost per iteration |
| Failure mode | Author drift / fatigue | Token budget exhaustion / criterion bug |

The trade-off: **token cost for time cost**. For high-frequency skills, the math is overwhelmingly in favor of the autonomous loop.

## Strategic implications

### For [[claude-skills]]
- **Closes the optimization gap** — every shipped skill can now be eval-converged before going to marketplace
- Pairs with [[skill-creator]] to form the canonical pre-ship pipeline
- Confirms **closed-loop optimization** as a 2026 skill-author standard, not an advanced technique
- The 109.7K-view audience reach signals this has crossed mainstream-creator territory — operators now *expect* skills to be eval-converged

### For [[anthropic]] (post-Karpathy hire)
- Autoresearch + autoresearch-style loops are about to be **Anthropic-internal architecture** per [[karpathy-llm-wiki]]
- Simon's instantiation is the **community-side template** for what Anthropic ships internally
- Suggests [[claude-for-small-business]]'s `/smb-onboard` and other meta-skills will likely include **closed-loop optimization** as a built-in tier, not an optional extension

### For [[ai-consulting]] and 3Ps
- **Self-improving skills become a deliverable** — clients receive *converged* skills, not first-draft skills
- The criterion list is **the consulting artifact** — defining "what good looks like" before convergence is where domain expertise lives
- Pairs with [[ai-operating-system-offer]] — the AI OS Offer can include "we'll set up your skills to self-improve overnight" as a premium tier
- Differentiation lever: most consultants ship hand-tuned skills; eval-converged skills are observably better

### For [[capital-allocation-framework]]
- Self-improving skills is **what "automate" looks like at the skill-author tier**
- The capital-allocation lever choice (automate vs build vs buy vs hire vs wait) applies recursively — the *skill optimization process* itself can be automated, but only if you can describe the binary criteria
- Confirms the [[capital-allocation-framework]] thesis: *do not automate what you cannot describe*; binary criteria *is* the description

## The second self-improvement mechanism: preference-tuning via auto-memory

In 2026-06-03, [[brad-bonanno]]'s [[content-ideas-skill]] (`/content-ideas`) surfaces a **second, distinct** way a skill can self-improve — not a binary-criteria overnight loop, but **encoded preference via Claude auto-memory**: every 👍/👎 the user leaves trains the skill so its output "starts to sound like you, not like an AI trend report." The two mechanisms are complementary halves of skill self-improvement:

| | [[self-improving-skills]] (Simon Scrapes) | [[content-ideas-skill]] auto-memory (Brad Bonanno) |
|---|---|---|
| Signal | Binary criteria (pass/fail, **objective**) | 👍/👎 in auto-memory (**subjective taste**) |
| Loop | Autonomous overnight convergence | Per-run, human-in-the-loop ratings |
| Optimizes for | Contract satisfaction | The user's personal taste |
| "What good looks like" | Specified up front as code | Learned incrementally from feedback |
| Best for | Skills with describable success criteria | Skills where quality *is* subjective (ideation, voice, style) |

The binary-criteria loop is the right tool when you *can* describe success; preference-tuning is the fallback when quality is irreducibly subjective — exactly the case [[capital-allocation-framework]] warns about (*"do not automate what you cannot describe"*). Auto-memory preference is how you self-improve a skill whose output you can't fully specify in advance.

## Open questions

- **Token budget per iteration** — the video probably names a working range; transcript would resolve
- **Criterion bug failure mode** — what happens when a criterion is mis-specified? Does the loop optimize for the wrong thing silently?
- **Cross-skill optimization** — can the loop optimize a *Skill System* (multiple chained skills), or only individual skills?
- **Description-field optimization** — does the loop also optimize the skill's `description:` field (Skill Creator's signature feature), or only the skill body?
- **Convergence detection** — when does the loop stop? Fixed budget? Plateau detection? Time-bound?
- **Comparison with frontier model revisions** — does using Opus 4.7 vs Sonnet 4.6 vs Haiku for the revision-generation step change convergence speed / quality?
- **Pairs with [[project-room-workflow]]** — Simon's binary criteria + Nate's missing-context list are both pre-prompt-artifact disciplines. Is there a unified "what goes into the canvas before the loop / prompt runs" framework? (Both videos shipped 2026-05-22)
- **Skool community pricing** — is this taught in `skool.com/scrapes` ("Build agentic systems that run your business")?

## Strategic significance

1. **First "self-healing skill" coverage in vault** — extends [[skill-creator]] from *acceptance testing* to *iterative optimization*
2. **Highest-views Claude-Skills-eval video in vault** (109.7K, exceeds [[chase-ai]]'s 107K) — confirms closed-loop framing has stronger pull than single-shot eval
3. **Confirms [[karpathy-llm-wiki]] / autoresearch lineage as Claude-Code-compatible** — predates Karpathy-Anthropic hire by 2 months but the pattern survives the transition
4. **Sister framework to [[project-room-workflow]]** (Nate B Jones in same batch) — both target "what an AI agent needs *before* doing the work" (criteria for Simon, canvas for Nate)
5. **Simon Scrapes' 2nd video and tier-graduation** — prior video was 30.5K (mid-tier); this video at 109.7K crosses into mainstream-creator territory; [[skill-systems]] + [[self-improving-skills]] form a durable framework pair
6. **Confirms the "automate" lever in [[capital-allocation-framework]]** — skill optimization itself can be automated once you can describe the binary criteria

## Related pages

- [[simon-scrapes]] — creator
- [[skill-creator]] — single-shot acceptance test; this extends with closed-loop optimization
- [[claude-skills]] — parent concept; this is the evals/optimization tier
- [[claude-code]] — substrate
- [[karpathy-llm-wiki]] — Karpathy lineage; autoresearch is the parent primitive
- [[andrej-karpathy]] — original autoresearch author
- [[anthropic]] — post-Karpathy-hire, autoresearch becomes first-party-future
- [[ai-question-method]] — Principle 2 ("ask what good looks like") is the human practice this operationalizes
- [[project-room-workflow]] — sister framework targeting "before-the-work artifacts"
- [[capital-allocation-framework]] — "automate" lever instantiated at the skill-eval tier
- [[skill-systems]] — Simon's other framework; composition layer that consumes converged skills
- [[ai-operating-system-offer]] — consulting deliverable that can include self-improving skills as a premium tier
- [[chase-ai]] — fellow evals-tier voice ([[skill-creator]] walkthrough)
- [[content-ideas-skill]] — the preference-tuning (auto-memory) self-improvement mechanism
- [[brad-bonanno]] — author of the auto-memory-tuned `/content-ideas` skill
- [[youtube-digest-apify-2026-05-23]] — citation
- [[youtube-digest-apify-2026-06-03]] — citation (auto-memory preference mechanism)
