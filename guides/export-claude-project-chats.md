---
title: "How to export all chats in a Claude project (2026)"
description: "Claude has no per-project export. Compare the account export, one-by-one export and project knowledge, with steps to get a project's chats as Markdown files."
---

# How to export all chats in a Claude project

Claude has no button that exports the chats of one project. Its built-in export (Settings, Privacy, Export data) covers your whole account, and Anthropic's help page does not say it separates projects. To get one project's chats, open each chat in the project, export it on its own, and collect the files in one folder.

## Why a project is awkward to export

Anthropic's help page describes projects as self-contained workspaces with their own chat histories and knowledge bases (the files and text you add, plus project instructions). Neither that page nor the page on managing projects mentions any export. So there are two things you might want out of a project: the chats inside it, which is what most people mean, and the knowledge files and instructions you put in. The chats are the hard part.

## Route 1: the account export (everything, not one project)

From Anthropic's help page:

1. Click your initials in the lower-left corner and choose **Settings**.
2. Open **Privacy** and click **Export data**.
3. A download link is emailed to the address on your account. You must be signed in to use it, and it expires 24 hours after delivery. If it lapses, request a new export.

The export runs from the web app or Claude Desktop, not from the iOS or Android app. Individual users on Free, Pro and Max plans can export; on Team and Enterprise plans only the organization's Primary Owner can. The help page says it contains your conversation data and user data, but gives no file format and does not mention projects. People who have opened the zip describe JSON files, with conversations in a `conversations.json`.

**Can you filter that JSON down to one project?** The common suggestion is to look for a project ID on each conversation and keep the matches. We could not confirm it: third-party write-ups disagree, and some say conversations carry no project link at all. Before you script anything, open your own `conversations.json` and search for "project". If there is such a field, filtering is a few lines of code. If not, the export cannot tell you which chat belongs to which project. Either way the result is raw JSON that needs a script before it reads like a conversation.

- **Good for:** a full account backup.
- **Not good for:** one project's chats, unless your export carries a project field and you are comfortable scripting.

## Route 2: export each chat in the project, one at a time

Claude has no per-chat download, so this route uses a browser extension that saves the open conversation to a file. The project itself tells you which chats belong together, which is the information the account export may lack. It takes a minute or two per chat, so it suits a project with up to a few dozen chats.

1. Open the project in claude.ai and find its chat history.
2. Make a folder on your computer for the project, for example `claude-project-pricing`.
3. Open the first chat in the project.
4. Export it as Markdown (with the extension below: Export, then Markdown).
5. Move the file into your folder. A date prefix, such as `2026-03-02 pricing review.md`, keeps the folder in order.
6. Go back to the project and repeat for the next chat until you have them all.

- **Good for:** a correct set of the project's chats, since you choose what goes in the folder.
- **Not good for:** projects with hundreds of chats. It is manual.

