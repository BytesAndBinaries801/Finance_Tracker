# Flat purchase planner

A single-page site with three sheets:

- **Dashboard** — live summary of your loan numbers and checklist progress
- **Loan calculator** — property price, down payment, tenure, rate, and an extra-annual-prepayment slider that shows how much earlier the loan closes and how much interest you save
- **Checklist** — 44-point due-diligence checklist for buying a flat

Checklist checks are saved in the browser via localStorage, so progress persists between visits on the same device.

## Host it on GitHub Pages

1. Create a new repository on GitHub (e.g. `flat-checklist`).
2. Upload `index.html` to the root of the repository (drag-and-drop on the GitHub web UI works, or `git add`, `git commit`, `git push`).
3. Go to the repo's **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Pick the `main` branch and `/ (root)` folder, then **Save**.
6. After a minute, your checklist will be live at:
   `https://<your-username>.github.io/<repo-name>/`

No build step, no dependencies — it's a static file.
