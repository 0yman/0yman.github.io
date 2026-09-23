# Empty but live — deployment record

## The deliverable

**Live URL: https://0yman.github.io**

| | |
|---|---|
| Repo | https://github.com/0yman/0yman.github.io (public) |
| Host | GitHub Pages — free tier, `main` branch, root path |
| Stack | Static HTML, no build step — matches the content map's plain multi-page plan |
| HTTPS | Enforced (`Strict-Transport-Security` present) |
| First commit | `be9aa31` — "Empty but live: name, claim, and a URL that resolves" |

## Verified live, not just deployed

Checked against the public URL over the internet, not a local file:

```
$ curl -sI https://0yman.github.io/
HTTP/1.1 200 OK
Server: GitHub.com
Content-Type: text/html; charset=utf-8
Content-Length: 3014
Strict-Transport-Security: max-age=31556952

$ curl -s https://0yman.github.io/ | grep -E 'class="(name|claim)"'
<h1 class="name">Ayman</h1>
<p class="claim">I build AI features that refuse to be confidently wrong.</p>
```

```
$ gh api repos/0yman/0yman.github.io/pages --jq .status
built
```

Screenshots (`screenshot-desktop.png`, `screenshot-mobile.png`) were both captured **against the live URL**, not the local file — 1280×800 and 390×844 (iPhone 14 Pro viewport). Custom fonts load correctly from Google Fonts in both.

## The one step left for you

**Open https://0yman.github.io on your phone.** The brief asks for a second *physical* device, and the 390×844 headless capture proves the responsive layout works but not that the site resolves over cellular/another network — that check is genuinely yours to make. It should take about ten seconds.

## Next deploy

```bash
git add -A
git commit -m "..."
git push          # Pages rebuilds automatically, live in ~30-60s
```
