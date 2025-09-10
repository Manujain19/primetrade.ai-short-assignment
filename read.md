# Trader Behavior Insights – Primetrade.ai Short Assignment

## Overview
This project explores the relationship between **trader performance** on the Hyperliquid exchange and the **Bitcoin market sentiment** (Fear/Greed Index).  
The analysis was completed as part of the **Primetrade.ai short assignment** and carried out in Google Colab (`Primetrade_ai_short_assignment.ipynb`).  

By combining execution-level trading data with sentiment labels, the goal was to uncover hidden patterns that explain how market mood affects profitability, risk-taking, and trader behavior.

---

## Objectives
- Merge Hyperliquid trading data with daily Fear/Greed sentiment.  
- Create **per-trade** and **per-trader-day** aggregated metrics (PnL, leverage, win rate, trade frequency).  
- Perform **exploratory data analysis (EDA)** with meaningful visualizations.  
- Run **statistical tests** to evaluate differences in performance across sentiment states.  
- Provide **actionable insights** and recommendations for trading strategies.  

---

## Data Sources
1. **Hyperliquid Historical Trader Data**  
   - Columns: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `start position`, `closedPnL`, `leverage`, etc.  

2. **Fear & Greed Index**  
   - Columns: `date`, `classification` (Fear / Greed).  

---

## Methodology
1. **Data Cleaning & Preparation**
   - Parsed timestamps, standardized columns, and mapped trades to sentiment dates.  

2. **Feature Engineering**
   - Derived metrics such as `total_pnl`, `win_rate`, `avg_leverage`, and `avg_size`.  

3. **Aggregation**
   - Built a **trader-daily dataset** (`cleaned_data/trader_daily_agg.csv`) for analysis.  

4. **Exploratory Data Analysis**
   - Visualized PnL distributions, leverage vs performance, and daily sentiment overlays.  

5. **Statistical Testing**
   - Compared Fear vs Greed performance with Mann–Whitney U tests and regressions.  

---

## Key Insights
- Traders generally performed **better on Greed days** than on Fear days.  
- **High leverage magnified losses** during Fear conditions.  
- Certain traders showed **consistent profitability** regardless of sentiment, suggesting robust strategies.  
- Trading activity (volume & frequency) was higher in Greed conditions.  

---

## Deliverables
- **Notebook:** `Primetrade_ai_short_assignment.ipynb` (Google Colab analysis)  
- **Report:** [`report.md`](./report.md) or PDF version summarizing methodology & findings  
- **Slides:** [`slides.pdf`](./slides.pdf) for a concise presentation of results  
- **Aggregated Data:** [`cleaned_data/trader_daily_agg.csv`](./cleaned_data/trader_daily_agg.csv)  

---

## How to Run
1. Open [`Primetrade_ai_short_assignment.ipynb`](./Primetrade_ai_short_assignment.ipynb) in **Google Colab**.  
2. Mount Google Drive or upload the raw datasets (Hyperliquid trades + Fear/Greed index).  
3. Run cells in order to reproduce cleaning, analysis, and visualizations.  
4. View outputs (plots, tables, insights).  

---

## Next Steps
- Add BTC price & volatility data as controls.  
- Develop predictive models to forecast profitability from sentiment.  
- Deploy dashboards for real-time monitoring of trader behavior vs sentiment.  

---

## Author
Prepared by **Vishesh Jain**  
Date: *August 18, 2025*
