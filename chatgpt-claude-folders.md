---
title: ChatGPT Folders Extension for Chrome, Also for Claude
description: A ChatGPT folders extension for Chrome that also works on Claude. Sort chats into folders, pin favorites and search titles, free, with nothing uploaded.
---

# ChatGPT folders extension for Chrome (and Claude)

ChatGPT and Claude have no folders in their chat lists. The closest built-in tool on both sites is Projects, which groups chats under a project with its own instructions and files. If you want plain folders in the sidebar, you need a browser extension. **Tidyleaf Folders for ChatGPT and Claude** is ours: it adds a Folders section above the chat list on chatgpt.com and claude.ai, lets you drag chats into folders, pin the ones you use and search every chat title. The free version gives you 5 folders. Below are the built-in options first, then what to check in any folders extension, then ours.

## Option 1: Projects, built into ChatGPT and Claude

Both sites have a feature called Projects. You create a project, move chats into it, and give it instructions and files that every chat in it can use.

- **Good for:** ongoing work that needs the same context every time, such as a codebase, a course or a client.
- **Not good for:** quick sorting. A project is a workspace with its own settings, not a lightweight label: a chat moved into one takes on that project's instructions and files. A chat sits in one project at a time, projects cannot be nested, and a ChatGPT project and a Claude project are two separate things in two separate apps. On ChatGPT, a chat started with a custom GPT cannot be moved into a project at all.

## Option 2: the site's own search, pins, stars and archive

ChatGPT has a chat search, lets you pin chats and has an archive. Claude has a search and lets you star chats, which puts them in a Starred list above Recents.

- **Good for:** finding a chat when you remember a word from it, and keeping a few favorites in reach.
- **Not good for:** grouping chats by topic. Pins and stars are one flat list, and archiving hides a chat rather than filing it.

## Option 3: a folders extension

A folders extension adds folders to the sidebar of the site, without changing your chats on the site itself. Several exist on the Chrome Web Store, some for ChatGPT only. Before you install one, check four things:

1. **Where your folders are stored.** Your folders contain your chat titles. An extension that stores them in the browser keeps them private; one that syncs to its own server sends them there. Read its privacy policy.
2. **How many folders are free.** Most folder extensions are freemium and cap the free folders. Check the cap against how many topics you have.
3. **Which sites it covers.** If you use both ChatGPT and Claude, one extension with one set of folders saves you keeping two systems.
4. **What it asks to access.** A folders extension needs access to the chat site. It should not need access to every site you visit.

## Tidyleaf Folders for ChatGPT and Claude

Disclosure: Tidyleaf is us, and this is our product.

What it does, free:

- Adds a **Folders** section right above the chat list on chatgpt.com and claude.ai, in the site's own look, light or dark.
- **Drag any chat** from the site's list onto a folder, or pick a folder for the open chat from a menu.
- **Up to 5 folders**, each with a color, which you can rename, reorder or collapse.
- **Pin** the chats you keep coming back to at the top.
- **One set of folders for both sites:** a ChatGPT chat and a Claude chat can sit in the same folder.
- **Instant search across all your chat titles**, in any language, including Chinese, Japanese and Korean.
- Deleting a folder never deletes a chat. It only takes the chats out of the folder.

**Tidyleaf Pro** ($24 a year or $3.99 a month, one key for every Tidyleaf extension) adds:

- **Search inside messages:** find a chat by anything said in it, not just its title, with the matching line shown under each result. You click "Index your messages" once, and the extension builds the search index inside the extension on your device. After that it reads only new or changed chats.
- **Unlimited folders.**
- **Folder export:** every chat in a folder saved as a Markdown file, in one zip, in the same format as [Tidyleaf AI Chat Exporter](ai-chat-exporter).

The free features stay free, and folders you made with Pro stay if you cancel. [Get Tidyleaf Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf).

| | Free | Pro |
|---|---|---|
| Folders | Up to 5 | Unlimited |
| Pins, colors, drag and drop | Yes | Yes |
| Search chat titles | Yes | Yes |
| Search inside messages | No | Yes |
| Export a folder to Markdown | No | Yes |
| Works on chatgpt.com and claude.ai | Yes | Yes |

