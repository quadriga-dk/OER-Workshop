# Why Jupyter Book?

## Proprietary and Open Formats for OER Creation
Open Educational Resources should ideally be editable and usable with free software and should be written in open standard formats whenever possible. Simple text files provide a particularly good solution for this purpose.

While classic text files (`.txt`) can certainly be used, <a href="https://en.wikipedia.org/wiki/Markup_language" target="_blank" class="external-link">markup languages</a> such as HTML (`.html`) or <a href="https://daringfireball.net/projects/markdown/" target="_blank" class="external-link">Markdown (`.md`)</a> are well-suited for structurally and typographically preparing content for reading. The markup languages mentioned here are particularly suitable for an end product that is intended to be consumed in a browser – as a website.

Through software like <a href="https://pandoc.org/index.html" target="_blank" class="external-link">Pandoc</a>, these text-based formats can also be transformed into various other file formats such as `.pdf` or `.docx`.

## Advantages of So-Called _Static Site Generators_ for OER Development
Traditional website hosting has certain minimum costs that steadily increase with heavy usage. This is especially true for sites that must perform database-based calculations per user access to present content. If the customizability gained through this is not necessary, a simpler model can be used.

A so-called _static site generator_ (SSG) compiles source files (e.g., Markdown files) into HTML files and structures them together with all necessary files such as images, `.css` and `.js` files into a folder structure that can then be hosted very affordably (in the case of using GitHub Pages, for example, practically free of charge). Traditional SSGs convert source files into a website structure, but other output formats are also conceivable.

The compilation only needs to be performed once when the source files are changed, not for each user / access.

## The Jupyter Ecosystem
In recent years, the <a href="https://jupyter.org" target="_blank" class="external-link">Jupyter project</a> has emerged as _the_ ecosystem in the field of Data Science and Machine Learning.

This is particularly due to the so-called Jupyter Notebooks (`.ipynb`), which allow text (formatted in Markdown) and executable program code as well as the code's results to be presented in combination. Jupyter Notebooks are text files in JSON format (`.json`). The "magic" occurs when a special editor (e.g., the Jupyter Notebook editor by the same name or more powerful development environments like Jupyter Lab or Visual Studio Code) reads the `.ipynb` file and starts a so-called kernel. A kernel is a program that can execute program code in a programming language like Python and transmit the calculation results to the editor so that it can incorporate them back into the `.ipynb` file. This allows a snippet of program code (in Jupyter Notebooks, these are also called cells or 'code cells') to be executed and the result to be displayed directly below the code that produced it.

## Jupyter Book
Jupyter Book is a SSG that not only understands Markdown and HTML files as input file formats – as is usually the case – but can also natively execute Jupyter Notebooks (`.ipynb`) and include them as results in the website compilation. This allows notebooks to be used directly and combined with Markdown files to create content.

In addition, Jupyter Book offers functionalities to open content from the resulting website in an interactive programming environment such as Binder, Colab, or a Jupyter Hub and continue working directly with the content. The transition from reading to editing is therefore seamless.