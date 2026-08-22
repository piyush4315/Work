# Data

| File | Purpose |
|---|---|
| `sample-lots.json` | Seed dataset (37 lots, auctions 21977–21980). Safe to commit. |

## Your live lots are not in Git

Edits you make in the browser are stored in **localStorage** (`scrapsale_pro_v4`), not in this folder.

Before you switch machines or AIs:

1. Open `ScrapSale_Pro.html`
2. **Export → JSON**
3. Save the file (e.g. `data/my-lots-YYYYMMDD.json`)
4. Commit it **only if** it is OK to store that business data in the repo

Import later: **Data & Backup → Import → Replace** or **Merge by Lot No**.

JSON is the complete snapshot (lots, custom columns, extras, manual SD/FP flags). Excel is a human backup and is also re-importable.
