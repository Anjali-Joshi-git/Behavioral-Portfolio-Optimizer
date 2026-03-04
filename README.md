# 📊 Behavioral Portfolio Optimizer

A quantitative finance project that integrates traditional portfolio optimization with behavioral finance principles to construct psychologically robust investment portfolios using real market data.

---

## 🚀 Project Overview

Traditional portfolio models assume investors are fully rational and risk is fully captured by variance. However, real-world investors exhibit loss aversion, asymmetric risk perception, and emotional reactions during market downturns.

This project extends classical portfolio optimization by incorporating behavioral utility inspired by Prospect Theory to account for investor psychology in asset allocation decisions.

---

## 🎯 Objectives

- Build a Traditional Mean-Variance Optimized Portfolio  
- Develop a Behavioral Portfolio Optimizer using asymmetric loss modeling  
- Compare risk-return characteristics of both approaches  
- Evaluate downside protection and emotional risk reduction  

---

## 📂 Dataset

Historical equity data was programmatically fetched using the `yfinance` API.

- Selected large-cap stocks from NIFTY 50
- Daily historical prices (2019–2024)
- NIFTY 50 Index used for benchmarking
- 252 trading days assumption for annualization

The project dynamically retrieves live market data — no static CSV files required.

---

## 🛠️ Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- SciPy (SLSQP Optimization)  
- yfinance API  

---

## 📊 Exploratory Data Analysis (EDA)

Performed the following analyses:

- Price trend visualization  
- Daily return distribution  
- Correlation heatmap  
- Volatility comparison  
- Cumulative growth plots  
- Portfolio vs Index performance  

### Key Insights

- Volatility clustering during stress periods  
- High cross-sector correlation during downturns  
- Fat-tailed return distributions  

These findings justify incorporating behavioral loss modeling.

---

## ⚙️ Methodology

### 1️⃣ Data Preparation

- Fetch stock price data  
- Compute daily log returns  
- Annualize mean returns and covariance matrix  

---

### 2️⃣ Traditional Optimization (Mean-Variance)

Objective:
Minimize portfolio variance subject to:

- Sum of weights = 1  
- Long-only constraint (0 ≤ weights ≤ 1)  

Efficient Frontier generated via Monte Carlo simulation.

Metrics Evaluated:

- Expected Return  
- Volatility  
- Sharpe Ratio  

---

### 3️⃣ Behavioral Optimization

Instead of maximizing Sharpe Ratio, this model maximizes Behavioral Utility.

Prospect Theory Inspired Value Function:

For gains:
v(x) = x^α

For losses:
v(x) = -λ(-x)^β

Where:
- λ = 2.25 (loss aversion coefficient)  
- α = β = 0.88  

Objective:
Maximize expected behavioral utility relative to a reference return.

Optimization solved using constrained nonlinear programming (SLSQP).

---

## 📈 Results Comparison

| Metric | Traditional Portfolio | Behavioral Portfolio |
|--------|----------------------|----------------------|
| Expected Return | Slightly Higher | Slightly Lower |
| Volatility | Higher | Lower |
| Downside Sensitivity | Not Explicit | Explicitly Penalized |
| Emotional Stability | Moderate | Improved |

### Core Insight

The Behavioral Portfolio reduces exposure to extreme downside risk and produces more psychologically sustainable allocations during market stress.

---

## 🧠 Key Takeaways

- Risk is not purely statistical — it is psychological  
- Variance alone does not capture investor discomfort  
- Behavioral optimization creates more stable allocations  
- Finance + Behavioral Economics improves real-world applicability  

---

## 🏆 Conclusion

This project demonstrates how quantitative finance models can be enhanced by incorporating behavioral economics.

By integrating asymmetric loss modeling into optimization, portfolio construction becomes more aligned with real-world investor behavior rather than assuming perfect rationality.

This approach is valuable for:

- Robo-advisory systems  
- Wealth management platforms  
- FinTech portfolio engines  
- Behavioral investment research  

---

## 🔮 Future Improvements

- Sortino Ratio based optimization  
- CVaR (Conditional Value at Risk) comparison  
- Rolling window backtesting  
- Market regime detection (Bull/Bear)  
- Reinforcement Learning asset allocation  

---

## 👩‍💻 Author

**Anjali Joshi**  
Data Science | Quantitative Finance | Behavioral Modeling  

---

⭐ If you found this project useful, consider giving it a star.
