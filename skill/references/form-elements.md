
# Form Elements Component Library

This skill defines every component in the FORM ELEMENTS group of the design system. Use these components — never recreate them from scratch — when building any form, data-entry, or interactive-control UI.

---

## Component Inventory

### 1. Input Field

**Component:** `Input field` (StateGroupId:1090:57817)
**Page:** ↳ Inputs

A single-line text input with label, hint text, help icon, and leading/trailing add-ons.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md`, `lg` | `sm` |
| Type | `Default`, `Leading dropdown`, `Trailing dropdown`, `Leading text`, `Payment input`, `Tags inner`, `Tags outer`, `Trailing button`, `Password`, `Date and time`, `Number counter horizontal`, `Number counter vertical`, `OTP`, `File upload` | `Default` |
| Destructive | `False`, `True` | `False` |
| State | `Placeholder`, `Filled`, `Focused`, `Disabled` | `Placeholder` |

**Boolean properties:**
- `Label` (default: on) — field label above the input
- `Hint text` (default: on) — helper text below the input
- `Help icon` (default: on) — tooltip trigger icon beside the label
- `Required *` (default: on) — asterisk indicating required field
- `Icon leading` (default: on) — icon inside the input, left side
- `Time selector` (default: on) — time picker add-on (Date and time type)

**Instance swap:** `Icon swap` — swap the leading/trailing icon

**When to use:**
- `Default` — standard text entry (name, email, URL, etc.)
- `Password` — password entry with show/hide toggle
- `Leading dropdown` / `Trailing dropdown` — input paired with a dropdown (e.g. phone country code + number, currency selector + amount)
- `Leading text` — input with a static text prefix (e.g. "https://")
- `Payment input` — credit card number entry
- `Tags inner` / `Tags outer` — multi-value token entry (e.g. email recipients)
- `Trailing button` — input with an action button (e.g. search, copy)
- `Date and time` — date/time value entry
- `Number counter horizontal` / `Number counter vertical` — numeric stepper
- `OTP` — one-time passcode entry
- `File upload` — inline file attachment input

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-placeholder` #717680, `fg-quaternary` #a4a7ae, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `border-brand` #1f4796, `bg-primary` #ffffff, `text-error-primary` #d92d20, `border-error` #f04438, `fg-success-primary` #079455, …
- Radius: `radius-sm` 6, `radius-md` 8
- Spacing: `spacing-none` 0, `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16
- Type: `Text xs/Regular` 12/18, `Text xs/Medium` 12/18, `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Text md/Regular` 16/24, `Text md/Medium` 16/24, `Text md/Semibold` 16/24

---

### 2. Textarea Input Field

**Component:** `Textarea input field` (StateGroupId:1238:278)
**Page:** ↳ Inputs

Multi-line text input for longer-form content.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md` | `sm` |
| Type | `Default`, `Tags inner`, `Tags outer` | `Default` |
| Destructive | `False`, `True` | `False` |
| State | `Placeholder`, `Default`, `Focused`, `Disabled` | `Placeholder` |

**Boolean properties:**
- `Label` (default: on)
- `Hint text` (default: on)
- `Required *` (default: on)
- `Help icon` (default: on)
- `Resize handle` (default: on) — corner drag handle for resizing

**When to use:**
- Comments, descriptions, bio fields, notes, and any content that may exceed a single line
- `Tags inner` / `Tags outer` — multi-value entry within a textarea context

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-placeholder` #717680, `fg-quaternary` #a4a7ae, `border-primary` #d5d7da, `border-brand` #1f4796, `border-error` #f04438, `border-error_subtle` #fda29b, `text-error-primary` #d92d20, `text-brand-tertiary` #193978, `bg-primary` #ffffff
- Radius: `radius-sm` 6, `radius-md` 8
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12
- Type: `Text xs/Regular` 12/18, `Text xs/Medium` 12/18, `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text md/Regular` 16/24

---

### 3. Verification Code Input Field

**Component:** `Verification code input field` (StateGroupId:1106:66757)
**Page:** ↳ Inputs

Segmented digit input for verification/OTP codes.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md`, `lg` | `sm` |
| Digits | `4`, `6` | `4` |

**Boolean properties:**
- `Label` (default: on)
- `Hint text` (default: on)

**When to use:**
- Email/phone verification flows, two-factor authentication, PIN entry

