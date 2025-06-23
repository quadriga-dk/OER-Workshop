# Markdown

In this section, you will create a new Markdown file and add some content to it. Then you will configure Jupyter Book to include this file in the final output. Afterwards, you will add more content while learning different elements of the Markdown syntax.

## Creating a New Markdown File

Theoretically, you can create a file containing content anywhere in the repository. We recommend that you create folders to represent the structure of your content and place the content files within these folders. For this example, we will create a new file in a folder called `trust`.

```{admonition} Caution
:class: caution
Git does not track empty folders. If you want to create a folder in your repository, you need to create at least one file in it. This can be an empty file, but it must exist.
```

```{figure} /assets/content/add_new_file.png
---
align: right
scale: 60%
name: fig-add-new-file
---
"Add file" button in the "Code" tab
```
To create a new file, click the button "Add file" and then on "Create new file" (see {numref}`fig-add-new-file`). This opens an editor where you can enter a filename.

The filename can contain forward slashes (`/`) to denote a folder structure. For the workshop, use the filename `trust/what_is_trust.md`. This means that you will create a new folder called `trust` and inside it a file called `what_is_trust.md` (see {numref}`fig-filename-filled-out`).
```{figure} /assets/content/filename_filled_out.png
---
align: center
scale: 60%
name: fig-filename-filled-out
---
"Filename" set to `trust/what_is_trust.md`
```

Now add a title to the page. In Markdown, titles are created by using a hash (`#`) followed by a space and the title text. Add the following line to the file:

```markdown
# What is Trust?
```
The result should look like this in the editor:

```{figure} /assets/content/minimal_markdown_file.png
---
align: center
name: fig-minimal-markdown-file
---
Minimal Markdown file with a title
```
Now commit your changes, add a commit message and try to locate the new file in the "Code" tab of your repository. 

```{admonition} Caution
:class: caution
You need to add a title to the markdown file by using a heading (e.g. `# What is Trust?`) in your Markdown file. Otherwise, Jupyter Book does not correctly add the files content to the result and the table of contents.

The first `#`-heading in the file will be used as the title of the page and in the table of contents on the resulting website.
```

## Configuring Jupyter Book to Include the Markdown File
If you look at the resulting website, you will see that the new file is not included in the navigation. To tell Jupyter Book to include the file, you need to edit the `_toc.yml` file in the root of your repository. This file defines the table of contents for your book.

Currently, the `_toc.yml` file looks like this:

```yaml
# Table of contents
# Learn more at https://jupyterbook.org/customize/toc.html

format: jb-book
root: index.md
options:
  numbered: 3
chapters:
  - file: präambel/toc.md
    sections:
      - file: präambel/lernziele.md
      - file: präambel/technische_voraussetzungen.md
      - file: präambel/vorkenntnisse.md
  - file: epilog/toc.md
    sections:
      - file: epilog/literaturverzeichnis.md
      - file: epilog/autor_innen.md
      - file: epilog/impressum.md
```

Add a new chapter entry for your new file. Commit the change, wait for the action to finish, and then check the resulting website.

```{admonition} Caution
:class: caution
YAML files are sensitive to indentation. Make sure you use multiples of two spaces for indentation and don't use tabs.

When editing the file follow the structure of the existing entries.
```

````{admonition} Exercise: Chapters and Sections
:class: exercise

Create a chapter with at least one section. The first section in the chapter should be the file `trust/what_is_trust.md`.

```{admonition} Solution
:class: solution, dropdown

1. Create a new file `introduction.md` in the folder `trust` with at least a heading as content.
2. Add a new entry for `introduction.md` in the `_toc.yml` file.
3. Move the entry for `what_is_trust.md` to be a section of `trust/introduction.md`.

```
````

(markdown:markup)=
## Markup in Markdown – Authoring Content
Now that you have a file you should add some content to it. Let's explore some parts of basic and advanced Markdown syntax useful for authoring OERs.

### Headings

Markdown files can be structured using headings. There are six levels of headings, corresponding to the number of hash symbols (`#`) used.

```markdown
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

```

You should only use consecutive headings, meaning that you should not skip levels. For example, you should not use a level 3 heading directly after a level 1 heading. Instead, you should use a level 2 heading in between.

### Typography

You can use Markdown to format text in various ways:
```markdown
*Italic text* is created with asterisks or underscores.

**Bold text** is created with double asterisks or underscores.

`Inline code / inline raw text` is created with backticks.
```

Other formatting options include:
```markdown
- Lists can be created with asterisks, plus signs, or hyphens.

1. Numbered lists can be created with numbers followed by a period.

- [ ] Checkboxes can be created with a hyphen followed by square brackets.

- Blockquotes can be created with a greater-than sign (`>`).
```

### Code / raw text
If you don't want to display code or raw text inline, you can use a code block. A code block is created by using three (or more) backticks (```) before and after the code.

The number of backticks should match, and you can nest code blocks in code blocks with a higher number of backticks.

You can specify the (programming) language for specific syntax highlighting by adding it after the opening backticks.

The code block: 
````markdown
```python
print(2+2)
```
````
produces the output:
```python
print(2+2)
```

### Links
Markdown supports HTML and therefore also HTML-style links via an `<a>`-tag. However, it is more common to use the Markdown syntax for links, which is:

```markdown
[Link text](https://example.com)
```
This creates a clickable link with the text "Link text" that points to `https://example.com`.

If you want to specify a link that opens in a new tab, you need to use the HTML syntax:

```html
<a href="https://example.com" target="_blank">Link text</a>
```

### Admonitions
Admonitions are an addition to standard Markdown specified by Jupyter Book. QUADRIGA developed a set of admonitions specifically for the use in OERs.

Admonitions are highlighted boxes that have an icon, a title, and content. They are defined by using code blocks with a specific syntax. The syntax is:

````markdown
```{admonition} Title
:class: tip
Content of the admonition.
```
````

Visit the page on <a href="https://quadriga-dk.github.io/Book_Template/formatierung/admonitions.html" target="_blank" class="external-link">QUADRIGA Admonitions</a> in the QUADRIGA template for inspiration.

### Images and Figures

There are two ways to include images in Markdown files. The first is the standard Markdown syntax:

```markdown
![Alt text](path/to/image.png)
```
The second is the Jupyter Book syntax, which allows for more options like captions and alignment:

````markdown
```{figure} path/to/image.png
---
name: fig-image-name
align: center
---
Caption for the image.
```
````

If you use a `{figure}` directive, you can reference the figure in your text using `{numref}`. For example, if you have a figure with the name `fig-image-name`, you can reference it like this:

```markdown
See {numref}`fig-image-name` for an example image.
```

You've already seen examples of figures and references in the previous pages of this book.

### Exercise

````{admonition} Exercise: Markdown Syntax
:class: exercise

Add content to your Markdown file using at least two different Markdown syntax elements.

```{admonition} Solution
:class: solution, dropdown
See [What is Trust?](/results/what_is_trust.md) for an example solution.
```

````

## Result

You now have a Markdown file with some content in it and it is included in your Jupyter Book. You can compare your result with the [sample solution](/results/what_is_trust.md).

In the next section, you will learn how to use Jupyter Notebooks to author content.