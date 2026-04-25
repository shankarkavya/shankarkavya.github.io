# shankarkavya.github.io

Personal website / portfolio — [shankarkavya.github.io](https://shankarkavya.github.io)

Inspired by the [Jon Barron](https://jonbarron.info/) academic template, but built from scratch in plain HTML + CSS (no Jekyll, no build step).

## Structure

```
.
├── index.html              # single-page site
├── README.md
├── .nojekyll               # tells GitHub Pages not to run Jekyll
└── assets/
    ├── style.css
    ├── Kavya_Shankar_CV_Feb2026.pdf
    └── images/
        └── portrait.jpg    # (add your own)
```

## Deploy to GitHub Pages

### Option A — User site at `shankarkavya.github.io` (recommended)

1. Create a new public repo on GitHub named exactly **`<your-username>.github.io`** (e.g. `kavya-shankar.github.io`).
2. Upload everything in this folder to the root of that repo. Either via the GitHub web UI (drag-and-drop the files) or from your terminal:
   ```bash
   cd kavya-site
   git init
   git add .
   git commit -m "initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. Wait ~1 minute. Your site is live at `https://<your-username>.github.io`.

### Option B — Project site under an existing repo

1. Push to any repo (e.g. `personal-site`).
2. Settings → Pages → Source: `main` / `/ (root)`.
3. It will live at `https://<your-username>.github.io/personal-site/`.

## Customise

- **Add a photo.** Drop a square-ish image at `assets/images/portrait.jpg`, then in `index.html` replace the entire `<div class="portrait">…</div>` block with:
  ```html
  <img src="assets/images/portrait.jpg" class="portrait" alt="Kavya Shankar" />
  ```
- **Update the CV.** Replace `assets/Kavya_Shankar_CV.pdf` with a newer version; the link in the header will pick it up automatically as long as the filename matches.
- **Add GitHub / Scholar links.** Search `index.html` for `href="https://github.com/"` and `href="#"` (the scholar one) and paste in your real URLs.
- **New project?** Copy one of the `<div class="project">…</div>` blocks and edit. Thumbnails are pure CSS (no images needed) — pick from `thumb-nlp`, `thumb-cv`, `thumb-time`, `thumb-robot`, `thumb-chat`, `thumb-retina`, or add your own `::before` pattern in `assets/style.css`.

## License

Content © Kavya Shankar. Code released under MIT if you want to reuse the template.
