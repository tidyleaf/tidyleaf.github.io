---
title: YouTube with Chinese and English subtitles at the same time
description: YouTube shows one caption track at a time. Here is how to watch with English and Chinese (Traditional or Simplified) subtitles together, with pinyin or zhuyin, and what each option costs.
---

# Watch YouTube with Chinese and English subtitles at the same time

YouTube's player shows one caption track at a time. You can switch it to English, or turn on auto-translate to Chinese, but not both at once. If you are learning Chinese or English, that single line is the problem: you either read the language you are learning and miss words, or read your own and stop learning.

What you want is two lines: the video's own captions on top and the translation underneath. YouTube cannot do that by itself, so it takes a browser extension.

## What YouTube can do without an extension

- **Captions in one language:** Settings (the gear), Subtitles/CC, pick a track.
- **Auto-translate into one language:** in the same menu, choose Auto-translate and pick Chinese (Traditional) or Chinese (Simplified). This replaces the original line; it does not add a second one.
- **The transcript panel:** under the video description, "Show transcript" lists the captions with timestamps. Handy for reading back a line, but it is one language and sits beside the video, not on it.

## Two lines on the video: Tidyleaf Dual Subtitles for YouTube

We built **Tidyleaf Dual Subtitles for YouTube 中英双字幕** for exactly this. Disclosure: Tidyleaf is us, and this is our product.

Free, with no account and no API key to paste:

- **Two lines over the player**, on regular videos and on Shorts: the video's captions plus your chosen translation.
- **Traditional Chinese (zh-TW) and Simplified Chinese (zh-CN) are first-class targets**, along with English, Japanese, Korean, Spanish, French, German, Portuguese, Russian, Italian, Arabic, Hindi, Indonesian, Vietnamese, Thai and Turkish.
- **Pinyin or zhuyin (Bopomofo)** above the Chinese characters, on the original line, the translated line, or both.
- Uses the video's **human-made captions** when they exist and falls back to YouTube's auto-generated ones.
- For the translation it uses, in order: a creator's own translated track, then YouTube's built-in translation, and only then a free machine-translation service. Most videos never touch a third-party server.
- Keeps up when you seek, change playback speed, skip ads or move to the next video.
- Font size, top or bottom position, distance from the edge, and hiding the original line are all in the toolbar popup.

Sensible defaults: Chinese-language videos are translated into English, and everything else into Traditional Chinese (or your pick). If your browser is set to Traditional Chinese, that is the starting choice.

**Tidyleaf Pro** ($24 a year or $3.99 a month) adds SRT download of the subtitles (both lines, original only or translation only), click-a-word saving with the sentence and timestamp, and a saved-words page with CSV export for Anki. Everything in the free list stays free.

**[Add to Chrome, free](https://chromewebstore.google.com/detail/jgjjfglbomhmpeniendnfknpjdpgfmgf)** Tidyleaf Dual Subtitles for YouTube is on the Chrome Web Store.

## Other extensions that do this

To be fair to the alternatives: Language Reactor and Immersive Translate also show two subtitle lines on YouTube, and both cover more sites (Netflix, web pages) with larger paid plans. Pick ours if you mainly watch YouTube, want Chinese done carefully (Traditional and Simplified kept apart, pinyin or zhuyin), and want the core feature free without a trial.

## Tips for learning with two lines

- **Hide the original line** once you can follow most of it, and turn it back on when you get lost. The toggle is in the popup.
- **Turn on zhuyin or pinyin only for the Chinese line** you are learning, so the English line stays clean.
- **Slow the video to 0.75x.** The subtitles stay in sync at any speed.
- **Prefer videos with human-made captions.** Auto-generated captions are less accurate, and translation errors stack on top of them. YouTube marks those tracks "auto-generated" in the subtitle menu.

## FAQ

**Is it free?**
Yes. Two-line subtitles, every language above and pinyin or zhuyin are free with no time limit. Pro adds SRT download and saved words.

**Does it work on videos without captions?**
No. It needs a caption track, but YouTube's auto-generated captions count, and most spoken videos have them.

**Does it send my viewing to anyone?**
No data is collected. Settings live in your browser. Only when YouTube has no translation into your language are the caption lines sent to a public translation endpoint (translate.googleapis.com) to be translated. See the [privacy policy](../dual-subtitles/privacy).

**My old dual-subtitle extension stopped working. Why?**
See [YouTube Dual Subtitles not working? What changed and what to use](youtube-dual-subtitles-not-working).

*Not affiliated with or endorsed by YouTube or Google. "YouTube" is a trademark of Google LLC, used only to describe the site the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Is it free?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. Two-line subtitles, every language above and pinyin or zhuyin are free with no time limit. Pro adds SRT download and saved words."
      }
    },
    {
      "@type": "Question",
      "name": "Does it work on videos without captions?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. It needs a caption track, but YouTube's auto-generated captions count, and most spoken videos have them."
      }
    },
    {
      "@type": "Question",
      "name": "Does it send my viewing to anyone?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No data is collected. Settings live in your browser. Only when YouTube has no translation into your language are the caption lines sent to a public translation endpoint (translate.googleapis.com) to be translated. See the privacy policy."
      }
    },
    {
      "@type": "Question",
      "name": "My old dual-subtitle extension stopped working. Why?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "See YouTube Dual Subtitles not working? What changed and what to use."
      }
    }
  ]
}
</script>
