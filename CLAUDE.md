# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

GitHub Pages site for tilthouse.github.io, using Jekyll with the Slate theme. Content is authored in HTML/Markdown and automatically built and deployed by GitHub Pages on push to `main`.

## Build & Development

```bash
# Local development (requires Ruby and Bundler)
bundle install
bundle exec jekyll serve    # serves at http://localhost:4000

# Build without serving
bundle exec jekyll build    # output goes to _site/
```

Note: There is no Gemfile yet — to run locally, create one with `github-pages` gem.

## Architecture

- `_config.yml` — Jekyll configuration (theme: jekyll-theme-slate)
- `index.html` — Site homepage (currently bare "Hello World")
- Content files (`.md`, `.html`) in the root are processed by Jekyll
- Jekyll layouts/assets come from the remote Slate theme gem — override by creating matching files locally (e.g., `_layouts/default.html`)
