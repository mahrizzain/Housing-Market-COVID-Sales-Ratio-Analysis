# Data

## Source

**Real Estate Sales 2001–2022** — Connecticut Office of Policy and Management (OPM), retrieved from [data.gov / data.ct.gov](https://catalog.data.gov/dataset/real-estate-sales-2001-2018).

- Population: ~1,000,000 Connecticut real estate transactions (sale amount > $2,000), 2001–2022.
- Sample analyzed in this project: **273,308 transactions, 2017–2022** (2017–2019 pre-COVID, 2020–2022 post-COVID).

## Files

| File | Description |
|------|-------------|
| `processed/data_summary.csv` | Yearly transaction counts, sales-ratio sums and averages, pre/post-COVID means, and the standard deviation of the sales ratio — computed from the full sample in Excel. |

> The full sample workbook (~27 MB, 273K rows) exceeds GitHub's file-size limits and is not hosted in this repository. It can be reproduced from the public source dataset above using the filters described in the project paper.

## Data Dictionary

| Column | Description |
|--------|-------------|
| Serial Number | Unique identifier for the transaction record |
| List Year | Year the property was listed |
| Date Recorded | Date the sale was recorded |
| Town | Connecticut town where the property is located |
| Address | Property address |
| Assessed Value | Town-assessed value of the property ($) |
| Sale Amount | Final sale price ($) |
| **Sales Ratio** | **Assessed Value ÷ Sale Amount** — the key variable in this analysis. Below 1 favors the seller; above 1 means the property sold below its assessed value |
| Property Type | Category of property (e.g., residential, commercial) |
| Residential Type | Subtype for residential properties |
| Non Use Code | Code indicating non-standard use, if any |
| Assessor Remarks | Notes from the town assessor |
| OPM Remarks | Notes from the Office of Policy and Management |
| Location | Property coordinates |
