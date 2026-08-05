# Tokens

S1's design tokens are the atomic values — color, spacing, radius, and type
scale — that every component is built from. Never hardcode a hex value, a
raw pixel spacing, or a corner radius in product work. Reach for the token
name instead: it keeps light/dark mode correct automatically and keeps every
surface visually consistent with the brand.

Source of truth: [S1 2.0 Figma — Design tokens](https://www.figma.com/design/wmlelbFhJ0FPS6DwpNXS2Z/S1-2.0?node-id=6472-97622) (colors), spacing, radius, and grid frames in the same file.

## Colors

S1's color system is organized into three semantic layers, each with a
light-mode and dark-mode value. Pick the layer by *what* you're coloring —
text, a border, or a shape/icon — not by which hex looks closest.

### Text colors

| Token | Light mode | Usage |
|---|---|---|
| `text-primary` (900) | `#171717` | Primary text such as page headings |
| `text-primary_on-brand` | white | Primary text on solid brand-color backgrounds (e.g. CTA sections) |
| `text-secondary` (700) | `#404040` | Secondary text — labels, section headings |
| `text-secondary_hover` | `#262626` | Secondary text, hover state |
| `text-secondary_on-brand` | brand-200 `#a5b5d5` | Secondary text on brand backgrounds |
| `text-tertiary` (600) | `#525252` | Tertiary text — supporting text, paragraph copy |
| `text-tertiary_hover` | `#404040` | Tertiary text, hover state |
| `text-tertiary_on-brand` | brand-200 `#a5b5d5` | Tertiary text on brand backgrounds |
| `text-quaternary` (500) | `#737373` | Subtle, lower-contrast text (e.g. footer column headings) |
| `text-quaternary_on-brand` | brand-300 `#7991c0` | Quaternary text on brand backgrounds (footers) |
| `text-white` | white | Always white regardless of mode |
| `text-placeholder` | `#737373` | Input field placeholder text |
| `text-brand-primary` (900) | `#11295b` | Primary brand text for headings (e.g. pricing page headers) |
| `text-brand-secondary` (700) | `#173779` | Brand buttons, accents, subheadings (e.g. blog post cards) |
| `text-brand-secondary_hover` | `#14306a` | Brand text, hover state |
| `text-brand-tertiary` (600) | `#1a3e88` | Lighter accented text/highlights (e.g. metric card numbers) |
| `text-brand-tertiary_alt` | `#1a3e88` | Alternative that stays lighter in dark mode (e.g. link buttons) |
| `text-error-primary` (600) | `#dc2626` | Error-state text |
| `text-warning-primary` (600) | `#ca8a04` | Warning-state text |
| `text-success-primary` (600) | `#16a34a` | Success-state text |

### Border colors

| Token | Light mode | Dark mode | Usage |
|---|---|---|---|
| `border-primary` | neutral-300 `#d4d4d4` | neutral-700 `#404040` | High-contrast borders — input fields, button groups, checkboxes |
| `border-secondary` | neutral-200 `#e5e5e5` | neutral-800 `#262626` | Medium-contrast, the default for most components — file uploaders, cards, tables, content dividers |
| `border-secondary_alt` | `rgba(0,0,0,0.1)` | neutral-800 `#262626` | Alpha-transparency alternative, used exclusively for floating menus (dropdowns, notifications) for a sharper bottom border |
| `border-tertiary` | neutral-100 `#f5f5f5` | neutral-800 `#262626` | Low-contrast, very subtle dividers (e.g. chart axis lines) |
| `border-brand` | brand-500 `#1d4597` | brand-400 `#4c6cab` | Default brand border — active states (e.g. focused input fields) |
| `border-brand_alt` | brand-600 `#1a3e88` | neutral-700 `#404040` | Brand border that turns gray in dark mode — banners, footers |
| `border-error` | red-500 `#ef4444` | red-400 `#f87171` | Error-state borders — input fields, file uploaders |
| `border-error_subtle` | red-300 `#fca5a5` | red-500 `#ef4444` | Lower-contrast alternative for error-state borders |

### Foreground colors (icons & non-text shapes)

Use these — never text or border tokens — for icons and other non-text
foreground elements.

| Token | Light mode | Dark mode | Usage |
|---|---|---|---|
| `fg-primary` (900) | `#171717` | white | Highest-contrast icons |
| `fg-secondary` (700) | `#404040` | neutral-300 `#d4d4d4` | High-contrast icons |
| `fg-secondary_hover` | `#262626` | neutral-200 `#e5e5e5` | Secondary icons, hover state |
| `fg-tertiary` (600) | `#525252` | neutral-400 `#a3a3a3` | Medium-contrast icons |
| `fg-tertiary_hover` | `#404040` | neutral-300 `#d4d4d4` | Tertiary icons, hover state |
| `fg-quaternary` (500) | neutral-400 `#a3a3a3` | neutral-500 `#737373` | Low-contrast icons — buttons, help icons, input-field icons |
| `fg-quaternary_hover` | `#737373` | neutral-400 `#a3a3a3` | Quaternary icons, hover state |
| `fg-white` | white | white | Always white regardless of mode |
| `fg-brand-primary` (600) | `#1a3e88` | brand-500 `#1d4597` | Primary brand icons — featured icons, progress bars |
| `fg-brand-primary_alt` | `#1a3e88` | neutral-300 `#d4d4d4` | Turns gray in dark mode — active horizontal tabs |
| `fg-brand-secondary` (500) | `#1d4597` | brand-500 `#1d4597` | Secondary brand icons — accents/arrows in marketing sections (e.g. hero headers) |
| `fg-brand-secondary_alt` | `#1d4597` | neutral-600 `#525252` | Turns gray in dark mode — brand buttons |
| `fg-error-primary` | `#dc2626` | red-500 `#ef4444` | Error-state featured icons |
| `fg-error-secondary` | `#ef4444` | red-400 `#f87171` | Error icons in input fields, negative metrics |
| `fg-warning-primary` | `#ca8a04` | yellow-500 `#eab308` | Warning-state featured icons |
| `fg-warning-secondary` | yellow-600 `#eab308` | yellow-400 `#facc15` | Secondary warning icons |
| `fg-success-primary` | `#16a34a` | green-500 `#22c55e` | Success-state featured icons |
| `fg-success-secondary` | green-600 `#22c55e` | green-400 `#4ade80` | Button dots, avatar online indicators, positive metrics |

### Background colors

Referenced by other tables above; documented in the Figma file's Background
color section. Known base values:

| Token | Light mode | Dark mode |
|---|---|---|
| `bg-primary` | white | `#0a0a0a` |
| `bg-secondary` | `#fafafa` | — |

**Status:** full `bg-*` table (all steps + usage notes) still needs a pass —
next iteration.

### How to apply color tokens

- Never reach for a raw hex or a Tailwind/neutral scale name (`neutral-700`)
  directly in product code — always the semantic token (`text-secondary`,
  `border-primary`, `fg-tertiary`). The semantic name is what survives a
  light/dark mode switch or a future rebrand; the raw value doesn't.
  Reserve raw neutral/brand scale names for documentation and swatches only.
- Match the token category to what you're styling: text -> `text-*`,
  strokes/dividers -> `border-*`, icons and shapes -> `fg-*`, fills -> `bg-*`.
- `_hover` and `_alt` suffixes are real states, not one-offs — use them for
  interactive states instead of hand-rolling an opacity or darken filter.

## Spacing

S1 uses a single spacing scale for padding, margin, and gap — expressed in
pixels in Figma. Confirmed steps:

`2, 4, 6, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96, 128, 160, 192, 224, 256, 320, 384, 480, 560, 640, 720, 768, 1024, 1280, 1440, 1600, 1920`

The same frame documents responsive container/breakpoint widths at the
larger end of this scale (768, 1024, 1280, 1440, 1600, 1920) — treat those
top values as layout breakpoints, not component spacing.

**Usage rule:** always pick from this scale. If a spacing need falls between
two steps, that's a signal to reconsider the layout, not to introduce a
one-off value.

## Radius

Radius scale (rem / px), 16px base:

| rem | px |
|---|---|
| 0rem | 0 |
| 0.125rem | 2 |
| 0.25rem | 4 |
| 0.375rem | 6 |
| 0.5rem | 8 |
| 0.625rem | 10 |
| 0.75rem | 12 |
| 1rem | 16 |
| 1.25rem | 20 |
| 1.5rem | 24 |
| infinity | full / pill |

Confirmed token names in use: `radius-xs` (4px), `radius-sm` (6px),
`radius-md` (8px), `radius-xl` (12px). Full name-to-step mapping for the
remaining sizes is a follow-up.

## Grids

Container and column-grid specifications live in the S1 Figma file's Grids
frame. **Status:** not yet pulled into this doc — follow-up pass.

## Typography (raw scale)

Font family: **Inter** (`font-family-body`, `font-family-display`), with
weights Regular / Medium / Semibold confirmed in use. The full numeric type
scale (display and text sizes with their paired line-heights) lives in the
Figma Foundations -> Typography frame. **Status:** numeric scale values are a
follow-up pull — see `typography.md` for usage rules (which weight/size for
which context), documented separately from these raw values.

## Logo

Logo asset and usage guidance: [S1 logo frame](https://www.figma.com/design/wmlelbFhJ0FPS6DwpNXS2Z/S1-2.0?node-id=1083-118533).
**Status:** not yet documented in this skill — follow-up pass.
