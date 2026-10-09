---
title: How to organize Claude.ai chats into folders (2026)
description: "How to organize claude.ai chats into folders: what Projects and renaming can and cannot do, and how to set up local folders that also cover ChatGPT."
---

# How to organize Claude.ai chats into folders

Claude has no folders for chats. The built-in way to group them is **Projects**: create a project, then move a chat into it from the dropdown next to the chat's name with **Add to project**. Every chat in a project shares the project's instructions and files, so a project is a workspace rather than a plain folder. For lighter sorting, rename chats with a topic prefix. For real folders in the sidebar, you need a browser extension. Here is what each option does and does not do.

## Option 1: Claude Projects (built in)

A project has a name, a description, project instructions and a knowledge base of files, plus the chats that belong to it. The steps, from Anthropic's help center:

1. Go to claude.ai/projects (or **Projects** in the left sidebar) and click **New Project** in the upper right. Give it a name and a description.
2. To start a chat inside a project, open the project and start a new chat there.
3. To move a chat you already have, click the dropdown arrow next to the chat name, choose **Add to project**, then pick the project in the **Move chat** window.
4. To take a chat out again, use the same dropdown and choose **Remove from project**.

What to know before you rely on it:

- **A project is more than a folder.** Its instructions and knowledge apply to every chat in it, so you cannot use one as a plain label without that context coming along.
- **Free accounts get five.** The help center says free users can create a maximum of five projects.
- **Chats do not share memory.** Context is not shared across chats in a project unless you add it to the project knowledge.
- **No subfolders.** The help center describes no nesting, so treat projects as a flat list.
- **Old chats are not sorted for you.** Nothing files your existing chats; you move them into projects yourself.
- **One project per chat.** A chat sits in one project at a time, so a project cannot work as a tag.
- **You can star a project** from the **...** menu on the Projects page, or the star icon inside the project, to keep it in quick reach in the sidebar.

Projects fit a client, a course, a codebase or a long piece of writing, where the same context helps every chat. They are a heavy tool for "put my recipe chats somewhere".

## Option 2: Rename with a prefix

Claude names chats automatically, and the names are often vague. To rename one on the web, hover over it in the sidebar (or in **Chats and tasks**), click the **⋮** button and choose **Rename**. On iOS, touch and hold the chat; on Android, open it and use the **⋮** menu at the top right.

Give every chat a short prefix that names its topic:

- `CLIENT-Acme: pricing page copy`
- `RECIPE: weeknight tofu`
- `CODE-invoices: CSV date bug`

Prefixed titles are easy to spot when you scroll the chat list, and easy to find with any tool that searches chat titles. Pick the prefixes once and stick to them; the method depends on typing the same word every time.

Limits: it works only while you are disciplined, it does nothing for the chats you already have, and it gives you labels, not a place to look. For finding a specific old chat, see [how to search old Claude chats](search-old-claude-chats).

## Option 3: A folders extension

A browser extension can add real folders to the Claude sidebar. Before you pick one, check four things:

1. **Where your folders are stored.** Folder names and the chat titles inside them are a map of your work. Browser-only storage keeps that on your device; an extension that syncs to its own server sends it there. Read the privacy policy.
2. **What the free plan allows.** Most cap the number of folders. Check the cap against how many topics you have.
3. **Whether it will still be around.** Small extensions come and go, and folders that live only inside an extension go with it. Check when it was last updated on its store page.
4. **Which sites it covers.** If you use Claude and ChatGPT, one extension with one set of folders beats two.

Treat folders as an index, not as the only copy of anything. If a chat matters, export it too; see [how to export a Claude conversation](export-claude-conversation).

We built one of these: **Tidyleaf Folders for ChatGPT and Claude**. Disclosure: Tidyleaf is us, and this is our product.

What it does, free:

- Adds a **Folders** section right above the chat list on claude.ai and chatgpt.com, in the site's own look, light or dark.
- **Drag any chat** from Claude's list into a folder, or pick a folder for the open chat from a menu.
- **Up to 5 folders**, each with a color, which you can rename, reorder or collapse.
- **Pin** the chats you keep coming back to at the top.
- **Instant search across all your chat titles**, in any language, including Chinese, Japanese and Korean.
- **One set of folders for both sites**, so a Claude chat and a ChatGPT chat can sit in the same folder.
- Deleting a folder never deletes a chat. It only takes the chats out of the folder.

