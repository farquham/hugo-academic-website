# Migration context (migrate/hugoblox-2026)

This branch was created to migrate the site to a newer HugoBlox starter and preserve authored content.

Summary of actions performed prior to this commit:
- Imported HugoBlox starter files and preserved `content/`, `static/`, and `data/` directories.
- Disabled legacy admin CMS content (moved `content/admin/index.md` to `content-disabled/admin/index.md`) because it referenced a removed output format.
- Added minimal fallback view partials to satisfy missing view fragments from the starter.
- Replaced deprecated `_build` front-matter keys with `build` where necessary to work with Hugo v0.162.
- Fixed file ownership issues for generated `public/` and `resources/` to avoid container permission errors.
- Updated site identity (params) to "Michael Farquharson" and added a `content/_index.md` to render home widgets.

Current work:
- This branch contains the migration changes. It builds locally in a Hugo container. Some deprecation warnings remain and visual theming may need adjustments.

Next steps:
- Visual QA and update theme params (email, LinkedIn, avatar) from canonical content.
- Re-enable or replace admin CMS with the new starter's admin flow if desired.

(Committed locally on branch `migrate/hugoblox-2026`. This commit will NOT be pushed per instructions.)
