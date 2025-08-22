# Opt-Out Dashboard (Static)

A local-first, static HTML/JS tool to guide and track data-broker opt-outs.
- No server required. Host on Vercel, GitHub Pages, or open over HTTPS locally.
- Your profile and progress are stored in the browser (localStorage).
- Data lives in `data/brokers.json`.

## Deploy (Vercel)
1. Create a new GitHub repo and add the contents of this folder.
2. In Vercel, “Import Project” → pick the repo → Framework Preset: **Other** → Root: `/`.
3. Build & Output settings can be left empty (static).

## Local Dev
- Use any static file server (e.g., `python -m http.server`) and open http://localhost:8000
- Opening `index.html` directly from the file system may block `fetch` of JSON due to browser CORS. Use a local server.

## Data
- Update `data/brokers.json` with new entries or flags.
- Columns expected:
  - Group Key, Parent Company, Broker Name, Relationship Type, Cascade Opt-Out?,
  - Opt-Out Method, Opt-Out URL/Email, Required Info, Notes, How to Initiate Opt-Out

## Notes
Many brokers require Captcha, email/SMS verification, or account login. This tool prepares prefilled emails and copy-paste steps and tracks status, rather than bypassing security controls.
