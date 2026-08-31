# arafat45.github.io — personal academic website

Static site (plain HTML + CSS, no build step). Live at **https://arafat45.github.io** once deployed.

## Files

```
index.html          — the whole site (all sections)
style.css           — styling
assets/profile.jpg  — headshot
assets/cv.pdf       — downloadable CV
```

## Deploy (one time, ~3 minutes)

1. On GitHub, create a **new public repository** named exactly: `arafat45.github.io`
   (do not add a README or .gitignore when creating it).
2. From this folder, run:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/arafat45/arafat45.github.io.git
   git push -u origin main
   ```

3. Wait 1–2 minutes, then open https://arafat45.github.io
   (If it 404s, check Settings → Pages → source is "Deploy from a branch", branch `main`, folder `/ (root)`.)

## Before / after deploying — one thing to fix

The **Google Scholar link** is a placeholder. Search `YOUR_SCHOLAR_ID` in `index.html`
(it appears twice) and replace the URL with your real Scholar profile link.

## Updating the site later

- **New publication:** copy one `<li>` block inside `<ol class="pub-list">` in `index.html`,
  edit the title/authors/venue, and pick a badge class:
  `badge published` / `badge accepted` / `badge review` / `badge prep`.
- **News item:** add a `<li>` at the top of `<ul class="news-list">`.
- **New CV:** overwrite `assets/cv.pdf`.
- Then: `git add . && git commit -m "update" && git push` — the live site refreshes in ~1 minute.
