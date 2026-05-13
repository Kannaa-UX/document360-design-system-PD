# Document360 — Miura Design System (DDS)
> Single source of truth for all Claude Design screen creation.
> Every designer on the team uses this file. Every screen must match it exactly.

---

## 1. Product Context

| Field | Value |
|---|---|
| Product | Document360 — Knowledge Base SaaS |
| Design System | Miura Design System (DDS) |
| Figma File | https://www.figma.com/design/uQ4D6PHaSJaavvN1nEmeWx/Miura-Design-System |
| FA Pro Kit | `78b5873547` (Font Awesome Pro 6.7.2) |
| FA Kit URL | https://kit.fontawesome.com/78b5873547.js |
| Tone | Professional, clean, trustworthy, minimal |

---

## 2. Color Tokens (Live from DDS Figma)

### Surface
| Token | Hex | Usage |
|---|---|---|
| Surface/White | `#ffffff` | Content area background, cards |
| Surface/Neutral-50 | `#fafafa` | Sub-nav panel background |
| Surface/Neutral-100 | `#f4f4f5` | Icon sidebar background, hover state |
| Surface/Neutral-200 | `#e4e4e7` | Section headers, active icon bg |
| Surface/Neutral-900 | `#18181b` | Topbar, icon sidebar (dark) |

### Primary / Accent
| Token | Hex | Usage |
|---|---|---|
| Primary/500 | `#7f56d9` | Active icon bg-light, Create button, purple accent |
| Primary/100 | `#ede9fe` | Active icon button background |
| Primary/700 | `#5b21b6` | Active nav item text |
| Active nav bg | `#e5ddf7` | Nav item active state background |

### Text
| Token | Hex | Usage |
|---|---|---|
| color.text.base | `#18181b` | Primary text, nav item labels |
| Text/Secondary | `#70707a` | Muted text, collapsed section headers |
| Text/Secondary (Grey BG) | `#51525c` | Expanded section header text |
| Text/Placeholder | `#d1d1d6` | Search placeholder, inactive text |
| Text/White | `#ffffff` | Text on dark backgrounds |
| Text/Yellow Heavy | `#451a03` | Trial badge text |

### Icon
| Token | Hex | Usage |
|---|---|---|
| Icon/Base | `#3e3e46` | All nav item icons (default) |
| Icon/Secondary | `#70707a` | Muted icons, topbar icons |
| Icon/Secondary (Grey BG) | `#51525c` | Icons on grey surfaces |
| Icon active | `#7f56d9` | Icon when sidebar item is active |

### Border
| Token | Hex | Usage |
|---|---|---|
| Border/Neutral-200 | `#e4e4e7` | Light separators |
| Border/Neutral-300 | `#d1d1d6` | Sub-nav border, search borders |
| Border/Dark | `#3e3e46` | Topbar border, dark sidebar border |
| Border/Yellow Light | `#ffc400` | Trial badge border, BETA badge border |
| Border/Red | `#de350b` | Error states |

### Status / Special
| Token | Hex | Usage |
|---|---|---|
| Pink/500 | `#ec4899` | Eddy AI sparkles icon, AI settings icon |
| Pink/100 | `#fce7f3` | Eddy AI icon button background |
| Surface/Yellow 100 | `#fffae6` | BETA badge background |
| Surface/Red 600 | `#de350b` | Notification badge, error badge |
| Teal | `#2dd4bf` | Warning/alert icon in topbar |
| Yellow | `#ffc400` | Trial badge background |

### Dark Mode Overrides
| Element | Dark Hex |
|---|---|
| Surface / sub-nav | `#1c1c21` |
| Content area | `#18181b` |
| Surface neutral | `#26272b` |
| Border | `#3e3e46` |
| Text base | `#f4f4f5` |
| Text secondary | `#a1a1aa` |
| Nav active bg | `#3b2d6e` |
| Nav active text | `#c4b5fd` |
| Icon active | `#a78bfa` |

---

## 3. Typography (DDS Inter Scale)

