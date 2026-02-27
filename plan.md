# Project Plan: DGA & State Affordability Gap Site

## Summary
A single-page HTML website showcasing Homium's two launched shared-appreciation mortgage programs (THHI Detroit and Utah Dream Fund), their borrower impact, media coverage, and a state-by-state affordability gap analysis tool. Deployed via GitHub Pages at vw04.github.io/dga-affordability-gap/.

## Goals
- Professional, clean site matching Homium brand (fonts, colors, whitespace)
- Clearly communicate what both programs do and their impact
- Embed YouTube video and link to news articles
- Interactive affordability gap explorer by state
- Mobile responsive
- Easy to maintain and update

## Current State
- [x] Project initialized, assets collected
- [x] CLAUDE.md, plan.md, log.md in place
- [x] index.html built and deployed to GitHub Pages
- [x] All phases complete: data prep, HTML structure, styling, affordability tool, deploy
- [x] Affordability tool redesigned: full US map background, two-column layout (state SVG left, data cards right), gap card full-width below
- [x] Map and zoom polish: center-positioned map background, aspect-ratio-aware state zoom, 19-state SVG panel with overflow:hidden containment
- [x] Methodology caption + expandable disclosure added below gap card (state-selected only)
- [x] Program card buttons updated to "Visit" only (removed displayed URL text)
- [x] Mobile layout fixed: affordability tool stacks full-width (dropdown → map → cards), cards centered, map no longer cut off
- [x] Affordability section moved above Relevant News; .alt class swapped to maintain background alternation; data cards pinned to #ffffff
- [x] Map outline updated: CSS mask approach with exact green rgba(61,122,88,0.35) to match selected-state border; desktop padding increased to 72px
- [x] Placeholder text color matched to section body gray (var(--gray) / #555)
- [x] Full page section reorder: hero → video → programs (gray) → affordability (white) → borrower impact (gray) → news (white); .alt classes adjusted to maintain alternating pattern

## Live Site
https://vw04.github.io/dga-affordability-gap/

## What's Next
- Optional polish:
  - Add Homium Gold logo to dark footer (currently using Blue logo with invert filter)
  - Consider adding a `.gitignore` for `.DS_Store` files
  - Consider expanding affordability tool beyond the current 19 states

## Build Phases

### Phase 1: Data Prep
1. Extract exact hex color values from assets/screenshots/homium website/
2. Convert data/DGA Affordability Gap Calculations - 2026.xlsx into a JavaScript object
3. Review assets/screenshots/gamma site template/ for content and layout reference
4. Review assets/slides/ PDFs for borrower impact stories and KPIs

### Phase 2: Core HTML Structure
5. Build page skeleton: nav, hero, programs, impact, video, news, affordability, footer
6. Add Google Fonts (Taviraj + Ubuntu)
7. Apply base typography rules
8. Add all text content (from Gamma template screenshots and slides)

### Phase 3: Styling
9. Apply Homium brand colors throughout
10. Style each section to match homium.io aesthetic
11. Add images/logos from assets/photos and logos/
12. Ensure generous whitespace and clean layout

### Phase 4: Affordability Tool
13. Build state dropdown component
14. Wire up JS data object to populate on state selection
15. Style the data display cards
16. Emphasize affordability gap number visually

### Phase 5: Polish + Deploy
17. Mobile responsiveness pass
18. Test all links (program sites, YouTube, news articles)
19. Final visual QA against homium.io screenshots
20. Enable GitHub Pages
21. Share live URL

## Decisions Made
- Single index.html file, all CSS/JS inline
- No frameworks — vanilla HTML/CSS/JS only
- Affordability data hardcoded as JS object (not fetched from xlsx at runtime)
- Fonts: Taviraj (headers), Ubuntu Bold uppercase (subheaders), Ubuntu Light (body)
- GitHub repo: dga-affordability-gap

## Open Questions
- Which borrower stories/quotes to feature? (will come from PDF review)
- Exact text content for hero section headline and subheadline?

## News Articles (include links + brief descriptions on site)
1. **Down Payment Challenge in Metro Detroit** — Axios reports it takes ~8 years to save for a down payment in Metro Detroit, highlighting how down payment barriers constrain homeownership and why DPA programs are critical.
   https://www.axios.com/local/detroit/2026/02/04/down-payment-metro-detroit-house-home-mortgage
2. **Housing Inventory Challenges** — WSJ reports on home builders turning to the White House for help addressing inventory constraints, underscoring the broader housing supply challenges that DPA programs help address.
   https://www.wsj.com/economy/housing/home-builders-turn-to-white-house-for-help-on-inventory-glut-7e41e708
3. **Innovative DPA Models** — Investopedia highlights a Midwestern city and NBA star partnership covering 40% of homebuyers' down payments, showcasing innovative philanthropic and community-driven approaches to down payment assistance.
   https://www.investopedia.com/this-midwestern-city-and-an-nba-star-will-cover-40-of-homebuyers-down-payments-11815298
4. **Rep. Andy Barr on Fair Share Appreciation Mortgages** — Congressional support for innovative mortgage solutions that expand homeownership access, highlighting bipartisan recognition of DPA programs' impact.
   https://www.linkedin.com/posts/homium_rep-andy-barr-fair-share-appreciation-mortgages-activity-7402075947799412736-IN3g
5. **Congressional Hearing on Housing & Urban Development** — C-SPAN coverage of House Committee oversight hearing featuring Rep. Andy Barr's remarks on innovative mortgage solutions at 1:07:30, demonstrating legislative support for DPA programs.
   https://www.c-span.org/clip/house-committee/user-clip-rep-jim-himes-and-rep-andy-barr-on-solutions-for-affordable-homeownership/5192601
6. **CFPB Issue Spotlight: Home Equity Contracts** — Endnote 23 references Homium as an example of companies offering shared equity programs that are 1:1 sales of the home's value.
   https://www.consumerfinance.gov/data-research/research-reports/issue-spotlight-home-equity-contracts-market-overview/

## Content Sources
- Program descriptions + impact data: assets/screenshots/gamma site template/
- Borrower impact stories: assets/slides/
- Style reference: assets/screenshots/homium website/
- Program site reference: assets/screenshots/thhi website/ and assets/screenshots/udf website/
- Affordability data: data/DGA Affordability Gap Calculations - 2026.xlsx
- Video: https://youtu.be/XZCdLg3x2T0?si=o5pLWt4IHojUm3bG
- Program sites: https://www.thhidetroit.com/ and https://www.utahdreamfund.com/
