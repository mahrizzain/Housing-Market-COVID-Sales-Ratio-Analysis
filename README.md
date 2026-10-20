# Housing Market Analysis: COVID-19 and the Sales Ratio

An analysis of roughly 273,000 Connecticut real estate transactions testing whether COVID-19 significantly changed the average **sales ratio** (assessed value ÷ sale amount) between the pre-COVID period (2017–2019) and the post-COVID period (2020–2022).

*HS Data Science and Analytics — Fort Worth, TX (2025). Built with Excel.*

## Research Question

Did the average sales ratio of real estate transactions differ significantly between pre- and post-COVID-19? A sales ratio below 1 favors the seller (the home sold for more than its assessed value); above 1 means it sold for less.

- **Null hypothesis:** There is no significant difference in mean sales ratio between pre- and post-COVID.
- **Alternative hypothesis:** There is a significant difference in mean sales ratio between pre- and post-COVID.

## Data

- **Source:** [Real Estate Sales 2001–2022](https://catalog.data.gov/dataset/real-estate-sales-2001-2018) — Connecticut Office of Policy and Management, via data.gov / data.ct.gov.
- **Population:** ~1 million Connecticut transactions (sales above $2,000), 2001–2022.
- **Sample analyzed:** 273,308 transactions from 2017–2022, stored and analyzed in Excel.
- **Variables used:** year of sale and sales ratio, plus property type, town, assessed value, and sale amount from the original records.

> The full workbook (273K rows, ~27 MB) exceeds GitHub's file-size limits, so the complete dataset is not hosted here. The yearly summary statistics are in [`data/processed/data_summary.csv`](data/processed/data_summary.csv), the data dictionary is in [`data/README.md`](data/README.md), and the raw data is publicly available at the source link above.

## Methods

1. Filtered the dataset to 2017–2019 (pre-COVID) and 2020–2022 (post-COVID).
2. Computed per-year transaction counts, total and average sales ratios, and the standard deviation of the sales ratio using Excel formulas.
3. Ran a **paired t-test** for the difference of means between the pre- and post-COVID periods (after checking randomness, normality, and independence conditions).
4. Flagged 2018 as a potential outlier year and verified it with a **1.5×IQR test**, then re-ran the t-test without 2018 to confirm the result held.

## Results

| Year | Transactions | Avg. Sales Ratio |
|------|-------------:|-----------------:|
| 2017 | 45,691 | 2.33 |
| 2018 | 50,709 | 9.35 *(outlier)* |
| 2019 | 58,954 | 1.14 |
| 2020 | 66,592 | 0.83 |
| 2021 | 39,511 | 1.42 |
| 2022 | 11,851 | 1.02 |
| **Total** | **273,308** | |

- **Pre-COVID mean sales ratio (2017–2019): 4.27**
- **Post-COVID mean sales ratio (2020–2022): 1.09**
- Standard deviation of sales ratio: **1.43**
- Paired t-test: **t = 787.52, df = 124,999, p ≈ 0.0** → reject the null hypothesis.
- 2018's average (9.35) exceeded the 1.5×IQR outlier threshold of 4.3. Excluding 2018, the re-run test (t = 160, p ≈ 0.0) was still highly significant.

## Conclusion

There is a statistically significant difference in sales ratio between the pre- and post-COVID periods — the average sales ratio dropped sharply after COVID, suggesting homes sold closer to (or above) their assessed values. However, the decline began in 2019, before the pandemic, so the results show a significant period difference without proving COVID-19 was the sole cause. The full reasoning, literature review, and limitations are in the [project paper](reports/paper.md).

## Project Structure

```
├── README.md                  # Project overview (this file)
├── data/
│   ├── README.md              # Data source and dictionary
│   └── processed/
│       └── data_summary.csv   # Yearly summary statistics
└── reports/
    └── paper.md               # Full project paper
```

## Tools

Excel (data cleaning, formulas, summary statistics, paired t-test) · Data from data.gov / data.ct.gov
