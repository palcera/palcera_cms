# Palcera CMS

A ready-to-run **Drupal CMS distribution** for professional-services brochure sites:
Schema.org-modeled content (people, services, articles, pages), Canvas page building,
SEO defaults, search, and a polished token-driven theme.

## Requirements

- PHP 8.3+, Composer 2
- A database (MySQL/MariaDB) — or just use [DDEV](https://ddev.com)

## Install

```bash
composer create-project -s beta palcera/palcera_cms my-site
cd my-site
# with DDEV:
ddev config --project-type=drupal11 --docroot=web && ddev start
ddev drush site:install --yes --site-name="My Site" /var/www/html/recipes/palcera_base
ddev launch
```

Or run the interactive Drupal CMS installer (`ddev launch` before installing) and pick
the Palcera template.

## What you get

- Content types with Schema.org mappings and JSON-LD: Person, Article, Service, General Page
- A 9-section Canvas home page, listing pages (/services, /team, /articles), content
  templates for cards + full views
- SEO: metatags with token fallbacks, XML sitemap, pathauto, redirects, breadcrumbs
- Search, cookie consent, contact forms, editorial moderation, accessibility checker
- The [Palcera theme](https://github.com/palcera/palcera_theme) — fully design-token
  driven (see its README for no-rebuild rebranding)

## The pieces

| Package | Role |
|---|---|
| `palcera/palcera_cms` | this project template (Composer scaffolding) |
| `palcera/palcera_base` | the site recipe: content model, config, demo content |
| `palcera/palcera_theme` | the standalone Mercury-generated theme |
| `palcera/palcera_brochure` | the genericized marketplace site template derived from this stack |

## License

GPL-2.0-or-later.
