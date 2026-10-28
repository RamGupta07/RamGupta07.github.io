# Ram Gupta: portfolio site

Single static page for `https://ramgupta07.github.io` (GitHub Pages user site, repo `RamGupta07/RamGupta07.github.io`). Not published yet.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole site: inline CSS, inline JS for the theme toggle, mobile menu, scroll-spy, skills toggles, copy-email and back-to-top. |
| `assets/fonts/` | Self-hosted Latin subsets of Inter (variable, 400–700) and Instrument Serif (400), from Google Fonts. |
| `assets/photo.webp` | 480 × 480 head-and-shoulders crop of my profile photo. |
| `assets/og-image.jpg` | 1200 × 630 link-preview image (JPEG, quality 80). |
| `assets/favicon.svg` | "RG" monogram. |
| `assets/apple-touch-icon.png` | 180 × 180 home-screen icon rendered from the favicon with square corners (iOS rounds them itself). |
| `assets/Ram_Gupta_Resume.pdf` | Copy of my current base resume. Re-copy it whenever the base resume changes. |
| `screenshots/` | Review screenshots for every tested viewport, light and dark. Not needed on the live site. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. |

## Preview locally

Open `index.html` in a browser, or run `python3 -m http.server 8000` in this folder and open `http://localhost:8000`.

## Theme

Always light by default, whatever the visitor's system setting: a small script in `<head>` sets `data-theme="light"` before the page renders. Dark applies only after the visitor uses the toggle in the nav, and that choice is remembered in `localStorage`. To make dark the default instead, change that script to set `dark`, and to switch to light only when `localStorage` holds `light`.

## Content rules

This README ships with the public repo, so it names no internal systems.

- Every claim on the page comes from my verified career notes (kept outside this repo). If it is not there, it is not on the page.
- Public page: no internal table, service or repository names, no customer names, no ticket keys, no code, no internal architecture images. The two diagrams are generic inline SVGs.
- Truthfulness: AI/Python since July 2026; "contributed to" the AI-driven development workspace; no design-doc counts; "investigated 247 bug tickets"; Java only as contributions; only skills I have used in production.
- Phone number (+91 83054 23483) is shown in the Contact card (call + WhatsApp) and the mobile menu, at Ram's request.
- Before every publish, run the banned-term grep from the portfolio plan in my notes against `index.html`.

## Publish (only with Ram's explicit OK for each step)

1. `gh repo create RamGupta07/RamGupta07.github.io --public`
2. Push this folder (without `screenshots/` if you prefer) to `main`.
3. Enable Pages from `main` / root (`gh api` if needed).
4. Check `curl -sI https://ramgupta07.github.io` returns 200 and the link preview shows the title, description and image.
