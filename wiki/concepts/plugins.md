---
title: Plugins (as Mech-Suit)
category: concept
summary: [[nate-b-jones]]'s 6-layer agentic-scaffolding taxonomy — prompts, skills, plugins, MCPs, hooks, scripts — explicitly positioning plugins as bigger than MCPs and undersold by the app-store analogy; the missing taxonomy layer above [[skill-systems]] composition and [[claude-skills]] units; "the leverage in 2026 lives in knowing which part of your workflow belongs in a prompt, a skill, a plugin, or an MCP"; in 2026-05-16 [[alex-mcfarland]]'s [[plugin-marketplace]] surfaces as the **distribution-layer artifact** for the plugin layer — a GitHub-hosted manifest + folder structure that lets a team install plugins via one command across machines (the build-walkthrough counterpart to [[brad-bonanno]]'s [[execution-layer]] deployment-pattern)
tags: [plugins, agentic-scaffolding, prompts, claude-skills, mcp, hooks, scripts, skill-systems, nate-b-jones, taxonomy, mech-suit, plugin-marketplace, distribution-layer, tool-overload, tech-with-tim, fifty-tool-ceiling, plugin-curation]
sources: 3
updated: 2026-07-07
---

# Plugins (as Mech-Suit)

## Definition

[[nate-b-jones]]'s **6-layer agentic-scaffolding taxonomy** — the explicit positioning of every layer that surrounds an LLM in productive use. Named in [[youtube-digest-apify-2026-05-10]] #11 (*You're Wasting 40% Of Your AI Time On Something Fixable*, 31.1K views).

The mech-suit metaphor: **the LLM is the human pilot; the mech is everything wrapped around it that makes the pilot effective.**

## The 6 layers

| # | Layer | Best for | Failure mode | Key chapter |
|---|---|---|---|---|
| 1 | **Prompts** | One-offs, exploration | Break under repeated workflows | 11:38 |
| 2 | **Skills** | "House style" encoded across any LLM | Mega-skill bloat ([[skill-systems]]) | 13:30 |
| 3 | **Plugins** | Whole workflows your team can install | Underdescribed by app-store analogy | 17:22 |
| 4 | **MCPs / app connectors** | Live access to where work lives | Token cost ([[printing-press]]) | 21:12 |
| 5 | **Hooks** | Deterministic events you don't trust the model with | Lock-in to specific runtime | 23:06 |
| 6 | **Scripts** | Deterministic logic you don't trust the model with | Brittleness, maintenance | 23:06 |

## Why this taxonomy is the missing layer

This vault tracked four of these as separate concepts ([[claude-skills]], [[mcp]], [[skill-systems]]) but never had the **map of where each fits relative to the others**. The plugin layer specifically was undefined.

The full vocabulary stack for agentic scaffolding now reads:

| Layer | Question | Source |
|---|---|---|
| **Taxonomy** | What types of scaffolding exist? | **[[nate-b-jones]] (this page)** |
| Authoring | How do I write *one* skill well? | [[code-with-beto]], [[anthropic]] Skill Creator |
| Authoring framework | What categories of skills exist? | [[ben-ai]] (3 Types) |
| Composition | How do skills chain into automations? | [[simon-scrapes]] ([[skill-systems]]) |
| Curation | Which skills to install? | [[nate-herk]], [[brock-mesarich]], [[dubibubii]] |

[[nate-b-jones]]' map sits **above** all of these — it's the categorical scaffolding within which authoring/composition/curation happen.

## Plugins specifically

Per [[nate-b-jones]] #11 (chapter at 17:22 + 25:27):

- **Plugins package up a whole workflow** that a team can install in one motion
- **Plugins are bigger than MCPs** — they may *contain* MCPs, skills, hooks, scripts as components
- **The app-store analogy undersells them** — apps are user-facing UI; plugins are agent-side composable workflows
- **The right mental model** is closer to a Unity asset pack or a Docker compose file — bundles of scaffolding ready to install
- **Reuse mechanic** — "your team can actually reuse them" (vs prompts/skills which often need re-authoring per use case)

## The plugin distribution layer ([[alex-mcfarland]] 2026-05-16)

The plugin layer needs **a distribution-layer primitive** to ship plugins between machines or to a team. [[alex-mcfarland]]'s [[plugin-marketplace]] (2026-03-16, resurfaced 2026-05-16) is the **first build walkthrough** for this primitive in the vault:

- `marketplace.json` manifest declaring the marketplace's plugins
- `plugins/` directory grouping skills into plugins
- GitHub-hosted repo (public OR private) — one-command install across machines
- A "Plugin Marketplace Builder Skill" (a [[skill-creator]]-shape meta-skill) that builds the marketplace from your existing skill folder

This is the **build-walkthrough counterpart** to [[brad-bonanno]]'s [[execution-layer]] deployment-pattern (2026-05-14) — Brad's framework gives the *architecture*, Alex's gives the *build steps*. The same artifact powers both the open-source authorship use case (public repo) and the consulting-deliverable use case (private repo).

## The count ceiling — curate down, don't max out ([[tech-with-tim]] 2026-07-06)

