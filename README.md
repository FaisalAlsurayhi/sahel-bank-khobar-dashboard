# Bank Branch Dashboard - Sahel Bank, Khobar 2024

A monthly performance dashboard for a fictional retail bank branch in Al-Khobar, tracking total deposits and loan applications across 2024. Built in Excel using Python.

The numbers are made up, but the seasonality is based on how this market can behave: the Ramadan deposit spike, the post-Eid financing wave, and the summer slowdown. The goal was to have data that tells a realistic story rather than just fills rows.

## Why I Built This

I wanted a finance-style dashboard that felt local to Khobar, not a generic sample workbook. This project gave me practice turning monthly branch data into a simple management report and writing out the business story behind the numbers.

## What the data shows

Ramadan started March 10th. Deposits that month hit 71.4M SAR, the highest of the year, while loan applications dropped to 87, the lowest. Both things happening at once makes sense once you think about it: people cut spending, accumulate cash, and generally avoid taking on new debt during Ramadan. You would miss all of that looking only at an annual average.

What surprised me was the loan application timing. I expected the post-Eid spike in April, and it was there at 162 applications. But the actual peak was May at 178. Most of the financing demand, especially car loans, took a few weeks after Eid to turn into real applications. April is when people decide, May is when they walk in.

July was the low point on both metrics. 43.7M in deposits, 98 loan apps. Summer travel in the Eastern Province hits branch foot traffic hard, and the data shows that clearly.

December recovered on deposits (79M) as year-end bonuses came in, though borrowing stayed flat.

## What's in the workbook

`Branch Data` is the 12-month table with deposits, loan application counts, month-on-month change for both, and a notes column. `Dashboard` pulls from it via live formulas and shows the full-year numbers alongside two charts and the observations above.

## How it was built

Python and openpyxl to generate the workbook programmatically. Update any number in `Branch Data` and the dashboard recalculates automatically.

```
bank_branch_dashboard.xlsx    # the workbook
build_dashboard.py            # script that generates it
```

```bash
pip install openpyxl
python build_dashboard.py
```

## Tools

Python, openpyxl, Excel

## Related Portfolio Work

- [Retail Sales Dashboard](https://github.com/FaisalAlsurayhi/retail-sales-dashboard)
- [Power BI Portfolio](https://github.com/FaisalAlsurayhi/powerbi-portfolio)
- [Applied Econometrics](https://github.com/FaisalAlsurayhi/applied-econometrics)
