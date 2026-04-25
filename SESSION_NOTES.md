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
- `logo_charcoal_rust.svg` — A palette, current best
- `logo_light_rust.svg` — B palette
- `logo_forest_amber.svg` — C palette
- `logo_slate_copper.svg` — D palette
- `logo_charcoal_rust_v1.svg` through `v5.svg` — dot exploration variants
- `portage_logo_panel.svg` — stripped-down working file (matches A palette currently)

### Open questions for next session

1. **Dev server setup** — Currently using a bare Python HTTP server (no hot reload, non-standard port). Need to set up `package.json` with `npm run dev`, live reload, and LAN access so user can work independently.

2. **Opacity → discrete colors** — All rail elements currently use `fill-opacity` on the same base hex as other elements. Before finalizing, need to bake opacity into resolved hex values per palette so every color in the logo is a discrete, pickable value (important for design tokens, brand guidelines, Illustrator usage).

3. **Color palette selection** — None locked in yet. User likes A (Charcoal + Rust) but wants to evaluate all four with fresh eyes.

4. **Water/land portage concept** — User was skeptical but the concept showed promise. Needs fresh-eyes evaluation. P3 (dashed trail path) was noted as most evocative.

5. **Divider pipe** — Keep or drop the vertical separator between mark and wordmark? Common in logo design but many modern logos use whitespace instead. Haven't tested without it yet.

6. **Font considerations** — Currently using Google Fonts import (DM Serif Display + IBM Plex Mono). Need to verify these render correctly when not connected to internet / in exported formats.
