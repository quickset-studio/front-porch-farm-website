# Front Porch Farm & Garden

The website for **Front Porch Farm & Garden** — a nine-acre regenerative farm in Goochland, Virginia growing organic vegetables, fruits, herbs, cut flowers, native plants, and pasture-raised heritage chickens.

> Grown from seed. Raised on pasture. Rooted in Goochland.

## Run locally

It's a single-file static site. Just serve the folder:

```bash
python3 -m http.server 5571
# then open http://localhost:5571/
```

Or open `index.html` directly in a browser.

## Stack

- A single `index.html` with inline CSS and a small inline JavaScript snippet for the mobile nav drawer.
- Google Fonts (Playfair Display + Lato).
- All farm photography lives in `assets/images/`.

No build step, no package manager, no framework.

## Design notes

- **Palette** — Cream `#F0EDE6` · Near-black `#1A1A1A` · Forest Green `#4A5D4E` · Warm white `#FAFAF8`.
- **Typography** — Playfair Display for headlines (sentence case), Lato 300/400 for body.
- **Logo** — black linework on cream; rendered with `mix-blend-mode: multiply` so it blends seamlessly with both the cream nav and the cream footer without a hard edge.
- **Aesthetic target** — *Patagonia meets farmers-market field journal*: thin 1px borders, generous whitespace, restrained use of forest-green accent on the CTA, drop cap, and small detail rules.

## Sections

1. Sticky nav (cream, logo left, links right, hamburger drawer on mobile)
2. Full-viewport hero — farmhouse at twilight with the porch lit
3. Our Philosophy — drop cap, two-column with field photo
4. What We Grow & Raise — 4-up bordered card grid (vegetables, flowers, chickens, coming soon)
5. From the Farm — dark photo grid (six images)
6. Find Us — minimal contact card
7. Footer — centered logo, italic tagline

## Mobile audit

Tested with Playwright at four viewports (iPhone 375, iPhone 390, Android 360, iPad 768) at 2× device scale.

- 0 horizontal overflow at every viewport
- 0 tap-target violations (CTA ≥ 48px, hamburger 44×44, nav links ≥ 44 high)
- Hamburger drawer opens/closes, ESC closes, body-scroll locked while open
- All section anchors land below the sticky nav (`scroll-margin-top: 96px`)

## Content placeholder

The contact email is currently shown as a placeholder in the **Find Us** section. Replace `[ Contact email — to be added before launch ]` in `index.html` with the real address before going live.
