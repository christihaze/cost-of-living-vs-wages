# Cost of Living vs Wages (2015–2025)
## Overview

This Power BI dashboard explores how the cost of living and wages have changed across the United States from 2015 through 2025.
I combined Consumer Price Index (CPI) data from the Bureau of Labor Statistics with Occupational Employment and Wage Statistics (OEWS) to see if paychecks have actually kept up with inflation.

The project looks at five main spending categories — food, shelter, energy, and medical care — which represent about 70% of essential living costs. The goal was to estimate how affordable life really is today compared to pre-COVID years.

## Questions
•How much have living costs and wages changed from 2015 to 2025?
•Which regions have seen the biggest gap between pay and expenses?
•Which spending categories (like housing or energy) are driving inflation the most?
•Did wages actually keep up with inflation, or are households falling behind?
•How has the COVID-19 period affected affordability trends?
•Which regions are the most and least affordable based on the Affordability Index?
•What does the Wage Power Gap show about real purchasing power across time?

## Data Sources
Bureau of Labor Statistics (BLS)	
OEWS (Occupational Employment and Wage Statistics)
Calculated Dataset

## Data Cleaning & Preparation

-Cleaned and merged CPI and wage data in Python.
-Grouped locations into Census-defined regions.
-Aggregated data by year and category.
-Adjusted 2025 values using trend-based estimates.
-Created calculated columns for:
-Estimated Cost = Base Cost × (CPI ÷ Base CPI)
-Affordability Index = (Avg Wage ÷ Estimated Cost) × 0.7
-Wage Power Gap % = Wage Growth % – Inflation Growth %

## Dashboard Pages

Data Overview – Snapshot of the dataset and national trends.
Regional Breakdown – Compares wages and CPI by region.
Cost Breakdown – Looks at how each spending category drives inflation.
Real-World Impact – Highlights wage vs. inflation growth over time.
Regional Wages vs. Costs – Year-by-year view of costs and wages per region.
U.S. Affordability Overview – Calculates the adjusted affordability index.
Data Transparency – Documents data sources, methods, and formulas.

## Key Takeaways

•Wages grew about 40% from 2015–2025, while inflation rose 35% — meaning paychecks only slightly outpaced rising prices.
•The average affordability index (1.03) shows most households are just breaking even.
•Northeast and Midwest remain the most stable regions, while the West faces the highest cost pressures.
•Once all living costs are included (beyond the 70% analyzed here), real affordability would likely fall below 1.0 — meaning costs still outweigh income.

