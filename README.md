# Glassmorphic 3D Calculator

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

A fully functional calculator with a frosted-glass (glassmorphism) design and real-time 3D mouse-tilt effect. Move your cursor over the card and watch it respond in 3D space — powered by VanillaTilt.js.

---

## ✨ Features

- **Glassmorphism card** — `backdrop-filter: blur(20px)` with semi-transparent border
- **3D mouse tilt** — VanillaTilt.js rotates the card up to 25° following the cursor
- **Glare effect** — moving light reflection on tilt
- **3D button depth** — buttons use `translateZ` to pop out of the card plane
- **Colour-coded keys** — C (red), + (purple, tall), = (gradient)
- **Ambient background orbs** — two blurred gradient circles for atmosphere
- **Keyboard support** — type numbers/operators, `Enter` to calculate, `Escape` to clear

---

## 🔴 Live Demo

**[👉 View Live Demo](https://github.com/professoralbay/glassmorphic-calculator-page/)**


## 🎬 Demo

![Demo](screenshot.gif)


## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Form structure, inline onclick handlers |
| CSS3 | Glassmorphism, `translateZ`, gradients |
| VanillaTilt.js | 3D mouse-tracking tilt (CDN) |
| Vanilla JS | Keyboard input support |

---

## 📁 Project Structure

```
glassmorphic-calculator/
├── index.html
└── README.md
```

---

## 🚀 Getting Started

```bash
git clone https://github.com/professoralbay/glassmorphic-calculator.git
open index.html
```

---

## 🧩 Challenges & How I Solved Them

**1. Glassmorphism cross-browser**
Added both `backdrop-filter` and `-webkit-backdrop-filter` for Safari support. Without the webkit prefix, the frosted effect breaks on iOS.

**2. Buttons feeling flat inside a tilted card**
Used `transform: translateZ(10px)` on buttons and `translateZ(20px)` on the form itself. This layers them above the tilt plane so they appear to float.

**3. Glare overlay clipping incorrectly**
VanillaTilt injects a `.js-tilt-glare` div dynamically. Applied `border-radius: 24px` to match the card's rounded corners.

**4. `eval()` crashing on bad input**
Wrapped the keyboard `Enter` handler in `try/catch` — shows `"Error"` on invalid expressions instead of breaking the page.

---

## 📄 License

MIT

> Inspired by [smrtpage/Glassmorphic-3D-Calculator](https://github.com/smrtpage/Glassmorphic-3D-Calculator). Rebuilt with keyboard support and enhanced button depth system.

*Made by [Akın Üner](https://github.com/professoralbay)*
