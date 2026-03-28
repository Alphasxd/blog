# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
bundle install                # install Ruby dependencies
bundle exec jekyll serve      # local dev server at http://127.0.0.1:4000 with live rebuild
bundle exec jekyll build      # production build to _site/
```

There is no test suite. `bundle exec jekyll build` is the regression check before any PR.

## Architecture

This is a Jekyll blog using the `moving` theme (defined in `moving.gemspec`). The theme is self-contained in this repo rather than loaded from a gem registry.

**Request/render flow:** Every page uses `_layouts/default.html` as the base (includes `_includes/head.html` and `_includes/footer.html`). Posts use `_layouts/post.html` (which extends `default`), and automatically include: a MathJax script, a table of contents via `_includes/toc.html`, a CC license notice, prev/next navigation, and Giscus comments via `_includes/giscus.html`.

**Key files:**
- `_config.yml` — site metadata, author info, social links, plugin list, and `moving:` theme options (avatar, date format, back button text)
- `_posts/` — content files named `YYYY-MM-DD-slug.md`
- `_sass/moving/` — theme styles split into `_base.scss` and `_layout.scss`, imported by `assets/css/main.scss`
- `_includes/giscus.html` — comment system; changes affect all post pages
- `_includes/head.html` — analytics and page metadata; changes are site-wide

## Conventions

- Always use `relative_url` filter for internal links and asset paths (e.g. `{{ "/path" | relative_url }}`)
- 2-space indentation in HTML, Liquid, SCSS, and YAML
- Post filenames: lowercase and hyphenated
- Front matter: keep it minimal and explicit
- Commit style: short imperative subjects like `fix: ...` or `update: ...`
