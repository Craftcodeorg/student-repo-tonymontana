# Module Title: Introduction to Quantitative Analysis

## Example 3: Implementing the Sharpe Ratio Formula in Python

### 1. Introduction
In this section, we will explore the significance of the Sharpe Ratio in finance and how it builds upon the key concepts discussed in Lecture 3: Introduction to Financial Metrics: ROI, Sharpe Ratio. The Sharpe Ratio is a vital financial metric that allows investors to assess the risk-adjusted return of an investment. By understanding this concept, aspiring Python developers can integrate it into their trading algorithms, enhancing their ability to make informed investment decisions.

### 2. Code Snippet
Below is a well-commented Python code snippet that demonstrates how to implement the Sharpe Ratio formula. This code is designed for a beginner-level programmer and includes error handling and best practices.

```python
def calculate_roi(net_profit, investment_cost):
    """
    Calculate Return on Investment (ROI).
    
    Parameters:
    net_profit (float): The profit made from the investment.
    investment_cost (float): The total cost of the investment.
    
    Returns:
    float: The ROI percentage.
    """
    if investment_cost <= 0:
        raise ValueError("Investment cost must be greater than zero.")
    return (net_profit / investment_cost) * 100

def calculate_sharpe_ratio(portfolio_return, risk_free_rate, std_dev):
    """
    Calculate the Sharpe Ratio.
    
    Parameters:
    portfolio_return (float): The return of the portfolio.
    risk_free_rate (float): The risk-free rate of return.
    std_dev (float): The standard deviation of the portfolio's excess return.
    
    Returns:
    float: The Sharpe Ratio.
    """
    if std_dev < 0:
        raise ValueError("Standard deviation must be non-negative.")
    return (portfolio_return - risk_free_rate) / std_dev

# Example values
try:
    roi = calculate_roi(200, 1000)
    sharpe_ratio = calculate_sharpe_ratio(0.10, 0.02, 0.05)
    
    print(f"ROI: {roi:.2f}%")
    print(f"Sharpe Ratio: {sharpe_ratio:.2f}")
except ValueError as e:
    print(f"Error: {e}")
```

### 3. Explanation
- **Function `calculate_roi`**: This function takes two parameters: `net_profit` and `investment_cost`. It first checks if the `investment_cost` is greater than zero to prevent division by zero errors. If valid, it calculates ROI using the formula provided in the lecture and returns it as a percentage.

- **Function `calculate_sharpe_ratio`**: This function calculates the Sharpe Ratio using three parameters: `portfolio_return`, `risk_free_rate`, and `std_dev`. It includes a check to ensure that the standard deviation is non-negative. If valid, it computes the Sharpe Ratio using its formula and returns the result.

- **Example Values**: The code then uses example values to demonstrate how to call these functions. It captures any potential `ValueError` exceptions that may arise from invalid input.

This code snippet effectively demonstrates how to calculate two important financial metrics, reinforcing the concepts learned in the lecture.

### 4. Application
In real-world finance, the Sharpe Ratio is commonly used by portfolio managers and individual investors to evaluate investment performance. For instance, an investor may compare two different portfolios: one with a high return but also high volatility and another with moderate returns but lower volatility. By calculating the Sharpe Ratio for both portfolios, the investor can determine which portfolio offers better risk-adjusted returns.

This application helps investors make informed decisions by highlighting not just the returns of an investment but also the risks associated with achieving those returns. As such, understanding and implementing the Sharpe Ratio can significantly enhance investment strategies and overall financial performance.

---

This structured content aligns with your learning objectives by providing practical coding experience while integrating essential financial concepts relevant to stock trading. By completing this module, you will be one step closer to achieving your goal of becoming a proficient Python Developer in finance.