# Module Title: Introduction to Python Programming

## Example 3: Creating a Simple Function

### 1. Introduction
In this section, we will explore the concept of creating simple functions in Python, building upon the foundational knowledge of basic syntax and data types discussed in Lecture 3. Functions are essential in programming as they allow you to encapsulate code into reusable blocks, making your code cleaner and more organized. In finance, functions can help automate calculations, such as determining the total investment value or calculating returns on investment.

### 2. Code Snippet
Here’s a simple function that calculates the total value of shares owned based on the number of shares and the price per share:

```python
def calculate_total_value(shares, price_per_share):
    """
    Calculate the total value of shares owned.
    
    Parameters:
    shares (int): The number of shares owned.
    price_per_share (float): The price per share.
    
    Returns:
    float: The total value of the shares.
    """
    # Error handling for invalid input types
    if not isinstance(shares, int) or not isinstance(price_per_share, (int, float)):
        raise ValueError("Invalid input: 'shares' must be an integer and 'price_per_share' must be a number.")
    
    # Calculate total value
    total_value = shares * price_per_share
    return total_value

# Example usage of the function
try:
    shares_owned = 100
    price_per_share = 150.75
    total_investment_value = calculate_total_value(shares_owned, price_per_share)
    print("Total Value of Shares: $", total_investment_value)
except ValueError as e:
    print(e)
```

### 3. Explanation
- **Function Definition**: The function `calculate_total_value` is defined with two parameters: `shares` and `price_per_share`. This allows us to pass in the number of shares and the corresponding price when we call the function.
  
- **Docstring**: The docstring provides a description of what the function does, its parameters, and its return type. This is crucial for documentation and helps other programmers understand how to use the function.

- **Error Handling**: Before performing calculations, the function checks if the input types are correct. If not, it raises a `ValueError`. This is a best practice to ensure that the function behaves correctly and helps in debugging.

- **Calculation**: The function multiplies `shares` by `price_per_share` to compute the total value.

- **Return Statement**: Finally, it returns the calculated total value.

- **Example Usage**: The code snippet includes an example of how to call the function and handle potential errors gracefully.

### 4. Application
In finance, this function can be applied in various scenarios such as:
- **Portfolio Management**: Investors can use this function to quickly assess the total value of their stock holdings, allowing them to make informed decisions about buying or selling shares.
- **Trading Algorithms**: Automated trading systems can utilize this function to calculate the value of assets in real-time, enabling traders to respond promptly to market changes.
- **Financial Reporting**: This simple function can be part of a larger application that generates financial reports, providing insights into an investor's portfolio performance.

### Integration
This content is structured with clear headings and sections for easy parsing and integration into your learning platform. The use of markdown formatting ensures that the material is presented in an organized manner, enhancing readability and comprehension for beginner-level programmers like yourself.

By mastering functions in Python, you will enhance your coding capabilities significantly, making it easier to develop applications tailored to your career goals in finance and stock trading. Continue practicing these concepts through project-based learning and interactive tutorials to solidify your understanding!