| Style Token | Family | Weight | Size | Line Height | Letter Spacing | Usage |
|---|---|---|---|---|---|---|
| Small/Regular | Inter | 400 | 13px | 20px | 0 | Nav item labels, body text |
| Tiny/Uppercase | Inter | 600 | 12px | 18px | 1px (0.08em) | Section headers (uppercase) |
| — | Inter | 500 | 13px | 20px | 0 | Active nav items |
| — | Inter | 600 | 12px | — | — | Topbar buttons |
| — | Inter | 700 | 10px | — | 0.1px | Badges, tags |

**Rules:**
- Font family: `Inter` always — load from Google Fonts
- Never use system fonts
- Section headers: always uppercase + letter-spacing `0.08em`
- Nav items: 13px regular, 13px medium when active

---

## 4. Spacing & Sizing (DDS Tokens)

| Token | Value | Usage |
|---|---|---|
| Spacing/2 | `8px` | Default gap, padding inside buttons |
| Spacing/3 | `12px` | Panel padding, nav item padding |
| Corner radius/4px | `4px` | Nav items, section headers, small buttons |
| Corner radius/8px | `8px` | Search bars, dropdowns, menus, modal cards |
| Corner radius/12px | `12px` | Large cards, panels |

---

## 5. Shadows

| Token | Value |
|---|---|
| Shadow/lg | `0 4px 6px -2px rgba(16,24,40,0.03), 0 12px 16px -4px rgba(16,24,40,0.08)` |
| Sidebar inset | `inset -3px 0 4px 0 rgba(0,0,0,0.06)` |
| Hover menu | `0 4px 16px rgba(0,0,0,0.12)` |

---

## 6. Icons (Font Awesome Pro 6.7.2)

### Rules
- **Default weight:** `fa-light` (weight 300) — all nav items, sidebar menus
- **Active state:** `fa-solid` (weight 900) — icon when sidebar item is active
- **Topbar:** `fa-regular` (weight 400) — bell, help, magnifying glass
- **Carets:** `fa-solid` always — `fa-caret-up`, `fa-caret-down`
- **Sparkles:** `fa-solid fa-sparkles` + `color: #ec4899` — AI settings and Eddy AI

### FA Pro Kit
Always load using the kit script (online) or the embedded woff2 fonts (offline):
```html
<script src="https://kit.fontawesome.com/78b5873547.js" crossorigin="anonymous"></script>
```

### Icon Map (Sidebar)
| Module | FA Icon | Behavior |
|---|---|---|
| Home | `fa-house` | Fly-out menu |
| Documentation | `fa-book-open` | Tooltip only |
| Eddy AI | `fa-book-open` + `fa-sparkles` overlay | Tooltip only, pink bg |
| Connections | `fa-diagram-project` | Fly-out menu |
| API | `fa-brackets-curly` | Tooltip only |
| Feedback | `fa-message-lines` | Fly-out menu |
| Analytics | `fa-chart-line-up` | Tooltip only |
| Content Tools | `fa-grid-2-plus` | Fly-out menu |
| Storage | `fa-hard-drive` | Tooltip only |
| KB Settings | `fa-book-open` + `fa-gear` badge | Tooltip only |
| Settings | `fa-gear` | Fly-out menu |

---

## 7. Templates

Four base templates exist. **Every design starts from one of these.**
Template files are in `/templates/` folder of this repository.

| Template | File | Active Icon | Secondary Panel | Use For |
|---|---|---|---|---|
| Settings | `d360-settings-template.html` | ⚙️ Gear | Settings accordion nav | All settings screens |
| Home | `d360-home-template.html` | 🏠 House | None | Dashboard, overview screens |
| Documentation | `d360-documentation-template.html` | 📖 Book Open | Category tree | Article editing, category management |
| AI Chatbot | `d360-ai-chatbot-template.html` | ✨ Eddy AI | None | AI chat, AI settings screens |

### CRITICAL Template Rules
```
✅ ONLY design inside: <main class="content" id="content">
✅ NEVER modify: topbar, icon sidebar, subnav panel
✅ NEVER change: active icon states (pre-set per template)
✅ ALWAYS match: DDS color tokens in this file
✅ ALWAYS use: fa-light icons for content area icons
✅ ALWAYS use: Inter font
```

---

## 8. Layout Structure

Every template follows this exact structure:

```
┌──────────────────────────────────────────────────────────┐
│  TOPBAR (40px, bg: #18181b)                              │
│  Logo | Project▾ | | Workspace▾ | Create▾ | Search       │
│                           Trial Badge | Alert | Open Site │
│                           | Notifications | Help | Avatar  │
├────┬──────────────┬───────────────────────────────────────┤
│    │              │                                        │
│ 48 │   260px      │          CONTENT AREA                 │
│ px │  Sub-nav     │    (Design goes here ONLY)            │
│    │  (settings/  │                                        │
│ I  │  doc only)   │    bg: #ffffff (light)                │
│ C  │              │    bg: #18181b (dark)                  │
│ O  │              │                                        │
│ N  │              │                                        │
│    │              │                                        │
│ S  │              │                                        │
│ I  │              │                                        │
│ D  │              │                                        │
│ E  │              │                                        │
│ B  │              │                                        │
│ A  │              │                                        │
│ R  │              │                                        │
└────┴──────────────┴───────────────────────────────────────┘
```

### Topbar Variants
Four topbar variants, selectable via avatar dropdown in the template:

| Variant | Contents | Use When |
|---|---|---|
| Documentation | Logo + Project + Workspace + Create + Search | Most screens |
| Home | Logo + Project + Workspace + Search (no Create) | Home/dashboard |
| Project only | Logo + Project + Search | Project-scoped screens |
| Plain | Logo only | Minimal / onboarding screens |

---

## 9. Topbar Component Details

### Left side
- **Logo:** D360 SVG (purple gradient), 24×24px
- **Project Name button:** Inter 12px semibold, white, `fa-caret-down`
- **Divider:** 1px vertical, gradient `transparent → #70707a → transparent`
- **Workspace Name:** with flag emoji circle + `fa-caret-down`
- **Create button:** bg `#7f56d9`, white, 12px semibold, `fa-caret-down`
- **Search bar:** bg `#3e3e46`, placeholder `#70707a`, `fa-regular fa-magnifying-glass`

### Right side
- **Trial badge:** bg `#ffc400`, text `#451a03`, 10px bold uppercase
- **Warning icon:** `fa-solid fa-triangle-exclamation`, color `#2dd4bf`
- **Open Site:** text button, `fa-solid fa-arrow-up-right-from-square`
- **Notifications:** `fa-regular fa-bell` with red badge `#ff5630`
- **Help:** `fa-regular fa-circle-question` + "HELP" text
- **Avatar:** 26×26px circle, gradient `#7f56d9 → #ec4899`, initials

### Avatar Dropdown
Contains: My Profile, Account Settings, Dark mode toggle, Topbar variant selector, Sign out

---

## 10. Icon Sidebar Details (48px wide)

### Item anatomy
- Container: 48×48px
- Button: 28×28px, `border-radius: 4px`
- Icon: 20×20px, 16px font-size

### States
| State | Button bg | Icon color |
|---|---|---|
| Default | transparent | `#3e3e46` |
| Hover | `#e4e4e7` | `#18181b` |
| Active | `#ede9fe` | `#7f56d9` |
| Active icon style | — | `fa-solid` |

### Eddy AI special item
- Button bg: `#fce7f3` (Pink/100)
- Main icon: `fa-regular fa-book-open`, color `#3e3e46`
- Overlay: `fa-solid fa-sparkles`, 8px, color `#f65f87`, top-right
- Never changes to fa-solid on active

### Fly-out menus (5 icons only)
Appear on hover, positioned `left: 48px`, aligned to icon top:

| Menu | Title | Items |
|---|---|---|
| Home | HOME | Overview, Tasks (badge:2), Recent, Starred, Archive, Recycle bin |
| Connections | CONNECTIONS | Knowledge base widget, Integrations, Extensions |
| Feedback | FEEDBACK MANAGER | Articles, Eddy AI |
| Content Tools | CONTENT RESOURCES / CONTENT MANAGEMENT / IMPORT & EXPORT | 12 items, 3 sections |
| Settings | SETTINGS | Knowledge base portal, Knowledge base site, Users & permissions, AI settings |

Menu style:
- bg: `#ffffff`, border: `1px solid #d1d1d6`, `border-radius: 8px`
- Shadow: `0 4px 16px rgba(0,0,0,0.12)`
- Width: 220px, padding: 12px
- Title: 11px semibold, color `#a0a0aa`, uppercase, `letter-spacing: 0.08em`
- Item: 13px regular, color `#18181b`, padding `8px`, `border-radius: 4px`
- Item hover: bg `#f4f4f5`

