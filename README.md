# Cost of Living vs Wages (2015–2025)
Overview

This Power BI dashboard explores how the cost of living and wages have changed across the United States from 2015 through 2025.
I combined Consumer Price Index (CPI) data from the Bureau of Labor Statistics with Occupational Employment and Wage Statistics (OEWS) to see if paychecks have actually kept up with inflation.

The project looks at five main spending categories — food, shelter, energy, and medical care — which represent about 70% of essential living costs. The goal was to estimate how affordable life really is today compared to pre-COVID years.

Objectives

Track CPI inflation trends by spending category.

Compare average wages vs. estimated household costs over time.

Measure how affordability has changed across U.S. regions (Midwest, South, Northeast, West).

Calculate the Affordability Index to show if households are breaking even or falling behind.

Show the Wage Power Gap, or the difference between wage growth and inflation growth.

Data Sources
Source	Description	Years	Notes
Bureau of Labor Statistics (BLS)	CPI data for food, shelter, energy, and medical care	2015–2025	Converted from monthly to yearly averages
OEWS (Occupational Employment and Wage Statistics)	Annual wage data by state and region	2015–2024	Used for wage comparisons
Calculated Dataset	Estimated total household costs	2015–2025	Adjusted to 70% coverage for core living costs
Data Cleaning & Preparation

Cleaned and merged CPI and wage data in Python.

Grouped locations into Census-defined regions.

Aggregated data by year and category.

Adjusted 2025 values using trend-based estimates.

Created calculated columns for:

Estimated Cost = Base Cost × (CPI ÷ Base CPI)

Affordability Index = (Avg Wage ÷ Estimated Cost) × 0.7

Wage Power Gap % = Wage Growth % – Inflation Growth %

Dashboard Pages

Data Overview – Snapshot of the dataset and national trends.

Regional Breakdown – Compares wages and CPI by region.

Cost Breakdown – Looks at how each spending category drives inflation.

Real-World Impact – Highlights wage vs. inflation growth over time.

Regional Wages vs. Costs – Year-by-year view of costs and wages per region.

U.S. Affordability Overview – Calculates the adjusted affordability index.

Data Transparency – Documents data sources, methods, and formulas.

Key Takeaways

Wages grew about 40% from 2015–2025, while inflation rose 35% — meaning paychecks only slightly outpaced rising prices.

The average affordability index (1.03) shows most households are just breaking even.

Northeast and Midwest remain the most stable regions, while the West faces the highest cost pressures.

Once all living costs are included (beyond the 70% analyzed here), real affordability would likely fall below 1.0 — meaning costs still outweigh income.

Tools Used

Power BI for data modeling and visualization

Python (pandas) for cleaning and combining datasets

Excel / CSVs for manual review

Color Theme: Dark mode with purple and white accents for readability
