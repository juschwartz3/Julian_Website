# Julian Schwartz - Personal Website

<div align="center">

[![Deploy Status](https://github.com/juschwartz3/Julian_Website/actions/workflows/publish.yml/badge.svg)](https://github.com/juschwartz3/Julian_Website/actions/workflows/publish.yml)
[![Quarto](https://img.shields.io/badge/Made%20with-Quarto-75AADB.svg)](https://quarto.org)
[![License](https://img.shields.io/badge/License-All%20Rights%20Reserved-red.svg)](LICENSE)

**[Visit Live Site →](https://juschwartz3.github.io/Julian_Website)**

</div>

---

## 📖 About

This is my personal portfolio and blog website, built with [Quarto](https://quarto.org/), a modern scientific and technical publishing system. The site serves dual purposes:

1. **Professional Portfolio**: A comprehensive CV showcasing my education, professional experience, and technical skills in analytical chemistry
2. **Technical Blog**: A platform for sharing insights on chemistry, analytical instrumentation, professional development, and technology

### Why Quarto?

- **Markdown-based**: Write content in simple, readable Markdown
- **Professional themes**: Beautiful, responsive designs out of the box
- **Scientific publishing**: Native support for equations, citations, and code
- **Flexible**: Works for both static pages and dynamic blog content
- **Modern**: Fast, accessible, and mobile-friendly

## ✨ Features

### Core Functionality
- 🎓 **Professional CV Homepage** - Education, experience, and skills prominently displayed
- 📝 **Blog with Listings** - Organized posts with categories, dates, and descriptions
- 🎨 **Responsive Design** - Looks great on desktop, tablet, and mobile
- 🔍 **Built-in Search** - Find content quickly across all pages
- 📊 **Automatic Sitemap** - SEO-friendly XML sitemap generation

### Technical Features
- ⚡ **Fast Static Site** - No databases, no servers, just blazing-fast HTML
- 🚀 **Automated Deployment** - Push to GitHub → Automatic build and deploy
- 🔄 **CI/CD Pipeline** - GitHub Actions handles everything
- 🎯 **Clean URLs** - Human-readable, SEO-optimized URLs
- 📱 **Social Media Ready** - Proper meta tags for sharing

### Design Elements
- 🖼️ **Custom Styling** - Tailored CSS for professional appearance
- 🎨 **Cosmo Theme** - Clean, modern Bootstrap-based theme
- 🔗 **Easy Navigation** - Simple navbar with clear sections
- 📧 **Contact Info** - Email and phone prominently displayed in footer

## 🚀 Quick Start

### Prerequisites

Before you begin, ensure you have the following installed:

- **Quarto** (version 1.3 or later) - [Download here](https://quarto.org/docs/get-started/)
- **Git** - For version control
- **Text Editor** - VS Code, Sublime Text, or your favorite editor

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/juschwartz3/Julian_Website.git
   cd Julian_Website
   ```

2. **Verify Quarto installation**
   ```bash
   quarto --version
   ```

3. **Preview the site**
   ```bash
   quarto preview
   ```

   This will:
   - Render the site
   - Start a local development server (usually at http://localhost:4200)
   - Open the site in your default browser
   - Auto-reload when you make changes

### Building the Site

To build the site without starting a server:

```bash
quarto render
```

This generates the complete static site in the `_site/` directory. You can then:
- Open `_site/index.html` in a browser to view locally
- Deploy the `_site/` folder to any web hosting service
- Use the output for testing before pushing to GitHub

## 📁 Project Structure

```
Julian_Website/
├── _quarto.yml                          # Main Quarto configuration
│                                        # - Project type (website)
│                                        # - Navigation structure
│                                        # - Theme and styling options
│                                        # - Site metadata
│
├── index.qmd                            # CV/Resume homepage
│                                        # - Professional experience
│                                        # - Education background
│                                        # - Technical skills
│
├── blog.qmd                             # Blog listing page
│                                        # - Configured to show all posts
│                                        # - Sorted by date (newest first)
│                                        # - Displays categories
│
├── posts/                               # Blog posts directory
│   └── YYYY-MM-DD-post-title/          # Each post in dated folder
│       ├── index.qmd                   # Post content (Markdown)
│       └── images/                     # Post-specific images (optional)
│
├── Images/                              # Site-wide images
│   └── Headshot.jpg                    # Profile photo
│
├── styles.css                           # Custom CSS styling
│                                        # - Headshot styling
│                                        # - Layout customizations
│
├── .github/
│   └── workflows/
│       └── publish.yml                 # GitHub Actions deployment
│                                        # - Triggered on push to main
│                                        # - Builds with Quarto
│                                        # - Deploys to GitHub Pages
│
├── .gitignore                           # Git ignore rules
│                                        # - Excludes _site/
│                                        # - Excludes .quarto/
│                                        # - Excludes build artifacts
│
└── README.md                            # This file!
```

### Key Configuration Files

#### `_quarto.yml`
The heart of the site configuration. Key sections:
- **project**: Defines output directory and type
- **website**: Site metadata, navigation, footer
- **format**: HTML output options, theme, CSS

#### `.github/workflows/publish.yml`
CI/CD pipeline that:
1. Checks out code from repository
2. Sets up Quarto in the GitHub Actions runner
3. Renders the entire site
4. Deploys to GitHub Pages

## ✍️ Creating Content

### Writing a New Blog Post

**Method 1: Using the command line**

```bash
# Create post directory with today's date
mkdir posts/$(date +%Y-%m-%d)-your-post-title

# Create the post file
touch posts/$(date +%Y-%m-%d)-your-post-title/index.qmd
```

**Method 2: Manual creation**

1. Navigate to the `posts/` directory
2. Create a new folder: `YYYY-MM-DD-descriptive-title` (e.g., `2026-02-17-my-first-post`)
3. Inside that folder, create `index.qmd`

**Post Template:**

```yaml
---
title: "Your Compelling Post Title"
author: "Julian Schwartz"
date: "2026-02-17"
categories: [chemistry, instrumentation, career]
description: "A brief description that appears in listings and search results"
image: "images/preview.jpg"  # Optional: preview image
draft: false                  # Set to true to hide from listings
---

## Introduction

Your content starts here. Use standard Markdown syntax.

## Main Content

### Subsections

- Bullet points
- Work great

### Code Blocks

```python
# Code is syntax-highlighted
def hello_world():
    print("Hello from my blog!")
```

### Images

![Image caption](images/your-image.jpg)

### Equations (LaTeX)

Inline equation: $E = mc^2$

Display equation:
$$
\frac{\partial u}{\partial t} = \nabla^2 u
$$

## Conclusion

Wrap up your thoughts here.
```

### Adding Images to Posts

**Option 1: Post-specific images**
```bash
# Create images folder in your post directory
mkdir posts/2026-02-17-your-post/images

# Add your images there
# Reference them as: images/photo.jpg
```

**Option 2: Site-wide images**
```bash
# Add to the main Images/ directory
# Reference them as: /Images/photo.jpg
```

### Updating Your CV

Edit `index.qmd` to update:
- Contact information
- Education
- Professional experience
- Skills and instrumentation expertise

The changes will appear on the homepage after rendering.

## 🎨 Customization

### Changing the Theme

Edit `_quarto.yml`:

```yaml
format:
  html:
    theme: cosmo  # Try: flatly, journal, lumen, minty, pulse, sandstone, etc.
```

[Browse all themes →](https://quarto.org/docs/output-formats/html-themes.html)

### Custom Styling

Edit `styles.css` to customize:
- Colors and fonts
- Layout and spacing
- Component styling

Example additions:
```css
/* Change primary color */
:root {
  --bs-primary: #2C3E50;
}

/* Custom heading style */
h2 {
  color: #3498db;
  border-bottom: 2px solid #ecf0f1;
  padding-bottom: 0.5rem;
}
```

### Modifying Navigation

Edit the `navbar` section in `_quarto.yml`:

```yaml
website:
  navbar:
    left:
      - text: "Home"
        href: index.qmd
      - text: "Blog"
        href: blog.qmd
      - text: "Publications"  # Add new section
        href: publications.qmd
    right:
      - icon: github
        href: "https://github.com/yourusername"
      - icon: linkedin       # Add LinkedIn
        href: "https://linkedin.com/in/yourprofile"
```

### Changing Footer Content

Edit the `page-footer` section in `_quarto.yml`:

```yaml
website:
  page-footer:
    center: |
      Your custom footer text | [Contact](mailto:your@email.com)
```

## 🚀 Deployment

### Initial Setup (One-Time)

**Step 1: Enable GitHub Pages**

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Build and deployment":
   - **Source**: Select **GitHub Actions** (not "Deploy from a branch")
4. Save changes

**Step 2: Push Your Changes**

```bash
git add .
git commit -m "Your commit message"
git push origin main
```

**Step 3: Monitor Deployment**

1. Go to the **Actions** tab in your repository
2. Watch the "Publish Quarto Website" workflow
3. When it shows a green checkmark ✅, deployment is complete
4. Visit your site: `https://yourusername.github.io/repository-name`

### Automated Deployment Workflow

Once set up, the deployment process is fully automated:

```
Local Changes → Commit → Push to GitHub → Actions Triggered → Site Built → Deployed to Pages
```

**What happens automatically:**

1. **Trigger**: Push to `main` branch
2. **Checkout**: GitHub Actions clones your repository
3. **Setup**: Installs Quarto in a clean Ubuntu environment
4. **Render**: Runs `quarto render` to build the site
5. **Deploy**: Uploads `_site/` to GitHub Pages
6. **Live**: Your changes appear at your GitHub Pages URL

**Typical deployment time:** 1-3 minutes

### Viewing Deployment Status

**Check the badge** in this README:
- 🟢 Green = Latest deployment successful
- 🔴 Red = Deployment failed
- 🟡 Yellow = Deployment in progress

**Detailed logs:**
1. Go to **Actions** tab
2. Click on the latest workflow run
3. Expand the steps to see detailed output
4. Look for errors if deployment fails

### Manual Deployment

You can also trigger deployment manually:

1. Go to **Actions** tab
2. Select "Publish Quarto Website" workflow
3. Click **Run workflow** → **Run workflow**

### Custom Domain (Optional)

To use a custom domain (e.g., `julianschartz.com`):

1. **Add CNAME file** to repository root:
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. **Configure DNS** at your domain registrar:
   - Add a CNAME record pointing to `yourusername.github.io`
   - Or add A records pointing to GitHub Pages IPs

3. **Update _quarto.yml**:
   ```yaml
   website:
     site-url: "https://yourdomain.com"
   ```

[Full GitHub Pages custom domain guide →](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

## 🛠️ Technologies & Tools

| Technology | Purpose | Version |
|------------|---------|---------|
| [Quarto](https://quarto.org/) | Static site generator | 1.6+ |
| [GitHub Pages](https://pages.github.com/) | Free static site hosting | - |
| [GitHub Actions](https://github.com/features/actions) | CI/CD automation | - |
| Markdown/QMD | Content authoring format | - |
| HTML/CSS/JS | Generated output | - |
| Bootstrap 5 | CSS framework (via Cosmo theme) | 5.x |

### Why These Technologies?

**Quarto**
- Modern, actively maintained
- Excellent documentation
- Scientific publishing features
- Multi-format output (HTML, PDF, DOCX)

**GitHub Pages**
- Free hosting for static sites
- Automatic HTTPS
- Custom domain support
- Fast CDN delivery

**GitHub Actions**
- Integrated with GitHub
- Free for public repositories
- Reproducible builds
- No external CI/CD services needed

## 🐛 Troubleshooting

### Build Fails Locally

**Problem**: `quarto render` produces errors

**Solutions**:
1. **Update Quarto**: `quarto --version` should be 1.3+
   ```bash
   # Check version
   quarto --version

   # Update Quarto - download latest from quarto.org
   ```

2. **Check file syntax**: Ensure YAML front matter is valid
   ```yaml
   ---
   title: "Title"  # Quotes needed if special characters
   date: "2026-02-17"  # YYYY-MM-DD format
   ---
   ```

3. **Validate images**: Ensure image paths exist
   ```bash
   # Check if image exists
   ls Images/Headshot.jpg
   ```

### GitHub Actions Deployment Fails

**Problem**: Workflow shows red X

**Solutions**:

1. **Check Actions logs**:
   - Go to Actions tab
   - Click failed workflow
   - Expand steps to see error

2. **Common issues**:

   - **Pages not enabled**: Go to Settings → Pages → Set source to "GitHub Actions"

   - **Permissions issue**: Check workflow has correct permissions in `publish.yml`
     ```yaml
     permissions:
       contents: read
       pages: write
       id-token: write
     ```

   - **Branch mismatch**: Ensure workflow triggers on correct branch
     ```yaml
     on:
       push:
         branches:
           - main  # Check this matches your default branch
     ```

3. **Re-run workflow**:
   - Go to Actions → Failed workflow
   - Click "Re-run jobs"

### Preview Not Working

**Problem**: `quarto preview` doesn't open or shows errors

**Solutions**:

1. **Port already in use**:
   ```bash
   # Use a different port
   quarto preview --port 4201
   ```

2. **Clear cache**:
   ```bash
   # Remove cache and try again
   rm -rf .quarto/
   quarto preview
   ```

3. **Browser not opening**:
   ```bash
   # Manually open the URL shown in terminal
   quarto preview --no-browse
   # Then visit http://localhost:4200
   ```

### Images Not Displaying

**Problem**: Images show broken link icon

**Solutions**:

1. **Check path**: Paths are case-sensitive
   - ✅ `Images/Headshot.jpg`
   - ❌ `images/headshot.jpg`

2. **Use relative paths**:
   - From `index.qmd`: `Images/Headshot.jpg`
   - From blog post: `../../Images/Headshot.jpg` or `/Images/Headshot.jpg`

3. **Verify file exists**:
   ```bash
   ls -la Images/
   ```

### Site Not Updating After Push

**Problem**: Changes pushed but site shows old content

**Solutions**:

1. **Check workflow completed**:
   - Actions tab should show green checkmark
   - Wait 1-3 minutes for deployment

2. **Clear browser cache**:
   - Hard refresh: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)
   - Or open in incognito/private window

3. **Check DNS cache** (if using custom domain):
   ```bash
   # May take up to 24 hours for DNS propagation
   ```

## 📚 FAQ

### Can I use this as a template?

Yes! Fork this repository and customize it for your own use. Replace:
- Personal information in `index.qmd`
- Contact details in `_quarto.yml`
- Repository URLs
- Profile photo in `Images/`

### How do I add more pages?

1. Create a new `.qmd` file in the root directory (e.g., `publications.qmd`)
2. Add it to navigation in `_quarto.yml`:
   ```yaml
   website:
     navbar:
       left:
         - text: "Publications"
           href: publications.qmd
   ```
3. Render and push

### Can I write posts in pure Markdown (.md)?

Yes, but `.qmd` is recommended because it supports:
- YAML metadata
- Embedded code execution (R, Python, Julia)
- More advanced features
- Better integration with Quarto

For simple posts, `.md` works fine. Just use `.md` extension instead of `.qmd`.

### How do I schedule posts for future publication?

Set `draft: true` in the front matter, then change to `draft: false` when ready:

```yaml
---
title: "Future Post"
date: "2026-12-31"
draft: true  # Post won't appear in listings
---
```

### Can I password-protect the site?

GitHub Pages doesn't support password protection. Options:
- Use a private repository (requires GitHub Pro)
- Deploy to a different platform (Netlify, Vercel) with auth
- Use client-side encryption (complex)

### How much does hosting cost?

**$0** - GitHub Pages is completely free for public repositories.

### Can I use Google Analytics?

Yes! Add to `_quarto.yml`:

```yaml
website:
  google-analytics: "G-XXXXXXXXXX"
```

Get your tracking ID from [Google Analytics](https://analytics.google.com/).

### How do I add comments to blog posts?

Integrate a comments system like:
- [giscus](https://giscus.app/) (GitHub Discussions)
- [utterances](https://utteranc.es/) (GitHub Issues)
- Disqus (third-party service)

Add to `_quarto.yml`:
```yaml
comments:
  giscus:
    repo: yourusername/Julian_Website
```

## 🔄 Development Workflow

### Typical workflow for adding content:

```bash
# 1. Create a new branch (optional but recommended)
git checkout -b new-blog-post

# 2. Create your content
mkdir posts/$(date +%Y-%m-%d)-new-post
# ... edit files ...

# 3. Preview locally
quarto preview

# 4. Make adjustments and preview again
# (preview auto-reloads on changes)

# 5. When satisfied, commit
git add .
git commit -m "Add blog post about [topic]"

# 6. Push to GitHub
git push origin new-blog-post  # If using branch
# OR
git push origin main  # If working directly on main

# 7. Automatic deployment happens!
# Check Actions tab for progress
```

### Best Practices

**Content**:
- ✅ Write posts in dedicated directories under `posts/`
- ✅ Use descriptive, URL-friendly directory names
- ✅ Include date in post directory name for organization
- ✅ Add meaningful categories to posts
- ✅ Write compelling descriptions (appear in listings and search)

**Images**:
- ✅ Optimize images before adding (compress, resize)
- ✅ Use descriptive filenames
- ✅ Add alt text for accessibility
- ❌ Avoid huge image files (keep under 500KB when possible)

**Git**:
- ✅ Write clear commit messages
- ✅ Commit related changes together
- ✅ Test locally before pushing
- ❌ Don't commit `_site/` or `.quarto/` (in `.gitignore`)

**SEO**:
- ✅ Use descriptive page titles
- ✅ Add meta descriptions
- ✅ Use proper heading hierarchy (H1 → H2 → H3)
- ✅ Include relevant keywords naturally

## 🤝 Contributing

This is a personal website, but suggestions are welcome!

**Found a bug or issue?**
1. Open an issue describing the problem
2. Include screenshots if relevant
3. Mention your browser/OS if it's a display issue

**Have a suggestion?**
1. Open an issue with the "enhancement" label
2. Describe what you'd like to see and why

## 📄 License

© 2026 Julian Schwartz. All rights reserved.

The content of this website (blog posts, CV, images) is proprietary. The structure and configuration may be used as reference for personal projects.

## 🔗 Resources

### Quarto Documentation
- [Official Quarto Guide](https://quarto.org/docs/guide/)
- [Website Creation](https://quarto.org/docs/websites/)
- [Blog Posts](https://quarto.org/docs/websites/website-blog.html)
- [HTML Themes](https://quarto.org/docs/output-formats/html-themes.html)

### GitHub
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Quarto GitHub Actions](https://github.com/quarto-dev/quarto-actions)

### Markdown
- [Markdown Guide](https://www.markdownguide.org/)
- [Quarto Markdown](https://quarto.org/docs/authoring/markdown-basics.html)

## 📞 Contact

**Julian Schwartz**
- Email: juschwartz3@gmail.com
- Phone: 215-528-8241
- GitHub: [@juschwartz3](https://github.com/juschwartz3)

---

<div align="center">

Built with ❤️ using [Quarto](https://quarto.org/)

**[⬆ Back to Top](#julian-schwartz---personal-website)**

</div>