**Tokens used** (from Figma)
- Color: `text-tertiary` #535862, `text-secondary` #414651, `text-placeholder` #717680, `border-primary` #d5d7da, `bg-primary` #ffffff, `utility-neutral-300` #d5d7da
- Radius: `radius-lg` 10, `radius-xl` 12
- Spacing: `spacing-xxs` 2, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Display lg/Medium` 48/60, `Display xl/Medium` 60/72

---

### 4. Checkbox

**Component:** `Checkbox` (StateGroupId:1097:63652)
**Page:** ↳ Checkboxes

Individual checkbox or radio-style check with optional label and supporting text.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Checked | `False`, `True` | `False` |
| Indeterminate | `False`, `True` | `False` |
| Size | `sm`, `md` | `sm` |
| Type | `Checkbox`, `Radio` | `Checkbox` |
| Text | `False`, `True` | `False` |
| State | `Default`, `Hover`, `Focused`, `Disabled` | `Default` |

**Boolean properties:**
- `Supporting text` (default: on)

**When to use:**
- `Checkbox` type — multi-select options (e.g. "Select all that apply"), terms acceptance, preferences
- `Radio` type — single-select within a list where Radio group is not needed
- `Indeterminate` — parent checkbox with partially selected children (e.g. "Select all" in a table)

**Tokens used** (from Figma)
- Color: `text-secondary` #414651, `text-tertiary` #535862, `fg-white` #ffffff, `border-primary` #d5d7da, `bg-primary` #ffffff, `bg-brand-solid` #193978, `bg-tertiary` #f5f5f5
- Radius: `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text md/Regular` 16/24, `Text md/Medium` 16/24

---

### 5. Toggle

**Component:** `Toggle` (StateGroupId:1102:4208)
**Page:** ↳ Toggles

On/off switch for binary settings.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Default`, `Slim` | `Default` |
| Pressed | `False`, `True` | `False` |
| Size | `sm`, `md` | `sm` |
| Text | `False`, `True` | `False` |
| State | `Default`, `Hover`, `Focus`, `Disabled` | `Default` |

**Boolean properties:**
- `Supporting text` (default: on)

**When to use:**
- Settings that take effect immediately (notifications, dark mode, feature flags)
- `Slim` — compact toggle for dense UIs (settings panels, table rows)
- Prefer Toggle over Checkbox when the change applies instantly without a form submission

**Tokens used** (from Figma)
- Color: `text-secondary` #414651, `text-tertiary` #535862, `fg-white` #ffffff, `border-secondary` #e9eaeb, `bg-primary` #ffffff, `bg-brand-solid` #193978, `bg-brand-solid_hover` #132b5a, `bg-tertiary` #f5f5f5
- Radius: `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-md` 8, `spacing-lg` 12
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text md/Regular` 16/24, `Text md/Medium` 16/24

---

### 6. Radio Group

**Component:** `Radio group` (StateGroupId:1142:87213)
**Page:** ↳ Radio groups

A group of mutually exclusive options.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md` | `sm` |
| Type | `Icon simple`, `Icon card`, `Avatar`, `Payment icon`, `Radio button`, `Checkbox` | `Icon simple` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Sub-component:** `Radio group item` (StateGroupId:124:2838) — individual item within the group.

| Property | Options | Default |
|---|---|---|
| Selected | `False`, `True` | `False` |
| Size | `sm`, `md` | `sm` |
| Type | `Icon simple`, `Icon card`, `Avatar`, `Payment icon`, `Radio button`, `Checkbox` | `Icon simple` |
| State | `Default`, `Hover`, `Focused` | `Default` |
| Breakpoint | `Mobile`, `Desktop` | `Desktop` |

**Boolean properties (item):**
- `Badge` (default: on) — optional badge on the item

**When to use:**
- `Radio button` — standard radio selection (plan tiers, shipping method)
- `Icon simple` / `Icon card` — visual option picker with icons (layout options, category selection)
- `Avatar` — person/team selection
- `Payment icon` — payment method selection (Visa, Mastercard, etc.)
- `Checkbox` — checkbox-styled items within a radio group context

