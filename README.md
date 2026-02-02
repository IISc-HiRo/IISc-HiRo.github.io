# HiRo Lab Website

A clean, minimal lab website featuring Home, Lab, and Research pages.

## 🚀 Quick Start

```bash
# Install dependencies (first time only)
bundle install

# Run locally
bundle exec jekyll serve

# Visit in browser
http://localhost:4000
```

## 📁 Structure

```
├── _config.yml                   # Site configuration
├── Gemfile                       # Ruby dependencies
│
├── _pages/                       # Main pages
│   ├── about.md                 # Home page
│   ├── lab.md                   # Lab members (edit here to add/remove people)
│   ├── research.md              # Publications page
│   └── 404.md                   # Error page
│
├── _bibliography/
│   └── papers.bib               # Publications in BibTeX format
│
├── _layouts/
│   ├── main.liquid             # Main layout
│   └── page.liquid              # Secondary layout
│
├── _includes/
│   ├── navbar.liquid            # Navigation bar
│   └── research_item.liquid     # Publication display template
│
└── assets/
    ├── css/
    │   ├── main.css            # Main styles
    │   └── extras.css          # Optional extras
    ├── js/
    │   └── gallery.js          # Optional slideshow
    └── img/                    # All images
        ├── people/             # Lab member photos
        └── publication_preview/ # Publication previews
```

## ✏️ How to Edit Your Site

### 1. Update Site Information

Edit `_config.yml`:

```yaml
title: HiRo Lab
email: ravipr@iisc.ac.in
url: https://IISc-HiRo.github.io
github_username: IISc-HiRo
```

### 2. Edit Homepage Content

Edit `_pages/about.md`:

- Update lab description
- Change links (GitHub, YouTube, etc.)
- Update hero image path

### 3. Add/Remove Lab Members

Edit `_pages/lab.md` directly. To add a member, copy this block:

```html
<div class="person-card">
  <img src="{{ '/assets/img/people/name.jpg' | relative_url }}" alt="Name" />
  <span class="name">Full Name</span>
  <span class="role">Role (e.g., PhD, Master's)</span>
</div>
```

Add the person's photo to `assets/img/people/`

### 4. Add a New Publication

Edit `_bibliography/papers.bib` and add:

```bibtex
@article{yourpaper2025,
  title={Your Paper Title},
  author={Author1 and Author2 and Prakash, Ravi},
  journal={Conference/Journal Name},
  year={2025},
  preview={preview.gif},  # optional, in assets/img/publication_preview/
  arxiv={2501.12345},     # optional
  website={https://...},  # optional
  github={https://...}    # optional
}
```

**Optional:** Add preview image/gif to `assets/img/publication_preview/`

### 5. Change Colors/Styling

Edit `assets/css/main.css`:

```css
:root {
  --primary-color: #2c3e50; /* Change heading colors */
  --link-color: #1a73e8; /* Change link colors */
}
```

### 6. Add a New Page (Optional)

1. Create `_pages/contact.md`:

```markdown
---
layout: stanford-real
title: Contact
permalink: /contact/
---

Your content here
```

2. Add link to `_includes/navbar.liquid`:

```html
<a href="{{ '/contact/' | relative_url }}" class="nav-link">Contact</a>
```

## 📦 Deploy to GitHub Pages

```bash
# Commit your changes
git add .
git commit -m "Update website"
git push origin main

# Enable GitHub Pages:
# GitHub → Settings → Pages → Select 'main' branch → Save
```

Your site will be live at: `https://IISc-HiRo.github.io/`

## 🆘 Troubleshooting

**Site won't build?**

```bash
bundle update
bundle exec jekyll serve --trace
```

**Images not showing?**

- Check paths start with `/assets/img/`
- Verify files exist

**Publications not showing?**

- Check BibTeX syntax in `papers.bib`
- Ensure jekyll-scholar plugin is installed

## 📧 Contact

**HiRo Lab** - Human-interactive Robotics Lab
Indian Institute of Science, Bengaluru
Email: ravipr@iisc.ac.in
GitHub: [IISc-HiRo](https://github.com/IISc-HiRo)
