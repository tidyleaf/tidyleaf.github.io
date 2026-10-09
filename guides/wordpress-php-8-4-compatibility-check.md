---
title: How to check WordPress plugins and themes for PHP 8.4 compatibility
description: Before you switch a WordPress site to PHP 8.4, find out which plugins and themes will break. Three ways to check, including one that runs on hosts that disable exec().
---

# How to check WordPress plugins and themes for PHP 8.4 compatibility

Your host is moving you to PHP 8.4, or you want the speed and security updates, and you need to know one thing first: which of your plugins and themes will break. WordPress core is ready for PHP 8.4. The risk is in plugins and themes, especially old, premium or custom ones that nobody has updated in a while.

There are three ways to find out, from most to least effort.

## Option 1: a staging site on PHP 8.4 (the final word)

Copy the site to staging (most hosts have a one-click staging copy), switch the staging copy to PHP 8.4, turn on `WP_DEBUG` and `WP_DEBUG_LOG`, then click through the pages, forms, checkout and admin screens you rely on. Read `wp-content/debug.log` for fatal errors and deprecation notices.

- **Good for:** proof. Nothing beats running the real code.
- **Not good for:** coverage. It only finds what you click on. A broken file that loads only on a rare page, a cron job or a payment callback stays hidden until a visitor hits it.

That is why it pays to scan the code first, and then test what the scan points at.

## Option 2: PHPCompatibility on the command line (for developers)

