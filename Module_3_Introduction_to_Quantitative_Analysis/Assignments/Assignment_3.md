### Assignment: Analyzing Investment Performance Metrics Using Visualizations

#### Problem Statement:
You are tasked with creating a Python program that analyzes and visualizes investment performance metrics, specifically focusing on Return on Investment (ROI) and the Sharpe Ratio. The program should take a list of investment returns and corresponding risk-free rates, calculate the ROI and Sharpe Ratio for each investment, and then visualize these metrics using a bar chart. This will help investors understand the performance of their investments in a clear and visual format.

#### Starter Code:
Below is a basic framework to get you started. This code includes functions to calculate ROI and Sharpe Ratio, as well as a placeholder for the visualization part. You will need to complete the visualization section using the Matplotlib library.

```python
import matplotlib.pyplot as plt

# Function to calculate ROI
def calculate_roi(net_profit, investment_cost):
    return (net_profit / investment_cost) * 100

# Function to calculate Sharpe Ratio
def calculate_sharpe_ratio(portfolio_return, risk_free_rate, std_dev):
    return (portfolio_return - risk_free_rate) / std_dev

# Sample data: List of net profits, investment costs, risk-free rates, and standard deviations
net_profits = [200, 500, 300]
investment_costs = [1000, 1500, 1200]
risk_free_rates = [0.02, 0.03, 0.01]  # Example risk-free rates
std_devs = [0.05, 0.07, 0.04]  # Example standard deviations of returns

# Step 1: Calculate ROI and Sharpe Ratio for each investment
rois = [calculate_roi(net_profit, cost) for net_profit, cost in zip(net_profits, investment_costs)]
sharpe_ratios = [calculate_sharpe_ratio(roi / 100, rf_rate, std_dev) for roi, rf_rate, std_dev in zip(rois, risk_free_rates, std_devs)]

# Step 2: Visualize the results
# You will implement the visualization here

# Placeholder for visualization code
def visualize_metrics(rois, sharpe_ratios):
    # Create a bar chart comparing ROI and Sharpe Ratio
    x_labels = ['Investment 1', 'Investment 2', 'Investment 3']
    
    # Set the positions and width for the bars
    positions = range(len(x_labels))
    width = 0.35
    
    fig, ax = plt.subplots()
    
    # Create bars for ROI and Sharpe Ratio
    ax.bar(positions, rois, width=width, label='ROI (%)', color='blue')
    ax.bar([p + width for p in positions], sharpe_ratios, width=width, label='Sharpe Ratio', color='orange')
    
    # Add labels and title
    ax.set_ylabel('Metrics')
    ax.set_title('Investment Performance Metrics')
    ax.set_xticks([p + width / 2 for p in positions])
    ax.set_xticklabels(x_labels)
    ax.legend()
    
    plt.show()

# Call the visualize function with calculated metrics
visualize_metrics(rois, sharpe_ratios)
```

#### Detailed Instructions:
1. **Step 1**: Modify the `visualize_metrics` function to create a bar chart that compares the ROI and Sharpe Ratio for each investment. Ensure that the bars are labeled correctly.

2. **Step 2**: Add titles and labels to your axes to make your chart clear and informative. Consider adding grid lines to enhance readability.

3. **Step 3**: Enhance the visualization by changing colors or adding data labels on top of each bar to indicate the exact values of ROI and Sharpe Ratio.

4. **Step 4**: Test your program with different sets of data to ensure that it works correctly and produces meaningful visualizations.

#### Criteria for Success and Evaluation:
- **Correctness**: The program accurately calculates ROI and Sharpe Ratio based on the provided data.
- **Visualization Quality**: The bar chart is clear, well-labeled, and visually appealing.
- **Code Quality**: The code is well-structured, follows best practices (e.g., proper naming conventions), and includes comments explaining each section.
- **Functionality**: The program runs without errors and handles different input values gracefully.

This assignment will help you apply the concepts of ROI and Sharpe Ratio from the lecture in a practical coding scenario while enhancing your Python skills relevant to finance.