---
title: Eric Tech
category: entity
summary: Small-tier AI YouTuber (3.4K views on the /wiki skill video) + Skool community operator (`skool.com/erictech`); first creator in this vault to ship a `/wiki` skill that **automates the entire LLM Wiki ingest workflow on a cron** — pulling from YouTube/Gmail/Slack/any-MCP-source into an Obsidian vault; **convergent-evolution proof** of this vault's exact architecture (skill + farmer subagents + scheduled cron); also operates **bookzero.ai** (AI-powered bookkeeping product built entirely with Claude Code) — first Claude-Code-built SaaS tracked in this vault, sibling positioning to [[claude-for-small-business]]
tags: [creator, youtube, small-channel, llm-wiki, wiki-skill, farmer-agents, cron-scheduling, claude-code, obsidian, skool, bookzero, claude-built-saas, vault-architecture-parallel, second-brain]
sources: 1
updated: 2026-05-22
---

# Eric Tech

## What it is

Person + YouTube channel **Eric Tech** + Skool community at `skool.com/erictech` (paid — skill + 100+ templates + weekly Claude Code masterclasses). Also operates **bookzero.ai** — an AI-powered bookkeeping product **built entirely with Claude Code**, the first Claude-Code-built SaaS surfaced in this vault.

## Why it matters for this wiki

**He shipped the exact primitive triple this vault implements.** Eric's `/wiki` skill + farmer subagents + cron-scheduling is the same architecture this vault has been running since 2026-05-03. Convergent evolution from two independent creators = strong correctness signal for the pattern, AND **a competitive datapoint** — "I built an LLM Wiki" is now creator-shipped-skill territory, not vault-only territory.

## Key video in [[youtube-digest-apify-2026-05-22]]

- **#8** *Karpathy's LLM Wiki + This Skill = Game Changer* — 3.4K views, 2026-05-20, 16:19

**Chapter map**:
- 0:00 Intro
- 1:50 The Workflow
- 4:26 **Wiki Skill**
- 5:24 Interview Phase
- 6:35 Folder Structure
- 8:34 **Farmer Agents**
- 10:53 Run Wiki Farm
- 13:18 Final Demo
- 14:23 **Schedule Cron**
- 15:24 Wrap Up

**The framing claim**: *"Karpathy's LLM Wiki is the smartest way to use AI for research — but it has one problem: you still have to manually feed it every single source. So I built a Claude Code skill that automates the entire workflow on a schedule."*

**The primitive triple** (the convergent-evolution evidence):

| Eric Tech's `/wiki` | This vault | Pattern shape |
|---|---|---|
| `/wiki` skill (init + ingest + lint wrapped) | `/wiki-ingest`, `/wiki-query`, `/wiki-lint` | Same triple, slightly different naming |
| **Farmer subagents** that ingest multiple sources in parallel | `farmers/<name>.md` configs + `farmer` skill | **Identical naming** ("farmer") + identical pattern |
| Schedule the workflow as a cron job | Daily ai-creators-youtube farm via Routines | Same scheduling pattern |
| Obsidian vault as the substrate | Obsidian vault as the substrate | Identical |
| Claude Code as the ingest agent | Claude Code as the ingest agent | Identical |

**The "Interview Phase"** (chapter 5:24) — Eric's `/wiki` skill asks the user about their use case before generating the vault structure. **Same shape as [[skill-creator]]'s description-optimization step** — meta-skill behavior that customizes the artifact to the user.

## bookzero.ai callout

- `bookzero.ai — AI-powered bookkeeping built entirely with Claude Code`
- **First Claude-Code-built SaaS tracked in this vault** — confirms Claude Code is now a viable production-application substrate (not just a developer-CLI tool)
- **Sibling positioning to [[claude-for-small-business]]** — both target SMB bookkeeping/financials, but bookzero is standalone SaaS while CFSB is an Anthropic-shipped plugin
- Open question: bookzero's actual product surface + pricing + traction — worth investigating as a Claude-Code-built reference customer

## Distribution / monetization

- **YouTube** — `Eric Tech` channel (3K-views-per-video small-tier range)
- **Skool community** — `skool.com/erictech` (paid; skill download + 100+ templates + weekly Claude Code masterclasses) — the `/wiki` skill is gated behind the community
- **Databox affiliate** — 14-day free trial (`databox.com/?_by=erictech`)
- **bookzero.ai** — standalone SaaS product (separate funnel)
- **Referenced video**: *Obsidian + Claude Code: The Second Brain CRM I built last month* — suggests he has prior Obsidian/CRM content predating the `/wiki` skill

## Strategic significance

1. **Convergent-evolution proof** for the vault's architecture — Eric and the vault independently arrived at the same primitive triple (skill + farmer subagents + cron) within weeks of each other. Strong correctness signal for the pattern.
2. **Differentiation pressure on the vault** — "I built an LLM Wiki" is now creator-shipped-skill territory. Vault differentiation now lives in:
   - What's *in* the wiki (3Ps + GTM + competitive intel content)
   - Quality + depth of farmer configs
   - Multi-source farming (YouTube + ads + future channels — Slack, Gmail, X, GitHub)
   - Cross-reference + synthesis density
3. **Adoption-tier signal** — small-channel (3.4K views) but ships paid Skool community. The [[karpathy-llm-wiki]] pattern is now a **mid-tier commercial product**, not a hobbyist artifact.
4. **bookzero.ai is the canonical Claude-Code-built reference customer** — every "can you actually ship production software in Claude Code" question now has Eric's bookkeeping SaaS as the existence proof.
5. **First "farmer" creator-namespace collision** — Eric's "farmer agents" and Brad's "farmer" pattern (referenced in [[brad-bonanno]] #23 *Company Brain*) and this vault's `farmer` skill **all use the same terminology**. The vocabulary is settling — "farmer" is the canonical name for source-ingest-subagents.

## Related

- [[karpathy-llm-wiki]] — the pattern Eric automates
- [[context-farming]] — direct parallel implementation
- [[claude-code]] — substrate
- [[claude-skills]] — `/wiki` skill artifact
- [[brad-bonanno]] — earlier "farmer" + "Company Brain" pattern; Eric is the **post-Brad** generation of the architecture
- [[andrej-karpathy]] — origin of the gist Eric builds on
- [[hermes-agent]] — alternative substrate that runs the same pattern (per [[corey-ganim]])
- [[claude-for-small-business]] — sibling SMB-targeted artifact (Anthropic-shipped vs Eric's bookzero standalone)

## Appears in

- [[youtube-digest-apify-2026-05-22]] — primary source

## Why track him for 3Ps

- **Direct architectural parallel** — anything he ships likely belongs in this vault's roadmap
- **bookzero.ai** is a reference customer for the "Claude Code as production substrate" thesis — every CAIO/SMB engagement can cite it
- **His Skool community** is a competitive benchmark for any 3Ps community product (paid skill + templates + weekly masterclasses model)
- **His /wiki skill** is the closest creator-shipped competitor to this vault as a deliverable artifact

## Open questions

- What does Eric's `/wiki` skill **actually do differently** from this vault's setup? Worth joining Skool to inspect the skill source.
- Is the "Interview Phase" (chapter 5:24) more sophisticated than this vault's static schema, or is it just an init wizard?
- bookzero.ai traction — MRR, customer count, retention?
- Does Eric run **other** farmers beyond YouTube/Gmail/Slack? Multi-source coverage is the vault's current advantage.
- Cross-platform presence (X, LinkedIn)?
- Pricing of the Skool community — sub count?
