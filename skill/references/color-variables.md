# Color Variables — semantic tokens with real values

This is the layer you actually apply. Bind every element to one of these
**semantic** variables — never a raw hex or a primitive step directly. Each
resolves automatically across light and dark modes.

- **Light** and **dark** values are both resolved from the **S1 Brand Guideline**
  variables export (`s1-ds.json`): each semantic token's per-mode alias resolved
  against the primitive scales in [`tokens.md`](tokens.md). This is the
  Untitled-UI-based S1 palette.
- Rule of thumb: text → `text-*`, icons/indicators → `fg-*`, strokes → `border-*`,
  fills → `bg-*`. Never cross categories.

---

## 1. Text colors

Use for all text. Never fill text nodes with a raw color.

### Neutral hierarchy

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `text-primary` | `#181d27` | `#f7f7f7` | Headings, titles, prominent labels |
| `text-primary_on-brand` | `#ffffff` | `#f7f7f7` | Primary text on solid brand backgrounds |
| `text-secondary` | `#414651` | `#cecfd2` | Labels, section headings |
| `text-secondary_hover` | `#252b37` | `#ececed` | Secondary text, hover |
| `text-secondary_on-brand` | `#a5b5d5` | `#cecfd2` | Secondary text on brand backgrounds |
| `text-tertiary` | `#535862` | `#94979c` | Body/supporting text, descriptions |
| `text-tertiary_hover` | `#414651` | `#cecfd2` | Tertiary text, hover |
| `text-tertiary_on-brand` | `#a5b5d5` | `#94979c` | Tertiary text on brand backgrounds |
| `text-quaternary` | `#717680` | `#94979c` | Subtle, low-contrast text (footer headings) |
| `text-quaternary_on-brand` | `#7991c0` | `#94979c` | Quaternary text on brand backgrounds |

### Special & brand text

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `text-white` | `#ffffff` | `#ffffff` | Always-white text |
| `text-placeholder` | `#717680` | `#85888e` | Input placeholders (neutral-500 for contrast) |
| `text-brand-primary` | `#42307d` | `#f7f7f7` | Primary brand headings (pricing headers) |
| `text-brand-secondary` | `#132b5a` | `#cecfd2` | Brand buttons, accents, subheadings |
| `text-brand-secondary_hover` | `#0c1c3c` | `#ececed` | Brand secondary text, hover |
| `text-brand-tertiary` | `#193978` | `#94979c` | Lighter accents (metric numbers) |
| `text-brand-tertiary_alt` | `#193978` | `#f7f7f7` | Link buttons (lighter in dark) |

### Semantic text

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `text-error-primary` | `#d92d20` | `#f97066` | Error messages |
| `text-warning-primary` | `#dc6803` | `#fdb022` | Warning text |
| `text-success-primary` | `#079455` | `#47cd89` | Success text |

---

## 2. Border colors

Use for all strokes and borders.

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `border-primary` | `#d5d7da` | `#373a41` | High-contrast: inputs, button groups, checkboxes |
| `border-secondary` | `#e9eaeb` | `#22262f` | Default: cards, tables, dividers, file uploaders |
| `border-secondary_alt` | `#00000014` | `#22262f` | Alpha alt for floating menus (dropdowns, notifications) |
| `border-tertiary` | `#f5f5f5` | `#22262f` | Low-contrast: subtle dividers, chart axes |
| `border-brand` | `#1f4796` | `#4c6cab` | Active/focused inputs, selected states |
| `border-brand_alt` | `#193978` | `#373a41` | Brand border → gray in dark (banners, footers) |
| `border-error` | `#f04438` | `#f97066` | Error borders: inputs, file uploader |
| `border-error_subtle` | `#fda29b` | `#f04438` | Subtle error borders |

---

## 3. Foreground colors (icons, indicators)

Use for icons, progress bars, dots, decorative shapes. Never use `text-*` on an
icon or `fg-*` on text.

### Neutral hierarchy

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `fg-primary` | `#181d27` | `#ffffff` | Highest-contrast icons |
| `fg-secondary` | `#414651` | `#cecfd2` | High-contrast icons |
| `fg-secondary_hover` | `#252b37` | `#ececed` | Secondary icons, hover |
| `fg-tertiary` | `#535862` | `#94979c` | Medium-contrast icons |
| `fg-tertiary_hover` | `#414651` | `#cecfd2` | Tertiary icons, hover |
| `fg-quaternary` | `#a4a7ae` | `#61656c` | Low-contrast: button/help/input icons |
| `fg-quaternary_hover` | `#717680` | `#85888e` | Quaternary icons, hover |
| `fg-white` | `#ffffff` | `#ffffff` | Always-white icons |

