# ENCORE project website

A static website for the ENCORE project at the Mace Head Atmospheric Research Station (University of Galway).
Plain HTML, CSS and a little JavaScript. No build step, so it runs as-is on GitHub Pages.

```
index.html            the page
assets/css/style.css  all styling (colours are set at the top in :root)
assets/js/main.js     mobile menu and scroll effects
assets/img/           photos, C-CAPS logo and favicon
```

## Preview locally

Open `index.html` in a browser, or run a small local server from this folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Editing content

All text lives in `index.html`, one `<section>` per part of the page (About, Why N₂O, Objectives, Mace Head, Team, Contact).
Images are in `assets/img/`; replace a file with one of the same name to swap a photo.
Colours and fonts are set at the top of `assets/css/style.css`.

Content is taken from the ENCORE page on macehead.org: https://www.macehead.org/project/encore/

## Publish on GitHub Pages

1. Create a new repository on GitHub (for example `encore`).
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "ENCORE website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/encore.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, choose `main` and `/ (root)`, then **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/encore/`.

To use a custom domain, add it under Settings → Pages; GitHub creates a `CNAME` file for you.
