# XenoAtom Lunet Template

Organization-level [lunet](https://github.com/lunet-io/lunet) template for all XenoAtom documentation sites. Extends the base [`lunet-io/templates`](https://github.com/lunet-io/templates) with XenoAtom-specific defaults.

## What this template provides

- **Organization defaults** — base URL (`xenoatom.github.io`), owner metadata, license, footer branding
- **Dark background override** — warm purple-tinted dark palette (`#1f1b25`) via `xenoatom-overrides.css`
- **Favicon and logo** — shared `favicon.ico` and `XenoAtom-logo.png`

Everything else (layouts, CSS, JS, bundles, search, Prism components, theme toggle) is inherited from `lunet-io/templates`.

## Layout

- `dist/config.scriban` — extends `lunet-io/templates`, sets XenoAtom defaults
- `dist/.lunet/css/xenoatom-overrides.css` — dark background color override
- `dist/favicon.ico` — shared favicon
- `dist/img/XenoAtom-logo.png` — default project logo

## How a project site consumes this template

1. Import the template:

   ```scriban
   extend "XenoAtom/lunet_template"
   ```

2. Set project-specific values in `site/config.scriban`:
   - `site_project_name`
   - `site_project_description`
   - `site_project_logo_path`
   - `site_project_social_banner_path`
   - `site_project_banner_background_path`
   - `site_project_package_id`
   - `site_project_github_repo`
   - `site_project_basepath`

3. Call `site_project_init` after site-specific properties are set.
