# Module Title: Introduction to Quantitative Analysis

## 1. Introduction
In this module, we will focus on **Example 2: Building a Simple ROI Calculator**. This example is a practical application of the statistical concepts discussed in Lecture 2, which covers key statistical measures such as mean, median, variance, and standard deviation. Understanding these concepts is crucial for analyzing financial data, particularly in stock trading. The ROI (Return on Investment) calculator will help you evaluate the profitability of investments, making it a vital tool for anyone looking to make informed financial decisions.

## 2. Code Snippet
Here’s a simple Python code snippet for building a basic ROI calculator:

```python
def calculate_roi(initial_investment, final_value):
    """
    Calculate the Return on Investment (ROI).

    Parameters:
    initial_investment (float): The amount of money invested initially.
    final_value (float): The value of the investment at the end of the period.

    Returns:
    float: The ROI as a percentage.
    """
    try:
        # Ensure the inputs are valid numbers
        initial_investment = float(initial_investment)
        final_value = float(final_value)

        if initial_investment <= 0:
            raise ValueError("Initial investment must be greater than zero.")

        # Calculate ROI
        roi = (final_value - initial_investment) / initial_investment * 100
        return roi

    except ValueError as e:
        return f"Error: {e}"

# Example usage
initial_investment = 1000  # Example initial investment
final_value = 1500         # Example final value of the investment

roi_result = calculate_roi(initial_investment, final_value)
print(f"Return on Investment (ROI): {roi_result:.2f}%")
```

## 3. Explanation
### Step-by-Step Breakdown:
1. **Function Definition**: The `calculate_roi` function takes two parameters: `initial_investment` and `final_value`.
2. **Input Validation**: The function checks if the inputs can be converted to float. It also ensures that the initial investment is greater than zero to avoid division by zero errors.
3. **ROI Calculation**: The formula used for calculating ROI is:
   \[
   \text{ROI} = \frac{\text{Final Value} - \text{Initial Investment}}{\text{Initial Investment}} \times 100
   \]
   This formula computes the percentage return based on the initial investment and the final value.
4. **Error Handling**: If there is an issue with the inputs, a ValueError is raised and caught, returning an appropriate error message.
5. **Example Usage**: The code provides an example where an initial investment of $1000 grows to $1500, and it prints the calculated ROI.

### Real-World Problem Solving:
This ROI calculator can be used by investors to quickly assess the profitability of their investments. By inputting different values for initial investments and final returns, users can evaluate various investment scenarios, helping them make better financial decisions.

## 4. Application
### Real-World Application in Finance:
In finance, understanding ROI is essential for evaluating investment opportunities. Investors can use this calculator to compare different stocks or investment projects based on their returns. For instance, if an investor has multiple options with varying initial investments and expected returns, they can use the ROI calculator to determine which investment yields the highest return.

This practical application not only aids in decision-making but also enhances portfolio management by allowing investors to track their performance over time. By integrating such tools into their financial analysis, investors can make data-driven decisions that align with their financial goals.

---

By mastering these concepts and tools, you will be well-equipped to pursue your career goal of becoming a Python Developer focused on stock trading. Keep practicing and exploring real-world applications to reinforce your learning!