# Lecture Notes for Data 102

## Repository overview

Here are some relevant files in the repository:

- The content is in the directory called: `./content`. That is the directory where all Markdown and Notebook files should be put into.

- The Table of Contents file is at `_data/toc.yml`.

- The configuration file is at `_config.yml`.

- The `content/features` directory showcases a few features of the Jupyter Books tool which for now we'll leave in place until we're all familiar with them (like input/code hiding, etc).

## Making changes to the book

This repository uses a tool called [Jupyter Book](https://jupyter.org/jupyter-book) to build
the textbook. This should all happen *automatically* when new changes are made to anything
in the `content/` folder. Here are the steps to follow:

1. **Make sure you have the latest changes from this repository**. You can pull in the latest
   changes with:

   ```
   git pull upstream master
   ```
2. **Make changes to the textbook**. This is everything in the `content/` directory.
3. **Make a pull-request for these changes**. This will allow others to take a look at
   your proposed changes to the book.
4. **For bigger changes, demo the book within the PR**. If your changes are significant,
   you may want to demo what they'll look like before merging. To do this, click on
   `show all checks`, then the **`Details`** link under `demo_html`. This will take you
   to a CircleCI page for the PR. Click on **`Artifacts`**, and you'll see a list of HTML
   files. Click one and you'll preview the page using the content in that pull-request.
5. **Deploy the changes to the live textbook**. This is simply accomplished by merging
   the PR into the master branch. Whenever the master branch changes, we automatically
   re-build the book and push the latest versions to the live website. This is done
   [with this circleci script](./.circleci/config.yml)