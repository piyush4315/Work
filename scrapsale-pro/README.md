# ScrapSale Pro

Single-file cash-receivables app for MSTC scrap-sale lots (security deposit, final payment, GST / TCS / TDS, outstanding).

Open **`ScrapSale_Pro.html`** in a browser. No build step, no server, no npm.

```
scrapsale-pro/
├── README.md                 ← you are here
├── LICENSE
├── .gitignore
├── index.html                 ← convenience launcher for static hosting
├── ScrapSale_Pro.html        ← the entire application
├── data/
│   ├── README.md
│   ├── sample-lots.json      ← current seed data (37 lots)
│   └── Combined_Bid_Sheet 17.08.2026 (2).xlsx ← source workbook
└── docs/
    ├── HANDOFF.md            ← give this to the next AI / teammate
    └── FORMULAS.md           ← calculation rules
```

## Run it

1. Clone this repo (or download the ZIP).
2. Double-click `ScrapSale_Pro.html`, or from a terminal:

   ```bash
   # optional local server (avoids some browser file:// limits)
   python3 -m http.server 8765
   # then open http://localhost:8765/ScrapSale_Pro.html
   ```

3. First launch loads the 37 lots from `Combined_Bid_Sheet 17.08.2026 (2).xlsx` (auctions 21977–21980).

## Save your work

| What | Where |
|---|---|
| Code / UI / formulas | This Git repo (`ScrapSale_Pro.html`) |
| Lots you type or import | Browser **localStorage** (`scrapsale_pro_v6`) — **not** in Git |

**Before you change computers, browsers, or AIs:**

1. In the app: **Export → JSON**
2. Keep that file with the repo (see `data/README.md`)
3. On the next machine: **Data & Backup → Import → Replace** or **Merge by Lot No**

JSON is the complete snapshot. Excel is a working backup and also re-imports.

## Features

- Same-page pivot: click a buyer / auction / material / unit → all matching lots below
- Column picker (▾ on headers) and custom columns
- **+ Add row** and **✎ Edit entire row** — charge **rates (%)** are typed; amounts auto-fill
- Live grid edits: GST TDS Rate, GST TDS, SD/FP expected & received, dates
- Undo / redo (Ctrl+Z / Ctrl+Y), 10 steps
- Export: Excel (live formulas + table `CashReceivables` + Pivot Analytics + Power BI sheet), HTML, PDF, CSV, TXT, JSON, Google Drive
- Import: XLSX, CSV, JSON, HTML, TXT

## GitHub

```bash
cd scrapsale-pro
git init
git add .
git commit -m "Initial ScrapSale Pro"
git branch -M main
git remote add origin https://github.com/piyush4315/scrapsale-pro.git
git push -u origin main
```

Optional GitHub Pages: Settings → Pages → Deploy from branch `main` `/` (root). Users then open `ScrapSale_Pro.html` on the Pages URL. Autosave still depends on each visitor’s browser.

## For the next developer or AI

Read `docs/HANDOFF.md` and `docs/FORMULAS.md`. Keep the app a single HTML file unless you intentionally split it.
