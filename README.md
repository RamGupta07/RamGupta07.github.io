# Ram Gupta: portfolio site

Single static page for `https://ramgupta07.github.io` (GitHub Pages user site, repo `RamGupta07/RamGupta07.github.io`). Not published yet.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole site: inline CSS, a few lines of JS for the theme toggle, Google Fonts (Inter, Plus Jakarta Sans). |
| `assets/photo.webp` | 480 × 480 head-and-shoulders crop of my profile photo. |
| `assets/og-image.png` | 1200 × 630 link-preview image, rendered with Playwright. |
| `assets/favicon.svg` | "RG" monogram. |
| `assets/Ram_Gupta_Resume.pdf` | Copy of my current base resume. Re-copy it whenever the base resume changes. |
| `screenshots/` | Review screenshots (desktop 1440 px, mobile 390 px, light and dark). Not needed on the live site. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. |

## Preview locally

Open `index.html` in a browser, or run `python3 -m http.server 8000` in this folder and open `http://localhost:8000`.

## Theme

Light by default; dark when the visitor's system prefers it. The toggle in the nav overrides both and is remembered in `localStorage`. To make dark the default for everyone, swap the token blocks: move the dark values onto bare `:root` and the light values into the `prefers-color-scheme: light` and `[data-theme="light"]` blocks.

## Content rules

This README ships with the public repo, so it names no internal systems.

- Every claim on the page comes from my verified career notes (kept outside this repo). If it is not there, it is not on the page.
- Public page: no internal table, service or repository names, no customer names, no ticket keys, no code, no internal architecture images. The two diagrams are generic inline SVGs.
- Truthfulness: AI/Python since July 2026; "contributed to" the AI-driven development workspace; no design-doc counts; "investigated 247 bug tickets"; Java only as contributions; only skills I have used in production.
- Phone number is deliberately left off (it is on the resume PDF).
- Before every publish, run the banned-term grep from the portfolio plan in my notes against `index.html`.

## Publish (only with Ram's explicit OK for each step)

1. `gh repo create RamGupta07/RamGupta07.github.io --public`
2. Push this folder (without `screenshots/` if you prefer) to `main`.
3. Enable Pages from `main` / root (`gh api` if needed).
4. Check `curl -sI https://ramgupta07.github.io` returns 200 and the link preview shows the title, description and image.
