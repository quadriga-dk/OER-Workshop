# Template

For use in the workshop, a <a href="https://quadriga-dk.github.io/OER-Workshop-Template" target="_blank" class="external-link">Template</a> (<a href="https://github.com/quadriga-dk/OER-Workshop-Template" target="_blank" class="external-link">GitHub</a>) has been developed that can be used to get started with Jupyter Book. This is based on the <a href="https://quadriga-dk.github.io/Book_Template" target="_blank" class="external-link">QUADRIGA-Template</a> (<a href="https://github.com/quadriga-dk/Book_Template" target="_blank" class="external-link">GitHub</a>), with many QUADRIGA-specific features removed.

For version control and collaborative work on content, we use Git and the so-called Git Forge GitHub, which not only stores the Git repository and manages access rights to it, but also provides an issue system, a CI/CD system, and a web host.

The template contains various folders and files, which are discussed in this section.

## Jupyter Book Files
Jupyter Book consists of two configuration files (`_config.yml` and `_toc.yml`), the associated content files (`.md`, `.ipynb`, image files, ...) as well as the `.css` and `.js` files necessary for website display situated in the `_static` folder. The `references.bib` file is used for citing and referencing literature.

The content files are sorted into the `preamble/` and `epilog/` folders for text, and `assets/` for image and other content files. This sorting is not required by Jupyter Book, but is useful for better overview during OER creation. We recommend collecting content files for a chapter in one folder.

The entry page (in the template `index.md`) as well as the website structure are defined in the table of contents `_toc.yml`. Files must be listed in the table of contents to be displayed on the website compiled by Jupyter Book.

The `_config.yml` file represents the configuration of Jupyter Book. Large parts of the file can be directly adopted – the parts that need to be adapted for this workshop are discussed in the [next chapter](/content/setup.md).

## Python Files
To use Jupyter Book on your own computer, it must first be installed. For this you need Python – preferably in the version specified in `.python-version` – and then you need to install the packages specified in the `requirements.txt` file.

```{admonition} Important
:class: important
For the workshop, you do not need to install Jupyter Book on your own computer. You can use the GitHub repository directly and work with it in the browser.
```

````{admonition} Instructions for Local Installation
:class: hinweis, dropdown

If you want a local installation, this works with the following commands:

```bash
$ python3.13 -m venv .venv            # create a new virtual environment

# On Unix/macOS:
$ source .venv/bin/activate           # activate the environment

# Or on Windows (cmd.exe):
> .venv\Scripts\activate              # activate the environment

$ pip install -r requirements.txt     # install the required Python packages
```
If you want to use Jupyter Book then, make sure you are in the root folder of your Jupyter Book project and that the appropriate virtual environment is activated. Then use the following commands:

```bash
# Compiles the website and saves the result in the _build/html/ folder.
$ jupyter book build .

# Cleans the _build folder to allow the book to be completely rebuilt.
# Does only need to be run if there are problems for example with the page navigation.
$ jupyter book clean . --all
```
````

## Git Files
The `.gitignore` file defines which files should not be tracked and versioned in version control. This particularly affects the Jupyter Book result folder `_build/` as well as various cache files that are created by running Python code. The file does not need to be changed in the workshop.

All version control takes place in the `.git/` folder, which is why the contents of this folder should _never_ be changed manually.

## GitHub Files
In the `.github/` folder, the so-called GitHub Action `deploy-book-python-only.yml` is defined in the `.github/workflows/` folder. This executes various commands when saving changes to GitHub (in the so-called `main` branch) to compile the Jupyter Book and provide the result via GitHub Pages. The contents of the file do not need to be adjusted in the workshop.

The `README.md` file contains a brief description of the repository contents and is prominently displayed on GitHub.

## Additional Files

The `LICENSE.md` file contains information about the licenses for the contents and the code of the template.

The `CITATION.cff` file defines metadata for citing the Git repository. It is used by GitHub and Zenodo to generate citation information.
