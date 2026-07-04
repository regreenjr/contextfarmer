---
title: Open Skills (Portable Procedures, Not Rented Prompts)
category: concept
summary: [[nate-b-jones]]' **30th named framework** + product launch (*The Skill vs Prompt Problem Everyone Gets Wrong*, 24.8K views, 2026-06-19) — agent skills **do not travel** between [[claude-code]], [[codex]], and Cursor, and *"that is becoming one of the most expensive problems in AI work"*; thesis: **memory alone doesn't make agents work** — the unsolved problem is *who owns the procedure when you switch tools*; prompt bloat becomes **procedural debt** across tools; a **real skill ≠ a clever prompt** (a skill adds verification + is a reusable primitive); **own portable procedures, not rented ones**, and stop re-explaining your work; the portability framework above [[claude-skills]] and the procedural-asset cousin of [[portable-judgment]] (career evidence) and [[retrieval-contract]] (own-it-vs-rediscover-it)
tags: [open-skills, nate-b-jones, framework, portable-skills, procedural-debt, prompt-vs-skill, claude-skills, skill-systems, portable-judgment, retrieval-contract, codex, cursor, claude-code, verification, primitives-vs-runbooks, own-not-rent, agent-ownership]
sources: 1
updated: 2026-07-04
---

# Open Skills

## What it is

[[nate-b-jones]]' **30th named framework** and the launch of his **Open Skills** project (*The Skill vs Prompt Problem Everyone Gets Wrong*, 24.8K views, 2026-06-19, 17:45) in [[youtube-digest-apify-2026-06-24]]. Companion: *The Complete Open Skills Guide* on his Substack.

The opening pain:

> *"Your AI agent finally works the way you want, then you switch tools and it breaks. Agent skills do not travel between Claude Code, Codex, and Cursor, and that is becoming one of the most expensive problems in AI work."*

## The framing claim

> *"The common story is that better memory fixes agent work, but the real question is who owns the procedure when you switch tools."*

Memory (the "Open Brain" problem, chapter 00:00) is necessary but not sufficient. The second, unsolved problem (chapter 00:44): **your agent doesn't know *how you work*** — the procedure. And procedures, today, are **trapped per-tool**: Cursor rules and Claude Code rules don't travel (chapter 03:04).

## Procedural debt

The cost mechanism (chapter 01:39, *Four places procedural debt shows up*): when your process lives as **prompt bloat** scattered across tools, every tool switch forces you to **re-explain your work**. That re-explanation cost is **procedural debt** — it compounds the same way technical debt does, and it's invisible until you switch.

## A real skill ≠ a clever prompt

The load-bearing distinction (chapters 05:36–08:46):

| | Clever prompt | Real skill |
|---|---|---|
| Lives | inside one tool's chat/rules | as a **portable primitive** |
| Travels | no | yes (Open Skills format) |
| Verification | none — you eyeball it | **built in** ("verification turns agent output into work you can trust") |
| Composition | one-shot | **runbooks compose skills** (skills as primitives, 08:46) |

Worked examples (06:00, *Prompt vs skill: search, voice, and browser QA*) show the same task as a throwaway prompt vs a portable, verifying skill.

## The thesis

> **Own portable procedures, not rented ones.** *"Skills will not make agents autonomous, but owning portable procedures is how you stop re-explaining your work and start compounding it across every tool."*

## Where it sits in the vault

- **The portability framework above [[claude-skills]]** — where [[nate-herk]] ranked Skills the #1 Claude Code feature and Anthropic shipped surface-portability (Chat/Cowork/Code), Jones names the *cross-vendor* gap: skills don't travel between **vendors** (Claude Code ↔ Codex ↔ Cursor). Open Skills is his proposed neutral format.
- **The procedural cousin of [[portable-judgment]]** — his 26th framework said *make your judgment portable before your badge stops working*; Open Skills says *make your procedures portable before your tool lock-in taxes you.* Both are "own the asset, don't rent it."
- **Same own-it-vs-rediscover-it instinct as [[retrieval-contract]]** — declare and own what the agent needs up front rather than re-paying every run/tool.
- **The skills-don't-travel claim sharpens [[nate-herk]]'s 3-layer cross-substrate model** — Herk showed `CLAUDE.md`↔`AGENTS.md` symmetry at the *instructions* layer; Jones argues the *skill* layer is where portability actually breaks.
- **Same-batch sibling to [[agent-ownership]]** — both 06-24 Jones videos are about *ownership*: who owns the procedure (Open Skills) and who owns the running agent ([[agent-ownership]]).

## Why it matters for 3Ps

- **Procedural debt is a billable audit** — "where is your process trapped as per-tool prompt bloat?" is a clean diagnostic, same shape as his [[agent-metering]] four-question or T/C/L/D week-tag exercises.
- **Portable skills are the sellable asset** — a 3Ps skill library marketed as *vendor-neutral, verifying primitives* directly answers this framework; the vault's own skills are the reference implementation.
- **"A skill verifies; a prompt doesn't"** is the cleanest one-line definition of the unit 3Ps should ship.

## Open questions

- **What is the Open Skills *format*?** Is it a spec, a converter, a registry? Mechanics gated to the Substack guide.
- **Does it interoperate** with Anthropic Skills / [[skill-authoring-lessons]] conventions, or compete with them?
- **Who adjudicates portability** — is there a runtime, or is it a documentation standard?

## Used in

- [[youtube-digest-apify-2026-06-24]] — vault entry point (Nate B Jones #7)
- [[nate-b-jones]] — author (30th framework)

## Related

- [[claude-skills]] — the unit this makes portable across vendors
- [[skill-systems]] — composition layer; "runbooks compose skills"
- [[portable-judgment]] — the career-evidence sibling; own-don't-rent
- [[retrieval-contract]] — own-it-vs-rediscover-it on the knowledge side
- [[agent-ownership]] — same-batch sibling; who owns the running agent
- [[codex]] — one of the three tools skills fail to travel between
- [[skill-creator]], [[skill-authoring-lessons]] — authoring-side neighbors
- [[reusable-agent-skeleton]]
