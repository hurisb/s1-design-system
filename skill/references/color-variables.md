# Color Variables — semantic tokens with real values

This is the layer you actually apply. Bind every element to one of these
**semantic** variables — never a raw hex or a primitive step directly. Each
resolves automatically across light and dark modes.

- **Light** values were extracted directly from the S1 2.0 Figma file.
- **Dark** values are resolved from the documented dark-mode primitive of each
  variable against the primitive scales in [`tokens.md`](tokens.md). Three
  `-primary` alert backgrounds resolve to a `-950` step not surfaced in the
  current extraction and are marked accordingly.
- Rule of thumb: text → `text-*`, icons/indicators → `fg-*`, strokes → `border-*`,
  fills → `bg-*`. Never cross categories.

---

## 1. Text colors

Use for all text. Never fill text nodes with a raw color.

### Neutral hierarchy

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `text-primary` | `#171717` | `#fafafa` | Headings, titles, prominent labels |
| `text-primary_on-brand` | `#ffffff` | `#fafafa` | Primary text on solid brand backgrounds |
| `text-secondary` | `#404040` | `#d4d4d4` | Labels, section headings |
| `text-secondary_hover` | `#262626` | `#e5e5e5` | Secondary text, hover |
| `text-secondary_on-brand` | `#a5b5d5` | `#d4d4d4` | Secondary text on brand backgrounds |
| `text-tertiary` | `#525252` | `#a3a3a3` | Body/supporting text, descriptions |
| `text-tertiary_hover` | `#404040` | `#d4d4d4` | Tertiary text, hover |
| `text-tertiary_on-brand` | `#a5b5d5` | `#a3a3a3` | Tertiary text on brand backgrounds |
| `text-quaternary` | `#737373` | `#a3a3a3` | Subtle, low-contrast text (footer headings) |
| `text-quaternary_on-brand` | `#7991c0` | `#a3a3a3` | Quaternary text on brand backgrounds |

### Special & brand text

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `text-white` | `#ffffff` | `#ffffff` | Always-white text |
| `text-placeholder` | `#737373` | `#a3a3a3` | Input placeholders (neutral-500 for contrast) |
| `text-brand-primary` | `#11295b` | `#fafafa` | Primary brand headings (pricing headers) |
| `text-brand-secondary` | `#173779` | `#d4d4d4` | Brand buttons, accents, subheadings |
| `text-brand-secondary_hover` | `#14306a` | `#e5e5e5` | Brand secondary text, hover |
| `text-brand-tertiary` | `#1a3e88` | `#a3a3a3` | Lighter accents (metric numbers) |
| `text-brand-tertiary_alt` | `#1a3e88` | `#fafafa` | Link buttons (lighter in dark) |

### Semantic text

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `text-error-primary` | `#dc2626` | `#f87171` | Error messages |
| `text-warning-primary` | `#ca8a04` | `#facc15` | Warning text |
| `text-success-primary` | `#16a34a` | `#4ade80` | Success text |

---

## 2. Border colors

Use for all strokes and borders.

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `border-primary` | `#d4d4d4` | `#404040` | High-contrast: inputs, button groups, checkboxes |
| `border-secondary` | `#e5e5e5` | `#262626` | Default: cards, tables, dividers, file uploaders |
| `border-secondary_alt` | `#0000001a` | `#262626` | Alpha alt for floating menus (dropdowns, notifications) |
| `border-tertiary` | `#f5f5f5` | `#262626` | Low-contrast: subtle dividers, chart axes |
| `border-brand` | `#1d4597` | `#4c6cab` | Active/focused inputs, selected states |
| `border-brand_alt` | `#1a3e88` | `#404040` | Brand border → gray in dark (banners, footers) |
| `border-error` | `#ef4444` | `#f87171` | Error borders: inputs, file uploader |
| `border-error_subtle` | `#fca5a5` | `#ef4444` | Subtle error borders |

---

## 3. Foreground colors (icons, indicators)

