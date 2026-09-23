# 0yman.github.io

Personal portfolio. Static HTML on GitHub Pages — no build step, no framework,
no dependencies beyond two Google Fonts.

**Live:** https://0yman.github.io

## Status

**Filled in.** The site now carries the two case studies it was promising, each
with the measured result that actually drove the design:

| Case study | The finding |
|---|---|
| [hybrid-rag-service](https://github.com/0yman/hybrid-rag-service) | Dense retrieval falls from 0.935 to 0.667 recall@3 on keyword queries where BM25 scores 1.000 — so the hybrid fusion came second on both query sets rather than first on either |
| [port-analyst-agent](https://github.com/0yman/port-analyst-agent) | Withholding the schema from the system prompt *raises* prompt tokens 5% and halves correct declines on unanswerable questions |

Single page by choice. A case study is worth its own URL when it has more to
say than fits in a screen; these two each have one number worth remembering,
and the repositories hold the full results.

## Stack

| | |
|---|---|
| Host | GitHub Pages (free, `main` branch, root) |
| Build | None — plain `index.html`, deploys on push |
| Type | Fraunces (headings) + Source Sans 3 (body) + system mono (measured values), via Google Fonts |
| Palette | bg `#F7F5EF` · sunk `#F1EEE4` · text `#17211F` · main `#8A5A1E` |

The palette and typefaces carry over from the first version of the site. What
is new is the mono voice, which exists because most of what is worth saying
here is a number.

## Local preview

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Checks worth repeating after an edit

- Every external link resolves (`curl -o /dev/null -w '%{http_code}' -L <url>`).
- The page reads at 400px wide — no horizontal scroll, metrics wrap rather than clip.
- Nothing on the page claims a number that is not in one of the two repositories.
