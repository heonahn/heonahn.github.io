# Personal academic website — Sangheon (Heon) Ahn

Source for [heonahn.github.io](https://heonahn.github.io). A single-page,
dependency-free site (plain HTML + CSS) served by GitHub Pages.

## Structure

```
index.html      # the entire site (content + styles inline)
assets/
  profile.jpg   # web-optimized portrait
cv/
  cv.tex        # CV source (LaTeX)
  cv.pdf        # compiled CV (linked from the site)
research/        # publication & working-paper PDFs
photo/           # original full-resolution portrait
```

## Editing

- **Content** (papers, bio, links): edit `index.html` directly. Each paper is a
  `<article class="paper">` block — copy one to add a new entry.
- **Styling**: all CSS lives in the `<style>` block at the top of `index.html`.
  Colors are CSS variables in `:root` (and a dark-mode override).
- **CV**: edit `cv/cv.tex`, then recompile:
  ```sh
  cd cv && pdflatex cv.tex
  ```
- **Photo**: replace `assets/profile.jpg` (keep it small — resize from the
  original in `photo/` with e.g. `sips -Z 900 in.jpg --out assets/profile.jpg`).

## Deploy

Pushing to the `main` branch auto-publishes via GitHub Pages (Settings → Pages →
Source: `main` / root).
