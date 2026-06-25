# Central OMR Flat — Affordability Calculator

An interactive, single-file calculator for estimating the cost of buying a flat in Central OMR, Chennai. Includes a pre-purchase checklist.

**Live demo:** `https://<your-username>.github.io/<repo-name>/`

---

## Features

- Adjust property price, down payment %, loan tenure, interest rate, and EMI/income ratio
- Instantly see: loan amount, monthly EMI, income required, total upfront cash, and total interest
- 20-item pre-purchase checklist across Legal, Financial, Builder, and Location categories
- Dark mode support
- Fully responsive (mobile-friendly)
- Zero dependencies — plain HTML, CSS, JavaScript

---

## Publishing to GitHub Pages (5 minutes)

### Option 1 — New repository

1. Go to [github.com/new](https://github.com/new)
2. Name it e.g. `omr-calculator` — keep it public
3. Upload `index.html` to the root of the repo
4. Go to **Settings → Pages**
5. Under **Source**, select `Deploy from a branch`
6. Choose `main` branch, `/ (root)` folder → **Save**
7. Your site will be live at `https://<username>.github.io/omr-calculator/` in ~1 minute

### Option 2 — GitHub CLI

```bash
git init
git add index.html README.md
git commit -m "Initial commit: OMR affordability calculator"
gh repo create omr-calculator --public --push --source=.
# Then enable Pages in Settings → Pages
```

---

## Customising

All parameters live in `index.html`. Key things you may want to change:

| What | Where in the file |
|------|-------------------|
| Price slider range (₹Cr) | `min="150" max="280"` on the `#price` input |
| Default down payment | `value="35"` on `#dp` |
| Stamp duty % | `price * 0.11` in the `calc()` function |
| Misc upfront costs | `+ 2` (₹2L) in the `calc()` function |
| Checklist items | `SECTIONS` array in the `<script>` block |

---

## Files

```
index.html   ← the entire app (calculator + checklist)
README.md    ← this file
```

---

## Notes

- Stamp duty is estimated at **11%** (TN registration + stamp duty combined). Verify the current rate for your transaction.
- EMI formula used: standard reducing-balance (P × r × (1+r)^n) / ((1+r)^n − 1)
- Checklist state is not saved between page reloads (no server or localStorage needed)
