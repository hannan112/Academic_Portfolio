# Hannan's Academic Portfolio Website

This is a personal academic website and portfolio powered by **Jekyll** and the **AcademicPages** template, designed for seamless hosting on **GitHub Pages**.

---

## 🚀 Quick Start: Deploying to GitHub Pages

### 1. Create your GitHub Pages Repository
1. Go to [GitHub](https://github.com/new) and create a **new public repository**.
2. **Name the repository exactly**: `<your-github-username>.github.io` (e.g., `hannan.github.io`).
3. Link your local project to this repository and push:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of academic portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-github-username>/<your-github-username>.github.io.git
   git push -u origin main
   ```
4. In GitHub, go to **Settings** > **Pages** > ensure the Source is set to **Deploy from a branch** (`main` / root).
5. Your website will be live in ~1 minute at `https://<your-github-username>.github.io/`!

---

## 🛠️ How to Customize Your Content

All content is written in standard **Markdown (`.md`)** and **YAML**:

### 1. Profile & Sidebar Info (`_config.yml`)
Open `_config.yml` to update your core details:
- `title`, `name`, `bio`, `employer`, `location`
- `email`: Your contact email
- `googlescholar`: Link to your Google Scholar profile
- `orcid`: Link to your ORCID
- `github`: Your GitHub username
- `linkedin`: Your LinkedIn profile URL

### 2. Profile Photo (`images/profile.png`)
- Place your portrait/headshot in `images/profile.png` (or update the filename in `_config.yml` under `author.avatar`).

### 3. Homepage / About Me (`_pages/about.md`)
- Edit your research summary, bullet points for **Research Interests**, and announcements in the **News & Updates** box.

### 4. Publications (`_publications/`)
To add a new paper, create a `.md` file in `_publications/` (e.g. `2026-paper-name.md`):
```yaml
---
title: "Paper Title"
collection: publications
category: conferences # Options: 'conferences', 'manuscripts', 'preprints', 'books'
permalink: /publication/2026-paper-name
excerpt: "Short summary / one-sentence abstract."
date: 2026-05-15
venue: "Conference or Journal Name (e.g., NeurIPS, SC, TPDS)"
paperurl: "https://arxiv.org/..."
slidesurl: "https://..."
citation: '<b>Hannan</b>, Co-author Name. (2026). &quot;Paper Title.&quot; <i>Conference Name</i>.'
---

### Abstract
Full abstract text goes here...
```

### 5. Research & Projects (`_portfolio/`)
Add project cards by creating Markdown files in `_portfolio/`:
- Add title, technologies used, links to GitHub repositories, documentation, or live demos.

### 6. CV & Experience (`_pages/cv.md` & `files/Hannan_CV.pdf`)
- Edit education, experience, awards, and skills directly in `_pages/cv.md`.
- Place your printable CV PDF at `files/Hannan_CV.pdf` to enable the **Download Full CV (PDF)** button.

---

## 📁 Repository Structure

```text
├── _config.yml               # Main site settings & author profile info
├── _data/
│   └── navigation.yml        # Top navigation menu bar items
├── _pages/
│   ├── about.md              # Homepage (Bio, Research Interests, News)
│   ├── cv.md                 # Curriculum Vitae & Experience
│   ├── portfolio.html        # Projects showcase listing page
│   └── publications.html     # Categorized publications listing page
├── _publications/            # Individual Markdown files for papers/preprints
├── _portfolio/               # Individual Markdown files for research projects
├── _posts/                   # Blog posts and announcements
├── files/                    # Downloadable files (Hannan_CV.pdf, slides, papers)
├── images/                   # Profile avatar (profile.png) and graphics
```
