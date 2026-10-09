---
title: How to organize ChatGPT chats into folders (2026)
description: "How to organize ChatGPT chats into folders: what Projects can and cannot do, how archive and search help, and when a folders extension fits better."
---

# How to organize ChatGPT chats into folders

ChatGPT has no plain folders for chats. The closest built-in feature is **Projects**: you create a project in the sidebar and drag chats into it, or pick "Move to project" from a chat's menu. Projects work as folders for a few big topics, but they are flat, they change how the chats inside them behave, and deleting a project deletes its chats. For anything finer, combine Projects with **archive** and **search**, or add a folders extension to the sidebar. Here is what each one does, and what it does not.

## Option 1: ChatGPT Projects (built in)

A project is a group of chats that share files and custom instructions. It shows up in the sidebar above your chat history, so it doubles as a folder.

How to use it as a folder:

1. In the sidebar, choose **New project** and give it a name.
2. Drag an existing chat from your history onto the project, or open the chat's **...** menu and choose **Move to project**.
3. To take a chat out again, use the same menu on the chat inside the project.
4. New chats started from inside the project land in it automatically.

What to know before you rely on it:

- **A project is more than a folder.** Chats moved into a project pick up its instructions and files. That is the point of Projects, but it means you cannot use one purely as a label without the context coming along.
- **Projects are flat.** There are no subfolders and no project inside a project.
- **One place per chat.** A chat sits in one project or in your general history; you cannot file the same chat under two topics.
- **Deleting a project deletes the chats in it**, along with its instructions and the files stored only in that project, and it cannot be undone. Move chats out first if you want to keep them.
- **Nothing sorts your old history for you.** Every existing chat has to be moved by hand.
- **Plan limits apply,** such as how many files a project can hold. They have changed over time, so check OpenAI's help center for your plan.

Projects are a good fit when a topic needs shared context, like a client, a course or a long piece of writing. They are a heavy tool for "put my recipe chats somewhere".

## Option 2: Archive what you are done with

Archiving takes a chat out of the sidebar without deleting it. Open a chat's **...** menu and choose **Archive**. Archived chats are listed under **Settings, Data controls, Archived chats**, where you can open or unarchive them, and they still appear in ChatGPT's search.

Archive does not organize anything by itself, but it shortens the list you scroll through. A simple routine: keep active work in the sidebar or a project, and archive the rest once a week.

## Option 3: Search and better titles

ChatGPT's search (the magnifying glass in the sidebar, or Ctrl+K on Windows and Cmd+K on Mac) looks through your chats, archived ones included. Two habits make it work much better:

- **Rename chats** with a clear title (**...** menu, then **Rename**). An automatic title like "Python Error Fix" is hard to tell apart from twenty others; "Invoice script: CSV date bug" is not.
- **Search specific words** that only appear in the chat you want, such as a project name, a function name or a place.

Search answers "where is that chat?", not "show me everything about X", so it complements folders rather than replacing them.

## Option 4: A folders extension

Several browser extensions add real folders to the ChatGPT sidebar. Most of them work as labels kept by the extension: the chat stays where it is in ChatGPT and nothing about its context changes. Check that deleting a folder in the one you pick does not delete the chats in it. Before you install any of them, check three things:

1. **Where your folders are stored.** On your device only, or on the extension maker's server?
2. **What it sends and to whom.** An extension that organizes chats can read your chat list; the privacy policy should say exactly what leaves your browser.
3. **What the free plan allows.** Most cap the number of folders and charge for more.

We built one of these: **Tidyleaf Folders for ChatGPT and Claude**. Disclosure: Tidyleaf is us, and this is our product.

What it does, free:

- Adds a **Folders** section right above the chat list on chatgpt.com, in the site's own light or dark look.
- **Drag any chat** from ChatGPT's list into a folder, or pick a folder for the open chat from a menu.
- **Up to 5 folders**, each with a color, which you can rename, reorder or collapse.
- **Pins** for the chats you keep coming back to.
- **Instant search across chat titles**, in any language, including Chinese, Japanese and Korean.
- Also works on **claude.ai**, with one set of folders for both sites, so a ChatGPT chat and a Claude chat can sit in the same folder.
- Deleting a folder never deletes a chat.

Your folders and pins are saved in your browser only. The chat list comes from ChatGPT itself, with your existing login, the same way ChatGPT's own page asks for it. There is no server, no account and no tracking; the only thing ever sent elsewhere is a Pro license key, to our payment provider, to check it (see the [privacy policy](../chat-folders/privacy)). Because folders live in the browser, they do not sync to your other devices or the ChatGPT mobile app.

