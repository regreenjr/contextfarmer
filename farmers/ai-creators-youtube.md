---
name: ai-creators-youtube
description: Track AI/automation YouTubers via Apify YouTube scraper (cloud-routine-friendly). Daily digest of recent videos from tracked channels + topical keyword searches.
fetcher: apify
fetcher_script: ~/.claude/skills/farmer/scripts/apify_youtube.py
fetcher_args:
  channels:
    - "@bradbonanno"          # Brad Bonanno (Karpathy wiki tinkerer, AI & Automation)
    - "@nateherk"             # Nate Herk (N8N + Claude Code OS courses)
    - "@natebjones"           # Nate B. Jones (Claude product tracking)
    - "@grace-leung"          # Grace Leung (marketing automation w/ Claude)
    - "@jackroberts"          # Jack Roberts (Claude Code feature coverage)
  keywords:
    - "Claude Code skill marketplace"
    - "Karpathy LLM wiki"
    - "AI consulting GTM"
  max_per_source: 5
  label: "AI creators + Claude topics"
raw_path: "raw/youtube/digest-{date}.md"
json_sidecar_path: "raw/youtube/digest-{date}.json"
ingest: auto
dedup_by: file-exists
last_run: 2026-05-03
schedule_cron: "0 6 * * *"
auto_commit: true
requires_env: [APIFY_TOKEN]
---

# AI Creators YouTube Farmer (Apify)

## Purpose

Daily digest of new videos from tracked AI/automation YouTubers, plus topical
keyword searches. Replaces the original yt-dlp-based farm with an Apify
implementation so the farm is **cloud-routine-friendly** (Anthropic's scheduled
agent infra may not have yt-dlp available, but always has internet for Apify).

Feeds:
- 3Ps content planning (what topics, frameworks, tools are getting traction)
- Competitive ideation (who's covering what, where the gaps are)
- Skool community pitch + AI Marketing Playbook positioning

## Why Apify

- **Cloud-compatible** — works in scheduled routines without local Python deps
- **Same data** as yt-dlp + better reliability for channel scraping
- **Already in your stack** — `x-monitor` uses Apify, so APIFY_TOKEN is configured
- **Costs ~$0.05-0.10 per daily run** at this volume (5 channels × 5 results)

## Sources

**Channels** (5):
- `@bradbonanno` — Brad Bonanno (708K subs in his AI niche; Karpathy wiki tinkerer; closest to 3Ps positioning)
- `@nateherk` — Nate Herk (708K subs; N8N + Claude Code OS courses)
- `@natebjones` — Nate B. Jones (Claude product feature coverage)
- `@grace-leung` — Grace Leung (136K; marketing-automation-via-Claude angle, closest persona match for 3Ps target customer)
- `@jackroberts` — Jack Roberts (203K; Claude Code feature coverage)

**Keywords** (3) — broader topical scan:
- `Claude Code skill marketplace` — captures discussion of skills as a category
- `Karpathy LLM wiki` — the methodology underlying this very wiki
- `AI consulting GTM` — direct 3Ps positioning research

## Tuning notes

- Edit `channels:` and `keywords:` lists as taste evolves
- Removing a channel doesn't delete already-ingested videos
- If daily volume is too high, drop `max_per_source` to 3
- If you discover a new creator, add their handle and re-run once manually
- For high-priority videos, drop the transcript into `raw/youtube/<channel>/<slug>.md` and run `/wiki-ingest` separately for full per-video ingest

## Required env

```bash
export APIFY_TOKEN=apify_api_xxxxx
```

You should already have this set if `x-monitor` works. Verify with:
```bash
echo "${APIFY_TOKEN:+set}${APIFY_TOKEN:-NOT SET}"
```

## How it runs

```bash
python ~/.claude/skills/farmer/scripts/apify_youtube.py \
  --channels "@bradbonanno" "@nateherk" "@natebjones" "@grace-leung" "@jackroberts" \
  --keywords "Claude Code skill marketplace" "Karpathy LLM wiki" "AI consulting GTM" \
  --max-per-source 5 \
  --output "$HOME/Obsidian/3Ps-Wiki/raw/youtube/digest-$(date +%Y-%m-%d).md" \
  --json "$HOME/Obsidian/3Ps-Wiki/raw/youtube/digest-$(date +%Y-%m-%d).json" \
  --label "AI creators + Claude topics"
```

After write, the farmer skill calls `/wiki-ingest` on the digest file.
