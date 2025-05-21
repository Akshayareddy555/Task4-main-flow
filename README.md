def add(x, y):
    return x + y

def subtract(x, y):
    return x - y
    
def multiply(x, y):
    return x* y
    
    def divide(x, y):
        if y == 0:
            return "Error: Division by zero is not allowed."
        return x / y
        
    def get_number(prompt):
        while True:
            try:
                return float(input(prompt))
            except ValueError:
                print("Invalid input. please enter a number.")
                
def  get_operation():
    operations = {'+': add, '-':  subtract, '*': multiply, '/':  divide}
    print("Available  operations:")
    for op in operation.keys():
        print(f" {op}")
        
    while True:
        operation = input("Enter the  operation(+, -, *, /): ")
        if operation in  operations:
            return operation[operation]
        else:
            print("Invalid operation. please enter one of +, -, *, /.")
            
def main():
    print("Simple Command-line Calculator")
    
    while True:
        num1 = get_number("Enter the firstnumber: ")
        op = get_operation()
        num2 = get_number("Enter the second number: ")
        
        result = op(num1, num2)
        print(f"Result: {result}")
        
        cont  = input("Do you want to perform another  calculation?(yes,no):").strip().lower()
        if cont not in ['yes', 'y']:
            break
        
        print("thank you for using the calculator!")
