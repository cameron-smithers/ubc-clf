# UBC CLF Hugo Theme

A Hugo theme that wraps the UBC CLF 7.0.5 shell using CDN-hosted assets and configurable unit metadata.

## Setup
- Copy or symlink this theme under `themes/ubc-clf`.
- In your site `config.toml|yaml|json` set `theme = "ubc-clf"`.
- Define navigation via `[menu.main]` entries.
- Populate unit details in `[params]`:
  - `unit_name`, `faculty_name`, `campus_label`, `unit_url`
  - `address_campus`, `address_street`, `address_city`, `address_province`, `address_province_code`, `address_country`, `address_postal`
  - `phone`, `email`
  - `social.facebook`, `social.twitter`, `social.youtube`
- Optional: add custom JS paths in `params.custom_js` (array) and add overrides to `static/css/custom.css`.

## Notes
- Uses CDN assets: `//cdn.ubc.ca/clf/7.0.5` and jQuery 1.12.4.
- Full-width layout by default; drop IE conditionals.
- Content renders in `main` as standard Hugo `.Content`; homepage uses `layouts/index.html`.
