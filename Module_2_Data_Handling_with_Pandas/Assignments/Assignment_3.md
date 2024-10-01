### Assignment: Analyze Historical Stock Data to Identify Seasonal Trends

#### Problem Statement
In this assignment, you will create a function that analyzes historical stock data to identify seasonal trends. You will use the data cleaning and preprocessing techniques discussed in Lecture 3 to ensure the dataset is ready for analysis. The goal is to calculate the average stock price for each month and identify any months where the stock price exceeds the average by more than 10%. This exercise will help you apply your knowledge of data cleaning and preprocessing in a real-world finance context.

#### Starter Code
Below is a basic code framework that you will build upon. This starter code includes comments that guide you on where to implement your solutions.

```python
import pandas as pd

def analyze_stock_data(file_path):
    # Step 1: Load the dataset
    df = pd.read_csv(file_path)
    
    # Step 2: Data Cleaning
    # Check for missing values and handle them
    print("Missing values before cleaning:")
    print(df.isnull().sum())
    
    # Fill missing values in 'Close' with the mean price
    df['Close'] = df['Close'].fillna(df['Close'].mean())
    
    # Remove duplicates
    df = df.drop_duplicates()
    
    # Convert date column to datetime format
    df['Date'] = pd.to_datetime(df['Date'])
    
    # Step 3: Analyze seasonal trends
    # Extract month from the date
    df['Month'] = df['Date'].dt.month
    
    # Calculate the average stock price for each month
    monthly_avg = df.groupby('Month')['Close'].mean()
    
    # Identify months where the average price exceeds the overall average by more than 10%
    overall_avg = df['Close'].mean()
    high_trend_months = monthly_avg[monthly_avg > overall_avg * 1.1]
    
    # Return results (students will need to format the output)
    return monthly_avg, high_trend_months

# Test the function with a sample dataset
file_path = 'historical_stock_data.csv'  # Replace with your actual file path
monthly_average, seasonal_trends = analyze_stock_data(file_path)
print("Monthly Average Prices:\n", monthly_average)
print("Months with High Trends:\n", seasonal_trends)
```

#### Detailed Instructions
1. **Data Loading**: Ensure that you replace `file_path` with the actual path to your historical stock data CSV file. This file should contain at least two columns: `Date` and `Close`.

2. **Data Cleaning**:
   - **Step 1**: After loading the dataset, check for missing values using `df.isnull().sum()`. Print the results before and after filling missing values.
   - **Step 2**: Use the mean of the 'Close' prices to fill any missing values.
   - **Step 3**: Remove any duplicate rows in the dataset.
   - **Step 4**: Convert the 'Date' column to datetime format using `pd.to_datetime()`.

3. **Analyzing Seasonal Trends**:
   - **Step 5**: Create a new column called 'Month' that extracts the month from the 'Date' column.
   - **Step 6**: Use `groupby()` to calculate the average closing price for each month and store this in a variable called `monthly_avg`.
   - **Step 7**: Calculate the overall average closing price and identify which months have an average price exceeding this by more than 10%. Store these results in a variable called `high_trend_months`.

4. **Output Formatting**: Ensure that the output of your function clearly displays both the monthly average prices and the months with high trends.

#### Criteria for Success and Evaluation
- **Correctness**: The function must correctly calculate monthly averages and identify high trend months based on the criteria provided.
- **Code Quality**: The code should be clean, well-structured, and include comments that explain each step.
- **Documentation**: Include a brief description at the top of your code explaining what the function does, its parameters, and its return values.
- **Output Clarity**: The output should be formatted in a clear manner that is easy to read and understand.

By completing this assignment, you will gain practical experience with data cleaning and preprocessing techniques while also applying them to a relevant finance scenario. Good luck!