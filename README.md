# peejayedz.github.io (user site)

Sets **https://dashboard.lawfirmmarketingpros.com** as the custom domain for all of peejayedz's GitHub Pages sites.
Every project site is then served at `dashboard.lawfirmmarketingpros.com/<repo>/`, and old `peejayedz.github.io/<repo>/` links redirect there (path, query and `#` kept).

- `CNAME`: the custom domain.
- `index.html`: `/` opens the Builder (`/ghl-subaccount-builder-page/`).
- `404.html`: for any address that isn't a page.

Team paths are behind Cloudflare Access (Google sign-in, @lawfirmmarketingpros.com): `/ghl-subaccount-builder-page/`, `/leadpro-kpi/admin/`,
`/automation-review/admin/`, `/clockin-report/`, `/invoice-builder/`, `/ghl-marketing-dashboard/`,
`/agency-analytics-weekly-report/`, `/lfmp-kpi-scorecard/`, `/leadpro-kpi-mahdavi/`. Everything else (client KPI dashboards, review pages, `/leadpro-training/`, `/lfmp-team-training/` (shown inside GHL),
`/lfmp-oauth/`, `/mkm-luxury-kpi-dashboard/`, `/premier-builders-kpi/`) is public.

`/automation-review/preview/` was never behind Access: it was a public copy of the classic review page with one client's data.
Since 17 Nov 2026 it only shows the public "This review has moved" page (the old copy is in PJ's LFMP workspace `archive/`).

**Rollback:** remove the custom domain in this repo's Settings → Pages (or delete `CNAME`), then PJ removes the `dashboard` DNS record in Cloudflare.
All sites go back to `peejayedz.github.io/<repo>/` within minutes. DNS changes are made by PJ only.
