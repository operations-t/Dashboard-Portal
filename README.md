# Dashboard Portal

Single access point for the `operations-t` dashboards. The top bar stays fixed
at all times, so you can switch between dashboards or return Home from anywhere —
including while a dashboard is open.

Live: https://operations-t.github.io/Dashboard-Portal/

## Files

| File | Purpose |
|---|---|
| `index.html` | The portal itself |
| `links.txt` | **The list of dashboards — edit this to add or change links** |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |
| `README.md` | This file |

## Adding a new dashboard

Open `links.txt`, copy any existing block, change the values, and commit.
Nothing else needs editing — the portal reads this file every time it loads.

```
title: My New Dashboard
tag: JavaScript
desc: One-line description shown on the card.
embed: https://operations-t.github.io/my-new-dashboard/
repo: https://github.com/operations-t/my-new-dashboard
live: true
```

Rules:
- Leave one blank line between blocks.
- Lines starting with `#` are ignored.
- `embed` must be a **live GitHub Pages URL**. A plain `github.com` repo page
  cannot be embedded — GitHub blocks it in iframes.
- Set `live: false` for a dashboard that isn't deployed yet. It shows as
  "Standby" with a fallback link to the repo.

## Setup on GitHub

1. Upload all files to the repository root.
2. Settings → Pages → Build and deployment → Source → **Deploy from a branch**,
   branch `main`, folder `/ (root)`.
3. Wait for the deploy to finish, then open the live URL.
