# Financial Market Intelligence & Risk Analytics

An end-to-end data analytics project exploring the historical performance and risk characteristics of five major US technology stocks using Python, Pandas, PostgreSQL, SQL, and Power BI.

## Project Overview

Financial Market Intelligence & Risk Analytics analyzes approximately ten years of historical stock price data for five publicly traded technology companies. The project demonstrates a complete analytics workflow, from collecting raw financial data to processing datasets, querying a relational database, calculating performance and risk metrics, and presenting findings through an interactive Power BI dashboard.

The primary objective is to understand how these stocks performed over time and compare their returns, volatility, and maximum drawdowns.

## Business Objectives

- Analyze long-term stock price movements and performance.
- Calculate daily returns and cumulative price performance.
- Compare average daily returns across stocks.
- Measure daily volatility as an indicator of price variability.
- Calculate maximum drawdown to understand historical peak-to-trough declines.
- Store and analyze structured financial data using PostgreSQL and SQL.
- Build an interactive Power BI dashboard for visual comparison and exploration.

## Stocks Analyzed

| Company   | Ticker |
|-----------|--------|
| Apple     | AAPL   |
| Amazon    | AMZN   |
| Alphabet  | GOOGL  |
| Microsoft | MSFT   |
| NVIDIA    | NVDA   |

**Dataset coverage:** October 21, 2016 – October 21, 2026

**Dataset size:** 12,565 rows across five stocks, with 2,513 observations per stock.

## Technology Stack

| Technology         | Purpose 							|
|--------------------|----------------------------------------------------------|
| Google Sheets      | Historical stock data collection using `GOOGLEFINANCE()` |
| CSV                | Data export and transfer                                 |
| Python             | Data processing and analysis 				|
| Pandas             | Data cleaning, transformation, and metric calculation	|
| PostgreSQL         | Relational database storage 				|
| SQL                | Performance and risk analysis 				|
| Microsoft Power BI | Interactive dashboard and visualization 			|

## Data Collection

Historical stock price data was collected using the `GOOGLEFINANCE()` spreadsheet function in Google Sheets.

The data was organized in spreadsheets and exported as CSV files. These files served as the raw inputs for subsequent processing and analysis in Python.

This workflow provided a straightforward way to collect and organize historical market data without building a custom API integration or web scraper.

## Project Workflow

1. **Data collection:** Retrieve historical stock price data in Google Sheets using `GOOGLEFINANCE()`.
2. **Data export:** Download the collected data as CSV files.
3. **Data processing:** Use Python and Pandas to inspect, clean, combine, and transform the datasets.
4. **Feature engineering:** Calculate daily returns and cumulative price returns.
5. **Database storage:** Load the consolidated stock price dataset into PostgreSQL.
6. **SQL analysis:** Query stock performance, daily risk, maximum drawdown, and summary metrics.
7. **Data export:** Save processed datasets and stock-level summary metrics as CSV files.
8. **Visualization:** Build an interactive Power BI dashboard for performance and risk analysis.

## Key Metrics

### 1. Price Change (%)

Measures the percentage change between the first and last recorded closing prices in the dataset.

### 2. Daily Return (%)

Measures the percentage change in closing price between consecutive trading observations.

### 3. Cumulative Return

Tracks price performance over time relative to the initial observation.

### 4. Daily Volatility (%)

Measures the standard deviation of daily returns, providing an indication of historical price variability.

### 5. Maximum Drawdown (%)

Measures the largest percentage decline from a historical running peak to a subsequent trough.

### 6. Average Daily Return (%)

Calculates the average of daily returns over the observed period.

## SQL Analysis

The project includes four SQL scripts:

- `01_stock_performance.sql` — Stock performance analysis.
- `02_daily_risk_analysis.sql` — Daily return and risk analysis.
- `03_maximum_drawdown.sql` — Maximum drawdown analysis.
- `04_stock_summary.sql` — Stock-level summary metrics.

The PostgreSQL database is named `financial_market_intelligence`, with the consolidated stock data stored in the `stock_prices` table.

## Power BI Dashboard

The interactive dashboard, titled **Financial Market Intelligence**, contains the following visuals:

- **KPI cards:** Average daily return, highest price change, number of stocks, and maximum volatility.
- **Daily closing prices:** Compares historical closing price trends across all five stocks.
- **Price change by stock:** Compares overall price appreciation over the analysis period.
- **Daily returns by stock:** Visualizes daily price movements and fluctuations.
- **Maximum drawdown by stock:** Compares the largest historical peak-to-trough declines.
- **Daily volatility by stock:** Compares the variability of daily returns.
- **Ticker slicer:** Allows users to filter the dashboard by individual stocks.

The dashboard uses a dark navy theme and a multi-panel layout to present performance and risk indicators together.

## Key Findings

The analysis highlights several differences in historical performance and risk across the five stocks.

- **NVIDIA (NVDA)** recorded the largest calculated price increase in the dataset, approximately 13,034%.
- **Apple (AAPL)** recorded a calculated price increase of approximately 1,080%.
- **Microsoft (MSFT)** recorded a calculated price increase of approximately 793%.
- **Alphabet (GOOGL)** recorded a calculated price increase of approximately 713%.
- **Amazon (AMZN)** recorded a calculated price increase of approximately 541%.
- NVIDIA also recorded the highest daily volatility among the five stocks, approximately 3.16%.
- NVIDIA experienced a maximum drawdown of approximately -66.36%, while Amazon experienced a maximum drawdown of approximately -56.15%.

These findings illustrate that stronger historical price appreciation can coexist with substantial volatility and drawdown risk.

*Note: These are historical observations from the collected dataset, not forecasts or investment recommendations.*

## Project Structure

```text
Financial_Market_Intelligence/
│
├── data/
│   ├── raw/
│   │   └── stock_prices/
│   └── processed/
│       ├── stock_market_master.csv
│       └── stock_summary.csv
│
├── notebooks/
│   └── 01_data_quality_check.ipynb
│
├── sql/
│   ├── 01_stock_performance.sql
│   ├── 02_daily_risk_analysis.sql
│   ├── 03_maximum_drawdown.sql
│   └── 04_stock_summary.sql
│
├── screenshots/
│
├── README.md
└── requirements.txt
```

The `screenshots/` directory and `requirements.txt` are intended for the final portfolio package if they have not yet been added. The Power BI report file should also be included in the repository or linked separately when appropriate.

## Limitations

- The analysis uses closing prices rather than dividend-inclusive adjusted total returns.
- Historical price changes do not represent an investor's complete realized return.
- Results depend on the accuracy, availability, and consistency of the source data.
- Stock splits and other corporate actions can affect price comparisons if historical prices are not consistently adjusted.
- Historical volatility and drawdowns do not predict future market risk.
- The project is intended for educational and analytical purposes and does not constitute investment advice.

## Future Improvements

Potential extensions include:

- Adding annual and rolling-period performance comparisons.
- Calculating risk-adjusted metrics such as the Sharpe ratio.
- Comparing stock performance against a market benchmark.
- Adding sector-level comparisons.
- Automating data refresh and the processing workflow.
- Improving reproducibility through documented dependencies and database setup instructions.

## Author

This is my first Data Analysis Project, A thought of combining my education related to Stock Market and Data Analysis initiated the idea to build this model. Took help from ChatGPT for better understanding and modeling of this project. Learned & Applied Python, Pandas, SQL, PostgreSQL, and Power BI to a financial market analysis use case. Looking forward for suggestions & new ideas. 
