# Great Lakes Label — Email Signature Assets

**Public** image host for the [email-signatures](https://github.com/Great-Lakes-Label/email-signatures)
project. Files here are served over GitHub Pages so employee signatures can
reference them by a stable URL.

> This repo is intentionally **public** and contains **images only** — no
> employee data. Logos and banners are already public (they ride along in every
> outgoing email). All private data and tooling stays in the private
> `email-signatures` repo.

## Why this exists

Signatures that **embed** images (base64) must be rebuilt and re-pasted by every
employee whenever an image changes. Images hosted here are **linked** by URL, so
updating one is a one-file swap that reaches every already-installed signature —
no rebuild, no re-paste.

## Live URLs (GitHub Pages)

```
https://great-lakes-label.github.io/email-signature-assets/banners/current.jpg
```

## How to update the banner everywhere

1. Replace `banners/current.jpg` with the new image (keep the **same filename**).
2. Commit and push.
3. Done — every signature that points at `current.jpg` shows the new banner the
   next time the email client refreshes images.

Notes:
- Keep the same dimensions (recommended width **600px**) so layouts don't shift.
- Email clients cache images; a change can take a while to appear for some
  recipients. For an instant, guaranteed swap, use a dated filename
  (`banners/2026-08.png`) and update the URL in the signature project's
  `brand.json` instead.

## Layout

```
banners/
  current.jpg     # the active banner (swap this file to update everywhere)
.nojekyll         # serve files as-is (no Jekyll processing)
```
