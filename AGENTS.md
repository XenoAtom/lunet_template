# lunet_template - Codex Agent Instructions

This repository is the shared Lunet template used by other XenoAtom documentation websites.

Paths and commands below are relative to this repository root.

## Repository Scope

- This repo is a reusable template, not a single project website.
- Keep shared layouts/assets/config in `dist/`.
- Keep content generic and reusable across consumer sites.

## Structure

- `dist/.lunet/layouts/**` -> shared HTML layouts
- `dist/.lunet/css/**` -> shared styles
- `dist/.lunet/js/**` -> shared scripts
- `dist/config.scriban` -> shared template config/functions
- `dist/readme.md` -> local placeholder landing page for template preview
- `dist/menu.yml` -> local placeholder nav menus for template preview
- `dist/404.md` -> default 404 page for template consumers

## Local Iteration

Install lunet (once):

`dotnet tool install -g lunet`

Build locally from the template root:

`cd dist`

`lunet build`

Optional local preview:

`lunet serve`

Notes:

- Local outputs are generated under `dist/.lunet/build/` and should not be committed.
- `dist/readme.md` is intentionally a placeholder so this template can be validated in isolation.
- `dist/menu.yml` is intentionally a placeholder and is expected to be overridden by consumer sites.

## Contribution Notes

- Prefer changes that stay template-level and avoid project-specific branding/content.
- If a change affects template defaults, verify by running `lunet build` from `dist/`.
- Keep consumer-facing defaults in `dist/config.scriban`; avoid duplicating values in pages/layouts when config can drive them.
