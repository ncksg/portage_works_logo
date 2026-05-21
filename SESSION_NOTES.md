# Portage Works Logo — Session Notes

## Session 1 (2026-04-23/24)

### What was done

1. **Stripped the original SVG** down to just the logo (removed background card, color label, swatches)
2. **Created four color palette variants:**
   - A — Charcoal + Rust (original)
   - B — Light + Rust (light background version)
   - C — Deep Forest + Amber
   - D — River Stone + Copper
3. **Explored origin dot visibility** — the original was nearly invisible (r=3, 30% opacity). Tested 5 variations, landed on **V1 (open ring)** — hollow circle, r=4, stroke-width=1.5
4. **Tuned rail opacity** — original 0.08 was too faint. Tested 0.14 and 0.20, chose **0.14** as the sweet spot for dark palettes, **0.10** for light
5. **Explored rotated mark** (vertical rails + horizontal traversal) — user didn't love it, page kept for reference
6. **Explored water/land portage concept** — two streams (top + bottom) with land between, traversal line as the portage path. Four variations (P1–P4) plus a dashed trail version. Not yet evaluated with fresh eyes.
7. **Dev server** — set up BrowserSync with live reload on port 3456
8. **Baked opacity into discrete hex values** — all rail/subtle elements now use resolved hex colors per palette, no fill-opacity

### Pages / files

| URL | File | What's on it |
|-----|------|-------------|
| localhost:3456 | `index.html` | Main workshop — four palette variants (A–D) with current best mark (V1 dot, 0.14 rails) |
| localhost:3456/test_dots.html | `test_dots.html` | Zoomed-in origin dot comparison (6 variants at large scale) |
| localhost:3456/test_rails.html | `test_rails.html` | Rail opacity comparison — current vs +1 shade vs +2 shades |
| localhost:3456/test_rails_all.html | `test_rails_all.html` | V1 dot + 0.14 rails across all four palettes |
| localhost:3456/test_rotated.html | `test_rotated.html` | Rotated mark (vertical rails) — mark only + full lockup, compared to original |
| localhost:3456/test_water.html | `test_water.html` | Water/land portage concept — 4 mark variants (P1–P4) + full lockups |

**Logo SVG files:**
- `logo_dark_charcoal.svg` — A palette, current best
- `logo_light_cream.svg` — B palette
- `logo_dark_forest.svg` — C palette
- `logo_dark_slate.svg` — D palette
- `logo_charcoal_rust_v1.svg` through `v5.svg` — dot exploration variants
- `portage_logo_panel.svg` — stripped-down working file (matches A palette currently)

### Open questions carried forward

1. **Water/land portage concept** — User was skeptical but the concept showed promise. Needs fresh-eyes evaluation. P3 (dashed trail path) was noted as most evocative.
2. **Divider pipe** — Keep or drop the vertical separator between mark and wordmark? Common in logo design but many modern logos use whitespace instead. Haven't tested without it yet.
3. **Font considerations** — Currently using Google Fonts import (DM Serif Display + IBM Plex Mono). Need to verify these render correctly when not connected to internet / in exported formats.

---

## Session 2 (2026-05-21)

### What was done

1. **Created brand reference** — `brand.html` (visual reference with dark/light toggle) and `BRAND.md` (machine-readable spec for agent consumption). Covers color tokens, typography, logo usage rules, clear space, minimum sizes, and palette-to-context mapping.

2. **Established typography system** — Three fonts:
   - DM Serif Display — brand name, hero text, major headings
   - IBM Plex Sans (new) — body copy, subheadings, UI text
   - IBM Plex Mono — labels, metadata, technical callouts, "WORKS" wordmark

3. **Tuned dark palette** — Several values adjusted from Session 1 for better contrast and readability:
   - Background: `#2E2E2A` → `#363630` (lighter, more contrast with surface)
   - Secondary text: `#706A60` → `#908A7E` (more readable on dark backgrounds)
   - Divider: `#464640` → `#7A7060` (warmer, more visible)
   - Updated logo SVGs to match (divider stroke, WORKS text color)

4. **Defined text color hierarchy** — Primary text (`#E8E2D4` dark / `#3E2C1E` light) for headings and emphasis; secondary text for body copy, captions, and labels. Better visual separation between heading and body content.

5. **Centered logo viewBox** — All logo SVGs reframed from `0 0 260 56` to `-16 -8.75 250 70`. Content was left-heavy with ~42px of dead space on the right and the "Portage" text actually extending above the viewBox. New framing centers visual content with symmetric padding. Dimensions divisible by 10.

6. **Created mark-only SVGs** — `mark_dark_charcoal.svg` and `mark_light_cream.svg` with square 60×60 viewBox. For favicons, app icons, social media avatars, and other contexts where the full lockup won't fit.

7. **Locked active palettes** — Dark Charcoal (A) and Light Cream (B) are the two active palettes. Forest (C) and Slate (D) retained as reserve variants with updated viewBoxes.

8. **Palette-to-context mapping established:**
   - Presentations, website, business cards → Dark Charcoal
   - Proposals, documents, email signatures → Light Cream

### Pages / files added

| URL | File | What's on it |
|-----|------|-------------|
| localhost:3456/brand.html | `brand.html` | Visual brand reference — dark/light toggle, swatches, typography, logo usage |

**New files:**
- `brand.html` — visual brand reference
- `BRAND.md` — machine-readable brand spec
- `mark_dark_charcoal.svg` — dark mark only (60×60)
- `mark_light_cream.svg` — light mark only (60×60)

### Open questions carried forward

1. **Water/land portage concept** — still unevaluated with fresh eyes
2. **Divider pipe** — still untested without it
3. **Font offline rendering** — Google Fonts imports in SVGs won't work offline; may need embedded fonts for exported/print contexts