### Brand & semantic

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `fg-brand-primary` | `#193978` | `#1f4796` | Primary brand icons, featured icons, progress bars |
| `fg-brand-primary_alt` | `#193978` | `#cecfd2` | Brand icon → gray in dark (active tabs) |
| `fg-brand-secondary` | `#1f4796` | `#1f4796` | Brand accents, arrows |
| `fg-brand-secondary_alt` | `#1f4796` | `#61656c` | Brand → gray in dark (brand buttons) |
| `fg-error-primary` | `#d92d20` | `#f04438` | Primary error icons |
| `fg-error-secondary` | `#f04438` | `#f97066` | Input error icons, negative charts |
| `fg-warning-primary` | `#dc6803` | `#f79009` | Primary warning icons |
| `fg-warning-secondary` | `#f79009` | `#fdb022` | Secondary warning icons |
| `fg-success-primary` | `#079455` | `#17b26a` | Primary success icons |
| `fg-success-secondary` | `#17b26a` | `#47cd89` | Dots, online indicators, positive charts |

---

## 4. Background colors

Use for fills on frames, shapes, and containers.

### Neutral & overlay

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `bg-primary` | `#ffffff` | `#0c0e12` | Page/card/component backgrounds |
| `bg-primary_alt` | `#ffffff` | `#13161b` | Alt primary (→ secondary in dark) |
| `bg-primary_hover` | `#fafafa` | `#22262f` | Hover for white-bg components (menu items) |
| `bg-primary-solid` | `#0a0d12` | `#13161b` | Dark solid: tooltips |
| `bg-secondary` | `#fafafa` | `#13161b` | Contrast against white (alternating sections) |
| `bg-secondary_alt` | `#fafafa` | `#0c0e12` | Alt secondary (→ primary in dark): border tabs |
| `bg-secondary_hover` | `#f5f5f5` | `#22262f` | Active nav items, date pickers |
| `bg-secondary-solid` | `#535862` | `#61656c` | Dark solid: featured icons |
| `bg-tertiary` | `#f5f5f5` | `#22262f` | Contrast against light bg: toggles |
| `bg-quaternary` | `#e9eaeb` | `#373a41` | Higher contrast: sliders, progress bars |
| `bg-overlay` | `#0a0d12` | `#22262f` | Modal/dialog backdrop |

### Brand backgrounds

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `bg-brand-primary` | `#d2daea` | `#1f4796` | Light brand surfaces, check icons |
| `bg-brand-primary_alt` | `#d2daea` | `#13161b` | Brand fill → secondary in dark (active tabs) |
| `bg-brand-secondary` | `#bcc8e0` | `#193978` | Featured icons |
| `bg-brand-solid` | `#193978` | `#193978` | Solid brand: buttons, toggles, messages |
| `bg-brand-solid_hover` | `#132b5a` | `#1f4796` | Solid brand, hover |
| `bg-brand-section` | `#0c1c3c` | `#13161b` | Dark brand sections: CTAs, testimonials |
| `bg-brand-section_subtle` | `#132b5a` | `#0c0e12` | Subtle brand section: FAQ |

### Semantic backgrounds

| Variable | Light | Dark | When to use |
|---|---|---|---|
| `bg-error-primary` | `#fef3f2` | `#55160c` | Light error fill: error alerts/buttons |
| `bg-error-secondary` | `#fee4e2` | `#d92d20` | Error featured icons |
| `bg-error-solid` | `#d92d20` | `#d92d20` | Solid error: buttons, metrics |
| `bg-error-solid_hover` | `#b42318` | `#f04438` | Solid error, hover |
| `bg-warning-primary` | `#fffaeb` | `#4e1d09` | Light warning fill |
| `bg-warning-secondary` | `#fef0c7` | `#dc6803` | Warning featured icons |
| `bg-warning-solid` | `#dc6803` | `#dc6803` | Solid warning: featured icons |
| `bg-success-primary` | `#ecfdf3` | `#053321` | Light success fill |
| `bg-success-secondary` | `#dcfae6` | `#079455` | Success featured icons |
| `bg-success-solid` | `#079455` | `#079455` | Solid success: featured icons, metrics |

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
