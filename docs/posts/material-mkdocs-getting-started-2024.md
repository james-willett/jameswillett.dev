---
date: 2024-09-03
authors: [james]
description: >
  This is the script for the YouTube video that gives an overview
  tutorial of Material for MkDocs
categories:
  - YouTube Videos
  - Material for MkDocs
---

# Getting Started with Material for MkDocs - 2024 Edition

## Video Status

!!! info

    This is the script for the 2024 edition of the "Getting Started with Material for MkDocs" YouTube video.<br/><br/>
    **Current Status**: Reviewing Script<br/>
    **Last Updated**: 03-Sept-2024

## 1. Intro

!!! example "Section Metadata"

    **:material-video-box: Recording Type**: Narration

    **:material-text-box: Description**: Introduction to the video, outling the features we will add to our MkDocs Material website

    **:octicons-git-branch-16: Demo Branch**: `N/A`

- Welcome back to the channel! In today’s video we’re diving into Material for MkDocs, the ultimate framework for creating stunning, interactive documentation sites.
- In this tutorial, we’ll be creating a new documentation portal completely from scratch, and then hosting that on the web for free using GitHub pages.

??? tip "B-roll ideas"

    Animated screencasts or screenshots of the completed site showing all the features below

- Along the way, I’ll show you just a handful of the awesome features that Material for MkDocs comes bundled with, such as:

    - Setting a dynamic colour scheme
    - Adding a splash of personality with emojis, icons and logos to make your content visually appealing
    - How to create custom code blocks that adjust based on the programming language specified
    - How to better organise your content using Tabs
    - How to empathize parts of your content using admonitions - also known as callouts
    - And how to bring your ideas to life with statically rendered diagrams directly in your docs

- If that sounds like something you'd be interested in, then breathe in, breathe out, and let’s explore this together 🙂

---

## 2. Prereqs

!!! example "Section Metadata"

    **:material-video-box: Recording Type**: Narration

    **:material-text-box: Description**: Cover off the prerequisites that the user needs to have installed to follow along with the tutorial

    **:octicons-git-branch-16: Demo Branch**: `N/A`

- Before we start, let’s go over the prerequistes you’ll need to have installed if you want to follow along with this tutorial

??? tip "B-roll ideas"
    Mac and Windows logos flash on screen

- Firstly, do be aware that i’ll be conducting this tutorial on a Mac. If you’re following on Windows then some of the commands we type into the terminal will be ever so slightly different… but I’ll try to call those out.

??? tip "B-roll ideas"
    B-ROLL: list of these prereqs appear to left or right of me

- So we’re going to be using the __PYTHON__ version of MkDocs in this tutorial, and you’ll need to have PYTHON 3 installed. I’ll be using version `3.12.4` in this video, so either that or a later version should work fine.
- We’ll be using the Python package manager called PIP to install the required dependencies… but if you are running Python 3.4 or later then PIP is included anyway by default… otherwise if you’re using an earlier version, you might need to install PIP.
- Now, to follow along with the coding, it’s helpful if you have an IDE installed, and I’ll be using Visual Studio Code in this video.
- And finally, we’ll be publishing our documentation portal on GITHUB PAGES… so you’ll need to have an account on [GitHub](http://github.com) and ideally have git installed and setup to work from the command line as well.

And that’s all we should need. So let’s jump over to a terminal and get started!

---

## 3. Initial Installation

!!! example "Section Metadata"

    **:material-video-box: Recording Type**: Screencast

    **:material-text-box: Description**: In this section we go over creating the Python virtual environment and creating a vanilla MkDocs site

    **:octicons-git-branch-16: Demo Branch**: `1_InitialInstallation`

- Open a terminal in the folder that you want to create the project in
- Do `which python` to show my Python is aliased to `python3`
- Do `which python3` to show my Python is installed with Homebrew
    - Mention if you are running on Windows you can do **`where python` instead**
- Virtual environment setup with `python -m venv venv`
- `source venv/bin/activate` to activate virtual environment
- Check pip version `pip --version`
- Install mkdocs material - `pip install mkdocs-material`
- Open Visual studio code in this folder with `vscode .`
- Open a terminal within VS code and create the new site `mkdocs new .`
- Add basic `mkdocs.yml` configuration:

```yaml title="mkdocs.yml"
site_name: My MkDocs Material Documentation
site_url: https://sitename.example
theme:
  name: material
```

- Do `mkdocs serve` to launch the site
- Check the site at [http://localhost:8000](http://localhost:8000)

---

## 4. Add Yaml Schema Validation

!!! example "Section Metadata"

    **:material-video-box: Recording Type**: Screencast

    **:material-text-box: Description**: Add MkDocs Material Yaml Schema Validation

    **:octicons-git-branch-16: Demo Branch**: `N/A`

- Explain that to activate most of the useful features in MkDocs Material, we need to make a few changes to the `mkdocs.yml` file… making these changes is much easier with the help of YAML schema validation.
- Install the `Yaml` plugin within Extensions
    - Plugin can also be found here [https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
- In VsCode open `settings.json`. You can open this by clicking on settings in the bottom left gear icon, then clicking the document icon in the top right.
- Add the following at the bottom:

```json title="settings.json"
  "yaml.schemas": {
    "https://squidfunk.github.io/mkdocs-material/schema.json": "mkdocs.yml"
  },
  "yaml.customTags": [
    "!ENV scalar",
    "!ENV sequence",
    "!relative scalar",
    "tag:yaml.org,2002:python/name:material.extensions.emoji.to_svg",
    "tag:yaml.org,2002:python/name:material.extensions.emoji.twemoji",
    "tag:yaml.org,2002:python/name:pymdownx.superfences.fence_code_format"
  ]
```

- Show the `mkdocs.yml` file and how we now get popups when we mouse over elements

---

## 5. Adjust Color Scheme

!!! example "Section Metadata"

    **:material-video-box: Recording Type**: Screencast

    **:material-text-box: Description**: Setup Light and Dark mode toggle within MkDocs, and change the colour scheme

    **:octicons-git-branch-16: Demo Branch**: `2_AdjustColor`


DONE TO HERE!!!

## 6. Adjust Font

## 7. Reminder to Like and Subscribe

!!! example "Section Metadata"

    **:material-video-box: Recording Type**: Narration

    **:material-text-box: Description**: remind viewers to like and subscribe to the channel

    **:octicons-git-branch-16: Demo Branch**: `N/A`

- Before we go on, if you’re finding this video helpful, please hit the like button down below, and subscribe to the channel for more videos just like this.
- OK. Let’s carry on setting up our MkDocs Material site!
