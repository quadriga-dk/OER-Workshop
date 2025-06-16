# OER-Workshop Translation Checklist

## Core Configuration Files

### `_config.yml`

- [ ] Translate `title: "OER-Workshop"` to English
- [ ] Update `author` field if needed
- [ ] Translate `copyright` field
- [ ] Update `extra_footer` section:
  - [ ] Translate Creative Commons license text
  - [ ] Translate QUADRIGA project description
  - [ ] Translate ministry funding acknowledgment
  - [ ] Update “Impressum” link text

### `_toc.yml`

- [x] Update file references to translated filenames (if renaming files)
- [x] No direct text content to translate in this file

## Content Files

### Root Files

- [ ] `index.md` - Main landing page
- [ ] `README.md` - Repository description

### Präambel (Preamble) Section

- [ ] `präambel/toc.md` - Section overview
- [ ] `präambel/lernziele.md` - Learning objectives
- [ ] `präambel/technische_voraussetzungen.md` - Technical requirements
- [ ] `präambel/vorkenntnisse.md` - Prerequisites
- [ ] `präambel/ablaufplan.md` - Workshop schedule/timeline

### Grundlagen (Fundamentals) Section

- [ ] `grundlagen/einleitung.md` - Introduction
- [ ] `grundlagen/dokumente.md` - Workshop materials/documents
- [ ] `grundlagen/jupyter_book.md` - Why Jupyter Book?
- [ ] `grundlagen/template.md` - Template explanation
- [ ] `grundlagen/github.md` - GitHub settings

### Inhalte (Content) Section

- [ ] `inhalte/einleitung.md` - Content creation introduction
- [ ] `inhalte/setup.md` - Setup and configuration
- [ ] `inhalte/markdown.md` - Markdown basics
- [ ] `inhalte/jupyter_notebooks.ipynb` - Jupyter Notebooks integration

### Bonus Section

- [ ] `bonus/einleitung.md` - Bonus introduction
- [ ] `bonus/typographie.md` - Advanced typography
- [ ] `bonus/ausführbares_markdown.md` - Executable Markdown
- [ ] `bonus/jupyterquiz.ipynb` - Jupyter Quiz
- [ ] `bonus/zenodo.md` - Zenodo publication

### Epilog Section

- [ ] `epilog/toc.md` - Epilog overview
- [ ] `epilog/literaturverzeichnis.md` - Bibliography
- [ ] `epilog/autor_innen.md` - Authors
- [ ] `epilog/impressum.md` - Legal notice/Imprint

## Special Elements to Translate

### Custom Admonitions (CSS classes)

- [ ] `lernziele` - Learning objectives
- [ ] `exercise` - Exercise
- [ ] `solution` - Solution
- [ ] `keypoint` - Key point
- [ ] `hinweis` - Note/Hint
- [ ] `zeitinfo` - Time information
- [ ] `frage-feedback` - Question/Feedback
- [ ] `citation-information` - Citation information

### Links and References

- [ ] Update internal cross-references between files
- [ ] Update anchor links within documents
- [ ] Verify external links still work after translation
- [ ] Update any German-specific external links to English equivalents where available

## Technical Files (Consider Translation)

### Documentation

- [ ] `LICENSE.md` - License information
- [ ] `CITATION.cff` - Citation metadata
  - [ ] Update `title` field
  - [ ] Update `abstract` field
  - [ ] Consider updating `url` to English version

### Python Files (Comments/Docstrings)

- [ ] `quadriga/__init__.py` - Module documentation
- [ ] `quadriga/colors.py` - Color configuration comments

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