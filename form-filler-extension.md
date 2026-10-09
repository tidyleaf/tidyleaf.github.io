---
title: Form Filler Chrome Extension With No Daily Limit - Tidyleaf
description: A form filler Chrome extension that fills any web form from profiles saved on your device, with no daily limit and no account. Free options compared.
---

# Form filler Chrome extension with no daily limit

A form filler Chrome extension types your saved details (name, email, phone, address and your own custom fields) into the form on the page you are on, in one click. Chrome can already fill basic address fields on its own, so you only need an extension when you want more: several profiles, custom fields, drop-downs and checkboxes, or a site that should get the same answers every time. Below are the free options, what each one is good for, and what to check before you give any extension your personal details.

## Option 1: Chrome's built-in autofill (free, nothing to install)

Chrome saves addresses and contact details under Settings, then Autofill and passwords, then Addresses and more. When you click into a field Chrome recognises, it offers a saved address and fills the related fields.

- **Good for:** checkout and sign-up forms with standard name, email, phone and address fields.
- **Not good for:** fields Chrome does not recognise, custom questions, or remembering what you entered on one particular site. You click into a field and pick a saved entry each time, and anything Chrome does not recognise stays empty.

## Option 2: your password manager's identity entries

Many password managers can store an identity (name, address, phone, email) alongside your passwords and fill it into forms.

- **Good for:** people who already use a password manager and want one place for everything.
- **Not good for:** custom fields or per-site answers. Identity filling is usually a side feature, and how well it matches fields varies by manager.

## Option 3: a form filler extension (whole page, your own fields)

A dedicated form filler reads each field's label, placeholder and name, matches it to a value from your profile, and fills the whole page in one go. Some are built for developers and type random test data instead of your details; if you test web apps, search for a "fake" or "dummy" form filler. If you want your own details filled, look for one that keeps profiles on your device.

**Tidyleaf Form Filler** is the one we built for this. Disclosure: Tidyleaf is us, and this is our product. It has no daily fill limit, needs no account and keeps everything on your device.

### What it does, free

- **One click or Alt+Shift+F** fills the current page. It works on any site.
- **Recognises common fields** from the label, placeholder, name and autocomplete hint: name, email, phone, address, city, state, postal code, country, company, job title, website, birthday and username. Custom fields you add are matched by their label.
- **Handles most field types:** text boxes, text areas, drop-down menus, radio buttons, checkboxes and date fields. It also fills forms built with React and similar frameworks, and forms inside same-site iframes.
- **"Save this form":** fill a form once by hand, press Save this form, and the extension remembers every value for that site. Next time one click restores it. A site rule beats your profile on that site.
- **No daily limit.** Free includes 1 profile and 3 site rules.

### What it never touches

It never saves and never fills password fields, card numbers, card security codes or one-time codes. It recognises them by field type, autocomplete attribute and label, and skips them every time. Keep those in your browser's password manager.

### Tidyleaf Pro

**Tidyleaf Pro** ($24 a year or $3.99 a month, one key for every Tidyleaf extension) adds:

- Unlimited profiles and site rules.
- JSON backup and restore of all profiles and rules, and CSV import to bring profiles over from another form filler (one row per profile with field names as columns, or rows of Profile, Field, Value).
{% raw %}- Smart values: a date relative to today (`{{date:+7d}}`), a random pick from a list (`{{random:red|green|blue}}`) or a random number (`{{randint:1-100}}`). In the free version these are skipped, never typed literally.{% endraw %}

[Get Tidyleaf Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf), then paste the license key in the extension's Options.

**Tidyleaf Form Filler is coming to the Chrome Web Store.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with the Chrome Web Store URL for Tidyleaf Form Filler once it is approved. -->

### How to use it

1. Open the extension's Options and enter your details in a profile.
2. Open a page with a form, click the extension icon and press **Fill this page** (or press Alt+Shift+F).
3. Optional: fill a form by hand and press **Save this form** to make a rule for that site.

## Which option should you use?

| You want | Use |
|---|---|
| Your address at checkout, nothing to install | Chrome's built-in autofill |
| Contact details from the same app as your passwords | Your password manager's identity entries |
| Random test data while developing a web app | A test-data ("fake") form filler |
| Your own details, custom fields and per-site answers, filled in one click | A profile-based form filler such as Tidyleaf Form Filler |
| Several profiles (home, work, a client) or a backup of them | A form filler with multiple profiles and export (Tidyleaf Pro) |

## Privacy: what to check before you install any form filler

A form filler holds your name, address and phone number, so look at three things on its store page and privacy policy:

1. **Where profiles are stored.** On your device, or in the developer's cloud account?
2. **What permissions it asks for.** "Read and change all your data on all websites" means it can run on every page you visit. A filler that only runs when you click it does not need that.
3. **What it sends over the network.** A filler has no reason to send your form values anywhere.

Tidyleaf Form Filler asks only for storage, the active tab and on-demand scripting, with no access to all sites. It runs on a page only when you click the button, use the popup or press the shortcut. Profiles and site rules are kept in Chrome's extension storage on your device, are not synced, and are deleted if you remove the extension. Filling and saving make no network request. The only request it ever makes is the Pro license check, which sends just your key to Polar, our payment provider, about once a day; without a key it contacts no one. Full details are in its [privacy policy](form-filler/privacy).

## FAQ

**What is the best free form filler for Chrome?**
For standard address fields, Chrome's own autofill is free and already installed. If you want the whole page filled in one click, custom fields or per-site answers, use a form filler extension, and pick one that stores profiles on your device and does not cap daily fills. Tidyleaf Form Filler's free version has no daily limit, with 1 profile and 3 site rules.

**Is there a form filler extension with no daily limit?**
Yes. Some form fillers limit how many fills the free version allows per day. Tidyleaf Form Filler has no fill limit in either the free or the Pro version; Pro lifts the profile and site-rule limits instead.

**Can a form filler extension fill Google Forms or job applications?**
A profile-based filler fills fields it can match by label, so it handles the name, email, phone and address parts of most application forms, and Save this form remembers your answers for a site you return to. Questions unique to one form still need you, and you should always read the form before you submit it.

**Can I keep more than one profile, such as home and work?**
Yes, with Tidyleaf Pro, which allows unlimited profiles. See [how to autofill forms with multiple profiles](guides/autofill-forms-multiple-profiles) for the general approach in any browser.

**Does it work in Edge or Firefox?**
The same extension is being prepared for Microsoft Edge Add-ons and Firefox Add-ons as well as the Chrome Web Store. Until those listings are live, check [tidyleaf.github.io](https://tidyleaf.github.io) for where it is available.

Other Tidyleaf extensions: [AI Chat Exporter](ai-chat-exporter) for saving ChatGPT, Claude and Gemini chats, and [Folders for ChatGPT and Claude](chatgpt-claude-folders).

*Tidyleaf is an independent maker of browser extensions. Not affiliated with or endorsed by Google or any other form-filler product. Chrome is a trademark of Google LLC, named only to describe the browser the extension works in.*

<!-- jsonld:auto -->
<script type="application/ld+json">
[
  {
    "@context": "https://schema.org",
    "@type": "FAQPage",
    "mainEntity": [
      {
        "@type": "Question",
        "name": "What is the best free form filler for Chrome?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "For standard address fields, Chrome's own autofill is free and already installed. If you want the whole page filled in one click, custom fields or per-site answers, use a form filler extension, and pick one that stores profiles on your device and does not cap daily fills. Tidyleaf Form Filler's free version has no daily limit, with 1 profile and 3 site rules."
        }
      },
      {
        "@type": "Question",
        "name": "Is there a form filler extension with no daily limit?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Yes. Some form fillers limit how many fills the free version allows per day. Tidyleaf Form Filler has no fill limit in either the free or the Pro version; Pro lifts the profile and site-rule limits instead."
        }
      },
      {
        "@type": "Question",
        "name": "Can a form filler extension fill Google Forms or job applications?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "A profile-based filler fills fields it can match by label, so it handles the name, email, phone and address parts of most application forms, and Save this form remembers your answers for a site you return to. Questions unique to one form still need you, and you should always read the form before you submit it."
        }
      },
      {
        "@type": "Question",
        "name": "Can I keep more than one profile, such as home and work?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "Yes, with Tidyleaf Pro, which allows unlimited profiles. See how to autofill forms with multiple profiles for the general approach in any browser."
        }
      },
      {
        "@type": "Question",
        "name": "Does it work in Edge or Firefox?",
        "acceptedAnswer": {
          "@type": "Answer",
          "text": "The same extension is being prepared for Microsoft Edge Add-ons and Firefox Add-ons as well as the Chrome Web Store. Until those listings are live, check tidyleaf.github.io for where it is available."
        }
      }
    ]
  },
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Tidyleaf Form Filler",
    "description": "Fill any web form in one click from profiles saved on your device. No daily limit, no account, nothing sent anywhere.",
    "applicationCategory": "BrowserApplication",
    "operatingSystem": "Chrome",
    "url": "https://tidyleaf.github.io/form-filler-extension",
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
