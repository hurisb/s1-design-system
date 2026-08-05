# Design Tokens — raw values

Every value on this page is pulled directly from the **S1 2.0 Figma file**
([file](https://www.figma.com/design/wmlelbFhJ0FPS6DwpNXS2Z/S1-2.0)). These are
the primitive/raw tokens the rest of the system is built from. For *which*
color to use in a given context (semantic tokens like `text-primary`,
`bg-brand-solid`), see [`color-variables.md`](color-variables.md); for named
type styles, see [`typography.md`](typography.md).

- Colors are hex; a trailing 2 hex digits = alpha (e.g. `#0000001a` = black 10%).
- Spacing, radius, and sizes are in **px** unless noted.
- Font family throughout is **Inter**.

---

## 1. Color primitives

Semantic color variables resolve to these primitive scales. The scales match
the Tailwind palette for the neutral and accent hues; the **brand** scale is
S1-custom (navy).

### Neutral (gray)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| neutral-50 | `#fafafa` | | neutral-600 | `#525252` |
| neutral-100 | `#f5f5f5` | | neutral-700 | `#404040` |
| neutral-200 | `#e5e5e5` | | neutral-800 | `#262626` |
| neutral-300 | `#d4d4d4` | | neutral-900 | `#171717` |
| neutral-400 | `#a3a3a3` | | neutral-950 | `#0a0a0a` |
| neutral-500 | `#737373` | | | |

**Base:** black `#000000` · white `#ffffff`

### Brand (S1 navy)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| brand-50 | `#e9edf5` | | brand-600 | `#1a3e88` |
| brand-200 | `#a5b5d5` | | brand-700 | `#173779` |
| brand-400 | `#4c6cab` | | brand-800 | `#14306a` |
| brand-500 | `#1d4597` | | brand-900 | `#11295b` |

> Brand steps `100`, `300`, and `950` were not surfaced in this extraction pass.
> Two brand tints used by background tokens are `#d2daea` and `#bcc8e0` (the
> light values of `bg-brand-primary` and `bg-brand-secondary`).

### Red (error)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| red-50 | `#fef2f2` | | red-400 | `#f87171` |
| red-100 | `#fee2e2` | | red-500 | `#ef4444` |
| red-200 | `#fecaca` | | red-600 | `#dc2626` |
| red-300 | `#fca5a5` | | red-700 | `#b91c1c` |

### Yellow (warning)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| yellow-50 | `#fefce8` | | yellow-500 | `#eab308` |
| yellow-100 | `#fef9c3` | | yellow-600 | `#ca8a04` |
| yellow-200 | `#fef08a` | | yellow-700 | `#a16207` |
| yellow-400 | `#facc15` | | | |

### Green (success)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| green-50 | `#f0fdf4` | | green-500 | `#22c55e` |
| green-100 | `#dcfce7` | | green-600 | `#16a34a` |
| green-200 | `#bbf7d0` | | green-700 | `#15803d` |
| green-400 | `#4ade80` | | | |

---

## 2. Extended "utility" palette (badges, tags, charts)

Beyond the core hues above, badges/tags expose a wider palette. These are the
`Component colors/Utility/*` variables — the exact steps the system uses on
badge/tag surfaces (`50` = fill, `200` = border, `500` = dot, `700` = text).

| Color | 50 | 200 | 400 | 500 | 700 |
|---|---|---|---|---|---|
| Neutral | `#fafafa` | `#e5e5e5` | `#a3a3a3` | `#737373` | `#404040` |
| Brand | `#e9edf5` | `#a5b5d5` | `#4c6cab` | `#1d4597` | `#173779` |
| Red | `#fef2f2` | `#fecaca` | `#f87171` | `#ef4444` | `#b91c1c` |
| Yellow | `#fefce8` | `#fef08a` | `#facc15` | `#eab308` | `#a16207` |
| Green | `#f0fdf4` | `#bbf7d0` | `#4ade80` | `#22c55e` | `#15803d` |
| Slate | `#f8fafc` | `#e2e8f0` | `#94a3b8` | `#64748b` | `#334155` |
| Sky | `#f0f9ff` | `#bae6fd` | `#38bdf8` | `#0ea5e9` | `#0369a1` |
| Blue | `#eff6ff` | `#bfdbfe` | `#60a5fa` | `#3b82f6` | `#1d4ed8` |
| Indigo | `#eef2ff` | `#c7d2fe` | `#818cf8` | `#6366f1` | `#4338ca` |
| Purple | `#faf5ff` | `#e9d5ff` | `#c084fc` | `#a855f7` | `#7e22ce` |
| Pink | `#fdf2f8` | `#fbcfe8` | `#f472b6` | `#ec4899` | `#be185d` |
| Orange | `#fff7ed` | `#fed7aa` | `#fb923c` | `#f97316` | `#c2410c` |

> The core hues also expose step `600`: Brand `#1a3e88`, Red `#dc2626`,
> Yellow `#ca8a04`, Green `#16a34a`. Badge color options map to these names
> (see `data-display.md` → Badge → `Color`).

---

## 3. Spacing scale

Padding, gaps, and margins. Base unit is 4px, with a 2px `xxs`/`sm` sub-step.

| Token | px | | Token | px |
|---|---|---|---|---|
| spacing-none | 0 | | spacing-3xl | 24 |
| spacing-xxs | 2 | | spacing-4xl | 32 |
| spacing-xs | 4 | | spacing-5xl | 40 |
| spacing-sm | 6 | | spacing-6xl | 48 |
| spacing-md | 8 | | spacing-7xl | 64 |
| spacing-lg | 12 | | spacing-8xl | 80 |
| spacing-xl | 16 | | spacing-9xl | 96 |
| spacing-2xl | 20 | | spacing-10xl | 128 |
| | | | spacing-11xl | 160 |

---

## 4. Radius scale

Corner radii.

| Token | px | | Token | px |
|---|---|---|---|---|
| radius-none | 0 | | radius-xl | 12 |
| radius-xxs | 2 | | radius-2xl | 16 |
| radius-xs | 4 | | radius-3xl | 20 |
| radius-sm | 6 | | radius-4xl | 24 |
| radius-md | 8 | | radius-full | 9999 (pill/circle) |
| radius-lg | 10 | | | |

---

## 5. Type scale (numeric)

Raw font sizes and line heights. For weights, usage, and named styles
(`Display sm/Semibold`, `Text sm/Medium`, etc.), see
[`typography.md`](typography.md). Letter-spacing is **-2%** on Display 2xl–md
and **0** everywhere else.

### Display (headings, hero) — family: Inter

| Style | Size | Line height | Letter-spacing |
|---|---|---|---|
| display-2xl | 72 | 90 | -2% |
| display-xl | 60 | 72 | -2% |
| display-lg | 48 | 60 | -2% |
| display-md | 36 | 44 | -2% |
| display-sm | 30 | 38 | 0 |
| display-xs | 24 | 32 | 0 |

### Text (body, UI) — family: Inter

| Style | Size | Line height | Letter-spacing |
|---|---|---|---|
| text-xl | 20 | 30 | 0 |
| text-lg | 18 | 28 | 0 |
| text-md | 16 | 24 | 0 |
| text-sm | 14 | 20 | 0 |
| text-xs | 12 | 18 | 0 |

**Weights:** Regular 400 · Medium 500 · Semibold 600 · Bold 700 (each size × 4 = 44 styles).

---

## 6. Layout — widths, containers, grid

### Container

| Token | px |
|---|---|
| container-max-width-desktop | 1280 |
| container-padding-desktop | 32 |
| container-padding-mobile | 16 |
| paragraph-max-width | 720 |

### Width scale

| Token | px | | Token | px |
|---|---|---|---|---|
| width-xxs | 320 | | width-2xl | 1024 |
| width-xs | 384 | | width-3xl | 1280 |
| width-sm | 480 | | width-4xl | 1440 |
| width-md | 560 | | width-5xl | 1600 |
| width-lg | 640 | | width-6xl | 1920 |
| width-xl | 768 | | | |

> **Grid follow-up:** the responsive grid's column count and gutter aren't
> exposed as variables (they live in Figma layout-grid styles, node
> `5245:373010`). The container max-width (1280) and padding (32 desktop /
> 16 mobile) above are exact; column/gutter specs still need a manual capture.

---

## Status

- **Done (real values, from Figma):** neutral / brand / red / yellow / green
  primitive scales; full extended utility palette; spacing, radius, and type
  scales; container + width tokens.
- **Follow-ups:** brand steps 100/300/950; the `25` step across scales; grid
  column/gutter spec; effect/shadow styles (out of scope for now).