**[Tidyleaf Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf)** ($24 a year or $3.99 a month, one key for every Tidyleaf extension) adds unlimited folders, **search inside messages** (find a chat by anything said in it, with the matching line shown; the index is built and kept on your device) and **export of a folder** to a zip of Markdown files. Gemini is not supported.

**Tidyleaf Folders for ChatGPT and Claude is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Folders for ChatGPT and Claude once it is approved. -->

More detail is on the [Tidyleaf Folders page](../chatgpt-claude-folders).

## Which option should you use?

| You want | Use |
|---|---|
| A few big topics that share files and instructions | ChatGPT Projects |
| A shorter sidebar without deleting anything | Archive |
| To find one chat you remember a word from | ChatGPT search, plus clear titles |
| Many small folders, or one chat filed without changing its context | A folders extension |
| Folders that cover both ChatGPT and Claude | A folders extension that supports both, such as Tidyleaf Folders |
| Folders on your phone too | Projects (folders extensions run in a desktop browser and do not reach the ChatGPT app) |

Most people end up with a mix: Projects for two or three heavy topics, a folders extension or archive for the long tail.

## FAQ

**Can you organize ChatGPT chats into folders?**
Not with folders as such. Projects are the built-in way to group chats and can be used as top-level folders. For plain folders, subfolders or more than a handful of groups, use a browser extension.

**Why are my ChatGPT folders gone or not showing?**
ChatGPT's own sidebar has Projects, not folders, so "folders" you saw came from an extension. If they disappeared, the extension may be turned off, removed, or broken by a ChatGPT redesign, or you may be in a different browser or profile, since many extensions keep folders in that one browser. Check the extension's page in your browser's extension settings first.

**Can I put ChatGPT chats into folders inside a project?**
No. Projects have no subfolders. A folders extension can hold chats from anywhere in your history, but it does not reach inside ChatGPT's project structure.

**Does deleting a ChatGPT project delete the chats?**
Yes. OpenAI's help center says deleting a project permanently removes its chats and instructions, and the files stored only in that project. Move any chat you want to keep back to your history before deleting the project. With an extension like ours, deleting a folder only empties the folder; the chats stay in ChatGPT.

**Can I organize ChatGPT chats by date?**
ChatGPT has no date filter or sort option. The sidebar lists chats by most recent activity, so an old chat you reopen moves back to the top. To keep an old chat in reach, pin it or file it in a folder; to get finished ones out of the way, archive them. To keep a copy outside ChatGPT, see [how to export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown).

Related: [find an old Claude chat](search-old-claude-chats) and [Tidyleaf AI Chat Exporter](../ai-chat-exporter).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by OpenAI or Anthropic. ChatGPT and Claude are trademarks of their respective owners, named only to describe the sites the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can you organize ChatGPT chats into folders?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Not with folders as such. Projects are the built-in way to group chats and can be used as top-level folders. For plain folders, subfolders or more than a handful of groups, use a browser extension."
      }
    },
    {
      "@type": "Question",
      "name": "Why are my ChatGPT folders gone or not showing?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ChatGPT's own sidebar has Projects, not folders, so \"folders\" you saw came from an extension. If they disappeared, the extension may be turned off, removed, or broken by a ChatGPT redesign, or you may be in a different browser or profile, since many extensions keep folders in that one browser. Check the extension's page in your browser's extension settings first."
      }
    },
    {
      "@type": "Question",
      "name": "Can I put ChatGPT chats into folders inside a project?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. Projects have no subfolders. A folders extension can hold chats from anywhere in your history, but it does not reach inside ChatGPT's project structure."
      }
    },
    {
      "@type": "Question",
      "name": "Does deleting a ChatGPT project delete the chats?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. OpenAI's help center says deleting a project permanently removes its chats and instructions, and the files stored only in that project. Move any chat you want to keep back to your history before deleting the project. With an extension like ours, deleting a folder only empties the folder; the chats stay in ChatGPT."
      }
    },
    {
      "@type": "Question",
      "name": "Can I organize ChatGPT chats by date?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "ChatGPT has no date filter or sort option. The sidebar lists chats by most recent activity, so an old chat you reopen moves back to the top. To keep an old chat in reach, pin it or file it in a folder; to get finished ones out of the way, archive them. To keep a copy outside ChatGPT, see how to export a ChatGPT conversation to Markdown."
      }
    }
  ]
}
</script>
