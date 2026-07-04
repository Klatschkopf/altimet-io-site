# altimet-io-site

Static site for <https://altimet.io> — the landing page plus the Privacy Policy
and Terms of Service for the **Altimet** Android app.

## How it works
- Source content is Markdown in `content/` (`index.md`, `privacy.md`, `terms.md`).
- A GitHub Actions workflow (`.github/workflows/deploy.yml`) converts it to HTML
  with **Pandoc** and publishes to **GitHub Pages** on every push to `main`.
- Custom domain `altimet.io` (DNS at Porkbun). HTTPS is auto-provisioned by
  GitHub Pages.
- **No cookies, no tracking, no third-party fonts** — system fonts only, by design.

## Update workflow
1. Edit a file in `content/`.
2. `git commit` + `git push`.
3. Live within ~60 seconds (check the Actions tab).

## Status
- Landing page: live.
- `privacy.md` / `terms.md`: **placeholders** — replaced with the finalized,
  legally-reviewed policy + terms (from `Taskapp/Documentation/05_Requirements/`)
  before app launch.
