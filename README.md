
# Small Business Financial Dashboard

**Why did a growing retailer's profit fall by 42%?**

A Power BI dashboard that analyses 24 months of sales, cost of sales and operating expenses for a fictional Cape Town homeware retailer, *Table Mountain Home Co.*, and explains why revenue grew while profit shrank.

![Dashboard overview] 
![Table Mountain Home Co. Financial Dashboard](table-mountain-dashboard.pdf)


---

## Business problem

Table Mountain Home Co. grew revenue by 14.6% between 2024 and 2025, but the owner feels the business is making less money. The dashboard answers: **where is the profit going?**

## Questions answered

| Question | Answer |
|---|---|
| Did revenue grow? | Yes. R3.05m (2024) to R3.50m (2025), up **14.6%**. |
| Is the business still profitable? | Yes, but net profit fell **42%**, from R310K to R180K. |
| Are margins healthy? | Gross margin slipped from 46.3% to 45.1%. Net margin halved from **10.2% to 5.1%**. |
| What are the biggest expenses? | Salaries & Wages (R808K in 2025, about 58% of all expenses), then Rent and Marketing. |
| Which costs grew fastest? | Marketing **+39%**, Salaries **+35%**, Software **+30%**. Rent and Utilities grew 10%. |
| How heavy are overheads? | Expenses rose from **36.1%** to **39.9%** of revenue. |
| Which product category earns the most gross profit? | Bedding & Linen (R570K) and Kitchenware (R562K), then Home Decor (R445K). |
| Which category has the best margin? | Home Decor at 49.5%. Kitchenware is lowest at 41.4%. |
| Which months lose money? | Jan 2024, Jan 2025, Mar 2025 and May 2025. |
| Is there seasonality? | Strongly. November and December produce half of 2024 net profit and **72% of 2025 net profit**. |

## Key findings

1. **Revenue is growing, profit is not.** Revenue +14.6%, net profit -42%.
2. **Overheads are the main driver.** Operating expenses grew 27%, almost twice as fast as revenue, led by salaries (a new hire from March 2025 plus a raise) and marketing.
3. **Margins are squeezed from both sides.** Supplier costs crept up (gross margin -1.2 points) while overheads climbed (net margin -5.1 points).
4. **Profit depends on the festive season.** In 2025, 72% of the year's profit came from two months.

## Recommendations

1. **Hold headcount and marketing spend** until sales growth justifies them, aiming to bring expenses back towards **36% of revenue** (the 2024 level).
2. **Review supplier pricing**, starting with Kitchenware, the lowest-margin category at 41%.
3. **Promote Home Decor.** It has the highest margin (about 50%) but the lowest volume.
4. **Reduce reliance on November and December** by building sales in January to May, when the business makes losses.

## What I built

- **Data model:** three fact tables (Sales, Cost of Sales, Expenses), a Date table and a Products table, connected with one-to-many relationships.
- **DAX measures:** Total Revenue, Total COGS, Gross Profit, Total Expenses, Net Profit, Gross Margin %, Net Margin %.
- **Visuals:** KPI cards, revenue vs net profit trend, cost of sales vs expenses by month, operating expenses by category, gross profit by product category, monthly P&L table and a Year slicer.
- **Validation:** dashboard totals were reconciled against an independent monthly summary built in Google Sheets with `SUMIFS` (2024 revenue R3,052,059 and net profit R310,170 matched exactly).

## Limitations

Being honest about what this project does and doesn't show:

- **Synthetic data, designed story.** The profit squeeze was deliberately built into the dataset. This is a demonstration of method, not a discovery from a real business.
- **"Net profit" is before tax, interest and depreciation.** It is closer to operating profit and would be labelled that way for a real client.
- **Profit is not cash.** This dashboard says nothing about cash flow, receivables timing or stock purchases (covered in later projects in this series).
- **COGS is recognised at the point of sale.** There is no inventory or purchases tracking, so stock levels and purchase timing are not analysed.
- **No budget or forecast.** There is no budget-vs-actual comparison or forward view.
- **Marketing return cannot be measured.** There is no campaign-level data to link spend to sales.
- **Single location and channel.** No store, online or regional breakdown.

## Tools

Power BI Desktop (data model, DAX, visuals) · Python (pandas, NumPy) for data generation · Google Sheets for reconciliation
---

*Built by Mavis Masikati, ACCA FIA candidate and freelance data analyst, Cape Town.*
