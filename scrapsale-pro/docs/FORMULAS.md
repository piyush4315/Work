# Formulas

All amounts INR, typically rounded to ₹1.

| Field | Rule |
|---|---|
| Material value | Qty × Rate |
| GST | GST % × Material value (form default **18%**) |
| TCS | TCS % × (Material + GST) (form default **2%**) |
| MSTC service charge | SC % × (Material + GST) (form default **2.25%**) |
| TDS 194H | 194H % × (**2.25% of Material value**) (form default **2%**, so 0.045% of material) |
| Net service charge | Service charge − TDS 194H |
| TDS 194O | 194O % × Material value (form default **0.1%**) |
| GST TDS | GST TDS % × Material value |
| Total Receivables in Cash (TRIC) | Material + GST + TCS − Net SC − TDS 194O − GST TDS |
| SD Expected | ROUND(Material × SD %, 0) — default **25%**, overridable |
| FP Expected | TRIC − SD Expected, unless overridden |
| Total Received | SD Received + FP Received |
| Outstanding | TRIC − Total Received |

## Add / Edit form

Only **percentages** are typed for charges. Amounts fill in live and are read-only in the form.

Qty, Rate, Buyer, Lot No, Auction, Material, Unit, and payment received fields stay directly editable.

## Grid

- GST is **not** inline-editable in the table.
- GST TDS Rate % and GST TDS **are** live-linked in the table.
- ✎ on a row opens the full-row form.

## Excel export

Sheet **Cash Receivables** is table `CashReceivables` with live formulas. Sheet **Pivot Analytics** uses SUMIF/COUNTIF against that table. Sheet **Power BI** has DAX notes and dimension lists.

Import looks for a sheet whose header contains **Lot No** and **Buyer**.
