# Logo

The S1 (Saltbox One) brand mark. Always use the official assets from the Figma
**Logos** page ([node `1083:118533`](https://www.figma.com/design/gSG4w3gVwXe5S3YWJsjzZX/S1-Brand-Guideline?node-id=1083-118533)) —
never redraw, retype, or recolor the logo by hand.

## The two lockups

| Lockup | What it is | Figma | Approx. size (at 24px cap height) |
|---|---|---|---|
| **Logomark** | The angular "S1" monogram mark on its own | `13042:508786` | ~32 × 24 |
| **Full logo** | Logomark + "Saltbox One" wordmark | `13042:508791` | ~139 × 24 |

Each lockup ships with **light** and **dark** mode variants (`Dark Mode=False` /
`Dark Mode=True`) — use the variant that matches the surface, don't restyle one
to fake the other.

- Use the **Full logo** by default — headers, footers, marketing, decks, docs.
- Use the **Logomark** alone only where space is tight or the brand is already
  established on the surface — app icons, favicons, avatars, compact nav.

## Colors (from Figma)

| Part | Token / value |
|---|---|
| Monogram mark | Brand gradient `brand-600 → brand-500` at 90° — `#193978 → #1f4796` |
| Wordmark ("Saltbox One") | `fg-primary` — `#181d27` light · `#ffffff` dark |

The mark keeps its brand gradient in both modes; only the wordmark swaps with
the mode. See [`color-variables.md`](color-variables.md) for the underlying
tokens.

## Usage

**Do**
- Pull the ready-made asset and its correct light/dark variant.
- Give it clear space on all sides — at least the **height of the monogram**
  (≈ the cap height) kept clear of other content.
- Keep it legible: don't render the mark below ~20px tall or the full logo below
  ~120px wide.
- Place the light-mode logo on light/neutral backgrounds and the dark-mode logo
  on dark or brand backgrounds, where contrast holds.

**Don't**
- Recolor the mark or wordmark, or replace the gradient with a flat fill.
- Stretch, skew, rotate, or otherwise distort the proportions.
- Add shadows, outlines, or effects.
- Recreate the wordmark by typing "Saltbox One" in Inter — always use the asset.
- Place the logo on a low-contrast or busy background that hurts legibility.

## Status

The two lockups, their light/dark variants, colors, and dimensions above are
taken directly from the Figma Logos page. Clear-space and minimum-size figures
are sensible defaults (not formally specified in the file) — confirm with the
brand owner if a stricter standard exists.
