### Assignment: Analyzing Stock Prices

#### Problem Statement:
In the world of finance, analyzing stock prices is crucial for making informed trading decisions. Your task is to create a function that takes a list of stock prices and returns the maximum and minimum prices from that list. This exercise will help you apply the basic syntax rules and data types discussed in Lecture 3 of the Python Programming course, while also giving you practical experience relevant to stock trading.

#### Starter Code:
Below is the starter code for your assignment. You will need to complete the function `analyze_stock_prices` to achieve the desired functionality.

```python
# Starter code for analyzing stock prices

def analyze_stock_prices(prices):
    # Step 1: Initialize variables to hold maximum and minimum prices
    max_price = None
    min_price = None
    
    # Step 2: Loop through each price in the list
    for price in prices:
        # Update max_price if necessary
        if max_price is None or price > max_price:
            max_price = price
        
        # Update min_price if necessary
        if min_price is None or price < min_price:
            min_price = price
            
    # Return the maximum and minimum prices
    return max_price, min_price

# Test the function with sample data
stock_prices = [150.75, 145.30, 160.00, 155.50, 142.80]
max_price, min_price = analyze_stock_prices(stock_prices)
print(f"Maximum Stock Price: ${max_price}")
print(f"Minimum Stock Price: ${min_price}")
```

#### Detailed Instructions:
1. **Step 1**: Review the starter code and understand how it initializes `max_price` and `min_price` to `None`. This allows you to determine if you are comparing with the first element of the list.

2. **Step 2**: Implement the logic inside the loop to correctly update `max_price` and `min_price`. Ensure that you only update these variables if the current price is greater than `max_price` or less than `min_price`.

3. **Step 3**: Modify the return statement to clearly return both `max_price` and `min_price`.

4. **Step 4**: Test your function with different sets of stock prices to ensure it works correctly under various scenarios, including edge cases like an empty list or a list with only one price.

5. **Step 5**: Add comments throughout your code to explain your logic and enhance readability.

#### Criteria for Success and Evaluation:
- **Functionality**: The function should correctly return the maximum and minimum stock prices from the provided list.
- **Code Quality**: The code should be clean, well-structured, and easy to read. Use meaningful variable names and include comments where necessary.
- **Testing**: You should test your function with at least three different lists of stock prices, including edge cases.
- **Documentation**: Your code should be documented with comments explaining each part of the process.

By completing this assignment, you will enhance your understanding of Python's basic syntax and data types while applying them to a real-world financial scenario. Good luck!