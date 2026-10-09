---
title: How to find old Claude conversations (search, Projects, export)
description: "How to find old Claude conversations with title search, Claude's own chat search, Projects and data export, plus the limits of each and how to stay organized."
---

# How to find old Claude conversations

To find an old Claude conversation, open the chat list on claude.ai and search for words from its title. If you remember only what was said, not the title, and you are on a paid plan, ask Claude in a new chat ("find the chat where we planned the Lisbon trip"): it can search your past conversations and link back to them. If neither finds it, export your account data and search the files on your computer. Below are each of those ways, what each one misses, and how to set things up so you do not have to dig next time.

## 1. Search the chat list by title

Claude's sidebar has a link to all your chats, with a search box at the top. Type a few words from the chat's title and the list filters as you type. Claude names each chat itself from the opening messages, so search for the subject you started with, not a phrase from the middle of the chat.

- **Good for:** a chat whose topic you remember.
- **Limits:** it works from titles. A chat titled "Python script help" will not come up when you search for the one function name it contained. If you rename important chats (hover a chat, open its menu, Rename), this search gets much more reliable.

`Ctrl+F` (or `Cmd+F` on a Mac) only searches the chat that is open on screen, and only the part that has loaded, so it does not help you find a chat in your history.

## 2. Ask Claude to search your past chats

On paid plans (Pro, Max, Team and Enterprise), Claude can search your earlier conversations when you ask it to, on the web, the desktop app and the mobile apps. Start a new chat and describe what you are looking for, for example: "Find the conversation where we compared two job offers." Claude shows the search as a step in the reply and cites the chats it used, with links back to them.

- **Good for:** a chat you remember by its content, not its title.
- **Limits:**
  - Not on the free plan.
  - Outside a Project, it searches your chats that are not in any Project. Inside a Project, it searches only that Project's chats. If the chat you want is in a Project, ask from inside that Project.
  - It is a retrieval step, not a keyword index: it can miss chats or return a related one instead of the exact one. Ask again with a more specific detail (a name, a number, a date range) if the first answer is off.
  - It can be switched off. If Claude says it cannot search your chats, check Settings, then Capabilities, and turn on "Search and reference chats".

Anthropic's help article "Use Claude's chat search and memory to build on previous context" describes the current plan list and settings.

## 3. Look inside your Projects

Chats started inside a Project are listed on that Project's page, not mixed into your general history the same way. If a chat is missing from the main list, open Projects in the sidebar and check each likely Project. Going forward, a Project per client, course or ongoing piece of work is Claude's own way of grouping related chats.

## 4. Export your data and search the files

When the chat list and Claude's own search both fail, the most thorough option is the account export. In Settings, the Privacy section has Export data. Anthropic emails you a link to a zip that holds your conversations as JSON.

Once you have it, any text search finds a phrase across every chat, including words deep inside long conversations. On macOS or Linux, from the folder you unzipped:

```bash
grep -l -i "lisbon" conversations.json
```

That tells you the phrase is there; to see which chats it is in, this short Python script prints the title and date of every conversation that contains it:

```python
import json, sys

phrase = sys.argv[1].lower()
with open("conversations.json", encoding="utf-8") as f:
    chats = json.load(f)

for chat in chats:
    text = json.dumps(chat, ensure_ascii=False).lower()
    if phrase in text:
        print(chat.get("created_at", "")[:10], chat.get("name") or "(untitled)")
```

Run it as `python3 find_chat.py "lisbon"`. Then search for that title in Claude's chat list to open the live chat.

- **Good for:** an exhaustive search, and a backup you keep.
- **Limits:** the link arrives by email rather than straight away, it covers every chat at once, and the JSON needs a script like the one above to be readable. The field names in the export are Anthropic's and may change; if the script prints nothing, open the file and check what the conversation title field is called.

## What if the chat was deleted?

Claude has no trash folder for chats. A deleted conversation does not come back from the chat list or from Claude's search. Your only copy is one you saved before: an earlier data export, a file you exported yourself, or text you pasted elsewhere. If a chat matters, save it somewhere you control.

## How to stop losing Claude chats

The underlying problem is that Claude's history is one long list sorted by date. These habits keep it findable:

- **Rename** chats that you will want again, with the words you would search for.
- **Star** the chats you return to often. Starred chats sit above Recents in the sidebar.
- **Use Projects** for ongoing work, so related chats live in one place.
- **Save the important ones as files.** A Markdown copy of a chat in your notes can be searched with your own tools forever, whatever happens to your account. Our guide on [exporting a Claude conversation](export-claude-conversation) covers the ways to do that.

## A folders panel for Claude (and ChatGPT)

Stars and Projects go a long way, but Projects change how Claude answers (they share files and instructions), and stars are one flat list. If you want plain folders, we built **Tidyleaf Folders for ChatGPT and Claude**, a browser extension that adds a Folders section to the claude.ai sidebar, above Starred and Recents. Disclosure: Tidyleaf is us, and this is our product.

