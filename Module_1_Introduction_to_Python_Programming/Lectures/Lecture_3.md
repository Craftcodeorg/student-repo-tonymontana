# Lecture 3: Basic Syntax and Data Types

### 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Understand and apply basic syntax rules in Python.
- Identify and utilize fundamental data types in Python programming.
- Recognize the relevance of these concepts in developing applications for stock trading.

### 2. Introduction:
In this lecture, we will explore the foundational elements of Python programming: its basic syntax and data types. Understanding these concepts is crucial for any aspiring Python developer, especially in fields like finance and stock trading, where precise data manipulation is key. As you aim to develop algorithms for stock analysis or trading bots, mastering the syntax and data types will empower you to write clean, efficient code that can handle financial data effectively.

### 3. Core Concepts:

#### A. Basic Syntax:
- **Indentation**: In Python, indentation is used to define the structure of the code blocks. Unlike other programming languages that use braces or keywords, Python relies on consistent indentation.
  - Example:
    ```python
    if True:
        print("This is indented")
    ```

- **Comments**: Comments are crucial for documenting your code. Use `#` for single-line comments and `''' '''` or `""" """` for multi-line comments.
  - Example:
    ```python
    # This is a single-line comment
    """
    This is a multi-line comment
    """
    ```

#### B. Data Types:
Python has several built-in data types, but we will focus on the most commonly used ones in finance:

1. **Integers**: Whole numbers without a decimal point.
   - Example: `shares = 100`

2. **Floats**: Numbers that contain a decimal point, useful for representing prices.
   - Example: `price_per_share = 150.75`

3. **Strings**: Text data, enclosed in quotes.
   - Example: `ticker_symbol = "AAPL"`

4. **Booleans**: Represents `True` or `False`, often used in conditions.
   - Example: `is_market_open = True`

### 4. Practical Application:
In stock trading applications, you will often work with these data types to manage and analyze financial data. For instance, you might need to calculate the total value of your shares:

```python
shares = 100
price_per_share = 150.75
total_value = shares * price_per_share
print("Total Value of Shares: $", total_value)
```

This snippet demonstrates how to use integers and floats together to compute the total value of shares you own.

### 5. Summary:
In this lecture, we covered the basic syntax of Python, including indentation and comments, which help maintain code readability. We also explored fundamental data types such as integers, floats, strings, and booleans, essential for handling financial data in stock trading applications. Remember, mastering these concepts is vital as they form the backbone of your programming skills.

### 6. Next Steps:
In the next lecture, we will dive into control structures such as loops and conditionals, which will allow you to make decisions in your code based on different conditions—an important skill for implementing trading strategies. To prepare, review the concepts of syntax and data types, and think about how you might use them in decision-making scenarios within stock trading algorithms.