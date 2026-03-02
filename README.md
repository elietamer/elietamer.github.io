# Elie Tamer GitHub Website

This folder is a GitHub Pages-ready static site.

## Local preview

```bash
cd github-site
python3 -m http.server 8000
```

Then open: `http://localhost:8000`

## Deploy to GitHub Pages

### Option A: `username.github.io` repo

```bash
cd github-site
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/username/username.github.io.git
git push -u origin main
```

### Option B: project repo (recommended if you already have a personal site repo)

```bash
cd github-site
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/username/repo-name.git
git push -u origin main
```

Then in GitHub: **Settings → Pages**

- **Source**: Deploy from a branch
- **Branch**: `main`
- **Folder**: `/ (root)`

Save and wait ~1–2 minutes.

If your repo is `username.github.io`, your site URL will be:

`https://username.github.io/`

If your repo is a project repo, URL will be:

`https://username.github.io/repo-name/`

## Notes

- This site uses relative links and includes `<base href="./">`, so it works in both root-domain and project-subpath GitHub Pages deployments.
- `.nojekyll` is included to avoid any Jekyll processing edge cases.
