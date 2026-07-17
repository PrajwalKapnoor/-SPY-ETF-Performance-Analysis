# SPY ETF Performance Analysis 📈

An end-to-end data analysis pipeline exploring 28 years of SPY (SPDR S&P 500 ETF Trust) daily price and volume data — from raw CSV to cleaned dataset, engineered metrics, and business-ready insights.

## Overview

This project walks through a complete data analysis workflow on a single, real-world financial time series: **Define → Load → Explore → Clean → Analyze → Visualize → Conclude**. It's built to demonstrate core data analysis skills — data wrangling, exploratory analysis, and translating raw numbers into a clear narrative — on a dataset any market participant would recognize.

**Dataset:** [ETF Prices dataset](https://www.kaggle.com/) (filtered to the SPY ticker) — 7,263 trading days from **1993-01-29 to 2021-11-30**.

## Key Findings

| Metric | Value |
|---|---|
| Highest close | $469.73 (Nov 18, 2021) |
| Lowest close | $43.41 (Feb 18, 1993) |
| Average daily return | 0.039% |
| Daily volatility (std) | 1.182% |
| Up days | 3,897 (53.7%) |
| Down days | 3,305 (45.5%) |
| Best single day | +14.52% (Oct 13, 2008) |
| Worst single day | -10.94% (Mar 16, 2020) |

**Takeaways:**
- SPY shows a long-term uptrend consistent with the S&P 500's historical growth, interrupted by sharp drawdowns during the Dot-Com Crash, the 2008 Financial Crisis, and the 2020 COVID crash.
- Daily returns cluster tightly around zero but with fat tails — large single-day moves are far more common than a normal distribution would predict.
- SPY closes up slightly more often than down, reflecting its long-run positive drift.
- Volume is right-skewed, with spikes clustering around the market's most volatile trading days rather than showing a simple linear relationship with returns.

## Visualizations

1. **Closing price trend** — full 28-year price history
2. **Daily return distribution** — histogram highlighting fat-tail risk
3. **Volume distribution** — trading activity skew
4. **Up vs. down days** — win/loss day split
5. **Volume vs. daily return** — scatter plot of activity vs. price movement

## Repository Structure

```
├── SPY_Day1_Pipeline.ipynb        # Full analysis notebook (Colab/Jupyter ready)
├── ETF_prices.csv                 # Source dataset (all ETFs; notebook filters to SPY)
├── outputs/
│   ├── 01_spy_close_price.png
│   ├── 02_daily_return_distribution.png
│   ├── 03_volume_distribution.png
│   ├── 04_up_vs_down_days.png
│   ├── 05_volume_vs_return.png
│   ├── spy_cleaned_analyzed.csv   # Cleaned, feature-added dataset
│   └── summary_report.txt         # Plain-text findings summary
└── README.md
```

## Tools & Libraries

- **Python** — pandas, NumPy, Matplotlib, Seaborn
- **Environment** — Google Colab / Jupyter Notebook

## How to Run

1. Clone the repo
2. Open `SPY_Day1_Pipeline.ipynb` in Google Colab or Jupyter
3. Run all cells top to bottom — outputs (charts, cleaned CSV, report) are written to `outputs/`

## About

Part of a personal portfolio of finance-focused data science projects. Feedback welcome!
