# CLAUDE.md — Site maintenance notes

Personal academic website for **Weibo Sun**, built on the **Academic Pages**
Jekyll template (a fork of Minimal Mistakes). Hosted on **GitHub Pages** at
<https://webberrr7.github.io>. Pushing to `master` triggers an automatic Jekyll
rebuild (~1–2 min). There is no Ruby/Jekyll toolchain on this machine, so builds
are verified on GitHub, not locally — unless the user runs `bundle exec jekyll serve`.

## How the pieces fit together

| File / dir | Controls |
|---|---|
| `_config.yml` | Site-wide config: title, author/sidebar block (avatar, bio, email, social), `collections:` declarations, `defaults:`, plugins. **Changes here require restarting `jekyll serve`** (not auto-reloaded). |
| `_data/navigation.yml` | The top menu bar **only** — ordered list of `title` + `url`. Removing an entry hides the link but does NOT delete the page/content. |
| `_pages/` | Standalone pages. Each is reachable via its `permalink`; it appears in the menu only if `navigation.yml` links to that permalink. |
| `_includes/` | Reusable HTML fragments (e.g. `footer.html`, `archive-single.html`, `author-profile.html`). |
| `_layouts/` | Page templates (`single`, `archive`, `talk`, etc.) referenced by `layout:` front matter. |
| `_sass/` , `assets/` | Styling and compiled CSS/JS. |
| `files/` | Static downloads (PDFs, bib). Served at `/files/...`. |
| `images/` | Images. Profile photo is `images/profile.png` (set via `author.avatar` in `_config.yml`). |

## Collections (content that auto-lists)

Declared under `collections:` in `_config.yml`. Each item is one `.md`/`.html`
file in the matching folder; a listing page in `_pages/` loops over the folder
and renders each via `{% include archive-single.html %}`.

| Collection folder | Listing page (`_pages/`) | Nav label | Item URL pattern |
|---|---|---|---|
| `_publications/` | `publications.html` | Publications | `/publications/:path/` |
| `_talks/` | `talks.html` | Talks | `/talks/:path/` |
| `_teaching/` | `teaching.html` | Teaching | `/teaching/:path/` |
| `_posts/` | `year-archive.html` | Blog Posts | (dated permalink) |

Note: there is **no** `_portfolio/` collection. The Portfolio nav entry points at
`/portfolio/`, which is a hand-written page tree in `_pages/` (see below).

A collection needs THREE things to work: (1) a `_folder/`, (2) an entry under
`collections:` in `_config.yml` with `output: true` + `permalink`, and usually a
matching block under `defaults:`, and (3) a listing page in `_pages/` plus a nav
link. Removing a collection means undoing all three.

## Pages that are NOT collections

- `about.md` → `/` — **homepage**.
- **Portfolio tree** — hand-written CFD gallery, two levels, not backed by a
  collection. All media lives in `images/cfd/` (see the README there for the
  file → page map). The hub embeds no media; every animation sits on exactly
  one child page.

  | File in `_pages/` | Permalink |
  |---|---|
  | `ifluid.md` (hub) | `/portfolio/` |
  | `portfolio-frontier-taylor-green.md` | `/portfolio/frontier/taylor-green/` |
  | `portfolio-frontier-ldc2d.md` | `/portfolio/frontier/ldc2d/` |
  | `portfolio-cloud-chamber-particle-2d.md` | `/portfolio/cloud-chamber/particle-2d/` |
  | `portfolio-cloud-chamber-taylor-green.md` | `/portfolio/cloud-chamber/taylor-green/` |
  | `portfolio-cloud-chamber-rayleigh-benard.md` | `/portfolio/cloud-chamber/rayleigh-benard/` |
- `cv.md` → `/cv/` (Markdown CV, currently linked) and `cv-json.md` → `/cv-json/`
  (JSON-driven alternative, hidden by default). Switch which is linked in `navigation.yml`.
- `markdown.md` → `/markdown/` — template's "Guide" demo page (Markdown/MathJax/
  Mermaid/Plotly examples). Safe to delete; this file captures its useful parts.
- Archive/util pages: `sitemap.md`, `category-archive.html`, `tag-archive.html`,
  `year-archive.html`, `page-archive.html`, `collection-archive.html`,
  `talkmap.html`, `404.md`, `terms.md`, `non-menu-page.md`.

## Adding content

- **File naming:** `.md` renders as Markdown, `.html` renders as HTML. Dated
  collections (`_publications`, `_talks`, `_posts`) use `YYYY-MM-DD-slug.md`.
- **Front matter:** every file starts with a YAML block between `---` fences.
  Common keys: `title`, `permalink`, `collection`, `excerpt`, `layout`,
  `author_profile`, `date`, `venue`.
- **New publication:** add `_publications/YYYY-MM-DD-title.md` with `collection: publications`,
  plus `title`, `venue`, `date`, `excerpt`, `paperurl`/`slidesurl`/`bibtexurl`,
  `citation`. The fields drive the listing, the item page, and the CV section.
- **New talk:** `_talks/YYYY-MM-DD-title.md`, `collection: talks`, with `type`,
  `venue`, `location`, `date`. Locations feed the talk map.
- **New teaching:** `_teaching/YYYY-...md`, `collection: teaching`, with `type`,
  `venue`, `date`.
- **New portfolio experiment:** add `_pages/portfolio-<project>-<slug>.md` with an
  explicit `permalink: /portfolio/<project>/<slug>/`, a `[← Back to Portfolio](/portfolio/)`
  link at the top, and the animations grouped by field. Then link it from an `h3`
  under the matching project `h2` in `_pages/ifluid.md`, and add the files to the
  table in `images/cfd/README.md`.

## Rendering features (from the Guide)

- **Markdown engine:** kramdown / GitHub-Flavored Markdown; emoji via Jemoji.
- **Math:** MathJax 3. `$$...$$` or `\\[...\\]` for display math, `\\(...\\)`
  for inline. Markdown escaping can interfere — sometimes need `\(...\)`.
- **Diagrams:** Mermaid via a ```` ```mermaid ```` code fence.
- **Plots:** Plotly via a ```` ```plotly ```` fence containing valid JSON (all
  keys must be quoted).
- **Notices/call-outs:** append `{: .notice}` to a paragraph.
- **Collapsible sections:** HTML `<details><summary>...</summary></details>`.
- Client-side JS works (GitHub Pages blocks server-side code).

## Build status & preview

- Build status: repo **commits list** on GitHub — green check = built,
  orange = building, red X = error.
- Local preview: `bundle exec jekyll serve -l -H localhost` then open
  <http://localhost:4000>. Restart after editing `_config.yml`.
