# Agricultural Market Price Analysis Dashboard

## Project Overview
This project analyzes agricultural commodity prices across India to identify arbitrage opportunities for traders and regional pricing patterns. It demonstrates end-to-end data analytics: SQL data cleaning, exploratory analysis, Excel visualization, and an interactive Power BI dashboard.

---

## Objectives
- Identify commodity price spreads across Indian mandis (wholesale markets)
- Compare average prices by state and commodity
- Visualize geographic price distribution
- Build an interactive dashboard for data exploration

---

## Dataset
- **Source**: Kaggle — Daily Wholesale Commodity Prices – India Mandis
- **Date**: 19 May 2025 (single-day snapshot)
- **Coverage**: 16 states, 157 districts, 268 markets, 145 commodities
- **Rows**: 2,733 (2,724 after cleaning)

---

## Data Quality & Limitations

### Limitations
- **Single-day snapshot**: Cannot perform trend or seasonal analysis; findings reflect pricing on one date only

### Issues Found & Resolved
- 9 rows with zero min/max price but valid modal price (Kerala mandis) → removed
- State spelling error: "Uttrakhand" → corrected to "Uttarakhand"
- Commodity names with commas → handled for CSV parsing

---

## Analysis Process

1. **Data Cleaning (SQL)**: PostgreSQL import, validation, removal of invalid rows, spelling fixes
2. **Exploratory Analysis (SQL)**: Price spread calculations, state averages, commodity rankings
3. **Visualization (Excel)**: Pivot table for state-level pricing comparison with conditional formatting
4. **Interactive Dashboard (Power BI)**: Multi-visual dashboard with filters and KPIs

---

## Key Findings

### 1. Largest Price Spreads (% difference, same-day cross-market)
- **Cauliflower**: 4,233% spread (₹150 in Vikasnagar, Uttarakhand → ₹6,500 in Angamaly, Kerala)
- **Onion**: 4,033% spread (₹150 → ₹6,200)
- **Mousambi (Sweet Lime)**: 3,020% spread

*These spreads represent significant arbitrage opportunities for traders sourcing across mandis.*

### 2. State-Level Pricing
- **Highest average**: Nagaland (₹7,300)
- **Lowest average**: Madhya Pradesh (₹625)
- **Range**: 11.7x difference across states

### 3. Market Liquidity (most widely traded commodities)
- Tomato (145 markets), Potato (144), Onion (135) — most reliable for cross-market comparison

---

## Tools & Technologies
- **Database**: PostgreSQL 18.4, pgAdmin 4
- **SQL Editor**: VS Code + SQLTools
- **Analysis**: SQL (data cleaning, aggregation, ranking)
- **Visualization**: Microsoft Excel (pivot tables, conditional formatting)
- **Dashboard**: Power BI Desktop (DAX, interactive slicers, maps)

---

## Dashboard Components
- **Bar Chart**: Top 10 commodities by price spread % (maximum aggregation across markets)
- **Geographic Map**: Average commodity price by state with bubble sizing (larger = higher avg price)
- **Commodity Slicer**: Dropdown filter to explore individual commodities
- **KPI Cards**: Headline metrics (avg spread %, total state coverage)

### Dashboard Preview
![Agricultural Market Price Analysis Dashboard](<img width="962" height="547" alt="Screenshot 2026-07-31 151614" src="https://github.com/user-attachments/assets/892d88ba-69d4-418b-b229-eddaa1b4f165" />
)

---

## How to Use This Project

### View the Analysis
1. **SQL queries**: See `/sql/01_data_import_and_cleaning.sql` for data cleaning and exploratory queries
2. **Raw data**: Check `/data/commodity_price_clean.csv` (2,724 rows, ready for analysis)
3. **Interactive dashboard**: Open `/dashboard/projectbi.pbix` in Power BI Desktop
   - Use the commodity slicer to filter by product
   - Hover over map bubbles to see state-level averages
   - Click bar chart bars to drill into commodity details

---

## Repository Structure
agri-commodity-prices/
├── README.md # This file
├── data/
│ └── commodity_price_clean.csv # Cleaned dataset (2,724 rows)
├── sql/
│ └── 01_data_import_and_cleaning.sql # SQL import & analysis queries
├── dashboard/
│ └── projectbi.pbix # Power BI interactive dashboard
└── images/
└── dashboard.png # Dashboard screenshot

---

## Skills Demonstrated
- **SQL**: Data import, cleaning, aggregation, window functions, ranking
- **Excel**: Pivot tables, conditional formatting, data validation
- **Power BI**: DAX calculations, interactive slicers, map visuals, KPI cards, data modeling
- **Data Analysis**: Problem identification, data quality assessment, insight communication
- **Tools**: PostgreSQL, VS Code, Power BI, Excel

---

## Author
**Kshitij Gharat**  
B.Sc. IT | Aspiring Data Analyst  
[GitHub](https://github.com/Kshitijdotcom) | [Email](mail to:kshitijgharat12@gmail.com)