---

## 11. Sub-nav Panel (Settings template — 260px wide)

### Structure
- bg: `#fafafa`, border-right: `1px solid #d1d1d6`
- Padding: 12px, gap between groups: 8px
- Search bar: white bg, `border-radius: 8px`, `fa-regular fa-magnifying-glass`

### Section headers
| State | bg | text color | font |
|---|---|---|---|
| Expanded (open) | `#e4e4e7` | `#51525c` | 12px semibold uppercase |
| Collapsed | transparent | `#70707a` | 12px semibold uppercase |

Accordion: active section expands, all others collapse.

### Nav items
- Height: auto, padding: `8px 12px`
- Icon: 14×14px, `fa-light`, color `#3e3e46`
- Label: 13px regular, color `#18181b`
- Hover: bg `#f4f4f5`
- Active: bg `#e5ddf7`, font-weight 500

### Section list (Settings template)
1. Knowledge Base Portal → General, Workspace & localization, Workflow designer, Notifications, Backup & restore, Migrate content, API tokens, Team auditing, Billing
2. Knowledge Base Site → General, Site customization, Custom domain, Article settings & SEO, Article redirect rules, Smart bars, Read receipt, Ticket deflector, IP restriction, Cookie consent
3. Users & Permissions → Users & groups, Roles & permissions, Content access, Readers & groups, Reader access, SSO configuration, JWT
4. AI Settings → Eddy AI settings, Customize Eddy AI, Style guide, Manage sources, Suggested questions
5. Integrations & Extensions → All integrations, Extensions, Webhooks

---

## 12. Documentation Panel (Documentation template — 280px wide)

### Toolbar (44px)
Left icons: `fa-regular fa-list`, `fa-regular fa-clock`, `fa-regular fa-star`
Right: 1px separator + `fa-regular fa-bars` (active, bg `#e4e4e7`)
Button size: 28×28px, `border-radius: 8px`

### Tree structure
- Row height: 32px
- L0 indent: 12px, L1: 30px, L2: 56px, L3: 74px
- Tree lines: 1px solid `#d1d1d6` (vertical + horizontal elbow)
- Toggle: `fa-solid fa-angle-down` (expanded) / `fa-solid fa-angle-right` (collapsed)
- Folder icon: `fa-light fa-folder-closed`, color `#3e3e46`
- Article icon: `fa-solid fa-memo-pad`
  - Published: `#22c55e` (green)
  - Draft: `#ffab00` (yellow)
- Label: 13px regular, `#18181b`
- Active row: bg `#e5ddf7`
- Hover row: bg `#f4f4f5`
- MAIN badge: bg `#dcfce7`, border `#4ade80`, text `#166534`, 10px bold
- Actions (lock + ellipsis): visible on hover/active rows

---

## 13. Content Area Design Rules

This is where ALL screen designs go.

### Do:
- Match DDS components exactly from Figma reference
- Use the color tokens defined in section 2
- Use Inter font throughout
- Use `fa-light` icons at 14–16px for content icons
- Use `border-radius: 8px` for cards and inputs
- Use `border-radius: 4px` for small elements (tags, badges)
- Support both light and dark mode using CSS variables
- Keep padding consistent: `24px` outer, `16px` inner sections

### Don't:
- Use hardcoded pixel colors not in the DDS token list
- Use any font other than Inter
- Add `position: fixed` elements that overlap the sidebar
- Redesign the topbar, sidebar, or subnav
- Use Font Awesome Free icons — only FA Pro

### Common DDS Components to reference in Figma:
- Buttons: Primary, Secondary, Destructive, Ghost
- Inputs: Text field, Search, Textarea
- Badges / Tags: Status, Count, Label
- Cards: Default, Bordered, Elevated
- Tables: Default row, Header, Striped
- Toggles / Switches
- Modals / Dialogs
- Breadcrumbs
- Empty states
- Toast notifications

---

## 14. Standard Design Brief (Team Prompt Template)

Copy and use this every time you start a new design:

```
TEMPLATE: [Settings / Home / Documentation / AI Chatbot]

SCREEN NAME: [e.g. Suggested Questions]

ACTIVE NAV ITEM: [e.g. AI Settings → Suggested Questions]

FIGMA NODE: [URL with node-id]
or
SCREENSHOT: [attached]

SCREEN PURPOSE:
[1–2 sentences describing what this screen does]

SPECIFIC REQUIREMENTS:
- [e.g. include empty state]
- [e.g. use DDS Toggle component for enable/disable]
- [e.g. show loading skeleton]

DDS REFERENCE: https://www.figma.com/design/uQ4D6PHaSJaavvN1nEmeWx/Miura-Design-System
FA PRO KIT: 78b5873547

INSTRUCTIONS FOR CLAUDE:
1. Read the template file for the chosen template above
2. Design ONLY inside <main class="content" id="content">
3. Never modify topbar, sidebar, or subnav
4. Match DDS components from the Figma reference
5. Use fa-light icons in content area
6. Support light and dark mode
7. Output the complete modified HTML file
8. Name the file: d360-[template]-[module]-[screenname]-v1.html
```

---

## 15. File Naming Convention

```
d360-[template]-[module]-[screenname]-v[n].html

Examples:
d360-settings-aisettings-suggestedquestions-v1.html
d360-settings-aisettings-suggestedquestions-v2.html  ← after revisions
d360-settings-users-rolesandpermissions-v1.html
d360-documentation-articles-editor-v1.html
d360-home-overview-dashboard-v1.html
d360-aichatbot-conversation-v1.html
```

---

## 16. Review & Handoff Process

```
1. DESIGN     Designer creates screen in Claude using this DESIGN.md
              → Downloads HTML file with correct naming convention
              → Stores in /designs/in-review/ folder

2. REVIEW     Share HTML file URL or attach to review tool
              Director/CEO opens in browser — fully interactive
              Feedback given as written notes

3. REVISE     Designer opens original conversation in Claude
              Pastes feedback: "Update v1: change X, fix Y"
              Downloads v2 with updated filename

4. APPROVE    Approved file moved to /designs/approved/ folder

5. HANDOFF    PATH A → Designer uses approved HTML as Figma reference
                        Recreates in Figma using DDS components
              PATH B → Developer uses Claude Code
                        Attaches approved HTML + this DESIGN.md
                        Prompt: "Convert this design to Angular using
                        the DDS component library. Match exactly."

6. DEV        Developer has: approved HTML + DDS Figma + DESIGN.md
              All three together = unambiguous implementation spec
```

---

## 17. Repository Structure

```
document360-design-system/
│
├── DESIGN.md                          ← This file (single source of truth)
│
├── templates/
│   ├── d360-settings-template.html
│   ├── d360-home-template.html
│   ├── d360-documentation-template.html
│   └── d360-ai-chatbot-template.html
│
├── designs/
│   ├── in-review/                     ← Screens awaiting director review
│   ├── approved/                      ← CEO-approved screens
│   └── archive/                       ← Old versions
│
├── skills/
│   └── d360-design/
│       └── SKILL.md                   ← Claude skill file (optional)
│
└── README.md                          ← Onboarding guide for new designers
```

---

## 18. Quick Reference Card

```
┌─────────────────────────────────────────────┐
│  D360 DESIGN QUICK REFERENCE                │
├─────────────────────────────────────────────┤
│  Purple accent    #7f56d9                   │
│  Active item bg   #e5ddf7                   │
│  Text base        #18181b                   │
│  Text muted       #70707a                   │
│  Surface light    #fafafa                   │
│  Border           #d1d1d6                   │
│  Topbar bg        #18181b                   │
├─────────────────────────────────────────────┤
│  Font             Inter (400, 500, 600)     │
│  Nav text         13px / 400               │
│  Section header   12px / 600 / uppercase   │
│  Border radius    4px (small) 8px (large)  │
├─────────────────────────────────────────────┤
│  Icons            FA Pro 6.7.2             │
│  Default          fa-light                 │
│  Active           fa-solid                 │
│  AI icon          fa-solid + pink #ec4899  │
├─────────────────────────────────────────────┤
│  Figma DDS  figma.com/design/uQ4D6PHaSJaav │
│  FA Kit     78b5873547                      │
└─────────────────────────────────────────────┘
```

---

*Last updated: May 2026 | Maintained by: Design Team*
*For questions or template updates, raise a GitHub issue or contact the design lead.*
