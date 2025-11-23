# 🌟 Portfolio Optimization Using Numerical Methods

A comprehensive **Python-based portfolio optimization project** demonstrating modern portfolio theory, numerical optimization, and Monte Carlo simulation. This project shows how mathematical and computational techniques can be applied to construct efficient investment portfolios using real-world stock data.



## 📊 Overview

This project explores:

- **Mean-Variance Optimization** (Markowitz)
- **Efficient Frontier construction**
- **Monte Carlo Simulation** for forecasting outcomes
- **Value at Risk (VaR)** and scenario-based risk analysis
- **Technical indicator integration** for deeper insights



## ✨ Features

### 🔹 Multi-Asset Portfolio
Analyzes a 5-asset portfolio:
**AMD, AMZN, CVX, NVDA, TSM**

### 🔹 Optimization
- Markowitz mean-variance model  
- Adjustable risk tolerance parameter **q**  
- Realistic constraints:  
  - No short-selling (`0 ≤ w ≤ 1`)  
  - Fully invested (`sum(w) = 1`)  


### 🔹 Interactive Visual Output
- Efficient frontier  
- Optimal portfolio weights  
- Monte Carlo simulation distribution  
- Weight changes across risk tolerance levels  



## 🛠️ Technologies Used

- **Python 3.x**
- **NumPy** — mathematical operations  
- **Pandas** — data manipulation  
- **Matplotlib / Seaborn** — visualization  
- **SciPy** — numerical optimization (`minimize`)



## 📈 Methodology

### 1️⃣ Data Collection
Historical data (Feb 2015 → Nov 2025) including:
- OHLC prices  
- Volume  
- Technical indicators  



### 2️⃣ Return & Risk Calculation

- **Daily Returns**: % change of closing prices  
- **Expected Return Vector (μ)**: mean daily return  
- **Covariance Matrix (Σ)**: captures cross-asset volatility relationships  



### 3️⃣ Portfolio Optimization

#### Objective Function
$
\[
\text{Cost}(w) = w^\top \Sigma w - q (w^\top r)
\]
$
Where:

| Symbol | Meaning |
|--------|---------|
| \( w \) | portfolio weights |
| \( \Sigma \) | covariance matrix |
| \( r \) | expected returns |
| \( q \) | risk tolerance |

#### Constraints
- Fully invested:  
  \[
  \sum w_i = 1
  \]
- No short-selling:  
  \[
  0 \le w_i \le 1
  \]



### 4️⃣ Monte Carlo Simulation

- **10,000 simulations**
- **252 trading days** (1-year horizon)
- Based on historical mean & covariance  
- Outputs:  
  - Final portfolio distribution  
  - Value at Risk (VaR 95%)  
  - Probability of loss  



### 5️⃣ Efficient Frontier
Risk tolerance **q** varied from **0 → 1000** to visualize optimal portfolios under different preferences.



## 🟦 Results

### 📌 Optimal Portfolio (q = 0.5)

| Stock | Weight |
|-------|--------|
| AMD | **17.99%** |
| AMZN | **26.32%** |
| CVX | **0.00%** |
| NVDA | **29.85%** |
| TSM | **25.84%** |

### 📌 Portfolio Metrics
- **Expected Return:** 0.182% (daily)  
- **Portfolio Std Dev:** 2.15% (daily)

### 💡 Insights
- **CVX** receives 0% due to poor risk-return profile  
- **NVDA** dominates due to strong returns  
- **AMZN + TSM** provide diversification  
- Overall risk significantly reduced vs. individual asset volatility  



## 📉 Visualizations Generated

- Efficient Frontier  
- Portfolio weight bar chart  
- Monte Carlo outcome distribution  
- Risk tolerance sensitivity plot  



## 🔍 Risk Analysis

- **Value at Risk (VaR 95%)**
- **Diversification benefits** clearly shown  
- **Scenario analysis** for stress-testing  



## 🎓 Concepts Demonstrated

- Markowitz Portfolio Theory  
- Constrained optimization  
- Monte Carlo simulation  
- Risk-return analysis  
- Numerical methods in finance  
- Data-driven portfolio construction  