**Tokens used** (from Figma)
- Color: `text-secondary` #414651, `text-tertiary` #535862, `text-brand-secondary` #132b5a, `fg-secondary` #414651, `fg-white` #ffffff, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `border-brand` #1f4796, `bg-primary` #ffffff, `bg-brand-solid` #193978, `utility-green-500` #16b364
- Radius: `radius-xs` 4, `radius-sm` 6, `radius-md` 8, `radius-xl` 12, `radius-full` 9999
- Spacing: `spacing-none` 0, `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-2xl` 20
- Type: `Text xs/Medium` 12/18, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Text md/Regular` 16/24, `Text md/Medium` 16/24, `Text md/Semibold` 16/24, `Text lg/Medium` 18/28, `Text lg/Semibold` 18/28, `Display sm/Semibold` 30/38, `Display md/Semibold` 36/44

---

### 7. Select

**Component:** `Select` (StateGroupId:3281:377673)
**Page:** ↳ Select

Single-selection dropdown.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md`, `lg` | `sm` |
| Type | `Default`, `Icon leading`, `Avatar leading`, `Dot leading`, `Search`, `Tags` | `Default` |
| State | `Placeholder`, `Default`, `Focused`, `Open`, `Disabled` | `Placeholder` |

**Boolean properties:**
- `Label` (default: on)
- `Hint text` (default: on)
- `Supporting text` (default: on)
- `Scroll bar` (default: on)
- `Required *` (default: on)
- `Help icon` (default: on)
- `Shortcut` (default: on) — keyboard shortcut hint

**Instance swap:** `Icon swap` — swap the leading icon

**When to use:**
- Choosing one option from a long list (country, timezone, category)
- `Search` — filterable select for large option sets
- `Icon leading` / `Avatar leading` / `Dot leading` — visual differentiation of options (status, user, category)
- `Tags` — selected value shown as tag/chip

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-placeholder` #717680, `fg-quaternary` #a4a7ae, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `border-brand` #1f4796, `bg-primary` #ffffff, `bg-primary_hover` #fafafa, `fg-brand-primary` #193978, `fg-success-secondary` #17b26a, …
- Radius: `radius-xs` 4, `radius-sm` 6, `radius-md` 8, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12
- Type: `Text xs/Regular` 12/18, `Text xs/Medium` 12/18, `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text md/Regular` 16/24, `Text md/Medium` 16/24

---

### 8. Multi-select

**Component:** `Multi-select` (StateGroupId:12206:577041)
**Page:** ↳ Select

Multi-selection dropdown with search and tag display.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md`, `lg` | `sm` |
| State | `Default`, `Active`, `Focused`, `Open default`, `Open active`, `Search empty state`, `Disabled` | `Default` |

**Boolean properties:**
- `Label` (default: on)
- `Hint text` (default: on)
- `Supporting text` (default: on)
- `Scroll bar` (default: on)
- `Required *` (default: on)
- `Help icon` (default: on)

**When to use:**
- Selecting multiple items from a list (assign team members, select categories, tag content)

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-placeholder` #717680, `fg-quaternary` #a4a7ae, `fg-white` #ffffff, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `border-brand` #1f4796, `bg-primary` #ffffff, `bg-brand-solid` #193978, `text-brand-secondary` #132b5a, …
- Radius: `radius-sm` 6, `radius-md` 8, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-2xl` 20
- Type: `Text xs/Regular` 12/18, `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Text md/Regular` 16/24, `Text md/Medium` 16/24

---

### 9. Slider

**Component:** `Slider` (StateGroupId:1086:534)
**Page:** ↳ Sliders

Range slider for selecting numeric values.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Label | `False`, `Bottom`, `Top floating` | `False` |
| Right control | `25%`, `50%`, `75%`, `100%` | `25%` |
| Left control | `0%`, `25%`, `50%`, `75%` | `0%` |

