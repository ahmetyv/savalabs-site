# savalabs-site

Corporate one-pager for Sava Labs Ltd at https://savalabs.io.

Purpose: legal/corporate surface only (app store developer enrollment, PSP/bank KYC,
Companies House consistency). Never a product surface; product brands are not listed here.
Facts on the page must stay identical to the Companies House record (company 16124943).

- Static HTML in `public/`, served by nginx (Dockerfile).
- `/press/` = rudimentary press kit (boilerplate, fact sheet, marks in `public/assets/`,
  palette Paper/Ink/Loden/Brass, usage). Marks are text-based SVGs (system serif); replace
  with outlined-path vectors if the brand ever needs pixel-identical rendering everywhere.
- Deployed as a Coolify application on prod2, domains savalabs.io + www (www 301s to apex).
- Branch model: `prod` = live, `main` = integration (house convention).
- No JS, no tracking, no cookies, so no consent banner.
- `/health` returns 200 for uptime checks.
