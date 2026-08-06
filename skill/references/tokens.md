# Design Tokens — raw values

Every value on this page comes from the **S1 Brand Guideline** Figma file
([S1 Brand Guideline](https://www.figma.com/design/gSG4w3gVwXe5S3YWJsjzZX/S1-Brand-Guideline))
and its variables export (`s1-ds.json`). These are the primitive/raw tokens the
rest of the system is built from. For *which* color to use in a given context
(semantic tokens like `text-primary`, `bg-brand-solid`), see
[`color-variables.md`](color-variables.md); for named type styles, see
[`typography.md`](typography.md).

- Colors are hex; a trailing 2 hex digits = alpha (e.g. `#00000014` = black 8%).
- Spacing, radius, and sizes are in **px** unless noted.
- Two typefaces: **Space Grotesk** for Display/headings (`font-family-display`),
  **Inter** for Text/body (`font-family-body`).

---

## 1. Color primitives

Semantic color variables resolve to these primitive scales. This is the
**Untitled-UI-based** S1 palette (updated from the S1 Brand Guideline file); the
**brand** scale is S1-custom navy.

### Neutral (Gray) — separate light & dark ramps

Light mode uses the *Gray (light mode)* ramp; dark mode uses *Gray (dark mode)*.

| Step | Light ramp | Dark ramp |
|---|---|---|
| 25 | `#fdfdfd` | `#fafafa` |
| 50 | `#fafafa` | `#f7f7f7` |
| 100 | `#f5f5f5` | `#f0f0f1` |
| 200 | `#e9eaeb` | `#ececed` |
| 300 | `#d5d7da` | `#cecfd2` |
| 400 | `#a4a7ae` | `#94979c` |
| 500 | `#717680` | `#85888e` |
| 600 | `#535862` | `#61656c` |
| 700 | `#414651` | `#373a41` |
| 800 | `#252b37` | `#22262f` |
| 900 | `#181d27` | `#13161b` |
| 950 | `#0a0d12` | `#0c0e12` |

**Base:** white `#ffffff` · black `#000000` · transparent

### Brand (S1 navy)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| 25 | `#e9edf5` | 500 | `#1f4796` |
| 50 | `#d2daea` | 600 | `#193978` |
| 100 | `#bcc8e0` | 700 | `#132b5a` |
| 200 | `#a5b5d5` | 800 | `#0c1c3c` |
| 300 | `#7991c0` | 900 | `#42307d` |
| 400 | `#4c6cab` | 950 | `#2c1c5f` |

> Note: the brand ramp is navy through `brand-800`, then deepens to **purple**
> at `brand-900` (`#42307d`) and `brand-950` (`#2c1c5f`) — this is intentional
> (confirmed by the brand owner), not a template default.

### Red (error)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| 25 | `#fffbfa` | 500 | `#f04438` |
| 50 | `#fef3f2` | 600 | `#d92d20` |
| 100 | `#fee4e2` | 700 | `#b42318` |
| 200 | `#fecdca` | 800 | `#912018` |
| 300 | `#fda29b` | 900 | `#7a271a` |
| 400 | `#f97066` | 950 | `#55160c` |

### Amber (warning)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| 25 | `#fffcf5` | 500 | `#f79009` |
| 50 | `#fffaeb` | 600 | `#dc6803` |
| 100 | `#fef0c7` | 700 | `#b54708` |
| 200 | `#fedf89` | 800 | `#93370d` |
| 300 | `#fec84b` | 900 | `#7a2e0e` |
| 400 | `#fdb022` | 950 | `#4e1d09` |

### Green (success)

| Step | Hex | | Step | Hex |
|---|---|---|---|---|
| 25 | `#f6fef9` | 500 | `#17b26a` |
| 50 | `#ecfdf3` | 600 | `#079455` |
| 100 | `#dcfae6` | 700 | `#067647` |
| 200 | `#abefc6` | 800 | `#085d3a` |
| 300 | `#75e0a7` | 900 | `#074d31` |
| 400 | `#47cd89` | 950 | `#053321` |

---

## 2. Extended "utility" palette (badges, tags, charts)

The wider palette used by badges, tags, and charts (`Component colors/Utility/*`).
Badge/tag `Color` options draw from these hues.

| Hue | 50 | 200 | 400 | 500 | 600 | 700 |
|---|---|---|---|---|---|---|
| brand | `#d2daea` | `#a5b5d5` | `#4c6cab` | `#1f4796` | `#193978` | `#132b5a` |
| gray | `#fafafa` | `#e9eaeb` | `#a4a7ae` | `#717680` | `#535862` | `#414651` |
| gray-blue | `#f8f9fc` | `#d5d9eb` | `#717bbc` | `#4e5ba6` | `#3e4784` | `#363f72` |
| error | `#fef3f2` | `#fecdca` | `#f97066` | `#f04438` | `#d92d20` | `#b42318` |
| warning | `#fffaeb` | `#fedf89` | `#fdb022` | `#f79009` | `#dc6803` | `#b54708` |
| success | `#ecfdf3` | `#abefc6` | `#47cd89` | `#17b26a` | `#079455` | `#067647` |
| green | `#edfcf2` | `#aaf0c4` | `#3ccb7f` | `#16b364` | `#099250` | `#087443` |
| yellow | `#fefbe8` | `#feee95` | `#fac515` | `#eaaa08` | `#ca8504` | `#a15c07` |
| blue | `#eff8ff` | `#b2ddff` | `#53b1fd` | `#2e90fa` | `#1570ef` | `#175cd3` |
| blue-light | `#f0f9ff` | `#b9e6fe` | `#36bffa` | `#0ba5ec` | `#0086c9` | `#026aa2` |
| blue-dark | `#eff4ff` | `#b2ccff` | `#528bff` | `#2970ff` | `#155eef` | `#004eeb` |
| indigo | `#eef4ff` | `#c7d7fe` | `#8098f9` | `#6172f3` | `#444ce7` | `#3538cd` |
| purple | `#f4f3ff` | `#d9d6fe` | `#9b8afb` | `#7a5af8` | `#6938ef` | `#5925dc` |
| fuchsia | `#fdf4ff` | `#f6d0fe` | `#e478fa` | `#d444f1` | `#ba24d5` | `#9f1ab1` |
| pink | `#fdf2fa` | `#fcceee` | `#f670c7` | `#ee46bc` | `#dd2590` | `#c11574` |
| orange | `#fef6ee` | `#f9dbaf` | `#f38744` | `#ef6820` | `#e04f16` | `#b93815` |
| orange-dark | `#fff4ed` | `#ffd6ae` | `#ff692e` | `#ff4405` | `#e62e05` | `#bc1b06` |

> Full ramps for each hue exist in the file (steps 25–900); the columns above
> are the most-used steps (50 fill, 200 border, 500 dot/solid, 700 text).

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

### Display (headings, hero) — family: Space Grotesk (`font-family-display`)

| Style | Size | Line height | Letter-spacing |
|---|---|---|---|
| display-2xl | 72 | 90 | -2% |
| display-xl | 60 | 72 | -2% |
| display-lg | 48 | 60 | -2% |
| display-md | 36 | 44 | -2% |
| display-sm | 30 | 38 | 0 |
| display-xs | 24 | 32 | 0 |

### Text (body, UI) — family: Inter (`font-family-body`)

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

### Responsive grid

Three breakpoints, each a fixed-margin column grid (derived from the Figma grid
frame geometry). Column width auto-fills the content area.

| Breakpoint | Device | Container | Columns | Gutter | Side margin | Content width | Column width |
|---|---|---|---|---|---|---|---|
| Desktop | MacBook Pro (1440 viewport) | 1280 | 12 | 32 | 32 | 1216 | 72 |
| Tablet | iPad Mini | 768 | 6 | 32 | 32 | 704 | ~90.7 |
| Mobile | iPhone 11 Pro / X (375) | 375 | 4 | 16 | 16 | 343 | ~73.75 |

**Container grid presets** (auto-fit column layouts used inside the 1280
container): **12**, **6**, **5**, **3**, and **2** columns.

> Rule of thumb: desktop and tablet use a **32px** gutter and margin; mobile
> drops to **16px** (matching `container-padding-mobile`). Gutters use
> `spacing-4xl` (32) / `spacing-xl` (16).

---

## Status

- **Complete, from the Brand Guideline variables export:** full primitive
  scales (Gray light + dark ramps, Brand, Error, Warning, Success — all steps
  `25`–`950`); the full extended utility palette (17 hues); spacing, radius,
  and type scales; container + width tokens; and the responsive grid. Every
  semantic token's light **and** dark value is resolved from these primitives
  (see `color-variables.md`).
- **Note:** `brand-900`/`brand-950` are intentionally purple (confirmed) — the
  navy ramp deepens to purple at the darkest two steps.
- **Out of scope:** effect/shadow styles.
