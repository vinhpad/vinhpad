# GitHub Pages Deployment Guide

## 📋 Setup Instructions

To enable GitHub Pages for this blog, follow these steps:

### 1. Enable GitHub Pages in Repository Settings

1. Go to your repository on GitHub: `https://github.com/vinhpad/vinhpad.github.io`
2. Click on **Settings** tab
3. In the left sidebar, click on **Pages**
4. Under **Build and deployment**:
   - **Source**: Select "GitHub Actions"
   - This will allow the workflow in `.github/workflows/deploy.yml` to deploy the site

### 2. Merge the Pull Request

Once this PR is merged to the `main` branch, the GitHub Actions workflow will automatically:
1. Build the Jekyll site
2. Deploy it to GitHub Pages

### 3. Access Your Blog

After the workflow completes (usually takes 1-2 minutes), your blog will be available at:
- **URL**: `https://vinhpad.github.io/`

## 🔍 What Was Set Up

### Jekyll Blog Structure
- **_config.yml**: Main configuration file
  - Site title, description, author
  - Minima theme
  - Plugins: jekyll-feed, jekyll-seo-tag
  
- **index.md**: Home page with blog post listings
- **about.md**: About page
- **_posts/**: Directory containing blog posts
  - Posts use naming format: `YYYY-MM-DD-title.md`
  - Each post has front matter with layout, title, date, and categories

### Deployment Workflow
- **`.github/workflows/deploy.yml`**: GitHub Actions workflow
  - Triggers on push to `main` branch
  - Builds Jekyll site
  - Deploys to GitHub Pages
  - Uses official GitHub Actions for Pages deployment

### Dependencies
- **Gemfile**: Ruby dependencies
  - github-pages gem (includes Jekyll and plugins)
  - Additional plugins for feed and SEO

## ✍️ Adding New Blog Posts

To create a new blog post:

1. Create a new file in `_posts/` directory
2. Name it: `YYYY-MM-DD-title-of-post.md`
3. Add front matter:
```yaml
---
layout: post
title: "Your Post Title"
date: 2026-02-12 12:00:00 +0000
categories: category1 category2
---
```
4. Write your content in Markdown
5. Commit and push to `main` branch
6. The site will automatically rebuild and deploy

## 🎨 Customization

### Change Theme
Edit `_config.yml` and change the `theme` value:
```yaml
theme: minima  # or another supported theme
```

Supported themes on GitHub Pages:
- minima (current)
- jekyll-theme-cayman
- jekyll-theme-slate
- And many more...

### Add Custom Pages
Create new `.md` files in the root directory with front matter:
```yaml
---
layout: page
title: Page Title
permalink: /page-url/
---
```

### Customize Site Info
Edit `_config.yml` to update:
- Site title
- Description
- Author name
- Permalink structure
- And more...

## 🛠️ Troubleshooting

### Site Not Showing Up
1. Check GitHub Actions tab for workflow status
2. Ensure GitHub Pages is enabled in Settings > Pages
3. Wait 1-2 minutes after workflow completes
4. Clear browser cache and retry

### Build Failures
1. Check the workflow logs in GitHub Actions tab
2. Common issues:
   - Invalid YAML front matter in posts
   - Incorrect date format in post filenames
   - Unsupported plugins (only use github-pages supported plugins)

### Local Testing (Optional)
If you want to preview locally before deploying:
```bash
# Install Ruby and Bundler first
bundle install
bundle exec jekyll serve

# Visit http://localhost:4000
```

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Minima Theme](https://github.com/jekyll/minima)
- [Markdown Guide](https://www.markdownguide.org/)

## ✅ Checklist for Deployment

- [x] Jekyll blog structure created
- [x] Sample blog posts added
- [x] GitHub Actions workflow configured
- [ ] **TO DO**: Enable GitHub Pages in repository settings (Settings > Pages > Source: GitHub Actions)
- [ ] **TO DO**: Merge PR to main branch
- [ ] **TO DO**: Verify blog is live at `https://vinhpad.github.io/`

## 🎉 Next Steps

After enabling GitHub Pages and merging:
1. Visit your blog URL
2. Start writing new blog posts
3. Customize the theme and layout as desired
4. Share your blog with others!

Enjoy your new blog! 🚀
