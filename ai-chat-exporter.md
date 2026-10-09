---
title: "Export ChatGPT, Claude and Gemini Chats: One Extension"
description: Export ChatGPT, Claude and Gemini chats to Markdown, PDF, text or JSON with one browser extension. Free, private, plus the built-in export options compared.
---

# Export ChatGPT, Claude and Gemini chats to Markdown or PDF

To export a single ChatGPT, Claude or Gemini conversation as a file, you need either the site's own account data export (every chat at once, as raw JSON or HTML, sent by email) or a browser extension that adds an Export button to the chat page. This page covers both, so you can pick the one that fits, and then describes our own extension, **Tidyleaf AI Chat Exporter**. Disclosure: Tidyleaf is us, and this is our product.

## What each site offers without an extension

None of the three sites has a "download this conversation" button. Each one does let you take your data out in some form:

| Site | Built-in option | What you get | Limits |
|---|---|---|---|
| ChatGPT | Settings, Data controls, Export data | A zip by email with `conversations.json` and a `chat.html` page | Every chat at once; the JSON needs a script to become readable; no Markdown |
| Claude | Settings, Privacy, Export data | A zip by email with your conversations as JSON | Every chat at once, raw JSON, not straight away |
| Gemini | Google Takeout (My Activity, then Gemini Apps), or Share & export, Export to Docs under one answer | Your activity history as a download, or one response in a Doc | Takeout is a history log, not tidy per-chat files; the Docs option covers one answer, not the whole chat |
| All three | Copy button on each reply, or select and paste | Text in your clipboard | One message at a time; you add who said what yourself, and formatting is often lost |

These are fine for a full backup or a single answer. They are awkward when you want one whole conversation as a clean `.md` or PDF, or when you use more than one of these assistants and want the same format from each.

## What to look for in a chat exporter extension

Several extensions add an export button to these sites. Whichever you try, check these points before trusting it with chats you care about:

1. **Which sites it covers.** Many exporters handle only ChatGPT. If you also use Claude or Gemini, one tool for all three gives you the same file format everywhere.
2. **Code blocks keep their language tag**, so `` ```python `` stays highlighted in your editor.
3. **Math stays as LaTeX source.** Some exporters save rendered math as Unicode symbols you cannot edit.
4. **Long chats come through complete.** An exporter that only reads what is on screen can miss messages that have not loaded.
5. **Where your chats go.** An exporter has to read your conversation to save it. Read its privacy policy and check whether anything is uploaded to the developer's server.

## Tidyleaf AI Chat Exporter

One extension for **chatgpt.com, claude.ai and gemini.google.com**. It adds an Export button on the right edge of the chat page, and the same actions are in the toolbar popup. No account and no sign-up.

### Free

- Export the open conversation to **Markdown, plain text, JSON or PDF**.
- Copy the whole chat as Markdown, or hover a single message and click **Copy MD**.
- Every message is labelled **User** or **Assistant**.
- **Code blocks** keep their language tag and exact indentation.
- Tables, lists, headings, quotes and links come through as proper Markdown.
- **LaTeX math is kept as source** between `$` and `$$`, so it pastes straight into Obsidian, Notion, Typora or a paper.
- Images and attachments become links or `[Attachment: name]` placeholders.
- PDF export opens a clean print view; choose "Save as PDF" in the print dialog.

### Tidyleaf Pro

Tidyleaf Pro is **$24 a year or $3.99 a month**, and one key unlocks Pro in every Tidyleaf extension. [Get Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf). The free exports above stay free.

- **Bulk export:** all your chats in one zip of Markdown files, one file per conversation, on chatgpt.com and claude.ai. Large accounts take a few minutes, because the extension fetches chats one at a time and pauses between requests; keep the tab open until the zip downloads. Anything it could not fetch is listed in a text file inside the zip.
- **Obsidian export:** Markdown with YAML properties at the top (title, provider, model when the site reports it, created date, URL, tags), ready to drop into a vault. Works for the open chat on all three sites, and for the bulk zip.
- **Notion export:** Markdown that imports as a page through Notion's Import, Text & Markdown. A bulk zip imports in one go.

Paste your key into the popup to unlock Pro. The key is checked at most once a day and keeps working for 7 days if you are offline. You can cancel any time from the [customer portal](https://polar.sh/data-gleaner/portal).

### How it reads each site

| | ChatGPT | Claude | Gemini |
|---|---|---|---|
| Single-chat export (free) | Yes | Yes | Yes |
| How the chat is read | Asks chatgpt.com for the conversation the way its own page does, with your login; falls back to the page | Same, on claude.ai, including attachments and artifacts | Reads the rendered page |
| Full active branch, not just what is on screen | Yes | Yes | Scroll to the top first, because Gemini loads long chats in pieces |
| Bulk export (Pro) | Yes | Yes | No: Gemini offers no stable way to list your chats |
| Obsidian and Notion export (Pro) | Yes | Yes | Yes, one chat at a time |

### Privacy, in plain words

Everything happens in your browser. The extension reads the conversation from the AI site you are already signed in to and saves the file to your computer. There is no Tidyleaf server, no analytics, no account and no tracking, and your chats are never uploaded. It asks only for the `storage` permission and access to chatgpt.com, claude.ai and gemini.google.com, and no other site. The one thing that leaves your browser is a Pro license key, if you enter one, which is sent to our payment provider Polar to check it. The full [privacy policy](chat-exporter/privacy) lists every request.

### Install

**Tidyleaf AI Chat Exporter is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf AI Chat Exporter once it is approved. -->

It needs Chrome 114 or later.

## Which option should you use?

| You want | Use |
|---|---|
| A backup of everything in one account | That site's own data export |
| One short answer in your notes | The copy button on that answer |
| One whole conversation as Markdown or PDF, from any of the three sites | An exporter extension (Tidyleaf AI Chat Exporter does this free) |
| Every ChatGPT or Claude chat as separate Markdown files, or in an Obsidian vault | An exporter with bulk export (Tidyleaf Pro) |

Step-by-step guides for each site: [export a ChatGPT conversation to Markdown](guides/export-chatgpt-conversation-markdown), [export a Claude conversation](guides/export-claude-conversation) and [export a Gemini conversation](guides/export-gemini-conversation).

## FAQ

**How do I export a Claude chat to PDF or Markdown?**
Claude has no per-chat download. Its account export (Settings, Privacy, Export data) emails you every conversation as JSON. For one chat as a file, use an exporter extension: open the chat on claude.ai, click Export and choose Markdown or PDF. For PDF, Tidyleaf opens a print view where you pick "Save as PDF".

**Can I export Gemini chats to Notion or Obsidian?**
Yes, one chat at a time. Free Markdown export already imports into either app. Tidyleaf Pro adds an Obsidian format with YAML properties and a Notion-ready format. Bulk export is not available for Gemini.

**Is there a bulk ChatGPT export extension?**
ChatGPT's own data export gives you every chat, but as one JSON file. Tidyleaf Pro exports every ChatGPT or Claude chat as its own Markdown file in a single zip.

**Does it work in Firefox or Edge?**
The Chrome version is in review first, and Firefox and Edge versions are being prepared. Check [tidyleaf.github.io](https://tidyleaf.github.io) for where it is available.

**Does the extension see my conversations?**
It has to read a conversation to save it, but it does that inside your browser and sends your chats nowhere. See the [privacy policy](chat-exporter/privacy).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by OpenAI, Anthropic or Google. ChatGPT, Claude and Gemini are trademarks of their respective owners, named only to describe the sites the extension works on.*
