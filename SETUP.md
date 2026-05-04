# 3Ps-Wiki — Setup & Operating Guide

Self-updating Karpathy-style LLM wiki for 3Ps consulting + GTM playbook + competitive intel.

## Architecture

```
Sources (real world)
    │
    ▼
┌─────────────────────────────────────────┐
│  Existing source skills (you own)       │
│  yt-search · x-monitor ·                │
│  competitive-ads-extractor ·            │
│  github-trending · lead-research-       │
│  assistant · custom MCPs                │
└──────────────┬──────────────────────────┘
               │ invoked by
               ▼
┌─────────────────────────────────────────┐
│  /farmer <name>  ←  this skill          │
│  reads farmers/<name>.md                │
│  fetches → saves to raw/ → ingests      │
└──────────────┬──────────────────────────┘
               │ writes raw/, calls
               ▼
┌─────────────────────────────────────────┐
│  /wiki-ingest  →  wiki-ingestor agent   │
│  reads source, discusses, writes        │
│  summary + 5-15 cross-refs, updates     │
│  index, appends log                     │
└──────────────┬──────────────────────────┘
               │
               ▼
       ~/Obsidian/3Ps-Wiki/wiki/
       (entities · concepts · sources ·
        comparisons · synthesis)
               │
               ▼
       /wiki-query, /wiki-lint, Marp export
```

## What's installed

| Component | Path | Source |
|---|---|---|
| llm-wiki skill | `~/.claude/skills/llm-wiki/` | alirezarezvani/claude-skills v2.3.2 |
| Sub-agents | `~/.claude/agents/wiki-ingestor.md` (+ librarian, linter) | same |
| Slash commands | `~/.claude/commands/wiki-init.md` (+ ingest, query, lint, log) | same |
| Farmer skill | `~/.claude/skills/farmer/` | custom — orchestrates your existing source skills |
| Vault | `~/Obsidian/3Ps-Wiki/` | initialized |
| Farm configs | `~/Obsidian/3Ps-Wiki/farmers/*.md` | 3 starter configs |

## Daily commands

```
/wiki-log --last 10                              # what farmers did overnight
/wiki-query "what are AI YouTubers covering?"    # ad-hoc question against the wiki
/wiki-lint                                        # weekly health check
/wiki-ingest <path>                               # manual ingest of a one-off source
```

## Schedule the farmers

Use `/schedule` (Claude Code Routines) to run each farmer daily. Stagger times so they don't fight for the wiki lock:

```
/schedule create "Run /farmer ai-creators-youtube" --cron "0 6 * * *"
/schedule create "Run /farmer x-trends"            --cron "30 6 * * *"
/schedule create "Run /farmer competitor-ads"      --cron "0 7 * * *"
```

Run any farmer manually first to verify wiring before scheduling:
```
/farmer ai-creators-youtube
```

## Adding a new farm (5-line addition)

1. `cp ~/Obsidian/3Ps-Wiki/farmers/x-trends.md ~/Obsidian/3Ps-Wiki/farmers/<new>.md`
2. Edit frontmatter: `name`, `fetcher_skill`, `fetcher_args`, `raw_path`, `dedup_by`
3. Edit body: why these sources, what to expect
4. Test: `/farmer <new>`
5. Schedule: `/schedule create "Run /farmer <new>" --cron "<your-time>"`

## Adding a new source skill

If a farm needs data the existing skills can't fetch (e.g., Slack DMs, Notion pages, custom scraper):
1. Either: build an MCP for it (see `/skill-creator` or `/mcp-builder`)
2. Or: write a one-off Python helper in `~/Obsidian/3Ps-Wiki/farmers/scripts/`
3. Reference it in the farm's `fetcher_skill: <new-skill-name>` field

## Iron rules

1. **`raw/` is immutable** — farmers and the user write here; the wiki agents only read.
2. **All wiki writes go through `/wiki-ingest`** — never edit `wiki/` files directly.
3. **Dedup before ingest** — re-ingesting corrupts date tracking. Each farm has `dedup_by`.
4. **Every farm run logs to `wiki/log.md`** — that's how you know what happened overnight.
5. **`auto_commit: true` requires the vault to be a git repo** — see "Git setup" below.

## Git setup (recommended)

For Brad-style "wake up to a wiki that updated overnight":

```bash
cd ~/Obsidian/3Ps-Wiki
git init
git add -A
git commit -m "init: 3Ps wiki + farmers"
gh repo create 3Ps-Wiki --private --source . --push
```

Then enable Obsidian Git plugin so the vault auto-pulls changes when farmers commit from the cloud (if you ever migrate farmers to Claude Code Routines that run on Anthropic infra).

## Obsidian setup

1. Open `~/Obsidian/3Ps-Wiki` as a vault in Obsidian
2. Recommended plugins: Graph view (built-in), Backlinks, Dataview, Marp, Templates, Git
3. Settings → Files and links → Attachment folder = `raw/assets/`
4. Bind Ctrl+Shift+D to "Download attachments for current file" (for clipped articles)

## Troubleshooting

**Farm runs but no new pages appear:** check `~/Obsidian/3Ps-Wiki/raw/` — files should be there. If not, the fetcher skill failed silently.

**Wiki has duplicates:** `dedup_by` is mis-specified. Check the farm's frontmatter.

**Routines aren't firing:** `/schedule list` to confirm. If empty, re-create. If listed but not running, check Claude Code's scheduled tasks status in the desktop app.

**`/wiki-ingest` not found:** the slash command files are at `~/.claude/commands/wiki-*.md`. They need to exist for invocation. Re-run install if missing.

**Wiki getting noisy:** run `/wiki-lint` weekly. It surfaces orphans, contradictions, stale claims, and concepts mentioned without their own page. Address top 3-5 each week.

## Future moves

- **Add wiki-audit (kfchou)** for fact-checking citation discipline if you start ingesting Medvi/regulatory sources
- **Marp export** — wiki pages → 3Ps consulting decks: `python ~/.claude/skills/llm-wiki/scripts/export_marp.py`
- **Farm Slack** — once the Slack MCP is wired, add `farmers/slack.md` (5-line addition)
- **Farm Fireflies** — meeting transcripts → wiki entity pages for clients/prospects

## Provenance

- LLM-wiki skill: [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) v2.3.2 — MIT
- Pattern: [Karpathy's LLM Wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) (April 2026)
- Farmer skill: custom; wraps existing skills you already had installed
