# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static HTML/CSS tribute page about the **People's Computer Company** — specifically its first newsletter from October 1972. No build tools, no JavaScript, no dependencies.

## Development

Open `index.html` directly in a browser — no server required. For live reloading during development, any static file server works:

```bash
python3 -m http.server 8000
# or
npx serve .
```

## Structure

- `index.html` — single page, content in French, layout centered with a fixed 800px container
- `style/reset.css` — CSS reset (zero out margins/padding/borders)
- `style/style.css` — site styles: dark background with a tiled archive.org image, black centered container, ghostwhite/darkgrey text palette
- `import/` — local image assets (cover and inside pages of the newsletter); also references `pcc` prefixed variants

## Key Details

- The body background image is loaded from an external `archive.org` URL — it requires internet access to display
- The page is in French; keep content edits in French
- Fixed-width layout (800px container, no responsive breakpoints currently)
- Font stack uses `courier` (set as `font:` shorthand on `p` — note this is a shorthand bug; it resets other font properties)
