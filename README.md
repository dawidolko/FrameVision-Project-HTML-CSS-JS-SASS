# FrameVision

> 📸 **One page, five sections, no framework** — a photography studio site where the scroll animations and the booking modal are hand-written

**FrameVision** is a single-page site for a photography studio: opening header, about, services, team and contact. Sections reveal as they enter the viewport, the navigation gains a background once you scroll past the header, a scroll-to-top button appears after 450 pixels, and a booking modal collects a name and a phone number with its own validation.

All of it is vanilla JavaScript and SCSS — no framework, no animation library, no build step beyond compiling the stylesheet.

![HTML5](https://img.shields.io/badge/HTML5-semantic-E34F26?logo=html5&logoColor=white)
![Sass](https://img.shields.io/badge/Sass-SCSS-CC6699?logo=sass&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black)
![WebP](https://img.shields.io/badge/Images-WebP%20%2B%20fallback-0A84FF)
![License](https://img.shields.io/badge/License-MIT-green)

**Live:** [framevision.dawidolko.pl](https://framevision.dawidolko.pl)

---

## 🎯 Key Features

- **Reveal animations written by hand** — elements marked `.reveal`, `.move` and `.moves` are checked against the viewport on scroll, each with its own trigger distance. No IntersectionObserver polyfill, no library.
- **A navigation that reacts to position** — the bar picks up a background after 50 pixels of scroll, so the opening photograph is not covered by a solid strip.
- **A burger menu that closes itself** — tapping any link inside the open menu closes it, which is the behaviour people expect and the one most hand-rolled menus forget.
- **A booking modal with validation** — name and phone are checked before submission and the fields are cleared on each open, so a second booking never starts with the previous person's details.
- **A scroll-to-top button that stays out of the way** — it only appears once there is something to scroll back from.
- **WebP with a JPG fallback** — every photograph ships in both formats.
- **SCSS split by breakpoint** — colours, sizes and mixins as partials, with `_small`, `_medium` and `_large` holding the responsive rules rather than scattering media queries.
- **Skip link and landmarks** — `#main-content` and named sections make keyboard navigation work.

---

## 🧩 The Page

| Section      | What it does                                              |
| ------------ | --------------------------------------------------------- |
| **Header**   | Full-bleed photograph with the booking call to action.     |
| **About**    | The studio, revealed on scroll.                            |
| **Services** | What is offered, as cards.                                 |
| **Team**     | The photographers.                                         |
| **Contact**  | Details and the booking modal.                             |

---

## 🛠️ Technology Stack

| Technology       | Role                                                       |
| ---------------- | ---------------------------------------------------------- |
| **HTML5**        | Semantic single-page markup with landmarks.                |
| **SCSS**         | Variables, mixins and one partial per breakpoint.          |
| **JavaScript**   | Scroll effects, burger menu, modal and validation.         |
| **Font Awesome** | Icon set.                                                  |

---

## 🚀 Getting Started

### Prerequisites

- Any static web server (or just a browser)
- Sass, if you intend to change the styles

### 1. Clone the repository

```bash
git clone https://github.com/dawidolko/FrameVision-Project-HTML-CSS-JS-SASS.git
cd FrameVision-Project-HTML-CSS-JS-SASS
```

### 2. Open it

```bash
open index.html          # or serve the directory
python3 -m http.server   # http://localhost:8000
```

### 3. Work on the styles

```bash
sass --watch sass/main.scss css/style.css
```

---

## 📁 Project Structure

```
FrameVision-Project-HTML-CSS-JS-SASS/
├── index.html        # the whole page: header, about, services, team, contact
├── js/
│   └── main.js       # nav background, burger, scroll-to-top, reveals, booking modal
├── sass/
│   ├── main.scss     # entry point
│   ├── _colors.scss  _sizes.scss  _mixins.scss
│   └── _small.scss  _medium.scss  _large.scss
├── css/              # compiled stylesheet
├── img/              # photographs, WebP + JPG
├── icons/            # section icons
└── robots.txt
```

---

## 📄 License

MIT © [Dawid Olko](https://dawidolko.pl)
