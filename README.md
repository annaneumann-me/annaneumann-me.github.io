# annaneumann-me.github.io

Personal research site, built with Jekyll (GitHub Pages builds this automatically — no build step needed once pushed).

## Editing content

Everything you'll normally touch is in `_data/*.yml` or the two `.md` pages:

- `index.md` — homepage bio, links, "little about me"
- `research.md` — page layout for the "stuff I did" page (rarely needs touching)
- `_data/papers_first_author.yml` — copy a block to add a new first-author paper
- `_data/papers_other.yml` — same, for co-authored/other papers
- `_data/talks.yml` — invited talks
- `_data/media.yml` — press/media mentions
- `_data/service.yml` — reviewing + internal service (`external:` / `internal:` lists)
- `_data/events.yml` — conferences/events attended or presented at
- `_data/teaching.yml` — courses and supervised theses

To add a new paper, open `_data/papers_first_author.yml` and copy-paste an existing
block, then edit the fields. `links` and `award` are optional.

## Still to fill in

- `index.md`: swap the placeholder Google Scholar, Substack, and Affiliation links for your real URLs
- Add your actual CV as `assets/cv.pdf` (referenced from the homepage)
- Several `url: "#"` placeholders in `_data/*.yml` (paper videos, media links, etc.) need real URLs
- Optional: add a `favicon.ico` / profile photo to `assets/` if you want one

## Preview locally

```
bundle install
bundle exec jekyll serve
```
Then open http://localhost:4000

## Deploy

Push to a GitHub repo named exactly `annaneumann-me.github.io` under your
`annaneumann-me` GitHub account. GitHub Pages builds and serves it automatically
at `https://annaneumann-me.github.io` — no Actions/workflow needed for a
standard Jekyll user site.
