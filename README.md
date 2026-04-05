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

 # Data Sources

data.gov.in — Government of India open data portal

# Step 1 — Data Cleaning
* Tools: SQL + Python (Pandas)
* Key cleaning tasks performed:

* Removed null / missing values in price and date columns
* Eliminated duplicate records across market entries
* Standardized Odia district names to English format
* Fixed date format inconsistencies (DD-MM-YYYY → YYYY-MM-DD)
* Detected and handled outliers using IQR method

  # Step 2 — Exploratory Data Analysis (EDA)
* Key questions answered:

* Which month sees the highest commodity prices? (Seasonality)
* Which district has the most expensive / cheapest prices? (Regional variance)
* How much have prices increased over the past 5 years?
* Which commodities show the most volatility?

* Key findings from the dashboard:

* Delhi leads with the highest average price (₹313/KG)
* Ghee is the most expensive commodity at ₹681/KG average
* Prices across cereals and oil categories spiked significantly around 2008–2010
* Milk and dairy show a steady upward trend post-2015

# Business Insights

1. July–September sees consistent price rises in vegetables → farmers should store crops and sell post-peak
2. Delhi and Maharashtra have significantly higher avg prices than eastern states → supply chain gap exists
3. Ghee and Tea are the highest-priced commodities → premium product opportunity for rural cooperatives
4. Oil prices are highly volatile (peaked 2008) → hedging strategies recommended for bulk buyers
5. Sikkim and Manipur show above-average prices despite smaller markets → logistics cost is the likely driver

 # About This Project
Built as part of a Data Analytics Portfolio to demonstrate end-to-end skills:

* Real data sourcing from government portals
* SQL + Python data engineering
* Statistical forecasting
* Business storytelling via Power BI

This project is specifically relevant for Odisha / India job market where hyper-local agricultural data analysis is an emerging and high-impact domain.
