# Changelog

## 2026-08-22
- Seed data refreshed from `Combined_Bid_Sheet 17.08.2026 (2).xlsx` (source commit `019f489e509f105d264e7fe3ba19f86942350c63`).
- Embedded app data and `data/sample-lots.json` now use the refreshed workbook values, including updated payment receipts and invoices.
- localStorage key bumped to `scrapsale_pro_v5` so existing browsers load the refreshed seed data.
- Detail table columns now follow the workbook order and include Mat. Value + GST, the second Service charge to MSTC field, Short/(Excess) Payment, SAP Document Date, and Doc./Invoice Date.
- localStorage key bumped to `scrapsale_pro_v6` so existing browsers load the new data and column layout.


## 2026-08-21
- Seed: Combined Bid Sheet 17.08.2026 — 37 lots, auctions 21977–21980
- localStorage key: `scrapsale_pro_v4`
- Live formulas: GST 18%, TCS 2% of (Mat+GST), MSTC SC 2.25% of (Mat+GST), TDS 194H = 2% of 2.25% of Material, TDS 194O 0.1% of Material, TRIC = Mat+GST+TCS−Net SC−TDS 194O−GST TDS
- Excel export with live formulas; no native PivotTable package

## 2026-08-19
- Initial GitHub folder: single-file app, sample lots, docs
