---
title: Netflix dual subtitles, with pinyin and zhuyin
description: Netflix shows one subtitle language at a time. How to get Netflix dual subtitles in Chrome for free, with pinyin or zhuyin, and what works on TV or iPad.
---

# Netflix dual subtitles: two languages at once, with pinyin and zhuyin

Netflix shows one subtitle language at a time, in every app and in the browser, and it has no setting for two. To see two languages together, for example the show's original subtitles on top and Chinese or English underneath, you need a browser extension on a computer. Several free ones exist. This page explains what each route can and cannot do, then describes ours, **Tidyleaf Dual Subtitles for Netflix**, which adds pinyin or zhuyin above Chinese.

## What Netflix can do by itself

- **One subtitle language:** during playback, open the speech-bubble menu (Audio & Subtitles) and pick a language. Picking a second one replaces the first.
- **The languages on offer depend on the title and your region.** The menu usually lists a handful of languages, while the title may have more that are not shown to you.
- **No two-line mode** on the TV app, the phone and tablet apps, or netflix.com.

So the manual workaround is to watch a scene with one language, then rewind and switch. It works for a few lines and gets tiring fast.

## Where dual subtitles can work

| Where you watch | Two subtitle lines? |
|---|---|
| Chrome or Edge on a computer | Yes, with an extension |
| Firefox on a computer | Only with an extension built for Firefox |
| Safari on a Mac | Only with an extension built for Safari |
| Netflix app on TV, iPhone, iPad, Android | No. Extensions cannot run inside the apps |
| TV, via a laptop | Yes, if the laptop runs the extension and you mirror or cable it to the TV |

## Your options

### 1. A free general-purpose language extension

Language-learning extensions such as Language Reactor show two subtitle lines on Netflix along with dictionaries and other study tools, and charge for some extra features. Good if you want a full study environment. Check what the free tier covers today, and read the privacy policy, since these tools see what you watch.

### 2. A small dual-subtitle extension

Several free Chrome and Firefox extensions do just one thing: draw a second subtitle line. They differ in which languages they handle well, whether they use Netflix's own subtitles or a machine translation, and how they handle Chinese. Things to check before you pick one:

1. **Does it use Netflix's own subtitles?** Human-made subtitles beat machine translation. A good extension uses Netflix's tracks and translates only when the title has none in your language.
2. **Does Chinese come out as text?** Netflix often serves Chinese, Japanese and Korean subtitles as images, which an extension cannot restyle, translate or add pinyin to.
3. **Does it keep up** when you seek, skip the intro or move to the next episode?
4. **What does it send, and where?** Look for a privacy policy that names every server it talks to.

### 3. Tidyleaf Dual Subtitles for Netflix (ours)

We built **Tidyleaf Dual Subtitles for Netflix 中英双字幕** for people learning Chinese or English. Disclosure: Tidyleaf is us, and this is our product.

**Free, with no trial timer:**

- Two lines over the player, on films and series, in a window or fullscreen.
- By default the top line is the show's original language and the second is Chinese, or English for Chinese shows. You can pick either line's language: Traditional Chinese (zh-TW), Simplified Chinese (zh-CN), English, Japanese, Korean, Spanish, French, German, Portuguese, Russian, Italian, Arabic, Hindi, Indonesian, Vietnamese, Thai and Turkish.
- **Pinyin or zhuyin (Bopomofo)** printed above Chinese characters.
- Chinese drawn with the right glyph forms for Traditional or Simplified, never in bold, with no stray spaces where Netflix breaks a line.
- Uses Netflix's own subtitles for both lines whenever the title has them, including languages Netflix does not list in your region's menu. It asks Netflix for text versions of the subtitles, so Chinese comes through as text rather than images.
- Only when a title has no subtitles in your second language is that line machine-translated, by a free translation service.
- Keeps in sync when you seek, pause, skip or move to the next episode.
- Font size, top or bottom position, distance from the edge, and hiding the top line, all in the toolbar popup.
- No account and no API key to paste. You need your own Netflix subscription.

**Tidyleaf Pro** ($24 a year or $3.99 a month, [get Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf)) adds:

- Download the subtitles as an SRT file: both lines, the top line only, or the second line only.
- Click any word in the subtitles to save it with its sentence and the moment in the episode.
- A saved-words page with delete and CSV export for Anki.

One Pro key unlocks Pro in every Tidyleaf extension, including [Dual Subtitles for YouTube](youtube-dual-subtitles). The free features above stay free.

**Supported sites:** www.netflix.com, in Chrome on a computer. It does not work in the Netflix apps.

**Privacy, in plain words:** we run no server and collect nothing. Your settings stay in your browser profile, and saved words stay on your device. The extension reads only the subtitle list and playback position on Netflix, not your account, profiles or viewing history. It makes two kinds of requests beyond Netflix: when a title has no subtitles in your second language, the subtitle text goes to translate.googleapis.com to be translated; and if you enter a Pro key, the key goes to Polar, our payment provider, to check it. Full details in the [privacy policy](netflix-subtitles/privacy).

**Tidyleaf Dual Subtitles for Netflix is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Dual Subtitles for Netflix once it is approved. -->

## Caveats that apply to any Netflix dual-subtitle extension

- **The second language must exist somewhere.** If a title has no subtitles in that language, the extension can only machine-translate, which is weaker on slang, names and jokes.
- **Netflix changes its player.** Extensions read data the player loads, so a Netflix update can break them for a while until the maker fixes it.
- **Computer only.** For the couch, play on a laptop and connect it to the TV.

## FAQ

**Can Netflix show two subtitles at once without an extension?**
No. Every Netflix app and netflix.com show one subtitle language at a time. Two lines need a browser extension on a computer.

**Do Netflix dual subtitles work on iPad, Android or a smart TV?**
Not in the Netflix apps, because extensions cannot run inside them. Use a desktop browser, and mirror or cable the computer to the TV if you want the big screen.

**Do Netflix dual subtitles work in Safari or Firefox?**
Only with an extension made for that browser. Tidyleaf Dual Subtitles for Netflix is for Chrome.

**Can I get pinyin on Netflix?**
Not from Netflix itself. Tidyleaf Dual Subtitles for Netflix prints pinyin or zhuyin above Chinese characters, free, on titles with Chinese subtitles or with Chinese chosen as a translated line.

**Is there a free Netflix dual subtitles extension?**
Yes, several, including ours: two lines, pinyin and zhuyin are free with no time limit. Pro adds SRT download and saved words.

More: [how to watch Netflix with two subtitles at once](guides/netflix-two-subtitles-at-once), and the same two-line setup for YouTube in [Tidyleaf Dual Subtitles for YouTube](youtube-dual-subtitles).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Netflix. "Netflix" is a trademark of Netflix, Inc., named only to describe the site the extension works on.*
