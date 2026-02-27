# Session Log

## Session 7 — 2026-02-27
- What was done:
  - Reordered all page sections for improved narrative flow: hero → video → programs → affordability → borrower impact → news
  - Adjusted `.alt` class assignments to maintain white/gray alternating background pattern: programs gained `.alt` (gray), affordability lost `.alt` (white); borrower impact and news unchanged
  - Used Python script to extract and reassemble section blocks cleanly (same approach as prior reorders)
- Decisions made:
  - Python script is the reliable method for multi-section HTML reorders — avoids giant Edit blocks and whitespace errors
  - `#affordability .data-card { background: #ffffff }` override left in place; harmless on white background
- Next session should: Add Homium Gold logo to footer; consider expanding affordability tool to more states

## Session 6 — 2026-02-26
- What was done:
  - Moved affordability section above Relevant News in page order; swapped `.alt` class between the two sections to preserve white → gray → white → gray → white alternating pattern; added `#affordability .data-card { background: #ffffff }` to keep cards crisp white on gray background
  - Replaced CSS `filter` approach for map outline with CSS `mask-image` + `background-color: rgba(61,122,88,0.35)` — guarantees exact same green as selected-state border stroke; fade-out transition on state select still works via `opacity`
  - Increased desktop affordability section padding from `48px` to `72px`; added explicit mobile override to keep `48px` on ≤768px
  - Changed `.tool-placeholder` color from `#bbb` to `var(--gray)` (#555) to match section body text
- Decisions made:
  - CSS `mask-image` is the correct approach for exact color matching when tinting an SVG background — `filter` is inherently approximate
  - Swapping `.alt` between reordered sections is the minimal change to fix background alternation
- Next session should: Add Homium Gold logo to footer; consider expanding affordability tool to more states

## Session 5 — 2026-02-25
- What was done:
  - Updated program card buttons to "Visit" only (removed displayed URL text); applies to both desktop and mobile — same HTML element
  - Fixed mobile affordability layout: added `align-items: stretch` to `.tool-columns` at 768px breakpoint — in column flex direction, `flex-start` caused items to shrink to content width and left-align; `stretch` makes them full-width
  - Fixed mobile map cut-off: added `#us-map { height: 220px }` on mobile to override desktop `280px`, eliminating overflow clip at `max-height: 240px`
- Decisions made:
  - `align-items: stretch` is the correct fix for full-width flex items in a column flex container
  - SVG height and panel max-height kept in sync (both 220px on mobile) to prevent any clipping
- Next session should: Add Homium Gold logo to footer; consider expanding affordability tool to more states

## Session 4 — 2026-02-25
- What was done:
  - Added 48px vertical padding to `#affordability` section for breathing room around the map
  - Added `#methodology-note` block below the gap card (visible only when a state is selected)
    - Muted caption (13px, #6B7280) with thin divider line above
    - Native `<details>/<summary>` "View Full Methodology" toggle — no JS required
    - Expanded body: data sources, methodology description, and Disclosure paragraph ("Disclosure:" bolded; no italics, no other bold)
- Decisions made:
  - `.state-selected` class toggle pattern reused to show/hide `#methodology-note` — consistent with existing approach
  - Native `<details>` element preferred over JS toggle for simplicity and accessibility
- Next session should: Mobile responsiveness for two-column layout; optional footer logo swap

## Session 3 — 2026-02-24
- What was done:
  - Redesigned affordability gap tool layout: two-column view (zoomed state SVG left, data cards right), gap card full-width below; `overflow:hidden` on state panel prevents state from bleeding into card area
  - Default view: full US map background (us-map-outline.svg) with dropdown centered; map fades out on state selection via `.state-selected` class toggle
  - Data cards reordered: AMI | Home Value / AHP | Down Payment / Rent (full-width), gap card separate
  - Iteratively fixed map background: `cover` → `82% auto` with `no-repeat`, `center center` positioning; map moved inside full section area (section-head moved inside `.tool-area`)
  - State zoom rewritten: `zoomToState()` now matches viewBox aspect ratio to SVG panel display dimensions so every state (tall CA, wide KS) fills the full panel
  - Compacted affordability section: reduced card padding/font-sizes, section padding, gap margins to fit on one viewport
  - Increased map opacity 0.10 → 0.16; tuned zoom padding factor 0.2 → 0.06
- Decisions made:
  - State panel strictly contained with `overflow: hidden` — no CSS hacks needed for z-index overlap
  - `background-size: 82% auto` with `background-repeat: no-repeat` prevents map tiling and keeps map within section bounds
  - viewBox aspect-ratio matching in JS is the correct fix for state zoom letterboxing
- Next session should: Mobile responsiveness pass for two-column affordability layout; optional footer logo swap; consider expanding to more states

## Session 2 — 2026-02-20 to 2026-02-23
- What was done:
  - Analyzed color palette from homium.io screenshots (primary green ~#3D7A58, white bg, dark navy text)
  - Converted affordability gap xlsx (19 states) to hardcoded JS object using user-provided pre-computed values
  - Built full index.html: nav, hero, programs, borrower impact metrics + stories, YouTube embed, 6 news articles, 19-state affordability tool, footer
  - Added background images to hero (homiumbackground.jpg) and program cards (Detroit photo, Utah landscape) with white overlays
  - Centered Programs section header, tuned overlay opacity to 0.72
  - Fixed image paths: URL-encoded spaces (%20) for GitHub Pages compatibility
  - Added .nojekyll to bypass Jekyll and serve static assets directly
  - Committed and pushed all assets to origin main; GitHub Pages enabled at vw04.github.io/dga-affordability-gap/
- Decisions made:
  - White overlay at rgba(255,255,255,0.72) for background images
  - YouTube embed left as-is; Error 153 is a file:// local issue, expected to resolve on HTTPS
  - Affordability Gap data hardcoded (not computed at runtime)
- Next session should: Verify live site fully functional — images, video, all links. Address any remaining visual polish.

## Session 1 — 2026-02-19
- What was done: Project folder created. Assets collected (photos, logos, screenshots, slides, affordability data xlsx). CLAUDE.md, plan.md, log.md created.
- Decisions made: Single-page HTML, inline CSS/JS, vanilla JS only, GitHub Pages deployment. Repo name: dga-affordability-gap.
- Next session should: Start Phase 1 — extract colors from homium screenshots, convert xlsx to JS data object, review gamma template for content, then begin building index.html.
