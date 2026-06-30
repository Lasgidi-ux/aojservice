# AOJ Service — Website

Single-page marketing site for **AOJ Service** (Jerry Ajayi Enterprise), Ogun State, Nigeria — one brand with two arms of expertise:

- **Fluent Door** — online French & Yoruba language tutoring (beginner to advanced, DELF/DALF/TEF prep)
- **Bookpreneur** — turning knowledge into published digital books
- **AOJWater** — certified plumbing, renovation & facility maintenance

## Overview

The site is a single, self-contained `index.html` (HTML, CSS and JS inline, images embedded as base64) so it can be hosted anywhere static — just open the file or drop it on any static host (GitHub Pages, Netlify, etc.). No build step required.

### Tech & libraries (loaded via CDN)

- [GSAP](https://gsap.com/) + ScrollTrigger, SplitText and Flip — reveals, count-ups, parallax, lightbox transitions and the gallery filter morph
- [Lenis](https://lenis.darkroom.engineering/) — smooth scrolling (desktop, fine-pointer only)
- Google Fonts — Space Grotesk (display), Fraunces (serif), Inter (body)

All motion is progressively enhanced: if scripts fail or the user prefers reduced motion, a `force-show` fallback reveals all content immediately.

## Design system

| Token | Value | Use |
| --- | --- | --- |
| `--bone` | `#F3F1EB` | page background |
| `--ink` | `#1A1B1D` | primary text |
| `--petrol` | `#15384B` | brand / primary action |
| `--accent` | `#C8923D` | warm brass highlight |

Typography pairs a geometric display sans (Space Grotesk) with an editorial serif (Fraunces) used for accents, pull-quotes and oversized numerals.

## Premium enhancement pass

This branch adds an awwwards-inspired polish layer on top of the original build, all additive and respecting `prefers-reduced-motion`:

- **Hero** — animated aurora glow, a serif-italic gradient accent word, a location badge over the imagery, and a "Scroll" cue
- **Editorial section numbering** — `(01) (02) …` auto-numbered eyebrows via CSS counters
- **Micro-interactions** — sweep-fill buttons, hover-lift cards, animated underline on the "Why" list, ledger row hover, marquee edge-fades + pause-on-hover
- **Floating WhatsApp button** — appears after the hero with a subtle ping
- **Accessibility** — `:focus-visible` outlines and custom selection colour
- **Audit fix** — the mobile navigation was only hidden at `≤680px` and leaked onto desktop; it is now hidden by default and shown only via the hamburger menu

## Local preview

```bash
# just open it
open index.html        # macOS
xdg-open index.html    # Linux

# or serve it
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Contact

- WhatsApp: 0805 148 1013 · 0807 205 3039
- Email: aojwater@gmail.com
- 12 Peace Avenue, Okepa Abule, Mowe–Pakuro Road, Ogun State, Nigeria
