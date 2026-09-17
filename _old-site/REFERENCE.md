# Old site snapshot (pre-consolidation)

A reference copy of `ujwalkandi.in` as it was **before** the September 2026
consolidation, when each section was its own repo and its own GitHub Pages
deployment. Kept for design reference — what the old pages looked like and which
CSS produced it.

Hugo does not publish this folder. It is not one of Hugo's known directories
(`content/`, `static/`, `layouts/`, `assets/`, `data/`, …), so the build ignores
it entirely. Nothing here is reachable on the live site.

## Layout

Mirrors the old multi-repo site as it was served, with the root being the
homepage repo and each section nested beneath it:

| Path | Was served at | Came from |
| --- | --- | --- |
| `index.html`, `index.json`, `index.xml` | `/` | `ujwalkandi.github.io` |
| `about/` | `/about/` | `about` repo |
| `projects/` | `/projects/` | `projects` repo |
| `links/` | `/links/` | `links` repo |
| `archive/index.html` | `/archive/` | `archive` repo |
| `_config.yml`, `_layouts/` | — | homepage repo (stale Jekyll-era leftovers, never live) |

## Stylesheets

Four genuinely different files, all kept at their original paths — do not assume
they are duplicates:

| File | Notes |
| --- | --- |
| `assets/css/main.css` | homepage stylesheet |
| `about/about.css` | what `/about/` actually loaded |
| `projects/projects.css` | byte-identical to `about/about.css` |
| `assets/css/about.css` | stale variant sitting in the homepage repo, not what `/about/` loaded |
| `assets/css/projects.css` | ditto, and a different size again |

Both per-page files are the full old PaperMod bundle. That bundle is worth
keeping: it scopes its markdown typography to `.post-content`, whereas current
PaperMod scopes the equivalent rules to `.md-content`. Copying the old class
names without the old CSS is what broke the About and Projects typography during
the migration.

## Deliberately excluded

Large binaries that are already preserved verbatim elsewhere in this repo, so
they are not duplicated here:

| Excluded | Already at |
| --- | --- |
| `archive/img/`, `archive/assets/` (~220 MB) | `static/archive/` |
| `projects/files/` (~14 MB) | `content/projects/<project>/` |
| `assets/img/`, `assets/Ujwal_Kandi_Resume.pdf` | `static/assets/` |

Everything present here is byte-identical to the original.

## Full history

The four standalone repos still exist on GitHub, renamed with an `-old` suffix
(`about-old`, `projects-old`, `links-old`, `archive-old`) — they were renamed
rather than deleted because GitHub Pages reserves the URL path
`username.github.io/<reponame>` for any repo of that name, which kept
`/about/` and friends from falling through to this repo. Their full commit
history lives there. The old homepage state is in this repo's own history, at
the commit before the consolidation.
