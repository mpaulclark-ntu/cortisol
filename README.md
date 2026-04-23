# BIOL09044 — Unit 5: Cortisol Teaching Website

A Quarto-based teaching website for the cortisol unit of the Inflammation & Cancer module at Nottingham Trent University.

## Quick Start

### Prerequisites
- [Quarto](https://quarto.org/docs/get-started/) (v1.4+)
- Git

### Local Preview
```bash
quarto preview
```

### Adding Support Materials

Copy your files from the local teaching folder into the appropriate `docs/` subdirectory:

```bash
# Lecture PDFs
cp "/Users/BIO3PAULM/Documents/Files/BIOL33141_CT Pharmacology/2025_26/YOUR_FILE.pdf" docs/lectures/

# Reading materials
cp "/Users/BIO3PAULM/Documents/Files/BIOL33141_CT Pharmacology/2025_26/YOUR_FILE.pdf" docs/reading/

# Past exams
cp "/Users/BIO3PAULM/Documents/Files/BIOL33141_CT Pharmacology/2025_26/YOUR_FILE.pdf" docs/exams/

# Practical guides
cp "/Users/BIO3PAULM/Documents/Files/BIOL33141_CT Pharmacology/2025_26/YOUR_FILE.pdf" docs/practicals/
```

Then update the links in `support-materials.qmd` to match your filenames.

### Deploy to GitHub Pages

1. Create a new GitHub repository
2. Push this project:
```bash
git init
git add -A
git commit -m "Initial commit - cortisol teaching site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/cortisol-teaching.git
git push -u origin main
```
3. In GitHub: Settings → Pages → Source → GitHub Actions
4. The site will build automatically on every push

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
├── docs/                    # ← Drop your PDFs here
│   ├── lectures/
│   ├── reading/
│   ├── exams/
│   └── practicals/
└── .github/workflows/
    └── publish.yml          # Auto-deploy on push
```

## Updating Content

- Edit `.qmd` files to update lecture content
- Add new PDFs to `docs/` subfolders and link them in `support-materials.qmd`
- Push to `main` branch — the site rebuilds automatically

## Author

Dr Mark Paul-Clark  
Senior Lecturer in Pharmacology  
Nottingham Trent University
