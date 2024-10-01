# Module Title: Data Handling with Pandas

## Exercise Requirements

### 1. Problem Statement
You are analyzing stock prices for a financial analysis project. Your dataset contains daily closing prices of a stock over the past month. However, before you can analyze trends or make predictions, you need to ensure the data is clean and ready for analysis. Your task is to calculate the mean and median of the closing stock prices after handling any missing values. This will help you understand the average performance of the stock and make informed decisions based on your analysis.

### 2. Fill-in-the-Blank Starter Code
```python
import pandas as pd

# Load the dataset
df = pd.read_csv('stock_prices.csv')

# Check for missing values in the 'Close' column
print("Missing values in 'Close':", df['Close'].isnull().sum())

# Fill missing values with the mean price
df['Close'] = df['Close'].fillna(______)

# Calculate the mean of the closing prices
mean_price = df['Close'].mean()

# Calculate the median of the closing prices
median_price = df['Close'].median()

# Print the results
print("Mean Closing Price:", mean_price)
print("Median Closing Price:", median_price)
```

### 3. Hints
- To fill in the missing values in the 'Close' column, consider using a function that calculates the average price of that column.
- Remember that the `mean()` and `median()` functions are built into Pandas and can be called directly on a Series (like `df['Close']`).
- Ensure that you check for any remaining missing values after your imputation to confirm that your dataset is clean.
- Comment your code to clarify each step, explaining why you are performing each action.

### 4. Expected Outcome
The student should be able to fill in the blanks correctly, demonstrating an understanding of how to handle missing data and calculate basic statistics using Pandas. The final solution should look like this:

```python
import pandas as pd

# Load the dataset
df = pd.read_csv('stock_prices.csv')

# Check for missing values in the 'Close' column
print("Missing values in 'Close':", df['Close'].isnull().sum())

# Fill missing values with the mean price
df['Close'] = df['Close'].fillna(df['Close'].mean())

# Calculate the mean of the closing prices
mean_price = df['Close'].mean()

# Calculate the median of the closing prices
median_price = df['Close'].median()

# Print the results
print("Mean Closing Price:", mean_price)
print("Median Closing Price:", median_price)
```

By completing this exercise, students will apply their knowledge of data cleaning and preprocessing techniques discussed in Lecture 3, reinforcing their understanding of these concepts in a real-world financial context.