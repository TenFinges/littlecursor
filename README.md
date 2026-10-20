# LittleCursor

An AI that sits by your cursor on your Mac. Press **⌥ Space**, ask about whatever's on screen, and it answers right there, drawing boxes and arrows on your screen as it explains. It can also take dictation into any app and run longer jobs in the background.

**[⬇ Download the latest version](https://github.com/TenFinges/littlecursor/releases/latest)** · macOS 14+ · Apple Silicon and Intel · free public beta

## Install
Unzip, drag **LittleCursor.app** to Applications, and open it. The beta isn't signed by Apple yet, so the first time macOS blocks it: go to **System Settings → Privacy & Security → Open Anyway**. Full steps: [INSTALL.md](INSTALL.md).

You'll need a free Gemini API key from Google (the welcome tour walks you through getting one in about a minute), or a Claude Pro/Max plan with Claude Code installed.

## Privacy
Your screen is only captured when you ask something, and it goes straight from your Mac to the model you chose (Google Gemini with your own key, or Claude Code). There's no LittleCursor server in this beta. Details: [PRIVACY.md](PRIVACY.md).

## Feedback and bugs
[Open an issue](https://github.com/TenFinges/littlecursor/issues/new), or use Settings → About → Report a bug in the app.

This repository holds releases only; the source isn't public.
