# UPRM Thesis and Dissertation LaTeX Template

LaTeX template for theses and dissertations at the University of Puerto Rico at Mayagüez (UPRM).

## Main file

Compile `tesis.tex`.

## Option 1 — Overleaf

1. Download this repository as a ZIP.
2. In Overleaf, create a new project and upload the ZIP.
3. Make sure `tesis.tex` is selected as the main document.
4. Compile with pdfLaTeX.

> Note: Overleaf's free plan may impose compilation-time limits. The same template can be compiled locally without those limits.

## Option 2 — Compile locally (recommended for large theses/dissertations)

### Windows

Install either **MiKTeX** or **TeX Live**, then install **Visual Studio Code** and the **LaTeX Workshop** extension.

1. Download or clone this repository.
2. Open the project folder in VS Code.
3. Open `tesis.tex`.
4. Build the LaTeX project from LaTeX Workshop.

### Command line

A complete build with BibTeX can be done with:

```bash
pdflatex tesis.tex
bibtex tesis
pdflatex tesis.tex
pdflatex tesis.tex
```

If `latexmk` is installed, this is simpler:

```bash
latexmk -pdf tesis.tex
```

## Project structure

- `tesis.tex` — main document
- `prelim/` — title page, abstract, acknowledgments, acronyms, symbols
- `chapters/` — thesis/dissertation chapters
- `images/` — figures used by the example document
- `referencias.bib` — BibTeX bibliography database

## Important

Do not add generated LaTeX files such as `.aux`, `.toc`, `.lof`, `.lot`, `.log`, `.ps`, or compiled PDFs to the repository unless you intentionally want to distribute a PDF release. These are recreated automatically during compilation.

## Committee title pages

The template includes title-page files for different committee sizes in `prelim/`. In `tesis.tex`, select the appropriate `\include{prelim/portada...}` line for your committee.

## License / institutional status

Add the appropriate license and institutional disclaimer here before public distribution, according to UPRM requirements.
