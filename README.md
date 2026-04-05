# Hyper-Local-Market-Trend-Analysis

# Project Overview
Local farmers, traders, and government bodies often lack data-driven insights into commodity price movements. This project bridges that gap by:

1. Tracking 41 unique commodities across 169 active markets in 31 States/UTs
2. Identifying seasonal price patterns and regional price disparities
3. Forecasting next 6-month commodity prices using Facebook Prophet / ARIMA
4. Visualizing insights on an interactive Power BI dashboard

 # Problem Statement

"Which commodity prices will rise in the next 6 months, and in which districts of Odisha are prices consistently highest?"

This helps:

* 🌾 Farmers — decide when to sell or store crops
* 🛒 Traders — plan inventory and procurement
* 🏛️ Government — identify supply chain issues and intervene early

# Project Structure

```text
HyperLocal-Market-Analysis/
│
├── 📂 data/
│   ├── raw/                    # Original data from data.gov.in / Agmarknet
│   ├── cleaned/                # Cleaned and processed datasets
│   └── forecasts/              # Model output — predicted prices
│
├── 📂 notebooks/
│   ├── 01_data_cleaning.ipynb      # SQL + Pandas cleaning
│   ├── 02_eda.ipynb                # Exploratory Data Analysis
│   ├── 03_forecasting.ipynb        # ARIMA / Prophet model
│   └── 04_insights_summary.ipynb   # Business insights
│
├── 📂 sql/
│   ├── cleaning_queries.sql        # Null handling, deduplication
│   └── analysis_queries.sql        # Window functions, aggregations
│
├── 📂 dashboard/
│   └── market_dashboard.pbix       # Power BI dashboard file
│
├── 📂 screenshots/
│   └── dashboard_preview.png       # Dashboard screenshot
│
└── 📄 README.md
```
# Tools & Technologies

  Layer----------------------------------------Tool
* Data Collection --------------------          data.gov.in, Agmarknet.gov.in, Web Scraping (Python)
* Data Cleaning    --------------------         SQL (PostgreSQL / MySQL), Python (Pandas)
* Analysis (EDA)   --------------------         Python (Matplotlib, Seaborn), SQL Window Functions
* Forecasting      --------------------         Python (Facebook Prophet, ARIMA)
* Visualization     --------------------        Power BI Desktop
* Version Control   --------------------        Git + GitHub
