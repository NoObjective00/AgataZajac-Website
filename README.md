# Agata Zając — Conductor

Static website. Plain HTML, CSS and JavaScript; no build step.

Version: **v2.1**

## Structure

| File | Purpose |
| --- | --- |
| `index.html` | English site — hero, upcoming, biography, watch, press, orchestras, gallery, contact |
| `fr/`, `es/`, `de/`, `pl/` | The same site, one static page per language |
| `support.js` | Runtime the page loads |
| `image-slot.js` | Image component used by every photograph |
| `orchestra-map.html` | Europe map, loaded in an iframe from the Orchestras section |
| `images/` | Photographs, web-sized |
| `favicon-*.png` | Favicon set (AZ monogram) |
| `CNAME` | Custom domain for GitHub Pages |
| `robots.txt`, `sitemap.xml` | Crawler directives |
| `about.html`, `calendar.html`, `videos.html`, `photos.html`, `press.html`, `contact.html` | Redirect stubs for the previous site's URLs |
| `_redirects` | Cloudflare Pages 301 rules (ignored by GitHub Pages) |
| `404.html` | Not-found page |

## Publishing

All pages share the assets at the root (`support.js`, `images/`, `orchestra-map.html`),
so keep the folder structure exactly as it is.

GitHub Pages: upload the contents of this folder to the repository root, then
Settings → Pages → Deploy from a branch → `main` → `/ (root)`.

Cloudflare Pages: framework preset None, no build command, output directory `/`.
Delete `CNAME` there — Cloudflare sets custom domains in its own dashboard.

## v2.1

- Sticky header fixed (`overflow-x: clip` no longer kills sticky positioning)
- Mobile: nav collapses behind a Menu button, compact ~40px pinned bar
- Licensed recording of the Grieg theme in the hidden game, with CC BY credit
- Safe-area padding for landscape and home-screen-app use

## v1.0.4

- Hidden game: tempo tiers from Largo to Presto, denser notes as it speeds up,
  synthesised Grieg theme with a sound toggle, frame-rate-independent motion

- Map: pinch to zoom, drag to pan, and taps snap to the nearest city
- Zoom buttons for pointer devices

## v1.1.2

- Facebook added to Follow and to the structured-data profile list
- Map fragment and 404 page excluded from search results
- Smaller map pins on mobile

## v1.1.1

- Redirects from the previous site's six inner URLs to the matching sections
- `404.html` for anything else

## v1.1.0

- Five static language pages: `/`, `/fr/`, `/es/`, `/de/`, `/pl/`
- Per-language title, meta description, Open Graph, canonical and hreflang
  cluster; sitemap lists all five with alternates
- Language switcher is now real links between the URLs, so crawlers follow them

## v1.0.3

- SEO/AEO: static title, meta description, canonical URL, Open Graph and
  Twitter cards, Person + MusicEvent structured data, sitemap and robots.txt
- Alt text on every photograph; photography credited to Oliwia Szygulska
- `index.html` is generated from the source by `build-publish.js`

## v1.0.2

- Gallery tap-to-expand on mobile
- Press section shows each outlet's icon
- Hidden encore: twenty taps on the hero portrait

## v1.0.1

- Five languages: EN, FR, ES, DE, PL
- Press section with reviews and interview links
- Interactive Europe map, hover or tap a city for orchestras and programmes
- Mobile: stacked hero copy clear of the portrait, tap-to-expand gallery,
  bottom-docked map card
