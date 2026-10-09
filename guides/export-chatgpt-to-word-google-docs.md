---
title: "Export ChatGPT, Claude or Gemini to Word or Google Docs without losing formatting"
description: "Export a ChatGPT, Claude or Gemini chat to Word or Google Docs with formatting intact: why copy-paste breaks tables, code and math, and two free Markdown routes."
---

# How to export a ChatGPT conversation to Word or Google Docs without losing formatting

Get the chat out as a Markdown file, then convert that file instead of pasting from the chat page. For a chat that is mostly prose and lists, open the `.md` file in Google Docs (**File**, **Open**, **Upload**) and download it as .docx. For a chat with tables, code or equations, convert it with the free tool Pandoc (`pandoc chat.md -o chat.docx`), which writes real Word tables, highlighted code blocks and Word equations. Both routes work the same for ChatGPT, Claude and Gemini.

## Why copy and paste breaks the formatting

Selecting a reply and pasting it into Word or Google Docs pastes a fragment of a web page, and the document app has to guess what each piece was. It guesses wrong in predictable places:

- **Tables** can arrive with odd column widths, as tab-separated lines, or as one run of text.
- **Code blocks** lose their fixed-width font and can lose indentation or line breaks, which can change what the code means.
- **Math** is drawn on the page from LaTeX source. What you copy may be the drawn symbols, a mix of symbols and source, or nothing usable.

Markdown avoids this because it is plain text with simple marks: `#` for headings, `**bold**`, `|` for table cells, triple backticks for code and `$...$` for math. Nothing is lost on the way to the file, and the converter only has to turn the marks into formatting.

## Step 1: get the chat out as Markdown

None of the three sites has a button that downloads one chat as a Markdown file. What they do offer:

| Site | Built-in route | What you get |
|---|---|---|
| ChatGPT | Copy under a reply; Settings, Data controls, Export data | One reply in your clipboard; a zip of your whole history by email |
| Claude | Copy a reply; Settings, Privacy, Export data | One reply in your clipboard; a download link to all your data by email |
| Gemini | **Share & export**, then **Export to Docs**, under a response | One response as a new Google Doc in your Drive |

Copying works one reply at a time, so a long chat means many copies and adding the speaker labels yourself. The account exports are backups of everything, not a document. Per-site details: [ChatGPT to Markdown](export-chatgpt-conversation-markdown), [Claude](export-claude-conversation) and [Gemini](export-gemini-conversation).

For one answer, paste it into a plain text editor, save it with a `.md` ending and go to step 2. For a whole conversation as one file, use an exporter extension (last section) or assemble the replies by hand.

For a single Gemini answer you can skip Markdown: **Export to Docs** creates the Google Doc directly. It covers only the response you clicked, so a whole chat means one Doc per answer.

## Step 2: open the Markdown in Google Docs

Google's help page on Markdown in Docs gives two ways in:

- **From Docs:** **File**, then **Open**, then **Upload**, and pick your `.md` file. It opens as a Google Doc.
- **From Drive:** upload the file, right-click it and choose **Open with**, then **Google Docs**.

Google lists what its Markdown support covers: bold, italics, bold italics, strikethrough, links and headings 1 to 6. Tables, code blocks and math are not on that list, so check them after import. For a chat that is mostly prose and lists, this route is quick and clean; for one that is mostly code or tables, use Pandoc.

## Step 3: download as .docx

In Google Docs, choose **File**, then **Download**, then **Microsoft Word (.docx)**.

## For tables, code and math: Pandoc (free)

