
# Typography Styles Reference

This skill defines every type style in the design system. Always apply these styles rather than setting font properties manually. The entire system uses **Inter** as the sole typeface.

---

## Type Scale

The system has two tiers: **Display** styles for large headings and hero content, and **Text** styles for body copy, labels, and UI elements.

### Display Styles

Large-scale typographic styles for headings, hero sections, and marketing content. Display 2xl through Display md use **-2% letter spacing** for tighter optical fit at large sizes. Display sm and xs use **0 letter spacing**.

| Style name | Size | Line height | Letter spacing | Weights available |
|---|---|---|---|---|
| **Display 2xl** | 72px / 4.5rem | 90px / 5.625rem | -2% | Regular, Medium, Semibold, Bold |
| **Display xl** | 60px / 3.75rem | 72px / 4.5rem | -2% | Regular, Medium, Semibold, Bold |
| **Display lg** | 48px / 3rem | 60px / 3.75rem | -2% | Regular, Medium, Semibold, Bold |
| **Display md** | 36px / 2.25rem | 44px / 2.75rem | -2% | Regular, Medium, Semibold, Bold |
| **Display sm** | 30px / 1.875rem | 38px / 2.375rem | 0 | Regular, Medium, Semibold, Bold |
| **Display xs** | 24px / 1.5rem | 32px / 2rem | 0 | Regular, Medium, Semibold, Bold |

### Text Styles

Standard typographic styles for body text, labels, UI elements, and all non-heading content. All use **0 letter spacing**.

| Style name | Size | Line height | Letter spacing | Weights available |
|---|---|---|---|---|
| **Text xl** | 20px / 1.25rem | 30px / 1.875rem | 0 | Regular, Medium, Semibold, Bold |
| **Text lg** | 18px / 1.125rem | 28px / 1.75rem | 0 | Regular, Medium, Semibold, Bold |
| **Text md** | 16px / 1rem | 24px / 1.5rem | 0 | Regular, Medium, Semibold, Bold |
| **Text sm** | 14px / 0.875rem | 20px / 1.25rem | 0 | Regular, Medium, Semibold, Bold |
| **Text xs** | 12px / 0.75rem | 18px / 1.125rem | 0 | Regular, Medium, Semibold, Bold |

---

## Weight Definitions

Every size is available in four weights:

| Weight | Inter style | CSS weight | Purpose |
|---|---|---|---|
| **Regular** | Regular (400) | 400 | Body text, descriptions, paragraphs, supporting content |
| **Medium** | Medium (500) | 500 | Labels, input text, navigation items, subtle emphasis |
| **Semibold** | Semi Bold (600) | 600 | Section headings, card titles, button text, strong emphasis |
| **Bold** | Bold (700) | 700 | Page titles, hero headings, maximum emphasis |

---

## Style Naming Convention

Styles follow the pattern: `{tier} {size}/{weight}`

Examples:
- `Display 2xl/Regular`
- `Display md/Semibold`
- `Text sm/Medium`
- `Text xs/Bold`

This produces **44 total styles** (11 sizes × 4 weights — 6 Display + 5 Text).

> All sizes, line heights, weights, and letter-spacing on this page are the
> exact values from the S1 2.0 Figma file (verified against the type-scale
> variables). Font family is **Inter** for both Display and Text tiers.

---

## When to Use Each Size

### Display sizes — headings and hero content

| Size | When to use |
|---|---|
| **Display 2xl** (72px) | Hero headlines on marketing landing pages, splash screens. Use sparingly — one per page maximum. |
| **Display xl** (60px) | Major section headlines on marketing pages, large feature callouts. |
| **Display lg** (48px) | Page-level headings on marketing pages, large modal titles, pricing page headers. |
| **Display md** (36px) | Section headings on marketing pages, large card group headings. |
| **Display sm** (30px) | Page titles in application UI, section headings in content-heavy pages. |
| **Display xs** (24px) | Card titles, modal headings, sidebar section headings, settings page titles. |