**When to use:**
- Price range filters, volume/brightness control, budget allocation
- Use two control handles for range selection (min/max)
- `Top floating` label — shows value in a floating tooltip above the handle
- `Bottom` label — shows value below the track

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `fg-brand-primary` #193978, `bg-primary` #ffffff, `bg-primary_alt` #ffffff, `bg-brand-solid` #193978, `bg-quaternary` #e9eaeb, `border-secondary_alt` #00000014
- Radius: `radius-md` 8, `radius-full` 9999
- Spacing: `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12
- Type: `Text xs/Semibold` 12/18, `Text md/Medium` 16/24

---

### 10. Progress Bar

**Component:** `Progress bar` (StateGroupId:1085:57382)
**Page:** ↳ Progress indicators

Horizontal bar showing completion progress.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Progress | `0%` through `100%` (10% increments) | `0%` |
| Label | `False`, `Right`, `Bottom`, `Top floating`, `Bottom floating` | `False` |

**When to use:**
- File upload progress, onboarding completion, multi-step form progress, loading states

**Tokens used** (from Figma)
- Color: `text-secondary` #414651, `fg-brand-primary` #193978, `bg-primary` #ffffff, `bg-primary_alt` #ffffff, `bg-quaternary` #e9eaeb, `border-secondary_alt` #00000014
- Radius: `radius-md` 8, `radius-full` 9999
- Spacing: `spacing-xs` 4, `spacing-md` 8, `spacing-lg` 12
- Type: `Text xs/Semibold` 12/18, `Text sm/Medium` 14/20

---

### 11. Progress Circle

**Component:** `Progress circle` (StateGroupId:1084:2717)
**Page:** ↳ Progress indicators

Circular/semi-circular progress indicator.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `xxs`, `xs`, `sm`, `md`, `lg` | `xxs` |
| Shape | `Circle`, `Half circle` | `Circle` |

**Boolean properties:**
- `Label` (default: on) — percentage text inside the circle

**When to use:**
- Dashboard KPIs, storage usage, skill/score visualization
- `Half circle` — gauge-style meter (e.g. performance score)

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-tertiary` #535862, `fg-brand-primary` #193978, `bg-primary` #ffffff, `bg-quaternary` #e9eaeb
- Spacing: `spacing-xs` 4
- Type: `Text xs/Medium` 12/18, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Display xs/Semibold` 24/32, `Display sm/Semibold` 30/38, `Display md/Semibold` 36/44, `Display lg/Semibold` 48/60

---

### 12. Tooltip

**Component:** `Tooltip` (StateGroupId:1052:489)
**Page:** ↳ Tooltips

Contextual information popup triggered on hover/focus.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Supporting text | `False`, `True` | `False` |
| Arrow | `None`, `Bottom left`, `Bottom right`, `Left`, `Right`, `Bottom center`, `Top center` | `None` |

**Text property:** `Text` (default: "This is a tooltip")

**When to use:**
- Explaining icons, abbreviations, truncated text, or disabled controls
- Always pair with a keyboard-focusable trigger for accessibility

**Tokens used** (from Figma)
- Color: `text-white` #ffffff, `bg-primary` #ffffff, `bg-primary-solid` #0a0d12
- Radius: `radius-md` 8
- Spacing: `spacing-xxs` 2, `spacing-md` 8, `spacing-lg` 12
- Type: `Text xs/Medium` 12/18, `Text xs/Semibold` 12/18

---

### 13. Help Icon

**Component:** `Help icon` (StateGroupId:1054:13)
**Page:** ↳ Tooltips

Question-mark icon that reveals a tooltip on interaction.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Open | `False`, `True` | `False` |
| Supporting text | `False`, `True` | `False` |
| Tooltip | `Top no arrow`, `Top arrow`, `Left`, `Top left`, `Bottom`, `Right`, `Top right` | `Top no arrow` |

**Boolean properties:**
- `Cursor` (default: on)

**When to use:**
- Beside form labels to explain field purpose or expected format
- On settings to clarify impact of a toggle or option

**Tokens used** (from Figma)
- Color: `text-white` #ffffff, `fg-quaternary` #a4a7ae, `fg-quaternary_hover` #717680, `bg-primary` #ffffff, `bg-primary-solid` #0a0d12
- Radius: `radius-md` 8
- Spacing: `spacing-xxs` 2, `spacing-md` 8, `spacing-lg` 12
- Type: `Text xs/Medium` 12/18, `Text xs/Semibold` 12/18

---

### 14. File Upload

**Component:** `File upload` (StateGroupId:1175:101149)
**Page:** ↳ File upload

Drag-and-drop file upload zone with queued file list.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Files queued | `True`, `False` | `False` |
| Type | `Progress bar`, `Progress fill` | `Progress bar` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**When to use:**
- Document uploads, image uploads, bulk file imports
- `Progress bar` — shows individual file progress as a bar
- `Progress fill` — shows progress as a fill overlay on the file icon

**Tokens used** (from Figma)
- Color: `text-secondary` #414651, `text-tertiary` #535862, `text-quaternary` #717680, `text-brand-secondary` #132b5a, `text-success-primary` #079455, `fg-secondary` #414651, `fg-quaternary` #a4a7ae, `fg-brand-primary` #193978, `fg-white` #ffffff, `fg-success-primary` #079455, `border-primary` #d5d7da, `border-secondary` #e9eaeb, …
- Radius: `radius-none` 0, `radius-sm` 6, `radius-md` 8, `radius-xl` 12, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-3xl` 24
- Type: `Text xs/Regular` 12/18, `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20

---

### 15. Text Editor

**Component:** `Text editor` (StateGroupId:9292:559325)
**Page:** ↳ Text editors

Rich text editor with formatting toolbar.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Default`, `Floating toolbar` | `Default` |
| Size | `sm`, `md` | `sm` |

