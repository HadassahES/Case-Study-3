# Portfolio Analysis and Optimization Project
## Hadassah Ely Sharon 21356994
### Assessment 3 for Fintech Applications
## Project Overview

This project is about analyzing and optimizing a portfolio of stocks using historical data, the Fama-French 3-factor model, and various financial metrics. It involves calculating and plotting the efficient frontier, creating portfolios based on different criteria, and evaluating a constrained portfolio.

The project is organized into sections, each focused on a different aspect of portfolio analysis.

## Files

- `main.ipynb`: Jupyter Notebook with all the code, analysis, and results.
- `Fama French Data.xlsx`: Excel file with Fama-French data including market returns, size premium (SMB), value premium (HML), and risk-free rate.

## Sections and Explanations

### A. Data Collection and Preprocessing

- **Goal**: Download stock price data, resample it to monthly frequency, and calculate monthly returns.
- **Steps**:
  - Download stock data using `yfinance`.
  - Resample to monthly data and calculate monthly returns.
  - Combine returns into one DataFrame with each column as a different stock.

### B. Correlation Matrix

- **Goal**: Compute and visualize the correlation between stocks.
- **Steps**:
  - Calculate the correlation matrix of monthly returns.
  - Plot a heatmap to see the relationships between different assets.
- **Why it Matters**: Lower correlation between assets is usually better for diversification.

### C. Cumulative Monthly Returns

- **Goal**: Plot the cumulative monthly returns for each stock.
- **Steps**:
  - Calculate cumulative returns.
  - Plot each stock’s cumulative return over time to see its performance.

### D. Efficient Frontier and Portfolio Optimization

- **Goal**: Calculate the efficient frontier, minimum risk portfolio, tangency portfolio, and Monte Carlo portfolios.
- **Steps**:
  - Define functions to calculate portfolio returns and risk.
  - Use optimization to find portfolios with the best return-to-risk ratios.
  - Plot the efficient frontier, showing the risk-return profiles of different portfolios.

### E. Efficient Portfolios' Weights Table

- **Goal**: Create a table of risk, return, and weights of efficient portfolios.
- **Steps**:
  - Store efficient portfolios’ risk, return, and weights in a DataFrame.
  - Display the DataFrame.

### F. Optimal Portfolios Summary

- **Goal**: Find and display the portfolios with:
  - The highest Sharpe ratio,
  - The lowest risk,
  - The highest expected return.
- **Output**: A table summarizing the weights for each of these portfolios.

### G. Tangency Portfolio vs. S&P 500

- **Goal**: Compare the cumulative returns of the tangency portfolio to the S&P 500.
- **Steps**:
  - Download S&P 500 data.
  - Calculate and plot cumulative returns for the tangency portfolio and S&P 500.

### H. Constrained Tangency Portfolio

- **Goal**: Find the tangency portfolio with constraints:
  - No short selling,
  - Max of 40% in any stock,
  - Min of 10% in any stock.
- **Output**: Plot showing cumulative returns of the constrained portfolio vs. S&P 500.

### I. Risk and Return Metrics

- **Goal**: Calculate risk and return metrics for the constrained portfolio:
  - **Value-at-Risk (VaR)**: Risk of loss over a specific time.
  - **Maximum Drawdown**: Largest peak-to-trough decline.
  - **Annualized Return and Volatility**: Standardized performance metrics.
  - **Active Return**: Extra return over the S&P 500.

### J. Performance Ratios

- **Goal**: Calculate performance metrics for evaluating portfolio performance:
  - **Jensen's Alpha**: Extra return above expected based on risk.
  - **Treynor's Ratio**: Return per unit of market risk.
  - **Information Ratio**: Active return divided by tracking error.
  - **Appraisal Ratio**: Alpha relative to idiosyncratic risk.

### K. Fama-French 3-Factor Model

- **Goal**: Use the Fama-French model to understand factor exposure for the constrained portfolio.
- **Steps**:
  - Align portfolio returns with Fama-French data.
  - Run a regression to see how the portfolio returns relate to Fama-French factors.
  - Get the factor loadings for market, size, and value premiums.

## How to Run

1. Install required libraries (`pandas`, `numpy`, `yfinance`, `scipy`, `matplotlib`, `seaborn`, and `statsmodels`).
2. Run each cell in the Jupyter Notebook (`main.ipynb`) in order.
3. Review the output plots and tables to interpret the results.

## Key Points

- **Date Overlap**: Ensure stock and Fama-French data dates overlap, or some calculations may fail.
- **Data Frequency**: Data is monthly to match Fama-French factors.
- **Portfolio Constraints**: Portfolio constraints can affect the best achievable Sharpe ratio.
- **Limitations**: This project assumes returns follow a normal distribution, which might not be true for future performance.