[Pandoc](https://pandoc.org) is a free command-line converter. From Markdown it writes a .docx with real Word tables, code blocks in a fixed-width style with syntax highlighting when the block has a language tag, and `$...$` math as editable Word equations. After installing it, run:

```
pandoc chat.md -o chat.docx
```

Open `chat.docx` in Word, or upload it to Google Drive and open it with Google Docs to keep editing there. If a terminal is a dealbreaker, use the Google Docs route and fix tables and code by hand.

## Limits of the Markdown route

- **Images and attachments** are links or placeholders in Markdown, not embedded pictures.
- **Styling is yours to set.** The document uses default fonts and spacing.
- **The document is only as complete as your export.** Gemini loads long chats in pieces, so scroll to the top before exporting from the page.

## Option: an extension that exports the whole chat to Markdown

An exporter extension writes the whole open chat to one Markdown file in a click, which removes the one-reply-at-a-time copying. We built **Tidyleaf AI Chat Exporter** for this step. Disclosure: Tidyleaf is us, and this is our product.

Free, with no account:

- Works on **chatgpt.com, claude.ai and gemini.google.com**.
- Exports the open conversation to **Markdown, plain text, JSON or PDF**, with every message labelled **User** or **Assistant**.
- Keeps **code blocks with their language tag** and exact indentation, so Pandoc can highlight them.
- Writes tables, lists, headings, quotes and links as Markdown, and keeps **LaTeX math as source** between `$` and `$$`.
- Copies the whole chat as Markdown, or one message with **Copy MD**.

It does not write .docx or Google Docs files itself; take its Markdown through step 2 or Pandoc. **Tidyleaf Pro** ($24 a year or $3.99 a month) adds bulk export of all your ChatGPT or Claude chats as a zip of Markdown files, plus Obsidian and Notion formats; the free exports stay free. Exports run in your browser and your chats are not sent to Tidyleaf or anyone else; the only outside request is a Pro key check with our payment provider, Polar. See the [privacy policy](../chat-exporter/privacy).

**Tidyleaf AI Chat Exporter is coming to the Chrome Web Store; the listing is pending review.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf AI Chat Exporter once it is approved. -->

More on the extension: [Tidyleaf AI Chat Exporter](../ai-chat-exporter).

## Which route should you use?

| Your chat is mostly | Use |
|---|---|
| One answer, prose and lists | Copy, save as `.md`, open in Google Docs, download .docx |
| One Gemini answer | Export to Docs, then download .docx |
| Tables, code or equations | Markdown, then Pandoc |
| A whole conversation | An exporter to Markdown, then either route |

## FAQ

**Can ChatGPT export a conversation straight to Word?**

Not one chat at a time. ChatGPT's own export (Settings, Data controls, Export data) emails a zip of your whole history, and the copy action works one reply at a time. The free workaround is to get the chat as Markdown and convert it with Google Docs or Pandoc.

**Why do my tables turn into plain text when I paste into Word?**

The table on the chat page is web page layout, and Word has to guess what it was. Saving the table as a Markdown pipe table and converting it with Pandoc gives you a real Word table. Google's Markdown support list does not include tables, so check them if you import through Google Docs.

**Will code blocks keep their formatting in Google Docs?**

The code text and indentation come through Markdown, but Google's Markdown support list covers only headings, bold, italics, strikethrough and links. Expect to set a fixed-width font on code yourself, or use Pandoc, which writes code blocks with a code style and syntax highlighting.

**What happens to math equations?**

In Markdown they are LaTeX source between dollar signs, so nothing is lost on export. Google Docs' Markdown support does not list math, so expect the source text rather than an equation. Pandoc turns `$...$` math into editable Word equations, and you can upload that .docx to Google Docs afterwards.

**Does this work for Claude and Gemini as well as ChatGPT?**

Yes. Everything after getting the Markdown is the same for all three. Only step 1 differs, and Gemini also offers Export to Docs for a single response.

**Is the free route really free?**

Yes. Copying, Google Docs and Pandoc cost nothing, and Tidyleaf's single-chat Markdown export is free. Bulk export of every chat is Tidyleaf Pro.

## Related guides

- [Export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown)
- [Save a ChatGPT conversation as a PDF](save-chatgpt-conversation-pdf)
- [Export a Gemini chat](export-gemini-conversation)

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by OpenAI, Anthropic or Google. ChatGPT, Claude and Gemini are trademarks of their respective owners, named only to describe the sites the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can ChatGPT export a conversation straight to Word?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Not one chat at a time. ChatGPT's own export (Settings, Data controls, Export data) emails a zip of your whole history, and the copy action works one reply at a time. The free workaround is to get the chat as Markdown and convert it with Google Docs or Pandoc."
      }
    },
    {
      "@type": "Question",
      "name": "Why do my tables turn into plain text when I paste into Word?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The table on the chat page is web page layout, and Word has to guess what it was. Saving the table as a Markdown pipe table and converting it with Pandoc gives you a real Word table. Google's Markdown support list does not include tables, so check them if you import through Google Docs."
      }
    },
    {
      "@type": "Question",
      "name": "Will code blocks keep their formatting in Google Docs?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The code text and indentation come through Markdown, but Google's Markdown support list covers only headings, bold, italics, strikethrough and links. Expect to set a fixed-width font on code yourself, or use Pandoc, which writes code blocks with a code style and syntax highlighting."
      }
    },
    {
      "@type": "Question",
      "name": "What happens to math equations?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "In Markdown they are LaTeX source between dollar signs, so nothing is lost on export. Google Docs' Markdown support does not list math, so expect the source text rather than an equation. Pandoc turns $...$ math into editable Word equations, and you can upload that .docx to Google Docs afterwards."
      }
    },
    {
      "@type": "Question",
      "name": "Does this work for Claude and Gemini as well as ChatGPT?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Everything after getting the Markdown is the same for all three. Only step 1 differs, and Gemini also offers Export to Docs for a single response."
      }
    },
    {
      "@type": "Question",
      "name": "Is the free route really free?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Copying, Google Docs and Pandoc cost nothing, and Tidyleaf's single-chat Markdown export is free. Bulk export of every chat is Tidyleaf Pro."
      }
    }
  ]
}
</script>
