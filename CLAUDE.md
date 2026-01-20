# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands

Compile the presentation:
```bash
xelatex slide.tex
```

For bibliography support, run the full sequence:
```bash
xelatex slide.tex && bibtex slide && xelatex slide.tex && xelatex slide.tex
```

## Required LaTeX Packages

Install these on Ubuntu/Debian:
```bash
sudo apt install texlive-latex-base texlive-latex-extra texlive-latex-recommended \
  texlive-fonts-recommended texlive-fonts-extra texlive-xetex texlive-pstricks
```

## Architecture

This is a University of Utah Beamer theme for LaTeX presentations.

**Key files:**
- `UofU.sty` - Theme style file defining colors, navigation bar, and footer layout
- `slide.tex` - Example presentation using the theme
- `ref.bib` - Bibliography file
- `pic/` - Image assets (logo, figures)

**Color definitions in UofU.sty:**
- `uofu`: #BE0000 (Utah Red) - primary color
- `uofudark`: #890000 (Dark Red) - used for navigation bar gradient
- `palette secondary`: 75% uofu + 25% black
- `palette tertiary/quaternary`: uofudark

**Theme features:**
- Uses `smoothbars` outer theme with custom footer showing author, institute, title, and page numbers
- Navigation dots displayed in single row
- Auto-generates section/subsection title frames via `\AtBeginSection` and `\AtBeginSubsection`
