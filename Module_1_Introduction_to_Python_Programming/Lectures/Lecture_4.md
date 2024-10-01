# Lecture Title: 4. Control Structures: If Statements, Loops

## 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Understand and implement control structures in Python, specifically if statements and loops.
- Apply these concepts to create decision-making algorithms and repetitive tasks relevant to stock trading applications.
- Write simple Python scripts that utilize control structures to analyze stock market data.

## 2. Introduction:
Control structures are fundamental components in programming that allow us to dictate the flow of execution based on certain conditions. In the context of stock trading, being able to make decisions based on market conditions is crucial. For instance, you may want to execute a trade only if a stock price drops below a certain threshold. This lecture will focus on two key types of control structures: **if statements** and **loops**. Mastering these concepts will empower you to write more dynamic and responsive trading algorithms, aligning with your goal of becoming a proficient Python Developer in the finance sector.

## 3. Core Concepts:
### A. If Statements
- **Definition**: An if statement evaluates a condition and executes a block of code if the condition is true.
- **Syntax**:
  ```python
  if condition:
      # execute this block
  ```
- **Example**:
  ```python
  stock_price = 150
  if stock_price < 100:
      print("Buy the stock")
  else:
      print("Hold the stock")
  ```
  In this example, we check if the stock price is below $100 and decide whether to buy or hold.

### B. Loops
- **Definition**: Loops allow you to execute a block of code multiple times. The two main types are `for` loops and `while` loops.
  
#### 1. For Loops
- **Usage**: To iterate over a sequence (like a list or range).
- **Syntax**:
  ```python
  for item in sequence:
      # execute this block
  ```
- **Example**:
  ```python
  stock_prices = [150, 200, 250]
  for price in stock_prices:
      print(f"Current price: {price}")
  ```

#### 2. While Loops
- **Usage**: To execute a block as long as a condition is true.
- **Syntax**:
  ```python
  while condition:
      # execute this block
  ```
- **Example**:
  ```python
  count = 0
  while count < 5:
      print("Counting:", count)
      count += 1
  ```

## 4. Practical Application:
In stock trading, you might use control structures to analyze price trends or automate trading decisions. For instance, consider a scenario where you want to monitor stock prices until they reach a desired threshold:

```python
stock_prices = [150, 145, 160, 155]
target_price = 140

for price in stock_prices:
    if price < target_price:
        print("Trigger buy order!")
        break
```
In this example, the loop checks each stock price, and if it finds one below the target price, it triggers a buy order.

## 5. Summary:
Today, we explored control structures in Python, focusing on if statements and loops. We learned how these constructs enable us to make decisions and repeat actions based on conditions—essential skills for developing trading algorithms. Remember that mastering these concepts is critical for your journey toward becoming a successful Python Developer in the finance sector.

## 6. Next Steps:
In our next lecture, we will delve into functions—how to create reusable code blocks that can simplify our programs and enhance their functionality. Before the next session, review the syntax for if statements and loops, and try writing a few examples of your own to solidify your understanding. This preparation will greatly enhance your grasp of functions when we cover them next!