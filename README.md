# Portfolio Site

[![Deploy Hugo site to GitHub Pages](https://github.com/martincarapia/PortfolioSite/actions/workflows/deploy.yml/badge.svg)](https://github.com/martincarapia/PortfolioSite/actions/workflows/deploy.yml)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?logo=github)](https://martincarapia.github.io/)
[![Hugo](https://img.shields.io/badge/Hugo-v0.120.4-FF4088?logo=hugo&logoColor=white)](https://gohugo.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?logo=linkedin&logoColor=white)](https://linkedin.com/in/your-profile)
[![GitHub followers](https://img.shields.io/github/followers/martincarapia?style=social)](https://github.com/martincarapia)
[![GitHub stars](https://img.shields.io/github/stars/martincarapia/PortfolioSite?style=social)](https://github.com/martincarapia/PortfolioSite/stargazers)

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/martincarapia/PortfolioSite/graphs/commit-activity)
[![Website](https://img.shields.io/website?down_color=red&down_message=offline&up_color=green&up_message=online&url=https%3A%2F%2Fmartincarapia.github.io%2F)](https://martincarapia.github.io/)
[![GitHub last commit](https://img.shields.io/github/last-commit/martincarapia/PortfolioSite)](https://github.com/martincarapia/PortfolioSite/commits/main)
[![GitHub repo size](https://img.shields.io/github/repo-size/martincarapia/PortfolioSite)](https://github.com/martincarapia/PortfolioSite)

A personal portfolio website built with Hugo static site generator and automatically deployed to GitHub Pages.

## 🚀 Live Site

Visit the live site at: [https://martincarapia.github.io/](https://martincarapia.github.io/)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- [Hugo Extended](https://gohugo.io/installation/) (v0.120.4 or later)
- [Git](https://git-scm.com/)
- [Go](https://golang.org/) (optional, for Hugo modules)

### Installing Hugo

**macOS (using Homebrew):**
```bash
brew install hugo
```

**Windows (using Chocolatey):**
```bash
choco install hugo-extended
```

**Linux (using Snap):**
```bash
sudo snap install hugo
```

## 🛠️ Local Development

### 1. Clone the Repository

```bash
git clone https://github.com/martincarapia/martincarapia.github.io.git
cd martincarapia.github.io
```

### 2. Install Dependencies

If using Hugo modules or themes with dependencies:
```bash
hugo mod download
```

### 3. Run Development Server

Start the local development server:
```bash
hugo server
```

Or with draft content and live reload:
```bash
hugo server --buildDrafts --buildFuture --disableFastRender
```

The site will be available at `http://localhost:1313`

### 4. Build for Production

Generate static files for production:
```bash
hugo --minify
```

The generated files will be in the `public/` directory.

## 📁 Project Structure

```
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions deployment workflow
├── archetypes/
│   └── default.md              # Content templates
├── assets/                     # Sass files, JS, images for processing
├── content/
│   ├── _index.md              # Homepage content
│   ├── about.md               # About page
│   └── blogs/                 # Blog posts
├── data/                      # Data files (YAML, JSON, TOML)
├── layouts/                   # HTML templates
├── static/                    # Static files (images, CSS, JS)
├── themes/                    # Hugo themes
├── hugo.yaml                  # Hugo configuration
└── .gitignore                # Git ignore rules
```

## 📝 Content Management

### Creating New Content

**Create a new blog post:**
```bash
hugo new content/blogs/my-new-post.md
```

**Create a new page:**
```bash
hugo new content/my-new-page.md
```

### Front Matter Example

```yaml
---
title: "My Awesome Post"
date: 2023-12-01T10:00:00Z
draft: false
description: "A brief description of the post"
tags: ["hugo", "web development"]
categories: ["blog"]
---

Your content here...
```

## 🎨 Customization

### Configuration

Main site configuration is in `hugo.yaml`. Key settings:

```yaml
baseURL: 'https://martincarapia.github.io/'
languageCode: 'en-us'
title: 'My Portfolio Site'
theme: 'your-theme'

params:
  author: 'Your Name'
  description: 'Your site description'
```

### Styling

- Custom CSS: Add files to `assets/css/`
- Images: Place in `static/images/`
- JavaScript: Add to `assets/js/`

## 🚀 Deployment

This site uses GitHub Actions for automatic deployment to GitHub Pages.

### Automatic Deployment

Every push to the `main` branch automatically:
1. Builds the Hugo site
2. Deploys to GitHub Pages
3. Makes the site live at `https://martincarapia.github.io/`

### Manual Deployment

You can also trigger deployment manually:
1. Go to the "Actions" tab in your GitHub repository
2. Select "Deploy Hugo site to GitHub Pages"
3. Click "Run workflow"

## 🔧 Development Workflow

### 1. Create a new branch for changes
```bash
git checkout -b feature/new-feature
```

### 2. Make your changes
- Edit content in `content/`
- Modify layouts in `layouts/`
- Update styles in `assets/`

### 3. Test locally
```bash
hugo server --buildDrafts
```

### 4. Commit and push
```bash
git add .
git commit -m "Add new feature"
git push origin feature/new-feature
```

### 5. Create a Pull Request
- Open a PR on GitHub
- Review changes
- Merge to `main` for automatic deployment

## 📊 Analytics & SEO

### Google Analytics
Add your GA4 measurement ID in `hugo.yaml`:
```yaml
googleAnalytics: 'G-XXXXXXXXXX'
```

### SEO Optimization
- Set proper `title` and `description` in front matter
- Use descriptive filenames and URLs
- Optimize images (use WebP when possible)
- Generate sitemap automatically with Hugo

## 🐛 Troubleshooting

### Common Issues

**Hugo server not starting:**
```bash
# Check Hugo version
hugo version

# Clear Hugo cache
hugo mod clean
```

**Build failing in GitHub Actions:**
- Check the Actions tab for detailed error logs
- Ensure all required files are committed
- Verify Hugo version compatibility

**Styles not loading:**
- Check file paths in templates
- Ensure CSS files are in the correct directory
- Clear browser cache

### Getting Help

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Hugo Community Forum](https://discourse.gohugo.io/)
- [GitHub Issues](https://github.com/martincarapia/martincarapia.github.io/issues)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Contact

- Website: [https://martincarapia.github.io/](https://martincarapia.github.io/)
- Email: your.email@example.com
- GitHub: [@martincarapia](https://github.com/martincarapia)

---

Built with ❤️ using [Hugo](https://gohugo.io/) and deployed on [GitHub Pages](https://pages.github.com/).