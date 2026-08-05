---
name: s1-design-system
description: >
  The Saltbox One (S1) design system — brand tokens (color, spacing, radius,
  type scale) and component groups (Typography, Form elements, Navigation,
  Data display). Use this skill whenever building, reviewing, or specifying
  any UI for an S1 or Salesforce Commerce Cloud client project — pages,
  components, prototypes, PRDs, Figma files, or code. Also use when someone
  asks "what's our token for X", "what component should I use for Y", or
  wants a design reviewed for S1 brand consistency, even if they don't say
  "design system" explicitly.
---

# S1 Design System

This skill is the single source of truth for Saltbox's design tokens and
component groups. It keeps every project — client-facing storefronts, the
S1 app, internal tools, marketing surfaces — visually and structurally
consistent with the S1 brand.

## Who this is for

Anyone touching an S1-branded UI: designers, front-end/back-end devs, QA,
PMs, architects, sales (demos/decks), and leadership reviewing work. You
don't need a design or code background to use this — describe what you're
building or reviewing in plain language and Claude will pull in the right
tokens and components.

## How this skill is organized

One skill, five reference sections. Claude reads only the section(s)
relevant to the task at hand.

| Section | File | Covers |
|---|---|---|
| Tokens | `references/tokens.md` | Color (text/border/foreground/background), spacing, radius, grid, and type-scale values — the raw values everything else is built from |
| Typography | `references/typography.md` | Font family, weights, display vs. text styles, usage rules |
| Form elements | `references/form-elements.md` | Inputs, selects, checkboxes, buttons, date/color pickers, and more |
| Navigation | `references/navigation.md` | Nav bars, breadcrumbs, tabs, tree views, slideout menus |
| Data display | `references/data-display.md` | Tables, cards, badges, charts, alerts, empty states |

## How to use this skill

- **Designers/devs building something new:** describe what you're building;
  Claude pulls the relevant tokens and points to the matching S1 component
  instead of inventing a new pattern.
- **QA/reviewers:** ask Claude to check a screen or PR against S1 tokens and
  component conventions.
- **PMs/sales/leadership:** ask in plain language ("does this follow our
  brand?", "what's our error-state color?") — no code knowledge needed.

## Core principles

- **Token-first.** Never a raw hex, pixel spacing, or corner radius in
  product code — always the named token from `tokens.md`. This is what
  keeps light/dark mode and future rebrands from requiring a manual sweep.
- **Semantic over literal.** Reach for what a color/spacing *means*
  (`text-secondary`, `border-error`) not what it looks like
  (`neutral-700`, `red-500`) — the semantic name is stable across modes and
  brand refreshes; the raw scale name isn't.
- **Reuse before you build.** Every component group has a named S1
  equivalent (see the four reference files) — check there before building
  a one-off.
- **Light and dark mode are both first-class.** Every color token is
  documented with both values; don't ship a state that only works in one
  mode.

## Status

Foundations (Tokens: color, spacing, radius) are documented in depth.
Component-level detail for Form elements, Navigation, and Data display is
indexed by name — deep per-component specs (variants, states) are a
planned follow-up. Grid specs, the full background-color table, the
numeric type scale, and logo usage guidance are also follow-ups — see the
"Status" notes inside `tokens.md` and `typography.md`.

## Use cases

- **Building a new form screen:** check `form-elements.md` for the closest
  existing component, then `tokens.md` for field border/error colors and
  spacing.
- **Auditing a client storefront for brand drift:** compare colors against
  the semantic token tables in `tokens.md` rather than eyeballing hex
  values.
- **Onboarding a new team member:** point them at this skill's five
  sections instead of a scattered set of Figma links and Slack threads.
