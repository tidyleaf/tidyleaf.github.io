# Privacy Policy - Tidyleaf Dual Subtitles for Netflix 中英双字幕

Last updated: 2026-10-09

Publisher: Tidyleaf

## Summary

This extension does not collect, store on our servers, sell or share any personal data. We run no server and have no analytics.

## What stays on your device

Your settings (the languages of the two subtitle lines, font size, position, whether to show the top line, pronunciation style, and the optional Pro license key) are saved in the browser's synced extension storage (`storage.sync`), in your browser profile, and your browser syncs them across your own devices if you have its sync turned on. We cannot see them.

## What the extension reads on netflix.com

On netflix.com the extension reads the list of subtitle tracks from the data the Netflix player loads for the title you are watching, and the playback position of the video. When the player asks Netflix for that data, the extension adds a request for text versions of the subtitles and for every subtitle language the title has. It does not read your account, profiles, viewing history or payment details, and it keeps nothing it reads after you leave the page.

## Network requests

1. **Netflix.** The extension downloads the two subtitle files you chose from Netflix's servers, using the addresses Netflix's own player received. That is a request between your browser and Netflix and is covered by Netflix's own policies.
2. **Translation fallback.** If the title has no Netflix subtitles in the language you chose for the second line, the extension sends the text of the top-line subtitles to `translate.googleapis.com` to be translated, in batches, and shows the result. Only the subtitle text and the target language code are sent, with no cookies, account details, title name or other identifier added by the extension. Google's servers receive your IP address as any web request does and handle it under Google's privacy policy.
3. **Pro license check.** Only if you enter a Pro license key: the extension sends that key, together with Tidyleaf's Polar organization id, to `api.polar.sh` (Polar, our payment provider) to ask whether the key is valid, when you paste it and then at most once a day. Nothing else is sent: no title, subtitle text, browsing data or other identifier is included. Polar receives your IP address as any web request does and handles it under Polar's privacy policy. The extension keeps the last answer on your device so Pro keeps working for up to 7 days without a connection. Without a key, this request is never made.

Apart from Netflix, these two (translation fallback and license check) are the only requests the extension makes.

## What we do not do

- No collection of browsing history, viewing history, titles watched, or account information.
- No advertising, tracking pixels, fingerprinting, or analytics.
- No remote code: everything the extension runs ships inside the package.
- No sale or transfer of data to third parties.

## Pro features

Saved words (a Pro feature) are stored in the browser's extension storage (`storage.local`) on your device only: the word, its sentence, the other subtitle line shown with it, the title name, the Netflix title id and the time in the episode. They are not synced and not sent anywhere; you can delete them or export them as a CSV file yourself from the saved-words page. The SRT download is built on your device from subtitles already loaded in the page and saved by your browser.

## Changes and contact

Changes will be posted at this address with a new date. Questions: contact the publisher through the support link on the store listing.
