# matthewgebara.com

Source for my personal website, [matthewgebara.com](https://matthewgebara.com).
Plain HTML and CSS, with no JavaScript and no build step, served by GitHub Pages.

## What's here

```
index.html            home page: about, projects, interests, links
photos.html           photo album
404.html              page-not-found page
style.css             all styling (colors are defined at the top, in :root)
photos/               album photos, the about-me photo, and link-preview images
favicon.ico,
favicon-32.png        browser tab icon
apple-touch-icon.png  phone home-screen icon
CNAME                 custom domain for GitHub Pages
```

## Updating the site

- **Publishing:** push to `main`. GitHub Pages republishes within a minute or two.
- **Previewing locally:** run `python3 -m http.server` in this folder and open
  <http://localhost:8000>. Opening the files directly mostly works too, but the
  header link and the 404 page use root paths (`/`), which only resolve through a server.
- **After changing `style.css`:** bump the `?v=` number on the stylesheet link in
  `index.html`, `photos.html`, and `404.html`, so browsers fetch the new version
  instead of a cached one.
- **Adding photos:** resize to about 1400px on the long edge and strip location
  metadata before committing. In `photos.html`, each `<figure class="photo">` is one
  row, and the `<div class="pair">` block is the one side-by-side row. Give every
  image a short `alt` description.
- **Link previews:** the `og:` tags in each page's `<head>` control the card shown on
  LinkedIn, Slack, and similar apps. Preview images are 1200×628 and live in `photos/`.
