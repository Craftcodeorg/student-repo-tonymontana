### Module Title: Introduction to Python Programming

---

### Example 1: Basic Variable Assignment

#### 1. Introduction
In the context of the lecture titled **"Overview of Python and its Applications in Finance,"** understanding basic variable assignment is crucial as it lays the groundwork for more complex programming concepts. Variables serve as containers for storing data values, which can be manipulated in various ways to analyze financial data, create algorithms, and develop trading strategies. Mastering variable assignment allows you to effectively manage and utilize data in financial applications, making it a vital skill for aspiring Python developers in the finance sector.

#### 2. Code Snippet
```python
# Example of Basic Variable Assignment in Python

# Assigning values to variables
stock_name = "NVIDIA"  # String variable to hold the name of the stock
stock_price = 250.75   # Float variable to hold the current price of the stock
shares_owned = 10      # Integer variable to hold the number of shares owned

# Calculating the total investment value
total_investment = stock_price * shares_owned  # Total investment calculation

# Displaying the results
print(f"Stock Name: {stock_name}")
print(f"Current Price per Share: ${stock_price}")
print(f"Shares Owned: {shares_owned}")
print(f"Total Investment Value: ${total_investment:.2f}")
```

#### Explanation
1. **Variable Assignment**:
   - `stock_name`, `stock_price`, and `shares_owned` are variables that store different types of data relevant to stock trading.
   - `stock_name` is a string, `stock_price` is a float (representing monetary values), and `shares_owned` is an integer.

2. **Calculation**:
   - The `total_investment` variable is computed by multiplying `stock_price` by `shares_owned`. This represents the total amount invested in the stock.

3. **Output**:
   - The `print` statements display the values stored in the variables, formatted neatly for clarity. The `:.2f` formatting ensures that the investment value is displayed with two decimal places, which is standard in financial reporting.

#### 3. Application
In real-world finance, understanding how to assign and manipulate variables is fundamental for tasks such as tracking investments, calculating potential profits or losses, and managing portfolios. For example, if a trader wants to evaluate their investment in NVIDIA stocks, they can easily adjust the `stock_price` or `shares_owned` variables to see how changes affect their total investment value. This capability allows traders to make informed decisions based on current market conditions and personal investment strategies.

---

### Integration
This content is structured with clear headings and sections to facilitate easy parsing and integration into your learning platform. Each part of the code snippet is well-commented to enhance understanding, ensuring that you can follow along with your learning objectives effectively.

By mastering basic variable assignment, you will build a solid foundation for more advanced programming concepts that are essential for your career goals in finance and stock trading.