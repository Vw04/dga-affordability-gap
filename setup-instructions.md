# Homium Impact Site — Setup Instructions

Follow these steps in order.

---

## Step 1: Create project folder

In your VS Code terminal:

```bash
mkdir -p ~/projects/homium-impact/assets/screenshots
mkdir -p ~/projects/homium-impact/assets/photos
mkdir -p ~/projects/homium-impact/data
cd ~/projects/homium-impact
code -r .
```

---

## Step 2: Collect assets

Save these files into the project folder before starting Claude Code:

### Screenshots (save to assets/screenshots/)
- [ ] homium-homepage.png — full page screenshot of homium.io
- [ ] homium-nav.png — close-up of the homium.io top navigation bar
- [ ] homium-footer.png — close-up of the homium.io footer
- [ ] homium-colors.png — a section of homium.io that clearly shows brand colors + buttons
- [ ] homium-typography.png — (optional) a section showing Taviraj headers and Ubuntu body text with visible sizing
- [ ] gamma-template.png — full page screenshot of https://homiumimpact-ciru0f1.gamma.site/

### Photos/Logos (save to assets/photos/)
- [ ] homium-logo.png — Homium logo file (or cropped from website)
- [ ] thhi-logo.png — THHI Detroit logo
- [ ] udf-logo.png — Utah Dream Fund logo
- [ ] thhi-impact.pdf — Detroit borrower impact slides
- [ ] udf-impact.pdf — Utah borrower impact slides
- [ ] Any borrower photos you want on the site

### Data (save to data/)
- [ ] affordability-data.xlsx — state-by-state affordability gap data

---

## Step 3: Copy project files into the folder

The three .md files generated with this guide need to be placed in your project root:

- CLAUDE.md → ~/projects/homium-impact/CLAUDE.md
- plan.md → ~/projects/homium-impact/plan.md
- log.md → ~/projects/homium-impact/log.md

You can drag and drop them into the VS Code explorer panel, or copy them via terminal.

---

## Step 4: Create GitHub repo

1. Go to github.com → + → New repository
2. Name: homium-impact
3. Public, no README, no .gitignore
4. Create repository

Back in VS Code terminal:

```bash
git init
git remote add origin https://github.com/Vw04/homium-impact.git
```

---

## Step 5: Initial commit

In VS Code terminal:

```bash
git add .
git commit -m "Initial project setup with CLAUDE.md, plan.md, log.md, and assets"
git push -u origin main
```

---

## Step 6: Start building with Claude Code

Open Claude Code panel. Switch to Plan mode (Shift+Tab). First message:

```
Read plan.md. Review all files in assets/screenshots/ to understand the design reference. Review data/affordability-data.xlsx to understand the data structure. Then tell me your plan for Phase 1 and Phase 2 before writing any code.
```

Claude will outline its approach. Review, adjust, approve. Then let it build.

---

## Step 7: When you're done for the day

```
Wrap up: update plan.md with what we accomplished and what's next. Add an entry to log.md for today. Then commit and push.
```

---

## Step 8: Enable GitHub Pages (after site looks good)

1. Go to github.com/Vw04/homium-impact
2. Settings → Pages
3. Source: Deploy from a branch
4. Branch: main, / (root)
5. Save

Live URL: https://vw04.github.io/homium-impact/
