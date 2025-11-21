# ds_web3_trading_team: Sentiment and Trading Behavior Analysis

This repository contains the analysis for the Web3 Trading Team data science assignment, exploring the relationship between Bitcoin Market Sentiment (Fear/Greed) and Historical Trader Behavior from a decentralized exchange (Hyperliquid).

## 1. Directory Structure

The submission strictly adheres to the required structure:
ds_aryan/
├── notebook_1.ipynb # All work should be done in Google Colab
notebooks.
├── notebook_2.ipynb # (Optional) Additional Colab notebook if
needed.
├── csv_files/ # Store all CSVs or data outputs here.
│ └── *.csv # Any intermediate or processed data files.
├── outputs/ # Store all visual outputs, graphs, or charts here.
│ └── *.png / *.jpg # Image results of EDA, charts, etc.
├── ds_report.pdf # Final summarized insights and explanations.
└── README.md # (Optional but encouraged) Setup
instructions, notes.


## 2. Setup and Execution

### Dependencies

The analysis requires the following Python libraries:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scipy`

### Data Cleaning and Processing Notes

1.  **Sentiment Classification:** The `classification` column was mapped to two categories: **Fear** (Extreme Fear, Fear) and **Greed** (Extreme Greed, Greed). **Neutral** days were excluded.
2.  **Leverage Metric:** To handle the lack of direct margin data, **Effective Leverage** was calculated as a proxy:
    $$\text{Effective Leverage} = \frac{\sum \text{Notional Value (Exposure)}}{\sum \text{Start Position Value (Margin Proxy)}}$$
    This metric was analyzed using the **median** due to extreme outliers in the calculated mean values.
3.  **Key Finding:** Contrary to typical market belief, **Fear** days in this dataset showed **statistically higher PnL and trading volume**.