# Matthew's home page

A tiny web 1.0 personal site. Plain HTML and CSS, no JavaScript, no build step.

```
index.html     home page (about, interests, links)
photos.html    photo album
style.css      all the styling (colors are at the top in :root)
404.html       shown by GitHub Pages for broken links
photos/        your pictures
```

## Put it on GitHub Pages

1. On GitHub, create a new **public** repository named exactly `YOUR-USERNAME.github.io`.
2. Upload these files to the root of the repo (Add file -> Upload files works fine; keep the `photos` folder).
3. Go to **Settings -> Pages**. If it isn't already publishing, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, and save.
4. After a minute or two the site is live at `https://YOUR-USERNAME.github.io`.

To preview locally, just double-click `index.html`.

## Things to fill in

Search `index.html` and `photos.html` for `EDIT:` and `YOUR-` to find every spot.

- **Links** - each one is a row in the links table in `index.html`.
- **About / interests** - rewrite freely; each interest is one `<li>` line.
- **Photos** - drop your images into `photos/` and update each `<figure>`:
  `src`, `href`, `alt` (a short description of the photo), and the caption.
  The album shows one photo per row, except for the `<div class="pair">` block,
  which puts two photos side by side (portrait shots work best there).
  Copy a whole `<figure class="photo">...</figure>` block to add another row, and
  cut and paste the `pair` block to move the side-by-side row.
  Resize images to about 1600px on the long edge so they stay under ~500 KB each;
  phone photos straight off the camera are 3-8 MB and will make the page slow.
- **Last updated** date in the footer.

## Changing the look

- Background color/stars: `html { ... }` near the top of `style.css`.
- Page width: `max-width` in `#page`.
- Title-bar headers: the `h2` rule.
