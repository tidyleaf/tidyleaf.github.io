# Privacy policy: Tidyleaf Folders for ChatGPT and Claude

Last updated: 2026-10-09

**Short version: Tidyleaf Folders collects no data. Your folders, pins and search index are kept on your device and never uploaded. The only thing sent anywhere is your Pro license key, to Polar, to check it.**

## What the extension does with your conversations

On chatgpt.com and claude.ai the extension adds a folders panel to the sidebar. To show your chats in it and to search their titles, it asks the site you are already on for the list of your conversations (their ids, titles and when they last changed), using your own login, exactly as the site's own page does.

If you have Pro and choose "Index your messages", the extension also asks the same site for the content of each of your conversations, again with your own login, and builds a search index from the text. If you export a folder, it asks the site for the conversations in that folder and builds a zip of Markdown files on your computer. These requests go only to the AI site you are on. They are never sent to us or anyone else, and your conversations are never uploaded.

## What we collect

Nothing. The extension has no server of ours, no analytics, no crash reporting, no advertising and no tracking. We never receive your conversations, your folders, your account details or your browsing.

## What is stored on your device

- Your folders (names, colors, order) and which chats are in them or pinned (the chat's id and title), in the browser's local extension storage.
- A copy of each site's chat list (ids, titles, last-changed times), so the panel can draw at once. It is refreshed from the site when you open it, at most every 10 minutes.
- With Pro, the message index: the text of your conversations, in the extension's own database (IndexedDB) inside your browser profile. It belongs to the extension, so chatgpt.com and claude.ai cannot read it. When a chat is deleted on the site, it is removed from the index the next time the index is refreshed. The popup has a button to delete the whole index.
- Your license key, the time of the last check and its result, so Pro stays unlocked between visits and for up to 7 days when you are offline.

Nothing is stored in your Google account or synced to other devices. Uninstalling the extension removes all of it. Removing the key in the popup removes the key and the last check.

## The one thing that leaves your browser: your Pro license key

If you paste a Pro license key into the popup, the extension sends that key (and our public Polar organization id) to Polar, our payment and licensing provider, at https://api.polar.sh to check that the key is valid and your subscription is active. It does this when you save the key and then at most once a day. Polar receives your IP address and the key, as any web request does, and handles them under its own privacy policy (https://polar.sh/legal/privacy). Nothing else is sent: no conversation, no folder, no page, no browser or account information. If you never enter a key, the extension never contacts Polar.

Payment itself happens on Polar's checkout page, not in the extension. We do not see your card details.

## Sharing

We do not sell, share or disclose any data, because we do not have any.

## Permissions

The extension asks for `storage` and for access to chatgpt.com and claude.ai only. It has no permission to read any other site. Each permission is explained in the store listing.

## Not affiliated

Tidyleaf Folders for ChatGPT and Claude is made by Tidyleaf and is not affiliated with OpenAI or Anthropic.

## Changes and contact

If this policy changes, the new version will be published at this address with a new date. Questions: use the support contact on the store listing.
