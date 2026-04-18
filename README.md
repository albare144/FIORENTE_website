# FIORENTE_website

Static mirror of **myfiorente.com** — the website for the yacht Fiorente — imported for editing.

## Contents

- `index.html` — Home page
- `yacht.html` — The Yacht
- `crew.html` — The Crew
- `the-experience/` — The Experience page
- `enquire/` — Enquiry page
- `wp-content/` — All images, CSS, JS and theme assets
- `wp-includes/` — WordPress core assets referenced by the pages

## Notes

This is a **static HTML mirror** captured from the live site, not a WordPress source export. That means:

- You can edit HTML, CSS, images and text directly in this repo
- The enquiry form on the live site posts back to WordPress — if you want the form to work from a static copy you'll need to point it at a form handler (Formspree, Netlify Forms, etc.)
- The YouTube video embed and external fonts will keep working as-is

## How it was imported

Mirrored with:

```
wget --mirror --convert-links --adjust-extension --page-requisites --no-parent https://myfiorente.com/
```

Links were rewritten for local/relative use so the site can be previewed by opening `index.html` in a browser.
