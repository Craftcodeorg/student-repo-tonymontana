# Assignment: Stock Price Data Analysis with Pandas

## Problem Statement
As an aspiring Python Developer in the finance sector, your task is to create a script that loads stock price data from a CSV file, cleans the data, and outputs summary statistics. This assignment will help you understand the practical applications of data manipulation using the Pandas library, which is essential for analyzing financial datasets.

## Starter Code
Below is a basic code framework that you will expand upon. The starter code sets up the environment and includes comments to guide you on where to implement your solutions.

```python
import pandas as pd

# Function to load, clean, and analyze stock price data
def analyze_stock_data(file_path):
    # Step 1: Load the stock price data from a CSV file
    data = pd.read_csv(file_path)

    # Step 2: Display the first few rows of the dataset
    print("Initial Data:")
    print(data.head())

    # Step 3: Clean the data (handle missing values and duplicates)
    # TODO: Implement data cleaning steps here

    # Step 4: Calculate summary statistics
    summary_statistics = data.describe()
    
    # Return cleaned data and summary statistics
    return data, summary_statistics

# Test the function with your CSV file path
file_path = 'path_to_your_stock_prices.csv'  # Replace with your actual file path
cleaned_data, stats = analyze_stock_data(file_path)
print("\nSummary Statistics:")
print(stats)
```

## Detailed Instructions
1. **Load the Data**: 
   - In Step 1 of the starter code, ensure that you correctly load the stock price data from a CSV file using `pd.read_csv()`.
   
2. **Inspect the Data**:
   - Use the `head()` method to display the first few rows of the dataset after loading it. This will help you understand the structure of your data.

3. **Data Cleaning**:
   - In Step 3, implement data cleaning steps:
     - Check for and handle any missing values using `data.dropna()` or `data.fillna()`.
     - Identify and remove any duplicate rows using `data.drop_duplicates()`.
   
4. **Calculate Summary Statistics**:
   - In Step 4, use the `describe()` method to calculate summary statistics for your dataset, which should include count, mean, standard deviation, min, max, and quartiles.

5. **Output Results**:
   - Print the cleaned data and the summary statistics in a clear format.

## Criteria for Success and Evaluation
Your assignment will be evaluated based on the following criteria:

- **Correctness**: The function correctly loads, cleans, and analyzes the stock price data.
- **Code Quality**: The code is clean, well-structured, and follows best practices (e.g., meaningful variable names, appropriate comments).
- **Output Clarity**: The output is formatted in a clear and user-friendly manner.
- **Data Handling Skills**: Demonstrates an understanding of key Pandas operations such as loading data, cleaning data, and generating summary statistics.

By completing this assignment, you will gain hands-on experience with Pandas in a context relevant to your career goals in finance. Good luck!