### Text sizes — body and UI content

| Size | When to use |
|---|---|
| **Text xl** (20px) | Lead paragraphs, feature descriptions, large supporting text on marketing pages. |
| **Text lg** (18px) | Body text on marketing pages, large input field text, prominent descriptions. |
| **Text md** (16px) | **Default body text.** Paragraphs, form labels, navigation items, button text (md/lg buttons), descriptions. This is the base size for most UI content. |
| **Text sm** (14px) | **Default UI text.** Table cells, input field text, small button text, metadata, secondary labels, tooltips, badges, helper text. Most component text uses this size. |
| **Text xs** (12px) | Captions, footnotes, timestamps, badge counts, overline labels, legal text. Use only when space is limited. |

---

## When to Use Each Weight

### Regular (400)
- Body paragraphs and descriptions
- Supporting/secondary text
- Placeholder text in inputs
- Long-form content
- Table cell values

### Medium (500)
- Form labels and input values
- Navigation items (non-active)
- Table header labels
- Dropdown menu items
- Subtle emphasis within body text
- Breadcrumb items
- Tag text

### Semibold (600)
- Section headings and card titles
- Button labels
- Active navigation items
- Modal titles
- Alert titles
- Badge text
- Column header sort labels
- Strong emphasis within UI

### Bold (700)
- Page-level titles (Display sizes)
- Hero headlines
- Metric values and KPI numbers
- Maximum typographic emphasis
- Marketing headline variants

---

## Common Component Typography Mappings

| Component | Style |
|---|---|
| Page title | Display sm/Semibold or Display xs/Semibold |
| Section heading | Text lg/Semibold |
| Card title | Text lg/Semibold or Text md/Semibold |
| Modal title | Text lg/Semibold |
| Form label | Text sm/Medium |
| Input field text | Text md/Regular |
| Input placeholder | Text md/Regular |
| Hint / helper text | Text sm/Regular |
| Button text (sm) | Text sm/Semibold |
| Button text (md-xl) | Text md/Semibold |
| Table header | Text xs/Medium |
| Table cell | Text sm/Regular |
| Badge / tag | Text xs/Medium or Text sm/Medium |
| Tooltip | Text xs/Regular or Text sm/Regular |
| Navigation item | Text md/Medium or Text sm/Medium |
| Active nav item | Text md/Semibold or Text sm/Semibold |
| Breadcrumb | Text sm/Medium |
| Tab label | Text sm/Medium or Text md/Medium |
| Metric value | Display md/Semibold or Display sm/Semibold |
| Metric label | Text sm/Medium |
| Alert title | Text sm/Semibold |
| Alert body | Text sm/Regular |
| Footer text | Text md/Regular |

---

## Best Practices

### Hierarchy
- Establish a clear visual hierarchy: use no more than 3-4 distinct sizes per page
- Pair a Display size heading with Text size body content — never use two Display sizes at adjacent hierarchy levels
- Step down sizes consistently (don't skip more than 2 size steps in a row)

### Weight pairing
- Pair **Semibold/Bold headings** with **Regular body text** for clear contrast
- Use **Medium** for labels and interactive elements that need emphasis without the weight of Semibold
- Avoid pairing Regular headings with Medium body text — the hierarchy inverts

### Responsive scaling
- Marketing pages: scale Display sizes down 1-2 steps on mobile (e.g. Display lg → Display sm)
- Application UI: Text sizes generally stay the same across breakpoints
- Never go below Text xs (12px) — it is the minimum readable size

### Accessibility
- Body text should be at least Text md (16px) for comfortable reading
- Line heights are pre-set for readability — do not override them
- Maintain a minimum contrast ratio of 4.5:1 for Text sm and smaller; 3:1 for Display and Text xl/lg
- Use weight (Medium/Semibold/Bold) rather than italics or underlines for emphasis
- Do not use letterspacing tighter than -2% (already set on Display 2xl–md)
