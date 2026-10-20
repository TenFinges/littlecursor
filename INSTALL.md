# Installing LittleCursor (public beta)

Works on any Mac (Apple Silicon or Intel) running **macOS 14 Sonoma or newer**. Free. You bring a free Gemini key from Google.

## 1. Install
1. Download `LittleCursor-<version>.zip` from the [latest release](https://github.com/TenFinges/littlecursor/releases/latest) and unzip it.
2. Drag **LittleCursor.app** into your **Applications** folder. (Do this first. Opening it from Downloads causes permission trouble.)
3. Open it. This beta isn't signed by Apple yet, so macOS blocks it the first time:
   - Click **Done** on the warning, then open **System Settings → Privacy & Security**, scroll down and click **Open Anyway** next to "LittleCursor", and confirm with your password.
   - *(Or in Terminal: `xattr -dr com.apple.quarantine /Applications/LittleCursor.app`, then open it normally.)*

LittleCursor lives in the **menu bar** (a cursor icon, top right). It has no Dock icon.

## 2. Set up (the welcome tour walks you through it)
1. **Gemini key**: click "Get a free key (I'll show you how)" and it guides you through Google AI Studio, or paste a key you already have from <https://aistudio.google.com/apikey>.
   - Already pay for Claude Pro/Max and have Claude Code installed? Settings → Account → "Use my Claude plan" works instead.
2. **Permissions**: grant what you want to use. Each is explained when asked.
   - Screen Recording: lets it see your screen when you ask (then click **Relaunch**)
   - Microphone and Speech Recognition: voice questions and dictation
   - Accessibility: typing dictation and drafts into other apps (optional)

It only looks at your screen and listens while you're asking something.

## 3. Use it
- **⌥ Space**: ask about whatever's on screen. "This" or "here" means what your mouse is on.
- **⌥ ⇧ T**: type a question instead.
- Hold **⌃ ⌥** and move the mouse to circle something while you talk.
- Hold **fn ⌃** to dictate into any app.
- **Esc** interrupts. Every shortcut can be changed in Settings → Shortcuts.

## Updates
When a new version is out, the menu bar menu shows **Update Available**. Click it, download the new zip, and replace the app in Applications (quit LittleCursor first). Your settings and key are kept.

## Problems?
Menu bar → Settings → About → **Report a bug** opens a GitHub issue with recent (content-free) log lines filled in. Read it before posting: issues are public.

## Uninstall
Quit it from the menu bar, delete it from Applications, and (to remove all data) delete `~/Library/Application Support/AICursor` and `~/Library/Logs/AICursor.log`.
