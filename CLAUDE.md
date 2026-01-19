# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll static site generator blog for michaeljosephkramer.com. It uses Ruby/Bundler for dependency management and Jekyll's Liquid templating system.

## Common Commands

```bash
bundle install              # Install dependencies
bundle exec jekyll serve    # Local dev server with live reload (http://localhost:4000)
bundle exec jekyll build    # Build static site to _site/
```

## Architecture

**Template System**: Layouts in `_layouts/` extend hierarchically (default.html → post.html/page.html). Reusable components live in `_includes/` (head, header, footer). All templates use Jekyll's Liquid templating.

**Content**: Blog posts are Markdown files in `_posts/` following Jekyll's naming convention: `YYYY-MM-DD-title.md`. Each post has YAML front matter for metadata (title, date, layout).

**Styling**: Main stylesheet is `css/main.scss` with SCSS variables for colors/fonts. Syntax highlighting uses Rouge with the Vim theme (`css/vim.css`).

**Configuration**: `_config.yml` contains site metadata, Google Analytics ID, social accounts, permalink structure, and Kramdown markdown settings. Plugins (jekyll-sitemap, jekyll-seo-tag) are configured there as well.