Several exporter extensions can do step 4, ours among them (below). For a large project, look for one that reads project membership: the Firefox add-on [Claude Exporter](https://addons.mozilla.org/addon/claude-exporter/) says it can organize and sort conversations by project and bulk-export all or filtered conversations as a zip. Its listing does not say whether the filter includes project, so test it on a small project first.

## Route 3: project knowledge (not an export)

You can go the other way and put what you need into the project. Anthropic's help page says you can upload documents, text, code and other files to a project's knowledge base. Export a few key chats as Markdown (Route 2) and upload them, and new chats in the project can draw on them. This carries old chats forward inside the project; it gets nothing out, so do not treat it as a backup.

Asking Claude to summarize the project into a document is quicker, but the result is a model-written summary, not a record of what was said, so details are lost and may be wrong.

## Doing Route 2 with Tidyleaf AI Chat Exporter

Disclosure: Tidyleaf is us, and this is our product. It is a browser extension for exporting chats from claude.ai, ChatGPT and Gemini.

On Claude, the free version:

- Exports the **open chat** to **Markdown, plain text, JSON or PDF**. PDF opens a clean print view where you choose "Save as PDF".
- Asks claude.ai for the conversation the way Claude's own page does, with your existing login, so you get the **full active branch of the chat with its attachments and artifacts**, not only what is on screen.
- Labels every message **User** or **Assistant**, keeps **code blocks with their language tag**, and keeps LaTeX math as source.
- Copies the whole chat as Markdown, or a single message with **Copy MD**.

That is all Route 2 needs: open a project chat, click Export, choose Markdown, and move the file into your folder.

**Tidyleaf Pro** is $24 a year or $3.99 a month, and one key unlocks Pro in every Tidyleaf extension. Its **bulk export** saves every Claude chat in your account as one zip, one Markdown file per conversation. That is all your chats, **not a single project**: it does not filter by project. It still saves time if you want everything and will sort it afterwards against the project's chat list. Large accounts take a few minutes, because it fetches chats one at a time and pauses between requests, and anything it could not fetch is listed in a text file inside the zip. Pro also adds Obsidian export (Markdown with YAML properties) and Notion-ready export. [Get Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf).

The extension runs in your browser and writes files to your computer. There is no Tidyleaf server, account or analytics, and your chats are not uploaded. The only thing that leaves your browser is a Pro license key, if you enter one, which goes to our payment provider Polar to be checked. See the [privacy policy](../chat-exporter/privacy).

**[Add to Chrome, free](https://chromewebstore.google.com/detail/belnajbhkcmnjjmmaibpahakpgpcpkip)** Tidyleaf AI Chat Exporter is on the Chrome Web Store.

More on the extension: [Tidyleaf AI Chat Exporter](../ai-chat-exporter).

## Which route should you use?

| You want | Use | Result |
|---|---|---|
| A backup of the whole account | Account export | JSON in a zip, by email |
| One project's chats as readable files | Export each chat, one at a time | A folder of .md files |
| Everything, to sort later | Bulk export (Tidyleaf Pro) | One zip, one .md per chat |
| Old chats available to new chats | Upload Markdown to project knowledge | Files in the project |

## FAQ

**Can I export an entire Claude project at once?**
Not with anything Claude provides. The account export covers your whole account, and its help page does not say it separates projects. To get one project's chats, export them one at a time from the project, or export everything and sort the files yourself.

**Is there a project ID in the Claude export I can filter by?**
We could not confirm it. Some write-ups say conversations carry no project field, so there would be nothing to filter on. Open your own conversations.json and search for "project" before relying on it, because the export format can change.

**Does the Claude data export include project files and instructions?**
Anthropic's help page does not say. Some third-party descriptions say it includes project names, instructions and documents. To be safe, copy your project instructions and download your knowledge files yourself while you still have access.

**How do I keep the exported chats in order?**
Name each file with the date and the chat title, and keep one folder per project. A date prefix sorts the files in order, and Obsidian can open the folder as a vault.

Related: [export a Claude conversation](export-claude-conversation), [search old Claude chats](search-old-claude-chats), [export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Anthropic. Claude is a trademark of Anthropic, PBC, named only to describe the site the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can I export an entire Claude project at once?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Not with anything Claude provides. The account export covers your whole account, and its help page does not say it separates projects. To get one project's chats, export them one at a time from the project, or export everything and sort the files yourself."
      }
    },
    {
      "@type": "Question",
      "name": "Is there a project ID in the Claude export I can filter by?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "We could not confirm it. Some write-ups say conversations carry no project field, so there would be nothing to filter on. Open your own conversations.json and search for \"project\" before relying on it, because the export format can change."
      }
    },
    {
      "@type": "Question",
      "name": "Does the Claude data export include project files and instructions?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Anthropic's help page does not say. Some third-party descriptions say it includes project names, instructions and documents. To be safe, copy your project instructions and download your knowledge files yourself while you still have access."
      }
    },
    {
      "@type": "Question",
      "name": "How do I keep the exported chats in order?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Name each file with the date and the chat title, and keep one folder per project. A date prefix sorts the files in order, and Obsidian can open the folder as a vault."
      }
    }
  ]
}
</script>
