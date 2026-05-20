# SOKE Video Gallery (GitHub Pages)

A simple static, mobile-friendly video gallery for showcasing multilingual sign language generation demos.

## Project structure

- `index.html` — main page (title, subtitle, styles, and video cards)
- `public/videos/` — local MP4 files served by the page

## How to run locally

Because this is a static site, you can:

1. Open `index.html` directly in your browser, **or**
2. Use a small local server (recommended), e.g.:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## How to change title and subtitle

Open `index.html` and edit:

- `<h1>` for the main title
- `<p class="subtitle">` for the subtitle

Current defaults:

- **Title:** `From Text to Sign: The State of Multilingual Sign Language Production`
- **Subtitle:** `Visualizing SOKE-based generation across ASL, DGS, and Chinese Sign Language`

## How to add or replace MP4 videos

1. Put your `.mp4` files in `public/videos/`.
2. In `index.html`, duplicate or edit a `<article class="video-card">` block.
3. Update:
   - the card title in `<h2>...`
   - the video path in `<source src="public/videos/your-file.mp4" type="video/mp4" />`

Example card block:

```html
<article class="video-card">
  <h2>My New Demo</h2>
  <video controls preload="metadata">
    <source src="public/videos/my-new-demo.mp4" type="video/mp4" />
    Your browser does not support the video tag.
  </video>
</article>
```

## GitHub Pages deployment

This repository is already compatible with GitHub Pages as a static site.

### Option A (Deploy from branch root)

1. Push to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose:
   - **Source:** `Deploy from a branch`
   - **Branch:** your branch (commonly `main`)
   - **Folder:** `/ (root)`
4. Save.

Your site will be published at:

- https://isottongloria.github.io/soke-video-gallery/

### Option B (GitHub Actions)

You can also use a Pages workflow, but it is not required for this project.

## Notes

- No backend, database, login, or upload system is included.
- Styling uses the **Lexend** font (Google Fonts), with a clean color palette and responsive layout.
