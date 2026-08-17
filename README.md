# 0yman.github.io

Personal portfolio. Static HTML on GitHub Pages — no build step, no framework, no dependencies beyond two Google Fonts.

**Live:** https://0yman.github.io

## Status

**Empty but live.** This is deliberately a near-blank page: the name, the one-line claim, and nothing else. The point of this milestone is that the URL exists and resolves, so build week is filling in a site that already ships rather than starting from zero.

## Stack

| | |
|---|---|
| Host | GitHub Pages (free, `main` branch, root) |
| Build | None — plain `index.html`, deploys on push |
| Type | Fraunces (headings) + Source Sans 3 (body), via Google Fonts |
| Palette | bg `#F7F5EF` · text `#17211F` · main `#8A5A1E` |

Matches the identity kit and the static multi-page content map (`/`, `/work/image-relevance`, `/work/triage-api`, `/about`).

## Next

Per the content map, in order:

1. Home — masthead + claim, proof panel, selected work (capstone first), how I work, about strip, contact
2. `/work/image-relevance` — the lead case
3. `/work/triage-api`
4. `/about`

## Local preview

```bash
python -m http.server 8000
# then open http://localhost:8000
```
