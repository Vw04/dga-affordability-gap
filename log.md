# Session Log

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
