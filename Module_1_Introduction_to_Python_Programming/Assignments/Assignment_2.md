### Assignment: Stock Price Average Calculator

#### Problem Statement:
In the world of finance, analyzing stock prices is crucial for making informed investment decisions. Your task is to create a Python program that takes user input for stock prices and calculates the average price. This assignment will help you apply the concepts learned in Lecture 2 about setting up your Python environment and using essential libraries.

#### Starter Code:
Below is the basic framework for your program. You will expand upon this code to complete the task.

```python
# Starter code for calculating the average stock price

def calculate_average_stock_price(prices):
    """
    This function calculates the average stock price from a list of prices.
    
    Parameters:
    prices (list): A list of stock prices (float).
    
    Returns:
    float: The average stock price.
    """
    # Step 1: Calculate the average price
    total_price = sum(prices)
    average_price = total_price / len(prices) if prices else 0
    return average_price

# Step 2: Get user input for stock prices
def get_stock_prices():
    prices = []
    while True:
        user_input = input("Enter a stock price (or type 'done' to finish): ")
        if user_input.lower() == 'done':
            break
        try:
            price = float(user_input)
            prices.append(price)
        except ValueError:
            print("Please enter a valid number.")
    return prices

# Main function to execute the program
def main():
    print("Welcome to the Stock Price Average Calculator!")
    stock_prices = get_stock_prices()
    
    # Step 3: Calculate and display the average stock price
    average = calculate_average_stock_price(stock_prices)
    print(f"The average stock price is: {average:.2f}")

if __name__ == "__main__":
    main()
```

#### Detailed Instructions:
1. **Step 1**: The `calculate_average_stock_price` function is already defined. Ensure it correctly computes the average of the provided list of stock prices.

2. **Step 2**: The `get_stock_prices` function prompts users to enter stock prices. It should continue to accept input until the user types 'done'. Make sure to handle invalid inputs gracefully by prompting the user again.

3. **Step 3**: In the `main` function, after retrieving the list of stock prices, call the `calculate_average_stock_price` function and print the result. Ensure that the output is formatted to two decimal places for better readability.

4. **Bonus Challenge**: Modify your program to handle edge cases, such as when no prices are entered. In such cases, inform the user that no data was provided.

#### Criteria for Success and Evaluation:
- **Correctness**: The program accurately calculates and displays the average stock price.
- **User Input Handling**: The program gracefully handles invalid inputs and allows users to enter multiple prices until they choose to stop.
- **Code Quality**: The code is well-structured, follows best practices, and includes comments explaining each section.
- **Output Formatting**: The average price is displayed in a clear and user-friendly manner, formatted to two decimal places.

This assignment not only reinforces your understanding of Python programming but also introduces you to practical applications in finance, aligning with your career goals in stock trading. Happy coding!