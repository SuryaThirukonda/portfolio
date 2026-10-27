# surya thirukonda - portfolio

Personal portfolio, plain static HTML/CSS/JS with no build step. Deploys anywhere that serves static files.

- `index.html` - the whole site: layout, styles, content data, project detail sheets, command palette, live GitHub activity, and theme toggle
- `assets/projects/<id>/` - screenshots for each project (`01.webp`, `02.webp`, ...) plus a `cover.webp` card image
- `assets/` - headshot and resume PDF

## Editing content

Every card, role, award and detail sheet renders from the `WORK`, `PROJECTS` and `AWARDS` lists at the top of the script in `index.html`. To add a project, add one object there and drop its screenshots in `assets/projects/<id>/`. Each `images` entry is `[width, height, caption]` in file order. Projects without screenshots get a generated cover.

Detail sheets are deep-linkable: `/#/tempo` opens Tempo directly.

## Live data

The "Latest push" button, the Activity section, the "Updated" labels on cards and the public-repo count come from the public GitHub API at page load (4 requests, cached in `localStorage` for 10 minutes). Repos listed in `GH_HIDE` (`autoapply`, `autobot`) never appear. If GitHub rate-limits a visitor, the page shows its cached copy; with no cache it falls back to the `SNAPSHOT` baked into `index.html`.

## Look

Light mode by default; the moon button switches to dark and remembers the choice. Type is SF Pro Display / SF Pro Text / SF Mono, which render natively on Apple devices and anywhere they are installed. Apple's license doesn't allow serving SF as a web font, so other systems fall back to Inter.

Press `/` or `⌘K` (`Ctrl K`) to search projects, sections and actions.
