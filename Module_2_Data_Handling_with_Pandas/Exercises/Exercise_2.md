# Module Title: Data Handling with Pandas

## Exercise Requirements

### 1. Problem Statement
You have been provided with a CSV dataset containing historical stock prices for NVIDIA. However, upon loading the data, you notice that some rows contain missing values (NaN) in critical columns such as 'Open', 'Close', and 'Volume'. As an aspiring Python Developer focusing on stock trading, your task is to clean this dataset by removing any rows that have missing values. This will ensure that your analysis is based on complete data, which is crucial for making informed trading decisions.

### 2. Fill-in-the-Blank Starter Code
```python
import pandas as pd

# Load the NVIDIA stock dataset
nvidia_stock_data = pd.read_csv('nvidia_stock_prices.csv')

# Display the first few rows of the dataset to inspect it
print(nvidia_stock_data.head())

# Check for missing values in the dataset
print(nvidia_stock_data.isnull().sum())

# Clean the dataset by removing rows with missing values
cleaned_data = nvidia_stock_data.______(______)

# Display the cleaned dataset
print(cleaned_data.head())

# Verify that there are no missing values left
print(cleaned_data.isnull().sum())
```

### 3. Hints
- For the blank in `cleaned_data = nvidia_stock_data.______`, think about the method used to drop rows based on missing values.
- The second blank requires you to specify how to handle missing data. Look for a method that allows you to remove rows with any NaN values.
- Remember to inspect the dataset before and after cleaning it to see the changes you've made.

### 4. Expected Outcome
Upon completing the exercise, you should be able to fill in the blanks correctly with:
- For the first blank: `dropna`
- For the second blank: `how='any'`

The final code should look like this:

```python
import pandas as pd

# Load the NVIDIA stock dataset
nvidia_stock_data = pd.read_csv('nvidia_stock_prices.csv')

# Display the first few rows of the dataset to inspect it
print(nvidia_stock_data.head())

# Check for missing values in the dataset
print(nvidia_stock_data.isnull().sum())

# Clean the dataset by removing rows with missing values
cleaned_data = nvidia_stock_data.dropna(how='any')

# Display the cleaned dataset
print(cleaned_data.head())

# Verify that there are no missing values left
print(cleaned_data.isnull().sum())
```

This solution demonstrates your understanding of data cleaning techniques as discussed in the lecture. You should also include comments explaining each step of your code, reinforcing your learning and ensuring clarity in your work.