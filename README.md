# TINCAN — Website

The public website for the **TINCAN** savings & budgeting app, hosted free on
GitHub Pages. Two self-contained static pages, no build step, no dependencies —
the app logo is embedded directly in the HTML, so there are no images or assets
to break.

Live site: **https://tincanexpensetracker.github.io/TinCan/**

## Pages

| File | URL | Purpose |
|------|-----|---------|
| `index.html` | `https://tincanexpensetracker.github.io/TinCan/` | Landing / home page — what TINCAN does, features, how it works |
| `privacy.html` | `https://tincanexpensetracker.github.io/TinCan/privacy.html` | Privacy Policy (Play Store requirement) |

Both pages share the same design (purple/pink theme, light & dark mode toggle).
The home page links to the privacy page; the privacy page contains an
in-page `#delete-account` section describing how users delete their data.

## URLs to use elsewhere

- **App home page / OAuth app domain:** `https://tincanexpensetracker.github.io/TinCan/`
- **Privacy policy** (Play Console → App content → Privacy policy; Google OAuth consent screen):
  `https://tincanexpensetracker.github.io/TinCan/privacy.html`
- **Account / data deletion** (Play Console → App content → Data deletion):
  `https://tincanexpensetracker.github.io/TinCan/privacy.html#delete-account`

> Note: the privacy policy now lives at `privacy.html` (it used to be the site root).
> If you previously registered `.../TinCan/#delete-account`, update it to
> `.../TinCan/privacy.html#delete-account`.

## Publish / update (GitHub Pages — free)

This repo is already published via **Settings → Pages → Deploy from a branch →
`main` / root**. To update:

1. Edit `index.html` and/or `privacy.html`.
2. For privacy-policy changes, bump the **"Last updated"** date near the top of `privacy.html`.
3. Commit & push to `main`:
   ```bash
   git add index.html privacy.html
   git commit -m "Update site"
   git push
   ```
4. GitHub Pages redeploys automatically (~1 minute). Hard-refresh to see changes.

## Editing tips

- **Colours / theme:** the CSS variables under `:root` (light) and `[data-theme="dark"]`
  (dark) at the top of each file control the entire palette.
- **Logo:** embedded as a base64 data URI in the hero `<img>` of each page.
- **Play Store link:** the home page has a "Get it on Google Play — Coming soon"
  button — replace its `href="#"` with the real Play Store URL once the app is live.
- **Contact email:** `customercare@tincan.anonaddy.com` (used in the footer and CTAs).
