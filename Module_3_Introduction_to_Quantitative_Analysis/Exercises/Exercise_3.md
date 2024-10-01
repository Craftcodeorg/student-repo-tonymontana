### Module Title: Introduction to Quantitative Analysis

### Exercise Requirements

#### 1. Problem Statement
You are tasked with simulating the stock returns of a fictional tech company, "Tech Innovations Inc.", over a period of 30 days. Your goal is to assess the risk of investing in this stock by calculating the standard deviation of the simulated returns and then using this information to compute the Sharpe Ratio. Assume the risk-free rate is 2%. 

Using the concepts discussed in Lecture 3, you will:
- Simulate daily returns using a normal distribution.
- Calculate the average return and standard deviation of the simulated returns.
- Compute the Sharpe Ratio based on your findings.

#### 2. Fill-in-the-Blank Starter Code
Below is a starter code template that you will complete. Make sure to fill in the blanks with appropriate calculations and variables as discussed in the lecture.

```python
import numpy as np

# Function to simulate stock returns
def simulate_stock_returns(mean_return, std_dev, days):
    # Generate random returns based on a normal distribution
    returns = np.random.normal(loc=______, scale=______, size=days)
    return returns

# Function to calculate average return and standard deviation
def calculate_metrics(returns):
    average_return = np.mean(returns)
    std_dev = np.std(returns)
    return average_return, std_dev

# Function to calculate Sharpe Ratio
def calculate_sharpe_ratio(average_return, risk_free_rate, std_dev):
    sharpe_ratio = (average_return - ______) / ______
    return sharpe_ratio

# Parameters
mean_return = 0.01  # Assume a daily mean return of 1%
std_dev = 0.02      # Assume a daily standard deviation of 2%
days = 30           # Simulate for 30 days
risk_free_rate = 0.02  # Risk-free rate of 2%

# Simulate stock returns
simulated_returns = simulate_stock_returns(mean_return, std_dev, days)

# Calculate metrics
average_return, calculated_std_dev = calculate_metrics(simulated_returns)

# Calculate Sharpe Ratio
sharpe_ratio = calculate_sharpe_ratio(average_return, risk_free_rate, calculated_std_dev)

# Output results
print(f"Average Return: {average_return:.4f}")
print(f"Standard Deviation: {calculated_std_dev:.4f}")
print(f"Sharpe Ratio: {sharpe_ratio:.4f}")
```

#### 3. Hints
- **Hint for simulating returns**: Remember that when using `np.random.normal`, you need to provide the mean and standard deviation as parameters.
- **Hint for calculating metrics**: Use `np.mean()` and `np.std()` to find the average and standard deviation of your simulated returns.
- **Hint for Sharpe Ratio**: Ensure you are correctly subtracting the risk-free rate from your average return before dividing by the standard deviation.

#### 4. Expected Outcome
By completing this exercise, you should be able to:
- Simulate random stock returns using Python.
- Calculate the average return and standard deviation of those returns.
- Compute the Sharpe Ratio to assess the risk-adjusted return of your simulated stock investment.

Your final solution should demonstrate an understanding of how these financial metrics apply to real-world scenarios in finance, and it should be well-commented to explain your reasoning behind each step.

### Integration
This exercise is structured to be easily integrated into your learning platform. The clear headings and sections will help guide students through the exercise while reinforcing their understanding of quantitative analysis in stock trading.