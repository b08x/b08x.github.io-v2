# PROJECT KNOWLEDGE BASE

**Generated:** 2026-02-17
**Branch:** development

## OVERVIEW

Jekyll-based portfolio theme (portfolYOU). Static site generator in Ruby with HTML/SCSS. Generates GitHub Pages-compatible portfolio.

## STRUCTURE

```
./
├── _config.yml          # Jekyll configuration
├── Gemfile              # Ruby dependencies
├── _elements/           # 21 HTML element partials (01-21)
├── _includes/           # Reusable components (navbar, footer, blog, projects)
├── _layouts/            # Page layouts (default, element, page, post)
├── _sass/               # SCSS stylesheets (15 files, theming)
├── pages/               # Top-level pages (blog, projects, about, index, tags)
├── _data/               # YAML data (skills, timeline, social-media)
├── _projects/           # Project markdown files
├── documentation/       # Theme docs (partials, features, customization)
└── test/                # Jekyll test config
```

## WHERE TO LOOK

| Task | Location | Notes |
|------|----------|-------|
| Add element | `_elements/` | Numbered 01-21, follows naming |
| Add page | `pages/` | Add .md or .html |
| Modify layout | `_layouts/` | default, element, page, post |
| Styling | `_sass/` | Theming in _theme*.scss |
| Config | `_config.yml` | Site-wide settings |
| Skills data | `_data/other-skills.yml`, `_data/programming-skills.yml` | YAML lists |
| Timeline | `_data/timeline/*.yml` | Event entries |

## CODE MAP

| Symbol | Type | Role |
|--------|------|------|
| default.html | Layout | Base layout wrapper |
| element.html | Layout | Element showcase page |
| navbar.html | Include | Navigation |
| footer.html | Include | Site footer |
| project-card.html | Include | Project display |
| post-card.html | Include | Blog post display |

## CONVENTIONS

- **Elements**: Named `01-headers.html`, `02-emphasis.html`, etc.
- **Data files**: YAML format in `_data/`
- **Projects**: Markdown in `_projects/` with frontmatter
- **Skills**: Split into `programming-skills.yml` and `other-skills.yml`
- **Timeline**: Year-based YAML files in `_data/timeline/`

## ANTI-PATTERNS (THIS PROJECT)

- Don't modify `portfolyou-jekyll-theme.gemspec` directly
- Don't add custom Ruby code (theme is meant to be configurable via data files)
- Avoid editing generated output in `_site/` - rebuild instead

## COMMANDS

```bash
jekyll serve          # Local dev server
jekyll build          # Production build
bundle exec jekyll    # With Bundler
```

## NOTES

- GitHub Pages compatible theme
- Supports dark mode via `_sass/_theme-dark.scss`
- Elements showcase at `/elements.html`
- Uses GitHub Flavored Markdown
