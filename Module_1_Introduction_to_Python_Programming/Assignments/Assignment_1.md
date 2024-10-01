# Assignment: Build a Simple Calculator for Financial Operations

## Problem Statement
Create a simple calculator in Python that can perform basic arithmetic operations: addition, subtraction, multiplication, and division. This calculator will serve as a foundational tool for financial calculations, enabling users to quickly compute values relevant to stock trading and investment analysis.

## Starter Code
Below is a basic framework for your calculator. You will need to expand upon this code to complete the assignment.

```python
# Starter code for a simple calculator

def calculator():
    print("Welcome to the Financial Calculator!")
    print("Select operation:")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")

    # Take input from the user
    operation = input("Enter operation (1/2/3/4): ")

    # Check if the operation is valid
    if operation in ['1', '2', '3', '4']:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        
        # Perform calculation based on user input
        if operation == '1':
            result = num1 + num2
            print(f"The result of {num1} + {num2} = {result}")
        elif operation == '2':
            result = num1 - num2
            print(f"The result of {num1} - {num2} = {result}")
        elif operation == '3':
            result = num1 * num2
            print(f"The result of {num1} * {num2} = {result}")
        elif operation == '4':
            # Handle division by zero
            if num2 != 0:
                result = num1 / num2
                print(f"The result of {num1} / {num2} = {result}")
            else:
                print("Error! Division by zero.")
    else:
        print("Invalid input! Please select a valid operation.")

# Call the calculator function to run the program
calculator()
```

## Detailed Instructions
1. **Enhance User Experience**: Modify the greeting message to include a brief description of what the calculator does and its relevance to financial calculations.

2. **Add Loop for Continuous Use**: Implement a loop that allows the user to perform multiple calculations without restarting the program. After each calculation, ask the user if they want to perform another operation.

3. **Implement Input Validation**: Ensure that the input for both numbers and operations is validated. If the user enters an invalid number or operation, prompt them to enter a valid one.

4. **Add Functionality for Percentage Calculation**: Introduce an additional option for calculating percentages. For example, allow users to calculate what percentage one number is of another.

5. **Format Output**: Ensure that the output is formatted nicely, with two decimal places for results. For example, if the result is `5.123456`, it should display as `5.12`.

6. **Documentation and Comments**: Add comments throughout your code explaining what each part does, especially where calculations occur. This will help others (and yourself) understand your code better.

## Criteria for Success and Evaluation
Your assignment will be evaluated based on the following criteria:

- **Functionality**: The calculator must perform all specified operations correctly and handle edge cases (like division by zero).
- **User Experience**: The program should provide a smooth user experience with clear instructions and options.
- **Code Quality**: Your code should be clean, well-organized, and follow best practices in Python programming.
- **Documentation**: Adequate comments should be included to explain the purpose of different sections of the code.

### Success Criteria:
- The calculator performs addition, subtraction, multiplication, and division correctly.
- The program allows for continuous use without restarting.
- Input validation is implemented effectively.
- The output is formatted to two decimal places.
- Code is well-documented and easy to understand.

This assignment not only reinforces your understanding of basic Python syntax and operations but also introduces you to practical applications in finance, aligning with your career goals in stock trading. Happy coding!