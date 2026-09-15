# Cathode — documentation and support site

Public site backing the two URLs required by the Shopify Theme Store, set in the theme's
`config/settings_schema.json` under `theme_info`:

| Setting | URL |
|---|---|
| `theme_documentation_url` | https://hamzabilalbaig.github.io/cathode/docs/ |
| `theme_support_url` | https://hamzabilalbaig.github.io/cathode/support/ |

This repo is public because GitHub Pages requires it on the free plan. It contains **only
the site** — the theme source stays private.

## Structure

```
_config.yml        site settings, including the support form endpoint
_layouts/          default.html (shell) and page.html (docs, with generated sidebar)
assets/site.css    all styling; palette matches the theme's Cathode preset
index.md           /          landing
docs.md            /docs/     merchant documentation
support.html       /support/  contact form and support policy
thanks.html        /thanks/   where FormSubmit redirects after a submission
```

## Before submitting the theme

1. **Connect the support form.** It posts to [FormSubmit](https://formsubmit.co) — free,
   no signup, 10MB of attachments per submission, and an auto-responder. `formsubmit_id`
   in `_config.yml` is `REPLACE_ME`, and a warning banner shows on `/support/` until it
   is set.
   - Set it to your support email, push, and submit one test message from `/support/`.
   - FormSubmit emails you an activation link and a masked token. Click the link, then
     replace the email in `_config.yml` with the token so your address is not exposed
     in the page HTML.
   - **Do not add `_captcha=false`.** FormSubmit's auto-responder does not fire when the
     captcha is disabled, and the Theme Store requires an auto-responder.
2. **Test it end to end.** Submit a real message and confirm three things land: the
   notification in your inbox with the chosen Subject as its subject line, the
   auto-reply in the sender's inbox, and an attached screenshot.
3. **Keep both URLs alive.** They ship inside every copy of the theme, so changing them
   later means pushing a theme update through review.

## Updating the documentation

`docs.md` is a copy of `docs/index.md` from the theme repo with front matter added. When
the theme's docs change, re-copy the body and keep the front matter block.

## Renaming this repo

`baseurl` in `_config.yml` is `/cathode`. If the repo is renamed, change it to match and
update both URLs in the theme's `settings_schema.json`.
