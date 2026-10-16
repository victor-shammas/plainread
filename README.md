# Plainread website (GitHub Pages, custom domain)

The static marketing, support and privacy pages for Plainread, an EPUB reader for the Mac. Plain HTML and
one stylesheet (shared with the other apps at victorshammas.com), with no build step, external fonts,
scripts or trackers. The app's source lives in the private repo `victor-shammas/plainread-app`.

| File | Published URL |
|---|---|
| `index.html` | https://victorshammas.com/plainread/ (Marketing URL) |
| `support.html` | https://victorshammas.com/plainread/support.html (Support URL; the app's Help menu opens it) |
| `privacy.html` | https://victorshammas.com/plainread/privacy.html (Privacy Policy URL) |
| `style.css`, `icon.png`, `favicon.png`, `apple-touch-icon.png` | assets (the icons come from `Design/icon_1024.png` in the app repo) |
| `.nojekyll` | tells Pages to serve files as-is |

Keep these paths stable: the app links to `support.html`, and App Store Connect to all three.

## How the URL works

The user site (`victor-shammas.github.io`) has the custom domain `victorshammas.com`, so every public
project repo with Pages turned on is served at `https://victorshammas.com/<repo-name>/`. This repo must be
named `plainread` and needs no `CNAME` file. Pages: Settings › Pages › Deploy from a branch › `main`, `/ (root)`.

## App bar

Every page ends with the shared app bar, one tile per app. When an app is added or a tagline changes,
update the app bar on every page of every app site, and the cards at https://victorshammas.com/apps/.

## At launch

- Replace the "Coming soon" span in `index.html` with the App Store link in the comment above it
  (`https://apps.apple.com/app/idAPP_ID?mt=12`, with the numeric Apple ID from App Store Connect) and
  the price.
- On https://victorshammas.com/apps/, turn Plainread's "Coming soon" pill into a Mac App Store link.
