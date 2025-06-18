# Setup and Configuration of Jupyter Book

In this section you will create a new repository in GitHub based on the OER-Workshop-Template and configure it. The result is a Website hosted on GitHub Pages that reflects the state of the template but belonging to your GitHub account. Then you will change `_config.yml` and `CITATION.cff` to personalize the repository and make it your own.

In the following sections you will add content to your repository and customize it further.


## Creating a New Repository from the Template

```{figure} /assets/content/use_this_template_button.png
---
align: right
scale: 60%
name: fig-use-this-template
---
"Use this template" button
```
Open the <a href="https://github.com/quadriga-dk/OER-Workshop-Template/" target="_blank" class="external-link">OER-Workshop-Template</a> on GitHub and click the "Use this template" button ({numref}`fig-use-this-template`) in the upper right corner. Select "Create a new repository".

On the next page, name your OER by filling out the field "Repository name". If you don't have anything in mind, use `my-oer`.

The repository need to be public, which is the default setting.

## Setting Up GitHub Pages
```{figure} /assets/content/pages_source_actions.png
---
align: right
scale: 40%
name: fig-pages-setup
---
Use GitHub Actions as<br>
the source for GitHub Pages
```
After creating the repository, you will be redirected to the new repository. In the upper right corner, click on "Settings". On the left side, click on "Pages". Under "Source" select "GitHub Actions" (see {numref}`fig-pages-setup`).

```{figure} /assets/content/github_pages_url.png
---
align: right
scale: 40%
name: fig-pages-url
---
Automatically fill the<br>
"Website" field with the URL to<br>
your GitHub Pages
```

Return to the main page of your repository via the "Code" tab in the top left. In the right sidebar you can edit the "About" section by clicking on the gear icon. Select the checkbox "Use your GitHub Pages website" (see {numref}`fig-pages-url`). This will prefill the "Website" field with the URL to your GitHub Pages.

## Edit `README.md`

```{figure} /assets/content/code_tab_readme_file.png
---
align: right
scale: 40%
name: fig-readme-file
---
`README.md` file in the<br>
"Code" tab
```
In the "Code" tab, click on the `README.md` file to open it (see {numref}`fig-readme-file`). In the file view, you can see the repository's folder structure on the left side while the currently selected file fills the rest of the page.

The file view has a toolbar at the top in which you can change the display mode on the left side and download or edit the file on the right side (see {numref}`fig-file-view-toolbar`).
```{figure} /assets/content/file_view_toolbar.png
---
align: center
name: fig-file-view-toolbar
---
Toolbar in the file view
```
Click on the pencil icon to edit the file. Change the contents to the following:

```markdown
# My OER
This is my first OER using the QUADRIGA OER Workshop Template.

```

```{figure} /assets/content/cancel_commit_changes.png
---
align: right
scale: 40%
name: fig-cancel-commit-changes
---
Cancel or commit changes
```

You can alter this file as you wish. When you are done, commit the changes by clicking on "Commit changes" in the top right corner (see {numref}`fig-cancel-commit-changes`). 

This opens a dialog where you can enter a commit message (see {numref}`fig-commit-message-dialog`). A commit message is a short description of the changes you made. It is good practice to write a meaningful commit message that describes what you changed and why. For example, "Update the README to make it my own". You can also add a longer description.

In this workshop, we will always use the "Commit directly to the `main` branch" option, which is the default setting. Branches allow for parallel development in a repository, but we will not use them in this workshop. Click on "Commit changes" to save your changes.

```{figure} /assets/content/commit_message_dialog.png
---
align: center
name: fig-commit-message-dialog
---
Commit message dialog
```

## GitHub Action
The commit to `main` automatically triggers the GitHub Action defined in `.github/workflows/deploy-book-python-only.yml` which is predefined in the template. This Action builds the Jupyter Book and deploys it to GitHub Pages. You can see the progress and possible errors of the Action by clicking on the "Actions" tab in the top menu of your repository.

In this workshop, we will not go into detail about GitHub Actions, but you can find more information in the <a href="https://docs.github.com/en/actions" target="_blank" class="external-link">GitHub Actions documentation</a>.


## Change the metadata
Now you can change the metadata of your repository to make it your own. Open the `_config.yml` file in the "Code" tab and edit it to fit your OER

## The Result

Now you can click on the URL in the "About" section of the "Code" tab. This will take you to your newly created GitHub Pages site.
