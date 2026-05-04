---
title: YouTube Digest (Apify) — smoke-test — 2026-05-03
source_type: youtube-digest-apify
source_url: https://www.youtube.com/
fetched: 2026-05-03
farmer: ai-creators-youtube
label: "smoke-test"
video_count: 2
---

# YouTube Digest (Apify) — 2026-05-03

## Source
- Label: **smoke-test**
- Videos returned: **2**
- Fetcher: Apify `streamers/youtube-scraper` actor

## Videos

| # | Title | Channel | Views | Date | Duration | URL |
|---|---|---|---|---|---|---|
| 1 | I FINALLY Stopped Babysitting Claude (Automate Anything) | Brad \| AI & Automation | 7641 | 2026-04-22 | 00:20:27 | https://www.youtube.com/watch?v=1RdkW1zqv-U |
| 2 | My Claude Code Can INSTANTLY Watch Any Video (Here's How) | Brad \| AI & Automation | 53727 | 2026-04-29 | 00:08:36 | https://www.youtube.com/watch?v=QZMljuD10sU |

## Per-video descriptions

### 1. I FINALLY Stopped Babysitting Claude (Automate Anything)

AI Strategy Call: https://cal.com/bradley-bonanno/ai-st...
The Complete Setup Guide (FREE): https://brad-b.kit.com/7f35d608cf

Anthropic shipped four different automation surfaces for Claude: Skills, Cowork, Routines, and Managed Agents. The result is that nobody actually knows which one to use for what. Most people pick whichever one they heard about first and hope it fits.

In this video I walk you through all five levels of Claude automation in order. At each level I build a real workflow end to end so you can see exactly what that level is for and where it breaks. By the end you'll know which level to reach for the next time you want to take work off your plate, plus the gotcha that means n8n and Make are not actually dead.

Links
Connect with Me:   / bradbonanno  
Skills Marketplace Waitlist: https://brad-b.kit.com/f9a7349a1c
Firecrawl: https://firecrawl.link/bradley-bonanno
Apify: https://www.apify.com?fpr=ih20xe

In this video I cover:
Why there is no one-size-fits-all way to automate with Claude
Level 1: turning a prompt you run every week into a reusable skill
Level 2: scheduling that skill to run on your own machine with Cowork
Level 3: moving scheduled work to the cloud so it runs with your laptop closed
Level 4: firing cloud routines from webhooks (Fireflies, Calendly, Stripe, HubSpot)
Level 5: when Managed Agents are the right tool, and when they are the wrong one
The exact webhook shape Claude routines require, and why Make still sits in the middle
Which workflo

### 2. My Claude Code Can INSTANTLY Watch Any Video (Here's How)

Watch Skill on GitHub (FREE): https://github.com/bradautomates/clau...

AI Strategy Call: https://cal.com/bradley-bonanno/ai-st...
Connect with Me:   / bradbonanno  
Skills Marketplace Waitlist: https://brad-b.kit.com/f9a7349a1c

Claude Code can't watch video. Anthropic still has not shipped a video model, so by default Claude is blind to anything that lives inside an mp4, a YouTube link, an Instagram reel, or a Loom. Every other transcript tool I tried before this one only ever read the words and missed half of what was actually on screen, which is where most of the interesting stuff in a video lives. This Claude skill fixes that by handing Claude both the frames and the timestamped transcript at once, so it can actually watch any video, not just read its captions.

In this Claude Code tutorial I walk you through the exact pipeline behind the skill. yt-dlp pulls the file from any of over a thousand sites it supports. ffmpeg slices the video into frames and a clean audio track. Free YouTube captions come in straight from the source when they exist, and Groq Whisper fills the gap when they don't. I run a 45 minute lecture through it in under two minutes, walk through the cost math (about a dollar per run, transcription almost always free on Groq's tier), and finish on the use case that actually changed how I consume content: feeding every video I would have watched manually straight into my Obsidian second brain.

Whether you make YouTube content, run a research-heavy job, man

## Notes
- Fetched via Apify `streamers/youtube-scraper`
- Date format may be relative ('3 days ago') depending on actor output
- For deeper ingest of any single video, fetch its transcript and drop in raw/youtube/<channel>/<slug>.md
