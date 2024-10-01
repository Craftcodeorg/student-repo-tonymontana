# Module Title: Introduction to Python Programming

## Exercise Requirements

### 1. Problem Statement
As you embark on your journey to become a Python Developer focusing on stock trading, it's essential to apply programming concepts to real-world scenarios. In the finance sector, we often deal with numerical data, including stock prices and trading volumes. 

For this exercise, you will write a function that checks if a stock price is even or odd. This can be useful for implementing specific trading strategies or for data analysis where certain operations might depend on the parity of a number (e.g., deciding to buy or sell based on whether the price is even or odd).

### 2. Fill-in-the-Blank Starter Code
Below is the starter code for your function. Your task is to fill in the blanks to complete the function that checks if a stock price is even or odd.

```python
# Starter code for implementing lecture concepts
def check_even_or_odd(price):
    """
    This function checks if the given stock price is even or odd.
    
    Parameters:
    price (float): The stock price to check.
    
    Returns:
    str: A message indicating whether the price is even or odd.
    """
    # Check if the price is even
    if price % 2 == 0:
        return "The stock price of ${} is even.".format(price)
    else:
        return "The stock price of ${} is odd.".format(price)

# Test the function with example stock prices
print(check_even_or_odd(______))  # Fill in with an even number
print(check_even_or_odd(______))  # Fill in with an odd number
```

### 3. Hints
- Remember that an even number is divisible by 2 without a remainder. You can use the modulus operator `%` for this check.
- When testing your function, consider using common stock prices you might encounter in your analysis.
- Ensure your function returns a string that clearly states whether the price is even or odd.

### 4. Expected Outcome
By completing this exercise, you should be able to:
- Fill in the blanks correctly to create a functional program.
- Demonstrate an understanding of how to apply conditional statements in Python.
- Produce output that clearly indicates whether a given stock price is even or odd, reflecting your ability to manipulate numerical data in a financial context.

Your final solution should adhere to best practices, including clear comments explaining each step of your logic. This exercise will help reinforce your understanding of Python programming as it applies to stock trading and financial analysis.

---

### Integration
This exercise is structured to align with your learning objectives and interests in finance and programming. Ensure that you save your work and test your function with different inputs to see how it behaves. Happy coding!