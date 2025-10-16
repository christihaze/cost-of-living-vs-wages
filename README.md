# Cost of Living vs Wages (2015–2025)
## Overview

This Power BI dashboard explores how the cost of living and wages have changed across the United States from 2015 through 2025.
I combined Consumer Price Index (CPI) data from the Bureau of Labor Statistics with Occupational Employment and Wage Statistics (OEWS) to see if paychecks have actually kept up with inflation.

The project looks at five main spending categories — food, shelter, energy, and medical care — which represent about 70% of essential living costs across the Four Census Regions. The goal was to estimate how affordable life really is today compared to pre-COVID years.

## Four Census Regions:

Northeast: Maine, New Hampshire, Vermont, Massachusetts, Rhode Island, Connecticut, New York, New Jersey, Pennsylvania

Midwest: Ohio, Indiana, Illinois, Michigan, Wisconsin,Minnesota, Iowa, Missouri, North Dakota, South Dakota, Nebraska, Kansas

South: Delaware, Maryland, District of Columbia, Virginia, West Virginia, North Carolina, South Carolina, Georgia, Florida, Kentucky, Tennessee, Alabama, Mississippi,Arkansas, Louisiana, Oklahoma, Texas

West: Montana, Idaho, Wyoming, Colorado, New Mexico, Arizona, Utah, Nevada, Washington, Oregon, California, Alaska, Hawaii

## Questions

•How much have living costs and wages changed from 2015 to 2025?

•Which regions have seen the biggest gap between pay and expenses?

•Which spending categories (like housing or energy) are driving inflation the most?

•Did wages actually keep up with inflation, or are households falling behind?

•How has the COVID-19 period affected affordability trends?

•Which regions are the most and least affordable based on the Affordability Index?

•What does the Wage Power Gap show about real purchasing power across time?

## What is CPI?

CPI = Consumer Price Index

Tracks price changes for everyday items (food, shelter, energy, healthcare)
Example: Food CPI goes 200 → 210 → +5% increase

-The Problem:

--cpi is an index its not in dollars(A value of 250 doesnt equal  $250,  it just means prices are 25% higher than the year before.)

-My Solution: Estimated Costs

Estimated Cost = Base Cost × (CPI ÷ Base CPI)

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

  --Estimated Cost = Base Cost × (CPI ÷ Base CPI)
      
  --Affordability Index = (Avg Wage ÷ Estimated Cost) × 0.7
  
  --Wage Power Gap % = Wage Growth % – Inflation Growth %

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

Explaining Cpis:

## Wage data gap solution:


Problem: CPI goes into 2025, but BLS hasn’t released 2025 wages yet  creating nan values. The wages were only for the regions no national data.

Solution: Since the BLS wage data wasn’t available for every single year — especially 2025 — I filled missing values using the previous year’s numbers or, for 2025, projected them forward using the average growth rate from prior years.
This way, the dataset stays consistent and realistic without breaking regional trends.
It’s not perfect, but it gives a reasonable estimate for how wages likely continued into 2025.

