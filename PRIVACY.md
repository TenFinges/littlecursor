# LittleCursor privacy (public beta)

Last updated: 2026-10-20. This describes what the beta app actually does.

## The short version
- LittleCursor looks at your screen and listens **only while you're asking something**.
- In this beta there is **no LittleCursor server and no account**. Your questions go straight from your Mac to the AI provider you set up. We (the developer) never receive your screen, voice, questions or answers.
- There is **no analytics or telemetry**.

## What goes where
| What | When | Where it goes |
|---|---|---|
| A screenshot of your screen (and a close-up near your cursor) | Each time you ask a question | The AI provider, for that one answer |
| Your question (typed, or a short audio clip + transcript) | Each question | The AI provider |
| Recent conversation and your project notes | Each question, as context | The AI provider |
| Text on screen (read on your Mac with Apple's Vision) | Each question | Stays on your Mac, except text you select in Click & Type |
| A version check | Once a day | GitHub (`api.github.com`), to see if a new version exists. Nothing about you is sent beyond a normal web request. |

**AI providers.** With your own Gemini key, requests go to Google (`generativelanguage.googleapis.com`) under your key and [Google's terms](https://ai.google.dev/gemini-api/terms); the app asks Google not to store the interaction (`store: false`). Note that on Google's free tier, Google may use content to improve its products. If you choose "Use my Claude plan", requests go through the Claude Code app on your Mac to Anthropic under your own Claude login and Anthropic's terms.

## What stays on your Mac
In `~/Library/Application Support/AICursor/`: settings, your Gemini key (in a file only your user can read; it moves to the macOS Keychain once the app is signed by Apple), recent conversation (text only, last 24 turns per project), project notes, agent files and monthly usage counts. The log at `~/Library/Logs/AICursor.log` records timings and errors, not what you say or type.

Screenshots and audio are not saved (except a screenshot an agent was asked to work from, kept in that agent's folder).

## Deleting your data
Settings → Privacy erases each kind of local data. To remove everything, delete the app, `~/Library/Application Support/AICursor` and `~/Library/Logs/AICursor.log`.

## Contact
Questions: [open an issue](https://github.com/TenFinges/littlecursor/issues/new).