**Boolean properties:**
- `Scroll bar` (default: on)
- `Hint text` (default: on)

**Sub-components:**
- `Text editor toolbar` — `Simple` or `Advanced` type, with optional `Dropdowns`
- `Text editor tooltip` — `Simple` or `Advanced` formatting tooltip

**When to use:**
- Blog/article authoring, comment editing with formatting, email composition, note-taking
- `Default` — toolbar pinned at top
- `Floating toolbar` — toolbar appears on text selection

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-tertiary` #535862, `fg-quaternary` #a4a7ae, `border-primary` #d5d7da, `border-secondary_alt` #00000014, `bg-primary` #ffffff, `utility-neutral-900` #181d27
- Radius: `radius-sm` 6, `radius-md` 8, `radius-xl` 12, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-2xl` 20
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text md/Regular` 16/24

---

### 16. Button Group

**Component:** `Button group` (StateGroupId:1046:10171)
**Page:** ↳ Button groups

Segmented control / button bar for toggling between views or options.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md` | `sm` |
| Icon | `False`, `Leading`, `Only` | `False` |

**When to use:**
- View switchers (list/grid/map), filter toggles, segmented controls
- `Icon Only` — compact toolbar actions
- `Leading` — icon + text per segment

**Tokens used** (from Figma)
- Color: `text-secondary` #414651, `fg-quaternary` #a4a7ae, `border-primary` #d5d7da, `bg-primary` #ffffff
- Radius: `radius-md` 8
- Spacing: `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16
- Type: `Text sm/Semibold` 14/20

---

### 17. Date Picker Dropdown

**Component:** `Date picker dropdown` (StateGroupId:1150:16803)
**Page:** ↳ Date pickers

Date selection dropdown with calendar.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Opened | `False`, `True` | `False` |
| Type | `Dual dates`, `Single date`, `Available times` | `Dual dates` |
| State | `Placeholder`, `Active` | `Placeholder` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**When to use:**
- `Single date` — birthday, due date, event date
- `Dual dates` — date range (check-in/check-out, reporting period)
- `Available times` — date + time slot selection (booking, scheduling)

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-quaternary` #717680, `text-placeholder` #717680, `text-brand-secondary` #132b5a, `fg-secondary` #414651, `fg-quaternary` #a4a7ae, `fg-brand-primary` #193978, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `bg-primary` #ffffff, `bg-brand-solid` #193978, …
- Radius: `radius-sm` 6, `radius-md` 8, `radius-2xl` 16, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-2xl` 20, `spacing-3xl` 24
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Text md/Regular` 16/24

---

### 18. Date Picker Modal

**Component:** `Date picker modal` (StateGroupId:1547:269867)
**Page:** ↳ Date pickers

Full-screen or centered modal date picker.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Dual dates`, `Single date`, `Available times` | `Dual dates` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**When to use:**
- Mobile date selection, complex date range picking, calendar-heavy flows where the dropdown would be too small

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-white` #ffffff, `text-brand-secondary` #132b5a, `fg-secondary` #414651, `fg-quaternary` #a4a7ae, `fg-brand-primary` #193978, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `bg-primary` #ffffff, `bg-secondary` #fafafa, `bg-overlay` #0a0d12, …
- Radius: `radius-sm` 6, `radius-md` 8, `radius-2xl` 16
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `container-padding-mobile` 16, `spacing-2xl` 20, `spacing-3xl` 24, `spacing-4xl` 32, `container-padding-desktop` 32, `spacing-8xl` 80
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Text md/Regular` 16/24

---

### 19. Color Picker

**Component:** `Color picker` (StateGroupId:12423:52680)
**Page:** ↳ Color pickers

Full-featured color selection component.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Solid color`, `Gradient stops`, `Image upload`, `Color swatch`, `Saved swatches sm`, `Saved swatches md`, `Brand swatches`, `Gray swatches`, `Minimal picker`, `Hue slider`, `Transparency slider`, `Palette picker` | `Solid color` |