**Tidyleaf Folders for ChatGPT and Claude is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Folders for ChatGPT and Claude once it is approved. -->

### Privacy, in plain words

Your folders and pins are saved in your browser only, and are not synced to other devices. The chat list comes from the site you are already signed in to, using the same request the site's own page makes. There is no server, no account, no analytics and no tracking. With Pro, the message index is kept in the extension's own storage on your device; chatgpt.com and claude.ai cannot read it, it is never uploaded, and the popup has a button to delete it. The only thing the extension ever sends elsewhere is your Pro license key, to our payment provider Polar, to check it. The extension asks for access to chatgpt.com and claude.ai only. Full details are in the [privacy policy](chat-folders/privacy).

### Good to know

- It works on chatgpt.com and claude.ai. Gemini is not supported yet, because Gemini has no stable way for an extension to list your chats.
- Indexing messages on a large account takes a few minutes, because the extension reads chats one by one and pauses between them. Keep the tab open while it runs.
- Folder export saves the chats of the site you are on. For a folder that mixes both sites, open the other site to export its chats.
- Folders live in the browser where you made them. Uninstalling the extension removes them.

## Which option should you use?

| You want | Use |
|---|---|
| The same instructions and files across a set of chats | Projects on ChatGPT or Claude |
| A few favorite chats in reach | ChatGPT's pins or Claude's stars |
| To find one chat by a word you remember | The site's own search |
| Plain folders and pins in the sidebar, for both sites | A folders extension, such as Tidyleaf Folders |
| To find a chat by something said inside it, across both sites | Tidyleaf Pro's message search |

For a step-by-step walkthrough of sorting a long ChatGPT history, see [how to organize ChatGPT chats into folders](guides/organize-chatgpt-chats-folders). If your problem is finding an old Claude chat rather than filing new ones, see [how to search old Claude chats](guides/search-old-claude-chats).

## FAQ

**Does ChatGPT have folders?**
Not as folders. ChatGPT's built-in way to group chats is Projects, which bundle chats with shared instructions and files. For simple folders in the sidebar you need an extension.

**Is there a ChatGPT folders Chrome extension that also works on Claude?**
Yes. Tidyleaf Folders works on both chatgpt.com and claude.ai, with one set of folders, so a folder can hold chats from both sites.

**Is a ChatGPT folders extension safe?**
It depends on where it keeps your data. A folders extension sees your chat titles, so read its privacy policy and check that it only asks for access to the chat sites. Tidyleaf Folders keeps everything in your browser and asks for chatgpt.com and claude.ai only; the only outside request is the Pro key check.

**My ChatGPT folders are gone or not showing. What happened?**
ChatGPT's own sidebar has Projects, not folders, so folders you saw there came from an extension. Check that the extension is still installed and enabled, and that you are in the same browser and profile where you made the folders: most folders extensions, Tidyleaf Folders included, keep them in that browser only. A redesign of the site's sidebar can also stop an extension from finding its place until the extension is updated. If Tidyleaf Folders cannot find the sidebar, it shows its panel at the bottom left of the page instead, so your folders stay reachable.

**Can I put folders inside ChatGPT Projects?**
No. Projects are ChatGPT's own grouping and have no subfolders. You can use Projects for chats that share instructions and files, and an extension's folders for everything else.

**Does deleting a folder delete my chats?**
Not with Tidyleaf Folders. Deleting a folder only takes the chats out of it; the chats stay on ChatGPT or Claude. Folders also never change anything on the site itself.

