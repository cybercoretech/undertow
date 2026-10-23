# Undertow project site

Served by GitHub Pages from `main` → `/docs` at
<https://cybercoretech.github.io/undertow/>.

- `index.html`: page content, plus `window.SITE` (default theme and signature mashups)
- `styles.css`, `app.js`: the shared Cybercore project-site kit (same files on every family site)

Themes load at runtime from the org site's registry (`/data/cybergrid.json`,
`/data/themes/<family>/<name>.json` on cybercoretech.github.io), so every
project site shares one source of truth. A signature mashup takes surfaces
(bg/panel/line/muted/white) from its `base` palette and neons from its
`accent` palette.

Local preview: serve a folder containing `undertow/` (this dir) and `data/`
(copied or symlinked from the org site repo), then open
`http://127.0.0.1:<port>/undertow/`.

The page consumes the versioned Cybercore Web Kit from
`https://cybercoretech.github.io/kit/v1/`. The shared theme runtime is no longer
copied into this repository; site-specific behavior remains in `index.html` and
`styles.css`. The runtime honors `window.SITE.web` motion/effect recipes and
`prefers-reduced-motion`.
