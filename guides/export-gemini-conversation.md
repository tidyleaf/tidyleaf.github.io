---
title: "How to export a Gemini chat (Docs, PDF, Markdown, Takeout)"
description: "How to export a Gemini chat: share links, Export to Docs, Google Takeout for your whole history, copy and print, and a one-click Markdown or PDF exporter."
---

# How to export a Gemini chat

Gemini has no button that saves a whole conversation as a file. For one answer, use **Share & export, then Export to Docs** under that response. For your whole history, use **Google Takeout** (My Activity, then Gemini Apps). For one complete chat as Markdown, text or PDF, print the page or use an exporter extension. Each option is below, with what it keeps and what it drops.

## Option 1: Export to Docs or Draft in Gmail (one response)

Under each Gemini response there is a **Share & export** button. It offers **Export to Docs**, which creates a new Google Doc in your Drive, and **Draft in Gmail**, which opens an email with the text.

- **Good for:** one answer you want to edit or send, with headings, lists and tables kept.
- **Not good for:** a whole conversation. The export is tied to the response you clicked, so a long chat means one Doc per answer, and your own prompts are not included as a back-and-forth. Once it is in Docs you can download it as .docx, PDF or plain text from File, then Download.

Google changes these menus from time to time, so the labels in your account may differ slightly.

## Option 2: a share link (to show someone, not to keep)

**Share & export, then Share** (or the share icon at the top of the chat) creates a public link at `g.co/gemini/share/...`. Anyone with the link can read the chat as it was when you shared it; messages you add later are not included.

- **Good for:** showing a conversation to a colleague.
- **Not good for:** keeping a copy. It is a web page on Google's servers, not a file you own, and you can delete it (or lose access to it) later. Anyone who has the link can read it, so check the chat for personal details first. You can manage your links in Gemini's settings under public links.

## Option 3: Google Takeout (your whole Gemini history)

Google Takeout exports every Gemini chat in your account at once:

