# Project: DGA & State Affordability Gap

## What This Is
Single-page HTML website showcasing Homium's two launched programs (THHI Detroit, Utah Dream Fund), borrower impact data, news coverage, and a state-by-state affordability gap analysis tool. Deployed via GitHub Pages.

## Tech Stack
- Single index.html file with inline CSS and JavaScript
- No frameworks. Vanilla JS only.
- Google Fonts: Taviraj (headers), Ubuntu (subheaders + body)
- Hosted via GitHub Pages at vw04.github.io/dga-affordability-gap/

## Typography Rules (STRICT)
- H1/H2 headers: Taviraj, regular weight
- Subheaders/labels: Ubuntu Bold, UPPERCASE, letter-spacing: 2px
- Body text: Ubuntu Light (300 weight)
- Do NOT use any other fonts

## Color Palette (match homium.io exactly)
- Reference: assets/screenshots/homium website/ for color and style reference
- Extract exact hex values from the screenshots before writing CSS

## Design Rules
- Clean, professional, minimal — not busy
- Generous whitespace between sections
- Reference assets/screenshots/gamma site template/ for content layout
- Reference assets/screenshots/homium website/ for style/fonts/colors
- Mobile responsive

## Page Sections (in order)
1. Nav bar with Homium logo
2. Hero section — Homium impact headline
3. Program cards — THHI Detroit + Utah Dream Fund (brief descriptions, links to program sites)
4. Borrower impact section — key stories and KPIs from both programs
5. Video embed — YouTube: https://youtu.be/XZCdLg3x2T0?si=o5pLWt4IHojUm3bG
6. News section — article links with titles (see plan.md for full list)
7. Affordability Gap Analysis — interactive state dropdown, populates data from inline JS object
8. Footer

## Affordability Gap Analysis Rules
- Central dropdown listing all states from the data file
- On state select: display AMI, Median Home Value, Median Rent, Affordable Home Price, Down Payment (3%), Affordability Gap
- Affordability Gap number should be visually emphasized (large, colored, prominent)
- Data source: data/DGA Affordability Gap Calculations - 2026.xlsx (convert to JS object during build, do NOT reference xlsx at runtime)
- Clean card/grid layout for the data points

## File Structure
- index.html — the entire site (CSS + JS inline)
- assets/photos and logos/ — logos, stock photos, brand images
- assets/screenshots/ — design reference only (gamma site template, homium website, thhi website, udf website)
- assets/slides/ — borrower impact PDFs (THHI and UDF)
- data/ — source xlsx for affordability gap data

## Rules for Claude
- Read plan.md at session start for current status
- Do NOT read files unless directly relevant to current task
- Do NOT scan the full project folder unless asked
- Show only changed sections when editing — never the full file
- Ask before making changes to multiple sections at once
- Keep all CSS and JS inline in index.html
- When building the affordability data, convert xlsx to a JS object ONCE and hardcode it into index.html

## Commands
- `open index.html` — preview locally
- `git add . && git commit -m "message" && git push` — deploy

## Current Status
- See plan.md for project plan and progress
- See log.md for session history
