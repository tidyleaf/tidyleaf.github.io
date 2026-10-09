---
title: How to export a ChatGPT conversation to Markdown (or PDF, text, JSON)
description: Three ways to save a ChatGPT chat as a Markdown file with code blocks, tables and math intact, from the built-in data export to a one-click browser extension.
---

# How to export a ChatGPT conversation to Markdown

ChatGPT has no button to download one conversation as a file. To get a single chat as a clean `.md` file, with headings, code blocks, tables and math intact, use an exporter extension. With nothing installed, you can request ChatGPT's full data export (JSON and HTML, not Markdown) or copy messages by hand. Each option is below, with what it is good and bad for.

## Option 1: ChatGPT's own data export (everything, but not Markdown)

In ChatGPT, open Settings, then Data controls, and under Export data choose Export, then confirm. Per OpenAI's help center, ChatGPT emails or texts you when the file is ready, which can take up to 7 days, and the download link expires 24 hours after it arrives. The zip holds every conversation you have ever had as `conversations.json` plus a `chat.html` page. Business and Enterprise workspaces have no self-service export; ask your workspace owner.

- **Good for:** a full backup of your account.
- **Not good for:** one chat as Markdown. You get every chat at once, and the JSON is a tree of message nodes that needs a script to turn into readable text. The HTML file is one long page with no Markdown.

## Option 2: copy and paste (one chat, by hand)

Select the conversation and paste it into your editor. Each answer also has its own copy button.

- **Good for:** a single short answer.
- **Not good for:** a whole conversation. You have to copy every message one by one and add who said what yourself, and selecting the page by hand loses the formatting.

## Option 3: an exporter extension (one click, the whole chat)

A browser extension can add an Export button to the chat page and write the whole conversation to a file. This is what we built **Tidyleaf AI Chat Exporter** for. Disclosure: Tidyleaf is us, and this is our product.

1. Open the conversation on chatgpt.com.
2. Click the Export button on the page, or the Tidyleaf icon in the browser toolbar.
3. Choose **Markdown** (or plain text, JSON or PDF). The file is saved to your downloads folder.

If the popup says it found no chat, reload the ChatGPT tab once and try again.

What it does, free:

- Exports the open conversation to **Markdown, plain text, JSON or PDF**, from an Export button on the page or the toolbar popup.
- Labels every message **User** or **Assistant**.
- Keeps **code blocks with their language tag** and exact indentation, and turns tables, lists, headings, quotes and links into proper Markdown.
- Keeps **LaTeX math as source** between `$` and `$$`, so it pastes straight into Obsidian, Notion, Typora or a paper.
- Turns images and attachments into links or `[Attachment: name]` placeholders.
- Can also copy the whole chat as Markdown, or a single message with "Copy MD".
- Works on **chatgpt.com, claude.ai and gemini.google.com**, with one extension.

On ChatGPT the extension asks the site for the conversation the same way ChatGPT's own page does, with your existing login, so you get the full active branch of the chat, not just what is on screen. Nothing is uploaded anywhere: there is no server, no account and no tracking. The only thing the extension ever sends elsewhere is a Pro license key, to our payment provider, to check it.

**Tidyleaf Pro** ($24 a year or $3.99 a month) adds a bulk export of all your ChatGPT or Claude chats as a zip of Markdown files, plus Obsidian export (Markdown with YAML properties: title, provider, model when the site reports it, created date, URL, tags) and Notion-ready export. The free exports above stay free.

**Tidyleaf AI Chat Exporter is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf AI Chat Exporter once it is approved. -->

## Which option should you use?

| You want | Use |
|---|---|
| A backup of every chat, any format | ChatGPT's data export |
| One short answer in your notes | The copy button on that answer |
| One whole conversation as a `.md` or PDF | An exporter extension |
| All your chats as separate Markdown files, or in an Obsidian vault | An exporter with bulk export (Tidyleaf Pro does this) |

## What a good Markdown export looks like

Check these four things in any exporter before you trust it with chats you care about:

1. **Code fences keep the language**, so `` ```python `` stays highlighted in your editor.
2. **Math stays as LaTeX.** Some exporters save the rendered math as a jumble of Unicode symbols that you cannot edit.
3. **Speakers are labelled**, so you can tell your prompt from the answer.
4. **Long chats come through complete.** An exporter that only reads the screen can miss messages that have not loaded yet.

## FAQ

**Is there an official way to export a single ChatGPT chat?**
Not as a file. The official route is the full data export, which covers every chat at once. ChatGPT's share link makes a web page others can open, not a file you keep.

**Does an exporter extension see my chats?**
It has to read the conversation to save it. Check where it sends it. Tidyleaf AI Chat Exporter writes the file on your computer and sends your conversation nowhere; its [privacy policy](../chat-exporter/privacy) lists the one request it makes to another site (the Pro key check).

**Can I export Claude and Gemini chats too?**
Yes, with the same extension. See [how to export a Claude conversation](export-claude-conversation). Gemini loads long chats in pieces, so scroll to the top before exporting to get everything. Bulk export is not available for Gemini.

**Can I turn the export into a PDF?**
Yes. Choose PDF; a clean print view opens, and you pick "Save as PDF" in the print dialog.

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by OpenAI. ChatGPT is a trademark of OpenAI, named only to describe the site the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Is there an official way to export a single ChatGPT chat?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Not as a file. The official route is the full data export, which covers every chat at once. ChatGPT's share link makes a web page others can open, not a file you keep."
      }
    },
    {
      "@type": "Question",
      "name": "Does an exporter extension see my chats?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "It has to read the conversation to save it. Check where it sends it. Tidyleaf AI Chat Exporter writes the file on your computer and sends your conversation nowhere; its privacy policy lists the one request it makes to another site (the Pro key check)."
      }
    },
    {
      "@type": "Question",
      "name": "Can I export Claude and Gemini chats too?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, with the same extension. See how to export a Claude conversation. Gemini loads long chats in pieces, so scroll to the top before exporting to get everything. Bulk export is not available for Gemini."
      }
    },
    {
      "@type": "Question",
      "name": "Can I turn the export into a PDF?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Choose PDF; a clean print view opens, and you pick \"Save as PDF\" in the print dialog."
      }
    }
  ]
}
</script>
