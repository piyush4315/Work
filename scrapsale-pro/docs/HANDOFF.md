# Handoff — give this to the next person or AI

## What to send

1. This Git repo (or a ZIP of the folder)
2. A **JSON export** of live lots if any work was done in the browser  
   (`Export → JSON` inside the app)

The HTML file does **not** contain edited lots. Those live in browser `localStorage` key `scrapsale_pro_v4`.

## What this project is

Single-file cash-receivables app for MSTC scrap sales.

- Dashboard KPIs + Pivot Analytics
- Click a buyer (or other group) → all that group’s lots on the **same page**
- Column picker, add column, add row, **✎ edit entire row**, delete
- Add/Edit form: type **% only**; amounts auto-fill
- Export: Excel (formulas + pivot + Power BI sheet), HTML, PDF, CSV, TXT, JSON, Google Drive
- Import: XLSX / CSV / JSON / HTML / TXT — merge or replace
- Undo/redo (10 steps)

## Rules when changing the code

- Keep it a **single self-contained HTML file** (`ScrapSale_Pro.html`) unless you deliberately split it and update the README.
- Preserve Excel **import** after any export change. Test: export → import → lot count and totals match.
- Do not put a native Excel PivotTable package in the `.xlsx` — Excel treated it as a corrupt file. Use the formula Pivot Analytics sheet instead.
- Do not put worksheet `autoFilter` on the same range as an Excel Table.

## Brief to paste

```
This is ScrapSale Pro. The app is scrapsale-pro/ScrapSale_Pro.html.
Read README.md, docs/HANDOFF.md, and docs/FORMULAS.md first.
If I attached a JSON export, import it before changing data or code.
Keep a single self-contained HTML file. Preserve Excel import/export
and same-page pivot drill-down. In the add/edit form only percentages
are typed for charges; amounts auto-fill.
```
