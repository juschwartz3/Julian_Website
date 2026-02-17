# Julian Schwartz - Personal Website

A personal portfolio and blog built with [Quarto](https://quarto.org/), featuring my CV and blog posts about chemistry, technology, and professional development.

## Features

- **CV Homepage**: Professional resume showcasing education, experience, and skills
- **Blog**: Regular posts on chemistry, analytical instrumentation, and career development
- **Automatic Deployment**: GitHub Actions workflow deploys to GitHub Pages on every push
- **Responsive Design**: Mobile-friendly layout using Quarto's Cosmo theme

## Local Development

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) (version 1.3 or later)

### Preview the Site

```bash
quarto preview
```

This will start a local server and open the site in your browser. The preview automatically reloads when you make changes.

### Render the Site

```bash
quarto render
```

This generates the static HTML site in the `_site/` directory.

## Project Structure

```
.
├── _quarto.yml              # Main Quarto configuration
├── index.qmd                # CV homepage
├── blog.qmd                 # Blog listing page
├── posts/                   # Blog posts directory
│   └── YYYY-MM-DD-title/    # Each post in its own dated folder
│       └── index.qmd        # Post content
├── Images/                  # Site images
├── styles.css               # Custom CSS
└── .github/
    └── workflows/
        └── publish.yml      # GitHub Actions deployment workflow
```

## Creating a New Blog Post

1. Create a new directory in `posts/` with the date and title:
   ```bash
   mkdir posts/$(date +%Y-%m-%d)-your-post-title
   ```

2. Create an `index.qmd` file in that directory with front matter:
   ```yaml
   ---
   title: "Your Post Title"
   author: "Julian Schwartz"
   date: "YYYY-MM-DD"
   categories: [category1, category2]
   description: "Brief description of the post"
   ---
   ```

3. Write your content using Markdown below the front matter.

4. Preview locally with `quarto preview`, then commit and push to deploy.

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch. The GitHub Actions workflow:

1. Checks out the repository
2. Sets up Quarto
3. Renders the site
4. Deploys to GitHub Pages

View the live site at: [https://juschwartz3.github.io/Julian_Website](https://juschwartz3.github.io/Julian_Website)

## Technologies

- **[Quarto](https://quarto.org/)**: Static site generator
- **GitHub Pages**: Free hosting
- **GitHub Actions**: Automated deployment
- **Markdown/Quarto Markdown**: Content authoring

## License

© 2026 Julian Schwartz. All rights reserved.
