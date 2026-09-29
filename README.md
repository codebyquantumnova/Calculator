# Calculator
A simple command-line calculator built while learning Python.





def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "You know better than to divide by zero"
    return a / b

def power(a, b):
    return a ** b


while True:
    first = float(input("First Number: "))
    operator = input("Choose + - * ^ / : ")
    second = float(input("Second Number: "))

    if operator == "+":
        result = add(first, second)
    elif operator == "-":
        result = subtract(first, second)
    elif operator == "*":
        result = multiply(first, second)
    elif operator == "/":
        result = divide(first, second)
    elif operator == "^":
        result = power(first, second)
    else:
        result = "Im not smart enough to figure this out"

    print("Result:", result)

    again = input("Another Calculation? (y/n): ")
    if again != "y":

        import tkinter as tk


        def press(symbol):
            screen.insert(tk.END, symbol)


        def clear():
            screen.delete(0, tk.END)


        def calculate():
            try:
                answer = eval(screen.get())
                clear()
                screen.insert(0, answer)
            except:
                clear()
                screen.insert(0, "Error")
