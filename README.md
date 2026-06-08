# Portfolio Changelog
 
All notable changes to michellepinsky.work are documented here.
 
---

 ## [2026-06-08] — Screen reader fixes

*Tested with JAWS*

### Navigation and page structure

- Fixed footer announcing before page content on load
- Fixed region count announcing twice on load

### `index.html`

- Project cards rebuilt using the block link pattern — card content now reads as static text rather than link text, with a single named link per card
- Filter tags and metric chips now read correctly
- Password-protected cards now announce their protected status before navigation

### All case studies

- Section labels and hero tags were hidden from screen readers — now exposed
- Figures: descriptions moved from `aria-label` on `<figure>` to `alt` on `<img>` for photo figures; `figcaption` repositioned after content where it had been placed before
- Decorative elements (arrows, dividers, colour swatches, status dots, rule lines) marked `aria-hidden`

### `case-study-cova-design-system.html`

- `aria-hidden` removed from all coded component figures; component panels, colour swatch groups, buttons, cards, hero, tabs, and stat blocks now grouped with `role="group"` and descriptive labels
- Semantic headings added to component demo panels per USWDS conventions
- Agency theme palette rows, contrast audit rows, T4 constraint diagram, component spec table, and field schema mock UI all grouped and labelled

### `case-study-darktide.html`

- Listening tour center node was hidden — now exposed and grouped
- Schedule table session blocks grouped by participant group
- Affinity board and Discord session images: descriptions corrected to `alt` text

### `case-study-beyond-audiogram.html`

- All three journey map figures (AAA baseline, emotional hotspots, redesigned journey): phases and individual stages grouped and labelled; hotspot stages carry emotional context in their label; decorative arrows hidden
- Themes grid columns grouped by phase
- Journey map legend swatches marked decorative

### `case-study-itc-register.html`

- HB 2541 gap analysis columns grouped and labelled
- Inbox chaos figures: Teams and email columns grouped; each message grouped by sender
- Scoring model tier cards grouped and labelled
- DevOps register: system work items and their child issues grouped together
- Kanban board: lanes and individual cards grouped and labelled with tier
- Work item detail view: main panel, sidebar, child issue list, metadata sections, and scoring all grouped and labelled

### `case-study-vita-redesign.html`

- Label comparison figure: column headers and each nav group (top-level, Policy & Governance, Procurement) grouped and labelled; flag swatch in caption marked decorative
- Site architecture diagram: each section branch grouped with page count; decorative trunk and branch lines hidden; legend swatches marked decorative

### `case-study-vt2-retrospective.html`

- Findings grid: each content area card grouped and labelled with content name and verdict
---

## [2026-06-08] — Accessibility fixes
 
### `index.html`
- Fixed WCAG 2.5.3 (Label in Name) violations on all six case study card links — `aria-label` values now open with the exact visible card title text
- Corrected Beyond Audiogram label from "Cochlear Implants" to "CI Recipients" to match rendered text
- Corrected COVA label from "Commonwealth of VA Design System" to "COVA Design System Rebuilt in USWDS"
- Corrected Darktide label from "Building a Qualitative Research Program at Fatshark" to "Building a Qualitatively Data Rich Playtest"
- Replaced em dashes with commas in all `aria-label` values for cleaner screen reader announcement
- Removed parentheses around "password protected" in favour of plain comma-separated phrasing
### `writing.html`
- Removed two prohibited `aria-labelledby` attributes from `<p>` elements (unsupported role/attribute combination)
- Replaced `<div class="writing-ai-card">` wrappers with `<figure>` elements; model name labels converted from `<p class="writing-ai-label">` to `<figcaption class="writing-ai-label">` for correct semantic association
- Removed now-unnecessary `id` attributes (`ai-label-gpt`, `ai-label-claude`) from former label paragraphs
### `style.css`
- Fixed contrast failure on `.cs-hero-tag` (Think Piece, AI & Disability Inclusion tags): text color `#C8DEFF` → `#ffffff`, ratio against `#1f72b2` background improves from 3.73:1 to 4.60:1 (WCAG AA)
- Fixed contrast failure on `--dim` across all case studies: `#767676` → `#666`, ratio against `#f7f6f3` improves from 4.20:1 to 5.31:1 (WCAG AA); ratio against `#ffffff` is 5.74:1
- Updated `--dim` custom property declaration and all 31 hardcoded `color: #767676` instances
---
 
## [2026-06-08] — Responsive layout and navigation
 
### `nav.html`
- Added hamburger menu for screen widths below 768px; site name remains visible at all sizes
- Hamburger toggles a mobile nav drawer with `aria-expanded` state management
### `index.html`
- Filter bar (All / Design / Research / Operations pills) hidden on mobile; "Selected work" heading remains visible
### `style.css`
- Fixed orphaned right border on case study meta info strip at narrow widths (affects all case studies)
- Fixed corner overflow on ITC register case study figures (top and bottom)
- Fixed ITC swim lane figure gap between swim lines at iPad-range widths
- Fixed Darktide research schedule: all time blocks visible at small screen sizes; unobserved freeplay block preserved at all sizes including iPad mini via `:has(.dt-evening-tag)` at the 860px breakpoint
- Fixed VITA IA figure: condenses to single stacked column without connectors at small screen sizes
### `footer.html`
- Added changelog link pointing to GitHub
---
 
## [2026-06-07] — Initial website launch
