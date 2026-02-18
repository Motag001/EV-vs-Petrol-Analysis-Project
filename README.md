# EV vs. Petrol Dataset Analysis Report

This report summarizes the initial data loading, exploration, and key findings from the `ev_vs_petrol_dataset_v3.csv` dataset.

## Data Loading and Initial Inspection

The dataset was successfully loaded into a pandas DataFrame. It contains `1200` entries and `22` columns, providing a comprehensive overview of various factors influencing the EV and petrol vehicle markets. The data types are appropriate for analysis, with a mix of numerical (int64, float64) and categorical (object) columns.

## Duplicate Check

A check for duplicate rows was performed, and it was confirmed that the dataset contains **no duplicate entries**, ensuring data integrity for further analysis.

## Key Findings

### Countries with Highest Fuel Prices

The analysis identified the following countries with the highest fuel prices (USD per liter):

| Country        | Max Fuel Price (USD/Liter) |
|:---------------|:---------------------------|
| Norway         | 2.153                      |
| Netherlands    | 2.153                      |
| Sweden         | 2.097                      |
| Italy          | 2.053                      |
| Belgium        | 2.007                      |
| Germany        | 2.007                      |
| France         | 1.983                      |
| Switzerland    | 1.937                      |
| Portugal       | 1.903                      |
| United Kingdom | 1.883                      |

### Relationship Between Fuel Price and EV Market Share

The Pearson correlation coefficient between 'fuel_price_usd_per_liter' and 'ev_market_share' was calculated to be approximately `0.554`.

This indicates a **moderate positive linear relationship**: as fuel prices per liter increase, the EV market share tends to increase. This suggests that rising fuel costs could be a contributing factor to the growth in electric vehicle adoption.

### Average EV Range Over the Years

The average EV range (in kilometers) has shown a consistent upward trend over the years, as visualized in the generated bar chart. This indicates significant advancements in battery technology and EV development, leading to vehicles capable of covering longer distances.

```python
# Data used for the EV range visualization:
#    year  avg_ev_range_km
# 0   2010           120.28
# 1   2011           128.20
# 2   2012           139.16
# 3   2013           143.12
# 4   2014           153.44
# 5   2015           168.60
# 6   2016           188.04
# 7   2017           217.48
# 8   2018           258.56
# 9   2019           295.08
# 10  2020           335.52
# 11  2021           366.20
# 12  2022           396.12
# 13  2023           423.36
# 14  2024           449.40
# 15  2025           471.40
```

## Next Steps

Further analysis could involve exploring causality, identifying other confounding factors influencing EV adoption (e.g., government subsidies, charging infrastructure, GDP per capita), and predictive modeling for future market trends.
