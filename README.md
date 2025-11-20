# FX Trend Strategy Using Exponential Smoothing  
### A Fully Reproducible Quantitative Research Project by Cheng Wu

This repository contains a complete, end-to-end quantitative analysis of the USD/CAD FX pair using **dual exponential smoothing (ES)** trend filters.  
The project studies whether simple parametric smoothing rules—paired with hyperparameter tuning, buffer thresholds, and deceleration-based exits—can generate meaningful and testable trading signals.

The project is implemented fully in **Python**, documented in a polished **LaTeX research report**, and structured to be **fully reproducible**.

---

## 🚀 Project Overview

FX markets often exhibit medium-term trend persistence.  
This project builds a **trend-following trading strategy** using:

- A fast exponential smoothing filter \( ES_\alpha \)
- A slow exponential smoothing filter \( ES_\beta \)
- Signal = crossovers between them

I answer five research questions:

1. **Is there an optimal combination of (α, β)?**  
2. **Should long and short trades use different smoothing parameters?**  
3. **What is the strategy’s actual accuracy (“probability of being correct”)?**  
4. **Should trades be closed when the slow trend decelerates?**  
5. **Should entries require a minimum buffer (x) between ES(α) and ES(β)?**

---

## 🎯 Key Findings

- Optimal smoothing parameters: **α = 0.20, β = 0.60**
- Long-only and short-only portfolios **prefer the same (α, β)**  
  → trend time horizon is symmetric, even though returns are not
- Trade-level accuracy is **~73%**, despite ~50% daily hit rate  
- Buffer thresholds **decrease Sharpe** and reduce opportunities  
- Deceleration-based exits **destroy performance** due to over-trading
- The **simplest ES crossover** performs best on USD/CAD (2003–2025)

---

## 🧠 Techniques and Methods Used

- Time-series filtering & signal engineering  
- Exponential smoothing \( ES_\alpha, ES_\beta \)  
- Full grid search over smoothing parameters  
- Backtesting (close-to-close returns)  
- Risk & performance analytics:
  - Sharpe ratio  
  - Daily & trade-level hit rate  
  - Volatility  
  - Trade counting  
- Sensitivity testing:
  - Buffer \( x \) thresholds  
  - Deceleration thresholds \( c \)  
- Matplotlib charting  
- Reproducible research workflow  
- LaTeX scientific reporting  

---

## 📁 Repository Structure

Exponential-Smoothing-Trend-Strategy/
│
├── FX_Trend_Strategy_ES_Crossover.ipynb # Main analysis & backtest
├── FX_Trend_Strategy_Report.pdf # Full LaTeX research report
│
├── data/
│ └── USD_CAD_Daily_OHLC_2003_2025.csv # Input data (cleaned)
│
├── figures/ # Auto-generated figures
│ ├── Sharpe_Heatmap.png
│ ├── Buffer_vs_Sharpe.png
│ ├── Buffer_vs_Trades.png
│ ├── Decel_vs_Sharpe.png
│ ├── Decel_vs_Trades.png
│ └── ES_Crossover_Example.png
│
└── README.md


---

## 📊 Example Figures (Screenshots)

*(Upload images into `/figures` then link them here if desired)*

### 🔸 Sharpe Ratio Heatmap  
Shows the optimal region at **(0.20, 0.60)**.

### 🔸 Buffer Effect  
Sharpe ratio declines as buffer x increases.

### 🔸 Deceleration Effect  
Deceleration increases turnover and destroys performance.

### 🔸 Baseline vs Optimized Strategy  
Optimized parameters more than **double** total return.

---


---

## 📊 Example Figures (Screenshots)

*(Upload images into `/figures` then link them here if desired)*

### 🔸 Sharpe Ratio Heatmap  
Shows the optimal region at **(0.20, 0.60)**.

### 🔸 Buffer Effect  
Sharpe ratio declines as buffer x increases.

### 🔸 Deceleration Effect  
Deceleration increases turnover and destroys performance.

### 🔸 Baseline vs Optimized Strategy  
Optimized parameters more than **double** total return.

---


## 📊 Example Figures (Screenshots)

*(Upload images into `/figures` then link them here if desired)*

### 🔸 Sharpe Ratio Heatmap  
Shows the optimal region at **(0.20, 0.60)**.

### 🔸 Buffer Effect  
Sharpe ratio declines as buffer x increases.

### 🔸 Deceleration Effect  
Deceleration increases turnover and destroys performance.

### 🔸 Baseline vs Optimized Strategy  
Optimized parameters more than **double** total return.

---

## 🔧 How to Run This Project

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>