**Boolean properties:**
- `Tabs` (default: on)

**When to use:**
- Theme customization, brand color selection, design tool color input
- `Solid color` — full spectrum picker
- `Palette picker` / `Brand swatches` / `Gray swatches` — constrained palette selection
- `Gradient stops` — gradient editor

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-quaternary` #717680, `fg-white` #ffffff, `fg-quaternary` #a4a7ae, `fg-brand-primary_alt` #193978, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `bg-primary` #ffffff, `bg-tertiary` #f5f5f5, `utility-brand-600` #193978, …
- Radius: `radius-sm` 6, `radius-md` 8, `radius-xl` 12, `radius-2xl` 16, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-2xl` 20
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Text lg/Semibold` 18/28

---

### 20. Color Picker Dropdown

**Component:** `Color picker dropdown` (StateGroupId:12424:15898)
**Page:** ↳ Color pickers

Compact color picker triggered from a swatch or input.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Swatch sm`, `Swatch button`, `Swatch button link`, `Hex input`, `Select`, `Swatch md` | `Swatch sm` |
| Open | `False`, `True` | `False` |

**Boolean properties:**
- `Percentage input` (default: on)

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-quaternary` #717680, `text-brand-secondary` #132b5a, `fg-white` #ffffff, `fg-quaternary` #a4a7ae, `fg-brand-primary_alt` #193978, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `border-brand` #1f4796, `bg-primary` #ffffff, …
- Radius: `radius-sm` 6, `radius-md` 8, `radius-xl` 12, `radius-2xl` 16, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-2xl` 20
- Type: `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20

---

### 21. Calendar

**Component:** `Calendar` (StateGroupId:8022:24550)
**Page:** ↳ Calendars

Full calendar view for event display and scheduling.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Month view`, `Week view`, `Day view` | `Month view` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**When to use:**
- Event/schedule management, booking systems, project timelines
- `Month view` — overview of events across a month
- `Week view` — detailed weekly schedule with time slots
- `Day view` — granular daily schedule

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-quaternary` #717680, `text-brand-secondary` #132b5a, `fg-white` #ffffff, `fg-quaternary` #a4a7ae, `fg-brand-primary` #193978, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `bg-primary` #ffffff, `bg-brand-solid` #193978, …
- Radius: `radius-xxs` 2, `radius-sm` 6, `radius-md` 8, `radius-xl` 12, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-2xl` 20, `spacing-3xl` 24
- Type: `Text xs/Regular` 12/18, `Text xs/Medium` 12/18, `Text xs/Semibold` 12/18, `Text sm/Regular` 14/20, `Text sm/Medium` 14/20, `Text sm/Semibold` 14/20, `Text md/Semibold` 16/24, `Text lg/Semibold` 18/28, `Text lg/Bold` 18/28

---

### 22. Dropdown Menu

**Component:** `Dropdown menu` (StateGroupId:3281:383083)
**Page:** ↳ Dropdowns

General-purpose dropdown menu triggered by buttons, icons, or account elements.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Button simple`, `Button advanced`, `Button link`, `Icon simple`, `Icon advanced`, `Search simple`, `Search advanced`, `Integrations`, `Account button`, `Account avatar`, `Account card xs`, `Account card sm`, `Account card md`, `Account breadcrumb` | `Button simple` |
| Open | `False`, `True` | `False` |

**Boolean properties:**
- `Scrollbar` (default: on)
- `Chevron dropdown` (default: on)

**When to use:**
- `Button simple` / `Button advanced` — action menus from buttons
- `Icon simple` / `Icon advanced` — kebab/meatball menus, toolbar overflow
- `Search simple` / `Search advanced` — filterable dropdown menus
- `Account *` — user/profile menus in navigation

**Tokens used** (from Figma)
- Color: `text-primary` #181d27, `text-secondary` #414651, `text-tertiary` #535862, `text-quaternary` #717680, `text-placeholder` #717680, `fg-white` #ffffff, `fg-quaternary` #a4a7ae, `fg-brand-primary` #193978, `border-primary` #d5d7da, `border-secondary` #e9eaeb, `bg-primary` #ffffff, `bg-brand-solid` #193978, …
- Radius: `radius-xs` 4, `radius-sm` 6, `radius-md` 8, `radius-lg` 10, `radius-xl` 12, `radius-full` 9999
- Spacing: `spacing-xxs` 2, `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8, `spacing-lg` 12, `spacing-xl` 16, `spacing-3xl` 24
- Type: `Text xs/Regular` 12/18, `Text xs/Medium` 12/18, `Text xs/Semibold` 12/18, `Text sm/Regular` 14/20, `Text sm/Semibold` 14/20

