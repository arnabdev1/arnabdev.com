# Arnab Dev — Personal Portfolio

Simple academic-style portfolio (plain HTML + CSS, no build step). Designed for GitHub Pages.

## Structure

```
research.portfolio/
├── index.html        # Home (photo, intro, links)
├── experience.html   # Industry skills + work experience
├── research.html     # Publications / posters, newest first
├── projects.html     # Hackathon & extracurricular project cards
├── cv.pdf            # Served at yoursite.com/cv.pdf
├── css/style.css     # All styling
└── assets/           # Images (see below)
```

## Images to copy in

Copy these from your old portfolio's `public/` folder (arnabdev.portfolio) into `assets/`:

- `arnab.jpg` (home page headshot)
- `neurosync-logo.png`, `sprinklify.png`, `vafuzz.png`, `utd.png`, `hydra.png`,
  `legal.png`, `ide.png`, `simplecalc.png`, `nifportfolio.png`, `personalportfolio.png`

Missing project images hide themselves automatically (the cards still render fine),
so you can add them gradually.

## How to add new content

Each page has a big `TO ADD A NEW ...` comment block with a copy-paste template:

- **Experience** (`experience.html`) — copy the `.entry` block, paste newest-first.
- **Research** (`research.html`) — two templates: *paper* (title + authors + link,
  no image) and *poster/talk* (with image + description). Paste new entries at the
  top so the list stays newest-first. The date always goes in `entry-meta`.
- **Projects** (`projects.html`) — copy the `.project-card` block. Delete the
  `<img>` line if the project has no image.

## Deploy to GitHub Pages

```bash
cd research.portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Source: Deploy from a branch → main / (root)**.

- If the repo is named `<your-username>.github.io`, the site is served at the root domain.
- Otherwise it's served at `https://<your-username>.github.io/<repo-name>/` — the site
  uses relative links, so both work, and `cv.pdf` is reachable at `<site-url>/cv.pdf`.
