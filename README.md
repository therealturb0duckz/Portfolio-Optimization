# Portfolio Optimization Using Numerical Methods
A comprehensive Python-based portfolio optimization project that applies mathematical and computational techniques to construct efficient investment portfolios. This project demonstrates the practical application of optimization algorithms, Monte Carlo simulation, and modern portfolio theory to real-world stock data.
## 📊 Overview
This project explores portfolio optimization through:

Mean-Variance Optimization using constrained optimization
Efficient Frontier visualization showing risk-return tradeoffs
Monte Carlo Simulation for portfolio performance forecasting
Risk Analysis including Value at Risk (VaR) calculations

## 🎯 Features

Multi-Asset Portfolio Analysis: Analyzes 5 major stocks (AMD, AMZN, CVX, NVDA, TSM)
Risk-Return Optimization: Implements Markowitz portfolio theory with customizable risk tolerance
Technical Indicators: Incorporates momentum, trend, and volatility indicators
Interactive Visualizations: Efficient frontier, weight distributions, and simulation results
No Short-Selling Constraints: Realistic portfolio constraints (weights between 0 and 1)

## 🛠️ Technologies Used

Python 3.x
NumPy: Numerical computations and linear algebra
Pandas: Data manipulation and analysis
Matplotlib/Seaborn: Data visualization
SciPy: Optimization algorithms (scipy.optimize.minimize)


## 📈 Methodology
1. Data Collection
Historical stock data spanning from February 2015 to November 2025 (2,701+ trading days) includes:

Price data (Open, High, Low, Close, Volume)
Technical indicators (RSI, MACD, Bollinger Bands, EMA, ATR)

2. Return & Risk Calculation

Daily Returns: Computed as percentage changes in closing prices
Expected Returns (μ): Mean of historical daily returns
Risk (Σ): Covariance matrix capturing correlations between assets

3. Portfolio Optimization
The optimization minimizes the cost function:
Cost(w) = w^T Σ w - q(w^T r)
Where:

w = portfolio weights
Σ = covariance matrix
r = expected returns vector
q = risk tolerance parameter

Constraints:

Sum of weights = 1 (fully invested)
No short selling: 0 ≤ w_i ≤ 1

4. Monte Carlo Simulation

Simulates 10,000 portfolio scenarios over 252 trading days (1 year)
Uses multivariate normal distribution based on historical statistics
Calculates Value at Risk (VaR) at 95% confidence level

5. Efficient Frontier
Visualizes optimal portfolios across different risk-return preferences by varying the risk tolerance parameter q from 0 to 1000.
📊 Key Results
Optimal Portfolio Allocation (q=0.5)
StockWeight AMD17.99%AMZN26.32%CVX0.00%NVDA29.85%TSM25.84%
Portfolio Metrics:

Expected Return: 0.182% (daily)
Portfolio Risk (Std): 2.15%

## Key Insights

CVX receives zero allocation due to lower returns and suboptimal risk-return profile
NVDA receives highest allocation, balancing high returns with acceptable risk
AMZN provides diversification benefits with moderate risk
Portfolio risk is significantly lower than individual stock volatilities due to diversification

## 📉 Visualizations
The project generates several key visualizations:

Efficient Frontier: Shows optimal risk-return combinations
Portfolio Weight Distribution: Bar chart of optimal allocations
Monte Carlo Simulation Histogram: Distribution of 1-year portfolio outcomes
Risk Tolerance Analysis: How weights change with different q values

## 🔍 Risk Analysis

Value at Risk (VaR): Quantifies potential losses at 5% confidence level
Diversification Benefits: Demonstrates risk reduction through optimal asset combination
Scenario Analysis: Explores portfolio behavior under various market conditions

## 🎓 Concepts Demonstrated

Modern Portfolio Theory (Markowitz)
Constrained optimization
Statistical simulation (Monte Carlo)
Risk-return tradeoff analysis
Numerical methods in finance
Data-driven investment strategies



⭐ If you found this project helpful, please consider giving it a star!
