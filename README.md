# Green & Noble holding page

Temporary page for greenandnoble.co.uk until the full site launches.
Published from web-studio-sites/greenandnoble-holding (GitHub Pages, custom
domain greenandnoble.co.uk, set 18 Nov 2026).

## DNS at IONOS (greenandnoble.co.uk)

- `@` A records: 185.199.108.153, 185.199.109.153, 185.199.110.153,
  185.199.111.153 (replacing 217.160.0.81)
- `@` AAAA: delete the IONOS one (2001:8d8:100f:f000::200)
- `www`: delete its A and AAAA records, add CNAME www -> web-studio-sites.github.io
- Leave the MX and TXT records alone: they run Jason's Google Workspace email.

Then tick "Enforce HTTPS" in the repo's Settings > Pages once the
certificate is issued. If no certificate appears, remove and re-add the
custom domain on that settings page.

## At launch

Remove the custom domain from this repo first, then set greenandnoble.co.uk
as the cname on the main site (Website/.github/workflows/deploy.yml and
web-studio-sites/greenandnoble-www). DNS stays as it is.
