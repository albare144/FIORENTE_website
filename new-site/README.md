# Fiorente — Redesigned Site (`new-site/`)

A complete redesign of myfiorente.com, built as a single-page static site.

The original WordPress mirror remains at the repo root for reference.

## Structure

```
new-site/
├── index.html      ← all page content, one file
├── styles.css      ← the full design system
└── images/         ← all photos used by the site
```

No build step, no framework. Open `new-site/index.html` in a browser to preview.

## Design system (for anyone editing)

- **Palette**: deep Mediterranean midnight (`--midnight #0b1a2d`), ivory (`--ivory #f5ede0`), antique brass (`--brass #b8935a`). All defined as CSS variables at the top of `styles.css`.
- **Typography**: Cormorant Garamond (display) + Manrope (body), both loaded from Google Fonts.
- **Tone**: editorial, Italian-luxury travel feature — Roman-numeral section markers, small-caps eyebrows, asymmetric magazine splits.

## Sections (in order)

1. **Hero** — full-viewport yacht image, title, key specs
2. **Quote band** — Sir Francis Drake quote
3. **The Yacht** — intro copy, exterior photo
4. **Specs** — 4-column dataplate
5. **Staterooms** ⟵ *new section*, 5 placeholder cards
6. **Entertainment & Leisure** ⟵ *expanded*, 6-feature grid
7. **Dining** ⟵ *expanded*, chef copy
8. **Crew** — 6 roles, roster-style layout
9. **Destinations** — 15 locations, editorial list
10. **Gallery** ⟵ *new*, mosaic grid with 2 empty placeholders
11. **Contact** — no form; email + broker copy
12. **Footer**

## Swapping in new photos

Every placeholder in the HTML is marked with either:
- a `<!-- PLACEHOLDER: ... -->` comment, or
- a visible `Photo pending` tag / `Placeholder` badge in the UI

To replace a photo:

1. Drop the new file into `new-site/images/` (keep filenames sensible — e.g. `stateroom-master.jpg`)
2. Update the `src="images/..."` attribute in `index.html`
3. Remove the placeholder tag span or the `gallery__item--placeholder` cell

### Suggested filenames for when new photos arrive

| Section | Filename |
| --- | --- |
| Hero | `hero-yacht.jpg` |
| The Yacht | `yacht-exterior.jpg` |
| Master suite | `stateroom-master.jpg` |
| Double I | `stateroom-double-1.jpg` |
| Double II | `stateroom-double-2.jpg` |
| Twin I | `stateroom-twin-1.jpg` |
| Twin II | `stateroom-twin-2.jpg` |
| Entertainment | `entertainment-01.jpg`, `entertainment-02.jpg` |
| Dining | `dining-01.jpg`, `dining-02.jpg` |
| Gallery | `gallery-01.jpg` … `gallery-06.jpg` |

## What's intentionally missing

- **No forms** — enquiry is directed to a plain email line, per brief
- **No WordPress / CMS** — pure static, edit HTML directly
- **No external JavaScript** beyond a 5-line nav-scroll handler

## Deploying

Any static host works: GitHub Pages, Netlify, Vercel, Cloudflare Pages, or a plain S3 bucket. Upload the `new-site/` folder and serve `index.html`.
