# Portfolio Changelog
 
All notable changes to michellepinsky.work are documented here.
 
---

## [2026-10-01] — Bug fix

### Fixes
- Fixed a bug that didn't allow the top nav's external LinkedIn profile link to style correctly on mobile devices.

---

## [2026-09-29] — General fixes

### Added
- **SafeWatch case study:**
  - A References section with full APA 7th-edition citations for all 24 sources. It replaces the short "Sources" line under the taxonomy comparison table.
  - A "The product" section heading above the walkthrough.
- **ACR Evaluator case study:** a "The product" section heading above the walkthrough.

### Changed
- **SafeWatch case study:**
  - Rewrote Context, Problem, Research, How it works, Who can do what, the walkthrough steps and Outcome.
  - Restructured the Taxonomy section: the sources comparison comes first, then the category definitions.
  - The category diagram now lists the full 66-term vocabulary instead of four samples per category.
  - Redesigned the thresholds diagram:
    - Each stage is now two columns: the stage on the left, its thresholds on the right.
    - The threshold values are aligned, and the badges line up with the stage headings.
    - The arrow between stages is centered.
    - An "or" divider marks Verified as an alternative route rather than a third stage.
  - Removed the numbers from the walkthrough steps and the principle cards.
- **ACR Evaluator case study:**
  - Rewrote the summary, Context, Problem, the principles, the walkthrough steps with their captions, and Outcome.
  - Removed the numbers from the walkthrough steps and the principle cards.
  - The waiver caption now describes how the app actually records waivers.
  - The "routes to a person" chip in the Blocked outcome now matches the spacing of the other chips.
- **Homepage cards:** on phones, each stat number is vertically centered against its description.
- **Footer:** centred on phones.

### Fixed
- **iPhone text size:** iPhone Safari no longer enlarges text in wide blocks. It had been blowing up the SafeWatch permissions table's group headings.
- **Sidebar highlighting:** the case study sidebar now highlights the last section (e.g. Outcome) when it's clicked or when you reach the bottom of the page.
- **Reference links:** long DOIs and URLs wrap on phones instead of making the page scroll sideways (SafeWatch and Writing).
- **Citations:** corrected the in-text citation for the Twitch hate-raids study to its first author (Cai et al., 2023), and added the missing citation for the 2024 trigger-warning meta-analysis (Bridgland et al., 2024).
- **Text fixes:** typos and punctuation throughout the SafeWatch case study ("SafeWatch" capitalization, curly quotes), plus the "evaluation" typo and a stray period in the ACR case study.

### Removed
- **SafeWatch case study:** the placement-rule diagram, whose caption and explanatory paragraph no longer matched it.

---

## [2026-09-28] - Content additions and general fixes

### Added
- **All work page (`work.html`)**, replacing `projects.html`
  - Every case study with a thumbnail, tags under the title, and category filters (Design / Research / Operations) beside the intro.
  - Filters announce the number of results to screen readers.
  - `projects.html` now redirects here, so old links keep working.
- **Screen recordings in place of static screenshots**, each with a pause/play button. They play only while on screen and start paused when the visitor's system is set to reduce motion.
  - ACR Evaluator: score review, PDAA profile review, DAC review, finalized report.
  - SafeWatch: reporting a trigger, voting and My submissions, studio verification.
- **ACR Evaluator case study:**
  - New step 06, "The coordinator settles it", covering the DAC review.
  - A permissions tree showing what each role can do, with DAC as a flag any role can carry.
  - The principles are now numbered cards.
- **Password-protected media:** images and videos for protected case studies are now also password protected.

### Changed
- **Navigation and labels:**
  - Top navigation: "Projects" is now "Work".
  - Homepage button: "View work" is now "View all work".
  - Case study back links: "All projects" is now "All work".
  - Bottom-of-page back links go to Selected Work (for case studies on the homepage) or All Work (for the others).
- **Selected work cards:**
  - Stat text is limited to two lines at every screen size.
  - On narrower cards, stats stack as aligned rows.
  - The ACR card's "AI-Assisted Scoring" tag is now "AI".
- **Case study layout:**
  - All case study images are now full width.
  - ACR decision tree: outcome pills sit on their own line under each outcome name.
- **Sitemap:**
  - "All work" entry, with public case studies in All work order.
  - Lock icons on protected case studies.
  - The banner tag is removed, and the intro runs full width.
  - The Writing description now links to Medium.
- **Media location:** protected case study images and videos are now password protected.

### Fixed
- **Accessibility:** a WCAG 2.2 AA audit of all 15 pages took automated violations from 4 rule types down to 0.
  - Footer links meet the 24px minimum target size.
  - Reference links on the Writing page are underlined.
  - No page scrolls sideways at 320px (fixes on SafeWatch and Writing).
  - Alt text rewritten for 10 images that no longer matched their screenshots.
  - Each recording now has a short accessible name, with its full description linked separately.
- **SafeWatch figures:** a dark edge showing at the rounded corners is gone, and the phone screenshot's corner radius is reduced to match the other figures.
- **All work page:** removed a stray closing tag in the page header.

### Removed
- 25 unused images (old ACR and SafeWatch screenshots replaced by recordings, and early SafeWatch mockups).
- 3 ACR screenshots made redundant by the recordings.

---

## [2026-09-22] — Content additions

### Writing

- New article: "Deus ex Machina: Synthetic Users Amplify Persona Flaws and Discriminatory Experiences"
- Moved previous article, "Can Artificial Intelligence Truly Understand Human Disability?" to Medium.com (https://medium.com/@Pinskers/can-artificial-intelligence-truly-understand-human-disability-a6c43899ff65).

---

## [2026-06-12] — General fixes

### All case studies

- Adjusted some tags to be more semantically-structured for screen reader accuracy and navigation.
  
### style.css
- Adjusted some color contrast ratios to be WCAG 2.2 AA conformant.

### case-study-vt2-retrospective.html
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
