# S1 Design System — Claude Skill

A Claude Skill that teaches Claude the Saltbox One (S1) design system —
tokens and component groups — so anyone on the team can build or review
S1-branded work consistently, without needing to be a designer or developer.

## What's inside

```
s1-design-system/
├── README.md              <- you are here
├── docs/
│   └── GETTING-STARTED.md  <- beginner guide: install + example prompts
└── skill/
    ├── SKILL.md             <- overview + entry point Claude reads first
    └── references/
        ├── tokens.md            <- raw values: color scales, spacing, radius, type, layout
        ├── color-variables.md   <- semantic colors w/ real light+dark hex
        ├── typography.md        <- fonts, weights, real size/line-height, usage
        ├── form-elements.md     <- inputs, buttons, selects, pickers, etc.
        ├── navigation.md        <- nav bars, tabs, breadcrumbs, tree views
        ├── data-display.md      <- tables, cards, badges, charts, alerts
        └── logo.md              <- S1 logo lockups, variants, usage
```

## How to use it

**New to Claude Skills or downloading from GitHub? Read the step-by-step
guide: [docs/GETTING-STARTED.md](docs/GETTING-STARTED.md).** It covers, in
plain language for any role, how to get the files, three ways to use them in
Claude (website/desktop, Claude Code, or no install at all), and a big list of
example prompts.

Quick version:

1. **Get the files** — Download ZIP from the green **`< > Code`** button (you
   need to be signed in and granted access, since this repo is private), or
   `git clone` it.
2. **Add it to Claude** — pick one:
   - **Claude.ai / desktop app:** zip the `skill/` folder and upload it under
     **Settings → Customize → Skills**.
   - **Claude Code:** copy the `skill/` folder to
     `~/.claude/skills/s1-design-system/`.
   - **No install:** attach `SKILL.md` + the `references/` files to a chat, or
     add them to a Claude **Project**.
3. **Just ask** — in plain language. Claude pulls in the right section
   automatically:
   - "What's our primary button style?"
   - "Build me a settings form using S1 components."
   - "Does this screen follow our brand tokens?" *(attach a screenshot)*

   More examples for designers, devs, QA, PMs, and leadership are in the
   [getting-started guide](docs/GETTING-STARTED.md#part-3--example-prompts-copypaste).

## Who it's for

Everyone at Saltbox touching an S1-branded surface: designers, developers,
QA, PMs, architects, sales/demos, interns, and leadership doing reviews. No
code or design background required to ask Claude questions using this skill.

## Status

Foundations are documented in depth with **real values from the S1 Brand
Guideline** (Figma + its `s1-ds.json` variables export): full primitive color
scales (all steps `25`–`950`), the complete semantic color set with light **and**
dark values, the extended utility palette, spacing, radius, and the numeric type
scale. Typography is a **two-font system** — Space Grotesk for headings, Inter
for body. Form Elements, Navigation, and Data Display carry **full variant
inventories** plus a **per-component "Tokens used" block**.

The responsive grid (breakpoints/columns/gutters) and the S1 logo (lockups,
light/dark variants, colors, usage) are documented too. Note: `brand-900`/
`brand-950` are intentionally purple (the navy ramp deepens to purple at its
darkest steps) — confirmed, not a template default. See the `SKILL.md`
"Status" section.

## Contributing

The skill stays in sync with two Figma files: **foundations** (colors, type,
spacing, radius, grid, logo) from the
[S1 Brand Guideline](https://www.figma.com/design/gSG4w3gVwXe5S3YWJsjzZX/S1-Brand-Guideline),
and **components** from the
[S1 2.0 component library](https://www.figma.com/design/wmlelbFhJ0FPS6DwpNXS2Z/S1-2.0).
When a token or component changes in Figma:

1. Update the relevant table in `skill/references/`.
2. Keep the "Status" notes accurate — mark something done once it's
   verified against Figma, not just drafted.
3. Commit with a message that names what changed (e.g. `tokens: add full
   background-color table`).

## Use cases

- **Building a new form screen:** check `form-elements.md` for the closest
  existing component, then `tokens.md` for field colors and spacing.
- **Auditing a client storefront for brand drift:** compare colors against
  the semantic token tables in `tokens.md` instead of eyeballing hex values.
- **Onboarding a new team member:** point them at this skill's five
  sections instead of a scattered set of Figma links and Slack threads.
