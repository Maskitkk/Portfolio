# AGENTS.md

## What this is

Single-page static portfolio site (`index.html`) — no build tools, no package manager, no framework.

## Structure

```
index.html                  — standalone portfolio page (585 lines)
me_3d_1_optimized_1.mp4     — hero background video 1
me_3d_2_optimized.mp4       — hero background video 2
recommendation_letter.png   — inline image in experience section
```

## Key facts

- **No build steps.** Just serve `index.html` as a static file (or open directly).
- **CDN deps** (loaded via `<script defer>` in `<head>`): Three.js r128, GSAP 3.12.2 + ScrollTrigger.
- **Vimeo iframes** lazily loaded via `IntersectionObserver` — card clicks are not required, just scroll into view.
- **Bilingual** (EN/RU). Language auto-detected from `navigator.language`. Toggle via `.lang-switch` button.
- **Scrolling branches exist**: `port_2` (current), `new_port`, `main` — the active dev branch is `port_2`.

## Commands

- **Preview locally**: open `index.html` in a browser or `npx serve .`
- **Deployment**: static hosting (no build step needed).
