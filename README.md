# Portfolio Changelog
 
All notable changes to michellepinsky.work are documented here.
 
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
