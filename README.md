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

- **Python 3.10**
- **NumPy** — mathematical operations  
- **Pandas** — data manipulation  
- **Matplotlib / Seaborn** — visualization  
- **SciPy** — numerical optimization (`minimize`)



## 📈 Methodology

### 1️⃣ Data Collection
Historical data (Feb 2015 -> Nov 2025) including:
- The data originally retrieved from Yahoo Finance


### 2️⃣ Return & Risk Calculation

- **Daily Returns**: % change of closing prices  
- **Expected Return Vector (μ)**: mean daily return  
- **Covariance Matrix (Σ)**: captures cross-asset volatility relationships  



### 3️⃣ Portfolio Optimization

#### Objective Function
The cost function is:

$$
\text{Cost}(w) = w^\top \Sigma w - q (w^\top r)
$$

Where:

| Symbol | Meaning |
|--------|---------|
| $w$ | portfolio weights |
| $\Sigma$ | covariance matrix |
| $r$ | expected returns |
| $q$ | risk tolerance |


#### Constraints
- Fully invested:

$$
\sum_i w_i = 1
$$

- No short-selling:

$$
0 \le w_i \le 1
$$




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



# 🟦 Portfolio Optimization Results

## 📌 Optimal Portfolio (Best Trade-Off at q = 1.0)

This portfolio delivers the **highest Sharpe Ratio (0.0853)** among all optimized selections, offering the best balance between return and volatility.

### **Portfolio Weights**

| Stock | Weight |
|-------|--------|
| **AMD** | **28.99%** |
| **AMZN** | **13.45%** |
| **CVX** | **0.00%** |
| **NVDA** | **43.53%** |
| **TSM** | **14.03%** |



## 📌 Portfolio Metrics (q = 1.0)

| Metric | Value |
|--------|--------|
| **Expected Return (daily)** | 0.0021 |
| **Portfolio Std Dev (daily)** | 0.0251 |
| **Annualized Sharpe Ratio (rf = 0)** | **0.0853** |



## 💡 Key Insights

### **1. NVDA Dominance**
- NVDA holds the highest allocation (**43.53%**).
- This is driven by its strong historical returns and attractive risk–reward characteristics.

### **2. CVX Exclusion**
- CVX receives **0% weight**.
- Its risk-return profile contributes less to improving portfolio efficiency compared with higher-growth assets.

### **3. Critical Trade-Off Point**
- The transition from the equal-weight-like portfolios (**q = 0.7**) to **q = 1.0** shows the **largest improvement in Sharpe Ratio**.
- For q > 1.0, additional concentration **adds risk without meaningful return gains**, demonstrating diminishing marginal benefit.



## 📉 Visualizations Generated

- **Efficient Frontier Plot**  
- **Portfolio Weight Bar Chart**  
- **Monte Carlo Outcome Distribution**  
- **Risk Tolerance Sensitivity Curve**  

These visualizations help illustrate the trade-offs between risk, return, and portfolio concentration.



## 🔍 Risk Analysis (1-Year Monte Carlo: 10,000 Simulations)

### **Key Risk Metrics**

| Metric | Result | Interpretation |
|--------|--------|----------------|
| **Mean Final Value (Growth Factor)** | **1.701** | On average, the portfolio grows to **170.1%** of initial value after 1 year. |
| **Value at Risk (VaR 95%)** | **0.826** | 5% chance portfolio falls to **82.6%** of initial value or lower → potential loss ≥ **17.4%**. |

### **Observations**
- The portfolio shows **clear diversification benefits**, reducing downside risk relative to single-asset exposure.
- Scenario-based stress testing further confirms stability under varying market conditions.


## 📝 Conclusion

The optimized portfolio at **q = 1.0** represents the **best balance of risk and reward**, providing:

- Moderate risk  
- Improved expected return  
- Highest risk-adjusted efficiency  
- Strong diversification  
- Controlled downside exposure  

This makes it a compelling choice for investors seeking growth while managing volatility effectively.


## 🎓 Concepts Demonstrated

- Markowitz Portfolio Theory  
- Constrained optimization  
- Monte Carlo simulation  
- Risk-return analysis  
- Numerical methods in finance  
- Data-driven portfolio construction  



