---
title: Skill Authoring Lessons (Anthropic's Internal Playbook)
category: concept
summary: Anthropic's official "lessons from building Claude Skills internally" article, surfaced 2026-06-06 via [[brock-mesarich]]'s *Anthropic Just Dropped Their Claude Skills Secrets* (11.3K views) — the first-party authoring discipline behind [[claude-skills]]; nine categories of skills; the **description field is the highest-leverage field** (write it for the model, not humans); the **gotchas section is "the highest-signal part of any skill"**; **progressive disclosure via the file system** (good-vs-avoid example files loaded only when needed); **stop railroading Claude** (don't over-constrain a capable model); distribute via `.claude/skills` + plugins; main takeaway *start small, iterate*; the official-source complement to creator authoring frames ([[ben-ai]] 3-types, [[code-with-beto]], [[chase-ai]] capability-vs-preference) and the human-readable companion to the [[skill-creator]] eval loop
tags: [skill-authoring, claude-skills, claude-code, anthropic, description-field, gotchas-section, progressive-disclosure, stop-railroading, nine-categories, file-system, write-for-the-model, start-small-iterate, plugins, brock-mesarich, official-guidance]
sources: 1
updated: 2026-06-06
---

# Skill Authoring Lessons (Anthropic's Internal Playbook)

Anthropic's official article **"Lessons from building Claude Skills"** (`claude.com/blog/lessons-from-...`) — the first-party authoring discipline behind [[claude-skills]], surfaced in this vault 2026-06-06 via [[brock-mesarich]]'s walkthrough *Anthropic Just Dropped Their Claude Skills Secrets (steal these)* (11.3K views, 2026-06-05, 10:27, [[youtube-digest-apify-2026-06-06]] #1).

It is the **official-source counterpart** to the creator-side authoring frames the vault already tracks ([[ben-ai]]'s "3 Types of Skills," [[code-with-beto]]'s best-practices, [[chase-ai]]'s capability-uplift-vs-encoded-preference split) — and the **human-readable companion** to the [[skill-creator]] eval loop (Skill Creator tests a skill; this article tells you how to *write* one worth testing).

## The lessons (per Brock's walkthrough of the article)

1. **Skill misconceptions** (chapter 1:00) — what people get wrong about skills before they start (specifics gated to the article/video).
2. **The 9 categories of skills** (2:01) — Anthropic's internal taxonomy of skill *kinds*. The specific nine are gated to the article; this is a more granular categorization than [[ben-ai]]'s "3 Types" frame.
3. **Build a gotchas section** (3:30) — Anthropic calls the **gotchas section the highest-signal part of any skill**. The edge cases, failure modes, and "don't do X" warnings are where a skill earns its keep — more valuable than the happy-path instructions.
4. **The email-drafter example — good vs avoid files** (4:20) — a worked example pairing a `good.md` (examples to imitate) with an `avoid.md` (anti-patterns to steer away from). Concrete instantiation of the progressive-disclosure pattern below.
5. **Progressive disclosure & the file system** (5:26) — the skill's body stays lean; supplemental material (examples, references, templates) lives in files that Claude loads **only when needed**. The file system *is* the context-management mechanism. (This vault implements the same pattern with `references/` and `.templates/`.)
6. **Stop railroading Claude** (6:36) — don't over-constrain a capable model with rigid step-by-step scripts. Over-specification wastes the frontier model's judgment; give it the goal and the guardrails, not a railroad track. (Same instinct as [[ai-question-method]]'s "senior partner, not junior teammate.")
7. **Write descriptions for the model, not humans** (7:41) — the **`description` field is the highest-leverage field in the skill**, and it should be written for the *model's* invocation decision, not as human-readable marketing. This matches [[skill-creator]]'s automated **description-field optimization** — the field that determines *whether the skill fires at the right time*.
8. **Distributing skills** (8:39) — `.claude/skills` directory for local/project skills + **plugins** for packaged distribution. Aligns with [[brock-mesarich]]'s own single-plugin-bundle distribution philosophy and the [[plugin-marketplace]] pattern.
9. **Main takeaway — start small, iterate** (9:43) — don't author a mega-skill up front. Ship a minimal skill, watch where it fails, and grow it. The anti-[[skill-systems]]-mega-skill discipline, stated by Anthropic directly.

## Why it matters

- **First-party validation of vault-tracked patterns.** Three things creators had been inferring are now confirmed by Anthropic directly: the **description field is the invocation lever** (matches [[chase-ai]]/[[skill-creator]]), **progressive disclosure via files** (matches this vault's `raw/`→`wiki/` + `references/` architecture), and **start-small-not-mega-skill** (matches [[simon-scrapes]]' [[skill-systems]] composition discipline).
- **The gotchas-section claim is the new high-signal datapoint.** "The gotchas section is the highest-signal part of any skill" reframes skill authoring around *failure modes first* — a clean, portable rule for any 3Ps client skill build. The vault's `> ⚠️ Contradiction:` callouts are the wiki-scale analog.
- **"Write the description for the model" is the single most actionable line.** It's the field most authors treat as a label and Anthropic treats as the core invocation mechanic. Pairs directly with [[skill-creator]]'s description-field optimization pass.
- **Official source slots above the creator funnel.** The [[claude-skills]] explainer funnel (official 201K explainer → developer walkthrough → authoring framework → beginner explainer → cross-surface tutorial) now has an **authoring-discipline article** at its first-party top — the "how to write one well" companion to the "what skills are" explainer.

## Related pages

- [[claude-skills]] — the primitive this article teaches you to author well
- [[skill-creator]] — the eval/optimization meta-skill; this article is its human-readable authoring companion (description-field optimization is shared)
- [[brock-mesarich]] — surfaced the article via his 2026-06-06 walkthrough
- [[anthropic]] — author of the source article
- [[ben-ai]] — creator-side "3 Types of Skills" authoring frame (the 9-categories taxonomy is the first-party, more granular version)
- [[chase-ai]] — capability-uplift vs encoded-preference eval split (pairs with the description-field guidance)
- [[skill-systems]] — "start small, iterate" is the anti-mega-skill composition discipline
- [[ai-question-method]] — "stop railroading Claude" = the senior-partner-not-junior-teammate instinct at the skill layer
- [[plugin-marketplace]] — the distribution half (`.claude/skills` + plugins)
- [[youtube-digest-apify-2026-06-06]] — citation
