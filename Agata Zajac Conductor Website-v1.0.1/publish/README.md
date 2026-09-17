# Agata Zając — Conductor

Static website. Plain HTML, CSS and JavaScript; no build step.

Version: **v1.0.1**

## Structure

| File | Purpose |
| --- | --- |
| `index.html` | The whole site — hero, upcoming, biography, watch, press, orchestras, gallery, contact |
| `support.js` | Runtime the page loads |
| `image-slot.js` | Image component used by every photograph |
| `orchestra-map.html` | Europe map, loaded in an iframe from the Orchestras section |
| `images/` | Photographs, web-sized |
| `favicon-*.png` | Favicon set (AZ monogram) |
| `CNAME` | Custom domain for GitHub Pages |

## Publishing

GitHub Pages: upload the contents of this folder to the repository root, then
Settings → Pages → Deploy from a branch → `main` → `/ (root)`.

Cloudflare Pages: framework preset None, no build command, output directory `/`.
Delete `CNAME` there — Cloudflare sets custom domains in its own dashboard.

## v1.0.1

- Five languages: EN, FR, ES, DE, PL
- Press section with reviews and interview links
- Interactive Europe map, hover or tap a city for orchestras and programmes
- Mobile: stacked hero copy clear of the portrait, tap-to-expand gallery,
  bottom-docked map card
