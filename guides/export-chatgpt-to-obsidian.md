---
title: "How to export a ChatGPT conversation to Obsidian (one chat or all)"
description: "How to export a ChatGPT conversation to Obsidian: one chat as Markdown with front matter, or a bulk import from conversations.json, plus naming, tags and privacy."
---

# How to export a ChatGPT conversation to Obsidian

To export a ChatGPT conversation to Obsidian, save it as a Markdown (`.md`) file inside your vault folder. ChatGPT has no button for this, so there are two routes. For one chat, copy it or use an exporter extension to produce a `.md` file with a front matter block, and drop it in the vault. For your whole history, request ChatGPT's data export and convert its `conversations.json` into one note per chat. Both are below, followed by file naming, tags, linking and privacy.

The Obsidian half is easy: Obsidian stores notes as Markdown plain text files in a vault folder, so any `.md` file you save there shows up in the app. The hard part is getting good Markdown out of ChatGPT.

## Workflow 1: one chat into the vault

### Option A: copy and paste (free, built in)

Each ChatGPT answer has a copy button, or you can select the text by hand. Paste into a new note.

- **Good for:** a single short answer.
- **Not good for:** a whole conversation. You copy message by message, add who said what yourself, and write the front matter by hand. Code formatting and math are often lost.

### Option B: Obsidian Web Clipper (free)