Use for icons, progress bars, dots, decorative shapes. Never use `text-*` on an
icon or `fg-*` on text.

### Neutral hierarchy

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `fg-primary` | `#171717` | `#ffffff` | Highest-contrast icons |
| `fg-secondary` | `#404040` | `#d4d4d4` | High-contrast icons |
| `fg-secondary_hover` | `#262626` | `#e5e5e5` | Secondary icons, hover |
| `fg-tertiary` | `#525252` | `#a3a3a3` | Medium-contrast icons |
| `fg-tertiary_hover` | `#404040` | `#d4d4d4` | Tertiary icons, hover |
| `fg-quaternary` | `#a3a3a3` | `#737373` | Low-contrast: button/help/input icons |
| `fg-quaternary_hover` | `#737373` | `#a3a3a3` | Quaternary icons, hover |
| `fg-white` | `#ffffff` | `#ffffff` | Always-white icons |

### Brand & semantic

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `fg-brand-primary` | `#1a3e88` | `#1d4597` | Primary brand icons, featured icons, progress bars |
| `fg-brand-primary_alt` | `#1a3e88` | `#d4d4d4` | Brand icon → gray in dark (active tabs) |
| `fg-brand-secondary` | `#1d4597` | `#1d4597` | Brand accents, arrows |
| `fg-brand-secondary_alt` | `#1d4597` | `#525252` | Brand → gray in dark (brand buttons) |
| `fg-error-primary` | `#dc2626` | `#ef4444` | Primary error icons |
| `fg-error-secondary` | `#ef4444` | `#f87171` | Input error icons, negative charts |
| `fg-warning-primary` | `#ca8a04` | `#eab308` | Primary warning icons |
| `fg-warning-secondary` | `#eab308` | `#facc15` | Secondary warning icons |
| `fg-success-primary` | `#16a34a` | `#22c55e` | Primary success icons |
| `fg-success-secondary` | `#22c55e` | `#4ade80` | Dots, online indicators, positive charts |

---

## 4. Background colors

Use for fills on frames, shapes, and containers.

### Neutral & overlay

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `bg-primary` | `#ffffff` | `#0a0a0a` | Page/card/component backgrounds |
| `bg-primary_alt` | `#ffffff` | `#171717` | Alt primary (→ secondary in dark) |
| `bg-primary_hover` | `#fafafa` | `#171717` | Hover for white-bg components (menu items) |
| `bg-primary-solid` | `#0a0a0a` | `#262626` | Dark solid: tooltips |
| `bg-secondary` | `#fafafa` | `#171717` | Contrast against white (alternating sections) |
| `bg-secondary_alt` | `#fafafa` | `#0a0a0a` | Alt secondary (→ primary in dark): border tabs |
| `bg-secondary_hover` | `#f5f5f5` | `#262626` | Active nav items, date pickers |
| `bg-secondary-solid` | `#525252` | `#525252` | Dark solid: featured icons |
| `bg-tertiary` | `#f5f5f5` | `#262626` | Contrast against light bg: toggles |
| `bg-quaternary` | `#e5e5e5` | `#404040` | Higher contrast: sliders, progress bars |
| `bg-overlay` | `#0a0a0a` | `#262626` | Modal/dialog backdrop |

### Brand backgrounds

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `bg-brand-primary` | `#d2daea` | `#1d4597` | Light brand surfaces, check icons |
| `bg-brand-primary_alt` | `#e9edf5` | `#262626` | Brand fill → secondary in dark (active tabs) |
| `bg-brand-secondary` | `#bcc8e0` | `#1a3e88` | Featured icons |
| `bg-brand-solid` | `#1a3e88` | `#1a3e88` | Solid brand: buttons, toggles, messages |
| `bg-brand-solid_hover` | `#173779` | `#1d4597` | Solid brand, hover |
| `bg-brand-section` | `#14306a` | `#262626` | Dark brand sections: CTAs, testimonials |
| `bg-brand-section_subtle` | `#173779` | `#0a0a0a` | Subtle brand section: FAQ |

