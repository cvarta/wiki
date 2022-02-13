# Chris Wikii build with Mkdocs
### Intro
MkDocs is a fast and simple static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

## MkDocs Installation
MkDocs Installation Guide: https://www.mkdocs.org

###  PiP Installation Methode
* Create Virtual environments: https://realpython.com/python-virtual-environments-a-primer/
* Install mkdocs
* Install mkdocs-material theme
* Install mkdocs-material extensions for emojii support

## Setup MkDocs

#### Create virtual environment
* Install virtualenv: ` pip install virtualenv`
* Create env dir: `mkdir python-virtual-environments && cd python-virtual-environments`
* Create virtual env: `python3 -m venv .venv`

#### Updating virtual environment
* To list currently installed package in your environment
  * activate environment
  * run: `pip3 list`
* To check if updates are available for installed packages
  * run: `pip3 list -- outdated`
* To upgrade all outdated packages
  * run: `pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U`

#### Write new requirements.txt file
* To write / update requirements.txt with list of installed / required packages:
  * run: `pip freeze > requirements.txt`

#### Install MkDocs
* Shortcut: `pip3 install -r requirements.txt`
* Manual Install:
    * `pip3 install mkdocs`
    * `pip3 install mkdocs-material`
    * `pip3 install mkdocs-material-extensions`
* Activate virtual environment:
  ```
  $ source env/bin/activate
  (env) $
  ```

## Setup Theme MkDocs-material
Getting Started: https://squidfunk.github.io/mkdocs-material/getting-started/

Setup Navigation: https://squidfunk.github.io/mkdocs-material/setup/setting-up-navigation/

Code: https://github.com/squidfunk/mkdocs-material


## Setup mkdocs-material-markdown_extensions
https://github.com/facelessuser/mkdocs-material-extensions

add following config to mkdocs.yml

```
markdown_extensions:
  - pymdownx.emoji:
      emoji_index: !!python/name:materialx.emoji.twemoji
      emoji_generator: !!python/name:materialx.emoji.to_svg
```

# Markdown Formatting Help
Images in Markdown:

https://medium.com/markdown-monster-blog/getting-images-into-markdown-documents-and-weblog-posts-with-markdown-monster-9ec6f353d8ec

Folding content in Markdown:
```
<details>
<summary>Click to expand</summary>

whatever

</details>
```

Emojis in Markdown: https://github.com/markdown-templates/markdown-emojis