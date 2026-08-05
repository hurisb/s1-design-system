
# Data Display Component Library

This skill defines every component in the DATA DISPLAY group of the design system. Use these components — never recreate them from scratch — when building any data presentation, feedback, layout structure, or content display UI.

---

## Component Inventory

### 1. Table

**Component:** `Table` (StateGroupId:1227:110587)
**Page:** ↳ Tables

Data table with header row, sortable columns, and interactive cells.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Example | `Team members`, `Companies`, `Sales`, `Files` | `Team members` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |
| Dividers | `Divider line`, `Alternating fills` | `Divider line` |

**Sub-components:**

**Table header cell** (StateGroupId:1221:107933):

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md` | `sm` |
| Text | `False`, `True` | `True` |
| Checkbox | `False`, `True` | `True` |

**Table cell** (StateGroupId:1222:107305):

| Property | Options | Default |
|---|---|---|
| Type | `Text`, `Avatar`, `File type icon`, `Payment method`, `Badge`, `Badges multiple`, `Trend positive`, `Trend negative`, `Avatar group`, `Select dropdown`, `Progress bar`, `Star ratings`, `Action buttons`, `Action icons`, `Action dropdown icon` | `Text` |
| Size | `sm`, `md` | `sm` |
| State | `Default`, `Hover/selected` | `Default` |

**Boolean properties (cell):**
- `Lead action` (default: on) — checkbox/radio/toggle in the leading position
- `Supporting text` (default: on)
- `Lead text` (default: on)

**Table cell lead action** — `Checkbox`, `Radio`, or `Toggle`

**When to use:**
- Structured data: user lists, transactions, file management, CRM records
- `Divider line` — clean separator lines between rows (default, best for most cases)
- `Alternating fills` — zebra striping for dense tables with many columns
- Use `sm` size for data-dense tables; `md` for tables with fewer columns

---

### 2. Filters Bar

**Component:** `Filters bar` (StateGroupId:12232:376165)
**Page:** ↳ Filters

Horizontal filter controls above content areas.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Simple`, `Tabs and search`, `Tabs and date picker`, `Date filters`, `Dropdowns`, `Dropdowns and date picker`, `Advanced inactive filter`, `Advanced active filters` | `Simple` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**When to use:**
- `Simple` — basic search + filter button
- `Tabs and search` — category tabs with search
- `Dropdowns` — multiple dropdown filter controls
- `Advanced *` — complex filter builder with active filter chips

---

### 3. Filters Dropdown Menu

**Component:** `Filters dropdown menu` (StateGroupId:12232:366410)
**Page:** ↳ Filters

Individual filter dropdown trigger with active state.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| State | `Default`, `Hover`, `Focused`, `Open empty state`, `Open inactive filter`, `Open active filters`, `Active`, `Disabled` | `Default` |
| Orientation | `Right aligned`, `Left aligned` | `Right aligned` |

**Boolean properties:**
- `Dropdown chevron` (default: on)
- `Counter badge` (default: on) — shows count of active filters

---

### 4. Filters Slideout Menu

**Component:** `Filters slideout menu` (StateGroupId:12232:375462)
**Page:** ↳ Filters

Side panel for complex multi-filter management.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| State | `Empty state`, `Inactive filter`, `Active filters` | `Empty state` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

---

### 5. Avatar

**Component:** `Avatar` (StateGroupId:11008:45389)
**Page:** ↳ Avatars

User/entity avatar with status indicator.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `xs`, `sm`, `md`, `lg`, `xl`, `2xl` | `xs` |
| Border | `False`, `True` | `False` |
| Placeholder icon | `False`, `True` | `False` |
| Placeholder text | `False`, `True` | `False` |

**Boolean properties:**
- `Status icon` (default: on) — online/offline/verified indicator

**Sub-component: Status icon** — `Offline`, `Online`, `Avatar`, `Verified tick`, `Count`

**Related components:**
- **Avatar label group** — avatar + name + supporting text (sizes: `sm`, `md`, `lg`)
- **Avatar group** — stacked avatar row with "more users" count and "add" button (sizes: `xs`, `sm`, `md`)
- **Avatar profile photo** — large profile photo with verified badge and optional placeholder/text (sizes: `sm`, `md`, `lg`)

