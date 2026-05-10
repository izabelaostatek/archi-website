# Izabela Ostatek — Architecture & Interior Design Website

## What this is
A static HTML/CSS/JS portfolio website for Izabela Ostatek, an architect and interior designer based in London. The site also serves as a property marketing platform for Mexican real estate developments. Hosted on GitHub Pages at `izabelaostatek/archi-website`.

## Tech stack
- Pure HTML, CSS, JS — no framework, no build step
- One shared stylesheet: `css/style.css`
- One shared script: `js/main.js` (handles nav scroll, hamburger menu, fade-in animations)
- Fonts: Cormorant Garamond (headings, serif, elegant), Inter (body, sans-serif)
- Colour palette: `--bg: #fafaf8`, `--text: #1a1a1a`, `--accent: #8b7355` (warm brown), `--border: #e8e4de`
- All images live in `images/`

## Site structure

### Core pages
| File | Purpose |
|------|---------|
| `index.html` | Homepage — hero, featured projects grid, about strip, services, Art Basel strip, Mexico strip, contact CTA |
| `portfolio.html` | Full portfolio grid with filter (All / Residential / Interior / Concept) |
| `about.html` | Studio bio, Izabela's portrait |
| `services.html` | Architecture, Interior Design, Concept & Vision |
| `contact.html` | Contact form / details |
| `mexico.html` | Mexico hub page — property investment, all Mexican developments listed |
| `art-basel.html` | Art Basel Miami Beach 2024 digital art series |
| `art-prints.html` | Shop for limited edition fine art prints |

### Portfolio project pages (London / International)
| File | Project |
|------|---------|
| `krystal-koncepts.html` | Sacred Geometry Nest — Costa Rica (sustainable housing concept, 2025) |
| `soulful-interiors-london.html` | High-End Apartment — London (Soulful Interiors, 2025) |
| `modern-penthouse-london.html` | Modern Penthouse — London (Interior Design, 2025) |
| `penthouse-london.html` | St. George Penthouse — London (2020) |
| `apartment-london.html` | Apartment Renovation — London (2020) |
| `new-york-penthouse.html` | Penthouse — New York (2024) |
| `costa-rica.html` | Coastal Residence — Costa Rica (2023) |
| `nigeria.html` | Family Home — Lagos, Nigeria (2019) |
| `miami.html` | Private Villa — Miami (2021) |
| `dubai-villa.html` | Opulent Villa — Dubai (2023) |
| `casablanca.html` | Sustainable Master Plan — Morocco (Urban Design, 2013) |
| `aquapark-warsaw.html` | Sustainable Aquapark — Warsaw (Public Architecture, 2008) |

### Mexico property pages
| File | Project |
|------|---------|
| `okom.html` | OKOM — Tulum development |
| `jaal-ja.html` | Jaal Ja — Mahahual beachfront land & villas (Costa Maya) |
| `tierra-madre.html` | Tierra Madre — Tulum development |
| `aldea-valladolid.html` | Aldea Valladolid — Valladolid development |
| `ardeh-tulum.html` | Ardeh Tulum — penthouse & rooftop pool development |
| `lula-tulum.html` | Lula Sanctuary — Mexico |
| `ciudad-colorin.html` | Ciudad Colorín — development |
| `corazon-de-playa.html` | Corazón de Playa — Playa del Carmen boutique residences for digital nomads |

## Design conventions
- Nav: fixed, 72px tall, `Izabela Ostatek` logo left, links right, hamburger on mobile
- Mobile breakpoint: 768px. Every page has inline `<style>` blocks in `<head>` for per-page mobile overrides
- Hamburger menu: animates to X on open, full-screen overlay (`nav-overlay`)
- Page headers use `.page-header` with `.section-label` (small caps eyebrow) + `<h1>` with `<em>` for italic accent word
- Buttons: `.btn` (dark fill) and `.btn-light` (light/outline for dark backgrounds)
- Fade-in animations: `.fade-in` class on sections, triggered by IntersectionObserver in `main.js`
- Images: never fixed-height crop on mobile — use `height: auto` and `aspect-ratio` instead of fixed `px` heights
- Hero sections on project pages: typically `80vh` or `100vh`, full-bleed image with text overlay

## Key image naming conventions
- `ardeh-*` → Ardeh Tulum images
- `av-*` / `av2-*` → Aldea Valladolid
- `tm-*` → Tierra Madre
- `okom-*` / `okom-pdf-*` → OKOM
- `jj-*` → Jaal Ja
- `krystal-*` → Sacred Geometry Nest / Krystal Koncepts
- `soulful-*` → Soulful Interiors London
- `art-*` → Art Basel series

## What has been built (git history summary)
- Full site built with all pages above
- Mexico hub + all 8 Mexican property project pages
- Art Basel 2024 gallery + print shop
- Mobile optimisation pass: hamburger animation, touch targets, responsive grids, iOS zoom fix, images uncropped on mobile
- Per-page hero and image fixes (Jaal Ja aerial, OKOM layout, Ardeh rooftop pool as hero, Lula aerial villa image)
- Homepage: portrait shown in full (no fixed crop height)

## GitHub & deployment
- Repo: `izabelaostatek/archi-website`
- Deployed via GitHub Pages (main branch)
- No build step — push to main and changes are live
- Development branch convention: `claude/<description>`

## Things to keep in mind
- No frameworks, no npm, no build — just edit HTML/CSS files directly and commit
- Mobile styles go as inline `<style>` in the `<head>` of each page (existing pattern), not in the shared stylesheet
- When adding a new project: (1) create the project HTML page, (2) add a card to `portfolio.html`, (3) add a card to the relevant hub page (mexico.html or homepage featured grid if prominent)
- Images should not be cropped with fixed heights on mobile — always use `aspect-ratio` or let height be auto
