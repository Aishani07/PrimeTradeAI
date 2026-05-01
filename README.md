# Bitcoin Market Sentiment vs Trader Performance Analysis

## Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader performance using historical trading data. The objective is to identify patterns in trading outcomes based on prevailing market sentiment and derive actionable insights for improved trading strategies.

---

## Datasets Used

### 1. Bitcoin Market Sentiment Dataset

* Columns:

  * `date`
  * `classification` (Fear, Greed, Extreme Fear, Extreme Greed, Neutral)
  * `value` (sentiment index score)

### 2. Historical Trader Data (Hyperliquid)

* Columns include:

  * `Account`
  * `Coin`
  * `Execution Price`
  * `Size Tokens`
  * `Size USD`
  * `Side` (Buy/Sell)
  * `Timestamp IST`
  * `Start Position`
  * `Direction`
  * `Closed PnL`
  * Additional trade-related attributes

---

## Methodology

### Data Preprocessing

* Cleaned column names by removing extra spaces
* Converted timestamp fields into datetime format
* Standardized both datasets to a common `date` field for alignment

### Data Integration

* Merged trader data with sentiment data using the `date` column
* Ensured proper temporal alignment between trades and sentiment values

### Data Analysis

The following analyses were performed:

* Average profit/loss (PnL) by sentiment category
* Total PnL by sentiment category
* Trade count distribution across sentiment categories
* Comparative performance of Buy and Sell trades under different sentiments

### Visualization

* Bar charts for average PnL across sentiment categories
* Bar charts for total PnL across sentiment categories
* Comparative bar charts for Buy vs Sell performance

---

## Key Insights

* Traders achieve higher average profitability during periods of market greed.
* Buy trades tend to perform better during fear-driven market conditions.
* Sell trades generate higher returns during greed-driven phases.
* Extreme sentiment conditions (especially extreme greed) show reduced profitability, indicating market saturation.
* Trading strategies that act contrary to prevailing sentiment tend to yield better results.

---

## Strategy Recommendations

* Adopt a contrarian approach: consider buying during fear and selling during greed.
* Exercise caution during extreme sentiment phases due to increased market risk and reduced efficiency.
* Use sentiment as a supplementary indicator alongside technical and quantitative signals.
* Adjust position sizing and leverage based on prevailing sentiment conditions.

---

## Conclusion

The analysis demonstrates a measurable relationship between market sentiment and trader performance. Traders who adapt their strategies based on sentiment dynamics, particularly by leveraging contrarian approaches, can potentially improve profitability. Market sentiment serves as a valuable indicator when combined with disciplined trading strategies.

---

## Tools and Technologies

* Python
* Pandas
* Matplotlib

---

## How to Run

1. Place both datasets (`historical_data.csv` and `fear_greed_index.csv`) in the working directory.
2. Execute the Python script provided in this project.
3. Review the generated outputs and visualizations for analysis.

---

## Future Work

* Incorporate machine learning models to predict trader profitability based on sentiment
* Include additional market indicators such as volatility and volume
* Perform time-series analysis for deeper insights
* Extend the analysis to other cryptocurrencies
