# houm.github.io

Static site for Houm, published with GitHub Pages: an overview of the app and its
[Privacy Policy](privacy.html).

## Structure

- `index.html` — landing page describing the app, its features, and the countries it operates in.
- `privacy.html` — privacy policy.
- `assets/styles.css` — shared stylesheet for both pages.
- `.github/workflows/deploy.yml` — GitHub Actions workflow that builds and deploys the site to GitHub Pages on every push to `main`.
- `.nojekyll` — disables Jekyll processing so the plain HTML/CSS is served as-is.

## Local preview

No build step is required. Serve the files with any static file server, for example:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deployment

The site deploys automatically via the `Deploy static site to GitHub Pages` workflow on
every push to `main`. One-time setup: in the repository **Settings → Pages**, set
**Build and deployment → Source** to **GitHub Actions**. After that, pushes to `main`
publish to `https://houm-so.github.io/houm.github.io/` (or the repo's configured custom
domain, if any).
