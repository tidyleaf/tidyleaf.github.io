---
title: Chrome Autofill Not Working on Some Forms? How to Fix It
description: "Chrome autofill not working on some forms or fields? Turn on address autofill, fix saved profiles, rule out other extensions, and fill the fields Chrome skips."
---

# Chrome autofill not working on some forms or fields

When Chrome fills some forms but skips others, the cause is usually one of four things: autofill is turned off for that kind of info, your saved address is incomplete, another extension (often a password manager) is getting in the way, or the website's form is built in a way Chrome cannot recognize. The first three take a few minutes to fix. The fourth you cannot fix from your side, because Chrome does not detect every field; for those forms, use a form filler that matches fields by their visible label. The steps below go from the quickest check to the last resort.

## Step 1: Check that autofill is on for addresses

Chrome keeps a separate on/off switch for each kind of saved info. If the switch for addresses is off, nothing in an address form will fill, however many addresses you have saved.

Per Google's Chrome help page for autofill, on a computer:

1. Select **More** (the three dots at the top right), then **Passwords and autofill**. Selecting your profile picture and then **Passwords and autofill** also works.
2. Select the type of info that is not filling, such as addresses, payments or contact info.
3. Make sure **Save and fill** is turned on for that type.

The same page says to make sure you are signed in to your Google Account in Chrome, and to check the name and email Chrome gets from your account at myaccount.google.com/personal-info. Menu labels can differ slightly between Chrome versions.

## Step 2: Look for an incomplete or messy saved address

Chrome fills a form from the saved address you pick. If that entry is missing a phone number, a postal code or a country, the matching fields stay empty, and it can look as if autofill "skipped" them when there was simply nothing to put there.

To check, go back to **Passwords and autofill** and open the address info type. Per Google's help page, next to a saved address you select **More**, then **Edit**, make your changes and save. To add a new address, select **Add** at the top right. Things to look for:

- **Blank fields** you assumed were saved, such as a phone number or a second address line.
- **Several similar entries** with different details. Chrome offers one of them, and it may not be the complete one.
- **Details typed into the wrong box**, such as a city in the street field, which sends the right values to the wrong place.

If you are signed in, Google says changes also show up on your other devices signed in to Chrome with the same account, so you fix it once.

## Step 3: Rule out another extension fighting Chrome

Chrome's autofill is not the only thing that tries to fill a form. A password manager, a coupon extension or another form filler can also react when you click into a field, and two tools competing for the same box can leave it empty or show no suggestion at all. Google's help page does not list this as a cause, so treat it as something to test, not a known rule.

A simple way to test it:

1. Open a form where autofill failed in an **Incognito window**. Extensions run in Incognito only if you turned on **Allow in Incognito** for them, so this usually shows how Chrome behaves on its own.
2. If Chrome fills the form there, go back to your normal window and open the extensions page (type `chrome://extensions` in the address bar).
3. Switch off the extensions that touch forms or passwords, one at a time, reloading the form after each. When the fill starts working, you have found the conflict.
4. Check that extension's own settings. Many password managers have an option to stop offering to fill addresses, or to leave the browser's built-in autofill alone. Aim to have one tool handling each kind of info.

## Step 4: Understand why Chrome skips some fields

If the first three steps change nothing and the problem is only on certain sites, the form itself is probably the cause. Chrome decides what a field is from hints in the page's code, not by reading the words next to it the way you do. Google's help page gives two reasons directly: the website "might not be secure enough to get this info from Chrome", and "if the website is secure, Chrome might not detect certain fields in the form."

Chrome's developer blog post on finding form issues with DevTools shows the developer's side. One example field has only `name="n300"`, and DevTools reports that it "doesn't have attributes that are meaningful to the browser", so it does not map to any saved value. The post's sample form shows the mistakes behind this: inputs with no `id` or `name`, an empty `autocomplete` attribute, duplicate IDs, and a label whose `for` does not match any field. It is not a complete rulebook, so treat this as the general picture, not a guarantee of which fields Chrome fills.

In everyday terms, these are the forms that most often get skipped:

- **Custom questions** such as "How did you hear about us?" or "Preferred start date". They have no saved-address equivalent, so Chrome has nothing to offer.
- **Unlabeled or oddly built fields**, where the box has a placeholder but no hint the browser understands.
- **Forms built from custom widgets**, such as a drop-down made out of page elements instead of a real list.
- **Fields that appear after you click**, such as an address form in a pop-up.

No setting on your side changes this. Only the site's developer can fix the form.

## Option: a form filler that matches by label

When the problem is the form, not your settings, a form filler extension helps. It reads each field's visible label, its placeholder and its name, matches them to a value in your own profile, and types the values in for you. Because it works from the label you can see, it can fill some fields Chrome has no hint for, and it can remember answers for one site.