**When to use:**
- `xs`–`sm` — inline mentions, table cells, compact lists
- `md` — cards, comments, activity feeds
- `lg`–`2xl` — profile pages, user settings
- `Placeholder icon` — unknown user with generic person icon
- `Placeholder text` — user initials when no photo is available
- `Border=True` — when avatar overlaps other content or in avatar groups

---

### 6. Badge

**Component:** `Badge` (StateGroupId:1046:3819)
**Page:** ↳ Badges

Status indicator, label, or count badge.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md`, `lg` | `sm` |
| Type | `Pill color`, `Badge color`, `Badge modern` | `Pill color` |
| Icon | `False`, `Dot`, `Country`, `X close`, `Avatar`, `Icon trailing`, `Icon leading`, `Only` | `False` |
| Color | `Gray`, `Brand`, `Error`, `Warning`, `Success`, `Slate`, `Sky`, `Blue`, `Indigo`, `Purple`, `Pink`, `Orange` | `Gray` |

**Instance swaps:** `Flag swap`, `Icon trailing swap`, `Icon leading swap`

**Related: Badge group** — badge paired with a text label (Leading or Trailing position).

**When to use:**
- `Pill color` — rounded pill badges for status labels, categories, counts
- `Badge color` — square-cornered badges for more structured contexts
- `Badge modern` — minimal outlined badge style
- `Dot` — minimal status indicator (online, new, active)
- `X close` — removable/dismissible badges
- Color semantics: `Error` = critical/failure, `Warning` = caution, `Success` = positive/complete, `Brand` = branded/highlighted, `Gray` = neutral/default

---

### 7. Content Divider

**Component:** `Content divider` (StateGroupId:1252:126874)
**Page:** ↳ Content dividers

Visual separator between content sections.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Heading`, `Text`, `Button`, `Button group icon`, `Button group`, `Button icon` | `Heading` |
| Style | `Single line`, `Dual line`, `Background fill` | `Single line` |

**When to use:**
- `Heading` — section breaks with a title
- `Text` — centered text label divider (e.g. "or", "and")
- `Button` / `Button icon` — dividers with action buttons (e.g. "Load more", "Add section")
- `Button group` — dividers with multiple action options

---

### 8. Modal

**Component:** `Modal` (StateGroupId:4057:415205)
**Page:** ↳ Modals

