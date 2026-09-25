# JakartaUpdate — WordPress Media Framework

**Version 1.0.0** is a modular starter framework for Indonesian digital publishers. It packages a responsive theme, an editorial/core plugin, and an optional LIVE/TV plugin. The theme controls presentation, Core provides editorial/advertising utilities, and Live owns channel and program data.

## Package structure

- `jakartaupdate/` — WordPress theme.
- `jakartaupdate-core/` — breaking ribbon, ticker, video post type, social links, ad slots, basic view counts, fallback SEO metadata/schema and admin settings.
- `jakartaupdate-live/` — channel/program post types and secure constrained stream output.
- `docs/` — installation and operations guides.

## Requirements

WordPress 6.2 or newer and PHP 8.1 or newer. HTTPS is required for streams. Works with standard WordPress menus, Gutenberg content, common caching plugins and WooCommerce templates in principle; a full compatibility matrix needs validation against each site's active plugins and hosting stack.

## Install

Upload and activate the theme, then upload and activate Core. Install Live only if needed. Create a page named “Live” with `[ju_live_tv]`; configure **Appearance → Customize → JakartaUpdate → Live page URL**. See [INSTALL.md](INSTALL.md).

## Not a claim of complete production verification

This package is a functional, extensible first release, not a guarantee of universal compatibility or broadcast reliability. The source is syntax-checked in this environment; live hosting, third-party SEO plugins, real stream endpoints, analytics consent requirements, and all viewport/plugin combinations must be tested on the target WordPress installation. Known gaps and setup steps are in `docs/ADMIN-GUIDE.md`.
