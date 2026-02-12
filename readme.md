# Lunet Website Template

This repository contains the shared [lunet](https://github.com/lunet-io/lunet) website template used by XenoAtom project docs sites.

## Layout

- `dist/.lunet/` — shared Lunet layouts, CSS, and JS assets
- `dist/config.scriban` — shared Lunet config (everything except site-specific values)
- `dist/404.md` — default 404 page
- `dist/banner.md` — default social/banner capture page
- `dist/.nojekyll` — GitHub Pages setting

## How a project site consumes this template

1. Import shared config from this template:

   ```scriban
   extend "XenoAtom/lunet_template@1.0.0"
   ```

2. Keep project-specific values in `site/config.scriban` only:
   - `site_project_name`
   - `site_project_description`
   - `site_project_logo_path`
   - `site_project_social_banner_path`
   - `site_project_banner_background_path`
   - `site_project_package_id`
   - `site_project_github_repo`
   - `site_project_basepath`

3. Call `site_project_init` after site-specific properties are set.

## Notes

- `dist` is the artifact-like source of truth for template content.
- Do not add `site/.lunet/build` outputs to this template.
