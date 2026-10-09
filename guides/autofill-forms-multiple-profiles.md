---
title: Autofill Web Forms With Multiple Profiles in Chrome
description: How to autofill web forms with multiple profiles in Chrome, such as home, work or test users, using built-in autofill, a password manager or a form filler.
---

# How to autofill web forms with multiple profiles in Chrome

Chrome has no named, switchable form profiles. It can save several addresses and let you pick one per form, and each Chrome profile (the people icon at the top right) keeps its own autofill data. If you want to choose "Work", "Home" or "Test user 3" and fill the whole page from it in one click, you need a password manager with identity entries or a form filler extension that supports several profiles. For QA test data, a short script is often better than any extension. Below are all four routes, what each handles, and where each falls short.

## Option 1: Chrome's built-in autofill (several saved addresses)

Chrome stores addresses under Settings, then Autofill and passwords, then Addresses and more. You can add as many entries as you like, each with a name, organisation, street address, phone and email.

How to use it as "profiles":

1. Add one address entry per identity: your home details, your work details, a family member's.
2. On a form, click into a field Chrome recognises, such as name or street address.
3. Chrome shows a drop-down of your saved entries. Pick one, and Chrome fills the related fields from that entry.

- **Good for:** checkout, delivery and sign-up forms with standard contact and address fields.
- **Limits:** you cannot give entries names of your own. If you are signed in to Chrome, the home and work addresses saved in your Google Account show up with those labels, but any other entry is listed only by its contents, so telling two similar ones apart can be awkward. Chrome fills only the fields it recognises, so custom questions, drop-downs with unusual options, checkboxes and site-specific answers stay empty. Each entry holds one set of contact details, with no custom fields.

### Variant: one Chrome profile per identity

Each Chrome profile has its own saved addresses, passwords, history and extensions. If your "profiles" are really separate lives, such as personal and a client's account, a separate Chrome profile for each keeps them apart completely. The cost is switching windows: you cannot fill a form in one profile's window with another profile's details.

## Option 2: identity entries in a password manager

Many password managers can store identities (name, address, phone, email, sometimes company or date of birth) next to your logins, and offer them when you click a form field.

- **Good for:** people who already use a password manager and want one place for everything, synced across devices.
- **Limits:** identity filling is a side feature, so field matching varies by manager, and custom fields or per-site answers are usually not covered. Check your manager's own help pages for what it fills.

## Option 3: a form filler extension with multiple profiles

A form filler extension reads each field's label, placeholder, name and autocomplete hint, matches it to a value in the profile you selected, and fills the whole page at once. This is the route for named profiles you switch between, custom fields of your own, and forms Chrome's autofill ignores.

Before you pick one, check:

- **How many profiles the free version allows**, and whether there is a daily fill limit.
- **Where profiles are stored:** on your device, synced by Chrome, or in the developer's cloud.
- **Which permissions it asks for.** "Read and change all your data on all websites" lets it run on every page you open. A filler that runs only when you click it does not need that.
- **Whether it skips passwords and card numbers.** A form filler has no reason to hold them.

### Tidyleaf Form Filler

**Tidyleaf Form Filler** is the form filler we built. Disclosure: Tidyleaf is us, and this is our product.

- **Profiles:** the free version has 1 profile and 3 site rules. [Tidyleaf Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf) ($24 a year or $3.99 a month) gives unlimited profiles and site rules. You switch the active profile from a drop-down in the toolbar popup.
- **Filling:** one click on **Fill this page**, or Alt+Shift+F, fills the page from the selected profile, with no daily limit. It recognises name, email, phone, address, city, state, postal code, country, company, job title, website, birthday and username, and matches custom fields you add by their label. It handles text boxes, text areas, drop-downs, radio buttons, checkboxes and date fields, React-style forms and same-site iframes.
- **Site rules:** fill a form by hand once and press **Save this form**; on that site the saved values win over the profile.
{% raw %}- **Pro extras:** JSON backup and restore, CSV import (one row per profile with field names as columns, or rows of Profile, Field, Value), and smart values such as `{{date:+7d}}`, `{{random:red|green|blue}}` and `{{randint:1-100}}`.{% endraw %}
- **Privacy:** it asks only for storage, the active tab and on-demand scripting, and runs only when you click or press the shortcut. Profiles stay in extension storage on your device and are not synced. It never saves or fills passwords, card numbers, card security codes or one-time codes. Details are in its [privacy policy](../form-filler/privacy) and on the [Form Filler page](../form-filler-extension).

**Tidyleaf Form Filler is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Form Filler once it is approved. -->

## Option 4: test data for QA

