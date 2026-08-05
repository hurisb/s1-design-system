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
        └── data-display.md      <- tables, cards, badges, charts, alerts
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

Foundations are documented in depth with **real values pulled from the S1 2.0
Figma file**: primitive color scales (hex), the full semantic color set with
light **and** dark values, the extended utility/badge palette, spacing, radius,
and the numeric type scale. Form Elements, Navigation, and Data Display now
carry their **full variant inventories** (every component, its variants,
options, and usage), not just a name index.

Remaining follow-ups: a few brand/`25` color steps, the three dark `-950` alert
backgrounds, grid column/gutter spec, per-component token annotations, and logo
usage. See the `SKILL.md` "Status" section for the current list.

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
