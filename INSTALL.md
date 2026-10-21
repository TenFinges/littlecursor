# Installing LittleCursor (public beta)

Works on any Mac (Apple Silicon or Intel) running **macOS 14 Sonoma or newer**. Free, and nothing to sign up for.

## 1. Install
1. Download `LittleCursor-<version>.zip` from the [latest release](https://github.com/TenFinges/littlecursor/releases/latest) and unzip it.
2. Drag **LittleCursor.app** into your **Applications** folder. (Do this first. Opening it from Downloads causes permission trouble.)
3. Open it. This beta isn't signed by Apple yet, so macOS blocks it the first time:
   - Click **Done** on the warning, then open **System Settings → Privacy & Security**, scroll down and click **Open Anyway** next to "LittleCursor", and confirm with your password.
   - *(Or in Terminal: `xattr -dr com.apple.quarantine /Applications/LittleCursor.app`, then open it normally.)*

LittleCursor shows up in the **Dock** and the **menu bar** (a cursor icon, top right). Click the Dock icon for Settings; right-click it for Talk, Home, Uninstall and Quit.

## 2. Set up (the welcome tour walks you through it)
1. **Start free**: LittleCursor uses its own free AI, so there's no key and no account (150 questions a month).
   - Have Claude Code installed and signed in? The tour offers "Use my Claude plan instead".
   - Have your own Gemini key? "I have my own Gemini key" makes it unlimited.
2. **Permissions**: grant what you want to use. Each is explained when asked.
   - Screen Recording: lets it see your screen when you ask (then click **Relaunch**)
   - Microphone and Speech Recognition: voice questions and dictation
   - Accessibility: typing dictation and drafts into other apps (optional)

It only looks at your screen and listens while you're asking something.

## Use your Claude plan (optional)
Have Claude Pro or Max? LittleCursor can answer with Claude through **Claude Code**, Anthropic's command-line tool (the Claude desktop app alone isn't enough):
1. In Terminal: `curl -fsSL https://claude.ai/install.sh | bash`
2. Run `claude` once and sign in with your Claude account, then quit it (`/exit`).
3. In LittleCursor: the welcome tour shows **Use my Claude plan instead**, or turn it on in Settings → Account → Use your Claude plan (click **Check again** if it says it isn't installed).

Answers then use your Claude plan's usage. Screenshots go from your Mac to Anthropic through Claude Code, never through LittleCursor's server.

## 3. Use it
- **⌥ Space**: ask about whatever's on screen. "This" or "here" means what your mouse is on.
- **⌥ ⇧ T**: type a question instead.
- Hold **⌃ ⌥** and move the mouse to circle something while you talk.
- Hold **fn ⌃** to dictate into any app.
- **Esc** interrupts. Every shortcut can be changed in Settings → Shortcuts.

## Updates
From 0.4.0 on, LittleCursor updates itself: it downloads new versions in the background and installs them the next time it quits. To update right away, choose **Restart to Update** in the menu bar menu. Your settings and permissions are kept.

On 0.3.x? Download 0.4.0 once from the [latest release](https://github.com/TenFinges/littlecursor/releases/latest) and replace the app in Applications (quit LittleCursor first). After that, updates are automatic.

## Problems?
Menu bar → Settings → About → **Report a bug** opens a GitHub issue with recent (content-free) log lines filled in. Read it before posting: issues are public.

## Quit
Any of these:
- Right-click the LittleCursor icon in the Dock and choose **Quit**.
- Press **⌘Q** in any LittleCursor window.
- Right-click the notch (or the small pill at the top of the screen) and choose **Quit LittleCursor**.
- Click **Quit** at the bottom of Settings, or the ⏻ button in Home (hover the notch).
- Menu bar icon → **Quit LittleCursor**.

Can't find any of them (the menu bar icon can hide behind the notch)? Double-click LittleCursor in Applications: while it's running, that opens Settings.

## Uninstall
Settings → About → **Uninstall LittleCursor…** quits it, moves it to the Bin and deletes everything it stored on your Mac.

(Dragging it to the Bin while it's running doesn't work: macOS says it's open. Quit it first. On 0.3.0, if you're stuck: open Terminal and run `killall AICursor`, then drag it to the Bin.)