Free:

- Up to 5 folders, each with a color. Drag a chat from Claude's list onto a folder, or pick a folder for the open chat from a menu.
- Pins for the chats you keep coming back to.
- Instant search across all your chat titles, in any language, including Chinese, Japanese and Korean.
- The same folders work on chatgpt.com, so a Claude chat and a ChatGPT chat can sit in one folder.
- Deleting a folder never deletes a chat.

**Tidyleaf Pro** ($24 a year or $3.99 a month, one key for every Tidyleaf extension) adds **search inside messages**: you click "Index your messages" once, the extension reads your chats from claude.ai with your own login and keeps a search index on your device, and then you can find a chat by anything said in it, with the matching line shown under each result. A large account takes a few minutes to index, because the extension reads chats one at a time and pauses between them. Pro also adds unlimited folders and export of a whole folder as a zip of Markdown files. [Get Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf).

Your folders, pins and the message index stay in your browser. There is no server, no account and no analytics; the only request to another site is the Pro license key check with Polar. Details are in the [privacy policy](../chat-folders/privacy). It works on chatgpt.com and claude.ai; Gemini is not supported.

**Tidyleaf Folders for ChatGPT and Claude is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Folders for ChatGPT and Claude once it is approved. -->

## Which way should you use?

| You remember | Use | Plan |
|---|---|---|
| Roughly what the chat was titled | Search the chat list | Free and paid |
| What was discussed, not the title | Ask Claude to search your past chats | Pro, Max, Team, Enterprise |
| That it was part of ongoing work | Open the Project it belongs to | Free and paid |
| An exact phrase, and nothing else worked | Export your data and search the files | Free and paid |
| You want this never to happen again | Rename, star, Projects, or folders | Free and paid |

## FAQ

**Can you search Claude chats?**
Yes. The chat list has a search box that matches chat titles, on every plan. On paid plans you can also ask Claude to search the content of your past chats for you.

**Why can't Claude find my old chats?**
The usual reasons: you are on the free plan, where Claude cannot search past chats; "Search and reference chats" is turned off in Settings, Capabilities; you asked from outside a Project about a chat that lives inside one (or the other way round); or the chat was deleted. Claude's search can also simply miss, so try a more specific detail.

**Does Claude search all chats or only recent ones?**
When you ask it to, Claude searches your past conversations, not just recent ones, but within a scope: all chats outside Projects, or only the current Project's chats when you ask from inside a Project.

**Where did my Claude chat history go?**
If the list looks empty or short, check that you are signed in to the same account (a work and a personal account have separate histories), check your Projects, and scroll the full chat list rather than the sidebar's Recents. A chat you deleted cannot be restored.

**How do I find old Claude Code conversations?**
Claude Code is a separate tool and keeps its sessions on your own computer, not in the claude.ai chat list. In the terminal, `claude --resume` lists past sessions in the current project folder so you can pick one, and `claude --continue` reopens the most recent.

## Related

- [Tidyleaf Folders for ChatGPT and Claude](../chatgpt-claude-folders)
- [Tidyleaf AI Chat Exporter](../ai-chat-exporter): save a Claude chat as Markdown, PDF or text
- [How to organize ChatGPT chats into folders](organize-chatgpt-chats-folders)

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Anthropic. Claude is a trademark of Anthropic, named only to describe the site the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can you search Claude chats?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. The chat list has a search box that matches chat titles, on every plan. On paid plans you can also ask Claude to search the content of your past chats for you."
      }
    },
    {
      "@type": "Question",
      "name": "Why can't Claude find my old chats?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The usual reasons: you are on the free plan, where Claude cannot search past chats; \"Search and reference chats\" is turned off in Settings, Capabilities; you asked from outside a Project about a chat that lives inside one (or the other way round); or the chat was deleted. Claude's search can also simply miss, so try a more specific detail."
      }
    },
    {
      "@type": "Question",
      "name": "Does Claude search all chats or only recent ones?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "When you ask it to, Claude searches your past conversations, not just recent ones, but within a scope: all chats outside Projects, or only the current Project's chats when you ask from inside a Project."
      }
    },
    {
      "@type": "Question",
      "name": "Where did my Claude chat history go?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "If the list looks empty or short, check that you are signed in to the same account (a work and a personal account have separate histories), check your Projects, and scroll the full chat list rather than the sidebar's Recents. A chat you deleted cannot be restored."
      }
    },
    {
      "@type": "Question",
      "name": "How do I find old Claude Code conversations?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Claude Code is a separate tool and keeps its sessions on your own computer, not in the claude.ai chat list. In the terminal, claude --resume lists past sessions in the current project folder so you can pick one, and claude --continue reopens the most recent."
      }
    }
  ]
}
</script>
