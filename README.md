# Business Growth Dashboard

Self-directed portfolio project — an interactive Power BI dashboard built on a public sales dataset (Kaggle), tracking revenue, profit margins, customer behavior, and product performance.

## Overview

Manual, spreadsheet-based sales reporting is a common problem for many businesses — reports take days to compile, and there's no easy way to drill into performance by product, region, or customer segment. I built this project to practice solving that kind of problem end-to-end: from raw sales data to a live, interactive Power BI dashboard.

Dataset: This analysis uses data with a structure and business context exactly comparable to real company data, extracted from a public dataset.

## Objectives
-Build a centralized, interactive dashboard for sales performance monitoring
-Practice drill-down and cross-filtering design for self-service analytics
-Model KPIs a real sales/business team would track: revenue, profit margin, growth rate, customer segments
-Explore what a fast (minutes, not days) reporting workflow could look like with Power BI vs. manual Excel reporting
## Approach

1. Data modeling : Built a star schema with a central Sales fact table and dimension tables for Date, Products, Customers, Regions, and Sales Representatives.

2. Dashboard build: Interactive Power BI report:

Executive Summary — high-level KPIs, revenue trend, top performers
Sales Analysis — YoY/MoM comparisons, sales breakdown by product/region/time
Product Performance — top/bottom products, profitability analysis
Customer Insights — RFM segmentation, customer lifetime value
Geographic Analysis — regional performance maps

3. DAX measures

Revenue = SUM(Sales[Amount])
Profit = SUM(Sales[Amount]) - SUM(Sales[Cost])
Profit Margin % = DIVIDE([Profit], [Revenue], 0)
YoY Growth = ([Current Year Revenue] - [Previous Year Revenue]) / [Previous Year Revenue]

4. Interactivity : Dynamic date slicers, cross-filtering across visuals, drill-through pages for product/customer detail, tooltips, bookmarks for saved views, and a mobile-optimized layout.

**What the analysis surfaced:** 
-A clear seasonal spike in Q4 sales in the dataset, the kind of pattern that would inform inventory planning in a real business
-A small share of products driving a disproportionate share of revenue (a classic 80/20 pattern)
Distinct customer segments via RFM analysis that could support targeted marketing in a real deployment

These are patterns observed in the dataset, not outcomes delivered for a live business — this project is a practice build, not a deployed company system.

How this dashboard could be adapted


-Faster reporting (self-service dashboard vs. multi-day manual compilation)

-Earlier visibility into underperforming products/regions

-Data-backed customer segmentation for marketing

Tools

Power BI Desktop · DAX · Power Query · Star schema data modeling
