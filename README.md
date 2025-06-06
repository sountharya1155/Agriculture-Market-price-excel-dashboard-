#  Agriculture Market Price Dashboard

A visually interactive Excel dashboard that transforms raw agricultural price data into actionable insights for farmers, traders, analysts, and policymakers.

## Project Overview

This project showcases how Excel — with smart formulas, pivot tables, and dynamic charts — can be used to create a powerful, no-code dashboard to analyze commodity prices across different markets and states.

The dashboard provides:
- Quick KPIs (e.g., total commodities, average modal price)
- Visual price comparison across commodities
- Distribution of markets by grade
- High-performing commodities & regional insights

## Data Cleaning & Preparation

Before building the dashboard, the dataset was thoroughly cleaned:

- **No blank cells** or missing values  
- **No duplicate rows**  
- Renamed columns (e.g., `Modal_x0020_Price` → `Modal Price`) for clarity  
- Named the entire dataset as `MarketData` for easy referencing in formulas  

##  Dashboard Features

### KPI Cards (Top-Level Metrics)
- **Total Commodities**:  
  `=COUNTA(UNIQUE(MarketData[Commodity]))`
- **Total Markets**:  
  `=COUNTA(UNIQUE(MarketData[Market]))`
- **Average Modal Price**:  
  `=ROUND(AVERAGE(MarketData[Modal Price]), 2)`
- **Highest Max Price Commodity**:  
  `=INDEX(MarketData[Commodity], MATCH(MAX(MarketData[Max Price]), MarketData[Max Price], 0))`

###  Visualizations via Pivot Charts
- **Clustered Column Chart**: Modal Price by Commodity
- **Stacked Column Chart**: Min, Modal, and Max Prices by Commodity
- **Pie Chart**: Count of Markets by Grade
- **Horizontal Bar Chart**: Count of Each Commodity

All charts are dynamically linked to the `MarketData` table using pivot tables to ensure updates flow smoothly with new data entries.

## Why This Matters

Whether you're a farmer identifying the best selling prices, a trader monitoring price trends, or a policymaker studying market distribution — this dashboard provides a **clear, actionable snapshot** of real-time market conditions.

## Getting Started

To try this project:
1. Clone the repository or download the `.xlsx` file
2. Open it in Excel 2019 or later (recommended)
3. Navigate the sheets — start with the **Dashboard** tab
4. Feel free to explore and customize the pivot tables and formulas

##  Tools Used

- Microsoft Excel 2019+
- Pivot Tables & Pivot Charts
- Dynamic Named Ranges
- Shapes & Illustrations



## Future Enhancements

- Add slicers for interactive filtering (by State, Date, etc.)
- Implement time-series trends (e.g., modal price over weeks)
- Enable automatic data refresh for live datasets
- Export PDFs for stakeholder reporting



