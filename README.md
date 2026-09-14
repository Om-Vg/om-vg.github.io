# om-vg.github.io

Personal portfolio site for Om Venugopal — Security Engineer (AppSec / DevSecOps).

Live at: https://om-vg.github.io/

## Stack

Static site, no build step or framework:

- `index.html` — page markup
- `css/style.css` — all styles
- `js/app.js` — custom cursor, scroll reveals, feed tabs, GitHub activity feed
- `assets/` — favicon and Open Graph image
- `robots.txt`, `sitemap.xml` — basic SEO

The "Daily Output" section pulls live data from the public GitHub REST API
(`api.github.com/users/Om-Vg/...`) client-side — no backend or API key
required, but it is subject to GitHub's unauthenticated rate limit (60
requests/hour/IP).

## Running locally

No build step. Either open `index.html` directly in a browser, or serve it
so relative paths behave the same as production:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Pushes to `main` deploy automatically via GitHub Pages.

## CI

`.github/workflows/check.yml` runs an HTML validator and a link checker on
every push and pull request.
