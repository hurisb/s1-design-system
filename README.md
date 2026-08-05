# S1 Design System — Claude Skill

A Claude Skill that teaches Claude the Saltbox One (S1) design system —
tokens and component groups — so anyone on the team can build or review
S1-branded work consistently, without needing to be a designer or developer.

## What's inside

```
s1-design-system/
├── README.md              <- you are here
└── skill/
    ├── SKILL.md             <- overview + entry point Claude reads first
    └── references/
        ├── tokens.md          <- color, spacing, radius, grid, type scale
        ├── typography.md      <- fonts, weights, usage rules
        ├── form-elements.md   <- inputs, buttons, selects, pickers, etc.
        ├── navigation.md      <- nav bars, tabs, breadcrumbs, tree views
        └── data-display.md    <- tables, cards, badges, charts, alerts
```

## How to use it

1. Clone or download this repo.
2. In Claude, add the `skill/` folder as a skill (via **Save skill** on the
   file card in a Claude conversation, or your org's skill install flow).
3. Ask Claude anything S1-related — "what's our primary button style?",
   "build me a settings form using S1 components," "does this screen follow
   our brand tokens?" — Claude pulls in the relevant section automatically.

## Who it's for

Everyone at Saltbox touching an S1-branded surface: designers, developers,
QA, PMs, architects, sales/demos, interns, and leadership doing reviews. No
code or design background required to ask Claude questions using this skill.

## Status

Foundations tokens (colors, spacing, radius) are documented in depth, with
real values pulled from the S1 2.0 Figma file. Component-level detail for
Form Elements, Navigation, and Data Display is indexed by name today —
deep per-component specs are a planned follow-up, along with the full grid
spec, background-color table, numeric type scale, and logo usage guidance.
See the `SKILL.md` "Status" section for the current list.

## Contributing

This skill is meant to stay in sync with the S1 Figma file
([S1 2.0](https://www.figma.com/design/wmlelbFhJ0FPS6DwpNXS2Z/S1-2.0)). When
a token or component changes in Figma:

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
