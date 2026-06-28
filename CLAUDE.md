# Personal Website — taishle.github.io

## Overview
This is Tai Le's personal academic website, hosted at `taishle.github.io` via GitHub Pages. The site is built with plain HTML/CSS/JS — no frameworks, no build step. All pages are self-contained (CSS and JS embedded per-page).

**Owner:** Tai Le (taile@mit.edu)  
**Position:** Biswas Postdoctoral Fellow, MIT Perceptual Engineering Lab / MIT HEALS Collaborative (start: July 2026)  
**GitHub username:** taishle  
**Google Scholar:** https://scholar.google.com/citations?user=3OYFFgcAAAAJ  

---

## File Structure

```
taishle.github.io/
├── index.html                  # Home page — bio, photo, news, links
├── publications.html           # All publications (journal, conference, book chapters)
├── research.html               # Research projects with descriptions and images
├── professional_activities.html # Reviewer roles, fellowships
├── contact.html                # Email, LinkedIn, GitHub
├── awards.html                 # (not in nav — keep for future use)
├── blogs.html                  # (not in nav — keep for future use)
├── projects.html               # (empty placeholder)
├── Tai_Le_CV.pdf               # CV file linked from home page
├── images/
│   ├── tai-headshot.jpg        # Profile photo (square crop)
│   ├── icon.jpg                # Browser favicon
│   └── *.png / *.jpg           # Research project images
└── blog/
    └── blog1.html              # (empty placeholder)
```

---

## Navigation

All 5 active pages share the same navbar:
```
[☀ / 🌙] | [Home] [Publications] [Research] [Professional Activities] [Contact]
```

When adding/removing nav links, update the navbar HTML in **all 5 pages**: index.html, publications.html, research.html, professional_activities.html, contact.html.

---

## Design System

**Colors (light theme):**
- Background: `#f5f5f5`
- Text: `#252020`
- Links: `#1478dd` → hover `#f09228`
- Section heading border: `#f09228` (orange left border)
- Name: `#062a4b`

**Dark theme** is toggled via JS and stored in `localStorage`. The `body.dark-theme` CSS class activates it. Copy the theme toggle JS block verbatim from any existing page when creating new pages.

**Font:** Lato (Google Fonts), fallback Verdana/Helvetica/sans-serif.

**Layout:** Fixed 1000px width, centered with `margin: 0 auto`.

**Icons:** Font Awesome 6.4.0 (CDN).

---

## How to Add a Publication

Open `publications.html` and add an entry inside the appropriate section (`<div id="journal">`, `<div id="conference">`, or `<div id="book">`).

Use this HTML pattern:
```html
<tr>
  <td width="75%" valign="top">
    <p>
      <papertitle>Title of the Paper</papertitle>
      <br>
      Author One, <strong>Tai Le</strong>, Author Three, ...
      <br>
      <em>Journal or Conference Name</em>, Year
      &nbsp;
      <a href="https://doi.org/...">[DOI]</a>
      <a href="https://arxiv.org/abs/...">[arXiv]</a>
    </p>
  </td>
</tr>
```

Bold **Tai Le** in the author list. Add DOI or arXiv links where available.

---

## How to Add a Research Project

Open `research.html` and add a block inside `<div id="research-projects">` using this pattern:
```html
<table class="project-table">
  <tr>
    <td width="50%" valign="top">
      <h3>Project Title</h3>
      <p>Description of the project, motivation, methods, and outcomes.</p>
      <p><strong>Technologies:</strong> list of tools/methods</p>
      <p><strong>Impact:</strong> grants, publications, or deployments</p>
    </td>
    <td width="50%" valign="top">
      <img src="images/project-image.png" class="project-image" alt="Project description">
    </td>
  </tr>
</table>
<hr class="styled">
```

Store project images in `images/` using lowercase-hyphenated filenames.

---

## How to Update the News Section

Open `index.html` and find `<div id="news">`. Add new items at the top (most recent first):
```html
<p>🎉 [Month Year] Brief description of news item. <a href="...">Link text</a></p>
```

Common badge emojis: 🎉 announcement, 📄 paper, 💰 grant/funding, 🏆 award, 📰 press coverage.

---

## How to Update the Profile Photo

1. Add a square-cropped JPG to `taishle.github.io/images/` (recommended: 400×400px, < 200KB)
2. In `index.html`, update the `<img src="images/...">` in the profile section

---

## Deployment

The site deploys automatically via GitHub Pages on push to the `main` branch of the `taishle/taishle.github.io` repository.

```bash
git add .
git commit -m "Update website content"
git push origin main
```

The live site is at: **https://taishle.github.io**

---

## Implementation Plan (reference)

Plan file: `C:\Users\lengo\.claude\plans\i-m-creating-a-personal-radiant-robin.md`

Pages implemented: Home, Publications, Research, Professional Activities, Contact  
Awards and Blogs: files kept but removed from navigation  
Publications source: Google Scholar (https://scholar.google.com/citations?user=3OYFFgcAAAAJ)  
Research projects source: https://sites.uci.edu/taile/projects/ and `Tai Le - past experience.pdf`  
MIT position info: https://mit-pel.com/news/  
