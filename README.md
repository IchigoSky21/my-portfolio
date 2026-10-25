# IchigoSky21 — Portfolio

> Building software piece by piece.

Personal portfolio of **Emmanuel (IchigoSky21)**, a Software Engineering student at Binus University who builds web apps and machine learning projects. It is a single-page site with a brick-inspired visual theme, written in plain HTML, CSS, and JavaScript with no frameworks and no build step.

**Live site:** https://my-portofolio.hetobias05.workers.dev/

## Features

- **Brick-inspired design:** studs, chunky shadows, and a build-instruction layout where each section is a numbered step.
- **Light and dark themes:** follows the system setting by default, with a toggle that remembers your choice.
- **Smooth, lightweight motion:** staggered entrance animations, scroll reveal, press feedback on buttons and cards, and a header that hides on scroll-down on phones. Animations use only `transform` and `opacity`, and are turned off for visitors who prefer reduced motion.
- **Project filter:** switch between All, Web, ML / AI, and Research.
- **Section tracking:** the navigation highlights the current section and a progress bar fills as you scroll.
- **Responsive:** designed for phones first and scales up to wide desktop screens.
- **Accessible basics:** semantic landmarks, visible keyboard focus, labelled controls, and no horizontal scrolling on small screens.
- **Link preview and favicon:** sharing the link on WhatsApp, LinkedIn, or X shows a title, description, and preview image.
- **Fast:** one HTML file of about 38 KB, no JavaScript libraries, no images. Only the fonts load from Google Fonts.

## Sections

| # | Section | What it contains |
|---|---------|------------------|
| 1 | Home | Introduction, call-to-action buttons, and the brick illustration |
| 2 | About | Short bio and a "build specification" card |
| 3 | Projects | Filterable project cards with tech tags and links |
| 4 | Experience | Education and experience timeline |
| 5 | Skills | Skills grouped by Web, Machine Learning, CV / NLP, and Academic |
| 6 | Contact | GitHub, email, and LinkedIn |

## Featured projects

| Project | What it does | Demo | Code |
|---------|--------------|------|------|
| GIFTo | AI-powered gift recommendation web app (PWA) | [Live](https://ai-gift-prediction.vercel.app/) | [ai-gift-prediction](https://github.com/IchigoSky21/ai-gift-prediction) |
| Citation Generator | IEEE and APA citation web utility | [Live](https://generate-sitation-app.vercel.app/) | [generate-sitation](https://github.com/IchigoSky21/generate-sitation) |
| TokoKita | Client-side PWA for small business (UMKM) sales, inventory, and Excel export | [Live](https://ichigosky21.github.io/UMKM-Ledger/) | [umkm-Ledger](https://github.com/IchigoSky21/umkm-Ledger) |
| Birthday Card Generator | Interactive animated birthday cards with music and PNG export | [Live](https://ichigosky21.github.io/birthday-gift/) | [birthday-gift](https://github.com/IchigoSky21/birthday-gift) |
| Fraud Detection | Random Forest fraud screening app built with Streamlit | [Live](https://fraud-detection-app-oz629kbvyj8qzc7833krcn.streamlit.app/) | [fraud-detection-app](https://github.com/IchigoSky21/fraud-detection-app) |

The portfolio also lists MindScan (NLP), Pothole Detection (computer vision), and an electricity forecasting paper. These are course and research projects without a public repository.

## Tech stack

- HTML5
- CSS3 (custom properties for theming, Grid, Flexbox, keyframe animations)
- Vanilla JavaScript (IntersectionObserver for reveal and section tracking)
- Google Fonts: Fredoka, Figtree, JetBrains Mono
- Hosted on Cloudflare

## Project structure

```text
my-portfolio/
├── index.html        # markup, styles, and scripts in a single file
├── og-image.png      # link preview image (1200 × 630)
└── README.md
```

## Run locally

No installation is needed. Open `index.html` in a browser.

To serve it over HTTP instead:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Customize

Everything lives in `index.html`.

**Colors.** Edit the variables at the top of the `<style>` block. `:root` holds the light theme, and the dark theme is defined twice (once for `prefers-color-scheme` and once for the manual toggle), so change both.

```css
:root{
  --red:#d42a47;
  --blue:#1f72c4;
  --yellow:#ffc72c;
  --green:#178a4c;
}
```

**Add a project.** Copy an existing `<article class="project">` block inside `#projectGrid`. Use `data-category="web"`, `"ml"`, or `"research"` so the filters work.

```html
<article class="project" data-category="web">
  <div class="project-top mono">
    <span class="project-kind">Web · Personal</span>
    <span>07</span>
  </div>

  <h3>Project name</h3>
  <p>One or two sentences about what it does.</p>

  <ul class="tags">
    <li>JavaScript</li>
  </ul>

  <div class="project-actions">
    <a class="small-btn primary" href="DEMO_URL" target="_blank" rel="noopener">Live Demo ↗</a>
    <a class="small-btn" href="REPO_URL" target="_blank" rel="noopener">GitHub ↗</a>
  </div>
</article>
```

**Add experience.** Copy an `<article class="timeline-item">` block in the Experience section and change the date, role, and description.

**Add a project screenshot or certificate image.** Put the file in an `images/` folder, keep it under about 150 KB (WebP at around 800 px wide works well), and add it inside the card:

```html
<img src="images/example.webp" alt="Describe the image" loading="lazy">
```

## Deployment

The site is deployed on Cloudflare. 

## Contact

- GitHub: [@IchigoSky21](https://github.com/IchigoSky21)
- LinkedIn: [Haposan Emmanuel Tobias](https://www.linkedin.com/in/haposan-emmanuel-tobias-903b77325)
- Email: see the contact section on the [live site](https://my-portofolio.hetobias05.workers.dev/#contact)
