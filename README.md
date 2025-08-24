# Mr. RootBoot Blog

**My Journey into Offensive Security and Compliance**

A Hugo-based static blog focused on cybersecurity, penetration testing, and compliance frameworks, deployed automatically to GitHub Pages.

## 🚀 Quick Start

### Prerequisites

- Git
- Hugo (extended version recommended)
- WSL2 (for Windows users)

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/rootboot-blog.git
   cd rootboot-blog
   ```

2. **Initialize the theme submodule**
   ```bash
   git submodule update --init --recursive
   ```

3. **Install Hugo (WSL2/Linux)**
   ```bash
   # Download and install Hugo extended
   wget https://github.com/gohugoio/hugo/releases/download/v0.128.0/hugo_extended_0.128.0_linux-amd64.deb
   sudo dpkg -i hugo_extended_0.128.0_linux-amd64.deb
   ```

4. **Start the development server**
   ```bash
   hugo server -D
   ```

   Your site will be available at `http://localhost:1313`

## 📝 Creating Content

### New Blog Post
```bash
hugo new posts/your-post-title.md
```

### Post Front Matter Template
```yaml
---
title: "Your Post Title"
date: 2025-08-24T12:00:00+02:00
draft: false
toc: true
images:
tags:
  - cybersecurity
  - penetration testing
---
```

## 🎨 Theme Configuration

This blog uses the [Hugo Terminal Theme](https://github.com/panr/hugo-theme-terminal). Key configurations in `hugo.toml`:

- **Theme Color**: Green (cybersecurity aesthetic)
- **Content Type**: Posts
- **Features**: Table of contents, reading time, last updated dates

## 🚀 Deployment

### GitHub Pages Setup

1. **Enable GitHub Pages**
   - Go to your repository settings
   - Navigate to "Pages" section
   - Set source to "GitHub Actions"

2. **Update Configuration**
   - Edit `hugo.toml` and update `baseURL` to your GitHub Pages URL:
     ```toml
     baseURL = 'https://yourusername.github.io/rootboot-blog'
     ```

3. **Automatic Deployment**
   - Push to `main` branch triggers automatic deployment
   - GitHub Actions workflow builds and deploys the site
   - Site updates are live within minutes

### Manual Deployment
```bash
# Build the site
hugo --gc --minify

# Deploy the public/ directory to your hosting provider
```

## 📁 Project Structure

```
rootboot-blog/
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions CI/CD
├── content/
│   ├── posts/
│   │   ├── _index.md
│   │   ├── welcome-to-mr-rootboot.md
│   │   └── getting-started-with-penetration-testing.md
│   └── about.md
├── themes/
│   └── hugo-theme-terminal/   # Git submodule
├── .gitmodules
├── hugo.toml                  # Site configuration
└── README.md
```

## 🛠️ Customization

### Adding New Menu Items
Edit `hugo.toml`:
```toml
[[languages.en.menu.main]]
  identifier = "resources"
  name = "Resources"
  url = "/resources"
```

### Changing Theme Colors
Available colors: orange, blue, red, green, pink
```toml
[params]
  themeColor = "green"
```

### Social Media Integration
```toml
[params.twitter]
  creator = "yourtwitterhandle"
  site = "yourtwitterhandle"
```

## 📚 Content Guidelines

### Blog Post Categories
- **Penetration Testing**: Walkthroughs, methodologies, tools
- **Vulnerability Research**: CVE analysis, exploit development
- **Compliance**: Framework guides, audit preparation
- **Tool Reviews**: Security tool comparisons and tutorials
- **Learning Resources**: Educational content and career advice

### Writing Style
- Educational and accessible
- Include practical examples
- Add proper disclaimers for security content
- Use code blocks for commands and configurations
- Include relevant tags for discoverability

## 🔒 Security Considerations

- All content is for educational purposes only
- Include appropriate disclaimers
- Never share actual credentials or sensitive information
- Follow responsible disclosure practices
- Emphasize the importance of proper authorization

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Add your content or improvements
4. Submit a pull request

## 📄 License

This project is open source. Please respect the licenses of the Hugo framework and Terminal theme.

## 🔗 Links

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Terminal Theme](https://github.com/panr/hugo-theme-terminal)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

---

**Happy blogging and stay secure!** 🛡️