Dialog overlay for focused tasks, confirmations, and forms.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Stacked left aligned`, `Horizontal`, `Warning stacked left aligned`, `Warning horizontal`, `Destructive stacked left aligned`, `Destructive horizontal`, `Log in`, `Sign up 01`, `Sign up 02`, `Checkboxes`, `Toggles`, `Link field`, `Dropdown`, `Input field`, `Labels`, `Access request`, `Email invite`, `User invite`, `Stacked with team`, `Stacked with team and link`, `Stacked with team and invites`, `Verification code`, `2FA code`, `Password prompt`, `Centered photo`, `Centered photo carousel`, `Centered video carousel`, `Payment details`, `Payment details with image`, `Plan 01`, `Plan 02`, `Payment method`, `Date picker`, `File upload`, `Profile settings`, `User selection`, `Image crop`, `Form 01`, `Form 02`, `Calendar event`, `Banner appearance`, `Appearance settings`, `A.I. assistant`, `User settings`, `New project`, `Text editor`, `Share project`, `Create event`, `Integration`, `New message (empty state)`, `New message (filled)` | `Stacked left aligned` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Sub-components:**
- **_Modal header** — Left aligned, Center aligned, or Horizontal left aligned; with optional X close, Featured icon, Divider
- **_Modal actions** — Horizontal/Vertical button layouts with optional Checkbox, Tertiary button, Destructive variant

**When to use:**
- `Stacked left aligned` / `Horizontal` — general confirmation/info dialogs
- `Warning *` — caution dialogs (yellow/warning icon)
- `Destructive *` — delete/remove confirmations (red destructive styling)
- Auth modals: `Log in`, `Sign up 01/02`, `Verification code`, `2FA code`, `Password prompt`
- Form modals: `Input field`, `Dropdown`, `Checkboxes`, `Toggles`, `Date picker`, `File upload`, `Text editor`
- User/team modals: `Email invite`, `User invite`, `User selection`, `Share project`, `Profile settings`, `User settings`
- Commerce modals: `Payment details`, `Payment method`, `Plan 01/02`
- Media modals: `Centered photo`, `Centered photo carousel`, `Centered video carousel`, `Image crop`

---

### 9. Empty State

**Component:** `Empty state` (StateGroupId:1182:317)
**Page:** ↳ Empty states

Placeholder content shown when a section has no data.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Icon | `Featured icon`, `Illustration`, `File type icon`, `Folder icon`, `Folder icon transparent`, `Users radius`, `Users row`, `Integrations` | `Featured icon` |
| Size | `sm`, `md`, `lg` | `sm` |

**Boolean properties:**
- `Featured icon` (default: on)

**Related: Illustration** — decorative illustrations (Cloud, Box, Documents, Credit card) in sm/md/lg sizes.

**When to use:**
- Empty tables, empty search results, first-time user states, no-data dashboards
- `sm` — inline empty states within cards or sidebars
- `md` — standard page-level empty states
- `lg` — full-page onboarding/first-run empty states
- Always include a clear CTA to help the user populate the empty area

---

### 10. Code Snippet

**Component:** `Code snippet` (StateGroupId:1234:243)
**Page:** ↳ Code snippets

Code block display with syntax highlighting area.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Horizontal`, `Vertical`, `Vertical with tabs` | `Horizontal` |

**Boolean properties:**
- `Mask content` (default: on) — gradient mask at bottom for overflow
- `Actions` (default: on) — action buttons below the code
- `Header copy button` (default: on) — copy-to-clipboard button

**When to use:**
- API documentation, developer guides, integration setup instructions, code examples
- `Horizontal` — side-by-side code with description
- `Vertical` — stacked code block
- `Vertical with tabs` — multi-language/multi-file code examples

---

### 11. Activity Feed

**Component:** `Activity feed` (StateGroupId:1254:128631)
**Page:** ↳ Activity feeds

Timeline of events or notifications.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Divider | `Divider`, `Connector`, `False`, `Line` | `Line` |
| Type | `Notifications`, `Messages` | `Notifications` |

**Sub-component: _Feed item base** — individual feed entry.

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md` | `sm` |
| Supporting item | `False`, `Labels`, `File`, `Text` | `False` |
| Connector | `True`, `False` | `True` |

**Boolean (item):** `New dot` (default: on) — unread indicator

**When to use:**
- Audit logs, notification history, comment threads, project activity
- `Notifications` — system events with icons and timestamps
- `Messages` — conversation-style feed with avatars
- `Connector` — visual line connecting sequential events (timeline style)

---

### 12. Alert

**Component:** `Alert` (StateGroupId:1130:81134)
**Page:** ↳ Alerts & notifications

Inline alert banner for contextual messages.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Color | `Default`, `Gray`, `Error`, `Warning`, `Success`, `Brand` | `Default` |
| Size | `Floating`, `Full-width` | `Floating` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Boolean properties:**
- `X close button` (default: on)
- `Actions` (default: on) — action buttons within the alert
- `Supporting text` (default: on)

**When to use:**
- `Error` — form validation errors, system errors, failed operations
- `Warning` — caution messages, deprecation notices, approaching limits
- `Success` — confirmation of completed actions, saved changes
- `Brand` — informational announcements, tips, feature highlights
- `Floating` — contained within a card/section
- `Full-width` — spanning the full page width (top banners)

---

### 13. Notification

**Component:** `Notification` (StateGroupId:1135:618)
**Page:** ↳ Alerts & notifications

Toast/snackbar notification popup.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Primary icon`, `Image`, `Avatar`, `Gray icon`, `Error icon`, `Warning icon`, `Success icon`, `No icon`, `Progress indicator` | `Primary icon` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Boolean properties:**
- `X close button` (default: on)
- `Actions` (default: on)
- `Supporting text` (default: on)