Your folders and pins are saved in your browser only. They are not synced to other devices or to the Claude mobile app, and uninstalling the extension removes them. The chat list comes from claude.ai, using the login you already have and the same request Claude's own page makes. There is no server, no account and no tracking; the only thing the extension sends elsewhere is a Pro license key, to our payment provider Polar, to check it.

**[Tidyleaf Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf)** ($24 a year or $3.99 a month, one key for every Tidyleaf extension) adds unlimited folders, **search inside messages** (find a chat by anything said in it; the index is built and kept on your device) and **export of a folder** to a zip of Markdown files. The free features stay free, and folders you made with Pro stay if you cancel.

**Tidyleaf Folders for ChatGPT and Claude is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Folders for ChatGPT and Claude once it is approved. -->

More detail is on the [Tidyleaf Folders page](../chatgpt-claude-folders).

### A ten-minute folder setup for Claude and ChatGPT

1. Write down five topics you actually use, such as Work, Code, Writing, Research and Personal. A few broad folders are easier to keep up than many narrow ones.
2. Create those folders, give each a color, and drag in the chats you already return to.
3. From then on, file a chat when you start it, from the open chat's folder menu, rather than sorting a backlog later.
4. Use the same folders for ChatGPT. A folder called Code can hold the Claude chat and the ChatGPT chat about the same project.
5. Keep Projects for the two or three topics that need shared instructions and files, and use folders for everything else.

## Which option should you use?

| You want | Use |
|---|---|
| Shared instructions and files across a set of chats | Claude Projects |
| Chat names you can recognize at a glance | Rename with a prefix |
| Many small folders without changing a chat's context | A folders extension |
| Folders that cover both Claude and ChatGPT | A folders extension that supports both, such as Tidyleaf Folders |

Most people end up with a mix: Projects for a couple of heavy topics, and folders or a naming habit for the rest.

## FAQ

**Can you make folders in Claude.ai?**
Not plain folders. Claude's built-in grouping is Projects, which put chats under shared instructions and files. For simple folders in the sidebar, use a browser extension.

**Why did my Claude folders disappear?**
Claude's own sidebar has no folders, so the ones you saw came from an extension. It may have been turned off or removed, or you may be in a different browser or profile from the one where you made them. Check your browser's extensions page first. Folders kept only inside an extension are lost if it is uninstalled, so export the chats that matter.

**Does moving a chat into a Claude project change it?**
In effect, yes: the project's instructions and knowledge apply to chats in it. If you only want a label, a rename prefix or a folders extension leaves the chat's context alone.

**How many projects can I have on the free plan?**
Five. Anthropic's help center says free users can create a maximum of five projects.

**Can I use the same folders for Claude and ChatGPT?**
Yes, with an extension that covers both. Tidyleaf Folders keeps one set of folders for claude.ai and chatgpt.com, so a chat from each site can sit in the same folder. The built-in Projects of the two apps are separate.

## Related guides

- [How to organize ChatGPT chats into folders](organize-chatgpt-chats-folders)
- [How to search old Claude chats](search-old-claude-chats)
- [How to export a Claude conversation](export-claude-conversation)

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Anthropic or OpenAI. Claude and ChatGPT are trademarks of their respective owners, named only to describe the sites the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can you make folders in Claude.ai?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Not plain folders. Claude's built-in grouping is Projects, which put chats under shared instructions and files. For simple folders in the sidebar, use a browser extension."
      }
    },
    {
      "@type": "Question",
      "name": "Why did my Claude folders disappear?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Claude's own sidebar has no folders, so the ones you saw came from an extension. It may have been turned off or removed, or you may be in a different browser or profile from the one where you made them. Check your browser's extensions page first. Folders kept only inside an extension are lost if it is uninstalled, so export the chats that matter."
      }
    },
    {
      "@type": "Question",
      "name": "Does moving a chat into a Claude project change it?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "In effect, yes: the project's instructions and knowledge apply to chats in it. If you only want a label, a rename prefix or a folders extension leaves the chat's context alone."
      }
    },
    {
      "@type": "Question",
      "name": "How many projects can I have on the free plan?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Five. Anthropic's help center says free users can create a maximum of five projects."
      }
    },
    {
      "@type": "Question",
      "name": "Can I use the same folders for Claude and ChatGPT?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, with an extension that covers both. Tidyleaf Folders keeps one set of folders for claude.ai and chatgpt.com, so a chat from each site can sit in the same folder. The built-in Projects of the two apps are separate."
      }
    }
  ]
}
</script>
