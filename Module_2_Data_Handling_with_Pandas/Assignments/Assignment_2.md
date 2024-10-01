### Assignment: Visualizing Stock Price Trends with Matplotlib

#### Problem Statement
As an aspiring Python Developer in the finance sector, it's essential to analyze stock price trends to make informed investment decisions. In this assignment, you will develop a visualization of stock price trends for NVIDIA over the last year using data from a CSV file. This task will help you apply the concepts of loading datasets and performing basic data inspection that were covered in the lecture.

#### Starter Code
Below is the starter code that sets up the environment for your analysis. You will need to complete this code to load the stock price data, inspect it, and create a visualization.

```python
import pandas as pd
import matplotlib.pyplot as plt

# Step 1: Load the dataset
nvidia_stock_data = pd.read_csv('nvidia_stock_prices.csv')

# Step 2: Inspect the dataset
print(nvidia_stock_data.head())
print(nvidia_stock_data.info())

# Step 3: Create a visualization of stock price trends
def plot_stock_trends(data):
    # Ensure the 'Date' column is in datetime format
    data['Date'] = pd.to_datetime(data['Date'])
    
    # Set the 'Date' column as the index
    data.set_index('Date', inplace=True)
    
    # Plotting the stock prices
    plt.figure(figsize=(12, 6))
    plt.plot(data['Close'], label='NVIDIA Closing Prices', color='blue')
    plt.title('NVIDIA Stock Price Trends Over the Last Year')
    plt.xlabel('Date')
    plt.ylabel('Stock Price (USD)')
    plt.legend()
    plt.grid()
    plt.show()

# Call the function to plot the trends
plot_stock_trends(nvidia_stock_data)
```

#### Detailed Instructions
1. **Load the Dataset**: Ensure you have a CSV file named `nvidia_stock_prices.csv` containing at least two columns: `Date` and `Close`. The `Date` column should contain dates and the `Close` column should have the corresponding closing stock prices.

2. **Inspect the Dataset**: Use the provided inspection methods (`head()` and `info()`) to check that your data has been loaded correctly. Make sure that there are no missing values in the columns you will be using.

3. **Modify the Function**:
   - In the `plot_stock_trends` function, ensure that you convert the 'Date' column to a datetime format and set it as the index of your DataFrame.
   - Use Matplotlib to create a line plot of the closing prices over time. Make sure to label your axes and include a title for clarity.

4. **Enhance Your Visualization**:
   - Consider adding features such as gridlines for better readability.
   - You can also customize colors or line styles to enhance your plot’s aesthetics.

5. **Run Your Code**: After completing your modifications, run your code to visualize NVIDIA's stock price trends over the past year.

#### Criteria for Success and Evaluation
Your submission will be evaluated based on the following criteria:
- **Correctness**: The function should correctly load the dataset, inspect it, and generate a clear and accurate plot of stock price trends.
- **Code Quality**: Your code should be clean, well-organized, and include comments explaining each step.
- **Visualization Clarity**: The final plot should be easy to read, with appropriate labels, legends, and titles.

By completing this assignment, you will gain practical experience in handling financial datasets and visualizing trends, which are crucial skills for your future career in finance.