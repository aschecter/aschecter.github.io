# aschecter.github.io

Personal website. Built with [Quarto](https://quarto.org/).

## Local preview

From the project root:

```bash
quarto preview
```

This opens the site at `http://localhost:NNNN` and rebuilds on every save. Edit any `.qmd` or `styles.css` and the browser refreshes automatically.

## Project structure

```
aschecter-site/
├── _quarto.yml          # Site config: navbar, theme, fonts
├── styles.css           # All visual styling lives here
├── index.qmd            # Home
├── research.qmd         # Research streams + publications
├── teaching.qmd         # Courses + AI cert
├── workshops.qmd        # Workshops & Consulting
├── code.qmd             # Code & Data (placeholder)
├── contact.qmd          # Contact
├── images/
│   └── headshot.jpg     # Drop your headshot here
└── cv.pdf               # Drop your CV PDF here
```

## To do before launch

1. Add `images/headshot.jpg` (any portrait-orientation JPG works; the photo
   tile will crop to fit).
2. Add `cv.pdf` at the project root.
3. Fill in placeholder `#` links for Google Scholar, LinkedIn (search the
   files for `href="#"`).
4. Sanity-check that `quarto preview` renders everything correctly.

## Build & deploy to GitHub Pages

```bash
quarto publish gh-pages
```

The first time, Quarto walks you through connecting to GitHub. After that,
this single command builds the site and pushes to the `gh-pages` branch.
GitHub Pages serves whatever is on that branch.

## Updating content

Most updates only touch a single `.qmd` file:

- New talk → add a line in `index.qmd` under the talks section.
- New paper → add a line in `research.qmd` under the right publication section.
- New workshop offering → add an `.item-row` block in `workshops.qmd`.

Visual updates (colors, spacing, fonts) live in `styles.css` and flow through
all pages at once.
