# 2027 Capacity Plan by Province

A self-contained, client-side capacity planning tool. No backend, no build step, no external services.

## Run locally
Open `index.html` in a browser, or serve the folder:

    python3 -m http.server 8000   # then visit http://localhost:8000

## Deploy (GitHub Pages)
1. Push this repo to GitHub (default branch `main`).
2. Go to **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. The included workflow (`.github/workflows/pages.yml`) publishes on every push to `main`.

Your site will be at `https://<user>.github.io/<repo>/`.

## Notes
- All third-party libraries (React 18.3.1, ReactDOM 18.3.1, htm 3.1.1) are vendored in `vendor/`, so the app works offline and has no CDN dependency.
- Plans are saved in the browser's `localStorage` (per browser, per site URL). Data is not shared between users or devices. Use the app's export features, if any, to back up or share plans.
- Do not commit sensitive/internal data into a public repo. Make the repository private (GitHub Pages on private repos requires a paid plan) if the defaults or content are confidential.
