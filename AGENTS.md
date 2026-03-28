# Repository Guidelines

## Project Structure & Module Organization
This repository is a Jekyll blog based on the `moving` theme. Site configuration lives in `_config.yml`. Posts are stored in `_posts/` using the `YYYY-MM-DD-slug.md` pattern. Shared templates are in `_layouts/` and reusable partials are in `_includes/`. Theme styles are split between `assets/css/main.scss` and `_sass/moving/`. Top-level pages such as `index.md` and `about.md` provide page entry points.

## Build, Test, and Development Commands
Run `bundle install` to install Ruby dependencies. Use `bundle exec jekyll serve` for local development with live rebuilds at `http://127.0.0.1:4000`. Use `bundle exec jekyll build` to produce a production build in `_site/`. If Bundler warns that `jekyll` is missing, install gems before troubleshooting templates.

## Coding Style & Naming Conventions
Use 2-space indentation in HTML, Liquid, SCSS, and YAML. Prefer Liquid filters such as `relative_url` for internal links and asset references. Keep includes small and single-purpose; shared third-party snippets such as Giscus belong in `_includes/`. Post filenames should remain lowercase and hyphenated. Keep front matter minimal and explicit.

## Testing Guidelines
There is no dedicated automated test suite in this repository today. Treat `bundle exec jekyll build` as the required regression check before opening a PR. After layout or include changes, manually verify the home page, at least one post page, and the about page. For comment-related changes, confirm Giscus still renders on a post page.

## Commit & Pull Request Guidelines
Recent history uses short, imperative commit subjects such as `fix: ...`, `update: ...`, or brief English summaries like `Fix post navigation links to use relative_url`. Keep commits focused on one concern. PRs should include a short summary, the reason for the change, and manual verification notes. Add screenshots for visible UI or typography changes, and mention any deploy-preview URL when available.

## Configuration Tips
Update site metadata, author details, and plugin settings in `_config.yml`. Be careful when editing third-party scripts in `_includes/head.html` and `_includes/giscus.html`; changes there can affect analytics, comments, or page metadata across the whole site.
