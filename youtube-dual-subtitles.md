---
title: "YouTube Dual Subtitles Extension for Chrome, Free | Tidyleaf"
description: "A free YouTube dual subtitles extension for Chrome: original captions plus a translation on two lines, in 17 languages, including Chinese with pinyin or zhuyin."
---

# YouTube dual subtitles extension

YouTube shows one subtitle track at a time, so to see two languages at once you need a browser extension that draws a second line over the player. **Tidyleaf Dual Subtitles for YouTube** is ours and is free: it shows the video's own captions on top and a translation underneath, on regular videos and Shorts, with no account. Below is what YouTube can do on its own, what a dual subtitles extension adds, how the main options compare, and the limits to expect from any of them.

**[Add to Chrome, free](https://chromewebstore.google.com/detail/jgjjfglbomhmpeniendnfknpjdpgfmgf)**

## What YouTube can do without an extension

- **One caption track:** the gear icon, then Subtitles/CC, then pick a language.
- **Auto-translate:** in the same menu, choose Auto-translate and a language. This replaces the original line; it does not add a second one.
- **Show transcript:** under the video description. It lists every caption line with its timestamp, in one language, beside the video rather than on it.

If you only need to understand a video, auto-translate is enough. If you are learning a language, you usually want both lines on screen together, and that is what an extension adds.

## How a dual subtitles extension works

The extension reads the same caption data the YouTube player uses, gets a translation of each line, and draws both lines in an overlay on the video, timed to playback. Two things decide how good it is:

1. **Where the translation comes from.** A creator's own translated track is best, YouTube's built-in translation is next, and a machine-translation service is the fallback.
2. **Whether it still gets captions at all.** YouTube changed how its player loads captions, and extensions that fetch them the old way now get an empty answer. If yours shows nothing, see [YouTube dual subtitles not working](guides/youtube-dual-subtitles-not-working).

## Tidyleaf Dual Subtitles for YouTube

Disclosure: Tidyleaf is us, and this is our product.

### Free, with no time limit

- **Two lines over the player** on regular videos and on Shorts: the original captions plus your chosen translation.
- **Translation targets:** Traditional Chinese (zh-TW) and Simplified Chinese (zh-CN), English, Japanese, Korean, Spanish, French, German, Portuguese, Russian, Italian, Arabic, Hindi, Indonesian, Vietnamese, Thai and Turkish.
- **Pinyin or zhuyin (Bopomofo)** above Chinese characters, on the original line, the translated line, or both.
- **Human-made captions first**, falling back to YouTube's auto-generated ones.
- **Translation in the cheapest, most accurate order:** a creator's own translated track, then YouTube's built-in translation, and only then a free machine-translation service. Most videos never touch a third-party server.
- **Stays in sync** when you seek, change playback speed, skip ads or move to the next video.
- **Settings in the toolbar popup:** target language, font size, top or bottom position, distance from the edge, hide the original line, pronunciation style.
- No account, no tracking and no API key to paste.

Default languages: Chinese-language videos are translated into English, and everything else into Traditional Chinese, or the language you pick. YouTube's own captions are hidden while the extension is on and come back when you switch it off in the popup.

### Tidyleaf Pro

**Tidyleaf Pro** costs $24 a year or $3.99 a month and adds:

- **SRT download** of the subtitles: both lines, the original only, or the translation only.
- **Click a word to save it** with its sentence and the video timestamp.
- **A saved-words page** with delete and CSV export for Anki.

One license key unlocks Pro in every Tidyleaf extension. [Get Tidyleaf Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf). Everything in the free list stays free.

### Where it works

YouTube in the browser (www.youtube.com), on Chrome. The Edge and Firefox versions are built and not yet listed. It does not work in the YouTube mobile apps, because phone apps cannot run browser extensions.

### Privacy, in plain words

We collect nothing and run no server. Your settings stay in your browser. The extension makes at most two requests besides YouTube itself: when YouTube has no translation into your language, it sends the caption text (and nothing else) to Google's public translation endpoint, translate.googleapis.com; and if you enter a Pro key, it sends that key to Polar, our payment provider, to check it. Saved words stay on your device. Full details are in the [privacy policy](dual-subtitles/privacy).

### Install

**[Add to Chrome, free](https://chromewebstore.google.com/detail/jgjjfglbomhmpeniendnfknpjdpgfmgf)** Tidyleaf Dual Subtitles for YouTube is on the Chrome Web Store.

## How the options compare

| Option | Two lines on the video | Cost | Notes |
|---|---|---|---|
| YouTube auto-translate | No, one line | Free | Built in; replaces the original line |
| YouTube transcript panel | No, beside the video | Free | Good for reading back a line |
| Language Reactor | Yes | Free tier, paid plan | Also covers Netflix and other sites |
| Immersive Translate | Yes | Free tier, paid plan | Also translates web pages and other video sites |
| Tidyleaf Dual Subtitles | Yes | Free; Pro for SRT and saved words | YouTube only; careful Chinese support (Traditional and Simplified kept apart, pinyin, zhuyin) |

Pick a broader tool if you watch on many sites. Pick ours if you mainly watch YouTube, want Chinese handled carefully, and want the core feature free without a trial.

## Limits every dual subtitles extension shares

- **No captions, no subtitles.** The extension needs a caption track. Auto-generated captions count, and most spoken videos have them, but music-only or silent videos often do not.
- **Live streams are not supported** by ours: on a live video it reports that there are no captions to show. Check other tools before relying on them for live streams.
- **Auto-generated captions make mistakes**, and a translation of a wrong line is also wrong. YouTube marks those tracks "auto-generated" in the subtitle menu; prefer videos with human-made captions when you are studying.
- **Machine translation is literal.** Idioms and slang come through flat. A creator's own translated track, when it exists, is better, which is why ours uses it first.
- **Nothing shows during ads.** YouTube serves no captions during an ad; subtitles return when the video resumes.

## FAQ

**Is there a free YouTube dual subtitles extension?**
Yes. Tidyleaf Dual Subtitles shows two lines, in every language listed above, with pinyin or zhuyin, free with no time limit. Language Reactor and Immersive Translate also have free tiers.

**Is there a YouTube dual subtitles extension for Firefox or Edge?**
Ours is on the Chrome Web Store and not yet listed in the Firefox or Edge stores. Edge installs Chrome Web Store extensions, so it works in Edge too.

**Can I get dual subtitles on the YouTube app on my phone or iPhone?**
Not with an extension: the YouTube apps on iOS and Android do not run browser extensions. On a phone, YouTube's own auto-translate gives you one translated line.

**Why is my YouTube dual subtitles extension not working?**
Most often because YouTube changed how its player loads captions, and the extension now gets an empty caption file. See [what changed and what to use now](guides/youtube-dual-subtitles-not-working).

**Can I watch YouTube with Chinese and English subtitles together?**
Yes. That is the case this extension was built for; see the step-by-step [guide to Chinese and English subtitles on YouTube](guides/youtube-dual-subtitles-chinese-english). For Netflix, see [Tidyleaf Dual Subtitles for Netflix](netflix-dual-subtitles).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by YouTube or Google. "YouTube" is a trademark of Google LLC, used only to describe the site the extension works on.*

<!-- jsonld:auto -->
<script type="application/ld+json">
[
  {
    "@context": "https://schema.org",
    "@type": "FAQPage",
    "mainEntity": [
      {
        "@type": "Question",
        "name": "Is there a free YouTube dual subtitles extension?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Yes. Tidyleaf Dual Subtitles shows two lines, in every language listed above, with pinyin or zhuyin, free with no time limit. Language Reactor and Immersive Translate also have free tiers."
        }
      },
      {
        "@type": "Question",
        "name": "Is there a YouTube dual subtitles extension for Firefox or Edge?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Ours is on the Chrome Web Store and not yet listed in the Firefox or Edge stores. Edge installs Chrome Web Store extensions, so it works in Edge too."
        }
      },
      {
        "@type": "Question",
        "name": "Can I get dual subtitles on the YouTube app on my phone or iPhone?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Not with an extension: the YouTube apps on iOS and Android do not run browser extensions. On a phone, YouTube's own auto-translate gives you one translated line."
        }
      },
      {
        "@type": "Question",
        "name": "Why is my YouTube dual subtitles extension not working?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Most often because YouTube changed how its player loads captions, and the extension now gets an empty caption file. See what changed and what to use now."
        }
      },
      {
        "@type": "Question",
        "name": "Can I watch YouTube with Chinese and English subtitles together?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Yes. That is the case this extension was built for; see the step-by-step guide to Chinese and English subtitles on YouTube. For Netflix, see Tidyleaf Dual Subtitles for Netflix."
        }
      }
    ]
  },
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Tidyleaf Dual Subtitles for YouTube",
    "description": "Two subtitle lines on YouTube: original plus translation. Traditional or Simplified Chinese, pinyin and zhuyin. No account needed.",
    "applicationCategory": "BrowserApplication",
    "operatingSystem": "Chrome",
    "url": "https://tidyleaf.github.io/youtube-dual-subtitles",
    "downloadUrl": "https://chromewebstore.google.com/detail/jgjjfglbomhmpeniendnfknpjdpgfmgf",
    "installUrl": "https://chromewebstore.google.com/detail/jgjjfglbomhmpeniendnfknpjdpgfmgf",
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
