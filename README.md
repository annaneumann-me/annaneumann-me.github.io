# annaneumann-me.github.io

Personal research site, built with Jekyll (GitHub Pages builds this automatically — no build step needed once pushed).

## Pages

- `index.md` — home: hero, "obsessed with" / "media" cards, research threads
- `about.md` — bio, CV link, academic service
- `publications.md` — papers, grouped by year, with typed links (paper/arxiv/video/poster)
- `teaching.md` — courses and supervised theses
- `talks.md` — invited talks and events
- `gallery.md` — photo carousel

## Editing content

Everything you'll normally touch is in `_data/*.yml`:

- `_data/publications.yml` — copy a block to add a new paper. `status` and `links` are optional.
  Each link has a `type` (`paper` / `arxiv` / `video` / `poster` — each renders in a different
  green hue) and a `url`.
- `_data/projects.yml` — research threads shown on the home page (title, summary, tags)
- `_data/talks.yml` — invited talks (date, venue)
- `_data/events.yml` — conferences/events attended or presented at
- `_data/media.yml` — press/media mentions (shown on home page)
- `_data/service.yml` — reviewing + internal service, shown on the about page (`external:` / `internal:` string lists)
- `_data/teaching.yml` — courses and supervised theses
- `_data/gallery.yml` — photos for the gallery carousel. Drop an image in `assets/img/`, then
  add `{ src: "/assets/img/yourfile.jpg", caption: "..." }` to the list.

## Photo

The homepage portrait is `assets/img/anna.jpg`, rendered in black-and-white with a green
duotone wash (pure CSS, see `.avatar` in `assets/css/style.css` — no image editing needed
to update it, just swap the file and keep the same name, or update the `src` in `index.md`).

## Still to fill in

- `index.md` / `about.md`: swap the placeholder Google Scholar, Substack, and Affiliation links for your real URLs
- Add your actual CV as `assets/cv.pdf` (linked from the about page)
- Several `url: "#"` placeholders in `_data/*.yml` and `_data/publications.yml` need real URLs

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
