# Portage Works — Brand Specification

Version 1.0 · For internal use and agentic tool context.

## Brand Accent

| Token    | Hex       | Usage                                      |
|----------|-----------|--------------------------------------------|
| `accent` | `#C07838` | Anchor color. Links, CTAs, highlights, the accent dot in the logo mark. Consistent across all palettes. |

## Dark Palette — Charcoal

Primary palette for presentations, website, and digital contexts.

| Token            | Hex       | Role                        |
|------------------|-----------|-----------------------------|
| `dark-bg`        | `#363630` | Page / slide background     |
| `dark-surface`   | `#242420` | Cards, inset panels         |
| `dark-text`      | `#E8E2D4` | Headings, emphasis, important content |
| `dark-secondary` | `#908A7E` | Body copy, captions, metadata, labels |
| `dark-subtle`    | `#484742` | Borders, card backgrounds   |
| `dark-divider`   | `#7A7060` | Separators, horizontal rules|
| `accent`         | `#C07838` | Highlights, links, CTAs     |

## Light Palette — Cream

For print, proposals, documents, and light-mode web contexts.

| Token             | Hex       | Role                        |
|-------------------|-----------|-----------------------------|
| `light-bg`        | `#F5EDD8` | Page background             |
| `light-surface`   | `#EDE5CF` | Cards, inset panels         |
| `light-text`      | `#3E2C1E` | Headings, emphasis, important content |
| `light-secondary` | `#8B7560` | Body copy, captions, metadata, labels |
| `light-subtle`    | `#E0D7C3` | Borders, card backgrounds   |
| `light-divider`   | `#C4A882` | Separators, horizontal rules|
| `accent`          | `#C07838` | Highlights, links, CTAs     |

## Typography

Three-font system. All available on Google Fonts.

### DM Serif Display

- **Role:** Brand name, hero text, major headings, slide titles
- **Weight:** 400 (regular only)
- **Sizes:** 40px hero, 28px section heading, 20px slide heading
- **Do not use for:** Body copy, small text, UI elements

### IBM Plex Sans

- **Role:** Body copy, subheadings, slide content, UI text, proposals
- **Weights:** 300 (light, decorative only), 400 (body), 500–600 (emphasis), 700 (strong headings)
- **Sizes:** 18px subheading, 16px body, 14px small/caption
- **Primary workhorse font for all readable content**

### IBM Plex Mono

- **Role:** Labels, metadata, technical callouts, code, "WORKS" wordmark, pricing, data
- **Weights:** 400 (regular), 500–600 (emphasis)
- **Style:** Often uppercase with letter-spacing 0.1–0.2em for labels
- **Do not use for:** Long-form body copy

## Logo Usage

### Structure

The logo lockup consists of: mark (rails + traversal line + origin ring + accent dot) | vertical divider | wordmark ("Portage" in DM Serif Display + "WORKS" in IBM Plex Mono).

### Logo Files

| File                      | Type      | Palette        | Background   |
|---------------------------|-----------|----------------|--------------|
| `logo_dark_charcoal.svg`  | Lockup    | Dark Charcoal  | `#363630`    |
| `logo_light_cream.svg`    | Lockup    | Light Cream    | `#F5EDD8`    |
| `mark_dark_charcoal.svg`  | Mark only | Dark Charcoal  | `#363630`    |
| `mark_light_cream.svg`    | Mark only | Light Cream    | `#F5EDD8`    |

### Mark Only

The mark (rails, traversal line, origin ring, accent dot) may be used standalone — without the divider and wordmark — for favicons, app icons, social media avatars, and other contexts where the full lockup won't fit or isn't needed. The mark SVG has a square 60×60 viewBox.

### Clear Space

Minimum clear space on all sides = 1× the cap-height of "Portage" in the wordmark. This scales proportionally with the logo at any size. No other elements may intrude into this zone.

### Minimum Size

- **Full lockup — Screen:** 160px wide minimum
- **Full lockup — Print:** 40mm wide minimum
- **Mark only — Screen:** 24px minimum
- **Mark only — Print:** 6mm minimum

Below these thresholds, details lose legibility.

### Don'ts

- Do not stretch or distort the logo proportions
- Do not recolor the logo outside of approved palette colors
- Do not reduce contrast to the point of illegibility
- Do not place the logo on busy backgrounds without sufficient contrast
- Do not remove the divider or rearrange lockup components

## Palette × Context Mapping

| Context               | Palette          | Rationale                                          |
|-----------------------|------------------|----------------------------------------------------|
| Presentation slides   | Dark — Charcoal  | Projects well; reduces eye strain in dimmed rooms   |
| Website               | Dark — Charcoal  | Primary site palette; light for specific sections   |
| Proposals & documents | Light — Cream    | Better print readability; conserves ink              |
| Business cards        | Dark — Charcoal  | Dark stock + light text + rust accent is distinctive|
| Email signatures      | Light — Cream    | Most email clients render on light backgrounds      |
