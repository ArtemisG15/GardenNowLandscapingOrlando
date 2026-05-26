# Garden Now Landscaping Orlando — Business Website

A fully responsive, production-ready marketing site built for a landscaping company in Orlando, FL. Designed as a freelance/spec project to demonstrate real-world front-end development skills without using any frameworks or build tools.

**[Live Demo](https://gardennowlandscapingorlando.netlify.app)**

---

## About the Project

Garden Now Landscaping Orlando needed a professional web presence that could speak to a multilingual client base — English, Spanish, and Portuguese — with a clean design, gallery of real project photos, and a contact form that works on any device. The goal was a fast, polished site that converts visitors into calls and quote requests.

Built entirely with vanilla HTML, CSS, and JavaScript. No React, no Tailwind, no Webpack — just clean, hand-written code.

---

## Features

- **Trilingual (EN / ES / PT)** — full English, Spanish, and Portuguese translation toggle; preference persisted in `localStorage` and auto-detected from `navigator.language` on first visit
- **Mobile-first responsive** — tested across three breakpoints; hamburger nav with scroll-lock overlay on mobile
- **Active nav link tracking** — Intersection Observer highlights the current section in the navbar as you scroll
- **Scroll animations** — Intersection Observer-driven reveal on every section; elements animate in once and stop firing
- **Before/After image sliders** — drag (mouse and touch) to reveal project transformations, built from scratch with `clipPath` and pointer events
- **Netlify Forms** — AJAX submission with a WhatsApp deep-link fallback; if fetch fails, the form opens a pre-filled WhatsApp message so no lead is ever lost
- **Floating WhatsApp CTA** — fixed button for mobile conversions
- **Google Maps embed** — business location embedded directly in the contact section
- **Custom SVG logo** — inline SVG leaf icon, no image file required
- **SEO-ready** — `<meta>` description and keywords tags targeting local landscaping searches
- **Accessible** — semantic HTML, `aria-label` on interactive elements, `aria-expanded`/`aria-hidden` on the mobile menu
- **Zero dependencies** — no npm, no build step; clone and open `index.html`

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 (semantic) |
| Styles | CSS3 — custom properties, Grid, Flexbox, keyframe animations |
| Scripts | Vanilla JavaScript (ES2020) |
| Icons | Font Awesome 6 |
| Fonts | Google Fonts — Montserrat + Open Sans |
| Hosting | Netlify (CD from GitHub) |
| Forms | Netlify Forms |

---

## Project Structure

```
GardenNowLandscapingOrlando/
├── index.html          # Single-page app — all sections
├── css/
│   └── style.css       # All styles — variables, layout, components, responsive
├── js/
│   └── main.js         # Navbar, scroll reveals, B/A sliders, form handling, i18n
└── images/
    ├── project-feature.jpg
    ├── team.jpg
    ├── gallery-design.jpg
    ├── gallery-sod.jpg
    ├── gallery-mowing.jpg
    ├── gallery-comercial.jpg
    ├── gallery-backyard-before.jpg
    ├── gallery-backyard-after.jpg
    ├── gallery-pavers-before.jpg
    └── gallery-pavers-after.jpg
```

---

## Sections

| Section | Description |
|---|---|
| **Hero** | Full-viewport intro with badge, hero copy, three CTA buttons (Call, WhatsApp, Services), and a stats bar showing Google rating, review count, women-owned badge, and location |
| **Services** | 6-card grid — Sod Installation, Landscape Design, Lawn Mowing, Shrub Trimming, Garden & Yard Cleanup, Pavers & Hardscaping |
| **Why Choose Us** | Dark section with feature photo, floating rating card, and a five-point value list |
| **Gallery** | Mixed grid with drag before/after sliders (backyard and paver transformations) and four single project photos |
| **Reviews** | Three real Google reviews with reviewer avatars, star ratings, and service tags |
| **About** | Two-column layout with team photo placeholder, women-owned badge card, and four core values |
| **Contact** | Netlify form + contact info panel (two phone contacts, email, hours, social links) + Google Maps embed |
| **Footer** | Brand, services links, full contact details, social icons, copyright |

---

## Local Development

No build step required.

```bash
git clone https://github.com/ArtemisG15/GardenNowLandscapingOrlando.git
cd GardenNowLandscapingOrlando
# Open index.html in your browser
```

> **Note:** The Netlify form will only submit successfully when deployed to Netlify. Locally it falls back to opening a pre-filled WhatsApp message.

---

## Design Decisions

- **No framework** — keeping the dependency surface at zero makes the codebase easy to audit and instant to load.
- **CSS custom properties** for theming — every color and shadow references a `:root` variable, making a brand swap a one-file change.
- **Intersection Observer** for reveals and active-nav tracking — no `scroll` event jank; each Observer disconnects from elements after they fire once.
- **Before/After sliders in pure JS** — no library; `clipPath: inset(...)` drives the reveal so the implementation is ~30 lines and GPU-accelerated.
- **WhatsApp fallback on the form** — the fallback doesn't just fail silently; it opens WhatsApp with the form data pre-filled so the business never misses a lead, even if JavaScript partially fails or the Netlify endpoint is unreachable.
- **Trilingual copy in JavaScript** — all three language objects live in `main.js` as a plain keyed object; `navigator.language` auto-selects the right one on first visit, with `localStorage` persisting the user's manual choice.

---

## Business Details

- **Business:** Garden Now Landscaping Orlando
- **Phone (Português):** Joilson — (407) 914-1712
- **Phone (English):** Luciana — (407) 437-6932
- **Email:** Gardennowlandscape@gmail.com
- **Address:** 2313 Lake Debra Dr, Orlando, FL 32835
- **Hours:** Mon–Fri 8:00 AM – 6:00 PM · Sat 9:00 AM – 4:00 PM
- **Instagram:** [@gardennow_](https://www.instagram.com/gardennow_/)
- **Facebook:** [Garden Now](https://www.facebook.com/luejoilsongardennow)

---

*Designed and developed by [Artemis Grace](https://github.com/ArtemisG15)*
