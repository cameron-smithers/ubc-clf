# UBC CLF Hugo Theme

A Hugo theme that wraps the UBC CLF 7.0.5 shell using CDN-hosted assets and configurable unit metadata.

> Note: This theme is not in production use yet. Treat it as a work-in-progress and validate in your own environment before deploying.

## Requirements
- Hugo `>= 0.152.2` (tested)
- Uses CDN assets `//cdn.ubc.ca/clf/7.0.5` and jQuery 1.12.4

## Install
- Clone or copy into your site at `themes/ubc-clf`
- In `config.toml|yaml|json` set `theme = "ubc-clf"`

## Configure
- Menus: define main navigation via `[menu.main]` entries (prefer `pageRef` for pages you own so links stay in sync)
- Unit details under `[params]`:
  - `unit_name`, `faculty_name`, `campus_label`, `unit_url`
  - `address_campus`, `address_street`, `address_city`, `address_province`, `address_province_code`, `address_country`, `address_postal`
  - `phone`, `email`
  - `social.facebook`, `social.twitter`, `social.youtube`
- Optional: add custom JS paths in `params.custom_js` (array) and overrides in `static/css/custom.css`

## Example site
- See `exampleSite/hugo.toml` for a working config
- Run locally from repo root: `hugo server -s exampleSite --themesDir ..`

## Notes
- Full-width layout by default; IE conditionals are removed
- Content renders in `main` as standard Hugo `.Content`; homepage uses `layouts/index.html`