If you test web apps, "profiles" usually means a set of test users: a valid one, one with a long name, one from another country, one with an edge-case postcode. Three ways to get them:

- **A test-data form filler.** Some extensions type random fake data into every field. Fast for smoke tests, but the values change each time, which makes a bug harder to reproduce.
- **A profile-based form filler.** Save each test user as a named profile and pick one before you fill, so every run uses the same values. With Tidyleaf Pro you can import them from a CSV and use smart values for a date a week from today or a random pick from a list.
- **A script.** For anything you run more than a few times, put the profiles in code. This Playwright example in Python fills a sign-up form from the profile you name:

```python
# pip install playwright && playwright install chromium
import sys
from playwright.sync_api import sync_playwright

PROFILES = {
    "valid":   {"#name": "Ana Lopez", "#email": "ana@example.com", "#zip": "94107"},
    "longname": {"#name": "A" * 120, "#email": "long@example.com", "#zip": "94107"},
    "intl":    {"#name": "Lin Mei", "#email": "lin@example.com", "#zip": "100-0001"},
}

profile = PROFILES[sys.argv[1] if len(sys.argv) > 1 else "valid"]

with sync_playwright() as p:
    browser = p.chromium.launch(headless=False)
    page = browser.new_page()
    page.goto("http://localhost:3000/signup")  # your app's form
    for selector, value in profile.items():
        page.fill(selector, value)
    page.pause()  # inspect, then submit by hand or add page.click("button[type=submit]")
    browser.close()
```

Change the selectors to match your form. Use `example.com` addresses and made-up details for test users, never real people's data.

## Which option should you use?

| You want | Use |
|---|---|
| Your home or work address at checkout, nothing to install | Chrome's saved addresses |
| Two completely separate identities with separate logins | One Chrome profile for each |
| Contact details synced with your passwords | Your password manager's identities |
| Named profiles, custom fields and whole-page fills | A form filler with multiple profiles |
| Repeatable test users for manual QA | A profile-based form filler with CSV import |
| Test users in automated or repeated runs | A Playwright or Selenium script |

## Caveats

- **Autofill fills what it recognises.** Every tool here guesses from field names and labels. Check the form before you submit, especially drop-downs and dates.
- **Some forms reject filled values.** A form can ignore a value set by a script if it listens for different events. If a field looks filled but the form says it is empty, type one character and delete it, or fill that field by hand.
- **Keep payment cards and passwords in the browser or your password manager**, not in a form filler profile.

## FAQ

**Can Chrome autofill have multiple profiles?**
Not named ones. Chrome can save several addresses and lets you pick one from a drop-down on each form, and each Chrome profile has its own separate autofill data. For named profiles you switch between, use a form filler extension or a password manager.

**How do I choose a different address in Chrome autofill?**
Click into a name or address field. Chrome shows your saved addresses; pick the one you want. To add or edit entries, go to Settings, then Autofill and passwords, then Addresses and more.

**How do I autofill custom fields that Chrome ignores?**
Chrome only fills field types it knows. A form filler that lets you add custom fields matched by label, or that remembers what you typed on a specific site, covers the rest.

**What is the best way to fill forms with test data?**
For quick manual checks, a form filler with one saved profile per test user, so values are the same every run. For repeated or automated tests, a script with the test users in code.

## Related

- [Form filler Chrome extension with no daily limit](../form-filler-extension): free form filler options compared, and the privacy checks to run before installing one.

*Tidyleaf is an independent maker of browser extensions. Not affiliated with, endorsed by or sponsored by Google. Chrome is a trademark of Google, named only to describe the browser the extension works in.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Can Chrome autofill have multiple profiles?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Not named ones. Chrome can save several addresses and lets you pick one from a drop-down on each form, and each Chrome profile has its own separate autofill data. For named profiles you switch between, use a form filler extension or a password manager."
      }
    },
    {
      "@type": "Question",
      "name": "How do I choose a different address in Chrome autofill?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Click into a name or address field. Chrome shows your saved addresses; pick the one you want. To add or edit entries, go to Settings, then Autofill and passwords, then Addresses and more."
      }
    },
    {
      "@type": "Question",
      "name": "How do I autofill custom fields that Chrome ignores?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Chrome only fills field types it knows. A form filler that lets you add custom fields matched by label, or that remembers what you typed on a specific site, covers the rest."
      }
    },
    {
      "@type": "Question",
      "name": "What is the best way to fill forms with test data?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "For quick manual checks, a form filler with one saved profile per test user, so values are the same every run. For repeated or automated tests, a script with the test users in code."
      }
    }
  ]
}
</script>
