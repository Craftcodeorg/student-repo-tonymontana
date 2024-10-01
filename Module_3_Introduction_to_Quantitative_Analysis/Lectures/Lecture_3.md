# Lecture 3: Introduction to Financial Metrics: ROI, Sharpe Ratio

## 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Understand and define key financial metrics: Return on Investment (ROI) and Sharpe Ratio.
- Calculate ROI and Sharpe Ratio using simple formulas.
- Recognize the significance of these metrics in evaluating investment performance, especially in stock trading.

## 2. Introduction:
In the world of finance and stock trading, quantitative analysis plays a crucial role in making informed decisions. Understanding financial metrics such as ROI and the Sharpe Ratio helps traders assess the profitability and risk of their investments. For aspiring Python Developers focusing on stock trading, these metrics are essential tools that can be integrated into trading algorithms and investment strategies. This lecture aims to equip you with the foundational knowledge of these metrics, enabling you to analyze stocks effectively and enhance your trading strategies.

## 3. Core Concepts:

### A. Return on Investment (ROI)
- **Definition**: ROI is a financial metric used to evaluate the efficiency of an investment. It measures the return relative to the investment cost.
- **Formula**: 
  \[
  \text{ROI} = \frac{\text{Net Profit}}{\text{Cost of Investment}} \times 100
  \]
- **Example**: If you invest $1,000 in a stock and sell it later for $1,200, your net profit is $200. Thus, 
  \[
  \text{ROI} = \frac{200}{1000} \times 100 = 20\%
  \]

### B. Sharpe Ratio
- **Definition**: The Sharpe Ratio measures the performance of an investment compared to a risk-free asset, considering its risk. A higher Sharpe Ratio indicates better risk-adjusted returns.
- **Formula**:
  \[
  \text{Sharpe Ratio} = \frac{R_p - R_f}{\sigma_p}
  \]
  where \( R_p \) is the return of the portfolio, \( R_f \) is the risk-free rate, and \( \sigma_p \) is the standard deviation of the portfolio's excess return.
- **Example**: If your portfolio has an average return of 10%, the risk-free rate is 2%, and the standard deviation of your portfolio's returns is 5%, then:
  \[
  \text{Sharpe Ratio} = \frac{10\% - 2\%}{5\%} = 1.6
  \]

## 4. Practical Application:
### Real-World Example:
Consider a hedge fund that uses both ROI and Sharpe Ratio to assess its performance:
- The fund calculates an ROI of 25% on its investments over a year.
- It also computes a Sharpe Ratio of 1.5, indicating that its returns are significantly higher than a risk-free investment when adjusted for volatility.

### Code Snippet:
Here’s a simple Python code snippet to calculate ROI and Sharpe Ratio:

```python
def calculate_roi(net_profit, investment_cost):
    return (net_profit / investment_cost) * 100

def calculate_sharpe_ratio(portfolio_return, risk_free_rate, std_dev):
    return (portfolio_return - risk_free_rate) / std_dev

# Example values
roi = calculate_roi(200, 1000)
sharpe_ratio = calculate_sharpe_ratio(0.10, 0.02, 0.05)

print(f"ROI: {roi}%")
print(f"Sharpe Ratio: {sharpe_ratio}")
```

## 5. Summary:
In this lecture, we explored two critical financial metrics: ROI and Sharpe Ratio. We learned how to calculate each metric and understood their significance in evaluating investment performance. These concepts are vital for making informed trading decisions and optimizing investment strategies as you pursue your goal of becoming a proficient Python Developer in stock trading.

## 6. Next Steps:
In our next lecture, we will delve into more advanced financial metrics and how they can be implemented in Python for real-time stock analysis. To prepare, consider reviewing basic Python functions and familiarize yourself with libraries such as NumPy and Pandas, which will be useful for data manipulation and calculations in financial analysis.