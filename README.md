# 0yman.github.io

Personal portfolio. Static HTML on GitHub Pages: no build step, no framework,
no dependencies beyond one Google Fonts family.

**Live:** https://0yman.github.io

## What is on it

Two case studies, each with the measured result that changed the design, and
the work in progress:

| Section | The finding |
|---|---|
| Hero | A recorded run of the live agent (Ministral 14B) on the revenue trap question, replayed step by step: its real SQL, step times, the figure check, and the currency symbol the guard took out |
| [ask-your-data](https://github.com/0yman/ask-your-data) | A one-sentence prompt rule against invented currency symbols cost 2.3 of 12 hard questions, so the fix moved into code after the answer. The same code scored 8.3 to 10.7 across sessions, so every change is now measured interleaved with the committed code. |
| [hybrid-rag-service](https://github.com/0yman/hybrid-rag-service) | Dense retrieval falls to 0.667 recall@3 on keyword queries where BM25 scores 1.000, so at k=3 BM25 alone was the safest retriever, not the hybrid. |
| Now | AYD-0.1, a 9B SQL agent model fine-tuned on execution-verified conversations. No numbers until they are measured. |

Single page by choice. The repositories hold the full results.

## Stack

| | |
|---|---|
| Host | GitHub Pages (free, `main` branch, root) |
| Build | None: plain `index.html`, deploys on push |
| Type | Geist (text) and Geist Mono (measured values), via Google Fonts |
| Palette | Neutral canvas with one emerald accent. Light: canvas `#f7f8f9`, surface `#fdfdfd`, text `#0f1012`, accent `#0d7d56` (white text). Dark: canvas `#08090a`, surface `#0f1011`, text `#f7f8f8`, accent `#2fbf8a` (near-black text), links `#34d399` |
| Theme | Light and dark follow the visitor's system setting |

The layout and type match the live demo of ask-your-data; the accent is its own.

## Local preview

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Checks worth repeating after an edit

- Every external link resolves (`curl -o /dev/null -w '%{http_code}' -L <url>`).
- The page reads at 375px wide in both themes, with no horizontal scroll.
- Every text colour pair holds 4.5:1 contrast or better.
- Nothing on the page claims a number that is not in one of the repositories.