**Is there a ChatGPT folders extension for Firefox?**
Some folder extensions have Firefox versions, listed on Firefox Add-ons (addons.mozilla.org). Tidyleaf Folders is coming to the Chrome Web Store first, and versions for Firefox and Microsoft Edge are planned. They will be linked here once they are listed.

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by OpenAI or Anthropic. ChatGPT and Claude are trademarks of their respective owners, named only to describe the sites the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
[
  {
    "@context": "https://schema.org",
    "@type": "FAQPage",
    "mainEntity": [
      {
        "@type": "Question",
        "name": "Does ChatGPT have folders?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Not as folders. ChatGPT's built-in way to group chats is Projects, which bundle chats with shared instructions and files. For simple folders in the sidebar you need an extension."
        }
      },
      {
        "@type": "Question",
        "name": "Is there a ChatGPT folders Chrome extension that also works on Claude?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Yes. Tidyleaf Folders works on both chatgpt.com and claude.ai, with one set of folders, so a folder can hold chats from both sites."
        }
      },
      {
        "@type": "Question",
        "name": "Is a ChatGPT folders extension safe?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "It depends on where it keeps your data. A folders extension sees your chat titles, so read its privacy policy and check that it only asks for access to the chat sites. Tidyleaf Folders keeps everything in your browser and asks for chatgpt.com and claude.ai only; the only outside request is the Pro key check."
        }
      },
      {
        "@type": "Question",
        "name": "My ChatGPT folders are gone or not showing. What happened?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "ChatGPT's own sidebar has Projects, not folders, so folders you saw there came from an extension. Check that the extension is still installed and enabled, and that you are in the same browser and profile where you made the folders: most folders extensions, Tidyleaf Folders included, keep them in that browser only. A redesign of the site's sidebar can also stop an extension from finding its place until the extension is updated. If Tidyleaf Folders cannot find the sidebar, it shows its panel at the bottom left of the page instead, so your folders stay reachable."
        }
      },
      {
        "@type": "Question",
        "name": "Can I put folders inside ChatGPT Projects?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "No. Projects are ChatGPT's own grouping and have no subfolders. You can use Projects for chats that share instructions and files, and an extension's folders for everything else."
        }
      },
      {
        "@type": "Question",
        "name": "Does deleting a folder delete my chats?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Not with Tidyleaf Folders. Deleting a folder only takes the chats out of it; the chats stay on ChatGPT or Claude. Folders also never change anything on the site itself."
        }
      },
      {
        "@type": "Question",
        "name": "Is there a ChatGPT folders extension for Firefox?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Some folder extensions have Firefox versions, listed on Firefox Add-ons (addons.mozilla.org). Tidyleaf Folders is coming to the Chrome Web Store first, and versions for Firefox and Microsoft Edge are planned. They will be linked here once they are listed."
        }
      }
    ]
  },
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Tidyleaf Folders for ChatGPT and Claude",
    "description": "Folders, pins and fast search for your ChatGPT and Claude chats. Free. Tidyleaf Pro adds search inside messages and folder export.",
    "applicationCategory": "BrowserApplication",
    "operatingSystem": "Chrome",
    "url": "https://tidyleaf.github.io/chatgpt-claude-folders",
    "offers": [
      {
        "@type": "Offer",
        "name": "Free",
        "price": "0",
        "priceCurrency": "USD"
      },
      {
        "@type": "Offer",
        "name": "Tidyleaf Pro (yearly)",
        "price": "24",
        "priceCurrency": "USD",
        "description": "Tidyleaf Pro subscription, US$24 billed yearly; one key unlocks Pro in every Tidyleaf extension",
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "24",
          "priceCurrency": "USD",
          "referenceQuantity": {
            "@type": "QuantitativeValue",
            "value": 1,
            "unitCode": "ANN"
          }
        }
      },
      {
        "@type": "Offer",
        "name": "Tidyleaf Pro (monthly)",
        "price": "3.99",
        "priceCurrency": "USD",
        "description": "Tidyleaf Pro subscription, US$3.99 billed monthly; one key unlocks Pro in every Tidyleaf extension",
        "priceSpecification": {
          "@type": "UnitPriceSpecification",
          "price": "3.99",
          "priceCurrency": "USD",
          "referenceQuantity": {
            "@type": "QuantitativeValue",
            "value": 1,
            "unitCode": "MON"
          }
        }
      }
    ],
    "publisher": {
      "@type": "Organization",
      "name": "Tidyleaf"
    }
  }
]
</script>
