# TRACE Lab website

Source for thetracelab.org — Tourism and Recreation Analytics for Communities and Ecosystems, University of Wyoming.
Built with [Quarto](https://quarto.org). No R or Python needed to build; just the Quarto CLI.

## Edit content

| Page            | File               |
|-----------------|--------------------|
| Home            | `index.qmd`        |
| Projects        | `projects.qmd`     |
| Work With Us    | `work-with-us.qmd` |
| Publications    | `publications.bib` (add a BibTeX entry; the page rebuilds itself, newest first) |
| People          | `people.qmd`       |
| Nav, footer     | `_quarto.yml`      |
| Colors, fonts   | `custom.scss`      |

## Add images

Drop files into `images/` and replace a placeholder block like

```html
<div class="photo-frame"><span>Fieldwork photo</span></div>
```

with

```html
<div class="photo-frame"><img src="images/mccarthy-road.jpg" alt="Gravel road along the Kennicott River"></div>
```

## Build locally

```
quarto preview      # live-reloading local server
quarto render       # writes the static site to _site/
```

## Deploy

**GitHub Pages:** push the repo, then run `quarto publish gh-pages` once from your machine. Quarto handles the rest.
For a custom domain, add a `CNAME` file containing `thetracelab.org` to the repo root and point DNS at GitHub Pages
(one A/ALIAS record for the apex, one CNAME for `www`).

**Cloudflare Pages:** connect the repo, set build command `quarto render` and output directory `_site`.
