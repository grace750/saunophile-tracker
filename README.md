[README.md](https://github.com/user-attachments/files/28797311/README.md)
# Saunophile Sauna Tracker — GitHub Pages

This folder is a complete, ready-to-publish static site. Just `index.html` (364 venues, self-contained) plus `.nojekyll`.

## Before you publish — set two links
Open `index.html`, find this block near the top of the `<script>` and paste in your URLs:
```js
const SUGGEST_URL="https://forms.gle/REPLACE-WITH-YOUR-FORM-ID";  // your Google Form
const NEWSLETTER_URL="https://saunophile.substack.com";           // your Substack
```

## First-time publish (≈5 min)
1. Create a repo on GitHub, e.g. **`saunophile-tracker`** (public).
2. Upload **`index.html`** and **`.nojekyll`** to the repo root (drag-drop in the GitHub web UI → "commit changes").
3. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = **`main`**, folder = **`/ (root)`** → Save.
4. Wait ~1 minute. Your map is live at **`https://<your-username>.github.io/saunophile-tracker/`**.

`.nojekyll` tells GitHub Pages to serve the file as-is (skip Jekyll processing). Keep it in the repo.

## Updating the map later
The data is baked into `index.html`, so updating = replacing that one file:
1. Get the new `index.html` (regenerated from the dataset after you approve new studios).
2. In the repo: open `index.html` → ✏️ edit (or upload to overwrite) → **commit**.
3. Pages redeploys in ~1 min. Same URL, refreshed map.

Tip: edits committed to `main` auto-publish. For a paper trail, each update is a commit you can roll back.

## Custom domain (optional)
Settings → Pages → **Custom domain** → enter e.g. `map.saunophile.com` → add the CNAME record your DNS host shows. HTTPS is automatic and free.

## Why this is "secure but public"
It's a single static file — no server, no database, no admin login, nothing to breach or deface. Anyone can view; only repo collaborators can change it. Suggestions flow into your private Google Sheet, and nothing hits the map until you regenerate and commit.