---

### 23. Context Menu

**Component:** `Context menu` (StateGroupId:11547:540792)
**Page:** ↳ Dropdowns

Right-click context menu.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Simple`, `Advanced` | `Simple` |
| Open | `False`, `True` | `False` |

**When to use:**
- Right-click actions on table rows, canvas elements, file items
- `Advanced` — includes keyboard shortcuts and sub-menus

**Tokens used** (from Figma)
- Color: `text-secondary` #414651, `text-secondary_hover` #252b37, `text-quaternary` #717680, `fg-quaternary` #a4a7ae, `fg-brand-primary` #193978, `fg-success-secondary` #17b26a, `border-secondary` #e9eaeb, `border-secondary_alt` #00000014, `bg-primary` #ffffff, `bg-primary_hover` #fafafa
- Radius: `radius-sm` 6, `radius-md` 8
- Spacing: `spacing-xs` 4, `spacing-sm` 6, `spacing-md` 8
- Type: `Text xs/Medium` 12/18, `Text sm/Semibold` 14/20

---

## Shared Size Convention

Most form components use a consistent size scale:
- **sm** — compact density; use in data-heavy UIs, tables, sidebars
- **md** — standard density; use in most forms and settings pages
- **lg** — touch-friendly; use in mobile-first or marketing/onboarding flows

Always use the same size across all form elements within a single form for visual consistency.

---

## UX, Accessibility & Heuristic Best Practices

### Labels & Help Text
- Always show `Label` on form fields (do not rely on placeholder text alone)
- Use `Hint text` to clarify expected format or constraints (e.g. "Must be at least 8 characters")
- Use `Help icon` for longer explanations that would clutter the form
- Mark required fields with `Required *`; alternatively, mark optional fields when most are required

### States
- Show `Focused` state on keyboard navigation for all interactive elements
- Use `Disabled` sparingly — prefer hiding unavailable options or explaining why they are disabled via a tooltip
- Use `Destructive=True` on Input fields only for real-time validation errors — never as the default state
- Always pair error states with clear, specific error messages in `Hint text`

### Input Selection Guide
- **< 5 options, single-select:** Radio group (all options visible)
- **< 5 options, multi-select:** Checkbox group
- **5-15 options, single-select:** Select dropdown
- **5+ options, multi-select:** Multi-select with search
- **Binary on/off, immediate effect:** Toggle
- **Binary yes/no, form submission:** Checkbox
- **Numeric range:** Slider (with Input field for precise entry when needed)
- **Date/time:** Date picker dropdown (inline) or Date picker modal (mobile)
- **Long text:** Textarea input field
- **Rich text:** Text editor
- **File attachment:** File upload

### Grouping & Layout
- Group related fields with consistent spacing
- Place labels above inputs (not inline) for better scanning and mobile readability
- Align form elements to a consistent left edge
- Use Button group for 2-5 mutually exclusive view/filter toggles
- Place primary actions (submit) at the bottom-right of forms; destructive actions should require confirmation

### Accessibility
- Every form control must have a visible label (use the `Label` boolean — keep it on)
- Do not use color alone to convey state (error, success) — always include text or an icon
- Checkboxes and Radio groups must have a group label describing the question
- Toggles should describe what happens when on, not just the setting name (e.g. "Enable notifications" not just "Notifications")
- Ensure sufficient color contrast between input text, placeholder text, and backgrounds
- Support keyboard navigation: Tab to move between fields, Space/Enter to activate, Escape to close dropdowns
- Slider should always have a visible label and current value

### Responsive Design
- Use `Breakpoint=Mobile` variants for Radio group items, Date pickers, Calendars, and File upload on small screens
- On mobile, prefer full-width inputs and larger touch targets (Size=`lg` or `md`)
- Date picker modal is preferred over dropdown on mobile for better usability
