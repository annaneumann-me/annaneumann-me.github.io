# annaneumann-me.github.io

Personal research site, built with Jekyll (GitHub Pages builds this automatically — no build step needed once pushed).

## Pages

- `index.md` — home: hero, "media" / "let's chat + obsessed with" cards, research threads
- `about.md` — bio, CV link, academic service (with role tags)
- `publications.md` — publications, grouped by year, with authors and typed file links (paper/arxiv/video/poster)
- `events.md` — invited talks and events, card-based with tags and group/event links
- `teaching.md` — courses and supervised theses
- `gallery.md` — masonry photo grid, auto-populated from `assets/img/gallery/`

## Editing content

Everything you'll normally touch is in `_data/*.yml`:

- `_data/publications.yml` — copy a block to add a new paper. `status`, `authors`, and `links`
  are optional. `authors` is a plain string with the full author list. Each link has a `type`
  (`paper` / `arxiv` / `video` / `poster` — each renders in a different green hue) and a `url`.
  - To link to a **paper PDF** you have locally: drop it into `assets/documents/papers/`, set
    `url: "/assets/documents/papers/yourfile.pdf"`.
  - To link to a **poster**: drop it into `assets/documents/posters/`, set
    `url: "/assets/documents/posters/yourfile.pdf"`.
  - `video` / `arxiv` links are usually external URLs.
- `_data/projects.yml` — research threads shown on the home page (title, summary, tags)
- `_data/talks.yml` — invited talks (date, venue). `role` and `url` (link to the hosting group) are optional.
- `_data/events.yml` — conferences/events attended or presented at. `role` renders as a tag,
  `note` is optional extra detail, `url` links to the event/group site.
- `_data/media.yml` — press/media mentions (shown on home page). `url` links out to the piece.
- `_data/service.yml` — academic service, shown on the about page. `external` entries are
  `{venue, role}` (role renders as a tag, e.g. "reviewer"); `internal` entries are `{year, role}`.
- `_data/teaching.yml` — courses and supervised theses

## Documents

`assets/documents/` holds any file you want to link to — `cv.pdf` goes directly in there,
paper PDFs go in `assets/documents/papers/`, posters in `assets/documents/posters/`. Link to
any of them with a normal `/assets/documents/...` URL.

## Gallery

Just drop an image file into `assets/img/gallery/` and it automatically appears in the
grid on `/gallery/` — no data file to edit. Images keep their natural proportions (no
cropping), so any size/orientation works. No captions are shown.

## Photo

The homepage portrait is `assets/img/anna.jpg`, rendered in black-and-white with a subtle
green shimmer (pure CSS, see `.avatar` in `assets/css/style.css` — no image editing needed
to update it, just swap the file and keep the same name, or update the `src` in `index.md`).

## Still to fill in

- `index.md` / `about.md`: swap the placeholder Google Scholar, Substack, and Affiliation links for your real URLs
- `index.md`: the linkedin/bluesky/x buttons in "let's chat" are placeholder `#` links — swap in your real profile URLs
- Add your actual CV as `assets/documents/cv.pdf` (linked from home and the about page)
- The "anna neumann et al." placeholder in `_data/publications.yml` needs real full author lists per paper
- Several `url: "#"` placeholders in `_data/*.yml` and `_data/publications.yml` need real URLs (group pages, event pages, media articles, paper/poster files)

## Preview locally

```bash
cd /Users/annaneumann/Documents/ClaudeCode/annaneumann-me.github.io
export PATH="/opt/homebrew/opt/ruby/bin:/opt/homebrew/lib/ruby/gems/4.0.0/bin:$PATH"
jekyll serve
```
Then open http://localhost:4000

## Deploy

```bash
git add -A
git commit -m "describe your change"
git push
```
GitHub Pages builds and serves it automatically at `https://annaneumann-me.github.io` (~1–2 min).
