# edgeone42.github.io

> Personal profile site for **Taylor Torres** (@edgeone42) — built with pure HTML/CSS/JS and deployed on GitHub Pages.

🌐 **Live site:** https://edgeone42.github.io

![GitHub Pages](https://img.shields.io/badge/deploy-GitHub%20Pages-58a6ff?style=flat-square)

---

## ✨ Features

- **Dark GitHub-style theme** — clean, modern, and easy on the eyes
- **Sticky glassmorphism navbar** — smooth-scroll anchors to every section
- **Typewriter effect** — rotating intro phrases in the hero (EN/中文)
- **Scroll-reveal animations** — powered by `IntersectionObserver`, with `prefers-reduced-motion` support
- **Live GitHub stats** — pulls real-time data from the **official GitHub API** (no third-party widgets):
  - Profile stats: repos, stars, forks, followers, following
  - Top languages: computed from repo language breakdowns, rendered as animated bars
- **SEO-ready** — meta description, Open Graph, Twitter Card, JSON-LD structured data, canonical URL
- **Fully responsive** — mobile-friendly layout

## 🛠 Tech Stack

- HTML5 / CSS3 (custom properties, grid, flexbox)
- Vanilla JavaScript (no frameworks, no build step)
- [GitHub REST API](https://docs.github.com/en/rest) — live data
- GitHub Pages — hosting

## 📁 Project Structure

```
.
├── index.html          # Single-page site (styles + markup + scripts)
└── (README.md)
```

The entire site lives in a single `index.html` — styles are in a `<style>` block and logic in a `<script>` block, keeping deployment a simple file push.

## 🚀 Local Development

Since there's no build step, just serve the folder with any static server:

```bash
# Option A: Python
python3 -m http.server 8080

# Option B: Node.js (npx)
npx serve .

# Then open http://localhost:8080
```

## 🎨 Customization

| What | Where |
|------|-------|
| Name / handle / bio | `.hero` section |
| Stats numbers | `.stats-grid` in `#stats` section |
| Project cards | `#projects` section |
| GitHub username (for live stats) | `GH_USER` constant in the script |
| Colors | CSS variables in `:root` |

To point the live stats at a different GitHub user, change:

```js
const GH_USER = 'edgeone42';
```

## 📝 Notes

- The **live stats** call the GitHub REST API anonymously (rate limit ≈ 60 req/h per IP), which is plenty for a personal site.
- If the API is unreachable, the cards fall back to a friendly error message instead of breaking the layout.

## 📄 License

[MIT](LICENSE) © Taylor Torres
