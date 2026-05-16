---
title: Plugin Marketplace (Private GitHub-Hosted)
category: concept
summary: [[alex-mcfarland]]'s 2026-03-16 build pattern (resurfaced 2026-05-16) for a **private Claude plugin marketplace hosted on GitHub** — `marketplace.json` manifest + `plugins/` directory grouping skills + one-command install across team/devices + a "Plugin Marketplace Builder Skill" (a [[skill-creator]]-shape meta-skill) that constructs the marketplace from your existing skill folder; the **distribution-layer primitive** sitting between [[claude-skills]] (units) / [[plugins]] (taxonomy) and [[execution-layer]] (team-operational deployment); the **build-walkthrough counterpart** to [[brad-bonanno]]'s deployment-pattern [[execution-layer]] — two creators describing the same primitive from two angles 2 months apart; built in Claude Code, consumed in Cowork
tags: [plugin-marketplace, claude-skills, plugins, cowork, github, alex-mcfarland, brad-bonanno, distribution-layer, builder-skill, meta-skill, team-marketplace, ai-consulting]
sources: 1
updated: 2026-05-16
---

# Plugin Marketplace (Private GitHub-Hosted)

## Definition

A **GitHub-hosted manifest + plugin folder structure** that lets a team install Claude plugins via one command across multiple machines or team members. The distribution-layer primitive between [[claude-skills]] (units) and [[execution-layer]] (team-operational deployment).

