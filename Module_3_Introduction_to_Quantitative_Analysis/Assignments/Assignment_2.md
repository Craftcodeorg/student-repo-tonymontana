### Assignment: Analyzing Investment Strategies Using Simulated Data

#### Problem Statement:
Create a Python function that analyzes the risk associated with different investment strategies by simulating stock price data. The function should calculate and return the mean, median, variance, and standard deviation of the simulated stock prices. This analysis will help you understand how different strategies might perform under various market conditions, reflecting the concepts taught in the lecture on key statistical concepts.

#### Starter Code:
```python
import numpy as np

def analyze_investment_strategy(stock_prices):
    """
    Analyzes the risk associated with an investment strategy based on stock prices.
    
    Parameters:
    stock_prices (list): A list of simulated stock prices.
    
    Returns:
    dict: A dictionary containing mean, median, variance, and standard deviation.
    """
    # Step 1: Calculate mean
    mean_price = np.mean(stock_prices)
    
    # Step 2: Calculate median
    median_price = np.median(stock_prices)
    
    # Step 3: Calculate variance
    variance_price = np.var(stock_prices)
    
    # Step 4: Calculate standard deviation
    std_dev_price = np.std(stock_prices)
    
    # Return results
    return {
        'Mean': mean_price,
        'Median': median_price,
        'Variance': variance_price,
        'Standard Deviation': std_dev_price
    }

# Test the function with sample simulated data
simulated_prices = [10, 12, 14, 16, 18, 20, 22]
results = analyze_investment_strategy(simulated_prices)
print(f"Investment Strategy Analysis: {results}")
```

#### Detailed Instructions:
1. **Step 1: Modify the function to accept user input for simulated stock prices.** 
   - Change the `stock_prices` parameter to allow the user to input a list of prices. You can use `input()` to gather this data from the user in a comma-separated format.
   - Example: `user_input = input("Enter simulated stock prices separated by commas: ")`

2. **Step 2: Enhance the output to provide more detailed feedback.**
   - Format the output to display each statistic with a descriptive message. For example, instead of just returning the values in a dictionary, print them out in a user-friendly format.
   - Example:
     ```python
     print(f"Mean Price: {mean_price}")
     print(f"Median Price: {median_price}")
     print(f"Variance: {variance_price}")
     print(f"Standard Deviation: {std_dev_price}")
     ```

3. **Step 3: Add error handling to ensure valid input.**
   - Implement try-except blocks to handle any potential errors that may arise from invalid input (e.g., non-numeric values).
   - Example:
     ```python
     try:
         stock_prices = [float(price) for price in user_input.split(',')]
     except ValueError:
         print("Please enter valid numeric values.")
     ```

4. **Step 4: Document your code properly.**
   - Ensure that each function and significant block of code has comments explaining what it does and why.

#### Criteria for Success and Evaluation:
- **Accuracy**: The function should correctly calculate and return the mean, median, variance, and standard deviation of the provided stock prices.
- **Code Quality**: The code should be clean, well-structured, and adhere to Python best practices (e.g., proper naming conventions, use of functions).
- **User Experience**: The output should be formatted clearly and provide meaningful feedback to the user.
- **Error Handling**: The program should handle invalid inputs gracefully without crashing.

By completing this assignment, you will not only reinforce your understanding of statistical concepts but also gain practical experience in coding relevant to finance, supporting your goal of becoming a Python Developer focused on stock trading.