# Privacy

Last updated: 2026-10-21. This is what the app actually does.

## In short
- LittleCursor sees your screen and hears you **only while you're asking something**.
- **No analytics, no tracking, no account.**
- Your screen, voice, questions and answers are **never stored** on our server.

## Where your question goes

| You use | Your screenshot + question go to |
|---|---|
| Free AI (default) | Our server (a Cloudflare Worker), which passes them to Google Gemini and back. Nothing is kept. |
| Your Claude plan | Straight from your Mac to Anthropic, through Claude Code. Never our server. |
| Your own Gemini key | Straight from your Mac to Google. Never our server. |

Each question sends: a screenshot (plus a close-up near your cursor), your question (text, or a short audio clip and its transcript), and recent conversation and project notes as context. The app asks Google not to store requests (`store: false`).

**Free-tier note:** the free AI runs on Google's free tier, where Google may use content to improve its products. If that matters to you, use your own paid Gemini key or your Claude plan.

## What our server keeps
- An anonymous install token and how many questions it used this month. Delete it any time: **Settings → Account → Delete account**.
- A keyed hash of your IP address (never the address itself): when an install first starts, to stop endless free installs, and with a count of free-AI questions from your network that day, so one network can't use up everyone's free AI. Deleted after two to three days.

## What stays on your Mac
In `~/Library/Application Support/AICursor/`: settings, your install token, your Gemini key (readable only by your user), recent conversation (text only, last 24 turns per project), project notes, agent files and usage counts.

Text on your screen is read **on your Mac** (Apple's Vision). Screenshots and audio are not saved, except a screenshot you hand to an agent, kept in that agent's folder. The log (`~/Library/Logs/AICursor.log`) has timings and errors, never what you say or type.

## Other connections
Once a day the app asks GitHub whether a new version exists, and downloads it if so. Nothing about you is sent.

## Delete your data
**Settings → Privacy** erases each kind of local data. **Settings → About → Uninstall** removes everything.

Questions? [Open an issue](https://github.com/TenFinges/littlecursor/issues/new).
