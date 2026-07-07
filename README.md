# annaneumann-me.github.io

Personal research site, built with Jekyll (GitHub Pages builds this automatically — no build step needed once pushed).

## Pages

- `index.md` — about / home
- `publications.md` — papers, grouped by year
- `projects.md` — research threads
- `talks.md` — invited talks, events, media, academic service, teaching

## Editing content

Everything you'll normally touch is in `_data/*.yml`:

- `_data/publications.yml` — copy a block to add a new paper. Fields `status` and `links` are optional.
- `_data/projects.yml` — research threads (title, summary, tags)
- `_data/talks.yml` — invited talks (date, venue)
- `_data/events.yml` — conferences/events attended or presented at
- `_data/media.yml` — press/media mentions
- `_data/service.yml` — reviewing + internal service (`external:` / `internal:` string lists)
- `_data/teaching.yml` — courses and supervised theses

To add a new paper, open `_data/publications.yml` and copy-paste an existing block, then edit the fields.

## Still to fill in

- `index.md`: swap the placeholder Google Scholar, Substack, and Affiliation links for your real URLs
- Add your actual CV as `assets/cv.pdf` (referenced from the homepage)
- Several `url: "#"` placeholders in `_data/*.yml` (paper videos, media links) need real URLs
- Optional: add a `favicon.ico` / profile photo to `assets/` if you want one

## Preview locally

```
bundle install
bundle exec jekyll serve
```
Then open http://localhost:4000

## Deploy

Push to `main` on `github.com/annaneumann-me/annaneumann-me.github.io`. GitHub Pages
builds and serves it automatically at `https://annaneumann-me.github.io`.