1. Go to [takeout.google.com](https://takeout.google.com), signed in to the account you use for Gemini.
2. Click **Deselect all**.
3. Tick **My Activity**. Your chats are stored here. The separate "Gemini" entry holds your Gems, not your conversations.
4. Click **All activity data included**, then **Deselect all**, tick only **Gemini Apps** and click OK.
5. Optional: under **Multiple formats**, switch the activity format from HTML to JSON if you plan to process it with a script.
6. Click **Next step**, choose how to receive it (an emailed download link, or Drive, Dropbox, OneDrive or Box), keep the .zip file type and click **Create export**.

What you get: a file under `Takeout/My Activity/Gemini Apps/` (`MyActivity.html` or `.json`) that lists your prompts and Gemini's responses as activity entries, newest first.

Caveats:

- It is an activity log, not a set of tidy conversations. Entries are not grouped into one file per chat, so pulling out a single conversation takes searching or a script.
- If **Gemini Apps Activity** was turned off, those chats were not saved to your account and are not in Takeout.
- On a work or school (Google Workspace) account, your administrator may have turned Takeout or Gemini history off.
- It is not instant: Google says an export can take hours or even days to be ready.

## Option 4: copy, or print to PDF (no install)

- **Copy:** each response has a copy button that copies that answer. To get the whole chat, select the page by hand and paste it into a document. You lose the formatting of code and tables, and you have to mark who said what yourself.
- **Print to PDF:** open the chat, scroll to the top so the whole conversation has loaded, press Ctrl+P (Cmd+P on a Mac) and choose **Save as PDF**. This keeps what you see, but the sidebar and buttons often come along and long code blocks can be cut at the page edge.

## Option 5: an exporter extension (one whole chat, one click)

A browser extension can add an Export button to gemini.google.com and write the open conversation to a file. This is what we built **Tidyleaf AI Chat Exporter** for. Disclosure: Tidyleaf is us, and this is our product.

What it does on Gemini, free:

- Exports the open chat to **Markdown, plain text, JSON or PDF** (PDF through a clean print view, where you choose "Save as PDF").
- Labels every message **User** or **Assistant**, so your prompts and Gemini's answers stay in order in one file.
- Keeps **code blocks with their language tag**, turns tables, lists, headings, quotes and links into Markdown, and keeps **math as LaTeX** source.
- Copies the whole chat as Markdown, or one message with "Copy MD".
- Works on chatgpt.com and claude.ai too, with the same extension.

How it reads Gemini: from the page itself. Gemini loads long chats in pieces, so **scroll to the top of the chat before exporting** to get every message. Nothing is uploaded: there is no server, account or tracking, and the file is written on your computer. See the [privacy policy](../chat-exporter/privacy).

**Tidyleaf Pro** ($24 a year or $3.99 a month) adds Obsidian export (Markdown with YAML properties) and Notion-ready export for the open Gemini chat. Bulk export of all chats works on ChatGPT and Claude but **not on Gemini**, because Gemini offers no stable way to list your chats; for your whole Gemini history, use Takeout (Option 3). [Get Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf).

**[Add to Chrome, free](https://chromewebstore.google.com/detail/belnajbhkcmnjjmmaibpahakpgpcpkip)** Tidyleaf AI Chat Exporter is on the Chrome Web Store.

More on the extension: [Tidyleaf AI Chat Exporter](../ai-chat-exporter).

## Which option should you use?

| You want | Use | Format |
|---|---|---|
| One answer to edit or send | Export to Docs or Draft in Gmail | Google Doc (then .docx or PDF) |
| To show a chat to someone | Share link | Web page |
| A backup of every chat | Google Takeout | HTML or JSON activity log |
| One whole chat as a PDF, no install | Print to PDF | PDF |
| One whole chat as Markdown, text or a clean PDF | An exporter extension | .md, .txt, .json, PDF |

## FAQ

**How do I export a Gemini chat as a PDF?**
For one answer, export it to Docs and download the Doc as PDF. For the whole chat, scroll to the top and print the page to PDF, or use an exporter that builds a print view of just the conversation.

**How do I export my Gemini chat history?**
Use Google Takeout: My Activity, then only Gemini Apps. You get every saved prompt and response in one HTML or JSON file. Chats made while Gemini Apps Activity was off are not included.

**Can I export a Gemini chat to Google Docs?**
Yes, with Share & export, then Export to Docs under a response. It exports that response, not the whole back-and-forth, so a long chat takes several exports or a different method.

**Can I move a Gemini chat to Claude, ChatGPT or another Google account?**
There is no transfer feature. Export the chat as Markdown or text, then paste it or attach the file in the new chat (or the new account) and ask it to continue from there.

**Can I export Gemini chats on my phone?**
The Gemini app has the same share options under a response, including Export to Docs and share links. Browser extensions do not run in the mobile app, and Takeout works from a phone browser.

Related: [save a ChatGPT conversation as a PDF](save-chatgpt-conversation-pdf), [export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown), [export a Claude conversation](export-claude-conversation).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Google. Gemini is a trademark of Google LLC, named only to describe the site the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How do I export a Gemini chat as a PDF?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "For one answer, export it to Docs and download the Doc as PDF. For the whole chat, scroll to the top and print the page to PDF, or use an exporter that builds a print view of just the conversation."
      }
    },
    {
      "@type": "Question",
      "name": "How do I export my Gemini chat history?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Use Google Takeout: My Activity, then only Gemini Apps. You get every saved prompt and response in one HTML or JSON file. Chats made while Gemini Apps Activity was off are not included."
      }
    },
    {
      "@type": "Question",
      "name": "Can I export a Gemini chat to Google Docs?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, with Share & export, then Export to Docs under a response. It exports that response, not the whole back-and-forth, so a long chat takes several exports or a different method."
      }
    },
    {
      "@type": "Question",
      "name": "Can I move a Gemini chat to Claude, ChatGPT or another Google account?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "There is no transfer feature. Export the chat as Markdown or text, then paste it or attach the file in the new chat (or the new account) and ask it to continue from there."
      }
    },
    {
      "@type": "Question",
      "name": "Can I export Gemini chats on my phone?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The Gemini app has the same share options under a response, including Export to Docs and share links. Browser extensions do not run in the mobile app, and Takeout works from a phone browser."
      }
    }
  ]
}
</script>
