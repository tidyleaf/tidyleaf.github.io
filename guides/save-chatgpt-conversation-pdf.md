---
title: How to save a ChatGPT conversation as a PDF
description: Save a ChatGPT conversation as a PDF with the print dialog, a share link, the data export or an extension, and fix cut-off code blocks and dark pages.
---

# How to save a ChatGPT conversation as a PDF

ChatGPT has no "Download as PDF" button. The quickest free way is your browser's print dialog: open the chat on chatgpt.com, press Ctrl+P (Cmd+P on a Mac) and choose **Save as PDF** as the destination. That works, but printing the live chat page often gives you the sidebar, cut-off code blocks and dark pages. Below are four ways to get a clean PDF, what goes wrong with each, and how to fix it.

## Option 1: print the chat page to PDF (free, no install)

1. Open the conversation on chatgpt.com in a desktop browser.
2. Switch ChatGPT to the light theme first (Settings, then General, then Light under Appearance). See the dark mode note below for why.
3. Scroll to the top of the chat and back down, so every message has loaded.
4. Press **Ctrl+P** (Windows, Linux) or **Cmd+P** (Mac).
5. Set the destination to **Save as PDF** in Chrome or Edge, **Save to PDF** in Firefox, or use the **PDF** menu at the bottom left of the Mac print dialog in Safari.
6. Open **More settings** and turn on **Background graphics** if code blocks look blank, then save.

**What goes wrong:**

- **Code blocks are cut off.** ChatGPT shows long lines of code in a box that scrolls sideways. Paper does not scroll, so anything past the right edge of the box is simply missing from the PDF.
- **Dark mode prints badly.** With the dark theme on, you can get light gray text on a white page (when background graphics are off) or pages full of black ink (when they are on). Switch to the light theme before printing.
- **Page furniture comes along.** The sidebar, the message box and buttons can end up in the PDF, and the layout can squeeze the chat into a narrow column.
- **Messages break across pages** in awkward places, and very long chats can come out with gaps if part of the conversation had not loaded.

**Fix for cut-off code:** before printing, you can make code blocks wrap instead of scroll. Open the browser console (F12, then the Console tab), paste this and press Enter, then print again:

```js
const s = document.createElement('style');
s.textContent = '@media print { pre, code { white-space: pre-wrap !important; word-break: break-word !important; overflow: visible !important; } }';
document.head.appendChild(s);
```

It only changes the page in your own tab, for this print, and is gone when you reload. ChatGPT changes its page often, so treat it as a quick fix rather than a guaranteed one.

## Option 2: print from a share link (cleaner page)

ChatGPT's **Share** button (top right of a chat) creates a public link to a read-only copy of the conversation. That page has no sidebar and no message box, so it prints more cleanly than the chat itself.

1. Click **Share**, then **Create link** (or **Copy link**).
2. Open the link in a new tab and print it to PDF as in Option 1.

**Caveats:** anyone with the link can read the conversation, so do not do this for chats with private or work data. Delete the link afterwards under Settings, then Data controls, then Shared links. The cut-off code problem can still happen here, and the console fix above applies.

## Option 3: ChatGPT's data export (every chat, then print one)

Under Settings, then Data controls, then **Export data**, OpenAI emails you a zip of your whole history. Inside is `chat.html`, a single page with all your conversations, which you can open in a browser and print to PDF.

- **Good for:** a full archive, or when you need a PDF of many chats.
- **Not good for:** one chat. The email can take a while to arrive, every conversation is on one long page, and you have to find yours and print only those pages.

## Option 4: an exporter extension (one click, built for paper)

A browser extension can read the conversation and lay it out as a print page made for PDF, rather than printing the chat app. This is one of the things we built **Tidyleaf AI Chat Exporter** for. Disclosure: Tidyleaf is us, and this is our product.

What its PDF export does, free:

- Opens a clean print view of the whole conversation: the chat title, the export date, and each message labelled **User** or **Assistant**, with no sidebar or buttons.
- **Wraps long code lines** instead of cutting them off, and labels each code block with its language when the site provides one.
- Prints on a **white page with dark text**, whichever ChatGPT theme you use.
- Keeps tables, lists, headings and quotes. Math is shown as its LaTeX source, not as rendered formulas.
- Gets the full active branch of the chat on ChatGPT, not just what is on screen, by asking the site for the conversation with your existing login.
- The print dialog opens on its own; you choose **Save as PDF**.

It also exports to Markdown, text and JSON, and works on claude.ai and gemini.google.com too. Nothing is uploaded: there is no server and no account, and the file is made in your browser. It is a desktop extension; it does not run in the ChatGPT phone app.

**Tidyleaf Pro** ($24 a year or $3.99 a month) adds bulk export of all your ChatGPT or Claude chats as a zip of Markdown files, plus Obsidian and Notion export. PDF export stays free.

**Tidyleaf AI Chat Exporter is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf AI Chat Exporter once it is approved. -->

## Which option should you use?

| You want | Use | Watch out for |
|---|---|---|
| A quick PDF of a short chat with no code | Print the chat page | Light theme first |
| A cleaner page without installing anything | Print from a share link | The link is public until you delete it |
| A PDF of every chat you have | Data export, then print `chat.html` | Slow, and one huge page |
| A long chat with code, regularly | An exporter extension | Read its privacy policy first |

## On a phone

The ChatGPT app has no print option. Open the chat at chatgpt.com in your phone's browser (or open a share link there), then:

- **iPhone or iPad (Safari):** tap Share, then **Print**, then Share again from the print preview and choose **Save to Files**. The same problems apply: use the light theme, and wide code blocks can still be cut off.
- **Android (Chrome):** tap the menu, then Share, then **Print**, and set the printer to **Save as PDF**.

## FAQ

**Can I save a ChatGPT conversation as a PDF without an extension?**
Yes. Print the chat page or its share link to PDF from your browser (Options 1 and 2). Switch to the light theme first, and use the console snippet above if code blocks are cut off.

**Why is my ChatGPT PDF missing part of the code?**
Code blocks on chatgpt.com scroll sideways, and a PDF cannot scroll, so the part past the edge is dropped. Make the code wrap before printing (the snippet in Option 1) or use an exporter whose print view wraps code.

**How do I save a ChatGPT conversation as a PDF in Firefox?**
The same way: Ctrl+P or Cmd+P, then set the destination to **Save to PDF**. Firefox has no "Background graphics" switch by that name; it is **Print backgrounds** under More settings.

**Is there a way to export a ChatGPT chat as a file other than PDF?**
Yes. See [how to export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown), which also covers text and JSON. For Claude, see [how to export a Claude conversation](export-claude-conversation).

**Can I keep my saved chats organized instead of exporting them?**
Inside ChatGPT, yes, with folders. See [how to organize ChatGPT chats into folders](organize-chatgpt-chats-folders).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by OpenAI. ChatGPT is a trademark of OpenAI, named only to describe the site the extension works on.*
