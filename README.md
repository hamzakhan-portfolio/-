# Hamza Khan — Portfolio

A cinematic, scroll-driven portfolio site for **Hamza Khan** — Full-Stack Developer, WordPress & AI Integration Specialist based in Karachi, Pakistan.

Single-page, single-file build: a pinned WebGL intro (glowing orb → silhouette → translucent black flower) driven by scroll, followed by About / Skills / Projects / Experience / Contact sections pulled from Hamza's CV.

## Tech stack

- Vanilla HTML/CSS/JS — no build step, no dependencies to install
- [Three.js](https://threejs.org/) r128 — procedural WebGL scene (glow sphere, particles, silhouette, layered flower geometry)
- [GSAP](https://gsap.com/) + ScrollTrigger — the pinned scroll sequence
- Google Fonts — Space Mono (display/mono) + Inter (body)
- Respects `prefers-reduced-motion` (disables the pinned animation and renders a static frame instead)

## Run locally

No build tools required — it's a single static HTML file.

```bash
# clone the repo, then from inside it:
python3 -m http.server 8000
# open http://localhost:8000
```

Or just double-click `index.html` to open it directly in a browser (some browsers restrict local file access for canvas/CORS edge cases, so a local server is the more reliable option).

## Deploy with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Choose the `main` branch and `/ (root)` folder, then **Save**.
5. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`.

No CI config or `gh-pages` branch needed since `index.html` sits at the repo root.

## Project structure

```
.
├── index.html      # entire site — markup, styles, and scripts in one file
├── LICENSE
├── README.md
└── .gitignore
```

## Editing content

All copy (headline, About/Skills/Projects/Experience/Contact text) lives directly in the HTML in `index.html` — search for the section by its `id` (`#about`, `#skills`, `#projects`, `#experience`, `#contact`) to edit. Site-wide colors, type, and spacing are defined as CSS custom properties at the top of the `<style>` block (`:root { ... }`).

## Contact

- Email: hamzashahid7297@gmail.com
- LinkedIn: [hamza-khan-016744368](https://www.linkedin.com/in/hamza-khan-016744368/)
- Fiverr: [fiverr.com/s/KerlLw4](https://www.fiverr.com/s/KerlLw4)

## License

MIT — see [LICENSE](LICENSE).
