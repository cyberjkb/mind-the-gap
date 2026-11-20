# Mind the Gap Man – Testing and Validation

[Back to README](README.md) · **Live site:** [https://cyberjkb.github.io/mind-the-gap/](https://cyberjkb.github.io/mind-the-gap/)

> **How to read this document:** Results marked **⬜ To confirm** are placeholders. They must be run and updated by the developer, with screenshots saved in `docs/testing-images/`, before submission. No result is claimed here unless the test has actually been carried out.

---

## Table of Contents

1. [Manual Testing Against the Submission Checklist](#manual-testing-against-the-submission-checklist)
2. [Feature and Link Testing](#feature-and-link-testing)
3. [User Story Testing](#user-story-testing)
4. [Responsiveness Testing](#responsiveness-testing)
5. [Code Validation](#code-validation)
   - [HTML Validation (W3C)](#html-validation-w3c)
   - [CSS Validation (Jigsaw)](#css-validation-jigsaw)
6. [Lighthouse Testing](#lighthouse-testing)
7. [Accessibility Testing](#accessibility-testing)
8. [Bugs](#bugs)
9. [Conclusion](#conclusion)

---

## Manual Testing Against the Submission Checklist

Every item on the *HTML CSS Bootstrap Project – Submission Checklist* is listed below with the way it was tested.

### LO1: Front-End Design and User Experience

| Checklist item | How it was tested | Expected | Result |
| --- | --- | --- | --- |
| Three-page website, each page with its own structure and style | Visited `index.html`, `services.html` and `contact.html` (plus `thank-you.html`) and compared their layouts | Home (hero, origin, comic strip), Services (cards, tiers, table, form) and Contact (HQ details, form) have clearly different layouts but share a theme | ⬜ To confirm |
| Main navigation menu is present and works | Clicked every navbar link on every page, at desktop and mobile widths | Each link loads the correct page, and the active page is highlighted | ⬜ To confirm |
| Content is structured and organised logically | Read each page from top to bottom | Introduction, then detail, then call to action, in a logical order | ⬜ To confirm |
| Semantic HTML tags (header, nav, main, footer, etc.) | Inspected the source and the DevTools Elements panel, and used the W3C outline | `header > nav`, `main` with `section`s, and `footer` are on every page | ⬜ To confirm |
| Appropriate colour contrast | WebAIM Contrast Checker on the main colour pairs (see [Accessibility](#accessibility-testing)), plus WAVE | All text pairs meet WCAG AA (4.5:1 for normal text, 3:1 for large text) | ⬜ To confirm |
| Alt text for all non-text elements | WAVE "Missing alternative text" check, and a manual source review | Every `<img>` has meaningful `alt`, and icon links have `aria-label` | ⬜ To confirm |
| No WCAG errors detected | WAVE run on all four pages | 0 errors | ⬜ To confirm |
| CSS colour variables used for consistent styling | Reviewed the `:root` block in `assets/css/style.css` | All theme colours are defined as custom properties and used through `var()` | Pass ✅ (`:root` defines `--tube-red`, `--tube-blue`, `--platform-yellow`, etc.) |
| WebP images used instead of JPEG/PNG (optional) | Listed `assets/images/` | All raster images are `.webp`, and the favicon is SVG | Pass ✅ |
| Lazy loading applied to images | Searched the source for `loading="lazy"` | Every image below the fold is lazy-loaded. The navbar and hero logos are not, because they are above the fold | ⬜ To confirm |
| Layout adapts to different screen sizes | DevTools device toolbar at 375, 768, 1366 and 1920 px | No horizontal scroll, and columns stack on small screens | ⬜ To confirm |
| No major errors or loss of functionality on resize | Dragged the viewport from 320 px to 1920 px | Navbar collapses and expands, the comic strip reflows from 3 + 2 to a single column, and forms stay usable | ⬜ To confirm |
| Information organised using UX principles | Reviewed against the wireframes and user stories | The most important content (who, what, price, how to book) comes first | ⬜ To confirm |
| Headers show structure and hierarchy | HeadingsMap extension / WAVE structure view | One `<h1>` per page, then `h2`, then `h3`, with no skipped levels | ⬜ To confirm |
| Information is easy to find | A first-time user was asked to find the Gold tier price and the distress form | Both found within a few seconds using the navbar or calls to action | ⬜ To confirm |
| User can start and control actions | Tested the hamburger toggle, the CTA buttons, the clickable cards and the form submit | Every action starts only when the user chooses. There is no autoplaying media | ⬜ To confirm |
| Immediate feedback for user actions (e.g. form submission) | Submitted forms with empty or invalid fields, then with valid data | The browser shows validation messages straight away, and a valid submit redirects to `thank-you.html` | ⬜ To confirm |

### LO2: Testing and Validation

| Checklist item | How it was tested | Expected | Result |
| --- | --- | --- | --- |
| Custom HTML passes W3C validation | [W3C Markup Validator](https://validator.w3.org/) by URI for all four pages | No errors | ⬜ To confirm |
| Custom CSS passes W3C Jigsaw validation | [Jigsaw](https://jigsaw.w3.org/css-validator/) by URI / file upload for `style.css` | No errors | ⬜ To confirm |
| No validation errors or warnings | Reviewed the warnings list from both validators | No warnings, or only warnings explained as false positives (e.g. CSS custom properties or vendor prefixes, which Jigsaw cannot check) | ⬜ To confirm |
| Lighthouse performance test completed | Chrome DevTools Lighthouse, desktop and mobile, on all four pages | A report is saved for each page and mode | ⬜ To confirm |
| Accessibility, Best Practices, SEO and Performance scores reviewed | Recorded the scores in the [Lighthouse table](#lighthouse-testing) | Scores are recorded and any score below 90 has an explanation | ⬜ To confirm |

### LO3: Cloud Deployment

| Checklist item | How it was tested | Expected | Result |
| --- | --- | --- | --- |
| Final version deployed to a cloud platform | Opened [https://cyberjkb.github.io/mind-the-gap/](https://cyberjkb.github.io/mind-the-gap/) | The site loads from GitHub Pages | ⬜ To confirm |
| Deployed version matches the development version | Compared the live pages with the local pages after the final push | No differences in content, styling or images (paths are relative and case-correct) | ⬜ To confirm |
| Git and GitHub used for version control | Checked the repository's commit history | The project is tracked in `cyberjkb/mind-the-gap` | ⬜ To confirm |
| Clear commit history with messages | Reviewed `git log --oneline` | Small, descriptive commits written in the imperative | ⬜ To confirm |
| Clean, commented code | Reviewed the HTML and CSS | Every HTML section and CSS block has a WHAT/WHY comment, with consistent 4-space indentation | ⬜ To confirm |
| All commented-out code removed before deployment | Searched for commented-out markup or rules | Only explanatory comments remain | ⬜ To confirm |
| Internal links and interactive elements work | See [Feature and Link Testing](#feature-and-link-testing) | Every link, button, card and form works | ⬜ To confirm |

### LO4: Documentation and Maintainability

| Checklist item | How it was tested | Expected | Result |
| --- | --- | --- | --- |
| Live link to deployed site at top of README | Read the top of README.md | The live link is the first thing under the title | Pass ✅ |
| Table of contents | README.md and TESTING.md | Both have a linked TOC | Pass ✅ |
| Website's purpose | README › Site Purpose and Goals | Purpose, user goals and site owner goals are explained | Pass ✅ |
| Brief descriptions of features and user benefits | README › Features | Each feature has a description and a "User benefit" | Pass ✅ |
| Deployment procedure | README › Deployment | Steps for GitHub Pages, cloning and forking | Pass ✅ |
| Screenshots of all pages on desktop and mobile | README › Features (desktop and mobile tables) | Every placeholder image is replaced with a real screenshot | ⬜ To confirm (screenshots to add) |
| Screenshots of passed HTML, CSS and Lighthouse tests | This document, [Code Validation](#code-validation) and [Lighthouse](#lighthouse-testing) | Every placeholder image is replaced with a real screenshot | ⬜ To confirm (screenshots to add) |
| Bugs / Errors section | README › Bugs and [Bugs](#bugs) below | Fixed and unfixed bugs are listed | Pass ✅ |
| Proper attribution for external code, images and video | README › Credits | Bootstrap, fonts, icons, Web3Forms, images and inspiration are credited | Pass ✅ |
| Declaration of use of AI | README › Declaration of AI Use | Accurate declaration, reviewed by the student | ⬜ To confirm (student to review wording) |
| Colour palette image included (optional) | README › Colour Palette | Coolors palette image is present | ⬜ To confirm (image to add) |
| Wireframes included (optional) | README › Wireframes | Wireframe images display from `docs/wireframes/` | ⬜ To confirm (copy files into repo) |
| Planned future updates (optional) | README › Future Features | List of future features | Pass ✅ |

---

## Feature and Link Testing

### Shared (all pages)

| Feature | Action | Expected | Result |
| --- | --- | --- | --- |
| Navbar logo | Click the shield logo | Loads `index.html` | ⬜ To confirm |
| Nav link: Home | Click | Loads `index.html`, and the link shows as active | ⬜ To confirm |
| Nav link: Services | Click | Loads `services.html`, and the link shows as active | ⬜ To confirm |
| Nav link: Distress Signal | Click | Loads `contact.html`, and the link shows as active | ⬜ To confirm |
| Hamburger menu | At under 1200 px, click the toggler, then click it again | The menu expands, then collapses, and `aria-expanded` toggles | ⬜ To confirm |
| Footer: Facebook icon | Click | `https://www.facebook.com/` opens in a new tab | ⬜ To confirm |
| Footer: X icon | Click | `https://x.com/` opens in a new tab | ⬜ To confirm |
| Footer: Instagram icon | Click | `https://www.instagram.com/` opens in a new tab | ⬜ To confirm |
| Footer: YouTube icon | Click | `https://www.youtube.com/` opens in a new tab | ⬜ To confirm |
| Footer: TikTok icon | Click | `https://www.tiktok.com/` opens in a new tab | ⬜ To confirm |
| Favicon | Load any page | The roundel favicon shows in the browser tab | ⬜ To confirm |

### Home Page (`index.html`)

| Feature | Action | Expected | Result |
| --- | --- | --- | --- |
| HERO banner | Load the page | "HE[logo]RO" letters, the "HERO FOR HIRE" tagline and the button all display, including on mobile | ⬜ To confirm |
| DISTRESS SIGNAL button | Click | Loads `contact.html` | ⬜ To confirm |
| Superpowers and Weaknesses list group | View | Both lists display, including "Will not fight south of Zone 4 after 9 PM" | ⬜ To confirm |
| Services comic strip | Hover, then click | The panel lifts on hover, and the click loads `services.html` | ⬜ To confirm |
| Comic strip layout | Resize | 3 + 2 panels on desktop, a single column on mobile | ⬜ To confirm |
| "I can be your Hero..." tier summary | Click the link or button | Loads `services.html` | ⬜ To confirm |
| Distress Signal SOS card | Click | Loads `contact.html` | ⬜ To confirm |

### Services Page (`services.html`)

| Feature | Action | Expected | Result |
| --- | --- | --- | --- |
| Service detail cards | View | Five services, each with an image, description and tier badge | ⬜ To confirm |
| Tier cards | View | Bronze £19, Silver £49 and Gold £199, with response times | ⬜ To confirm |
| Comparison table | View on mobile | The table scrolls horizontally inside its wrapper, and the page does not | ⬜ To confirm |
| Rescue form: required fields | Submit empty | The browser blocks submission and shows a "Please fill in this field" message | ⬜ To confirm |
| Rescue form: email format | Type `abc` in email and submit | The browser shows an invalid email message | ⬜ To confirm |
| Rescue form: tier dropdown | Open the select | Lists the Bronze, Silver and Gold options | ⬜ To confirm |
| Rescue form: labels | Click each label | Focus moves to the matching field | ⬜ To confirm |
| Rescue form: submit | Submit valid data (with a real access key) | Web3Forms redirects to `thank-you.html`, and an email arrives | ⬜ To confirm |

### Contact Page (`contact.html`)

| Feature | Action | Expected | Result |
| --- | --- | --- | --- |
| HQ details | View | Fictional hotline, email, address and hours display with icons | ⬜ To confirm |
| Distress form: required fields | Submit empty | The browser blocks submission and shows validation messages | ⬜ To confirm |
| Distress form: email format | Enter an invalid email | The browser shows an invalid email message | ⬜ To confirm |
| Distress form: honeypot | Inspect | The `botcheck` field is hidden from users and skipped by the keyboard | ⬜ To confirm |
| Distress form: submit | Submit valid data (with a real access key) | Web3Forms redirects to `thank-you.html`, and an email arrives | ⬜ To confirm |

### Thank You Page (`thank-you.html`)

| Feature | Action | Expected | Result |
| --- | --- | --- | --- |
| Confirmation message | Arrive here after submitting | A clear confirmation that the distress signal was received | ⬜ To confirm |
| Return links | Click the link back home or to services | The correct page loads | ⬜ To confirm |
| Navbar state | View | No nav link is marked active | ⬜ To confirm |

---

## User Story Testing

| User story | How the site meets it | Evidence | Result |
| --- | --- | --- | --- |
| **M1:** Understand who the hero is straight away | HERO banner and tagline at the top of the home page, followed by the origin story | `docs/testing-images/story-m1.webp` | ⬜ To confirm |
| **M2:** See services and prices | Services comic strip and tier summary on Home, and detail cards on Services | `docs/testing-images/story-m2.webp` | ⬜ To confirm |
| **M3:** Compare tiers side by side | Three tier cards and a comparison table on Services | `docs/testing-images/story-m3.webp` | ⬜ To confirm |
| **M4:** Send a distress signal and get confirmation | Web3Forms forms on Services and Contact, with a redirect to Thank You | `docs/testing-images/story-m4.webp` | ⬜ To confirm |
| **M5:** Navigate on any device | Responsive navbar with hamburger menu and a Bootstrap grid | See [Responsiveness](#responsiveness-testing) | ⬜ To confirm |
| **M6:** Accessible content | Alt text, labels, landmarks and contrast | See [Accessibility](#accessibility-testing) | ⬜ To confirm |
| **M7:** Consistent comic brand | Shared navbar, footer, fonts and palette on every page | `docs/testing-images/story-m7.webp` | ⬜ To confirm |
| **S1:** Superpowers and weaknesses | List group in the Origin Story section | `docs/testing-images/story-s1.webp` | ⬜ To confirm |
| **S2:** Response times | Stated on each tier card | `docs/testing-images/story-s2.webp` | ⬜ To confirm |
| **S3:** Always-reachable distress CTA | "Distress Signal" nav link on every page, plus the hero button and SOS card | `docs/testing-images/story-s3.webp` | ⬜ To confirm |
| **S4:** Social links | Footer icons on every page open in a new tab | `docs/testing-images/story-s4.webp` | ⬜ To confirm |
| **S5:** HQ details and hours | Contact page detail list | `docs/testing-images/story-s5.webp` | ⬜ To confirm |
| **C1–C4:** Could-Have | Not built in this release (see README › Future Features) | – | Deferred |

---

## Responsiveness Testing

Each page was checked in Chrome DevTools device mode and on real browsers at these widths. Check for: no horizontal scroll, readable text, images that scale, a working navbar collapse, and usable forms.

| Page | Desktop 1920 px | Laptop 1366 px | Tablet 768 px | Mobile 375 px |
| --- | --- | --- | --- | --- |
| Home | ⬜ | ⬜ | ⬜ | ⬜ |
| Services | ⬜ | ⬜ | ⬜ | ⬜ |
| Contact | ⬜ | ⬜ | ⬜ | ⬜ |
| Thank You | ⬜ | ⬜ | ⬜ | ⬜ |

### Browser Compatibility

| Browser | Home | Services | Contact | Thank You | Notes |
| --- | --- | --- | --- | --- | --- |
| Google Chrome | ⬜ | ⬜ | ⬜ | ⬜ | |
| Mozilla Firefox | ⬜ | ⬜ | ⬜ | ⬜ | |
| Microsoft Edge | ⬜ | ⬜ | ⬜ | ⬜ | |
| Safari (macOS / iOS) | ⬜ | ⬜ | ⬜ | ⬜ | |

*Replace ⬜ with ✅ (works as expected) or ❌ plus a note.*

### Screenshots

| Device | Screenshot |
| --- | --- |
| Desktop (1920 px) | ![Home page at 1920px](docs/testing-images/responsive-desktop-1920.webp) |
| Laptop (1366 px) | ![Home page at 1366px](docs/testing-images/responsive-laptop-1366.webp) |
| Tablet (768 px) | ![Home page at 768px](docs/testing-images/responsive-tablet-768.webp) |
| Mobile (375 px) | ![Home page at 375px](docs/testing-images/responsive-mobile-375.webp) |

---

## Code Validation

### HTML Validation (W3C)

Each page was validated **by URI** using the live GitHub Pages URL in the [W3C Markup Validation Service](https://validator.w3.org/nu/).

| Page | URL | Errors | Warnings | Result | Screenshot |
| --- | --- | --- | --- | --- | --- |
| Home | `https://cyberjkb.github.io/mind-the-gap/index.html` | ⬜ | ⬜ | ⬜ To confirm | ![W3C result for index.html](docs/testing-images/html-index.webp) |
| Services | `https://cyberjkb.github.io/mind-the-gap/services.html` | ⬜ | ⬜ | ⬜ To confirm | ![W3C result for services.html](docs/testing-images/html-services.webp) |
| Contact | `https://cyberjkb.github.io/mind-the-gap/contact.html` | ⬜ | ⬜ | ⬜ To confirm | ![W3C result for contact.html](docs/testing-images/html-contact.webp) |
| Thank You | `https://cyberjkb.github.io/mind-the-gap/thank-you.html` | ⬜ | ⬜ | ⬜ To confirm | ![W3C result for thank-you.html](docs/testing-images/html-thank-you.webp) |

### CSS Validation (Jigsaw)

`assets/css/style.css` was validated with the [W3C CSS Validation Service (Jigsaw)](https://jigsaw.w3.org/css-validator/), by URI and/or file upload, using the **CSS level 3 + SVG** profile.

| File | Errors | Warnings | Result | Screenshot |
| --- | --- | --- | --- | --- |
| `assets/css/style.css` | ⬜ | ⬜ | ⬜ To confirm | ![Jigsaw result for style.css](docs/testing-images/css-style.webp) |

> **Note:** Jigsaw may show warnings that CSS custom properties (`var(--...)`) "cannot be statically checked". These are expected and do not count as errors. Validating by URI may also report issues in the Bootstrap CDN stylesheet. That file is third-party code and outside the scope of this project's custom CSS.

---

## Lighthouse Testing

Lighthouse reports were generated in Chrome DevTools (incognito window, to avoid interference from extensions) for every page in both **Desktop** and **Mobile** modes.

### Lighthouse Score Reference

| Category | Score Range | Indicator | Explanation |
| --- | --- | --- | --- |
| Performance | 90–100 | 🟢 | Fast loading and efficient at runtime |
| Performance | 50–89 | 🟠 | Moderate performance, with room for improvement |
| Performance | 0–49 | 🔴 | Poor performance, usually caused by heavy assets or blocking resources |
| Accessibility | 90–100 | 🟢 | Content is accessible to most users |
| Best Practices | 90–100 | 🟢 | Follows modern, secure web standards |
| SEO | 90–100 | 🟢 | Good visibility to search engines |

### Results Summary

| Page | Mode | Performance | Accessibility | Best Practices | SEO |
| --- | --- | --- | --- | --- | --- |
| Home | Desktop | ⬜ | ⬜ | ⬜ | ⬜ |
| Home | Mobile | ⬜ | ⬜ | ⬜ | ⬜ |
| Services | Desktop | ⬜ | ⬜ | ⬜ | ⬜ |
| Services | Mobile | ⬜ | ⬜ | ⬜ | ⬜ |
| Contact | Desktop | ⬜ | ⬜ | ⬜ | ⬜ |
| Contact | Mobile | ⬜ | ⬜ | ⬜ | ⬜ |
| Thank You | Desktop | ⬜ | ⬜ | ⬜ | ⬜ |
| Thank You | Mobile | ⬜ | ⬜ | ⬜ | ⬜ |

### Home Page

- **Desktop:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜
- **Mobile:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜

![Lighthouse desktop report for the home page](docs/testing-images/lighthouse-index-desktop.webp)
![Lighthouse mobile report for the home page](docs/testing-images/lighthouse-index-mobile.webp)

---

### Services Page

- **Desktop:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜
- **Mobile:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜

![Lighthouse desktop report for the services page](docs/testing-images/lighthouse-services-desktop.webp)
![Lighthouse mobile report for the services page](docs/testing-images/lighthouse-services-mobile.webp)

---

### Contact Page

- **Desktop:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜
- **Mobile:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜

![Lighthouse desktop report for the contact page](docs/testing-images/lighthouse-contact-desktop.webp)
![Lighthouse mobile report for the contact page](docs/testing-images/lighthouse-contact-mobile.webp)

---

### Thank You Page

- **Desktop:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜
- **Mobile:** Performance ⬜ · Accessibility ⬜ · Best Practices ⬜ · SEO ⬜

![Lighthouse desktop report for the thank-you page](docs/testing-images/lighthouse-thank-you-desktop.webp)
![Lighthouse mobile report for the thank-you page](docs/testing-images/lighthouse-thank-you-mobile.webp)

### Performance Considerations

- All raster images are WebP and have explicit `width`/`height` attributes to reduce Cumulative Layout Shift.
- `loading="lazy"` defers images below the fold. The above-the-fold logos load eagerly.
- `preconnect` hints for Google Fonts, and `display=swap` to avoid invisible text while the fonts load.
- No custom JavaScript, so the only script cost is the Bootstrap bundle and the Font Awesome kit.
- *Expected impact on mobile scores:* the third-party Font Awesome kit and Google Fonts can lower mobile Performance through render-blocking requests. Note any measured effect here.

---

## Accessibility Testing

### WAVE (WebAIM)

| Page | Errors | Contrast Errors | Alerts | Result | Screenshot |
| --- | --- | --- | --- | --- | --- |
| Home | ⬜ | ⬜ | ⬜ | ⬜ To confirm | ![WAVE report for the home page](docs/testing-images/wave-index.webp) |
| Services | ⬜ | ⬜ | ⬜ | ⬜ To confirm | ![WAVE report for the services page](docs/testing-images/wave-services.webp) |
| Contact | ⬜ | ⬜ | ⬜ | ⬜ To confirm | ![WAVE report for the contact page](docs/testing-images/wave-contact.webp) |
| Thank You | ⬜ | ⬜ | ⬜ | ⬜ To confirm | ![WAVE report for the thank-you page](docs/testing-images/wave-thank-you.webp) |

### Colour Contrast Checks

Checked with the [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/). The ratios are approximate. Confirm each one with the tool and record the exact figure.

| Foreground | Background | Used for | Approx. ratio | WCAG AA (normal / large) | Result |
| --- | --- | --- | --- | --- | --- |
| `--ink` #111111 | `--paper` #fff8e7 | Body text | ~18:1 | Pass / Pass | ⬜ To confirm |
| `--ink` #111111 | `--platform-yellow` #ffd300 | Comic buttons, captions | ~13:1 | Pass / Pass | ⬜ To confirm |
| #ffffff | `--tube-blue-dark` #000f66 | Footer text | ~17:1 | Pass / Pass | ⬜ To confirm |
| `--platform-yellow` #ffd300 | `--tube-blue-dark` #000f66 | Footer heading and links | ~12:1 | Pass / Pass | ⬜ To confirm |
| #ffffff | `--tube-blue` #0019a8 | Blue buttons | ~12:1 | Pass / Pass | ⬜ To confirm |
| #ffffff | `--tube-red` #dc241f | Distress buttons | ~5:1 | Pass / Pass | ⬜ To confirm |
| `--tube-blue` #0019a8 | `--paper` #fff8e7 | Headings | ~11:1 | Pass / Pass | ⬜ To confirm |

### Keyboard and Screen Reader

| Test | Expected | Result |
| --- | --- | --- |
| Tab through each page | Focus order is logical and the focus outline is visible on every link, button and field | ⬜ To confirm |
| Activate the hamburger menu with Enter or Space | The menu opens and closes | ⬜ To confirm |
| Screen reader (NVDA / VoiceOver) reads the social icons | Announces e.g. "Facebook (opens in a new tab)" | ⬜ To confirm |
| Screen reader reads the form labels | Each field is announced with its label | ⬜ To confirm |

---

## Bugs

### Fixed

| Bug | Cause | Fix | Status |
| --- | --- | --- | --- |
| Unstable navbar and grid behaviour | A Bootstrap 6 **alpha** CDN build was linked | Replaced with the stable Bootstrap **5.3.3** CSS and JS bundle, with SRI hashes | Fixed ✅ |
| Rotated first letter on headings had no effect | `::first-letter` does not support `transform` | Wrapped the first letter in `<span class="comic-tilt">` (inline-block), which can be rotated | Fixed ✅ |
| Form did not land on the thank-you page | The Web3Forms `redirect` used a relative path, which cannot resolve from the Web3Forms server | Used the absolute URL `https://cyberjkb.github.io/mind-the-gap/thank-you.html` | Fixed ✅ |

### Unfixed / Known Limitations

- The forms need a real Web3Forms access key in place of `YOUR_ACCESS_KEY_HERE` before they will send.
- A form submitted from a local copy redirects to the **live** thank-you page, because the redirect URL is absolute.
- *Add any issues found during final testing here.*

---

## Conclusion

> *Complete this after all tests have been run.*

Mind the Gap Man has been tested against every item on the submission checklist, every user story, every interactive feature, four viewport sizes and four browsers. It has also been checked with the W3C HTML and CSS validators, Lighthouse and WAVE. Fill in the summary of results here, e.g. "All pages pass W3C validation with no errors, Lighthouse scores are ... and no WCAG errors were found", together with any remaining known issues.

[Back to top](#mind-the-gap-man--testing-and-validation) · [Back to README](README.md)
