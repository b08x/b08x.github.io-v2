# syncopated notes

A personal portfolio built with [portfolYOU](https://github.com/yousinix/portfolYOU), a Jekyll theme designed for GitHub Pages.

## Overview

Static portfolio site generating via Jekyll. Content managed through YAML data files. Supports blog posts, project showcases, skills display, and timeline features.

## Structure

```
├── _config.yml          # Site configuration
├── _data/               # YAML data (skills, timeline, social links)
├── _includes/           # Reusable components
├── _layouts/            # Page layouts
├── _posts/              # Blog posts (Markdown)
├── _projects/           # Project entries (Markdown)
├── _sass/               # Stylesheets (SCSS)
├── pages/               # Static pages
└── assets/              # CSS, JS, images
```

## Quick Start

```bash
# Install dependencies
bundle install

# Local development server
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

Access at `http://localhost:4000`.

## Configuration

Edit `_config.yml`:

| Setting | Description |
|---------|-------------|
| `title` | Site title |
| `description` | Site subtitle |
| `baseurl` | Subdirectory (empty for root) |
| `author` | Profile info, social links |
| `plugins` | Jekyll plugins enabled |

## Content

### Posts
Create Markdown files in `_posts/`:
```
---
layout: post
title: "Post Title"
tags: [tag1, tag2]
---
```

### Projects
Add YAML or Markdown to `_projects/`:
```yaml
name: Project Name
description: Brief description
url: https://github.com/user/repo
```

### Skills
Edit `_data/programming-skills.yml` and `_data/other-skills.yml`.

### Timeline
Add entries to `_data/timeline/*.yml`.

## Customization

### Theming
Edit `_sass/_variables.scss` for colors. Dark mode available via `_sass/_theme-dark.scss`.

### Layouts
- `default` — Base layout
- `page` — Static pages
- `post` — Blog posts
- `element` — Element showcase

## Deployment

Push to GitHub Pages branch. GitHub automatically builds via Jekyll.

## License

MIT License © 2019 Youssef Raafat
