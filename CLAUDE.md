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

## University of Utah Official Brand Colors

**Primary Core Colors** (required for all official branding):
| Name | HEX | RGB | Usage |
|------|-----|-----|-------|
| Utah Red | #BE0000 | 190-0-0 | Primary brand color, must be prioritized |
| Black | #000000 | 0-0-0 | Secondary element |
| White | #FFFFFF | 255-255-255 | Secondary element |
| Zion Cinder Cone | #707271 | 112-114-113 | Secondary element |

**Accent Colors** (max 10% of design, never in logos/marks):
| Name | HEX | RGB |
|------|-----|-----|
| Granite Peak | #708E99 | 117-142-153 |
| Wasatch Sunrise | #FFB81D | 255-184-29 |
| Red Rocks | #890000 | 130-0-0 |
| Mountain Green | #6CC24A | 108-194-74 |
| Great Salt Lake | #3ABFC0 | 58-191-192 |
| Salt Flat Grey | #E2E6E6 | 226-230-230 |

**Color definitions in UofU.sty:**
- `utahred` (#BE0000): Primary color for frametitle, footline, structure
- `redrocks` (#890000): Used for navigation bar gradient (palette tertiary/quaternary)
- `uofu`/`uofudark`: Aliases for backward compatibility

**Theme features:**
- Uses `smoothbars` outer theme with custom footer showing author, institute, title, and page numbers
- Navigation dots displayed in single row
- Auto-generates section/subsection title frames via `\AtBeginSection` and `\AtBeginSubsection`
