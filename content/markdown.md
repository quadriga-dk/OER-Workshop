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


## Markup in Markdown – Authoring Content
Now that you have a file you should add some content to it. Let's explore some parts of basic and advanced Markdown syntax useful for authoring OERs.

### Headings

### Typography

### Code / raw text

### Links

### Admonitions

### Images and Figures

### Excercise

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