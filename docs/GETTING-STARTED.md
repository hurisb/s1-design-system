# Getting Started — for everyone

This guide is for anyone who wants to use the S1 Design System skill and has
**never installed a Claude Skill or downloaded files from GitHub before.** No
code or design background needed. Pick the path that matches how you use
Claude.

- [What the S1 design system covers](#what-the-s1-design-system-covers)
- [Part 1 — Get the files from GitHub](#part-1--get-the-files-from-github)
- [Part 2 — Use it in Claude](#part-2--use-it-in-claude)
  - [A. Claude.ai (website) or the desktop app — as a Skill](#a-claudeai-website-or-the-desktop-app--as-a-skill)
  - [B. Claude Code (the terminal app) — as a Skill](#b-claude-code-the-terminal-app--as-a-skill)
  - [C. No install — the 2-minute options](#c-no-install--the-2-minute-options)
- [Part 3 — Example prompts (copy/paste)](#part-3--example-prompts-copypaste)
- [Part 4 — Troubleshooting](#part-4--troubleshooting)

> **Not sure which path?** If you use Claude in a web browser or the desktop
> app, use **2A** (or the no-install option **2C**). If you use Claude in a
> terminal (Claude Code), use **2B**. When in doubt, **2C** works for everyone
> and takes two minutes.

---

## What the S1 design system covers

A quick tour of the pieces the skill knows about. You can ask Claude about any
of these in plain language — you don't need to memorize the names below.

**Fonts — two typefaces**
- **Space Grotesk** — every heading and display/title.
- **Inter** — all body text, labels, and UI.
- Each comes in Regular / Medium / Semibold / Bold (plus italics), on one size
  scale from 12px (fine print) up to 72px (hero headlines).

**Colors — a light + dark semantic system**
- You use names that describe *meaning* (`text-primary`, `bg-brand-solid`,
  `border-error`) instead of raw hex codes, and every color has a **light and a
  dark** value baked in.
- Covered: text, borders, icons, and backgrounds; the **S1 brand navy**; status
  colors (**error / warning / success**); and an extended palette for
  badges, tags, and charts.

**Spacing & layout**
- A consistent spacing scale (2, 4, 6, 8, 12, 16, 20, 24 … px) for padding and
  gaps, a corner-radius scale (2–24px, plus fully round), and a responsive grid
  (12 columns on desktop, 6 on tablet, 4 on mobile).

**Form elements**
- Inputs, text areas, selects and multi-selects, checkboxes, radios, toggles,
  sliders, date and color pickers, file upload, buttons and button groups,
  tooltips — each with its variants and states (default, hover, focus, error…).

**Navigation**
- Buttons, tabs, breadcrumbs, sidebars, top bars, pagination, tree views,
  progress steps, dropdown and context menus, tags, and slide-out panels.

**Data display**
- Tables, cards, badges, avatars, charts, alerts, notifications, modals, empty
  states, metrics/KPIs, activity feeds, and page/section headers.

**Logo**
- The S1 "Saltbox One" logo — the standalone mark and the full lockup, in light
  and dark, with usage do's and don'ts.

Each of these lives in a file under `skill/references/` (colors in
`color-variables.md` + `tokens.md`, fonts in `typography.md`, and one file each
for form elements, navigation, data display, and the logo). Claude opens
whichever one your question needs.

---

## Part 1 — Get the files from GitHub

This repo is **private**, so you first need access, then you download it.

### Step 1: Make sure you have access

1. You need a free GitHub account. If you don't have one, sign up at
   [github.com/join](https://github.com/join).
2. Ask the repo owner (Huri) to add you as a collaborator. They do this in
   **Settings → Collaborators → Add people**, using your GitHub username.
3. You'll get an email invite — click **Accept**. Until you do, the repo link
   will show a "404 / not found" page even though it exists.

### Step 2: Download the files (no coding)

1. Open the repo while signed in:
   **https://github.com/hurisb/s1-design-system**
2. Click the green **`< > Code`** button near the top right.
3. Click **Download ZIP**.
4. Find the `.zip` in your Downloads folder and **double-click to unzip it**.

You now have a folder called `s1-design-system` containing a `README.md` and a
`skill/` folder. That `skill/` folder is the thing Claude needs.

### (Optional) For developers: clone instead

```bash
git clone https://github.com/hurisb/s1-design-system.git
```

---

## Part 2 — Use it in Claude

You only need to do **one** of these. Skills work by giving Claude the S1
knowledge automatically — once it's installed, you just ask questions in plain
language and Claude pulls in the right section.

### A. Claude.ai (website) or the desktop app — as a Skill

Best if you want it available in **every** chat without re-uploading. Available
on Free and paid plans; you may need **code execution** turned on (Settings →
Capabilities).

1. **Make a zip of the `skill` folder specifically** (not the whole repo):
   - **Mac:** open the unzipped `s1-design-system` folder, right-click the
     `skill` folder → **Compress "skill"**. You'll get `skill.zip`.
   - **Windows:** right-click the `skill` folder → **Send to → Compressed
     (zipped) folder**.
   - The zip must contain the `skill` folder with `SKILL.md` **inside** it —
     that's already how it's laid out, so just zip the `skill` folder as-is.
2. In Claude, open **Settings → Customize → Skills** (wording may be slightly
   different in your version — look for a **Skills** section).
3. Click **Upload skill** (or the **+**) and choose your `skill.zip`.
4. It appears under your **Personal** skills with a toggle — make sure it's
   **on**.
5. Start any chat and ask an S1 question (see [Part 3](#part-3--example-prompts-copypaste)).
   Claude uses the skill automatically when your question is design-related.

> Official steps, in case the menus moved:
> [Use Skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
> and [How to create custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills).

### B. Claude Code (the terminal app) — as a Skill

Best if you work in a terminal. A Skill here is just a folder with a `SKILL.md`
inside it.

1. Copy the `skill` folder from the repo into your Claude Code skills folder,
   renaming it to the skill's name:

   **Install for yourself (all your projects):**
   ```bash
   mkdir -p ~/.claude/skills
   cp -R skill ~/.claude/skills/s1-design-system
   ```

   **Or install for one project only** (run from that project's folder):
   ```bash
   mkdir -p .claude/skills
   cp -R /path/to/s1-design-system/skill .claude/skills/s1-design-system
   ```

   After copying you should have `SKILL.md` at
   `~/.claude/skills/s1-design-system/SKILL.md` with a `references/` folder next
   to it.

2. That's it — Claude Code discovers skills automatically (no restart). Claude
   decides to use it based on the `description` in `SKILL.md`, so just ask an
   S1 question and it pulls the skill in. You can also confirm it's installed by
   listing your skills.

> Reference: [Claude Code — Skills](https://code.claude.com/docs/en/skills).

### C. No install — the 2-minute options

Perfect if you don't want to set anything up, or you're helping someone
non-technical. Nothing to configure.

**Option 1 — Attach the files to a chat (fastest):**

1. Start a new chat in Claude.
2. Click the **attach / paperclip (+)** button in the message box.
3. Attach `SKILL.md` **and** the files inside `skill/references/` (at minimum
   `tokens.md` and `color-variables.md` for colors), then ask your question.
   - Trade-off: you re-attach them each new chat.

**Option 2 — Claude Projects (reusable knowledge, no coding):**

1. In Claude.ai, open **Projects** in the left sidebar → **+ New project**.
2. Name it something like "S1 Design System".
3. Use **Add content / Upload files** and add `SKILL.md` plus everything in
   `skill/references/`.
4. Every chat *inside that project* can now reference the S1 files. Great for a
   team space where designers, PMs, and QA all ask questions in one place.
   - Note: Projects treat these as reference documents (not an auto-triggered
     Skill), so it helps to say "using the S1 files, ..." in your first message.

> Reference: [What are Projects?](https://support.claude.com/en/articles/9517075-what-are-projects)

---

## Part 3 — Example prompts (copy/paste)

Once the skill is active (any path above), talk to Claude in plain language.
You don't need to name files or tokens — Claude finds them. Examples by role:

### Designers & developers — building something

- "Using the S1 design system, what's our primary button style — colors,
  radius, and padding?"
- "What fonts does S1 use for headings vs body, and at what sizes/weights?"
- "Build a settings form using S1 form elements. Include labels, an email
  input, a dropdown, and a save button, and use S1 spacing and border tokens."
- "What S1 component should I use for a list of orders with status badges?"
- "Give me the light and dark mode values for our text and border colors."
- "I need an error state for a text field. Which S1 token is the error border
  color, and what does the helper text look like?"

### QA & reviewers — checking work

- "Here's a screenshot of a client storefront. Does it follow S1 brand tokens?
  Call out anything using a raw hex or spacing that isn't in the system."
  *(attach the screenshot)*
- "Review this React component against the S1 design system and list any
  hard-coded colors, spacing, or radii that should be tokens instead."
  *(paste the code)*
- "Which S1 semantic token should replace `#D92D20` in this button?"

### PMs, sales & leadership — plain-language questions

- "In simple terms, what colors and fonts define the S1 brand?"
- "Does this landing page mockup look on-brand for S1? What's off?"
  *(attach the image)*
- "Write a short paragraph for a client deck explaining that our product uses a
  consistent design system with light and dark mode."
- "What's our error-state color, and where is it used?"

### Onboarding a new team member

- "Explain the S1 design system to me like I'm new here — what are the main
  parts and when would I use each?"
- "What's the difference between a semantic token like `text-secondary` and a
  raw one like `gray-700`, and why does S1 prefer the semantic one?"

> Tip: if an answer seems generic, add "using the S1 design system skill" to
> your prompt, or (in Projects/no-install mode) start with "using the S1 files
> I gave you, ...".

---

## Part 4 — Troubleshooting

**The GitHub link shows "404 / not found."**
You're not signed in, or you haven't been granted access yet. Sign in to GitHub
and accept the collaborator invite (see [Part 1, Step 1](#step-1-make-sure-you-have-access)).

**I don't see a "Skills" option in Claude's settings.**
Skills are relatively new — update your app to the latest version. If it's still
missing, use the no-install path ([2C](#c-no-install--the-2-minute-options)) —
it works on every version.

**The upload was rejected because the description is too long.**
Some versions of the Skills uploader cap the `description` field (around 200
characters). Open `skill/SKILL.md`, shorten the text after `description:` to a
sentence or two, save, re-zip the `skill` folder, and upload again. This only
affects the web/desktop Skill upload — it doesn't matter for Claude Code or the
no-install options.

**Claude gives an answer but ignores the skill.**
Say "using the S1 design system" (or "using the S1 files I attached") in your
message. Skills are triggered by the topic of your question, so being explicit
helps.

**I want the whole team to have it.**
On a Team or Enterprise plan an admin can share a Skill org-wide. Otherwise, the
simplest shared setup is one **Project** ([2C, Option 2](#c-no-install--the-2-minute-options))
that everyone opens, or just point people at this guide.
