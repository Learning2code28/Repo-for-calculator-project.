# Repo-for-calculator-project.
#Code for my calculator project for week 8 task.

# Simple calculator program that performs basic arithmetic operations.

def add(num1, num2):
    #Add two numbers
    return num1 + num2

def subtract(num1, num2):
    #Subtract the second number from the first
    return num1 - num2

def multiply(num1, num2):
    #Multiply two numbers
    return num1 * num2

def divide(num1, num2):
    #Divide the first number by the second, checking for division by zero
    if num2 == 0:
        return "Error! Division by zero is not allowed."
    return num1 / num2

# Main program loop
def main():
    while True:
        print("Select an operation to perform:")
        print("1. Add")
        print("2. Subtract")
        print("3. Multiply")
        print("4. Divide")
        print("5. Exit")

        # Take input from the user for operation choice
        operation = input("Enter your choice (1/2/3/4/5): ")

        if operation == "5":
            print("Thank you for using the calculator!")
            break

        if operation in ["1", "2", "3", "4"]:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
          
          # Initialize result variable to avoid unbound error
            result = None  
            
            if operation == "1":
                result = add(num1, num2)
            elif operation == "2":
                result = subtract(num1, num2)
            elif operation == "3":
                result = multiply(num1, num2)
            elif operation == "4":
                result = divide(num1, num2)

            if isinstance(result, str):
                print(result)
            else:
                print(f"The result is {result:.2f}")
        
