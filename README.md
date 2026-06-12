# Portfolio Changelog
 
All notable changes to michellepinsky.work are documented here.
 
---

## [2026-06-12] — General fixes

### All case studies

- Adjusted some tags to be more semantically-structured for screen reader accuracy and navigation.
  
### style.css
- Adjusted some color contrast ratios to be WCAG 2.2 AA conformant.

### vt2-retrospective.html
- Full PDF report now password-protected.

---

## [2026-06-11] — General fixes

### All case studies

- Added an executive summary at the top of the main content for those with limited time

### style.css
- Fixed `.dt-cell-note:has(.dt-evening-tag)` specificity collision between `≤860px` and `≤560px` breakpoints; "Diary study begins" no longer overlaps AM/PM blocks when stacked at small screen sizes
- Added `.cs-exec-summary`, `.cs-exec-summary-label`, `.cs-exec-summary-text` styles for grey executive summary box (`#F5F4F2` background, 8px border-radius)
- Added `.card-title a` base styles (ink color, no underline at rest) and `.card:hover .card-title a` hover state (accent blue, underline)
- Added `.card:hover .card-title .light` hover state to carry accent color through to grey subtitle span

---

## [2026-06-10] - General fixes

### index.html
- Updated hero subtitle copy to reflect portfolio content: now references UX research, design leadership, accessibility, inclusive design, and regulated/high-governance environments with bolded key terms
- Added `tabindex="-1"` to all `.card-arrow` divs; full-card click already handled by `.card-title a::after` overlay

### about.html
- Added Skills & Tooling section with four categories: Research, Design & Systems, Accessibility, Tools & Platforms (includes Dovetail, UserTesting, Claude)
- Reordered page sections: Skills & Tooling moved between bio and Guiding Principles

### case-study-vt2-retrospective.html
- Added "View the full report" CTA button in hero section
- Updated impact row; added 80.9% core player stat
- Pulled methodology into its own dedicated `#methodology` section with structured tables for quantitative and qualitative approaches; sidenav updated to include new anchor
- Additional survey figures surfaced from PDF report: platform split (97.8% PC), difficulty distribution (46.2% Legend), lapsed-player segment (42.5% hadn't played in 1+ month)

### case-study-beyond-audiogram.html
- Added "View the full academic paper" CTA button in hero section
- Added journey mapping Miro board image (`images/journey-mapping-miro.png`) with caption in Process section
- Added Figure 1: diverging Likert bar chart (7 statements, n=197, real CSV data) with per-segment percentage labels, staggered below-bar label rows, tick lines, and inline labels for very narrow segments; full screen reader `aria-label` with per-statement percentages
- Added Figure 2: co-designer dot plot (Likert scores on 7–35 scale, 6 participants, avg 13.86 marked) with legend, descriptive figcaption, and screen reader `aria-label`

### style.css
- Added `.about-skills-wrap`, `.skills-grid`, `.skill-group-title`, `.skill-list` styles for About skills section; responsive at 768px (2-col) and 560px (1-col)
- Fixed `.about-skills-wrap` alignment: now matches `.about-principles-wrap` padding structure (`max-width: 1120px`, `48px` horizontal padding)
- Added `.cs-hero-actions` and `.btn-ghost--hero` for case study hero CTA buttons
- Fixed `dt-cell-note` overflow in Darktide schedule table: added `min-width: 0`, `word-break`, `overflow-wrap`; widened note column from 120px to 140px in `dt-row` grid template

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
