# surya thirukonda - portfolio

Personal portfolio, pure static HTML/CSS/JS with no build step. Deploys anywhere that serves static files.

- `index.html` - the whole site: layout, styles, the 3D ASCII name renderer, ambient background, ASCII portrait, terminal palette, GitHub ticker, and theme toggle
- `assets/` - headshot and resume PDF

Live data: the footer ticker reads the public GitHub events API at page load and stays hidden if the request fails.

Themes: follows `prefers-color-scheme` by default; the nav toggle pins light or dark and persists in `localStorage`.
