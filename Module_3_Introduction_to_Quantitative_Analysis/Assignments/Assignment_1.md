### Assignment: Create a Financial Model to Evaluate Potential Investments

#### Problem Statement:
Using the concepts of quantitative analysis discussed in the lecture, your task is to create a financial model that evaluates potential investments based on historical stock data. Specifically, you will analyze the historical prices of NVIDIA's stock and determine the average price over a specified period. Additionally, you will identify days where the stock price exceeded the average price by more than 5%. This assignment will help you apply descriptive statistics and reinforce your understanding of risk assessment in stock trading.

#### Starter Code:
Below is a basic code framework that you will build upon. It includes comments to guide you on where to implement your solutions.

```python
import pandas as pd

# Starter code for analyzing NVIDIA stock prices
def analyze_stock_prices(stock_data):
    # Step 1: Calculate the average stock price
    avg_price = stock_data['Price'].mean()
    
    # Step 2: Identify days where the price exceeded the average by more than 5%
    high_price_days = stock_data[stock_data['Price'] > avg_price * 1.05]
    
    # Return results (students will need to format the output)
    return avg_price, high_price_days

# Sample data: Stock prices for NVIDIA over a week
data = {
    'Day': ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'],
    'Price': [150, 155, 152, 158, 160]
}
df = pd.DataFrame(data)

# Test the function with sample data
average_price, high_days = analyze_stock_prices(df)
print(f"The average stock price for NVIDIA this week is: ${average_price:.2f}")
print("Days where the stock price exceeded the average by more than 5%:")
print(high_days)
```

#### Detailed Instructions:
1. **Step 1**: Modify the function to return not only the average price but also a list of days where the stock price exceeded the average by more than 5%. 
   - Use the condition `stock_data['Price'] > avg_price * 1.05` to filter for these days.

2. **Step 2**: Enhance the output to provide more detailed feedback to the user. 
   - Format the output to include both the average price and a clear list of days when the stock price was significantly higher than average.
   - You can use `high_price_days['Day'].tolist()` to get a list of day names.

3. **Step 3**: Add error handling to ensure that if the input DataFrame is empty or does not contain the necessary columns, a meaningful message is returned.

4. **Step 4**: Document your code with comments explaining each part of your logic. This will help you and others understand your thought process.

#### Criteria for Success and Evaluation:
- **Success Criteria**:
  - The function correctly calculates the average stock price and identifies days where the price exceeded the average by more than 5%.
  - The code is clean, well-documented, and follows best practices.
  - The output is formatted in a clear and user-friendly manner, making it easy to read and understand.

- **Evaluation Rubric**:
  - **Functionality (50 points)**: The model correctly computes and returns both the average price and high price days.
  - **Code Quality (30 points)**: Code is well-structured, easy to read, and follows Python conventions.
  - **Documentation (20 points)**: Clear comments and documentation are provided throughout the code.

This assignment will not only reinforce your understanding of quantitative analysis but also help you build practical coding skills relevant to stock trading in Python. Good luck!