# Nocturne — documentation and support site

Public site backing the two URLs required by the Shopify Theme Store, set in the theme's
`config/settings_schema.json` under `theme_info`:

| Setting | URL |
|---|---|
| `theme_documentation_url` | https://hamzabilalbaig.github.io/nocturne/docs/ |
| `theme_support_url` | https://hamzabilalbaig.github.io/nocturne/support/ |

This repo is public because GitHub Pages requires it on the free plan. It contains **only
the site** — the theme source stays private.

## Structure

```
_config.yml        site settings, including the support form endpoint
_layouts/          default.html (shell) and page.html (docs, with generated sidebar)
assets/site.css    all styling; palette matches the theme's Nocturne preset
index.md           /          landing
docs.md            /docs/     merchant documentation
support.html       /support/  contact form and support policy
```

## Before submitting the theme

1. **Connect the support form.** `form_endpoint` in `_config.yml` is `REPLACE_ME`, and a
   warning banner shows on `/support/` until it is a real URL. Create the form at
   [Tally](https://tally.so) or [Formspree](https://formspree.io), then:
   - enable **file uploads** without requiring a login — Google Forms cannot do this, its
     upload field forces a Google sign-in, which fails the Theme Store's "no login" rule
   - enable the **auto-responder**, stating the two business day response time
   - confirm the Subject field populates the notification email's subject line
2. **Submit a test message** and check that both the notification and the auto-reply land.
3. **Keep both URLs alive.** They ship inside every copy of the theme, so changing them
   later means pushing a theme update through review.

## Updating the documentation

`docs.md` is a copy of `docs/index.md` from the theme repo with front matter added. When
the theme's docs change, re-copy the body and keep the front matter block.

## Renaming this repo

`baseurl` in `_config.yml` is `/nocturne`. If the repo is renamed, change it to match and
update both URLs in the theme's `settings_schema.json`.