Named and walked through by [[alex-mcfarland]] in *You Need a Private Claude Plugin Marketplace (Cowork)* ([[youtube-digest-apify-2026-05-16]] #3, 2026-03-16, 3.2K views, 25:47). The video predates [[brad-bonanno]]'s [[execution-layer]] (2026-05-14) by 2 months — Alex shipped the build pattern before Brad named the deployment layer.

## The artifact

The minimum-viable marketplace:

| Component | Purpose |
|---|---|
| `marketplace.json` | Manifest declaring the marketplace's plugins |
| `plugins/` directory | Each plugin is a folder grouping related skills |
| `skills/` inside each plugin | The actual [[claude-skills]] units |
| GitHub-hosted repo (public OR private) | One-command install across team/devices |
| **Plugin Marketplace Builder Skill** | The skill that *builds* the marketplace from your existing skill folder |

## The build flow ([[alex-mcfarland]] chapters 7:00-12:00)

1. Install the Plugin Marketplace Builder Skill (free download from Alex's Substack)
2. Open Claude Code in your skills folder
3. Launch the builder — it reads existing skills, asks for grouping decisions, generates marketplace structure
4. GitHub setup — accounts, authentication, first-timer onboarding (chapter 9:30)
5. Skill grouping and plugin organization (chapter 10:30)
6. Name the repo; pick public vs private (chapter 12:00)
7. Install on any other machine via one command

## Built in Claude Code, consumed in Cowork (chapter 6:15)

A key clarification despite the video title's "Cowork" tag — the **build happens in Claude Code**. Cowork is the **consumption surface** (where the marketplace gets installed *to*); Claude Code is the **construction surface** (where the marketplace is built).

Same construction/consumption separation pattern Anthropic ships across its product surface (per [[brad-bonanno]]'s 13-product tour in [[youtube-digest-apify-2026-05-10]]):

- **Claude Code** = construction (developer surface)
- **Cowork** = consumption (team/user surface)
- The marketplace bridges them

## Why this is the missing distribution layer

Prior vault coverage of the Claude operational stack covered:

| Layer | Framework | Author |
|---|---|---|
| Unit | [[claude-skills]] | [[anthropic]] |
| Authoring | Skill Creator + 3 Types | [[anthropic]] + [[ben-ai]] |
| Composition | [[skill-systems]] | [[simon-scrapes]] |
| Scaffolding taxonomy | [[plugins]] | [[nate-b-jones]] |
| **Distribution** | **[[plugin-marketplace]] (this concept)** | **[[alex-mcfarland]]** |
| Team deployment | [[execution-layer]] | [[brad-bonanno]] |
| Runtime deployment | [[deployment-framework]] | [[nate-herk]] |
| Eval / meta | [[skill-creator]] | [[anthropic]] + [[chase-ai]] |

The distribution layer was previously implicit — every creator referenced "the marketplace" without naming the build pattern. Alex McFarland is the first creator in this vault to walk through **the actual build steps** for the GitHub-hosted manifest pattern.

## The build-walkthrough vs deployment-pattern duality

[[alex-mcfarland]] (this concept) and [[brad-bonanno]] ([[execution-layer]]) describe the **same architectural primitive from two angles**:

| Angle | Author | What it gives | Date |
|---|---|---|---|
| **Build walkthrough** | [[alex-mcfarland]] | Concrete file structure, builder-skill, GitHub steps | 2026-03-16 |
| **Deployment pattern** | [[brad-bonanno]] [[execution-layer]] | Architectural role + sub-plugins + PR-back loop + cross-vendor framing | 2026-05-14 |

Brad's framework is **what you ship**; Alex's framework is **how you build it**. Together they describe a complete plugin-marketplace stack.

**Possible interpretation**: Alex was implementing what Brad later formalized. The 2-month gap suggests Alex's pattern was the **prior art** that Brad's execution-layer codified.

## The builder-skill is a meta-skill

The **Plugin Marketplace Builder Skill** is a [[skill-creator]]-shape meta-skill — a skill that builds other artifacts:

| Meta-skill | Author | What it builds |
|---|---|---|
| [[skill-creator]] | [[anthropic]] | Tests and benchmarks other skills |
| Plugin Marketplace Builder | [[alex-mcfarland]] | Marketplace.json + folder structure from existing skills |
| `/create-farmer` | [[brad-bonanno]] | New farmer config + scheduled routine |
| CLAUDE.md generator | [[anthropic]] | Bootstrap project schema |

**Meta-skills are themselves becoming a tracked category** — at least four canonical examples now exist in the vault. This may deserve a future synthesis page on **builder skills as a primitive category**.

## Audience positioning

[[alex-mcfarland]]'s explicit audience (from his description):

> "This is for solopreneurs running Claude across multiple machines, team leads managing shared workflows, freelancers building skill libraries for clients, and anyone who wants a professional plugin system without touching code."

Four distinct user segments — most relevant to 3Ps:

| Segment | Use case | 3Ps relevance |
|---|---|---|
| Solopreneurs multi-machine | Sync skills across desktop/laptop/cloud | Direct (vault user) |
| Team leads | Shared team workflows | Direct (3Ps client) |
| **Freelancers building for clients** | **Skill library as deliverable** | **Highest match — canonical 3Ps deliverable** |
| Non-developer team leads | Professional plugin system without code | Beginner-tier extension |

The third segment — *freelancers building skill libraries for clients* — is **the canonical 3Ps consulting deliverable shape**.

## Public vs private (chapter 12:00)

The GitHub repo can be public OR private:

| Public marketplace | Private marketplace |
|---|---|
| Free distribution; community discovery | Team-only / client-only access |
| No access control | Per-repo collaborator list |
| Discoverable via GitHub search | Hidden; requires invitation |
| Same install command shape | Same install command shape |
| Use case: open-source plugin authors | Use case: 3Ps client deliverables, team SOPs |

The same artifact powers both — only the GitHub repo visibility setting differs. This means a single builder-skill output is reusable across the open-source authorship use case and the consulting-deliverable use case.

## Why it matters for 3Ps

1. **Direct 3Ps deliverable artifact** — Alex names "freelancers building skill libraries for clients" as an explicit audience segment; the marketplace is the deliverable
2. **Private GitHub repo as client handoff** — each client engagement could ship a private repo + one-command install line as the durable artifact
3. **Builder-skill is replicable** — once 3Ps has a marketplace-builder skill template, every client engagement bootstraps faster
4. **Sits below [[execution-layer]] in the deliverable stack** — Phase 2 of a 3Ps engagement (after the wiki + farmer + skills are in place) ships the marketplace + builder-skill
5. **No-code-positioned** — extends the [[ai-consulting]] audience tier to the non-developer team-lead band that Alex addresses

## Open questions

- **What's the marketplace.json schema?** — is there an Anthropic-blessed spec, or is this a creator-defined convention? (Worth checking the `claude-plugins-official` repo for the canonical schema)
- **How does install actually work?** — one-command install requires a Claude Code CLI command + GitHub auth + manifest parsing; what's the actual command?
- **Cross-version compatibility** — what happens when skills update? Does the marketplace ship version pins?
- **Sub-plugin support** — does Alex's pattern support the [[brad-bonanno]] [[execution-layer]] sub-plugin decomposition (sales/ops/CS), or is that a Brad-specific extension?
- **Discovery mechanism for private marketplaces** — once a client has a private repo, how do new team members find it?
- **PR-back loop integration** — Brad's [[execution-layer]] explicitly names the PR-back loop; does Alex's pattern bake this in, or is it a separate workflow layer?

## Contrasts with

- **`claude-plugins-official`** — Anthropic's centrally-hosted marketplace; private marketplaces decentralize this
- **[[execution-layer]]** — team-operational deployment of the marketplace; this concept is the marketplace's *file artifact*
- **[[plugins]] taxonomy** — categorical "what scaffolding type is this"; this concept is the distribution layer for the taxonomy's outputs
- **Skill folder direct sharing** — the pre-marketplace pattern (just zip up your skills folder); private marketplace adds versioning, manifest, one-command install
- **NPM / PyPI** — package-manager pattern; private marketplaces are similar but Claude-specific and skill-typed

## Used in

- [[youtube-digest-apify-2026-05-16]] — primary citation ([[alex-mcfarland]] #3)
- [[alex-mcfarland]] — primary author
- [[plugins]] — taxonomy layer whose outputs the marketplace distributes
- [[execution-layer]] — [[brad-bonanno]]'s deployment-pattern counterpart
- [[claude-skills]] — units distributed
- [[skill-creator]] — sibling meta-skill pattern
- [[claude-code]] — construction surface
- [[ai-consulting]] — productization target

## Related pages

- [[alex-mcfarland]], [[brad-bonanno]] (sibling), [[anthropic]]
- [[execution-layer]] — deployment-pattern counterpart
- [[claude-skills]], [[plugins]], [[skill-systems]], [[skill-creator]], [[deployment-framework]] — sibling operational-stack frameworks
- [[claude-code]] — substrate; construction surface
- (Cowork — consumption surface; future entity stub if it ever surfaces with substantive coverage)