### Semantic backgrounds

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `bg-error-primary` | `#fef2f2` | red-950 * | Light error fill: error alerts/buttons |
| `bg-error-secondary` | `#fee2e2` | `#dc2626` | Error featured icons |
| `bg-error-solid` | `#dc2626` | `#dc2626` | Solid error: buttons, metrics |
| `bg-error-solid_hover` | `#b91c1c` | `#ef4444` | Solid error, hover |
| `bg-warning-primary` | `#fefce8` | yellow-950 * | Light warning fill |
| `bg-warning-secondary` | `#fef9c3` | `#ca8a04` | Warning featured icons |
| `bg-warning-solid` | `#ca8a04` | `#ca8a04` | Solid warning: featured icons |
| `bg-success-primary` | `#f0fdf4` | green-950 * | Light success fill |
| `bg-success-secondary` | `#dcfce7` | `#16a34a` | Success featured icons |
| `bg-success-solid` | `#16a34a` | `#16a34a` | Solid success: featured icons, metrics |

> \* Dark value resolves to the `-950` step of that hue, which wasn't surfaced
> in the current Figma extraction. Fill these three in on the next pass
> (they're the deepest tint of red/yellow/green).

---

## Application rules

### By element type
- **Text** → `text-*` · **Icons/indicators/shapes** → `fg-*` · **Strokes** → `border-*` · **Fills** → `bg-*`
- Never mix categories (e.g. never use a `text-*` variable for an icon fill).

### Hierarchy
Headings → `*-primary` · Labels/subheadings → `*-secondary` · Body → `*-tertiary` · Subtle → `*-quaternary`.

### Variant suffixes
- `_hover` — use the paired hover variable on hover interactions.
- `_on-brand` — text/fg placed on solid brand backgrounds (CTA sections, brand footer); lighter tints for legibility.
- `_alt` — switches from brand color to neutral gray in **dark** mode (tabs, brand buttons). The non-alt version keeps the brand color in both modes.

### Semantic color rules
- **Error** (red) = validation failures, destructive states, critical alerts.
- **Warning** (yellow) = caution, approaching limits, deprecation.
- **Success** (green) = completed actions, positive metrics, online status.
- Each state has primary (lightest fill), secondary (medium), and solid (dark) background variants. Never rely on color alone — pair with text and an icon.

### Accessibility
- `text-placeholder` is neutral-500 (not 400) in light mode for contrast — don't override.
- `*-solid` backgrounds use the same value in both modes (consistent across themes).
- With `text-white`/`fg-white`, ensure ≥ 4.5:1 contrast (3:1 for large text/icons).
- Always test both light and dark.

### Common component mappings

**Input field:** label `text-secondary` · placeholder `text-placeholder` · value `text-primary` · border `border-primary` · border (focus) `border-brand` · border (error) `border-error` · icon `fg-quaternary` · error message `text-error-primary` · bg `bg-primary`

**Primary button:** bg `bg-brand-solid` · bg hover `bg-brand-solid_hover` · text `text-white` · icon `fg-white`

**Card:** bg `bg-primary` · border `border-secondary` · title `text-primary` · subtitle `text-secondary` · body `text-tertiary`

**Modal:** overlay `bg-overlay` · bg `bg-primary` · title `text-primary` · body `text-tertiary`

**Sidebar nav:** bg `bg-primary` · item text `text-secondary` · active bg `bg-secondary_hover` · active text `text-brand-secondary` · icon `fg-quaternary` · active icon `fg-brand-primary`

**Tooltip:** bg `bg-primary-solid` · text `text-white`

**Alerts:** error → bg `bg-error-primary`, border `border-error`, text `text-error-primary`, icon `fg-error-primary` · warning → bg `bg-warning-primary`, text `text-warning-primary`, icon `fg-warning-primary` · success → bg `bg-success-primary`, text `text-success-primary`, icon `fg-success-primary`
