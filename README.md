# Zhao Yuxi · Portfolio

A static personal site styled as an academic preprint: title page, boxed
Abstract, a two-column body (Education & Experience, Selected Projects,
Instrument Panel, Correspondence). Plain HTML/CSS/JS: no build step, no
framework, no tracking.

## Files

- `index.html`: all content
- `style.css`: styling (dark multi-hue gradient backdrop, by design, no theme toggle)
- `script.js`: mobile nav toggle, scroll-reveal, active-section nav highlight
- `assets/CV_Yuxi.pdf`: copy of the CV, linked from the header "PDF" button

## Contact links

Email, GitHub (`github.com/YUXI-NUM`) and LinkedIn
(`linkedin.com/in/yuxi-zhao-394a24330`) are already filled in under
`<section id="contact">`. Phone number and home address from the CV were
**left out on purpose**; add them back under `.contact-facts` in
`index.html` if you want them public.

## Deploy to GitHub Pages

1. Create a new GitHub repo. For a `YUXI-NUM.github.io` style URL, the repo
   must be named exactly `YUXI-NUM.github.io`; any other name works too and
   serves at `YUXI-NUM.github.io/<repo-name>/`.

2. From this folder:

   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/YUXI-NUM/<repo-name>.git
   git push -u origin main
   ```

3. In the repo on GitHub: **Settings → Pages → Build and deployment → Source:
   Deploy from a branch**, branch `main`, folder `/ (root)`. Save.

4. The site goes live at the URL GitHub shows there (usually live within a
   minute or two).

## Local preview

No server needed, just open `index.html` directly in a browser. If you want
to test with a local server (closer to how Pages serves it):

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Updating project content later

- The featured project (MOGA humanoid) is the `<article class="prj">` block
  under `<section id="projects">`, marked `[1]`.
- Projects 2 through 8 are `<li class="ref-item">` entries in the
  `<ol class="ref-list">` right after it, each one paragraph ending in a
  `Keywords:` line.
- Education/experience entries are `<li>` items in `<ol class="cv-list">`
  under `<section id="education">`.
