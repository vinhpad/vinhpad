# Vinhpad Blog

This is my personal blog built with Jekyll and hosted on GitHub Pages.

## 🌐 Live Site

The blog is automatically deployed to GitHub Pages and available at:
- **GitHub Pages URL**: `https://vinhpad.github.io/`

## 📝 About

This blog is created using Jekyll, a static site generator that's natively supported by GitHub Pages. It features:
- Clean and minimal design (Minima theme)
- Automatic deployment via GitHub Actions
- Blog posts in Markdown format
- SEO optimization
- RSS feed support

## 🚀 How It Works

1. Blog posts are written in Markdown and stored in the `_posts` directory
2. When changes are pushed to the main branch, GitHub Actions automatically builds and deploys the site
3. The blog is served via GitHub Pages

## 📂 Structure

```
.
├── _config.yml          # Jekyll configuration
├── _posts/              # Blog posts (Markdown files)
├── index.md             # Home page
├── about.md             # About page
├── Gemfile              # Ruby dependencies
└── .github/workflows/   # GitHub Actions workflow for deployment
```

## ✍️ Writing New Posts

To add a new blog post:
1. Create a new file in the `_posts` directory
2. Name it following the format: `YYYY-MM-DD-title.md`
3. Add front matter at the top:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD HH:MM:SS +0000
   categories: category1 category2
   ---
   ```
4. Write your content in Markdown below the front matter
5. Commit and push - the blog will automatically update!

## 🛠️ Local Development

To run the blog locally (optional):
```bash
# Install dependencies
bundle install

# Run Jekyll server
bundle exec jekyll serve

# Visit http://localhost:4000
```

## 📄 License

This blog and its content are maintained by Vinhpad.
