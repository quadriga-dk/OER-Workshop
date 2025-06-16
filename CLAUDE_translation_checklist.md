# OER-Workshop Translation Checklist

## Core Configuration Files

### `_config.yml`

- [x] Translate `title: "OER-Workshop"` to English
- [x] Update `author` field if needed
- [x] Translate `copyright` field
- [x] Update `extra_footer` section:
  - [x] Translate Creative Commons license text
  - [x] Translate QUADRIGA project description
  - [x] Translate ministry funding acknowledgment
  - [x] Update “Impressum” link text

### `_toc.yml`

- [x] Update file references to translated filenames (if renaming files)
- [x] No direct text content to translate in this file

## Content Files

### Root Files

- [x] `index.md` - Main landing page
- [x] `README.md` - Repository description

### Präambel (Preamble) Section

- [x] `präambel/toc.md` - Section overview
- [x] `präambel/lernziele.md` - Learning objectives
- [x] `präambel/technische_voraussetzungen.md` - Technical requirements
- [x] `präambel/vorkenntnisse.md` - Prerequisites
- [x] `präambel/ablaufplan.md` - Workshop schedule/timeline

### Grundlagen (Fundamentals) Section

- [x] `grundlagen/einleitung.md` - Introduction
- [x] `grundlagen/dokumente.md` - Workshop materials/documents
- [x] `grundlagen/jupyter_book.md` - Why Jupyter Book?
- [x] `grundlagen/template.md` - Template explanation
- [x] `grundlagen/github.md` - GitHub settings

### Inhalte (Content) Section

- [x] `inhalte/einleitung.md` - Content creation introduction
- [x] `inhalte/setup.md` - Setup and configuration
- [x] `inhalte/markdown.md` - Markdown basics
- [x] `inhalte/jupyter_notebooks.ipynb` - Jupyter Notebooks integration

### Bonus Section

- [x] `bonus/einleitung.md` - Bonus introduction
- [x] `bonus/typographie.md` - Advanced typography
- [x] `bonus/ausführbares_markdown.md` - Executable Markdown
- [x] `bonus/jupyterquiz.ipynb` - Jupyter Quiz
- [x] `bonus/zenodo.md` - Zenodo publication

### Epilog Section

- [x] `epilog/toc.md` - Epilog overview
- [x] `epilog/literaturverzeichnis.md` - Bibliography
- [x] `epilog/autor_innen.md` - Authors
- [x] `epilog/impressum.md` - Legal notice/Imprint # NOTE: not to be translated

## Special Elements to Translate

### Custom Admonitions (CSS classes)
NOTE: Not to be translated here
- [x] `lernziele` - Learning objectives
- [x] `exercise` - Exercise
- [x] `solution` - Solution
- [x] `keypoint` - Key point
- [x] `hinweis` - Note/Hint
- [x] `zeitinfo` - Time information
- [x] `frage-feedback` - Question/Feedback
- [x] `citation-information` - Citation information

### Links and References

- [x] Update internal cross-references between files
- [ ] Update anchor links within documents
- [ ] Verify external links still work after translation
- [ ] Update any German-specific external links to English equivalents where available

## Technical Files (Consider Translation)

### Documentation

- [x] `LICENSE.md` - License information
- [x] `CITATION.cff` - Citation metadata
  - [x] Update `title` field
  - [x] Update `abstract` field
  - [x] Consider updating `url` to English version

### Python Files (Comments/Docstrings)

- [x] `quadriga/__init__.py` - Module documentation
- [x] `quadriga/colors.py` - Color configuration comments

## Post-Translation Tasks

### File Structure

- [x] Decide whether to rename German folder names (`präambel`, `grundlagen`, `inhalte`, `bonus`, `epilog`)
- [x] Update `_toc.yml` if folder/file names change
- [x] Update all internal links if file paths change

### Testing

- [ ] Build the book locally to check for broken links
- [ ] Verify all admonitions render correctly
- [ ] Test all interactive elements (if any)
- [ ] Check that bibliography still works
- [ ] Verify GitHub Actions still work

### GitHub Repository

- [ ] Update repository description
- [ ] Update repository topics/tags
- [ ] Consider creating English branch or separate repository
- [ ] Update GitHub Pages URL if needed

## Notes

- Some technical terms (like “Jupyter Book”, “GitHub”, “Markdown”) should remain in English
- Academic terms might have established English translations
- Consider your target audience when deciding on technical terminology
- Keep German abbreviations like “OER” but expand on first use if needed