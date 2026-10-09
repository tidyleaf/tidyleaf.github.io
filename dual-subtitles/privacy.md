# Privacy Policy - Tidyleaf Dual Subtitles for YouTube 中英双字幕

Last updated: 2026-10-09 (Pro license check added)

Publisher: Tidyleaf

## Summary

This extension does not collect, store on our servers, sell or share any personal data. We run no server and have no analytics.

## What stays on your device

Your settings (target language, font size, position, whether to show the original line, pronunciation style, and the optional Pro license key) are saved in the browser's synced extension storage (`storage.sync`), in your browser profile, and your browser syncs them across your own devices if you have its sync turned on. We cannot see them.

## Network requests

1. **YouTube.** On youtube.com the extension asks YouTube for the caption data of the video you are watching, the same request the YouTube player makes itself. That is a request between your browser and YouTube and is covered by YouTube's own policies.
2. **Translation fallback.** If YouTube has no translation of a video's captions into the language you chose, the extension sends the text of those caption lines to `translate.googleapis.com` to be translated, in batches, and shows the result. Only the caption text and the target language code are sent, with no cookies, account details, video address or other identifier added by the extension. Google's servers receive your IP address as any web request does and handle it under Google's privacy policy. 

3. **Pro license check.** Only if you enter a Pro license key: the extension sends that key, together with Tidyleaf's Polar organization id, to `api.polar.sh` (Polar, our payment provider) to ask whether the key is valid, when you paste it and then at most once a day. Nothing else is sent: no video, caption text, browsing data or other identifier is included. Polar receives your IP address as any web request does and handles it under Polar's privacy policy. The extension keeps the last answer on your device so Pro keeps working for up to 7 days without a connection. Without a key, this request is never made.

Apart from YouTube, these two (translation fallback and license check) are the only requests the extension makes.

## What we do not do

- No collection of browsing history, video titles, watch history, or account information.
- No advertising, tracking pixels, fingerprinting, or analytics.
- No remote code: everything the extension runs ships inside the package.
- No sale or transfer of data to third parties.

## Pro features

Saved words (a Pro feature) are stored in the browser's extension storage (`storage.local`) on your device only: the word, its sentence, the translation line shown with it, the video title, id and timestamp. They are not synced and not sent anywhere; you can delete them or export them as a CSV file yourself from the saved-words page. The SRT download is built on your device from captions already in the page and saved by your browser.

## Changes and contact

Changes will be posted at this address with a new date. Questions: contact the publisher through the support link on the store listing.
