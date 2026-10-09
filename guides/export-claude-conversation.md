---
title: How to export a Claude conversation to Markdown, PDF or Obsidian
description: Save a Claude.ai chat as a Markdown file with its artifacts, code and math intact, or send all your Claude chats to an Obsidian vault. Built-in options and a one-click extension compared.
---

# How to export a Claude conversation

Claude.ai has no button that saves one conversation as a file. If you want a chat in your notes, your repo or an Obsidian vault, these are the options that work today.

## Option 1: Claude's account data export

In Claude's settings, the Privacy section has an Export data option. Anthropic emails you a download link to a zip of your account data, with your conversations as JSON.

- **Good for:** a full backup.
- **Not good for:** reading or reusing one chat. It is every conversation at once, as raw JSON that needs a script before it is readable, and it arrives by email rather than straight away.

## Option 2: copy and paste

Each Claude reply has a copy button, and you can select text by hand.

- **Good for:** one reply.
- **Not good for:** a whole chat. You copy each turn yourself and lose who said what, and artifacts (the code or documents Claude writes in the side panel) have to be copied separately.

## Option 3: an exporter extension

**Tidyleaf AI Chat Exporter** adds an Export button to claude.ai (and to ChatGPT and Gemini). Disclosure: Tidyleaf is us, and this is our product.

Free:

- Exports the open Claude conversation to **Markdown, plain text, JSON or PDF**.
- Asks claude.ai for the conversation the same way Claude's own page does, with your existing login, so you get the **full active branch of the chat with its attachments and artifacts**, not just the part on screen.
- Labels every message User or Assistant, keeps code blocks with their language tag, and keeps LaTeX math as source between `$` and `$$`.
- Copies the whole chat as Markdown, or one message with "Copy MD".

**Tidyleaf Pro** ($24 a year or $3.99 a month, one key for every Tidyleaf extension):

- **Bulk export:** every Claude chat as its own Markdown file, in one zip. Large accounts take a few minutes, because the extension fetches chats one at a time and pauses between them; keep the tab open until the zip downloads. Anything it could not fetch is listed in a text file inside the zip.
- **Obsidian export:** Markdown with YAML properties at the top (title, provider, model when the site reports it, created date, URL, tags), ready to drop into a vault.
- **Notion export:** Markdown that imports as a page through Notion's Import, Text & Markdown. A bulk zip imports in one go.

Your conversations never leave your computer: there is no server, no account and no analytics. The only request to another site is the Pro license key check with our payment provider, Polar. Details are in the [privacy policy](../chat-exporter/privacy).

**Tidyleaf AI Chat Exporter is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf AI Chat Exporter once it is approved. -->

## Claude chats into Obsidian, step by step

1. Open the Claude conversation you want.
2. Click Export, then Obsidian (Pro).
3. Move the downloaded `.md` file into your vault. Obsidian reads the YAML block at the top as note properties, so you can filter chats by provider, date or tag.

For your whole history, use bulk export, unzip it, and drop its `Claude` folder into the vault.

## FAQ

**Does it include artifacts?**
Yes, on Claude the export reads the conversation from the site's own conversation data, which carries the artifacts, so they come out with the chat.

**Will my exported file show which Claude model answered?**
In the Obsidian export, the model goes into the properties when the site reports it. If the site does not say, the field is left out rather than guessed.

**What about ChatGPT and Gemini?**
Same extension, same formats. See [how to export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Anthropic. Claude is a trademark of Anthropic, named only to describe the site the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Does it include artifacts?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, on Claude the export reads the conversation from the site's own conversation data, which carries the artifacts, so they come out with the chat."
      }
    },
    {
      "@type": "Question",
      "name": "Will my exported file show which Claude model answered?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "In the Obsidian export, the model goes into the properties when the site reports it. If the site does not say, the field is left out rather than guessed."
      }
    },
    {
      "@type": "Question",
      "name": "What about ChatGPT and Gemini?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Same extension, same formats. See how to export a ChatGPT conversation to Markdown."
      }
    }
  ]
}
</script>
