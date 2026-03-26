# Reuben Thomas — Personal Portfolio

A single-page personal portfolio for Reuben Thomas, a Product Manager and UTD Honors Business Analytics student. The site showcases his experience, skills, and provides a way to get in touch.

**Live at:** (https://github.com/reubent-code/Personal-Portfolio)

---

## Overview

| Section | Description |
|---|---|
| **Hero** | Introduction, tagline, and call-to-action buttons |
| **About** | PM philosophy and core competency cards (Strategy, Analytics, Execution, Leadership) |
| **The Journey** | Work experience tiles — Adobe, Mercedes-Benz, Korn Ferry, Bonsai, Nike |
| **Skills & Tools** | Figma, SQL, Tableau, JIRA/Agile, JavaScript, Scrum Master, SDLC, HTML/CSS |
| **Contact** | Email form powered by Formsubmit.co + direct contact info |

---

## Tech Stack

- **HTML** — single `index.html` file, no build step required
- **Tailwind CSS** — loaded via CDN with a custom dark-mode design system
- **Google Fonts** — Manrope (headlines) + Inter (body)
- **Material Symbols** — icons via Google Fonts CDN
- **Formsubmit.co** — contact form backend (no server needed)

---

## Project Structure

```
Website/
├── index.html        # Main site (all sections)
├── design.md         # Design system reference (colors, typography, spacing)
├── Profile.JPG       # Hero headshot
├── nike-logo.svg     # Nike swoosh (white fill, used in experience section)
├── Adobe-Logo.png    # Adobe logo asset
├── KornFerry-logo.jpg
└── MB LOGO.png
```

---

## Running Locally

No build tools or dependencies required. Just open `index.html` in a browser:

```bash
open index.html
```

Or use any static file server:

```bash
npx serve .
```

---

## Contact Form Setup

The contact form submits to [Formsubmit.co](https://formsubmit.co). On the **first submission**, Formsubmit will send a one-time confirmation email to `reubenthomas03@gmail.com` — click the link in that email to activate the form.

---

## Contact

**Reuben Thomas**
- Email: reubenthomas03@gmail.com
- LinkedIn: [linkedin.com/in/reubent](https://www.linkedin.com/in/reubent)
- Phone: (214) 529-6721