The 6-layer taxonomy answers *which layer* work belongs in; [[tech-with-tim]]'s *The Only Claude Code Plugins You Actually Need* ([[youtube-digest-apify-2026-07-07]] #3) adds the missing *how many* constraint → new concept [[tool-overload]]:

> *"Once Claude can see more than about **50 tools** at once, it starts picking the wrong ones — and your agent actually gets **worse, not better**."*

The failure mode is **tool-selection quality**, not just token cost — a sharper, empirically-numbered version of this page's *"40% wasted on the wrong layer."* Where [[nate-b-jones]] says *right layer*, Tim says *bounded count*: too many similar tools crowd the model's tool-pick decision and degrade every unrelated task. His pruned slate (TigerData MCP, GitHub MCP, Context7, Figma, Frontend Design) is the inverse of maximalist curation ([[dubibubii]]'s 33 tools). → See [[tool-overload]].

## When to use each layer

[[nate-b-jones]]'s decision rule (paraphrased from #11):

| If the work is... | Use |
|---|---|
| One-off exploratory | **Prompt** |
| Repeated across one user's workflows | **Skill** |
| Repeated across a team and bundles multiple components | **Plugin** |
| About reaching live external systems | **MCP** |
| Triggered by deterministic events | **Hook** |
| Logic you don't trust the model with | **Script** |

The "40% wasted" stat in the title comes from: **operators putting the work in the wrong layer.** Common errors:
- One-shot prompt for what should be a skill (re-tokens every use)
- Mega-skill for what should be a plugin (bloat)
- MCP for what should be a CLI / script (token-cost; see [[printing-press]])
- Skill for what should be a hook (re-prompts when an event would trigger automatically)

## Why now (chapter at 9:42)

[[nate-b-jones]]: GPT-5.5 + messy multi-part work makes the layers visible. As agents do real work, the scope-mismatch errors compound — wrong-layer choices that didn't matter at small scale become 40% of the operator's time at production scale.

## Implications for [[claude-code]] users

- The vault's `claude/` directory should be auditable through this taxonomy: how many of your scaffolding artifacts are **wrong-layer**?
- **Cross-vendor portability**: prompts and skills port across [[claude-code]] / [[codex]] / [[hermes-agent]]; plugins/MCPs/hooks/scripts vary by substrate
- **Plugin-format compatibility** is the **next big interop question** — if Anthropic, OpenAI, and Hermes each ship plugin formats, the cross-vendor compatibility story collapses without an open standard

## Why it matters for 3Ps

1. **Sales-conversation framework** — when a prospect describes a vague need, the 6-layer map turns the conversation into a categorization exercise
2. **Audit deliverable** — "your team has 40 skills, 12 of which should be plugins, 8 should be hooks, 6 should be scripts" is a high-value 1-2 day engagement with concrete output
3. **Authorship of plugins** — plugins are **the next packaging unit** above skills; 3Ps can author and sell branded plugins (multi-skill bundles + MCPs + hooks + scripts) as paid product
4. **Content angle** — "you're wasting 40% of your AI time on something fixable" is a sticky headline reusable across content surfaces
5. **Plays with [[work-primitive]]** — when the substrate has rich meaning + authority, more work fits in plugins (vs prompts); when substrate is bare access only, more work falls back to prompts

## Open questions

- **Plugin format standardization** — is there an emerging cross-vendor plugin spec, or will each substrate ship its own?
- **Anthropic plugins** — `claude-plugins-official` exists; does Anthropic have a plugin manifest spec, or is "plugin" a marketplace label?
- **Plugin marketplace economics** — paid plugins are emerging; what's the take-rate, distribution model?
- **Plugin vs Skill System** ([[skill-systems]]) — is a plugin always a Skill System + MCPs/hooks/scripts, or can a plugin be smaller than a Skill System?
- **Hook/script triggers** — what events trigger hooks vs scripts vs scheduled cron?

## Related pages

- [[claude-skills]] — units packaged inside plugins
- [[skill-systems]] — composition discipline; layer below plugins
- [[mcp]] — connector layer; can be packaged inside plugins
- [[printing-press]] — CLI alternative to MCP; layer 4 alternative
- [[work-primitive]] — sibling [[nate-b-jones]] framework (substrate-side)
- [[anticipation-gap]] — sibling [[nate-b-jones]] framework (user-side)
- [[claude-code]] — substrate where this taxonomy is realized
- [[codex]] — sibling substrate; taxonomy ports across
- [[hermes-agent]] — sibling substrate
- [[nate-b-jones]] — author
- [[alex-mcfarland]] — author of the [[plugin-marketplace]] distribution-layer counterpart
- [[brad-bonanno]] — author of the [[execution-layer]] deployment-pattern counterpart
- [[plugin-marketplace]] — distribution-layer artifact for plugins
- [[execution-layer]] — team-operational deployment pattern
- [[deployment-framework]] — runtime-selection framework for where plugins execute
- [[ai-consulting]] — direct deliverable framework
- [[tool-overload]] — the ~50-tool selection ceiling; the *how many* count constraint on this *which layer* taxonomy
- [[tech-with-tim]] — author of the curation-ceiling argument
- [[youtube-digest-apify-2026-05-10]], [[youtube-digest-apify-2026-05-16]], [[youtube-digest-apify-2026-07-07]] — primary citations