**When to use:**
- Transient feedback: saved, sent, deleted, error, upload progress
- `Progress indicator` — for ongoing operations (file uploads, processing)
- `Avatar` — social notifications (new message from user, team invite)
- `Image` — rich notifications with preview thumbnails
- Notifications should auto-dismiss after 5-8 seconds unless they contain actions

---

### 14. Card Header

**Component:** `Card header` (StateGroupId:1211:169)
**Page:** ↳ Card headers

Reusable header for card containers.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Avatar | `False`, `True` | `False` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Boolean properties:**
- `Actions` (default: on) — action buttons
- `Dropdown icon` (default: on)
- `Supporting text` (default: on)
- `Divider` (default: on) — bottom border
- `Badge` (default: on)

**When to use:**
- Top section of any card component: settings cards, data cards, profile cards
- `Avatar=True` — for user/entity cards

---

### 15. Charts

**Page:** ↳ Charts

#### Line and Bar Chart
**Component:** `Line and bar chart` (StateGroupId:1062:46989)

| Property | Options | Default |
|---|---|---|
| Legend | `False`, `Top`, `Right` | `False` |
| Axis labels | `False`, `True` | `False` |
| Chart style | `Line`, `Bar` | `Line` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

#### Pie Chart
**Component:** `Pie chart` (StateGroupId:1084:114)

| Property | Options | Default |
|---|---|---|
| Size | `xxs`, `xs`, `sm`, `md`, `lg` | `xxs` |
| Legend | `False`, `True` | `False` |

**Sub-component: _Pie chart** — `Hole`: `False`, `25%`, `50%`, `75%` (donut chart)

#### Activity Gauge
**Component:** `Activity gauge` (StateGroupId:1078:155)

| Property | Options | Default |
|---|---|---|
| Size | `xs`, `sm`, `md`, `lg` | `xs` |
| Legend | `False`, `Bottom`, `Right` | `False` |

#### Radar Chart
**Component:** `Radar chart` (StateGroupId:1084:7362)

| Property | Options | Default |
|---|---|---|
| Legend | `False`, `Right`, `Bottom` | `False` |

#### Chart Marker
**Component:** `Chart marker` (StateGroupId:8100:193259) — hover tooltip on charts (`Line`, `Dash`, `Minimal` types)

**When to use:**
- `Line` chart — trends over time (revenue, traffic, growth)
- `Bar` chart — comparisons across categories (monthly sales, team performance)
- `Pie` chart — proportion/distribution (market share, budget allocation). Use donut (Hole > 0) for a modern look.
- `Activity gauge` — ring-based progress/completion (fitness, goal tracking)
- `Radar` chart — multi-dimensional comparisons (skill assessments, product feature comparisons)

---

### 16. Command Bar

**Component:** `Command bar` (StateGroupId:3307:407570)
**Page:** ↳ Command menus

Keyboard-driven command palette (Cmd+K / Ctrl+K).

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Users`, `Actions`, `Users menu`, `Integrations menu`, `Command only`, `Empty state` | `Users` |
| Text | `Default`, `Stacked` | `Default` |

**When to use:**
- Power user quick-access: search users, trigger actions, navigate pages, launch integrations
- `Command only` — minimal search-only command palette
- `Actions` — command palette with action shortcuts
- `Stacked` text — two-line items with description

---

### 17. Inline CTA

**Component:** `Inline CTA` (StateGroupId:1255:131915)
**Page:** ↳ Inline CTAs

Inline call-to-action banner within content areas.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Image`, `Actions`, `Email field`, `Change plan`, `Upgrade plan`, `Payment method`, `Receipt` | `Image` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**When to use:**
- Upgrade prompts, newsletter signups, plan change CTAs, payment reminders
- Place inline within page content (between sections, within settings)

---

### 18. Video Player 16:9

**Component:** `Video player 16:9` (StateGroupId:9264:576771)
**Page:** ↳ Video players

Standard 16:9 video player with controls.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Size | `sm`, `md`, `lg` | `sm` |
| Playing | `False`, `True` | `False` |

