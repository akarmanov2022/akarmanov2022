# Website Instructions

This document describes how the personal website is built, deployed, and customized.

## Overview

The site is built with Jekyll and GitHub Pages. The repository is named after the GitHub username (`akarmanov2022`), so:

- `README.md` doubles as the GitHub profile page **and** the site homepage (GitHub Pages converts it to `index.html` because there is no `index.*` file).
- The site is a **project site**, served at `https://akarmanov2022.github.io/akarmanov2022/` (not the domain root). All internal links must therefore include the `/akarmanov2022` prefix, and `baseurl` in `_config.yml` is set to `/akarmanov2022` for exactly this reason.

## Structure

- `README.md`: profile page + site homepage
- `resume.md`: resume page (`/akarmanov2022/resume/`)
- `404.md`: custom 404 page
- `_config.yml`: site configuration (baseurl, theme, navigation, markdown engine)
- `Gemfile`: gem dependencies for local development (uses the `github-pages` gem)
- `.github/workflows/jekyll-gh-pages.yml`: build & deploy workflow
- `img/`: images referenced from pages

The visual theme is the Cayman remote theme (`pages-themes/cayman`), loaded via the `jekyll-remote-theme` plugin. There are no local `_layouts/` or `_includes/` directories.

## Deployment

Deployment is automatic: every push to the `develop` branch triggers the GitHub Actions workflow, which builds the site with Jekyll and deploys it to GitHub Pages. There are no manual steps.

## Local Development

```bash
bundle install               # install dependencies
bundle exec jekyll serve     # serve at http://localhost:4000
```

Note: locally the site is served at the root (`http://localhost:4000/`), but Jekyll applies the `baseurl`, so pages live under `http://localhost:4000/akarmanov2022/`.

## Customization

### Content

- Edit `README.md` to update the homepage / profile introduction.
- Edit `resume.md` to update the professional resume.

### Configuration

- Edit `_config.yml` to update site title, description, navigation (`header_pages`), and other settings.
- Do not remove or change `baseurl: "/akarmanov2022"` — it is required because the site is a project site.

### Links

Use root-relative links with the `/akarmanov2022` prefix for internal pages (e.g. `/akarmanov2022/resume/`), or full URLs (`https://akarmanov2022.github.io/akarmanov2022/...`) in places that render outside the site, such as the GitHub profile view of `README.md`.

## Need Help?

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)
