# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static single-page website for **Zenon Portal v1.5** — a visual explainer of a trust-reduced Bitcoin-Zenon interoperability protocol. Live at [ebtc.wtf](https://ebtc.wtf). Hosted via GitHub Pages (CNAME: `ebtc.wtf`).

## Architecture

This is a no-build, no-framework static site. There is no build step, bundler, or package manager.

- **`index.html`** — The entire site: 16 full-viewport image slides with scroll-snap, nav dots, keyboard navigation (Arrow/Page/Space keys), IntersectionObserver-based slide tracking, and a page counter. All JS is inline at the bottom of the file.
- **`assets/css/style.css`** — All styles. Dark background (#111110), scroll-snap slides, fixed nav dots on the right edge, fixed footer bar, video slide hover effects, mobile breakpoint at 640px.
- **`assets/images/`** — WebP slide images (1920×1071 aspect ratio) plus PNG files for OG/social preview. Hero image is preloaded; all others use `loading="lazy"`.
- **`assets/icons/favicon.svg`** — SVG favicon.

## SEO/Infrastructure Files

- `_headers` — Cloudflare/GitHub Pages cache headers (immutable caching for assets)
- `robots.txt` — Permits all crawlers including AI bots (GPTBot, ClaudeBot, etc.)
- `sitemap.xml` — Single-URL sitemap for `https://ebtc.wtf/`
- `pagespeedapi.txt` — PageSpeed API verification file (listed in `.gitignore`)

## Development

Open `index.html` in a browser or use any local server:

```
python3 -m http.server 8000
```

There are no tests, linters, or build commands.

## Key Conventions

- Images use WebP format with explicit `width="1920" height="1071"` and descriptive `alt` text containing full technical content for SEO.
- The `<div class="sr-only">` block in `index.html` contains hidden semantic HTML duplicating all slide content for search engines and screen readers.
- The last slide is a video link (YouTube) with a play overlay, not a static image slide.
- The `reference/` directory contains the source PDF specification (`Zenon_Portal_Blueprint.pdf`).