**Boolean properties:**
- `Overlay action` (default: on) — centered play/pause overlay button
- `Actions bar` (default: on) — bottom control bar

**When to use:**
- Embedded video content, tutorials, media galleries, course content

---

### 19. Message

**Component:** `Message` (StateGroupId:1242:996)
**Page:** ↳ Messaging

Chat message bubble with multiple content types.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Message`, `Message reply`, `File`, `Audio`, `Image`, `Video`, `Link preview`, `Link minimal`, `Writing` | `Message` |
| Sent | `False`, `True` | `False` |
| Actions panel | `False`, `True` | `False` |

**Boolean properties:**
- `Reactions` (default: on)
- `Status icon` (default: on) — read/unread/failed indicator

**Related: Message action** — input area (`Minimal`, `Textarea input`, `Advanced`)

**When to use:**
- Chat/messaging interfaces, support conversations, team communication
- `Sent=True` — messages sent by the current user (right-aligned bubble)
- `Sent=False` — received messages (left-aligned with avatar)
- `Writing` — typing indicator
- `File`, `Audio`, `Image`, `Video` — rich media message types
- `Link preview` / `Link minimal` — URL sharing with preview cards

---

### 20. Loading Indicator

**Component:** `Loading indicator` (StateGroupId:1192:610)
**Page:** ↳ Loading indicators

Spinner/loading animation.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Style | `Dot circle`, `Line spinner`, `Line simple` | `Line simple` |
| Size | `sm`, `md`, `lg`, `xl` | `sm` |

**Boolean properties:**
- `Supporting text` (default: on) — "Loading..." text

**When to use:**
- Page loads, section refreshes, data fetching, lazy-loading content
- `sm` — inline loading (within buttons, table cells)
- `md`–`lg` — section-level loading
- `xl` — full-page loading

---

### 21. Metric Item

**Component:** `Metric item` (StateGroupId:1560:266217)
**Page:** ↳ Metrics

KPI/metric display card.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Actions | `False`, `True` | `False` |
| Type | `Simple`, `Icon 01`, `Icon 02`, `Icon 03`, `Icon 04`, `Chart 01`, `Chart 02`, `Chart 03`, `Chart 04` | `Simple` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Boolean properties:**
- `Dropdown icon` (default: on)
- `Featured icon` (default: on)

**Sub-components:**
- **_Chart mini** — sparkline/mini chart (12 chart shapes, Positive/Negative trend)
- **_Change** — trend indicator with arrow and percentage (3 styles, Positive/Negative)

**When to use:**
- Dashboard KPIs, analytics summaries, financial metrics, performance indicators
- `Simple` — metric with label, value, and change indicator
- `Chart *` — metric with embedded sparkline chart
- `Icon *` — metric with featured icon

---

### 22. Page Header

**Component:** `Page header` (StateGroupId:1239:122640)
**Page:** ↳ Page headers

Top-level page header with title, actions, and optional banner.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Style | `Simple`, `Avatar`, `Banner avatar`, `Banner simple`, `Banner avatar centered`, `Banner simple centered` | `Simple` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Boolean properties:**
- `Breadcrumbs` (default: on)
- `Supporting text` (default: on)
- `Actions` (default: on)
- `Search` (default: on)
- `Divider` (default: on)

**When to use:**
- `Simple` — standard page title with actions
- `Avatar` — profile/user page header
- `Banner *` — pages with hero/cover images (profile pages, project pages)
- `* centered` — centered layout for marketing-style pages

---

### 23. Section Header

**Component:** `Section header` (StateGroupId:1214:38)
**Page:** ↳ Section headers

Header for content sections within a page.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Tabs | `False`, `True` | `False` |
| Type | `Buttons`, `Search`, `Button group` | `Buttons` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Boolean properties:**
- `Dropdown icon` (default: on)
- `Supporting text` (default: on)
- `Actions` (default: on)
- `Divider` (default: on)

**Related: Section label** — compact section label with optional Required indicator, Supporting text, Help icon, and Actions.

**When to use:**
- Above tables, card grids, form sections, content blocks
- `Tabs=True` — section header with integrated tab navigation
- `Search` — section with filterable content
- `Button group` — section with segmented view controls

---

### 24. Section Footer

**Component:** `Section footer` (StateGroupId:3275:372571)
**Page:** ↳ Section footers

Footer for content sections and cards.

**Variant properties:**

| Property | Options | Default |
|---|---|---|
| Type | `Section`, `Card` | `Section` |
| Button group | `True`, `False` | `True` |
| Breakpoint | `Desktop`, `Mobile` | `Desktop` |

**Boolean properties:**
- `Secondary button` (default: on)
- `Actions` (default: on)
- `Divider` (default: on)

**When to use:**
- Below form sections (save/cancel), below card content, pagination areas
- `Card` — footer contained within a card border
- `Section` — full-width section footer

---

## UX, Accessibility & Heuristic Best Practices

### Data Tables
- Always include sortable column headers for key data columns
- Use `Checkbox` lead action for bulk-select operations
- Keep tables horizontally scrollable on mobile (`Breakpoint=Mobile`)
- Use `Alternating fills` dividers for tables with 5+ columns to improve scanability
- Right-align numeric data columns; left-align text columns
- Place action buttons/icons in the rightmost column

### Feedback Components
- **Alerts** are persistent — use for important information that should remain visible
- **Notifications** are transient — use for confirmatory feedback that can auto-dismiss
- Use semantic colors consistently: `Error` for failures, `Warning` for caution, `Success` for confirmation
- Never use only color to convey meaning — always include an icon and text
- Destructive modals must require explicit confirmation (never auto-proceed)

### Empty States
- Always include a descriptive message explaining why the area is empty
- Always include a primary CTA to help the user take the next step
- Use illustrations for first-time/onboarding empty states; use icons for transient empty states

### Layout Structure
- Use **Page header** at the top of every page for consistent page identity
- Use **Section header** to introduce each distinct content block within a page
- Use **Card header** as the top of any card container
- Use **Section footer** for actions that apply to the section above
- Use **Content dividers** sparingly — whitespace is often sufficient

### Charts
- Always include axis labels when data context is not obvious
- Include a legend when showing 2+ data series
- Use Line charts for time-series trends; Bar charts for category comparisons
- Pie/donut charts should have no more than 5-7 segments
- Use mini charts in Metric items for at-a-glance trends

### Modals
- Keep modals focused on a single task — avoid multi-step flows in modals (use pages instead)
- Always include a close button (X) and an Escape key handler
- Trap keyboard focus within the modal while open
- Return focus to the triggering element when the modal closes
- Use `Destructive *` modal types only for irreversible actions

### Avatars & Badges
- Use `Placeholder text` (initials) as the primary fallback when no photo is available
- Use `Placeholder icon` only when the user has no name to derive initials from
- Limit avatar groups to 4-5 visible avatars plus a "+N more" indicator
- Badge colors must be used consistently across the app (e.g. `Error` always means the same thing)

### Accessibility
- Tables: use proper `<table>`, `<thead>`, `<tbody>`, `<th>` semantics; sortable headers need `aria-sort`
- Modals: use `role="dialog"`, `aria-modal="true"`, `aria-labelledby` pointing to the header
- Alerts: use `role="alert"` for error/warning; `role="status"` for success/info
- Notifications: use `role="status"` with `aria-live="polite"` for non-urgent; `aria-live="assertive"` for errors
- Loading indicators: use `aria-busy="true"` on the loading region; announce completion
- Charts: provide text alternatives (data tables or `aria-label` summaries)
- Video players: require captions/subtitles support and keyboard-accessible controls
- Command bar: support full keyboard navigation (arrow keys, Enter, Escape)
- Empty states: ensure the CTA button is focusable and clearly labeled

### Responsive Design
- Use `Breakpoint=Mobile` variants for Tables, Modals, Alerts, Notifications, Inline CTAs, Page headers, Section headers, Section footers, Filters, Metric items, and Card headers
- Tables on mobile should either horizontally scroll or transform to a card/list layout
- Modals on mobile should be full-screen or bottom-sheet style
- Metric items should stack vertically on mobile
