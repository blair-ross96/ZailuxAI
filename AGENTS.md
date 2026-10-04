# Base44 Dev Environment

## Project
Static single-page marketing site for "Zailux — AI Receptionist." A single `index.html` with inline CSS/JS, Tailwind via CDN, and Google Fonts. No build step, no backend, no dependencies.

## Running
```
docker compose -f docker-compose.base44.yml up -d
```
Serves `index.html` via nginx on host port 3000. Files are bind-mounted read-only, so edits to `index.html` are reflected immediately on refresh — no reload needed.

## Notes
- No secrets required. The only external API call is a public currency-rate endpoint (`open.er-api.com`), no credentials.
- Deployed to GitHub Pages in production via `.github/workflows/static.yml`.
