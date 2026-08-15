# BOSS New Collection Catalog — PWA

A self-contained Progressive Web App. No backend, no build step — everything
(PDF extraction, Excel parsing, PDF generation) runs in the browser.

## Files
- `index.html` — the app
- `manifest.json` — install/app metadata
- `service-worker.js` — offline caching of the app shell + libraries
- `icons/` — app icons (192, 512, 512 maskable)

## Deploy to GitHub Pages (same flow as BOSS CRM)
1. Create a new GitHub repo, e.g. `boss-new-collection-catalog`.
2. Upload all files in this folder to the repo root, keeping the `icons/`
   folder structure intact.
3. Repo Settings → Pages → Source: **Deploy from branch**, branch `main`,
   folder `/ (root)`.
4. Your app will be live at:
   `https://<your-username>.github.io/boss-new-collection-catalog/`

## Install as an app
- **Desktop (Chrome/Edge):** open the URL → click the install icon in the
  address bar, or use the "Install App" button in the header.
- **iPhone (Safari):** open the URL → Share → **Add to Home Screen**.
- **Android (Chrome):** open the URL → menu → **Install app** (or use the
  "Install App" button).

Once installed it opens full-screen like a native app and keeps working
offline after the first load (your uploaded PDFs/Excel files are processed
locally and are never uploaded anywhere).

## Updating later
Any time you want to change something, edit `index.html` and re-upload it to
the same repo — GitHub Pages updates automatically within a minute or two.
If a device doesn't pick up the change right away, close and reopen the app
(the service worker refreshes cached files in the background).