[PHPCompatibility](https://github.com/PHPCompatibility/PHPCompatibility) is the open-source rule set for PHP_CodeSniffer that most checkers are built on. Run it on a copy of `wp-content`:

```bash
mkdir phpcompat-check && cd phpcompat-check
cp -r /path/to/your/site/wp-content .
composer init --no-interaction --name=me/phpcompat-check
composer config --no-plugins allow-plugins.dealerdirect/phpcodesniffer-composer-installer true
composer require --dev "phpcompatibility/php-compatibility:dev-develop" dealerdirect/phpcodesniffer-composer-installer
vendor/bin/phpcs -p --standard=PHPCompatibility --runtime-set testVersion 8.4 --extensions=php wp-content/plugins wp-content/themes
```

The output lists each file with line numbers, for example:

```text
 2 | WARNING | Implicitly marking a parameter as nullable is deprecated since PHP 8.4. ...
 3 | ERROR   | Curly brace syntax for accessing array elements and string offsets has been deprecated in PHP 7.4 and removed in PHP 8.0. Found: $s{0}
 4 | ERROR   | Function get_magic_quotes_gpc() is deprecated since PHP 7.4 and removed since PHP 8.0
```

Use the development line (`dev-develop`): as of October 2026 the latest stable release of PHPCompatibility is 9.3.5 from 2019, which predates PHP 8 and misses the 8.x changes; version 10 is still in alpha. The installer package registers the standard with PHP_CodeSniffer, so `--standard=PHPCompatibility` is found. Expect some false positives from code that only runs on old PHP versions behind a version check.

- **Good for:** developers with shell access and Composer.
- **Not good for:** most site owners, and managed hosts without SSH.

## Option 3: a checker plugin inside WordPress

The best-known plugin for this, WP Engine's PHP Compatibility Checker (about 200,000 installs), now carries a "no longer maintained" notice on WordPress.org and is tested only up to WordPress 6.4. Its description says it checks up to PHP 8.0, and its reviews describe scans that time out or hang. Other scanners rely on `exec()` to run a command-line tool, which many managed and shared hosts disable.

We built **Tidyleaf PHP Compatibility Checker** to fill that gap. Disclosure: Tidyleaf is us, and this is our plugin. It is free.

- **Checks PHP 7.4, 8.0, 8.1, 8.2, 8.3 and 8.4**, using PHP_CodeSniffer and the current development line of PHPCompatibility, with the WordPress-specific exclusions of PHPCompatibilityWP. It covers the 8.1 to 8.4 changes, including implicitly nullable parameters, `${}` string interpolation, `E_STRICT` and the `utf8_encode()` deprecation.
- **Runs on any host.** The scan runs inside WordPress, with no `exec()` or `shell_exec()`, and the plugin makes no external requests. Your code is never sent anywhere.
- **Checks every plugin and theme you have**, premium, custom and abandoned code included, because it reads the files on your server rather than looking plugins up in a database.
- **Does not time out.** Large sites are scanned in short background batches, progress is saved after every file, and a file too big for the server is skipped and reported instead of stopping the scan.
- **Results you can act on:** errors (code that fails on the target version) and warnings (deprecations that still run but log notices), each with file, line, the reason and a plain-English fix hint. If an update is waiting for that plugin, the report says so.
- **CSV report** to send to a plugin author, developer or client.
- **WP-CLI:** `wp phpcompat scan --version=8.4` prints a summary per plugin and theme, takes `--scope=active` and `--format=csv|json`, and exits with status 1 when it finds errors, so it can gate a deploy or CI job.

How we tested it: on a WordPress 7.1 site running PHP 8.4, we scanned two abandoned plugins with known PHP 8 breakage, two maintained clean plugins, WooCommerce (3,664 PHP files) and Plugin Check. The files it flagged as unparseable on PHP 8 were exactly the files that PHP 8.4's own `php -l` rejects, no more and no fewer, and the clean plugins came back with zero findings.

**Tidyleaf PHP Compatibility Checker is in review for the WordPress.org plugin directory.** Until it is listed, see [tidyleaf.github.io](https://tidyleaf.github.io).
<!-- TODO(store-link): replace the line above with https://wordpress.org/plugins/tidyleaf-php-compatibility-checker/ once the plugin is approved. -->

## Reading the results

- **Errors first.** An error means code that fails on the target version: a removed function, removed syntax that stops a file from loading, or changed behaviour. A file that cannot be parsed is a fatal error the moment anything includes it.
- **Then check for updates.** Most findings in maintained plugins disappear after an update.
- **Warnings can wait,** but not forever. A deprecation still runs on PHP 8.4 and logs a notice; it will break in a later version.
- **Verify on staging.** A static scan reads code without running it. Code used only on old PHP versions, behind a version check or `function_exists()`, can still be reported, and problems that appear only at run time, such as passing `null` to a built-in function, cannot be seen. Treat the report as the list to test, then use Option 1 on those plugins.

## What changed in PHP 8.4 that breaks old code

- **Implicitly nullable parameters are deprecated.** `function f(Foo $x = null)` now logs a deprecation; it should be `?Foo $x = null`.
- **`E_STRICT` is deprecated**, along with code that still references it.
- Older removals still catch abandoned plugins: curly-brace string and array offsets (`$str{0}`) stopped parsing in PHP 8.0, and functions such as `get_magic_quotes_gpc()` and the `mcrypt_*` family are gone.

## FAQ

**Is WordPress itself compatible with PHP 8.4?**
Recent WordPress releases run on PHP 8.4; we test the checker on WordPress 7.1 with PHP 8.4. The question is your plugins and themes.

**Does the scan slow down my site?**
It works in short batches, driven by the admin page while it is open and by WP-Cron when you leave it, so no single request runs long. WP-Cron runs alongside page loads, so on a busy shop start the scan at a quiet time, or use WP-CLI.

**Does it fix the problems?**
No. It tells you where they are and how to fix them. Updating the plugin is usually the fix.

*Not affiliated with WP Engine, WordPress.org or the PHPCompatibility project. Names are used only to describe the tools.*

<!-- jsonld:auto -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Is WordPress itself compatible with PHP 8.4?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Recent WordPress releases run on PHP 8.4; we test the checker on WordPress 7.1 with PHP 8.4. The question is your plugins and themes."
      }
    },
    {
      "@type": "Question",
      "name": "Does the scan slow down my site?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "It works in short batches, driven by the admin page while it is open and by WP-Cron when you leave it, so no single request runs long. WP-Cron runs alongside page loads, so on a busy shop start the scan at a quiet time, or use WP-CLI."
      }
    },
    {
      "@type": "Question",
      "name": "Does it fix the problems?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. It tells you where they are and how to fix them. Updating the plugin is usually the fix."
      }
    }
  ]
}
</script>
