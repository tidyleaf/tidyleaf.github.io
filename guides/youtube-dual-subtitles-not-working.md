---
title: YouTube Dual Subtitles not working? What changed, and what to use now
description: If your dual-subtitle extension shows nothing on YouTube, YouTube changed how its player loads captions. How to check, what you can try, and a maintained replacement.
---

# YouTube Dual Subtitles not working? What changed, and what to use now

You open a video, the dual-subtitle extension is on, and nothing appears. Or the second line flickers and disappears, or YouTube's own captions break while the extension is active. You are not alone: as of October 2026, the Chrome Web Store page of the popular "YouTube Dual Subtitles" extension (about 200,000 users) shows its last update in November 2024, and many of its recent reviews say the subtitles no longer appear.

## What changed on YouTube

YouTube's player fetches captions from its own caption endpoint. The player's caption request now carries a token that the player creates for that video, and a request without it comes back empty, with no error. Extensions that fetch captions the old way get an empty answer, so they have nothing to draw. Some also get rate-limit errors (HTTP 429) when they retry.

This is the most common reason dual-subtitle extensions went quiet, and it is not something a setting on your side can fix. Only an update to the extension can.

## Quick checks before you give up on it

1. **Does the video have captions at all?** Open the gear menu, Subtitles/CC. If there is no track, no extension can show subtitles.
2. **Turn other caption and translation extensions off.** Two extensions drawing over the same player often hide each other.
3. **Reload the page after the ad.** YouTube serves no captions during ads, and some extensions give up if they start then.
4. **Check the extension's last update** on its Chrome Web Store page. If it predates the breakage and recent reviews describe the same symptom, it will not come back without its developer.

## What to use instead

- **Tidyleaf Dual Subtitles for YouTube 中英双字幕** (ours, disclosed: Tidyleaf is us). It reads captions the way YouTube's own player does, from the player's own request, so it works with the current caption system. Two lines on regular videos and Shorts, Traditional and Simplified Chinese plus 15 other languages, pinyin or zhuyin, no account and no API key. The core feature is free with no trial. Details on [YouTube with Chinese and English subtitles at the same time](youtube-dual-subtitles-chinese-english).
- **Language Reactor** and **Immersive Translate** also show two lines on YouTube and cover more sites, with paid plans.
- **YouTube's built-in auto-translate** gives you one translated line (gear, Subtitles/CC, Auto-translate). Not two lines, but it works with nothing installed.

**Tidyleaf Dual Subtitles for YouTube is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Dual Subtitles for YouTube once it is approved. -->

## Will this break again?

Possibly. YouTube changes its player often, and any extension that shows subtitles depends on it. The honest test for any replacement, including ours, is the date of its last update and whether its recent reviews are about the current YouTube. We test ours against live YouTube videos, including a seek and a speed change, and update it when YouTube changes.

## FAQ

**Is Tidyleaf Dual Subtitles the same extension with a new name?**
No. It is a separate extension by a different developer (us), written from scratch.

**Do I need my own translation API key, like some alternatives?**
No. It uses a creator's own translation when there is one, then YouTube's built-in translation, and only then a free public translation service.

**Does it collect my data?**
No. Settings stay in your browser. Caption lines go to translate.googleapis.com only when YouTube has no translation into your language. See the [privacy policy](../dual-subtitles/privacy).

*Not affiliated with or endorsed by YouTube, Google, or the developers of the other extensions named here. Product names are used only to describe them.*