Replies in the Obsidian forum thread [Exporting your ChatGPT conversations to Obsidian](https://forum.obsidian.md/t/exporting-your-chatgpt-conversations-to-obsidian/104172) say Obsidian's official Web Clipper can clip ChatGPT and Claude chats. We have not tested it on long chats, code or math, so try one conversation first.

### Option C: an exporter extension (the whole chat, one click)

An extension adds an Export button to chatgpt.com and writes the open conversation to a file. We cover ours, Tidyleaf AI Chat Exporter, in its own section below. Whichever one you pick, check four things in the output:

1. **Code fences keep the language**, so `` ```python `` is highlighted in Obsidian.
2. **Math stays as LaTeX** between `$` and `$$`, which Obsidian renders, instead of a jumble of Unicode.
3. **Speakers are labelled**, so you can tell your prompt from the answer.
4. **The whole conversation comes through**, not just the part on screen.

## Workflow 2: all your chats, from conversations.json

### Step 1: request ChatGPT's data export

In ChatGPT, open your profile menu, then **Settings**, **Data controls**, and under **Export data** select **Export**, then **Confirm export**. OpenAI's [help page](https://help.openai.com/en/articles/7260999-exporting-your-chatgpt-history-and-data) says the export can take up to 7 days, arrives by email (or SMS for phone-only accounts), and the download link expires 24 hours after you receive it. Self-service export is not available in ChatGPT Business, Enterprise or Healthcare workspaces. The ZIP holds your chat history as a `conversations.json` file and a `chat.html` page.

### Step 2: turn the JSON into notes

This is where the built-in route stops. `conversations.json` is one large file in which each conversation is a tree of message nodes, not a readable transcript, and `chat.html` is one long page with no Markdown. Neither can be dropped into a vault as it is.

The Obsidian forum thread linked above offers three ways to convert it:

- **A conversion script.** The thread's author shared a Node script that reads `conversations.json` and writes Markdown files into a folder you choose. It is free, but you need Node installed and run it from a terminal.
- **A community plugin.** Its developer recommends the Nexus AI Chat Importer plugin for importing ChatGPT and Claude exports, with attachments and artifacts. Check its page in Obsidian's community plugin browser for current details.
- **A Chrome extension** that saves the open conversation to the vault through `obsidian://` links, one chat at a time.

Read any script before you run it. After converting, spot-check a long chat, one with code and one with math.

## File naming that holds up

Chat titles are messy: duplicates, slashes, colons, question marks. A scheme that works:

- **Date first, then title:** `2026-10-09 Debugging a regex.md`. Notes sort by date in the file explorer, and two chats with the same title do not collide.
- **Avoid the characters Obsidian warns about.** Its help page says link text containing `#`, `|`, `^`, `:`, `%%`, `[[` or `]]` may not work as links. File systems also reject `\ / * ? " < >`, so drop those too.
- **Make duplicates unique.** If two chats share a date and a title, add a short suffix.

Tidyleaf's bulk export follows this scheme (see below); the same rules work on any script's output.

## Front matter and tags

Obsidian stores properties as YAML at the top of a note, between two `---` lines. Its three default properties are `tags`, `aliases` and `cssclasses`, and `tags` is a list. A useful block for a chat note looks like this:

```yaml
---
title: "Debugging a regex"
provider: "ChatGPT"
created: 2026-10-09
url: "https://chatgpt.com/c/..."
tags:
  - ai-chat
  - chatgpt
---
```

Why these fields:

- **`created`** lets you sort and filter chats by date, for example with a Bases view or a Dataview query if you use that plugin.
- **`url`** brings you back to the original chat if you want to continue it.
- **`provider`** (and `model`, if you record it) matters once you also keep Claude or Gemini chats in the same vault.
- **Tags:** start small. One shared tag such as `ai-chat`, plus one per provider, is enough. Add topic tags by hand later, on the chats you reuse; hundreds of auto-generated tags make the tag pane useless.

## Linking chats to the rest of your notes

A chat note is raw material. It becomes useful when other notes point to it.

- **Link from the note you are writing:** `[[2026-10-09 Debugging a regex]]`. Use a pipe to change the display text: `[[2026-10-09 Debugging a regex|the regex chat]]`.
- **Link to a section** with `[[Note name#Heading]]`. If your export turns each message into a `##` heading (User, Assistant), you can link straight to the answer you want.
- **Distill, do not hoard.** Pull the one useful answer into a permanent note and link back to the chat as the source. Keep chats in a folder such as `AI chats/` and add an index note per project.

## Keeping the vault private

Chats often hold names, work details, keys pasted by mistake and half-formed ideas. Before you import hundreds of them:

- **Notes are local files,** so privacy depends on where the vault goes next. If you sync with iCloud, Dropbox, OneDrive, Git or another third-party service, that service holds copies of your chats; if you use Obsidian Sync, read its own data-handling documentation.
- **Use a separate folder, or a separate vault,** for AI chats if the rest of your vault is shared or published. Obsidian recommends against creating a vault inside another vault, so make it a sibling vault rather than a subfolder.
- **If your vault is in Git,** decide first whether chats belong in the repository, especially a public one. Add the chat folder to `.gitignore` if not.
- **Search the notes for secrets** (API keys, passwords, tokens) before you sync or publish anything, and check that your converter runs on your machine rather than uploading chats.

## Option: Tidyleaf AI Chat Exporter

Disclosure: Tidyleaf is us, and this is our product.

Tidyleaf AI Chat Exporter is one extension for chatgpt.com, claude.ai and gemini.google.com. On ChatGPT it asks for the conversation the way ChatGPT's own page does, with your existing login, so you get the full active branch of the chat, not just what is on screen. Your chats are never uploaded: there is no Tidyleaf server, no account and no tracking. The only thing it sends anywhere is a Pro license key, if you enter one, to the payment provider Polar to check it.

**Free:** export the open chat to Markdown, plain text, JSON or PDF. Every message is labelled User or Assistant, code blocks keep their language tag, tables, lists and links become Markdown, and LaTeX math is kept as source between `$` and `$$`. That plain Markdown file already works in a vault, and you can paste in your own front matter.

**Tidyleaf Pro** ($24 a year or $3.99 a month, one key for every Tidyleaf extension) adds:

- **Obsidian export:** Markdown with YAML properties at the top (title, provider, model when the site reports it, created date, URL, exported date, and tags `ai-chat` plus the site name). It works for the open chat on all three sites and for the bulk zip.
- **Bulk export:** every ChatGPT or Claude chat as its own Markdown file in a single zip, named like `2026-10-09 Title.md`, with characters such as `/ : # | [ ]` removed and duplicate names numbered. Large accounts take a few minutes because chats are fetched one at a time; keep the tab open until the zip downloads. Anything it could not fetch is listed in a text file in the zip. This replaces the script and the wait for the data-export email. It is a paid feature and does not work on Gemini.

**[Add to Chrome, free](https://chromewebstore.google.com/detail/belnajbhkcmnjjmmaibpahakpgpcpkip)** Tidyleaf AI Chat Exporter is on the Chrome Web Store. It needs Chrome 114 or later.

More on the extension: [Tidyleaf AI Chat Exporter](../ai-chat-exporter).

## FAQ

**Can Obsidian import ChatGPT's conversations.json directly?**
No. Obsidian works with Markdown files, and `conversations.json` is one large file in which each chat is a tree of message nodes. Convert it to one Markdown note per chat first, with a script, a community plugin such as Nexus AI Chat Importer, or an exporter with bulk export.

**Will code blocks and LaTeX survive the export?**
They survive if the exporter keeps code fences with their language tag and leaves math as LaTeX source between `$` and `$$`. Check one chat with code and one with math before you convert everything.

**What should I put in the front matter of a ChatGPT note?**
A title, a created date, the chat URL and a short tags list are enough. Keep tags few and shared across chats, such as `ai-chat` and the provider name, and add topic tags by hand later.

**Is it safe to put my ChatGPT history in an Obsidian vault?**
Obsidian keeps notes as local files on your computer, so the risk is wherever the vault goes next: a sync service, a Git repository or a published site. Review chats for secrets and keep them in a folder or vault that you do not share.

## Related guides

- [Export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown)
- [Export a Claude conversation](export-claude-conversation)
- [Organize ChatGPT chats into folders](organize-chatgpt-chats-folders)

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by OpenAI or Obsidian. ChatGPT and Obsidian are trademarks of their respective owners, named only to describe the products the extension works with.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can Obsidian import ChatGPT's conversations.json directly?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Obsidian works with Markdown files, and conversations.json is one large file in which each chat is a tree of message nodes. Convert it to one Markdown note per chat first, with a script, a community plugin such as Nexus AI Chat Importer, or an exporter with bulk export."
      }
    },
    {
      "@type": "Question",
      "name": "Will code blocks and LaTeX survive the export?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "They survive if the exporter keeps code fences with their language tag and leaves math as LaTeX source between $ and $$. Check one chat with code and one with math before you convert everything."
      }
    },
    {
      "@type": "Question",
      "name": "What should I put in the front matter of a ChatGPT note?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "A title, a created date, the chat URL and a short tags list are enough. Keep tags few and shared across chats, such as ai-chat and the provider name, and add topic tags by hand later."
      }
    },
    {
      "@type": "Question",
      "name": "Is it safe to put my ChatGPT history in an Obsidian vault?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Obsidian keeps notes as local files on your computer, so the risk is wherever the vault goes next: a sync service, a Git repository or a published site. Review chats for secrets and keep them in a folder or vault that you do not share."
      }
    }
  ]
}
</script>
