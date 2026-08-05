# Typography

Typography usage rules for S1. For the raw numeric scale (sizes,
line-heights), see `tokens.md` — this file covers *when* to use *which*
level, which is the part that keeps a page consistent.

## Font family

Inter, across both the body and display font-family roles
(`font-family-body`, `font-family-display`). Don't introduce a second
typeface for product UI.

## Weights

Three weights are in confirmed use:

- **Regular** — default body copy, paragraph text, table cells
- **Medium** — labels, badges, table headers, small supporting UI text
- **Semibold** — headings, section titles, emphasized values (e.g. metric
  numbers), primary CTAs

Don't reach for a fourth weight (e.g. Bold) unless it's confirmed present in
the type scale — Inter's weight jumps are large enough that an unlisted
weight will read as visually inconsistent with the rest of the system.

## Display vs. text styles

S1 separates **display** styles (marketing/landing headlines, hero copy —
larger, looser tracking) from **text** styles (product UI — body copy,
labels, table content, form fields). When building product/app screens,
default to text styles; reserve display styles for marketing surfaces
(saltbox.one, landing pages, campaign pages).

## Usage guidance

- Match heading level to document structure, not to desired visual size —
  don't skip levels or reuse a heading style purely because it "looks
  right" at a given size.
- Body/paragraph copy uses Regular weight at a text-level size — never a
  display size, even in a hero section's supporting line.
- Labels, table headers, and badges use Medium weight at the smallest
  legible text size in context (typically `text-xs` or `text-sm` — see
  `tokens.md` once the numeric scale is filled in).
- Metric/number emphasis (e.g. dashboard KPIs) uses Semibold with a
  brand-tertiary text color token (see `tokens.md` → Text colors) rather
  than plain neutral text, to draw the eye without needing a larger size.

**Status:** this file will get more specific size-by-context guidance once
the numeric type scale (`tokens.md`) is pulled from Figma in full.
