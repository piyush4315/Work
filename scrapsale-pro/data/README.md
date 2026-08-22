# Data

| File | Purpose |
|---|---|
| `sample-lots.json` | Current seed dataset (37 lots, auctions 21977–21980). Safe to commit. |
| `Combined_Bid_Sheet 17.08.2026 (2).xlsx` | Source workbook used for the current seed data. |

## Your live lots are not in Git

Edits you make in the browser are stored in **localStorage** (`scrapsale_pro_v5`), not in this folder. The key was bumped for the 2026-08-22 workbook refresh so existing browsers load the updated seed data.

Before you switch machines or AIs:

1. Open `ScrapSale_Pro.html`
2. **Export → JSON**
3. Save the file (e.g. `data/my-lots-YYYYMMDD.json`)
4. Commit it **only if** it is OK to store that business data in the repo

Import later: **Data & Backup → Import → Replace** or **Merge by Lot No**.

JSON is the complete snapshot (lots, custom columns, extras, manual SD/FP flags). Excel is a human backup and is also re-importable.
