# Black Arc Development — Portfolio Site

Static portfolio site for Black Arc Development. Plain HTML/CSS/JS, no build step — ready for GitHub Pages.

## Structure

```
index.html              Home page
web-development.html    Web Development project list
mods-scripting.html     Mods & Scripting project list
css/styles.css          All styling (design tokens at the top)
js/main.js              Mobile nav toggle
assets/                 Logo variants + favicons
assets/source/          Full-res original logo (not used on the site)
```

## Deploying to GitHub Pages

1. Push this folder to a GitHub repo (e.g. `blackarcdevelopment.github.io`, or any repo name).
2. In the repo: **Settings → Pages → Source** → select the `main` branch and `/ (root)` folder → Save.
3. GitHub will give you a live URL in a minute or two (e.g. `https://yourusername.github.io/repo-name/`).

## Editing content

- **Project cards** live directly in the HTML (`index.html`, `web-development.html`, `mods-scripting.html`). Each card is a self-contained `<div class="card">` block — copy/paste one to add a new project.
- Replace the `#` placeholder links in each card's `.card-links` with real URLs (live site, GitHub repo, etc.).
- Card status: use class `live` (green) or `progress` (blue) on `.card-status` to reflect project state.

## Adding a new discipline (e.g. Software, Security, Games)

1. Duplicate `web-development.html`, rename it (e.g. `software.html`).
2. Update the `<title>`, page header text, and eyebrow number.
3. Add its nav link to the `.nav-links` list in **all** pages (including this new one).
4. On `index.html`, move its tile in `#disciplines` from `.discipline locked` to `.discipline active` and link it.

## Design notes

- Palette, fonts, and spacing are all defined as CSS variables at the top of `css/styles.css` — change them there and they propagate everywhere.
- The signature interaction is the arc-trace glow on project card hover, a nod to the "Arc" in the brand name.
