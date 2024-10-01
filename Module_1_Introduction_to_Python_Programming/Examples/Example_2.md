# Module Title: Introduction to Python Programming

## Example 2: Using if statements for decision making

### 1. Introduction
In finance, making informed decisions based on data is crucial. This is where conditional statements, such as `if` statements, come into play. They allow you to execute specific code based on certain conditions, which is essential for tasks like analyzing stock prices and making trading decisions. Building on the concepts from the previous lecture, where we learned how to set up our Python environment, this example will illustrate how to use `if` statements to make decisions based on stock data.

### 2. Code Snippet
Here’s a simple Python code snippet that uses `if` statements to determine whether to buy, hold, or sell a stock based on its current price compared to a target price:

```python
# Define the current stock price and target price
current_price = 150.00  # Example current price of the stock
target_price = 145.00    # Target price for buying the stock

# Decision making using if statements
if current_price < target_price:
    print("Buy the stock!")
elif current_price > target_price:
    print("Sell the stock!")
else:
    print("Hold the stock!")

# Error handling example
try:
    # Simulate a potential error by dividing by zero
    risk_factor = 0
    decision = current_price / risk_factor
except ZeroDivisionError:
    print("Error: Cannot divide by zero. Adjust your risk factor.")
```

### 3. Explanation
- **Variables**: The code begins by defining two variables: `current_price` and `target_price`. These represent the stock's current market price and the price at which you want to buy the stock, respectively.
  
- **If Statements**: 
  - The first `if` checks if the `current_price` is less than the `target_price`. If true, it prints "Buy the stock!" indicating that it's a good time to purchase.
  - The `elif` (else if) checks if the `current_price` is greater than the `target_price`. If this condition is true, it suggests selling the stock.
  - The final `else` statement covers the scenario where the current price equals the target price, prompting a "Hold the stock!" message.

- **Error Handling**: The code also includes a try-except block to handle potential errors gracefully. In this case, it simulates an error by attempting to divide by zero, which would normally crash the program. Instead, it catches the `ZeroDivisionError` and prints an informative message.

### 4. Application
In real-world finance, traders often rely on algorithms that utilize conditional statements like these to automate their trading decisions. For example, a trader might set a target price for a stock based on their analysis of market trends. By using an automated script that includes `if` statements, they can quickly react to market changes without manual intervention.

This approach not only saves time but also helps in making consistent and emotion-free trading decisions. For instance, if a trader has set a target price of $145 for buying shares of NVIDIA and the current market price drops below this threshold, their automated script can execute a buy order instantly.

### Conclusion
Understanding and implementing `if` statements in Python is vital for decision-making in finance. This example builds upon the foundational skills learned in setting up your Python environment and demonstrates how to apply programming concepts in real-world scenarios relevant to stock trading. As you continue your learning journey, consider how you can expand upon these concepts with more complex conditions and data analysis techniques.