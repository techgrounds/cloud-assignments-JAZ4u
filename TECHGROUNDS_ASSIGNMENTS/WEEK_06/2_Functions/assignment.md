# [2/ Functions]

You’ve already seen and used a couple of functions, like *print()* and *input()*. A function is a block of code that only runs when it is called. Functions are recognizable by the brackets *()* next to the function name. These brackets serve as a place to input data into a function.Functions return data as a result.

Besides the built-in functions, you can also write custom functions, or import functions from a library or package.

## Key-terms

- **print()**: The `print()` function is a built-in function used to output data to the console. It accepts zero or more arguments and prints them to the console separated by spaces by default.
  
  Example:
  
  `print("Hello, World!")`

- **input()**: The `input()` function is a built-in function used to prompt the user to enter data from the keyboard. It reads a line of input from the user as a string.
  
  Example:
  
  `name = input("Enter your name: ")`

- **Brackets ()**: In Python, parentheses () are used for various purposes, such as grouping expressions, defining function parameters, calling functions, and creating tuples.
  
  Example:
  
  `result = (2 + 3) * 4`

- **Built-in Function**: Built-in functions are functions that are pre-defined in Python and are available for use without the need for additional imports. Examples include `print()`, `input()`, `len()`, `range()`, etc.

- **Custom Function**: Custom functions, also known as user-defined functions, are functions created by the user to perform specific tasks. They are defined using the `def` keyword and can accept input parameters and return values.
  
  Example:
  
  `def greet(name):     return "Hello, " + name + "!"  print(greet("Alice"))`

- **Import Function**: In Python, you can import functions, classes, or variables from modules or packages using the `import` statement. This allows you to use functionality defined in other Python files.
  
  Example:
  
  `from math import sqrt print(sqrt(25))`

- **Library**: A library, also known as a module or module library, is a collection of pre-written code that provides specific functionalities. Libraries can contain functions, classes, constants, and variables. Examples include the `math` library, `random` library, `datetime` library, etc.

- **Package**: A package is a hierarchical directory structure that contains Python modules and other packages. It allows you to organize your code into logical groups and namespaces. Packages are used to distribute and install libraries and applications in Python.

- **Terminal**: In the context of Python, the terminal usually refers to the command-line interface where you can interact with the Python interpreter or execute Python scripts. It's also known as the command prompt, shell, or console.

- **Integer**: An integer is a whole number, positive or negative, without any decimal point. In Python, integers are a built-in numeric data type and can be represented without quotes.
  
  Example:
  
  `x = 10`

- **Argument**: An argument is a value that is passed to a function when the function is called. Functions can accept zero or more arguments. When a function is called, the arguments are assigned to the parameters defined in the function's definition.
  
  Example:
  
  `def greet(name):     print("Hello, " + name + "!")  greet("Alice")  # "Alice" is the argument passed to the function greet()`

- **Random**: The `random` module in Python provides functions for generating random numbers. It includes functions for generating random integers, floating-point numbers, and selecting random elements from sequences.
  
  Example:
  
  `import random x = random.randint(1, 100)  # Generate a random integer between 1 and 100`

- **Average**: In Python, the average is the measure of central tendency calculated by summing up a set of numbers and dividing the sum by the count of numbers. You can calculate the average of a list of numbers using the formula `(sum of numbers) / (count of numbers)`.
  
  Example:
  
  `numbers = [1, 2, 3, 4, 5] average = sum(numbers) / len(numbers)`

- **Parameter**: A parameter is a variable in a function definition. It's a placeholder that represents a value that the function expects to receive when it is called. Parameters are defined within the parentheses of the function header.
  
  Example:
  
  `def greet(name):     print("Hello, " + name + "!")`

- **Return**: The `return` statement in Python is used to exit a function and return a value or values to the caller. It's optional, and if omitted, the function returns `None` by default. A function can return one or more values separated by commas.
  
  Example:
  
  `def add(a, b):     return a + b`
  
  

- **Module**: In Python, a module is a file containing Python code. The code in a module can define functions, classes, variables, or other Python objects. Modules are used to organize Python code into logical units, making it easier to manage and reuse code.
  Modules play a crucial role in Python development by facilitating code organization, reuse, and modularity. They are an essential concept for writing maintainable and scalable Python code.

## Assignment

Exercise 1:

- Create a new script.
- Import the random package.
- Print 5 random integers with a value between 0 and 100.  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/50733c31626de82900d79da6463e2176/image4.png)

 Exercise 2:

- Create a new script.
- Write a custom function myfunction() that prints “Hello, world!” to the terminal. Call myfunction.
- Rewrite your function so that it takes a string as an argument. Then, it should print “Hello, NAME!”.  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/50733c31626de82900d79da6463e2176/image3.png)

Image label

 Exercise 3:

- Create a new script.

Copy the code below into your script.

`   def avg():   # write your code here   # you are not allowed to edit any code below here      x = 128   y = 255   z = avg(x,y)      print("The average of",x,"and",y,"is",z)   `

- Write the custom function avg() so that it returns the average of the given parameters. You are not allowed to edit any code below the second comment.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

# Result

Exercise 1:

- Create a new script.
- Import the random package.
- Print 5 random integers with a value between 0 and 100.  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/50733c31626de82900d79da6463e2176/image4.png)

```
# Import the random package
import random

# Print 5 random integers between 0 and 100
for _ in range(5):
    print(random.randint(0, 100))
```

![import_package.png](import_package.png)

This script will generate and print 5 random integers, each between 0 and 100.

 Exercise 2:

- Create a new script.
- Write a custom function myfunction() that prints “Hello, world!” to the terminal. Call myfunction.
- Rewrite your function so that it takes a string as an argument. Then, it should print “Hello, NAME!”.  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/50733c31626de82900d79da6463e2176/image3.png)

```
# Define the custom function myfunction() to print "Hello, world!"
def myfunction():
    print("Hello, world!")

# Call myfunction
myfunction()

# Modified function to take a string argument and print "Hello, NAME!"
def myfunction_with_name(name):
    print("Hello,", name + "!")

# Call myfunction_with_name with a name argument
myfunction_with_name("Jaz")
```

The first part of the script calls `myfunction()`, which prints "Hello, world!" to the terminal. The second part defines a modified function `myfunction_with_name()` that takes a string argument `name` and prints "Hello, NAME!" using the provided name. Finally, it calls `myfunction_with_name("Jaz")` as an example.

![myfunction.png](myfunction.png)

 Exercise 3:

- Create a new script.

Copy the code below into your script.

`   def avg():   # write your code here   # you are not allowed to edit any code below here      x = 128   y = 255   z = avg(x,y)      print("The average of",x,"and",y,"is",z)   `

- Write the custom function avg() so that it returns the average of the given parameters. You are not allowed to edit any code below the second comment.
  
  ```
  def avg(x, y):
      # Calculate the average of x and y
      return (x + y) / 2
  
  # you are not allowed to edit any code below here
  x = 128
  y = 255
  z = avg(x, y)
  print("The average of", x, "and", y, "is", z)
  ```
  
  In this script, the avg() function takes two parameters x and y, calculates their average (x + y) / 2, and returns the result. The rest of the code remains unchanged, as per your instructions.

![average.png](average.png)