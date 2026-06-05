# baba-gah — liquid chalk store

Static single-page storefront. The repository root **is** the deployable site
(`index.html` plus its assets), so no build step is required.

## Deploy on Cloudflare Pages
1. Push this repo to GitHub (see below).
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Pick this repository.
4. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/`
5. **Save and Deploy.**

## What's here
- `index.html` — the site (pre-compiled, no in-browser build needed)
- `vendor/` — self-hosted React + fonts (no Google Fonts / Babel CDN dependency)
- `*.js` — bundled meshes / configs (`baba-mesh`, `bottle-obj`, `bottle-config`,
  `baba-wordmark`, `rock-config`)
- `*.svg`, `*.png` — logo, wordmark, and icons

The only external runtime dependency is **three.js from unpkg** (the 3D models);
everything else is self-hosted.

## Push to GitHub
```sh
git remote add origin https://github.com/<you>/baba-gah-store.git
git push -u origin main
```
