# Southbound Monitor — Sector Dashboard

A single, self-contained HTML dashboard for Hong Kong Stock Connect **southbound** holdings,
aggregated by GICS sector and theme (monthly, Jan 2025 – Jun 2026). All data is embedded in
`index.html`; the only external dependency is Chart.js loaded from a CDN. No build step, no server.

## Publish a public link with GitHub Pages (recommended)

This gives you a clean URL like `https://<your-username>.github.io/southbound-monitor/`.

1. Create a GitHub account if you don't have one: https://github.com/join
2. Create a new **public** repository — e.g. name it `southbound-monitor`.
   (github.com → **+** top-right → **New repository** → Public → **Create repository**)
3. Upload `index.html`:
   - On the repo page click **Add file → Upload files**, drag in `index.html`, then **Commit changes**.
4. Turn on Pages:
   - Repo **Settings → Pages**.
   - Under **Build and deployment → Source**, choose **Deploy from a branch**.
   - Branch: **main**, folder: **/ (root)** → **Save**.
5. Wait ~1 minute, then refresh the Settings → Pages panel. Your public link appears at the top:
   `https://<your-username>.github.io/southbound-monitor/`

To update the dashboard later, just upload a new `index.html` (same steps as 3); the link stays the same.

## Fastest alternative — GitHub Gist

1. Go to https://gist.github.com, create a **public** gist, paste the contents of `index.html`,
   name the file `index.html`, and **Create public gist**.
2. View it rendered via: `https://htmlpreview.github.io/?` + the **Raw** URL of your gist file.
   (Open the gist, click **Raw**, copy that URL, and prepend the htmlpreview prefix.)

## Notes

- **Data is public once you publish.** The holdings figures for all 107 stocks are embedded in the
  HTML source, so anyone with the link can read them. April 2026 was corrected from the A003/A004
  CCASS source files; Feb 2025 is interpolated (telecom names missing from that snapshot).
- The page needs internet access only to load Chart.js from the CDN. If you ever want a fully
  offline copy, the Chart.js `<script>` can be inlined on request.
