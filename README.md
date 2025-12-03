# Portfolio Advisory — CFM101 Group Project

This Jupyter Notebook was developed for the **CFM101 group project** as a complete portfolio optimization tool. It processes a list of stock tickers, evaluates their financial characteristics, and constructs a fully optimized long-term equity portfolio. The final output includes precise share quantities for a configurable investment amount.

The resulting portfolio is **designed and estimated to outperform the market**, using a quantitative selection process and the Black-Litterman optimization framework.

---

## Overview

This project generates an optimized portfolio by combining quantitative screening with modern asset allocation techniques. After validating the provided tickers, the model identifies the most attractive equities and allocates capital strategically with long-term performance and benchmark outperformance in mind.

### Core Functionality

* Accepts a CSV file containing **only ticker symbols**
  (see `tickers_example.csv` for correct formatting or testing)
* Cleans and validates tickers using `yfinance`
* Computes four quantitative metrics for each ticker:
  **Alpha, Sortino Ratio, Momentum, Beta**
* Ranks and selects the **top X tickers** (default: 10)
* Uses **three years of historical market data** for all calculations
* Optimizes portfolio weights using the **Black-Litterman Model**, producing allocations intended to outperform the benchmark market average
* Constructs a portfolio of **$1,000,000 CAD** (default)
* Outputs a final CSV containing:

  * Ticker
  * Optimized weight
  * Number of shares to purchase

---

## Getting Started

### 1. Download Files

Download PortfolioOptimser.ipynb, open in an environment that supports jupyter notebook files, and create a list of tickers in a csv (or use one of ours)!

### 2. Input File

Upload a CSV file containing only ticker symbols, one per line. Replace `Tickers_Example.csv` with your csv. 
Refer to `Tickers_Example.csv` for the expected structure or to test the system.

### 3. Adjustable Parameters

At the beginning of the notebook, you may modify:

* Total portfolio value (default: $1,000,000 CAD)
* Number of stocks to include in the portfolio (default: 10)

### 4. Running the Notebook

Once executed, the notebook will:

1. Validate and clean the input tickers
2. Calculate financial metrics
3. Rank and select the strongest candidates
4. Optimize their weights using the Black-Litterman Model
5. Generate a new CSV containing the completed portfolio

---

## Notes and Limitations

This program relies on the `yfinance` API for historical data.
If errors occur due to temporary API issues, simply re-running the notebook will typically resolve the problem.
