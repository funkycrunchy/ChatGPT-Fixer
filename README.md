# ChatGPT Fixer

**Keep long ChatGPT conversations fast, responsive, and crash-free.**

ChatGPT Fixer solves a common problem with long-running ChatGPT conversations:  
as chats grow, the web app can become laggy, freeze when sending messages, or even crash entirely.

This extension keeps ChatGPT usable by limiting how much conversation history is loaded into your browser — while still letting you load older messages when you actually need them.

---

## Why this exists

If you’ve ever experienced any of the following, this extension is for you:

- Typing becomes laggy in long ChatGPT chats
- Clicking **Send** freezes the page
- Responses take ages because the tab becomes unresponsive
- Chrome asks if you want to “Exit page”
- Scrolling through old messages feels painfully slow

The cause is simple:  
**the ChatGPT web app loads the entire conversation into memory**, even when it’s thousands of messages long.

ChatGPT Fixer addresses that directly.

---

## What ChatGPT Fixer does

- Keeps only the **most recent messages** loaded in the page (default: 40)
- Prevents massive in-memory conversation state from slowing the UI
- Keeps typing and sending messages fast
- Lets you **load older messages on demand**, in controlled steps
- Allows a one-time **full history load** if you really need everything

Nothing is deleted. Everything is reversible.

---

## How it works (high level)

ChatGPT Fixer intercepts the conversation data as it loads in your browser and trims it down to a manageable size **before** the ChatGPT interface processes it.

This dramatically reduces:
- memory usage
- UI re-render work
- input lag
- tab freezes

All processing happens **locally in your browser**.

---

## Features

- ⚡ Dramatically improves performance in long chats
- 🧩 Clean, collapsible in-chat control panel
- ➕ Load older messages incrementally
- 🔄 Reset to fast default at any time
- 🧯 One-time “Full history” option
- 💾 Remembers your settings
- 🔐 No tracking, no analytics, no external servers

---

## What this extension does NOT do

- ❌ Does not delete your chats
- ❌ Does not modify server-side data
- ❌ Does not affect ChatGPT’s responses or intelligence
- ❌ Does not collect or transmit personal data

---

## Privacy

ChatGPT Fixer does **not** collect, track, or transmit any user data.

- No analytics
- No telemetry
- No remote servers
- Settings are stored locally using Chrome’s storage APIs

See [`PRIVACY.md`](./PRIVACY.md) for full details.

---

## Supported sites

The extension only runs on:
- https://chat.openai.com/*
- https://chatgpt.com/*

---

## Installation

### Chrome Web Store
(Once published)
- Install directly from the Chrome Web Store
- No configuration required — it works out of the box

### Local development
1. Clone this repository
2. Open `chrome://extensions`
3. Enable **Developer mode**
4. Click **Load unpacked**
5. Select the extension folder

---

## FAQ

### Does this make ChatGPT “forget” things?
No. This only affects how much history is loaded into your browser tab.  
ChatGPT’s server-side context and behavior are unchanged.

### Can I still see older messages?
Yes. Use the in-chat menu to load older messages in steps, or load full history once if needed.

### Is this safe to use?
Yes. The extension is fully client-side and open-source. You can inspect all code in this repository.

---

## Support / Issues

If something breaks after a ChatGPT update, or you have suggestions:

👉 Please open an issue on GitHub.

---

## License

MIT License