We built one: **Tidyleaf Form Filler**. Disclosure: Tidyleaf is us, and this is our product.

What it does, free:

- **One click or Alt+Shift+F** fills the current page, on any site.
- **Matches fields by label, placeholder, name and autocomplete hint** for name, email, phone, address, city, state, postal code, country, company, job title, website, birthday and username. Custom fields you add yourself are matched by their label, which covers questions Chrome has no equivalent for.
- **Handles text boxes, text areas, drop-down menus, radio buttons, checkboxes and date fields**, including forms built with React and similar frameworks and forms inside same-site iframes.
- **Per-site answers:** fill a form once by hand, press **Save this form**, and next time one click restores every value for that site. A site rule beats your profile on that site.
- **No daily limit and no account.** Profiles stay on your device. Free includes 1 profile and 3 site rules.

It never saves or fills password fields, card numbers, card security codes or one-time codes, so keep those in your browser's password manager.

**Tidyleaf Pro** costs $24 a year or $3.99 a month, with one key for every Tidyleaf extension. It adds unlimited profiles and site rules, JSON backup and restore, and CSV import.

Honest limits: it fills only what it can match, so a question unique to one form still needs you, and you should always read a form before you submit it. It runs on a page only when you click the button, use the popup or press the shortcut, so it does not fill anything in the background. And **the Chrome Web Store listing is pending review**, so until it is approved, check [the Tidyleaf site](https://tidyleaf.github.io) for where to get it. Permissions, privacy and setup are covered on the [Tidyleaf Form Filler page](../form-filler-extension).

## FAQ

**Why does Chrome autofill work on some websites but not others?**
Chrome fills a field only when it can tell what the field is, and it does that from hints in the page's code. Sites that label their fields clearly get filled; sites with unlabeled, custom-built or unusual fields get skipped. Google's help page says Chrome might not detect certain fields in a form.

**How do I turn on address autofill in Chrome?**
On a computer, open the three-dot menu, choose Passwords and autofill, pick the address info type, and turn on Save and fill. Menu labels can differ slightly between Chrome versions.

**Can a password manager stop Chrome autofill from working?**
Possibly; Google does not list it as a cause, but two tools reacting to the same field can interfere. To check, open the form in Incognito, then switch off form-related extensions one at a time in chrome://extensions until the fill returns, and look for a setting in the extension that leaves address filling to the browser.

**Why does Chrome not fill custom questions like "How did you hear about us"?**
Chrome fills from saved info such as addresses, payments and contact details. A custom question has no saved equivalent, so there is nothing for Chrome to offer. A form filler with custom fields, or one that saves your answers for a site, can fill it.

**Is Tidyleaf Form Filler on the Chrome Web Store yet?**
Not yet. The listing is pending review. Until it is approved, check tidyleaf.github.io for where to get it. The free version has no daily limit and includes 1 profile and 3 site rules.

## Related guides

- [How to autofill web forms with multiple profiles in Chrome](autofill-forms-multiple-profiles)
- [Form filler Chrome extension with no daily limit](../form-filler-extension)

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Google. Chrome is a trademark of Google, named only to describe the browser the extension works in.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Why does Chrome autofill work on some websites but not others?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Chrome fills a field only when it can tell what the field is, and it does that from hints in the page's code. Sites that label their fields clearly get filled; sites with unlabeled, custom-built or unusual fields get skipped. Google's help page says Chrome might not detect certain fields in a form."
      }
    },
    {
      "@type": "Question",
      "name": "How do I turn on address autofill in Chrome?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "On a computer, open the three-dot menu, choose Passwords and autofill, pick the address info type, and turn on Save and fill. Menu labels can differ slightly between Chrome versions."
      }
    },
    {
      "@type": "Question",
      "name": "Can a password manager stop Chrome autofill from working?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Possibly; Google does not list it as a cause, but two tools reacting to the same field can interfere. To check, open the form in Incognito, then switch off form-related extensions one at a time in chrome://extensions until the fill returns, and look for a setting in the extension that leaves address filling to the browser."
      }
    },
    {
      "@type": "Question",
      "name": "Why does Chrome not fill custom questions like \"How did you hear about us\"?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Chrome fills from saved info such as addresses, payments and contact details. A custom question has no saved equivalent, so there is nothing for Chrome to offer. A form filler with custom fields, or one that saves your answers for a site, can fill it."
      }
    },
    {
      "@type": "Question",
      "name": "Is Tidyleaf Form Filler on the Chrome Web Store yet?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Not yet. The listing is pending review. Until it is approved, check tidyleaf.github.io for where to get it. The free version has no daily limit and includes 1 profile and 3 site rules."
      }
    }
  ]
}
</script>
