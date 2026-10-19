# L. Felipe Perrone — personal website

Plain HTML + one stylesheet. No build step, no database, no plugins.

## Structure

```
index.html            About (home)
bio/index.html        Bio
teaching/index.html   Teaching (every semester since 2003)
students/index.html   Research students
research/index.html   Publications, theses, talks
robolab/index.html    RoboLab
style.css             All styling (colors and fonts are tokens at the top)
img/portrait.jpg      Your photo (add this file; a monogram shows until you do)
.nojekyll             Tells GitHub Pages to serve files as-is
```

## Publish on GitHub Pages

1. On github.com, create a **public** repository named exactly `YOUR-USERNAME.github.io`.
2. Upload the contents of this folder (Add file → Upload files), or:
   ```
   git init && git add . && git commit -m "New website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
   git push -u origin main
   ```
3. In the repo: Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
4. The site appears at `https://YOUR-USERNAME.github.io/` within a minute or two.

## Preview locally

Open `index.html` in a browser. All links are relative, so the whole site works from your disk.

## Editing

- Each page is a self-contained HTML file; edit text directly.
- To add a semester on the Teaching page, copy a `<div class="term">` block.
- To add a publication, copy an `<article class="pub">` block into the right year.

## Redirect from Bucknell

Replace the WordPress files in `~perrone` with an `index.html` containing:

```html
<meta http-equiv="refresh" content="0; url=https://YOUR-USERNAME.github.io/">
```

Keep the `wp-content/`, `research-docs/`, and `students-docs/` folders on the Bucknell
server (or copy them into this repo): many PDF links on the Research and Students pages
point there.
