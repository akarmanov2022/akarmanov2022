# Website Instructions

This document provides instructions on how to deploy and customize your personal website.

## Overview

Your website is built using Jekyll and GitHub Pages. The site includes:

1. **Home Page**: A landing page with your introduction and skills
2. **Resume Page**: A detailed professional resume
3. **Projects Page**: A showcase of your projects
4. **Custom Styling**: CSS customizations to enhance the default theme

## Structure

- `index.md`: Main landing page content
- `resume.md`: Your professional resume
- `projects.md`: Your portfolio of projects
- `_config.yml`: Site configuration
- `_layouts/default.html`: Custom layout template
- `_includes/head-custom.html`: Custom head includes
- `assets/css/style.css`: Custom CSS styles
- `img/`: Directory containing images

## How to Deploy

1. **Push to GitHub**: 
   - Make sure your repository is named `username.github.io` (where `username` is your GitHub username)
   - If your repository has a different name, update the `baseurl` in `_config.yml`

2. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click on "Settings"
   - Scroll down to the "GitHub Pages" section
   - Select the branch you want to deploy (usually `main` or `master`)
   - Click "Save"

3. **Wait for Deployment**:
   - GitHub will build and deploy your site
   - You'll see a green checkmark when it's ready
   - Your site will be available at `https://username.github.io` or `https://username.github.io/repository-name`

## How to Customize

### Content

1. **Update Personal Information**:
   - Edit `index.md` to update your introduction and skills
   - Edit `resume.md` to update your professional experience
   - Edit `projects.md` to showcase your projects

2. **Add Images**:
   - Place images in the `img/` directory
   - Reference them in your markdown files using relative paths: `![Alt text](img/image.jpg)`

### Configuration

1. **Site Settings**:
   - Edit `_config.yml` to update site title, description, and other settings

2. **Navigation**:
   - Edit `_layouts/default.html` to update the navigation menu
   - Edit `_config.yml` to update the `header_pages` list

### Styling

1. **Custom CSS**:
   - Edit `assets/css/style.css` to customize the appearance of your site

## Local Development (Optional)

If you want to test changes locally before pushing to GitHub:

1. **Install Jekyll**:
   ```bash
   gem install bundler jekyll
   ```

2. **Create a Gemfile**:
   ```
   source 'https://rubygems.org'
   gem 'github-pages', group: :jekyll_plugins
   ```

3. **Install Dependencies**:
   ```bash
   bundle install
   ```

4. **Run Locally**:
   ```bash
   bundle exec jekyll serve
   ```

5. **View Site**:
   - Open your browser to `http://localhost:4000`

## Need Help?

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/basic-syntax/)