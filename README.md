# Sugar Plant Supply Planning: Excel Practice Case

A self-study supply planning case built in Excel for a sugar refinery that packs white sugar and ships it to distributors. I played the role of the planning analyst.

> **Data note:** All numbers are synthetic (invented for practice). They are not from any real company, including any I interned at.

## What the case covers

| # | Task | Method |
|---|------|--------|
| 1 | Demand forecast (52 weeks of history) | 4-week moving average vs exponential smoothing (alpha 0.3), compared by MAPE |
| 2 | Inventory policy | Safety stock (95% service level, demand and lead-time variability), reorder point, EOQ |
| 3 | 12-week supply plan check | Projected inventory vs safety stock, flags for shortage risk, excess and over capacity |
| 4 | KPIs | Fill rate, forecast accuracy, days of cover, inventory value |
| 5 | ABC classification | 8 SKUs ranked by annual value, cumulative % of value |

## Key results

- Better forecast method: moving average (MAPE 8.27% vs 8.39%), forecast for week 53: 92.6 t
- Safety stock: about 100.5 t. Reorder point: about 324 t. EOQ: about 112 t
- Inventory position is 280 t, below the reorder point, so order now
- 12-week plan: shortage risk in week 60, over capacity in week 63, excess in week 64
- Fill rate (weeks 41 to 52): 96.6%. Forecast accuracy: 91.7%. Days of cover: 11.3
- ABC: bulk sugar 50 kg and liquid sugar carry about 93% of value; the other six SKUs are class C

## Repository layout

```
data/       input data (weekly demand, parameters)
excel/      the Excel workbook with the task sheets and formulas
results/    exported results as CSV
```

## How to use

1. Open `excel/Sugar_Planning_Practice.xlsx`.
2. Do the tasks on sheets `1_Forecast` to `5_ABC` using formulas.
3. Compare with the `Key_` sheets.

## Tools

Microsoft Excel: AVERAGE, STDEV, NORMSINV, SUMIF, ranking, conditional flags.

## Author

Abdelrahman Mohamed, Chemical Engineer, Cairo University
LinkedIn: https://www.linkedin.com/in/abdelrahman-mohamed-b12b67203/
