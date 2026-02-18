---
title: Home
layout: simple
og_type: website
---

# New Website Quickstart

This is the default landing page for a new website using the **XenoAtom** template.

This template extends [`lunet-io/templates`](https://github.com/lunet-io/templates) with XenoAtom organization defaults (base URL, owner metadata, favicon) and a distinctive warm purple-tinted dark background.

Use it as a setup checklist, then replace it with your real homepage content.

## 1) Create `config.scriban`

Reference the template and set project values:

```scriban
extend "XenoAtom/lunet_template"

site_project_name = "MyProject"
site_project_description = "Short project description."
site_project_logo_path = "/img/myproject-logo.png"
site_project_social_banner_path = "/img/myproject-banner.png"
site_project_banner_background_path = "/img/myproject-banner-background.png"
site_project_package_id = "MyProject"
site_project_github_repo = "MyProject"
site_project_basepath = "/myproject"

site_project_init
```

Notes:

- `site_project_logo_path` defaults to `/img/XenoAtom-logo.png` if not set.
- Favicon defaults to `/favicon.ico`. Override with `site_project_favicon_path`.
- Owner, license, and GitHub user are pre-set for XenoAtom. Override `site_project_*` values if needed.

## 2) Create top navigation `menu.yml`

Define the left and right navbar menus:

```yml
home:
  - {path: readme.md, title: "<i class='bi bi-house-door' aria-hidden='true'></i> Home"}
  - {path: docs/readme.md, title: "<i class='bi bi-book' aria-hidden='true'></i> Docs", folder: true}

home2:
  - {url: "https://github.com/<org>/<repo>/", title: '<i class="bi bi-github"></i> GitHub', link_class: btn btn-info}
```

- `home` is rendered on the left.
- `home2` is rendered on the right.

## 3) Add content pages

Typical starting structure:

```text
site/
  config.scriban
  menu.yml
  readme.md
  img/
    myproject-logo.png
    favicon.ico
  docs/
    readme.md
    getting-started.md
    menu.yml
```

## 4) Add docs menu (`docs/menu.yml`)

For docs pages, define a local docs menu:

```yml
doc:
  - {path: readme.md, title: "<i class='bi bi-book' aria-hidden='true'></i> User Guide"}
  - {path: getting-started.md, title: "<i class='bi bi-rocket-takeoff' aria-hidden='true'></i> Getting Started"}
```

## 5) Replace this default homepage

`readme.md` is the homepage (`/`). Keep frontmatter and replace this body with project-specific content.

## Build locally

```bash
lunet build
```

or:

```bash
lunet serve
```
