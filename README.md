# Cortisol Teaching Website

A Quarto-based teaching website covering cortisol physiology, pathophysiology, and drug discovery, taught at Nottingham Trent University.

Live site: <https://mpaulclark-ntu.github.io/cortisol/>

## Quick Start

### Prerequisites
- [Quarto](https://quarto.org/docs/get-started/) (v1.4+)
- Git

### Local Preview
```bash
quarto preview
```

### Adding Support Materials

Copy your files from your local teaching folder into the appropriate `docs/` subdirectory. Use lowercase, hyphenated filenames (e.g. `cortisol-lecture-slides.pdf`, not `Cortisol_Lecture_Slides.pdf`).

```bash
# Lecture PDFs and practice materials
cp ~/path/to/your-file.pdf docs/lectures/

# Reading materials
cp ~/path/to/your-file.pdf docs/reading/

# Practical guides
cp ~/path/to/your-file.pdf docs/practicals/
```

Then update the links in `support-materials.qmd` to match your filenames.

> Note: `docs/exams/` is listed in `.gitignore` and is not published. Keep any materials you don't want students to access via that folder.

### Day-to-day updates

1. Edit `.qmd` files to update lecture content or add support-material links.
2. Commit and push:
   ```bash
   git add -A
   git commit -m "Short description of change"
   git push
   ```
3. The GitHub Actions workflow rebuilds and redeploys the site automatically on every push to `main` (~2 minutes).

### Project Structure

```
cortisol-teaching-site/
├── _quarto.yml              # Site configuration
├── index.qmd                # Landing page
├── support-materials.qmd    # Downloadable resources page
├── resources.qmd            # Reading list & glossary
├── styles.css               # Website theme
├── styles-slides.scss       # Presentation theme
├── lectures/
│   ├── 01-endocrine-gr-signalling.qmd
│   ├── 02-physiological-actions.qmd
│   ├── 03-pathophysiology.qmd
│   ├── 04-ncx1015-discovery.qmd
│   ├── 05-drug-discovery-process.qmd
│   ├── cortisol-full.qmd    # Combined slide deck
│   └── assessment-questions.qmd
├── docs/                    # Published alongside the site
│   ├── lectures/
│   ├── reading/
│   └── practicals/
└── .github/workflows/
    └── publish.yml          # Auto-deploy on push
```

## Author

Dr Mark Paul-Clark
Senior Lecturer in Pharmacology
Nottingham Trent University
