# Project: Mind the Gap Man (Code Institute Milestone Project 1)

## Goal & Grading Target
- Build a responsive 3-page website (`index.html`, `services.html`, `contact.html`, plus `thank-you.html` if needed for pure-HTML form confirmation) aiming for **Distinction** level.
- Deploy via GitHub Pages (`cyberjkb/mind-the-gap`, `main` branch, `/root`).
- Maintain `README.md` and `TESTING.md` modeled on high-scoring Code Institute milestone projects.

## Reference Repositories (Sibling Folders)
- `../project-1-ref/` — Read before building and check after each milestone:
  - `mind-the-gap brief.pdf` (project scope & copy)
  - `HTML CSS Bootstrap Project - Submission Checklist (1).pdf` (grading criteria)
  - `Example Website Projects (1).pdf` (Pass/Merit/Distinction examples)
  - `wireframe-1.jpg`, `wireframe-2.jpg`, `services-comic-strip-sketch.jpg` (layout sketches)
  - Brand assets to copy into `assets/images/`: `favicon.svg`, `mind-the-gap-man-logo-transparent.webp`
- `../mei-wong/` — Reference for clean Bootstrap layout structure and project organization.

## Directory Structure (`mind-the-gap/`)
- `index.html` — Home page (Navbar, HERO banner, Origin Story + Superpowers/Weaknesses list group, Comic-strip Services preview card, Distress Signal preview card, Footer).
- `services.html` — Detailed Bronze/Silver/Gold packages, tier selector, and Web3Forms service request form.
- `contact.html` — Distress Signal general emergency contact page with Web3Forms message form.
- `assets/css/style.css` — Custom comic-book strip styling.
- `assets/images/` — Local `.webp`, `.png`, and `favicon.svg` assets.

## Tech Stack & Strict Constraints
- **HTML5, CSS3, and Bootstrap 5.3 ONLY.**
- **NO custom JavaScript.** (Only Bootstrap's standard bundle if needed for the mobile navbar toggler, and the Font Awesome kit `<script src="https://kit.fontawesome.com/265cd67e49.js" crossorigin="anonymous"></script>`).
- **Web3Forms Integration:** Use standard HTML `<form action="https://api.web3forms.com/submit" method="POST">` with clear HTML comments showing where to paste `access_key` and optional redirect URL for confirmation.

## Visual Style: Superhero Comic Book Strip
- **Palette:** London Underground Red (`#EE2436`), Underground Blue (`#0019A8`), Platform Warning Yellow (`#FFCE00`), Ink Black (`#111111`), Comic Paper Off-White (`#F8F9FA`).
- **Typography:** Google Font `'Bangers'` for headings, buttons, and hero display text; clean sans-serif (`'Roboto'` or `'Open Sans'`) for body paragraphs and footer copyright.
- **Comic Styling (Pure CSS):** Thick ink-black borders (`3px–4px solid #111111`), hard offset comic drop shadows (`box-shadow: 6px 6px 0 #111111`), comic panel grid layouts, and subtle rotation (`transform: rotate(-2deg)`) on buttons and heading accents/`::first-letter`.
- **Navbar:** Small logo on left, links on right, mobile hamburger menu, responsive `mind-the-gap-platform-floor-crop.png` background keeping centered "MIND THE GAP" floor text visible across desktop, tablet, and mobile.
- **Images:** Prefer `.webp` for raster images. Use descriptive `alt` attributes on every image.

## Code Comments & Quality Rules
- **Educational Code Comments:** Above every major HTML section and CSS rule block across all files, write a concise comment explaining **what** the code is and **why** it is used.
- **Validation:** Ensure W3C-valid HTML5 (`-->` comment endings, semantic tags, accessible `<label>` elements) and W3C-valid CSS3.
- **Workflow:** Build and verify one page/milestone at a time. Ask before running `git push`.