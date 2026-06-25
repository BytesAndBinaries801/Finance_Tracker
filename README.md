# Ledger — Monthly Finance Tracker

A single-page finance tracker: log income and expenses, browse by month, and see
a dashboard with KPIs, an income-vs-expense trend chart, a category donut chart,
and a spreadsheet-style monthly summary table. All amounts are in ₹ (INR).

**Live site:** `https://<your-username>.github.io/<repo-name>/` (once Pages is enabled — see below)

## How your data works

This is a static page — there's no database and no server. Entries you add are
saved in your **browser's local storage**, on whichever device/browser you're
using. They are *not* uploaded anywhere, and they are *not* stored in this repo.

To back your data up or move it to another device:
- Click **Export JSON** in the tracker → save the file → commit it to this repo
  if you want it versioned (e.g. as `data/ledger-data.json`), or keep it elsewhere
  if you'd rather not put real numbers in a public repo.
- Click **Import JSON** on any device to restore from that file.

> Heads up: this repo is **public**, since GitHub Pages on the free plan only
> serves sites from public repos. The page's code being public is harmless —
> your actual numbers live in your browser, not in this code. Just be mindful
> about whether you ever commit an exported `ledger-data.json` here, since that
> file *would* contain real numbers.

## Publishing this with GitHub Pages

Following GitHub's own [Pages quickstart](https://docs.github.com/en/pages/quickstart):

1. Push this repo to GitHub (see commands below).
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Under **Branch**, select `main` and folder `/ (root)`, then **Save**.
5. Wait a few minutes, then visit `https://<your-username>.github.io/<repo-name>/`.

## Pushing this folder to GitHub

```bash
cd path/to/this/folder
git init
git branch -M main
git add .
git commit -m "Initial commit: finance tracker"
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Updating the tracker later

Replace `index.html` with the new version, then:

```bash
git add index.html
git commit -m "Update tracker"
git push
```

GitHub Pages will redeploy automatically (usually within a few minutes).
