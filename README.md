# Thesis template (papers-based, UTwente / ITC)

Flat, papers-template-style version of the UT dissertation template.

| To change...            | Edit                                   |
|-------------------------|----------------------------------------|
| **Colors**              | `Colors.tex` (one `\SetPalette` line)  |
| Title, names, committee | `Main.tex`, section 1                  |
| Which chapters compile  | `Main.tex`, section 3                  |
| Summary, dankwoord...   | `FrontMatter/`                         |
| Appendices, bio, pubs   | `EndMatter/`                           |
| Acronyms / references   | `Acronyms.tex` / `Main.bib`            |

## Adding a paper as a chapter
1. Copy `Chapters/02_Paper1` to e.g. `Chapters/05_MyPaper`.
2. Drop in the section files from your paper (`Introduction.tex`, `Methodology.tex`, ...) and figures in `figures/`.
3. Paste the abstract/keywords in `Chapter.tex` (`\sep` works as in elsarticle) and set `\chapterbasedon{bibkey}`.
4. Add `\IncludeChapter{Chapters/05_MyPaper}` in `Main.tex`.

Use chapter-specific label prefixes (`sec:paper3:...`) to avoid clashes.

## Modes
`\usepackage[review]{thesis-style}` (A4, line numbers), `[draft]` (chapters only), `[print,cover]` (bleed, crop marks, cover PDFs).

Compile: pdfLaTeX + BibTeX (Overleaf default) or `latexmk -pdf Main`.
