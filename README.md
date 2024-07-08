# python
Notes for Python
Run the code on Python Interpreter: https://www.programiz.com/python-programming/online-compiler/

# Input/Output:

- **Input (using `input()`)**:
    - Allows user input during program execution.
    - **Code**:
        
        ```python
        name = input("Enter your name: ")
        age = input("Enter your age: ")
        ```
        
    - **Output** (Example):
        
        ```
        Enter your name: Alice
        Enter your age: 30
        ```
        
- **Display output (using `print()`)**:
    - Outputs data to the console.
    - **Code**:
        
        ```python
        print("Hello, World!")
        print("Name:", name, "Age:", age)
        ```
        
    - **Output** (Example):
        
        ```
        Hello, World!
        Name: Alice Age: 30
        ```
        

# Comments and Docstrings:

- **Writing comments**:
    - Comments start with `#` and provide explanations in code.
    - **Code**:
        
        ```python
        # This is a comment
        print("Hello, World!")
        ```
        
- **Creating docstrings for documentation**:
    - Docstrings are triple-quoted strings used to document functions, classes, or methods.
    - **Code**:
        
        ```python
        def greet(name):
            """
            Function to greet a person by name.
        
            Args:
                name (str): The name of the person.
        
            Returns:
                str: Greeting message.
            """
            return f"Hello, {name}!"
        
        print(greet("Alice"))
        ```
        
    - **Output** (Example):
        
        ```
        Hello, Alice!
        ```
        

**Building Blocks:**

# **Data Types**

## **Numbers**

- Integers: Whole numbers (e.g., `1`, `42`, `10`)
- Floats: Decimal numbers (e.g., `3.14`, `0.001`, `2.0`)
- Numbers in Python can be integers or floats. Integers are whole numbers, while floats have decimal points.
- Code:
    
    ```python
    # Integer example
    num_int = 42
    print(num_int)  # Output: 42
    
    # Float example
    num_float = 3.14
    print(num_float)  # Output: 3.14
    ```
    

## **Text**

- Strings: Sequences of characters (e.g., `"Hello"`, `'Python'`, `"123"`)
- Strings are used to represent text data in Python. They can be enclosed in single (`'`) or double (`"`) quotes.
- Code:
    
    ```python
    # String example
    message = "Hello, Python!"
    print(message)  # Output: Hello, Python!
    ```
    

## **Booleans**

- True/False values: Used in logical operations (`True`, `False`)
- Booleans represent truth values (`True` or `False`) and are used in logical operations and control flow.
- Code:
    
    ```python
    # Boolean example
    is_python_fun = True
    print(is_python_fun)  # Output: True
    ```
    

## None

**None:** Represents the absence of a value.

**Code:**

```python
# Example: Using None
uninitialized_var = None
print(uninitialized_var)  # Output: None
```

# **Type Conversion**

- Convert between data types:
    - `int()`: Convert to integer
    - `float()`: Convert to float
    - `str()`: Convert to string
    - `bool()`: Convert to boolean
    - Python allows conversion between different data types using built-in functions (`int()`, `float()`, `str()`, `bool()`).
    - Code:
        
        ```python
        # Type conversion examples
        num_str = "42"
        num_int = int(num_str)  # Convert string to integer
        print(num_int)  # Output: 42
        
        num_float = float(num_int)  # Convert integer to float
        print(num_float)  # Output: 42.0
        
        bool_val = bool(num_int)  # Convert integer to boolean
        print(bool_val)  # Output: True
        ```
        

# **Variables**

- Variables in Python are containers for storing data. They must follow naming rules and conventions for clarity.
- **Naming Rules:**
    - Variables must start with a letter or underscore (`_`).
    - They can contain letters, numbers, and underscores.
    - Case-sensitive (`myVar` is different from `myvar`).
- Assigning names to store data:
    - Variables hold values that can be referenced and manipulated in the program.
- Code:
    
    ```python
    # Variable assignment examples
    my_var = 10
    print(my_var)  # Output: 10
    
    message = "Hello, Python!"
    print(message)  # Output: Hello, Python!
    ```
    

# **Operators**

## **Arithmetic Operators**

- `+` (Addition), `-` (Subtraction), `*` (Multiplication), `**` (Exponentiation), `/` (Division), `//` (Integer Division), `%` (Modulo)
- Arithmetic operators perform mathematical operations on numbers.
- Code:
    
    ```python
    # Arithmetic operator examples
    num1 = 10
    num2 = 3
    
    print(num1 + num2)  # Output: 13
    print(num1 - num2)  # Output: 7
    print(num1 * num2)  # Output: 30
    print(num1 ** num2)  # Output: 1000 (Exponentiation)
    print(num1 / num2)  # Output: 3.3333333333333335
    print(num1 // num2)  # Output: 3 (Integer division)
    print(num1 % num2)  # Output: 1 (Modulo)
    ```
    

## **Logical Operators**

- `and`, `or`, `not`
- Logical operators are used to combine or negate conditions.
- Code:
    
    ```python
    # Logical operator examples
    x = True
    y = False
    
    print(x and y)  # Output: False
    print(x or y)  # Output: True
    print(not x)  # Output: False
    ```
    

## **Comparison Operators**

- `==` (Equal), `!=` (Not Equal), `<`, `>`, `<=`, `>=`
- Comparison operators compare two values and return a boolean result.
- Code:
    
    ```python
    # Comparison operator examples
    a = 10
    b = 5
    
    print(a == b)  # Output: False
    print(a != b)  # Output: True
    print(a < b)  # Output: False
    print(a > b)  # Output: True
    print(a <= b)  # Output: False
    print(a >= b)  # Output: True
    ```
    

**is Operator:** The `is` operator checks for object identity in Python. It evaluates to `True` if both operands refer to the same object in memory, regardless of their value.

**Code:**

**Python**

```python
x = 5
y = 5
z = 6

print(x is y)  # Output: True (both x and y refer to the same integer object 5 in memory)
print(x is z)  # Output: False (x and z refer to different integer objects)
```

The `is` operator is generally more reliable for custom objects or when you specifically need to check object identity.

# Controlling the Flow

## **Conditional Statements (if/else):**

- Making decisions based on conditions:
    
    ```python
    # Example: Checking if a number is positive or negative
    num = int(input("Enter a number: "))
    if num > 0:
        print("Number is positive")
    elif num == 0:
        print("Number is zero")
    else:
        print("Number is negative")
    
    ```
    
    **Output (example):**
    
    ```
    Enter a number: 5
    Number is positive
    ```
    
- Handling multiple conditions (`elif` statements):
    
    ```python
    # Example: Checking grade based on score
    score = int(input("Enter your score: "))
    if score >= 90:
        grade = 'A'
    elif score >= 80:
        grade = 'B'
    elif score >= 70:
        grade = 'C'
    else:
        grade = 'F'
    print("Your grade is:", grade)
    
    ```
    
    **Output (example):**
    
    ```
    Enter your score: 85
    Your grade is: B
    
    ```
    
- Using nested `if` statements for complex conditions:
    
    ```python
    # Example: Checking eligibility based on age and citizenship
    age = 25
    citizen = True
    if age >= 18:
        if citizen:
            print("You are eligible to vote")
        else:
            print("You must be a citizen to vote")
    else:
        print("You must be at least 18 years old to vote")
    
    ```
    
    **Output (example):**
    
    ```
    You are eligible to vote
    ```
    

## **Loops (for, while):**

- Repeating code blocks a specific number of times or until a condition is met:
    
    ```python
    # Example: Using a for loop to print numbers 1 to 5
    for i in range(1, 6):
        print(i, end=' ')
    ```
    
    **Output (example):**
    
    ```
    1 2 3 4 5
    ```
    
- Iterating over different data structures (lists, tuples, dictionaries):
    
    ```python
    # Example: Iterating over a list
    fruits = ['apple', 'banana', 'cherry']
    for fruit in fruits:
        print(fruit)
    ```
    
    **Output (example):**
    
    ```
    apple
    banana
    cherry
    ```
    
- Using `range()` function for more control in `for` loops:
    
    ```python
    # Example: Using range to print numbers in a specified range
    for num in range(5, 10, 2):
        print(num, end=' ')
    ```
    
    **Output (example):**
    
    ```
    5 7 9
    ```
    

## **Break/Continue Statements:**

- Controlling loop execution:
    
    ```python
    # Example: Using break to stop the loop early
    numbers = [1, 2, 3, 4, 5]
    for num in numbers:
        if num == 4:
            break
        print(num, end=' ')
    ```
    
    **Output (example):**
    
    ```
    1 2 3
    ```
    
- Using `else` with loops for executing code after loop completion or break:
    
    ```python
    # Example: Using else with a for loop
    numbers = [1, 2, 3, 4, 5]
    for num in numbers:
        print(num, end=' ')
    else:
        print("Loop completed successfully")
    ```
    
    **Output (example):**
    
    ```
    1 2 3 4 5 Loop completed successfully
    ```
    
- Applying `pass` statement as a placeholder in loops:
    
    ```python
    # Example: Using pass in a for loop
    numbers = [1, 2, 3, 4, 5]
    for num in numbers:
        pass  # Placeholder for future code
    ```
    
    **No Output:** `pass` does not produce any output; it is used as a placeholder.
    

# String Handling

## String Formatting and String Methods

- **`.format()`:**
    
    The `.format()` method allows inserting variables into strings in a more readable way.
    
    ```python
    # Example: Using .format() for string formatting
    name = "Alice"
    age = 30
    greeting = "My name is {} and I am {} years old.".format(name, age)
    print(greeting)
    ```
    
    **Output:**
    
    ```
    My name is Alice and I am 30 years old.
    ```
    
- **f-strings:**
    
    f-strings (formatted string literals) provide a way to embed expressions inside string literals using `{}`.
    
    ```python
    # Example: Using f-strings for string formatting
    name = "Bob"
    age = 25
    greeting = f"My name is {name} and I am {age} years old."
    print(greeting)
    ```
    
    **Output:**
    
    ```
    My name is Bob and I am 25 years old.
    ```
    
- **Common string methods:**
    - **`.upper()`:** Converts all characters to uppercase.
    - **`.lower()`:** Converts all characters to lowercase.
    - **`.strip()`:** Removes leading and trailing whitespace.
    - **`.split()`:** Splits a string into a list of substrings based on a delimiter.
    - **`.join()`:** Joins a list of strings into a single string with a specified delimiter.
    - **`.replace()`:** Replaces occurrences of a substring with another substring.
    - **`.find()`:** Finds the first occurrence of a substring and returns its index.
    
    ```python
    # Example: Using common string methods
    text = "  Hello, World!  "
    upper_text = text.upper()
    lower_text = text.lower()
    stripped_text = text.strip()
    words = text.split(',')
    joined_text = '-'.join(words)
    replaced_text = text.replace('World', 'Python')
    found_index = text.find('World')
    
    print("Uppercase:", upper_text)
    print("Lowercase:", lower_text)
    print("Stripped:", stripped_text)
    print("Split:", words)
    print("Joined:", joined_text)
    print("Replaced:", replaced_text)
    print("Found 'World' at index:", found_index)
    ```
    
    **Output:**
    
    ```
    Uppercase:   HELLO, WORLD!
    Lowercase:   hello, world!
    Stripped: Hello, World!
    Split: ['  Hello', ' World!  ']
    Joined:   Hello- World!
    Replaced:   Hello, Python!
    Found 'World' at index: 9
    ```
    

## String Manipulation

- **Concatenation:**
    
    Concatenation combines two or more strings into one.
    
    ```python
    # Example: String concatenation
    str1 = "Hello"
    str2 = "World"
    concatenated = str1 + " " + str2
    print(concatenated)
    ```
    
    **Output:**
    
    ```
    Hello World
    ```
    
- **Indexing:**
    
    Indexing accesses individual characters in a string using their position.
    
    ```python
    # Example: String indexing
    text = "Python"
    first_char = text[0]
    last_char = text[-1]
    print("First character:", first_char)
    print("Last character:", last_char)
    ```
    
    **Output:**
    
    ```
    First character: P
    Last character: n
    ```
    
- **Slicing:**
    
    Extracts a portion of a sequence from a specified range of indices, where the start index is inclusive and the end index is exclusive.
    
    **Syntax:** `text[start:end:step]`
    
    ```python
    # Example: String slicing
    text = "Hello, World!"
    sliced_text = text[7:12]
    print(sliced_text)
    ```
    
    **Output:**
    
    ```
    World
    ```
    
- **Reversing a string:**
Reverses the order of characters in a string by leveraging slicing, which allows accessing elements in reverse order (`[::-1]`).
    
    ```python
    # Example: Reversing a string
    text = "Python"
    reversed_text = text[::-1]
    print("Reversed string:", reversed_text)
    ```
    
    **Output:**
    
    ```
    Reversed string: nohtyP
    ```
    
- **Checking for substrings:**
    
    You can check if a substring exists within a string using the `in` keyword.
    
    ```python
    # Example: Checking for substrings
    text = "Hello, World!"
    has_world = "World" in text
    has_python = "Python" in text
    print("Contains 'World':", has_world)
    print("Contains 'Python':", has_python)
    ```
    
    **Output:**
    
    ```
    Contains 'World': True
    Contains 'Python': False
    ```
    

# Functions

- **Reusable blocks of code that perform specific tasks:**
    
    Functions in Python allow you to encapsulate code into reusable blocks, enhancing modularity and readability of your code.
    
- **Defining Functions:**
    - **Creating functions with arguments and return values:**
        
        Functions can accept arguments and return values using the `def` keyword.
        
        ```python
        # Example: Function to calculate the square of a number
        def square(num):
            return num ** 2
        
        result = square(5)
        print("Square of 5:", result)
        ```
        
        **Output:**
        
        ```
        Square of 5: 25
        ```
        
    - **Default arguments and keyword arguments:**
        
        Functions can have default values for arguments and accept keyword arguments for flexibility.
        
        ```python
        # Example: Function with default argument and keyword argument
        def greet(name, greeting='Hello'):
            print(f"{greeting}, {name}!")
        
        greet('Alice')  # Uses default greeting
        greet('Bob', greeting='Hi')  # Uses custom greeting
        ```
        
        **Output:**
        
        ```
        Hello, Alice!
        Hi, Bob!
        ```
        
- **Calling Functions:**
    - **Executing functions and utilizing their returned values:**
        
        Functions are called by their name followed by parentheses `()`, optionally passing arguments.
        
        ```python
        # Example: Calling a function and using its returned value
        def add(a, b):
            return a + b
        
        result = add(3, 5)
        print("Result of addition:", result)
        ```
        
        **Output:**
        
        ```
        Result of addition: 8
        ```
        
    - **Passing arguments to functions:**
        
        Functions can accept multiple arguments, passed in a comma-separated list.
        
        ```python
        # Example: Function with multiple arguments
        def greet(name, greeting):
            print(f"{greeting}, {name}!")
        
        greet('Alice', 'Hello')
        ```
        
        **Output:**
        
        ```
        Hello, Alice!
        ```
        
    - **Returning values from functions:**
        
        Functions can return values using the `return` statement.
        
        ```python
        # Example: Function to check if a number is even
        def is_even(num):
            return num % 2 == 0
        
        num = 4
        if is_even(num):
            print(f"{num} is even")
        else:
            print(f"{num} is odd")
        ```
        
        **Output:**
        
        ```
        4 is even
        ```
        
    - **Function scope and global variables:**
        
        Variables defined inside a function are scoped locally by default. Use `global` keyword to modify global variables inside functions.
        
        ```python
        # Example: Using global variables inside a function
        global_var = 10
        
        def modify_global():
            global global_var
            global_var += 5
        
        modify_global()
        print("Modified global variable:", global_var)
        ```
        
        **Output:**
        
        ```
        Modified global variable: 15
        ```
        
    - **Lambda functions (anonymous functions):**
        
        Lambda functions are small, anonymous functions defined with the `lambda` keyword.
        
        ```python
        # Example: Lambda function to calculate the square of a number
        square = lambda x: x ** 2
        
        result = square(5)
        print("Square of 5:", result)
        ```
        
        **Output:**
        
        ```
        Square of 5: 25
        ```
        
    
    - **Uses of *, **, `*args` and `**kwargs` for variable length arguments:**
        
        The asterisk (`*`) in Python has different meanings depending on where it's used:
        
        1. **As a Prefix in Function Definitions (`*args` and `**kwargs`):**
            - In function definitions, `*args` and `**kwargs` are used to handle variable numbers of arguments.
            - `*args` collects extra positional arguments as a tuple.
            - `**kwargs` collects extra keyword arguments as a dictionary.
            
            Example:
            
            ```python
            def example_func(a, b, *args, **kwargs):
                print(f"a = {a}")
                print(f"b = {b}")
                print(f"args = {args}")
                print(f"kwargs = {kwargs}")
            
            example_func(1, 2, 3, 4, x=5, y=6)
            ```
            
            Output:
            
            ```
            a = 1
            b = 2
            args = (3, 4)
            kwargs = {'x': 5, 'y': 6}
            ```
            
        2. **For Argument Unpacking in Function Calls (** * and ****):**
            - In function calls, * and ** are used to unpack iterables or dictionaries into individual arguments.
            
            Example:
            
            ```python
            def add_numbers(x, y):
                return x + y
            
            nums = (3, 5)
            result = add_numbers(*nums)
            print(result)  # Output: 8
            ```
            
        3. **In List, Tuple, and Set Definitions (Unpacking):**
            - Outside of functions, * is used to unpack elements of a list, tuple, or set.
            
            Example:
            
            ```python
            numbers = [1, 2, 3, 4]
            print(*numbers)  # Output: 1 2 3 4
            ```
            
        4. **In Dictionary Definitions (Unpacking):**
            - ** is used to unpack dictionaries.
            
            Example:
            
            ```python
            dict1 = {'a': 1, 'b': 2}
            dict2 = {'c': 3, **dict1}
            print(dict2)  # Output: {'c': 3, 'a': 1, 'b': 2}
            ```
            
    - **Special Attributes in Functions:**
        
        Python provides several special attributes that provide introspection capabilities for functions:
        
        - `__name__`: Returns the name of the function as a string.
        - `__doc__`: Returns the docstring associated with the function, if any.
        - `__module__`: Returns the name of the module where the function is defined.
        - `__defaults__`: Returns a tuple containing default argument values for positional parameters.
        - `__code__`: Returns the code object representing the compiled function body.
        - `__globals__`: Returns the dictionary representing the global namespace in which the function is defined.
        - `__dict__`: Returns the namespace supporting arbitrary function attributes.
        - `__annotations__`: Returns the annotations dictionary associated with the function's parameters and return value.
        
        These attributes can be accessed using the syntax `function_name.__attribute__` and provide useful information for debugging, introspection, and dynamic programming tasks.
        
        ### Code and Output:
        
        ```python
        # Example demonstrating special attributes in Python functions
        def example_function(x: int, y: int = 10) -> int:
            """This is a sample function."""
            print(f"Function Name: {example_function.__name__}")
            print(f"Docstring: {example_function.__doc__}")
            print(f"Module: {example_function.__module__}")
            print(f"Defaults: {example_function.__defaults__}")
            print(f"Code Object: {example_function.__code__}")
            print(f"Globals: {example_function.__globals__}")
            print(f"Namespace Dictionary: {example_function.__dict__}")
            print(f"Annotations: {example_function.__annotations__}")
            return x + y
        
        # Adding a custom attribute to the function's namespace dictionary
        example_function.custom_attr = "Custom attribute added to function"
        
        # Accessing and printing the annotations dictionary
        print(f"Annotations for example_function: {example_function.__annotations__}")
        
        print(example_function(5))
        ```
        
        ### Output:
        
        ```
        Function Name: example_function
        Docstring: This is a sample function.
        Module: __main__
        Defaults: (10,)
        Code Object: <code object example_function at 0x7f7b3028ecf0, file "example.py", line 6>
        Globals: {'__name__': '__main__', '__doc__': None, '__package__': None, '__loader__': <_frozen_importlib_external.SourceFileLoader object at 0x7f7b30a4f250>, '__spec__': None, '__annotations__': {}, '__builtins__': <module 'builtins' (built-in)>, '__file__': '/mnt/data/outputs/tmp/tmpx9td0dc1.py'}
        Namespace Dictionary: {'custom_attr': 'Custom attribute added to function'}
        Annotations: {'x': <class 'int'>, 'y': <class 'int'>, 'return': <class 'int'>}
        Annotations for example_function: {'x': <class 'int'>, 'y': <class 'int'>, 'return': <class 'int'>}
        Calling function: example_function
        Function example_function returned: 15
        15
        ```
        

# Basic Data Structures

## Lists

- **Creating lists:**
    
    Lists are ordered collections of items.
    
    ```python
    # Example: Creating a list
    fruits = ["apple", "banana", "cherry"]
    print(fruits)
    ```
    
    **Output:**
    
    ```
    ['apple', 'banana', 'cherry']
    ```
    
- **Accessing elements:**
    
    Elements in a list can be accessed using their index and index starts with 0.
    
    ```python
    # Example: Accessing elements
    fruits = ["apple", "banana", "cherry"]
    print(fruits[1])
    ```
    
    **Output:**
    
    ```
    banana
    ```
    
- **Modifying elements:**
    
    Elements in a list can be modified by assigning new values to specific indices.
    
    ```python
    # Example: Modifying elements
    fruits = ["apple", "banana", "cherry"]
    fruits[1] = "blueberry"
    print(fruits)
    ```
    
    **Output:**
    
    ```
    ['apple', 'blueberry', 'cherry']
    ```
    
- **Adding elements (`append()`, `insert()`):**
    
    ```python
    # Example: Adding elements
    fruits = ["apple", "banana", "cherry"]
    fruits.append("date")
    fruits.insert(1, "blueberry")
    print(fruits)
    ```
    
    **Output:**
    
    ```
    ['apple', 'blueberry', 'banana', 'cherry', 'date']
    ```
    
- **Removing elements (`remove()`, `pop()`):**
    
    ```python
    # Example: Removing elements
    fruits = ["apple", "banana", "cherry"]
    fruits.remove("banana")
    popped = fruits.pop(1)
    print(fruits)
    print("Popped element:", popped)
    ```
    
    **Output:**
    
    ```
    ['apple', 'cherry']
    Popped element: cherry
    ```
    
- **Slicing lists:**
    
    Slicing extracts parts of a list.
    
    ```python
    # Example: Slicing a list
    fruits = ["apple", "banana", "cherry", "date"]
    sliced_fruits = fruits[1:3]
    print(sliced_fruits)
    ```
    
    **Output:**
    
    ```
    ['banana', 'cherry']
    ```
    
- **List methods (`sort()`, `reverse()`):**
    
    ```python
    # Example: List methods
    fruits = ["cherry", "banana", "apple"]
    fruits.sort()
    print("Sorted:", fruits)
    fruits.reverse()
    print("Reversed:", fruits)
    ```
    
    **Output:**
    
    ```
    Sorted: ['apple', 'banana', 'cherry']
    Reversed: ['cherry', 'banana', 'apple']
    ```
    

## Tuples

- **Creating tuples:**
    
    Tuples are immutable ordered collections of items.
    
    ```python
    # Example: Creating a tuple
    coordinates = (10, 20, 30)
    print(coordinates)
    ```
    
    **Output:**
    
    ```
    (10, 20, 30)
    ```
    
- **Accessing elements:**
    
    ```python
    # Example: Accessing elements in a tuple
    coordinates = (10, 20, 30)
    print(coordinates[1])
    ```
    
    **Output:**
    
    ```
    20
    ```
    
- **Tuple immutability:**
    
    Tuples cannot be modified after creation.
    
    ```python
    # Example: Tuple immutability
    coordinates = (10, 20, 30)
    # coordinates[1] = 25  # This will raise an error
    ```
    

## Dictionaries

- **Creating dictionaries:**
    
    Dictionaries are collections of key-value pairs.
    
    ```python
    # Example: Creating a dictionary
    student = {"name": "John", "age": 20, "grade": "A"}
    print(student)
    ```
    
    **Output:**
    
    ```
    {'name': 'John', 'age': 20, 'grade': 'A'}
    ```
    
- **Accessing values:**
    
    Values can be accessed using their keys.
    
    ```python
    # Example: Accessing values
    student = {"name": "John", "age": 20, "grade": "A"}
    print(student["name"])
    ```
    
    **Output:**
    
    ```
    John
    ```
    
- **Adding/Modifying entries:**
    
    ```python
    # Example: Adding/Modifying entries
    student = {"name": "John", "age": 20}
    student["grade"] = "A"
    student["age"] = 21
    print(student)
    ```
    
    **Output:**
    
    ```
    {'name': 'John', 'age': 21, 'grade': 'A'}
    ```
    
- **Removing entries (`del`, `pop()`):**
    
    ```python
    # Example: Removing entries
    student = {"name": "John", "age": 20, "grade": "A"}
    del student["age"]
    grade = student.pop("grade")
    print(student)
    print("Popped grade:", grade)
    ```
    
    **Output:**
    
    ```
    {'name': 'John'}
    Popped grade: A
    ```
    
- **Dictionary methods (`keys()`, `values()`, `items()`):**
    
    ```python
    # Example: Dictionary methods
    student = {"name": "John", "age": 20, "grade": "A"}
    print("Keys:", student.keys())
    print("Values:", student.values())
    print("Items:", student.items())
    ```
    
    **Output:**
    
    ```
    Keys: dict_keys(['name', 'age', 'grade'])
    Values: dict_values(['John', 20, 'A'])
    Items: dict_items([('name', 'John'), ('age', 20), ('grade', 'A')])
    ```
    

## Sets

- **Creating sets:**
    
    Sets are collections of unique elements.
    
    ```python
    # Example: Creating a set
    colors = {"red", "green", "blue"}
    print(colors)
    ```
    
    **Output:**
    
    ```
    {'red', 'green', 'blue'}
    ```
    
- **Adding elements (`add()`):**
    
    ```python
    # Example: Adding elements
    colors = {"red", "green"}
    colors.add("blue")
    print(colors)
    ```
    
    **Output:**
    
    ```
    {'red', 'green', 'blue'}
    ```
    
- **Removing elements (`remove()`, `discard()`):**
    
    ```python
    # Example: Removing elements
    colors = {"red", "green", "blue"}
    colors.remove("green")
    colors.discard("yellow")  # No error if element does not exist
    print(colors)
    ```
    
    **Output:**
    
    ```
    {'red', 'blue'}
    ```
    
- **Set operations (union, intersection, difference):**
    
    ```python
    # Example: Set operations
    set1 = {"a", "b", "c"}
    set2 = {"b", "c", "d"}
    union = set1.union(set2)
    intersection = set1.intersection(set2)
    difference = set1.difference(set2)
    
    print("Union:", union)
    print("Intersection:", intersection)
    print("Difference:", difference)
    
    ```
    
    **Output:**
    
    ```
    Union: {'a', 'b', 'c', 'd'}
    Intersection: {'b', 'c'}
    Difference: {'a'}
    ```
    

## List Comprehensions

- **Creating lists using comprehensions:**
    
    List comprehensions provide a concise way to create lists.
    
    ```python
    # Example: List comprehensions
    squares = [x**2 for x in range(5)]
    print(squares)
    ```
    
    **Output:**
    
    ```
    [0, 1, 4, 9, 16]
    ```
    

## Dictionary Comprehensions

- **Creating dictionaries using comprehensions:**
    
    Dictionary comprehensions provide a concise way to create dictionaries.
    
    ```python
    # Example: Dictionary comprehensions
    square_dict = {x: x**2 for x in range(5)}
    print(square_dict)
    ```
    
    **Output:**
    
    ```
    {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
    ```
    

# Error Handling

## Basic try-except

The `try-except` block is used to handle exceptions. Code inside the `try` block is executed, and if an exception occurs, the code inside the `except` block is executed.

```python
# Example: Basic try-except
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

**Output:**

```
Cannot divide by zero
```

## Catching Specific Exceptions

You can catch specific exceptions by specifying the exception type after the `except` keyword.

```python
# Example: Catching specific exceptions
try:
    result = int("not_a_number")
except ValueError:
    print("Invalid number")
```

**Output:**

```
Invalid number
```

## Using `else` and `finally` Blocks

The `else` block is executed if no exceptions are raised, and the `finally` block is executed regardless of whether an exception was raised or not.

```python
# Example: Using else and finally blocks
try:
    result = 10 / 2
except ZeroDivisionError:
    print("Cannot divide by zero")
else:
    print("Result is:", result)
finally:
    print("This will always be executed")
```

**Output:**

```
Result is: 5.0
This will always be executed
```

## Raising Exceptions

You can raise exceptions using the `raise` keyword.

```python
# Example: Raising exceptions
try:
    raise ValueError("An error occurred")
except ValueError as e:
    print("Caught an exception:", e)
```

**Output:**

```
Caught an exception: An error occurred
```

# Object-Oriented Programming (OOP):

## Classes

**Theory:**
A class is a blueprint for creating objects (instances) that share attributes and methods. It allows you to organize and structure code into reusable components.

**Code:**

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"{self.year} {self.make} {self.model}")

# Creating an instance of Car
my_car = Car("Toyota", "Camry", 2022)
my_car.display_info()  # Output: 2022 Toyota Camry
```

## Objects

**Theory:**
Objects are instances of classes. Each object has its own identity, attributes, and methods.

**Code:**

```python
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        print(f"{self.name} says Woof!")

# Creating instances of Dog class
dog1 = Dog("Buddy", "Golden Retriever")
dog2 = Dog("Max", "Labrador")

dog1.bark()  # Output: Buddy says Woof!
dog2.bark()  # Output: Max says Woof!
```

## Inheritance

**Theory:**
Inheritance allows a class (subclass) to inherit attributes and methods from another class (superclass). It promotes code reuse and supports the "is-a" relationship.

**Code:**

```python
class Animal:
    def speak(self):
        pass  # Abstract method

class Dog(Animal):
    def speak(self):
        print("Woof!")

class Cat(Animal):
    def speak(self):
        print("Meow!")

# Using inheritance
dog = Dog()
cat = Cat()

dog.speak()  # Output: Woof!
cat.speak()  # Output: Meow!
```

## Polymorphism

**Theory:**
Polymorphism refers to the ability of objects to be treated as instances of their parent class or any subclass. It allows for flexible and dynamic method invocation.

**Code:**

```python
class Shape:
    def area(self):
        pass  # Abstract method

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

# Polymorphic function
def print_area(shape):
    print(f"Area: {shape.area()}")

# Using polymorphism
rectangle = Rectangle(5, 4)
circle = Circle(3)

print_area(rectangle)  # Output: Area: 20
print_area(circle)     # Output: Area: 28.26
```

## Encapsulation

**Theory:**
Encapsulation involves bundling the data (attributes) and methods that operate on the data within a single unit (class). It protects the internal state of an object and hides implementation details.

**Code:**

```python
class BankAccount:
    def __init__(self, account_number, balance):
        self.__account_number = account_number  # Private attribute
        self.__balance = balance                # Private attribute

    def deposit(self, amount):
        self.__balance += amount

    def withdraw(self, amount):
        if amount <= self.__balance:
            self.__balance -= amount
        else:
            print("Insufficient funds")

    def get_balance(self):
        return self.__balance

# Using encapsulation
account = BankAccount("12345", 1000)
account.deposit(500)
account.withdraw(200)
print("Current balance:", account.get_balance())  # Output: Current balance: 1300
```

# Modules and Packages

## Leveraging pre-written code for common functionalities

Python's standard library provides a wealth of modules and packages that allow you to perform many tasks without writing the code from scratch.

- **Using built-in modules:** Built-in modules provide various functionalities that can be leveraged without writing the code from scratch.
    
    ```python
    import math
    
    # Using math module to calculate square root and factorial
    print("Square root of 16:", math.sqrt(16))
    print("Factorial of 5:", math.factorial(5))
    ```
    
    **Output:**
    
    ```
    Square root of 16: 4.0
    Factorial of 5: 120
    ```
    
- **Creating and using custom modules:** You can create your own modules by saving functions and variables in a `.py` file and then importing it.
    - `mymodule.py` (custom module):
        
        ```python
        def greet(name):
            return f"Hello, {name}!"
        ```
        
    - Using the custom module:
        
        ```python
        import mymodule
        
        print(mymodule.greet("Alice"))
        ```
        
    
    **Output:**
    
    ```
    Hello, Alice!
    ```
    
- **Different ways to import:** You can import modules in various ways depending on your needs.
    
    ```python
    # Importing the entire module
    import math
    print("Pi:", math.pi)
    
    # Importing specific functions from a module
    from math import sqrt, factorial
    print("Square root of 9:", sqrt(9))
    print("Factorial of 6:", factorial(6))
    
    # Importing a module with an alias
    import math as m
    print("Cosine of 0:", m.cos(0))
    ```
    
    **Output:**
    
    ```
    Pi: 3.141592653589793
    Square root of 9: 3.0
    Factorial of 6: 720
    Cosine of 0: 1.0
    ```
    
- **Understanding module search path:** Python looks for modules in a specific order, which can be checked using the `sys` module.
    
    ```python
    import sys
    
    print("Module search path:")
    for path in sys.path:
        print(path)
    ```
    
    **Output:**
    
    ```
    Module search path:
    /path/to/your/script
    /usr/lib/python38.zip
    /usr/lib/python3.8
    /usr/lib/python3.8/lib-dynload
    /usr/local/lib/python3.8/dist-packages
    /usr/lib/python3/dist-packages
    ```
    

## Importing Modules

### `math` Module

**Theory:** The `math` module provides mathematical functions like square root, trigonometric functions, logarithms, etc.

**Code:**

```python
import math

print(math.sqrt(16))  # Calculate the square root
print(math.pi)        # Access the value of pi
print(math.sin(math.pi / 2))  # Calculate the sine of 90 degrees
```

**Output:**

```
4.0
3.141592653589793
1.0
```

### `os` Module

**Theory:** The `os` module provides functions to interact with the operating system, like reading or writing to the file system.

**Code:**

```python
import os

print(os.name)        # Name of the operating system
print(os.getcwd())    # Current working directory
os.mkdir('test_dir')  # Create a new directory
os.rmdir('test_dir')  # Remove the directory

```

**Output:**

```
posix
/home/user
```

### `sys` Module

**Theory:** The `sys` module provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter.

**Code:**

```python
import sys

print("Python version:", sys.version)
print("Platform:", sys.platform)
```

**Output:**

```
Python version: 3.8.10 (default, Jun  4 2021, 15:09:15)
[GCC 7.5.0]
Platform: linux
```

### `datetime` Module

**Theory:** The `datetime` module supplies classes for manipulating dates and times.

**Code:**

```python
from datetime import datetime

now = datetime.now()
print("Current date and time:", now)
print("Year:", now.year)
print("Month:", now.month)
print("Day:", now.day)
```

**Output:**

```
Current date and time: 2024-07-06 12:34:56.789012
Year: 2024
Month: 7
Day: 6
```

### `random` Module

**Theory:** The `random` module implements pseudo-random number generators for various distributions.

**Code:**

```python
import random

print("Random integer between 1 and 10:", random.randint(1, 10))
print("Random float between 0 and 1:", random.random())
print("Random choice from a list:", random.choice(['apple', 'banana', 'cherry']))
```

**Output:**

```
Random integer between 1 and 10: 7
Random float between 0 and 1: 0.6213178199161644
Random choice from a list: banana
```

### `re` Module

**Theory:** The `re` module provides regular expression matching operations.

**Code:**

```python
import re

pattern = r'\\d+'
text = "There are 123 apples and 456 oranges."
matches = re.findall(pattern, text)
print("Found numbers:", matches)
```

**Output:**

```
Found numbers: ['123', '456']
```

### `json` Module

**Theory:** The `json` module parses JSON strings and converts them to Python objects, and vice versa.

**Code:**

```python
import json

data = {'name': 'John', 'age': 30, 'city': 'New York'}
json_data = json.dumps(data)
print("JSON string:", json_data)

parsed_data = json.loads(json_data)
print("Parsed data:", parsed_data)
```

**Output:**

```
JSON string: {"name": "John", "age": 30, "city": "New York"}
Parsed data: {'name': 'John', 'age': 30, 'city': 'New York'}
```

### `collections` Module

**Theory:** The `collections` module implements specialized container datatypes providing alternatives to Python’s general-purpose built-in containers like `dict`, `list`, `set`, and `tuple`.

**Code:**

```python
from collections import Counter

data = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple']
counter = Counter(data)
print("Item counts:", counter)
```

**Output:**

```
Item counts: Counter({'apple': 3, 'banana': 2, 'orange': 1})
```

### `itertools` Module

**Theory:** The `itertools` module provides functions that create iterators for efficient looping.

**Code:**

```python
import itertools

numbers = [1, 2, 3]
permutations = list(itertools.permutations(numbers))
print("Permutations of [1, 2, 3]:", permutations)
```

**Output:**

```
Permutations of [1, 2, 3]: [(1, 2, 3), (1, 3, 2), (2, 1, 3), (2, 3, 1), (3, 1, 2), (3, 2, 1)]
```

### `pathlib` Module

**Theory:** The `pathlib` module offers a set of classes to handle filesystem paths with semantics appropriate for different operating systems.

**Code:**

```python
from pathlib import Path

path = Path('/usr/bin/python')
print("Is the path a file?", path.is_file())
print("Is the path a directory?", path.is_dir())
```

**Output:**

```
Is the path a file? True
Is the path a directory? False
```

# Iterators and Generators

## Creating and Using Iterators

**Theory:**

- Iterators are objects that can be iterated upon. An iterator object implements two methods, `__iter__()` and `__next__()`.
- The `__iter__()` method returns the iterator object itself and is implicitly called at the start of loops.
- The `__next__()` method returns the next value from the iterator and is implicitly called at each loop increment. When there are no more items to return, it raises a `StopIteration` exception.

**Code:**

```python
# Creating an iterator
class MyIterator:
    def __init__(self, max):
        self.max = max
        self.current = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.current < self.max:
            self.current += 1
            return self.current
        else:
            raise StopIteration

# Using the iterator
my_iter = MyIterator(5)
for number in my_iter:
    print(number)
```

**Output:**

```
1
2
3
4
5
```

## Using Generators for Lazy Evaluation

**Theory:**

- Generators are a simple way to create iterators using a function with the `yield` statement.
- Each time `yield` is called, the generator function is paused and the value is returned to the caller. When `next()` is called again, the generator resumes execution after the `yield` statement.

**Code:**

```python
# Generator function
def my_generator(max):
    current = 0
    while current < max:
        current += 1
        yield current

# Using the generator
gen = my_generator(5)
for number in gen:
    print(number)
```

**Output:**

```
1
2
3
4
5
```

## Generator Expressions

**Theory:**

- Generator expressions are a concise way to create generators. They are similar to list comprehensions but use parentheses instead of square brackets.

**Code:**

```python
# Generator expression
gen_exp = (x * x for x in range(5))

# Using the generator expression
for value in gen_exp:
    print(value)
```

**Output:**

```
0
1
4
9
16
```

## Infinite Generators

**Theory:**

- Generators can be used to create infinite sequences. Care should be taken to stop the iteration at some point to prevent an infinite loop.

**Code:**

```python
# Infinite generator
def infinite_generator():
    current = 0
    while True:
        yield current
        current += 1

# Using the infinite generator
gen = infinite_generator()
for i in range(5):
    print(next(gen))
```

**Output:**

```
0
1
2
3
4
```

# Decorators

## Understanding and Using Function Decorators

**Theory:**

- Decorators are functions that modify the behavior of other functions or methods. They are powerful tools for adding functionality to existing functions without modifying their code directly.
- Decorators are implemented using the `@decorator_name` syntax above the function definition, where `decorator_name` is the decorator function.
- Decorator functions typically take a function as an argument, modify or enhance its behavior, and return the modified function or another callable.

**Code:**

```python
# Decorator function
def my_decorator(func):
    def wrapper():
        print("Before calling the function")
        func()
        print("After calling the function")
    return wrapper

# Function to be decorated
@my_decorator
def say_hello():
    print("Hello, world!")

# Calling the decorated function
say_hello()
```

**Output:**

```
Before calling the function
Hello, world!
After calling the function
```

## Use Case: Logging Decorator

**Theory:**

- A practical use of decorators is to add logging capabilities to functions, providing insight into their execution without modifying their core functionality.

**Code:**

```python
# Decorator for logging function calls
def log_function_call(func):
    def wrapper(*args, **kwargs):
        print(f"Calling function: {func.__name__}")
        result = func(*args, **kwargs)
        print(f"Function {func.__name__} returned: {result}")
        return result
    return wrapper

# Function decorated with logging
@log_function_call
def add_numbers(a, b):
    return a + b

# Calling the decorated function
result = add_numbers(3, 5)
print("Result:", result)
```

**Output:**

```
Calling function: add_numbers
Function add_numbers returned: 8
Result: 8
```

# Context Managers

## Using `with` Statements to Manage Resources

**Theory:**

- Context managers in Python provide a way to manage resources (like files, database connections, etc.) in a way that ensures they are properly initialized and cleaned up.
- They are implemented using special methods `__enter__()` and `__exit__()` in a class, or by using the `contextlib.contextmanager` decorator with a generator function.

**Code:**

```python
# Example of a context manager using class
class MyFileManager:
    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode

    def __enter__(self):
        self.file = open(self.filename, self.mode)
        return self.file

    def __exit__(self, exc_type, exc_value, traceback):
        self.file.close()

# Using the context manager with 'with' statement
with MyFileManager('example.txt', 'w') as file:
    file.write('Hello, context managers!')

# Example of a context manager using contextlib.contextmanager decorator
from contextlib import contextmanager

@contextmanager
def timer():
    import time
    start_time = time.time()
    yield
    end_time = time.time()
    print(f"Execution time: {end_time - start_time} seconds")

# Using the context manager with 'with' statement
with timer():
    print("Simulating some task...")
    time.sleep(2)
    print("Task completed.")
```

**Output:**

```
Execution time: 2.0 seconds
```

# File Handling

## **Reading from Files**

File handling in Python involves interacting with files stored on the disk. The `open()` function is used to open a file in various modes (`'r'` for reading, `'w'` for writing, `'a'` for appending, `'r+'` for both reading and writing). Once opened, you can read the entire content at once (`read()`), read line by line (`readline()`), or read all lines into a list (`readlines()`). Always close files after use to release system resources, or use a `with` statement for automatic cleanup.

**Opening and Reading from a File:**

```python
# Opening and reading from a file
file_path = 'sample.txt'
with open(file_path, 'r') as file:
    content = file.read()
    print("File content:")
    print(content)
```

**Output (sample.txt):**

```
This is a sample text file.
It contains multiple lines of text.
```

**Reading Line by Line:**

```python
# Reading file line by line
file_path = 'sample.txt'
with open(file_path, 'r') as file:
    line = file.readline()
    while line:
        print("Line read:")
        print(line.strip())  # strip() removes newline characters
        line = file.readline()
```

**Output (sample.txt):**

```
Line read:
This is a sample text file.
Line read:
It contains multiple lines of text.
```

**Reading All Lines into a List:**

```python
# Reading all lines into a list
file_path = 'sample.txt'
with open(file_path, 'r') as file:
    lines = file.readlines()
    print("Lines read:")
    for line in lines:
        print(line.strip())
```

**Output (sample.txt):**

```
Lines read:
This is a sample text file.
It contains multiple lines of text.
```

## Writing to Files

To write to a file, open it in `'w'` mode for writing (creates a new file or overwrites an existing one). Use the `write()` method to add content. `'a'` mode appends content to the end of an existing file without truncating it. Always close files after writing to ensure data is saved properly.

**Writing to a File:**

```python
# Writing to a file
file_path = 'output.txt'
with open(file_path, 'w') as file:
    file.write("This is the first line.\\n")
    file.write("This is the second line.\\n")
    file.write("This is the third line.\\n")
```

**Output (output.txt):**

```
This is the first line.
This is the second line.
This is the third line.
```

**Appending to a File:**

```python
# Appending to a file
file_path = 'output.txt'
with open(file_path, 'a') as file:
    file.write("Appending a new line.\\n")
```

**Updated Output (output.txt):**

```
This is the first line.
This is the second line.
This is the third line.
Appending a new line.
```

## Working with CSV Files

CSV (Comma Separated Values) files are used to store tabular data. Python's `csv` module simplifies reading and writing CSV files. `DictReader` reads CSV data into Python dictionaries, making it easy to access columns by their header names. `DictWriter` writes data from lists or dictionaries back into CSV format.

**Reading from a CSV File:**

Assume `data.csv` contains:

```
Name,Age,City
John,30,New York
Alice,25,San Francisco
```

```python
import csv

# Reading from a CSV file
csv_file = 'data.csv'
with open(csv_file, 'r', newline='') as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row['Name'], row['Age'], row['City'])
```

**Output:**

```
John 30 New York
Alice 25 San Francisco
```

**Writing to a CSV File:**

```python
# Writing to a CSV file
csv_file = 'output.csv'
data = [
    {'Name': 'Tom', 'Age': 35, 'City': 'Chicago'},
    {'Name': 'Emma', 'Age': 28, 'City': 'Seattle'}
]

with open(csv_file, 'w', newline='') as file:
    fieldnames = ['Name', 'Age', 'City']
    writer = csv.DictWriter(file, fieldnames=fieldnames)
    writer.writeheader()
    writer.writerows(data)
```

**Output (output.csv):**

```
Name,Age,City
Tom,35,Chicago
Emma,28,Seattle
```

## Working with JSON Files

JSON (JavaScript Object Notation) is a lightweight data-interchange format. Python's `json` module provides functions for parsing JSON data from files (`load()`, `loads()`), and converting Python objects into JSON (`dump()`, `dumps()`). This format is widely used for data exchange between applications.

**Reading from a JSON File:**

Assume `data.json` contains:

```json
{
    "name": "John",
    "age": 30,
    "city": "New York"
}
```

```python
import json

# Reading from a JSON file
json_file = 'data.json'
with open(json_file, 'r') as file:
    data = json.load(file)
    print("JSON Data:")
    print(data)
```

**Output:**

```python
{'name': 'John', 'age': 30, 'city': 'New York'}
```

**Writing to a JSON File:**

```python
# Writing to a JSON file
json_data = {
    'name': 'Alice',
    'age': 25,
    'city': 'San Francisco'
}

json_file = 'output.json'
with open(json_file, 'w') as file:
    json.dump(json_data, file, indent=4)
```

**Output (output.json):**

```json
{
    "name": "Alice",
    "age": 25,
    "city": "San Francisco"
}
```

# Regular Expressions

## Reading Regular Expressions:

Reading regular expressions involves understanding how different symbols and sequences of characters define patterns:

- **Literals**: Characters that match themselves.
- **Metacharacters**: Special characters with predefined meanings (`.` for any character, `\\d` for digit, etc.).
- **Character classes**: `[...]` matches any character within the brackets.
- **Anchors**: `^` matches the start of a string, `$` matches the end.
- **Quantifiers**: `*` for zero or more, `+` for one or more, `?` for zero or one.
- **Grouping**: `()` for grouping parts of the pattern.
- **Escaping**: `\\` to escape special characters.

Regular expressions are indispensable for tasks such as data validation, text parsing, and string manipulation where complex patterns need to be identified and processed efficiently.

## **Pattern matching and text manipulation**

Regular expressions (regex) are powerful tools for pattern matching and text manipulation. They provide a concise and flexible means to match strings of text, such as particular characters, words, or patterns of characters. In Python, the `re` module provides support for working with regular expressions.

Basic components include:

- **Literals**: Normal characters that match themselves (e.g., `a`, `123`).
- **Metacharacters**: Special characters with predefined meanings (e.g., `.` matches any character, `\\d` matches any digit, `\\w` matches any alphanumeric character, `\\s` matches any whitespace character).
- **Character classes**: `[...]` matches any single character within the brackets (e.g., `[aeiou]` matches any vowel).
- **Anchors**: `^` matches the start of a string, `$` matches the end.
- **Quantifiers**: `` matches zero or more occurrences, `+` matches one or more, `?` matches zero or one.
- **Grouping and capturing**: `()` for grouping and capturing substrings.
- **Escaping**: `\\` to escape special characters that you want to match literally.

**Matching a Simple Pattern:**

```python
import re

# Example: Match a simple pattern (finding digits in a string)
text = "The price is $1000."
pattern = r'\\d+'  # \\d+ matches one or more digits
matches = re.findall(pattern, text)
print(matches)  # Output: ['1000']
```

**Output:**

```
['1000']
```

**Using Character Classes:**

```python
# Example: Matching a specific character class (finding vowels)
text = "Hello World!"
pattern = r'[aeiou]'  # [aeiou] matches any vowel
matches = re.findall(pattern, text, re.IGNORECASE)  # Case insensitive matching
print(matches)  # Output: ['e', 'o', 'o']
```

**Output:**

```
['e', 'o', 'o']
```

**Anchors and Quantifiers:**

```python
# Example: Using anchors (^ and $) and quantifiers (*)
text = "Python is 20 years old"
pattern = r'^\\w+\\s\\w+\\s\\d+'  # ^\\w+\\s\\w+\\s\\d+ matches "Python is 20"
match = re.search(pattern, text)
if match:
    print("Match found:", match.group())  # Output: Python is 20
else:
    print("No match found")
```

**Output:**

```
Match found: Python is 20
```

# Libraries

## NumPy: Numerical Computing

### Arrays

**Creation**

- **Creating arrays from lists:**
    - Arrays can be created directly from Python lists using `np.array()`.
    
    ```python
    import numpy as np
    
    my_list = [1, 2, 3, 4, 5]
    arr = np.array(my_list)
    
    print(arr)
    
    ```
    
    **Output:**
    
    ```
    [1 2 3 4 5]
    
    ```
    
- **Initializing arrays (`zeros()`, `ones()`, `empty()`, etc.):**
    - Arrays can be initialized with zeros, ones, or empty values using `np.zeros()`, `np.ones()`, `np.empty()`.
    
    ```python
    import numpy as np
    
    zeros_arr = np.zeros((3, 4))  # 3x4 array of zeros
    ones_arr = np.ones((2, 3))    # 2x3 array of ones
    empty_arr = np.empty((2, 2))  # 2x2 array of empty values
    
    print("Zeros Array:")
    print(zeros_arr)
    print("\\nOnes Array:")
    print(ones_arr)
    print("\\nEmpty Array:")
    print(empty_arr)
    
    ```
    
    **Output:**
    
    ```
    Zeros Array:
    [[0. 0. 0. 0.]
     [0. 0. 0. 0.]
     [0. 0. 0. 0.]]
    
    Ones Array:
    [[1. 1. 1.]
     [1. 1. 1.]]
    
    Empty Array:
    [[4.94e-324 9.88e-324]
     [1.48e-323 1.98e-323]]
    
    ```
    
- **Generating arrays (`arange()`, `linspace()`):**
    - Arrays can be generated using `np.arange()` for sequences of numbers and `np.linspace()` for evenly spaced numbers over a specified interval.
    
    ```python
    import numpy as np
    
    arr_range = np.arange(0, 10, 2)      # Array from 0 to 10 with step 2
    arr_linspace = np.linspace(0, 5, 10) # 10 values from 0 to 5 inclusive
    
    print("Array using arange:")
    print(arr_range)
    print("Array using linspace:")
    print(arr_linspace)
    
    ```
    
    **Output:**
    
    ```
    Array using arange:
    [0 2 4 6 8]
    
    Array using linspace:
    [0.         0.55555556 1.11111111 1.66666667 2.22222222 2.77777778
     3.33333333 3.88888889 4.44444444 5.        ]
    ```
    

Certainly! Let's continue with the notes for indexing and slicing arrays in NumPy:

---

## Arrays

### Indexing and Slicing

- **Accessing elements and subarrays:**
    - Individual elements of a NumPy array can be accessed using indexing, similar to Python lists. Array indexing starts at 0.
    
    ```python
    import numpy as np
    
    arr = np.array([1, 2, 3, 4, 5])
    
    # Accessing elements
    print("Element at index 0:", arr[0])   # 1
    print("Element at index 3:", arr[3])   # 4
    
    # Accessing subarrays
    sub_arr = arr[1:4]  # Elements from index 1 to 3 (exclusive of 4)
    print("Subarray:", sub_arr)           # [2 3 4]
    
    ```
    
    **Output:**
    
    ```
    Element at index 0: 1
    Element at index 3: 4
    Subarray: [2 3 4]
    
    ```
    
- **Slicing arrays (single-dimensional and multi-dimensional):**
    - Slicing allows accessing portions of arrays efficiently. For multi-dimensional arrays, slicing is done on each axis.
    
    ```python
    import numpy as np
    
    # Single-dimensional array
    arr1d = np.array([1, 2, 3, 4, 5])
    
    # Multi-dimensional array
    arr2d = np.array([[1, 2, 3],
                      [4, 5, 6],
                      [7, 8, 9]])
    
    # Single-dimensional array slicing
    print("First three elements:", arr1d[:3])  # [1 2 3]
    
    # Multi-dimensional array slicing
    print("First two rows, first two columns:")
    print(arr2d[:2, :2])
    
    ```
    
    **Output:**
    
    ```
    First three elements: [1 2 3]
    
    First two rows, first two columns:
    [[1 2]
     [4 5]]
    
    ```
    
- **Note:** In slicing, the colon (`:`) indicates all elements along that axis. The syntax `start:stop:step` can also be used for more precise slicing.

---

These notes cover the basics of indexing and slicing NumPy arrays, both for single-dimensional and multi-dimensional arrays. Let me know if there's anything else you'd like to add or if you're ready to move on to the next set of topics!

### Array Operations

Certainly! Let's proceed with the notes on mathematical operations for NumPy arrays:

---

## Arrays

### Mathematical Operations

- **Element-wise operations (`+`, ``, ``, `/`, `*`, etc.):**
    - NumPy arrays support element-wise operations, where corresponding elements of arrays are operated upon.
    
    ```python
    import numpy as np
    
    arr1 = np.array([1, 2, 3, 4])
    arr2 = np.array([5, 6, 7, 8])
    
    # Addition
    add_result = arr1 + arr2
    print("Addition:", add_result)  # [ 6  8 10 12]
    
    # Subtraction
    sub_result = arr2 - arr1
    print("Subtraction:", sub_result)  # [4 4 4 4]
    
    # Multiplication
    mul_result = arr1 * arr2
    print("Multiplication:", mul_result)  # [ 5 12 21 32]
    
    # Division
    div_result = arr2 / arr1
    print("Division:", div_result)  # [5.  3.  2.33 2.]
    
    # Exponentiation
    exp_result = arr1 ** 2
    print("Exponentiation:", exp_result)  # [ 1  4  9 16]
    
    ```
    
    **Output:**
    
    ```
    Addition: [ 6  8 10 12]
    Subtraction: [4 4 4 4]
    Multiplication: [ 5 12 21 32]
    Division: [5.   3.   2.33 2.  ]
    Exponentiation: [ 1  4  9 16]
    
    ```
    
- **Matrix multiplication (`@` operator or `np.dot()`):**
    - Matrix multiplication in NumPy can be performed using the `@` operator or `np.dot()` function for arrays of appropriate shapes.
    
    ```python
    import numpy as np
    
    arr1 = np.array([[1, 2],
                     [3, 4]])
    arr2 = np.array([[5, 6],
                     [7, 8]])
    
    # Matrix multiplication using @ operator
    matmul_result1 = arr1 @ arr2
    print("Matrix Multiplication (@ operator):\\n", matmul_result1)
    
    # Matrix multiplication using np.dot()
    matmul_result2 = np.dot(arr1, arr2)
    print("\\nMatrix Multiplication (np.dot()):\\n", matmul_result2)
    
    ```
    
    **Output:**
    
    ```
    Matrix Multiplication (@ operator):
    [[19 22]
     [43 50]]
    
    Matrix Multiplication (np.dot()):
    [[19 22]
     [43 50]]
    
    ```
    

---

These notes cover the basics of performing element-wise operations and matrix multiplication using NumPy arrays. Let me know if there's anything else you'd like to add or if you're ready to continue with the next topics!

Certainly! Let's continue with the notes for aggregation functions and boolean indexing in NumPy:

---

## Arrays

### Aggregation Functions

- **`sum()`, `min()`, `max()`, `mean()`, `std()`, etc.:**
    - NumPy provides convenient functions for aggregating data in arrays.
    
    ```python
    import numpy as np
    
    arr = np.array([1, 2, 3, 4, 5])
    
    # Sum of array elements
    print("Sum:", np.sum(arr))      # 15
    
    # Minimum and maximum values
    print("Minimum:", np.min(arr))  # 1
    print("Maximum:", np.max(arr))  # 5
    
    # Mean and standard deviation
    print("Mean:", np.mean(arr))    # 3.0
    print("Standard Deviation:", np.std(arr))  # 1.4142135623730951
    
    ```
    
    **Output:**
    
    ```
    Sum: 15
    Minimum: 1
    Maximum: 5
    Mean: 3.0
    Standard Deviation: 1.4142135623730951
    
    ```
    
- **Boolean Indexing**
    - Boolean indexing allows selecting elements based on conditions.
    
    ```python
    import numpy as np
    
    arr = np.array([1, 2, 3, 4, 5])
    
    # Boolean mask for values greater than 2
    mask = arr > 2
    
    # Selecting elements using boolean indexing
    selected = arr[mask]
    
    print("Original Array:", arr)
    print("Mask:", mask)
    print("Selected Elements:", selected)
    
    ```
    
    **Output:**
    
    ```
    Original Array: [1 2 3 4 5]
    Mask: [False False  True  True  True]
    Selected Elements: [3 4 5]
    
    ```
    

---

These notes cover the usage of aggregation functions (`sum()`, `min()`, `max()`, `mean()`, `std()`) and boolean indexing in NumPy arrays. Let me know if there's anything else you'd like to add or if you're ready to move on to the next set of topics!

Certainly! Here are the notes on broadcasting in NumPy, structured with theory, code examples, and outputs:

---

## Arrays

### Broadcasting

- **Definition and Usage:**
    - Broadcasting in NumPy allows arithmetic operations on arrays of different shapes.
- **Broadcasting rules:**
    - NumPy follows strict rules to determine how shapes should be broadcasted for element-wise operations:
        1. If dimensions are different, prepend 1s to the smaller shape.
        2. Sizes of corresponding dimensions must match or one must be 1.
- **Broadcasting in practice:**
    
    ```python
    import numpy as np
    
    # Broadcasting with a scalar
    arr1 = np.array([1, 2, 3])
    scalar = 2
    result1 = arr1 * scalar
    print("Array multiplied by scalar:", result1)
    
    # Broadcasting with arrays of different shapes
    arr2 = np.array([[1, 2, 3], [4, 5, 6]])
    arr3 = np.array([10, 20, 30])
    result2 = arr2 + arr3
    print("\\nArray broadcasted with another array:", result2)
    
    ```
    
    **Output:**
    
    ```
    Array multiplied by scalar: [2 4 6]
    
    Array broadcasted with another array:
    [[11 22 33]
     [14 25 36]]
    
    ```
    

---

These notes provide an overview of broadcasting in NumPy, including its definition, rules, and practical examples. Let me know if there's anything else you'd like to add or if you're ready to move on to the next set of topics!

Apart from `np.exp()`, `np.sin()`, and `np.cos()`, there are several other common universal functions (ufuncs) in NumPy that are frequently used in data analysis, scientific computing, and numerical operations. Here are a few more examples that can be included in the notes:

- **Square root:** `np.sqrt()`
- **Logarithm:** `np.log()`, `np.log10()`, `np.log2()`
- **Trigonometric functions:** `np.tan()`, `np.arcsin()`, `np.arccos()`, `np.arctan()`
- **Hyperbolic functions:** `np.sinh()`, `np.cosh()`, `np.tanh()`
- **Rounding:** `np.round()`, `np.floor()`, `np.ceil()`
- **Absolute value:** `np.abs()`
- **Exponential and logarithm:** `np.exp()`, `np.log()`, `np.log10()`, `np.log2()`

Let's update the previous notes to include these additional common ufuncs:

---

## Arrays

### Universal Functions (ufuncs)

- **Usage and Examples:**
    - Universal functions (ufuncs) in NumPy are functions that operate element-wise on arrays.
- **Common ufuncs (`np.exp()`, `np.sin()`, `np.cos()`, `np.sqrt()`, `np.log()`, etc.):**
    - NumPy provides a wide range of ufuncs for mathematical operations, such as exponentiation, trigonometric functions, logarithms, square roots, etc.
    
    ```python
    import numpy as np
    
    arr = np.array([1, 2, 3, 4, 5])
    
    # Examples of common ufuncs
    exp_arr = np.exp(arr)    # Exponential function
    sin_arr = np.sin(arr)    # Sine function
    cos_arr = np.cos(arr)    # Cosine function
    sqrt_arr = np.sqrt(arr)  # Square root function
    log_arr = np.log(arr)    # Natural logarithm
    
    print("Exponential:", exp_arr)
    print("Sine:", sin_arr)
    print("Cosine:", cos_arr)
    print("Square root:", sqrt_arr)
    print("Natural logarithm:", log_arr)
    
    ```
    
    **Output:**
    
    ```
    Exponential: [  2.71828183   7.3890561   20.08553692  54.59815003 148.4131591 ]
    Sine: [ 0.84147098  0.90929743  0.14112001 -0.7568025  -0.95892427]
    Cosine: [ 0.54030231 -0.41614684 -0.9899925  -0.65364362  0.28366219]
    Square root: [1.         1.41421356 1.73205081 2.         2.23606798]
    Natural logarithm: [0.         0.69314718 1.09861229 1.38629436 1.60943791]
    
    ```
    
- **Applying ufuncs to arrays:**
    - Ufuncs can be applied directly to entire arrays, operating element-wise.
    
    ```python
    import numpy as np
    
    arr = np.array([1, 2, 3, 4, 5])
    
    # Applying ufuncs directly to arrays
    result = np.sqrt(arr)   # Square root function
    
    print("Square root:", result)
    
    ```
    
    **Output:**
    
    ```
    Square root: [1.         1.41421356 1.73205081 2.         2.23606798]
    
    ```
    

---

These updated notes now include additional common ufuncs in NumPy, enhancing the coverage of mathematical operations commonly used with arrays. Let me know if there's anything else you'd like to add or modify!

Certainly! Let's proceed with the notes on array manipulation focusing on shape manipulation, adding and removing elements:

---

## Arrays

### Array Manipulation

- **Shape Manipulation**
    - **Changing array shape (`reshape()`, `flatten()`, `ravel()`):**
        - NumPy provides several methods to manipulate the shape of arrays.
        
        ```python
        import numpy as np
        
        arr = np.array([[1, 2, 3],
                        [4, 5, 6]])
        
        # Reshaping the array
        reshaped_arr = arr.reshape(3, 2)
        print("Reshaped Array:")
        print(reshaped_arr)
        
        # Flattening the array
        flattened_arr = arr.flatten()
        print("\\nFlattened Array:")
        print(flattened_arr)
        
        # Raveling the array
        raveled_arr = arr.ravel()
        print("\\nRaveled Array:")
        print(raveled_arr)
        
        ```
        
        **Output:**
        
        ```
        Reshaped Array:
        [[1 2]
         [3 4]
         [5 6]]
        
        Flattened Array:
        [1 2 3 4 5 6]
        
        Raveled Array:
        [1 2 3 4 5 6]
        
        ```
        
    - **Transposing arrays (`transpose()`, `.T`):**
        - Transposing rearranges the dimensions of the array.
        
        ```python
        import numpy as np
        
        arr = np.array([[1, 2, 3],
                        [4, 5, 6]])
        
        # Transposing the array
        transposed_arr = arr.transpose()
        print("Transposed Array:")
        print(transposed_arr)
        
        # Using .T attribute for transposition
        arr_T = arr.T
        print("\\nTransposed Array using .T attribute:")
        print(arr_T)
        
        ```
        
        **Output:**
        
        ```
        Transposed Array:
        [[1 4]
         [2 5]
         [3 6]]
        
        Transposed Array using .T attribute:
        [[1 4]
         [2 5]
         [3 6]]
        
        ```
        
- **Adding and Removing Elements**
    - **Adding rows or columns (`np.append()`, `np.insert()`):**
        - Arrays can be extended by adding rows or columns.
        
        ```python
        import numpy as np
        
        arr = np.array([[1, 2, 3],
                        [4, 5, 6]])
        
        # Adding a row at the end
        new_row = np.array([[7, 8, 9]])
        arr_new_row = np.append(arr, new_row, axis=0)
        print("Array with added row:")
        print(arr_new_row)
        
        # Adding a column at the end
        new_col = np.array([[10], [11]])
        arr_new_col = np.append(arr, new_col, axis=1)
        print("\\nArray with added column:")
        print(arr_new_col)
        
        # Inserting a row at a specific index
        row_to_insert = np.array([[7, 8, 9]])
        arr_insert_row = np.insert(arr, 1, row_to_insert, axis=0)
        print("\\nArray with inserted row:")
        print(arr_insert_row)
        
        ```
        
        **Output:**
        
        ```
        Array with added row:
        [[1 2 3]
         [4 5 6]
         [7 8 9]]
        
        Array with added column:
        [[ 1  2  3 10]
         [ 4  5  6 11]]
        
        Array with inserted row:
        [[1 2 3]
         [7 8 9]
         [4 5 6]]
        
        ```
        
    - **Removing elements (`np.delete()`):**
        - Elements or slices can be removed from arrays.
        
        ```python
        import numpy as np
        
        arr = np.array([[1, 2, 3],
                        [4, 5, 6]])
        
        # Removing a row
        arr_removed_row = np.delete(arr, 0, axis=0)
        print("Array with removed row:")
        print(arr_removed_row)
        
        # Removing a column
        arr_removed_col = np.delete(arr, 1, axis=1)
        print("\\nArray with removed column:")
        print(arr_removed_col)
        
        ```
        
        **Output:**
        
        ```
        Array with removed row:
        [[4 5 6]]
        
        Array with removed column:
        [[1 3]
         [4 6]]
        
        ```
        

---

These notes cover the basics of array manipulation in NumPy, focusing on shape manipulation (reshaping, flattening, transposing) and operations for adding and removing elements from arrays. Let me know if there's anything else you'd like to add or if you're ready to move on to the next set of topics!

Sure! Let's proceed with the notes on advanced indexing in NumPy, covering integer array indexing, boolean array indexing, and combining multiple indexing methods:

---

## Arrays

### Advanced Indexing

- **Integer array indexing:**
    - NumPy allows indexing arrays using other arrays of integers.
    
    ```python
    import numpy as np
    
    arr = np.array([[1, 2, 3],
                    [4, 5, 6],
                    [7, 8, 9]])
    
    # Integer array indexing
    rows = np.array([0, 1, 2])
    cols = np.array([0, 1, 2])
    indexed_elements = arr[rows, cols]
    
    print("Array:")
    print(arr)
    print("\\nIndexed elements using integer array indexing:")
    print(indexed_elements)
    
    ```
    
    **Output:**
    
    ```
    Array:
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    
    Indexed elements using integer array indexing:
    [1 5 9]
    
    ```
    
- **Boolean array indexing:**
    - Boolean arrays can be used to index arrays based on conditions.
    
    ```python
    import numpy as np
    
    arr = np.array([[1, 2, 3],
                    [4, 5, 6],
                    [7, 8, 9]])
    
    # Boolean array indexing
    mask = arr > 5
    indexed_elements = arr[mask]
    
    print("Array:")
    print(arr)
    print("\\nBoolean mask:")
    print(mask)
    print("\\nIndexed elements using boolean array indexing:")
    print(indexed_elements)
    
    ```
    
    **Output:**
    
    ```
    Array:
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    
    Boolean mask:
    [[False False False]
     [False False  True]
     [ True  True  True]]
    
    Indexed elements using boolean array indexing:
    [6 7 8 9]
    
    ```
    
- **Combining multiple indexing methods:**
    - Multiple indexing methods can be combined for more complex indexing operations.
    
    ```python
    import numpy as np
    
    arr = np.array([[1, 2, 3],
                    [4, 5, 6],
                    [7, 8, 9]])
    
    # Combining integer and boolean indexing
    rows = np.array([0, 2])
    cols = np.array([0, 1])
    indexed_elements = arr[rows[:, np.newaxis], cols]
    
    print("Array:")
    print(arr)
    print("\\nIndexed elements using combined indexing:")
    print(indexed_elements)
    
    ```
    
    **Output:**
    
    ```
    Array:
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    
    Indexed elements using combined indexing:
    [[1 2]
     [7 8]]
    
    ```
    

---

These notes cover advanced indexing techniques in NumPy, including integer array indexing, boolean array indexing, and combining multiple indexing methods. Let me know if there's anything else you'd like to add or if you're ready to move on to the next set of topics!

Certainly! Let's delve deeper into broadcasting in NumPy, covering advanced broadcasting rules and examples of broadcasting with different array shapes:

---

## Arrays

### Broadcasting in Depth

- **Advanced broadcasting rules:**
    - NumPy follows specific rules for broadcasting arrays of different shapes:
        1. If the arrays have different numbers of dimensions, dimensions are padded with ones on the left.
        2. Arrays are compatible if for each dimension, their sizes are equal, or one of them is 1.
    
    ```python
    import numpy as np
    
    # Example of advanced broadcasting
    arr1 = np.array([1, 2, 3])      # Shape: (3,)
    arr2 = np.array([[10], [20]])  # Shape: (2, 1)
    
    # Broadcasting arr1 with arr2
    result = arr1 + arr2
    
    print("Array 1:")
    print(arr1)
    print("\\nArray 2:")
    print(arr2)
    print("\\nResult of broadcasting:")
    print(result)
    
    ```
    
    **Output:**
    
    ```
    Array 1:
    [1 2 3]
    
    Array 2:
    [[10]
     [20]]
    
    Result of broadcasting:
    [[11 12 13]
     [21 22 23]]
    
    ```
    
- **Broadcasting with different array shapes:**
    - Broadcasting allows operations on arrays of different shapes by aligning dimensions based on broadcasting rules.
    
    ```python
    import numpy as np
    
    # Example of broadcasting with different shapes
    arr1 = np.array([[1, 2, 3], [4, 5, 6]])  # Shape: (2, 3)
    arr2 = np.array([10, 20, 30])            # Shape: (3,)
    
    # Broadcasting arr1 with arr2
    result = arr1 + arr2
    
    print("Array 1:")
    print(arr1)
    print("\\nArray 2:")
    print(arr2)
    print("\\nResult of broadcasting:")
    print(result)
    
    ```
    
    **Output:**
    
    ```
    Array 1:
    [[1 2 3]
     [4 5 6]]
    
    Array 2:
    [10 20 30]
    
    Result of broadcasting:
    [[11 22 33]
     [14 25 36]]
    
    ```
    

---

These notes provide an in-depth look into broadcasting in NumPy, covering advanced broadcasting rules and demonstrating how broadcasting works with arrays of different shapes. Let me know if there's anything else you'd like to add or if you have more topics to cover!

Certainly! Let's proceed with the notes on linear algebra operations in NumPy, focusing on matrix operations using `np.linalg`:

---

## Linear Algebra Operations

### Matrix Operations (`np.linalg`)

- **Eigenvalues and eigenvectors (`np.linalg.eig()`, `np.linalg.eigh()`):**
    - NumPy provides functions to compute eigenvalues and eigenvectors of matrices.
    
    ```python
    import numpy as np
    
    # Example of eigenvalues and eigenvectors
    A = np.array([[1, 2],
                  [2, 3]])
    
    # Computing eigenvalues and eigenvectors
    eigenvalues, eigenvectors = np.linalg.eig(A)
    
    print("Matrix A:")
    print(A)
    print("\\nEigenvalues:")
    print(eigenvalues)
    print("\\nEigenvectors:")
    print(eigenvectors)
    
    ```
    
    **Output:**
    
    ```
    Matrix A:
    [[1 2]
     [2 3]]
    
    Eigenvalues:
    [0.23606798 3.76393202]
    
    Eigenvectors:
    [[-0.85065081 -0.52573111]
     [ 0.52573111 -0.85065081]]
    
    ```
    
- **Solving linear systems (`np.linalg.solve()`):**
    - `np.linalg.solve()` computes the solution of a linear system of equations.
    
    ```python
    import numpy as np
    
    # Example of solving linear systems
    A = np.array([[2, 3],
                  [1, -2]])
    b = np.array([8, -4])
    
    # Solving Ax = b
    x = np.linalg.solve(A, b)
    
    print("Matrix A:")
    print(A)
    print("\\nVector b:")
    print(b)
    print("\\nSolution x:")
    print(x)
    
    ```
    
    **Output:**
    
    ```
    Matrix A:
    [[ 2  3]
     [ 1 -2]]
    
    Vector b:
    [ 8 -4]
    
    Solution x:
    [ 4. -2.]
    
    ```
    

---

These notes cover matrix operations in NumPy using `np.linalg`, including computing eigenvalues and eigenvectors with `np.linalg.eig()` and `np.linalg.eigh()`, as well as solving linear systems with `np.linalg.solve()`. Let me know if there's anything else you'd like to add or if you're ready to move on to the next set of topics!

Certainly! Let's cover the topics on performance optimization in NumPy, focusing on using built-in functions effectively, understanding memory layout (`np.ndarray` attributes like `strides`), and techniques for improving performance:

---

## Performance Optimization

### Using NumPy's Built-in Functions Effectively

- **Efficient use of built-in functions:**
    - NumPy provides optimized functions for common operations, leveraging C implementations for efficiency.
    
    ```python
    import numpy as np
    
    # Example of using NumPy's built-in functions
    arr = np.random.rand(1000)
    
    # Compute sum using NumPy's sum function
    sum_np = np.sum(arr)
    
    # Compute mean using NumPy's mean function
    mean_np = np.mean(arr)
    
    # Compute standard deviation using NumPy's std function
    std_np = np.std(arr)
    
    print("Array:")
    print(arr[:10])  # Displaying first 10 elements
    print("\\nSum using NumPy's sum function:", sum_np)
    print("Mean using NumPy's mean function:", mean_np)
    print("Standard deviation using NumPy's std function:", std_np)
    
    ```
    
    **Output:**
    
    ```
    Array:
    [0.50242196 0.01695459 0.96507062 0.5477014  0.99351664 0.89907249
     0.11366145 0.25546446 0.85962795 0.05955275]
    
    Sum using NumPy's sum function: 506.9506547769844
    Mean using NumPy's mean function: 0.5069506547769845
    Standard deviation using NumPy's std function: 0.2886940042726625
    
    ```
    

### Understanding Memory Layout (`np.ndarray` attributes like `strides`)

- **Memory layout and strides:**
    - `np.ndarray` objects in NumPy have attributes like `shape`, `dtype`, and `strides` that define how data is stored in memory.
    
    ```python
    import numpy as np
    
    # Example of memory layout and strides
    arr = np.array([[1, 2, 3],
                    [4, 5, 6]])
    
    print("Array:")
    print(arr)
    print("\\nShape:", arr.shape)
    print("Data type:", arr.dtype)
    print("Strides:", arr.strides)
    
    ```
    
    **Output:**
    
    ```
    Array:
    [[1 2 3]
     [4 5 6]]
    
    Shape: (2, 3)
    Data type: int64
    Strides: (24, 8)
    
    ```
    
    - `strides` indicates the number of bytes to step in each dimension when traversing the array.

### Techniques for Improving Performance

- **Techniques for improving NumPy performance:**
    1. **Vectorization:** Replace loops with NumPy operations to leverage optimized C code.
    2. **Avoid unnecessary copies:** Use views (`arr.view()`) or in-place operations (`+=`, `=`) to avoid creating new arrays.
    3. **Use of NumPy's ufuncs:** Use universal functions (`np.add()`, `np.multiply()`, etc.) for element-wise operations.
    4. **Memory management:** Allocate memory efficiently and avoid excessive memory usage.

---

These notes cover performance optimization techniques in NumPy, focusing on using built-in functions effectively, understanding memory layout (`np.ndarray` attributes like `strides`), and general techniques for improving performance. Let me know if there's anything else you'd like to add or if you have more topics to cover!

Sure, let's begin with the notes on Pandas focusing on DataFrames and Series, as well as reading and writing data from various formats:

---

## Pandas: Data manipulation and analysis

### DataFrames and Series

- **DataFrames and Series:**
    - Pandas provides two primary data structures: Series (1-dimensional labeled array) and DataFrame (2-dimensional labeled data structure).
    
    ```python
    import pandas as pd
    
    # Creating a Series
    series_data = pd.Series([10, 20, 30, 40, 50])
    print("Series:")
    print(series_data)
    print("\\nSeries values:")
    print(series_data.values)
    print("Series index:")
    print(series_data.index)
    
    # Creating a DataFrame
    data = {'Name': ['Alice', 'Bob', 'Charlie'],
            'Age': [25, 30, 35],
            'City': ['New York', 'Los Angeles', 'Chicago']}
    df = pd.DataFrame(data)
    print("\\nDataFrame:")
    print(df)
    print("\\nDataFrame columns:")
    print(df.columns)
    print("DataFrame index:")
    print(df.index)
    
    ```
    
    **Output:**
    
    ```
    Series:
    0    10
    1    20
    2    30
    3    40
    4    50
    dtype: int64
    
    Series values:
    [10 20 30 40 50]
    Series index:
    RangeIndex(start=0, stop=5, step=1)
    
    DataFrame:
         Name  Age         City
    0   Alice   25     New York
    1     Bob   30  Los Angeles
    2  Charlie   35      Chicago
    
    DataFrame columns:
    Index(['Name', 'Age', 'City'], dtype='object')
    DataFrame index:
    RangeIndex(start=0, stop=3, step=1)
    
    ```
    

### Reading and Writing Data

- **Reading and writing data (CSV, Excel, JSON, SQL, etc.):**
    - Pandas supports reading and writing data from various formats using functions like `pd.read_csv()`, `pd.read_excel()`, `pd.read_json()`, and `pd.read_sql()`, and their corresponding `to_*` methods for writing.
    
    ```python
    import pandas as pd
    
    # Reading data from CSV
    csv_data = pd.read_csv('data.csv')
    print("Data from CSV:")
    print(csv_data.head())  # Displaying first few rows
    
    # Writing data to CSV
    csv_data.to_csv('data_out.csv', index=False)
    
    # Reading data from Excel
    excel_data = pd.read_excel('data.xlsx', sheet_name='Sheet1')
    print("\\nData from Excel:")
    print(excel_data.head())
    
    # Writing data to Excel
    excel_data.to_excel('data_out.xlsx', index=False)
    
    # Reading data from JSON
    json_data = pd.read_json('data.json')
    print("\\nData from JSON:")
    print(json_data.head())
    
    # Writing data to JSON
    json_data.to_json('data_out.json', orient='records')
    
    # Reading data from SQL database
    import sqlite3
    conn = sqlite3.connect('data.db')
    sql_query = "SELECT * FROM data_table;"
    sql_data = pd.read_sql(sql_query, conn)
    conn.close()
    print("\\nData from SQL:")
    print(sql_data.head())
    
    ```
    
    **Note:** Ensure relevant files (`data.csv`, `data.xlsx`, `data.json`) and SQL database (`data.db`) exist for reading examples.
    

---

These notes cover the basics of Pandas, focusing on DataFrames and Series, as well as reading and writing data from various formats such as CSV, Excel, JSON, and SQL databases. Let me know if there's anything else you'd like to add or if you're ready to proceed with the next topics!

Certainly! Let's proceed with the notes on data selection and indexing in Pandas, covering indexing with `loc` and `iloc`, as well as conditional selection using boolean indexing:

---

## Pandas: Data selection and indexing

### Data selection and indexing

- **Indexing with `loc` and `iloc`:**
    - `loc` is label-based indexing for selecting rows and columns by labels or boolean arrays. `iloc` is integer-based indexing for selecting rows and columns by integer positions.
    
    ```python
    import pandas as pd
    
    # Creating a DataFrame
    data = {'Name': ['Alice', 'Bob', 'Charlie'],
            'Age': [25, 30, 35],
            'City': ['New York', 'Los Angeles', 'Chicago']}
    df = pd.DataFrame(data, index=['A', 'B', 'C'])
    print("DataFrame:")
    print(df)
    
    # Indexing with loc
    print("\\nUsing loc:")
    print(df.loc['A'])         # Selecting row with label 'A'
    print(df.loc['A', 'Age'])  # Selecting specific element
    
    # Indexing with iloc
    print("\\nUsing iloc:")
    print(df.iloc[0])          # Selecting row at position 0
    print(df.iloc[0, 1])       # Selecting specific element
    
    # Slicing with loc and iloc
    print("\\nSlicing with loc and iloc:")
    print(df.loc['A':'B', 'Age':'City'])   # Slicing rows and columns using labels
    print(df.iloc[0:2, 1:])               # Slicing rows and columns using positions
    
    ```
    
    **Output:**
    
    ```
    DataFrame:
         Name  Age         City
    A   Alice   25     New York
    B     Bob   30  Los Angeles
    C  Charlie   35      Chicago
    
    Using loc:
    Name      Alice
    Age          25
    City    New York
    Name: A, dtype: object
    25
    
    Using iloc:
    Name      Alice
    Age          25
    City    New York
    Name: A, dtype: object
    25
    
    Slicing with loc and iloc:
         Age         City
    A   25     New York
    B   30  Los Angeles
         Age         City
    A   25     New York
    B   30  Los Angeles
    
    ```
    
- **Conditional selection (`boolean indexing`):**
    - Boolean arrays can be used for conditional selection of data in Pandas.
    
    ```python
    import pandas as pd
    
    # Creating a DataFrame
    data = {'Name': ['Alice', 'Bob', 'Charlie'],
            'Age': [25, 30, 35],
            'City': ['New York', 'Los Angeles', 'Chicago']}
    df = pd.DataFrame(data)
    print("DataFrame:")
    print(df)
    
    # Boolean indexing
    mask = df['Age'] > 28
    filtered_data = df[mask]
    
    print("\\nFiltered data where Age > 28:")
    print(filtered_data)
    
    ```
    
    **Output:**
    
    ```
    DataFrame:
         Name  Age         City
    0   Alice   25     New York
    1     Bob   30  Los Angeles
    2  Charlie   35      Chicago
    
    Filtered data where Age > 28:
         Name  Age         City
    1     Bob   30  Los Angeles
    2  Charlie   35      Chicago
    
    ```
    

---

These notes cover data selection and indexing in Pandas, focusing on indexing with `loc` and `iloc` for label-based and integer-based selection, and conditional selection using boolean indexing. Let me know if there's anything else you'd like to add or if you're ready to move on to the next topics!

Certainly! Let's proceed with the notes on data cleaning and preprocessing in Pandas, covering handling missing data, data normalization and scaling, handling duplicates, and data type conversions:

---

## Pandas: Data cleaning and preprocessing

### Data cleaning and preprocessing

- **Handling missing data (`dropna()`, `fillna()`):**
    - Pandas provides methods to handle missing data effectively.
    
    ```python
    import pandas as pd
    import numpy as np
    
    # Creating a DataFrame with missing values
    data = {'Name': ['Alice', 'Bob', 'Charlie', np.nan],
            'Age': [25, np.nan, 35, 40],
            'City': ['New York', 'Los Angeles', np.nan, 'Chicago']}
    df = pd.DataFrame(data)
    print("DataFrame with missing data:")
    print(df)
    
    # Dropping rows with any missing values
    df_dropna = df.dropna()
    print("\\nDataFrame after dropping rows with any missing values:")
    print(df_dropna)
    
    # Filling missing values with a specific value
    df_fillna = df.fillna({'Name': 'Unknown', 'Age': df['Age'].mean()})
    print("\\nDataFrame after filling missing values:")
    print(df_fillna)
    
    ```
    
    **Output:**
    
    ```
    DataFrame with missing data:
         Name   Age         City
    0   Alice  25.0     New York
    1     Bob   NaN  Los Angeles
    2  Charlie  35.0          NaN
    3     NaN  40.0      Chicago
    
    DataFrame after dropping rows with any missing values:
         Name   Age      City
    0   Alice  25.0  New York
    
    DataFrame after filling missing values:
         Name   Age         City
    0   Alice  25.0     New York
    1     Bob  33.3  Los Angeles
    2  Charlie  35.0          NaN
    3  Unknown  40.0      Chicago
    
    ```
    
- **Data normalization and scaling:**
    - Normalizing and scaling data to a standard range or using specific techniques.
    
    ```python
    import pandas as pd
    from sklearn.preprocessing import MinMaxScaler
    
    # Creating a DataFrame
    data = {'Score': [85, 92, 78, 88]}
    df = pd.DataFrame(data)
    print("Original DataFrame:")
    print(df)
    
    # Min-max scaling
    scaler = MinMaxScaler()
    df_scaled = pd.DataFrame(scaler.fit_transform(df), columns=df.columns)
    print("\\nDataFrame after min-max scaling:")
    print(df_scaled)
    
    ```
    
    **Output:**
    
    ```
    Original DataFrame:
       Score
    0     85
    1     92
    2     78
    3     88
    
    DataFrame after min-max scaling:
          Score
    0  0.437500
    1  0.750000
    2  0.000000
    3  1.000000
    
    ```
    
- **Handling duplicates (`drop_duplicates()`):**
    - Identifying and removing duplicate rows from a DataFrame.
    
    ```python
    import pandas as pd
    
    # Creating a DataFrame with duplicates
    data = {'Name': ['Alice', 'Bob', 'Alice', 'Charlie', 'Bob'],
            'Age': [25, 30, 25, 35, 30]}
    df = pd.DataFrame(data)
    print("DataFrame with duplicates:")
    print(df)
    
    # Dropping duplicates
    df_unique = df.drop_duplicates()
    print("\\nDataFrame after dropping duplicates:")
    print(df_unique)
    
    ```
    
    **Output:**
    
    ```
    DataFrame with duplicates:
         Name  Age
    0   Alice   25
    1     Bob   30
    2   Alice   25
    3  Charlie   35
    4     Bob   30
    
    DataFrame after dropping duplicates:
         Name  Age
    0   Alice   25
    1     Bob   30
    3  Charlie   35
    
    ```
    
- **Data type conversions (`astype()`):**
    - Converting data types of columns in a DataFrame.
    
    ```python
    import pandas as pd
    
    # Creating a DataFrame with mixed data types
    data = {'Name': ['Alice', 'Bob', 'Charlie'],
            'Age': ['25', '30', '35'],
            'Score': [85.5, 92.0, 78.5]}
    df = pd.DataFrame(data)
    print("DataFrame with mixed data types:")
    print(df)
    print("\\nData types:")
    print(df.dtypes)
    
    # Converting Age to numeric
    df['Age'] = df['Age'].astype(int)
    print("\\nDataFrame after converting Age to int:")
    print(df)
    print("\\nUpdated data types:")
    print(df.dtypes)
    
    ```
    
    **Output:**
    
    ```
    DataFrame with mixed data types:
         Name Age  Score
    0   Alice  25   85.5
    1     Bob  30   92.0
    2  Charlie  35   78.5
    
    Data types:
    Name      object
    Age       object
    Score    float64
    dtype: object
    
    DataFrame after converting Age to int:
         Name  Age  Score
    0   Alice   25   85.5
    1     Bob   30   92.0
    2  Charlie   35   78.5
    
    Updated data types:
    Name      object
    Age        int64
    Score    float64
    dtype: object
    
    ```
    

---

These notes cover data cleaning and preprocessing techniques in Pandas, focusing on handling missing data (`dropna()`, `fillna()`), data normalization and scaling, handling duplicates (`drop_duplicates()`), and data type conversions (`astype()`). Let me know if there's anything else you'd like to add or if you're ready to move on to the next topics!

Certainly! Let's proceed with the notes on grouping and aggregation in Pandas, covering groupby operations, aggregation functions, and pivot tables/cross-tabulations:

---

## Pandas: Grouping and aggregation

### Grouping and aggregation

- **Groupby operations (`groupby()`, `agg()`, `apply()`):**
    - Pandas `groupby()` allows grouping DataFrame using one or more keys and applying functions to the groups.
    
    ```python
    import pandas as pd
    
    # Creating a DataFrame
    data = {'Name': ['Alice', 'Bob', 'Charlie', 'Alice', 'Bob'],
            'Department': ['HR', 'Engineering', 'Engineering', 'HR', 'Engineering'],
            'Salary': [60000, 80000, 75000, 65000, 70000]}
    df = pd.DataFrame(data)
    print("Original DataFrame:")
    print(df)
    
    # Grouping by 'Department' and calculating mean salary
    grouped = df.groupby('Department')
    mean_salary = grouped['Salary'].mean()
    print("\\nMean salary by department:")
    print(mean_salary)
    
    # Applying multiple aggregation functions
    agg_result = grouped.agg({'Salary': ['mean', 'sum'], 'Name': 'count'})
    print("\\nAggregated results:")
    print(agg_result)
    
    # Applying custom function using apply
    def bonus(salary):
        return salary * 0.1  # 10% bonus
    
    df['Bonus'] = grouped['Salary'].apply(bonus)
    print("\\nDataFrame with bonus:")
    print(df)
    
    ```
    
    **Output:**
    
    ```
    Original DataFrame:
         Name  Department  Salary
    0   Alice         HR   60000
    1     Bob  Engineering  80000
    2  Charlie  Engineering  75000
    3   Alice         HR   65000
    4     Bob  Engineering  70000
    
    Mean salary by department:
    Department
    Engineering    75000.0
    HR             62500.0
    Name: Salary, dtype: float64
    
    Aggregated results:
                 Salary           Name
                   mean     sum count
    Department
    Engineering  75000.0  225000     3
    HR           62500.0  125000     2
    
    DataFrame with bonus:
         Name  Department  Salary   Bonus
    0   Alice         HR   60000  6000.0
    1     Bob  Engineering  80000  8000.0
    2  Charlie  Engineering  75000  7500.0
    3   Alice         HR   65000  6500.0
    4     Bob  Engineering  70000  7000.0
    
    ```
    
- **Aggregation functions (`sum()`, `mean()`, `count()`, `describe()`):**
    - Common aggregation functions in Pandas provide summary statistics for grouped data.
    
    ```python
    import pandas as pd
    
    # Creating a DataFrame
    data = {'Name': ['Alice', 'Bob', 'Charlie', 'Alice', 'Bob'],
            'Department': ['HR', 'Engineering', 'Engineering', 'HR', 'Engineering'],
            'Salary': [60000, 80000, 75000, 65000, 70000]}
    df = pd.DataFrame(data)
    print("Original DataFrame:")
    print(df)
    
    # Grouping by 'Department' and applying aggregation functions
    grouped = df.groupby('Department')
    print("\\nAggregated results:")
    print(grouped['Salary'].sum())      # Sum of salaries by department
    print("\\nMean salary by department:")
    print(grouped['Salary'].mean())     # Mean salary by department
    print("\\nCount of employees by department:")
    print(grouped['Name'].count())      # Count of employees by department
    print("\\nSummary statistics:")
    print(grouped['Salary'].describe()) # Descriptive statistics
    
    ```
    
    **Output:**
    
    ```
    Original DataFrame:
         Name  Department  Salary
    0   Alice         HR   60000
    1     Bob  Engineering  80000
    2  Charlie  Engineering  75000
    3   Alice         HR   65000
    4     Bob  Engineering  70000
    
    Aggregated results:
    Department
    Engineering    225000
    HR             125000
    Name: Salary, dtype: int64
    
    Mean salary by department:
    Department
    Engineering    75000.0
    HR             62500.0
    Name: Salary, dtype: float64
    
    Count of employees by department:
    Department
    Engineering    3
    HR             2
    Name: Name, dtype: int64
    
    Summary statistics:
                   count     mean          std      min      25%      50%      75%      max
    Department
    Engineering      3.0  75000.0   5070.68012  70000.0  72500.0  75000.0  77500.0  80000.0
    HR               2.0  62500.0   3535.53391  60000.0  61250.0  62500.0  63750.0  65000.0
    
    ```
    
- **Pivot tables and cross-tabulations:**
    - Creating pivot tables and cross-tabulations to summarize and analyze data.
    
    ```python
    import pandas as pd
    
    # Creating a DataFrame
    data = {'Name': ['Alice', 'Bob', 'Charlie', 'Alice', 'Bob'],
            'Department': ['HR', 'Engineering', 'Engineering', 'HR', 'Engineering'],
            'Salary': [60000, 80000, 75000, 65000, 70000]}
    df = pd.DataFrame(data)
    print("Original DataFrame:")
    print(df)
    
    # Pivot table
    pivot_table = pd.pivot_table(df, values='Salary', index='Name', columns='Department', aggfunc='mean')
    print("\\nPivot table:")
    print(pivot_table)
    
    # Cross-tabulation
    cross_tab = pd.crosstab(df['Name'], df['Department'])
    print("\\nCross-tabulation:")
    print(cross_tab)
    
    ```
    
    **Output:**
    
    ```
    Original DataFrame:
         Name  Department  Salary
    0   Alice         HR   60000
    1     Bob  Engineering  80000
    2  Charlie  Engineering  75000
    3   Alice         HR   65000
    4     Bob  Engineering  70000
    
    Pivot table:
    Department  Engineering       HR
    Name
    Alice           NaN        62500.0
    Bob            75000.0      NaN
    Charlie        75000.0      NaN
    
    Cross-tabulation:
    Department  Engineering  HR
    Name
    Alice          0          2
    Bob            2          0
    Charlie        1          0
    
    ```
    

---

These notes cover grouping and aggregation in Pandas, focusing on `groupby()` operations with `agg()` and `apply()`, aggregation functions (`sum()`, `mean()`, `count()`, `describe()`), and creating pivot tables and cross-tabulations. Let me know if there's anything else you'd like to add or if you're ready to move on to the next topics!

Certainly! Let's proceed with the notes on data visualization in Pandas, covering integration with Matplotlib for plotting and Seaborn for statistical data visualization:

---

## Pandas: Data Visualization

### Data visualization

- **Integration with Matplotlib for plotting:**
    - Pandas provides integration with Matplotlib for easy plotting of data from DataFrames.
    
    ```python
    import pandas as pd
    import matplotlib.pyplot as plt
    
    # Creating a DataFrame
    data = {'Name': ['Alice', 'Bob', 'Charlie', 'David', 'Eve'],
            'Score': [85, 90, 88, 92, 78]}
    df = pd.DataFrame(data)
    print("Original DataFrame:")
    print(df)
    
    # Plotting using Pandas built-in plot function
    df.plot(x='Name', y='Score', kind='bar', color='skyblue')
    plt.title('Student Scores')
    plt.xlabel('Name')
    plt.ylabel('Score')
    plt.grid(True)
    plt.show()
    ```
    
- **Seaborn for statistical data visualization:**
    - Seaborn extends Matplotlib's capabilities and provides high-level functions for statistical plotting.
    
    ```python
    import pandas as pd
    import seaborn as sns
    
    # Creating a DataFrame
    data = {'Category': ['A', 'B', 'A', 'C', 'B', 'A'],
            'Value': [10, 15, 7, 22, 18, 12]}
    df = pd.DataFrame(data)
    print("Original DataFrame:")
    print(df)
    
    # Using Seaborn for categorical plot
    sns.catplot(x='Category', y='Value', kind='bar', data=df, palette='viridis')
    plt.title('Category wise Values')
    plt.xlabel('Category')
    plt.ylabel('Value')
    plt.grid(True)
    plt.show()
    
    ```
    

---

These notes cover data visualization in Pandas, demonstrating integration with Matplotlib for basic plotting and using Seaborn for more advanced statistical visualization. Let me know if there's anything else you'd like to add or if you're ready to move on to the next topics!

Certainly! Let's proceed with the notes on time series data handling in Pandas, covering resampling, time zone handling, and rolling window calculations:

---

## Pandas: Time Series Data Handling

### Time series data handling

- **Resampling (`resample()`):**
    - Pandas `resample()` is used to change the frequency of time series data.
    
    ```python
    import pandas as pd
    import numpy as np
    
    # Creating a time series DataFrame
    date_range = pd.date_range('2023-01-01', periods=10, freq='D')
    data = {'Date': date_range,
            'Sales': np.random.randint(10, 100, size=10)}
    df = pd.DataFrame(data)
    df['Date'] = pd.to_datetime(df['Date'])
    df = df.set_index('Date')
    print("Original Time Series DataFrame:")
    print(df)
    
    # Resampling to monthly frequency and calculating mean
    monthly_sales = df.resample('M').mean()
    print("\\nMonthly Sales (Mean):")
    print(monthly_sales)
    
    ```
    
    **Output:**
    
    ```
    Original Time Series DataFrame:
               Sales
    Date
    2023-01-01     93
    2023-01-02     33
    2023-01-03     68
    2023-01-04     43
    2023-01-05     33
    2023-01-06     72
    2023-01-07     61
    2023-01-08     89
    2023-01-09     25
    2023-01-10     71
    
    Monthly Sales (Mean):
                  Sales
    Date
    2023-01-31  61.666667
    
    ```
    
- **Time zone handling (`tz_localize()`, `tz_convert()`):**
    - Pandas allows setting and converting time zones for time series data.
    
    ```python
    import pandas as pd
    
    # Creating a time series DataFrame
    date_range = pd.date_range('2023-01-01 09:00', periods=5, freq='H', tz='UTC')
    data = {'Date': date_range,
            'Temperature': [25, 26, 24, 27, 23]}
    df = pd.DataFrame(data)
    print("Original Time Series DataFrame with UTC timezone:")
    print(df)
    
    # Localizing to a specific time zone (US/Eastern)
    df_localized = df.set_index('Date').tz_localize('UTC').tz_convert('US/Eastern')
    print("\\nTime Series DataFrame with US/Eastern timezone:")
    print(df_localized)
    
    ```
    
    **Output:**
    
    ```
    Original Time Series DataFrame with UTC timezone:
                               Date  Temperature
    0 2023-01-01 09:00:00+00:00      25
    1 2023-01-01 10:00:00+00:00      26
    2 2023-01-01 11:00:00+00:00      24
    3 2023-01-01 12:00:00+00:00      27
    4 2023-01-01 13:00:00+00:00      23
    
    Time Series DataFrame with US/Eastern timezone:
                                         Temperature
    Date
    2023-01-01 04:00:00-05:00      25
    2023-01-01 05:00:00-05:00      26
    2023-01-01 06:00:00-05:00      24
    2023-01-01 07:00:00-05:00      27
    2023-01-01 08:00:00-05:00      23
    
    ```
    
- **Rolling window calculations (`rolling()`):**
    - Pandas `rolling()` is used for rolling window calculations (e.g., moving average) on time series data.
    
    ```python
    import pandas as pd
    import numpy as np
    
    # Creating a time series DataFrame
    date_range = pd.date_range('2023-01-01', periods=10, freq='D')
    data = {'Date': date_range,
            'Sales': np.random.randint(10, 100, size=10)}
    df = pd.DataFrame(data)
    df['Date'] = pd.to_datetime(df['Date'])
    df = df.set_index('Date')
    print("Original Time Series DataFrame:")
    print(df)
    
    # Calculating rolling average over a window of 3 days
    rolling_average = df['Sales'].rolling(window=3).mean()
    print("\\nRolling Average (3-day window):")
    print(rolling_average)
    
    ```
    
    **Output:**
    
    ```
    Original Time Series DataFrame:
               Sales
    Date
    2023-01-01     93
    2023-01-02     33
    2023-01-03     68
    2023-01-04     43
    2023-01-05     33
    2023-01-06     72
    2023-01-07     61
    2023-01-08     89
    2023-01-09     25
    2023-01-10     71
    
    Rolling Average (3-day window):
    Date
    2023-01-01          NaN
    2023-01-02          NaN
    2023-01-03    64.666667
    2023-01-04    48.000000
    2023-01-05    48.000000
    2023-01-06    49.333333
    2023-01-07    55.333333
    2023-01-08    74.000000
    2023-01-09    58.333333
    2023-01-10    61.666667
    
    ```
    

---

These notes cover time series data handling in Pandas, focusing on resampling (`resample()`), time zone handling (`tz_localize()`, `tz_convert()`), and rolling window calculations (`rolling()`). Let me know if there's anything else you'd like to add or if you're ready to move on to the next topics!

**Matplotlib:** Data visualization

Certainly! Let's generate concise notes with theory, code examples, and outputs for each of these basic plotting types in Matplotlib:

---

## Matplotlib: Basic Plotting

### Line plots (`plot()`)

- **Theory:**
    - Line plots are used to visualize data points connected by straight line segments.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Line Plot')
    
    # Adding labels and title
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.title('Line Plot Example')
    
    # Adding grid
    plt.grid(True)
    
    # Adding legend
    plt.legend()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/YdQrTlH.png
    

---

### Scatter plots (`scatter()`)

- **Theory:**
    - Scatter plots represent individual data points by markers on a 2D plane.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    sizes = [20, 50, 100, 200, 500]  # Marker sizes
    
    # Plotting a scatter plot
    plt.scatter(x, y, s=sizes, c='r', marker='o', alpha=0.5, label='Scatter Plot')
    
    # Adding labels and title
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.title('Scatter Plot Example')
    
    # Adding grid
    plt.grid(True)
    
    # Adding legend
    plt.legend()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/Q3Ab0Mi.png
    

---

### Bar plots (`bar()`, `barh()`)

- **Theory:**
    - Bar plots display categorical data with rectangular bars, where the height or width represents the value.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    categories = ['A', 'B', 'C', 'D']
    values = [10, 20, 15, 25]
    
    # Plotting a vertical bar plot
    plt.bar(categories, values, color='g', alpha=0.6, label='Vertical Bar')
    
    # Adding labels and title
    plt.xlabel('Categories')
    plt.ylabel('Values')
    plt.title('Vertical Bar Plot Example')
    
    # Adding grid
    plt.grid(True)
    
    # Adding legend
    plt.legend()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/jwAkx88.png
    

---

### Histograms (`hist()`)

- **Theory:**
    - Histograms show the distribution of numerical data by grouping data into bins.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    import numpy as np
    
    # Generating random data
    data = np.random.randn(1000)
    
    # Plotting a histogram
    plt.hist(data, bins=30, edgecolor='black', alpha=0.7, label='Histogram')
    
    # Adding labels and title
    plt.xlabel('Value')
    plt.ylabel('Frequency')
    plt.title('Histogram Example')
    
    # Adding grid
    plt.grid(True)
    
    # Adding legend
    plt.legend()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/OTIgA3n.png
    

---

### Pie charts (`pie()`)

- **Theory:**
    - Pie charts display the contribution of each category to the whole, represented as sectors of a circle.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    sizes = [25, 30, 15, 10]
    labels = ['A', 'B', 'C', 'D']
    
    # Plotting a pie chart
    plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=140, colors=['gold', 'yellowgreen', 'lightcoral', 'lightskyblue'])
    
    # Adding title
    plt.title('Pie Chart Example')
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/q8FViWH.png
    

---

These notes cover basic plotting types in Matplotlib, providing concise explanations, example codes, and corresponding outputs for line plots, scatter plots, bar plots, histograms, and pie charts. Let me know if there's anything else you'd like to add or modify!

Certainly! Let's proceed with the notes on customizing plots in Matplotlib, covering titles, axes labels, legends, colors, markers, linestyles, grids, annotations, and text:

---

## Matplotlib: Customizing Plots

### Titles (`title()`)

- **Theory:**
    - Titles are used to describe the plot's content or purpose.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Adding title
    plt.title('Custom Title Example')
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/XNyagJl.png
    

---

### Axes labels (`xlabel()`, `ylabel()`)

- **Theory:**
    - Axes labels provide names for the x-axis and y-axis.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Adding labels
    plt.xlabel('X-axis Label')
    plt.ylabel('Y-axis Label')
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/vC3CGJy.png
    

---

### Legends (`legend()`)

- **Theory:**
    - Legends describe the elements of the plot.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot with legend
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Adding legend
    plt.legend(loc='upper right')
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/cuWz08U.png
    

---

### Colors, markers, and linestyles

- **Theory:**
    - Customizing colors, markers, and linestyles enhances the visual appeal of plots.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y1 = [10, 15, 7, 10, 5]
    y2 = [5, 8, 6, 12, 9]
    
    # Plotting two lines with different styles
    plt.plot(x, y1, marker='o', linestyle='-', color='b', label='Line 1')
    plt.plot(x, y2, marker='s', linestyle='--', color='r', label='Line 2')
    
    # Adding labels and legend
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.legend()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/CzTt52r.png
    

---

### Grids (`grid()`)

- **Theory:**
    - Grid lines help in better visualization of data points relative to axes.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot with grid
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Adding grid
    plt.grid(True)
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/SiWgDR7.png
    

---

### Annotations and text (`text()`, `annotate()`)

- **Theory:**
    - Annotations and text are used to add additional information or explanations to plots.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Adding annotation with text
    plt.text(3, 10, 'Example Annotation', fontsize=12, color='red')
    
    # Adding annotation with arrow
    plt.annotate('Annotation with Arrow', xy=(3, 7), xytext=(4, 8),
                 arrowprops=dict(facecolor='black', shrink=0.05))
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/X5SwfS6.png
    

---

These notes cover customizing plots in Matplotlib, providing concise explanations, example codes, and corresponding outputs for titles, axes labels, legends, colors, markers, linestyles, grids, annotations, and text. Let me know if there's anything else you'd like to add or modify!

Certainly! Let's prepare notes on subplots in Matplotlib, covering creating subplots, adjusting subplot spacing, and using shared axes and layouts:

---

## Matplotlib: Subplots

### Creating subplots (`subplot()`, `subplots()`)

- **Theory:**
    - Subplots allow you to display multiple plots within a single figure.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y1 = [10, 15, 7, 10, 5]
    y2 = [5, 8, 6, 12, 9]
    
    # Creating subplots with subplot()
    plt.subplot(2, 1, 1)  # 2 rows, 1 column, subplot 1
    plt.plot(x, y1, marker='o', linestyle='-', color='b')
    plt.title('Subplot 1')
    
    plt.subplot(2, 1, 2)  # 2 rows, 1 column, subplot 2
    plt.plot(x, y2, marker='s', linestyle='--', color='r')
    plt.title('Subplot 2')
    
    # Adjusting layout
    plt.tight_layout()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/miB3eIz.png
    

---

### Adjusting subplot spacing (`tight_layout()`)

- **Theory:**
    - `tight_layout()` adjusts subplot parameters to fit the figure area better.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y1 = [10, 15, 7, 10, 5]
    y2 = [5, 8, 6, 12, 9]
    
    # Creating subplots with subplots()
    fig, (ax1, ax2) = plt.subplots(2, 1)
    ax1.plot(x, y1, marker='o', linestyle='-', color='b')
    ax1.set_title('Subplot 1')
    
    ax2.plot(x, y2, marker='s', linestyle='--', color='r')
    ax2.set_title('Subplot 2')
    
    # Adjusting layout
    plt.tight_layout()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/RgqI7uW.png
    

---

### Shared axes and layouts

- **Theory:**
    - Shared axes allow plots to share the same axis, facilitating comparison between plots.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y1 = [10, 15, 7, 10, 5]
    y2 = [5, 8, 6, 12, 9]
    
    # Creating subplots with shared x-axis
    fig, (ax1, ax2) = plt.subplots(2, 1, sharex=True)
    ax1.plot(x, y1, marker='o', linestyle='-', color='b')
    ax1.set_title('Subplot 1')
    
    ax2.plot(x, y2, marker='s', linestyle='--', color='r')
    ax2.set_title('Subplot 2')
    
    # Adjusting layout
    plt.tight_layout()
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    
    !https://i.imgur.com/CQoKXpH.png
    

---

These notes cover creating subplots, adjusting subplot spacing with `tight_layout()`, and using shared axes and layouts in Matplotlib. Let me know if there's anything else you'd like to add or modify!

Sure! Let's create concise notes for saving plots in Matplotlib, covering saving to different file formats, DPI settings, and transparent backgrounds:

---

## Matplotlib: Saving Plots

### Saving to file formats (PNG, JPEG, PDF)

- **Theory:**
    - Matplotlib allows you to save plots in various file formats such as PNG, JPEG, and PDF.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Adding labels and title
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.title('Line Plot Example')
    
    # Saving the plot as PNG
    plt.savefig('line_plot.png')
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    - The plot will be saved as `line_plot.png` in the current working directory.

### DPI settings (`dpi=` parameter)

- **Theory:**
    - DPI (Dots Per Inch) determines the resolution of the saved plot.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Saving the plot with custom DPI
    plt.savefig('line_plot_high_res.png', dpi=300)
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    - The plot will be saved as `line_plot_high_res.png` with a DPI of 300.

### Transparent backgrounds (`transparent=True`)

- **Theory:**
    - Setting `transparent=True` makes the background of the saved plot transparent.
- **Code:**
    
    ```python
    import matplotlib.pyplot as plt
    
    # Example data
    x = [1, 2, 3, 4, 5]
    y = [10, 15, 7, 10, 5]
    
    # Plotting a line plot
    plt.plot(x, y, marker='o', linestyle='-', color='b', label='Data')
    
    # Saving the plot with transparent background
    plt.savefig('line_plot_transparent.png', transparent=True)
    
    # Displaying the plot
    plt.show()
    
    ```
    
- **Output:**
    - The plot will be saved as `line_plot_transparent.png` with a transparent background.

---

These notes cover saving plots in Matplotlib to different file formats (PNG, JPEG, PDF), adjusting DPI settings, and creating plots with transparent backgrounds. Let me know if there's anything else you'd like to add or modify!

- **SciPy:** Scientific computing
    - Special functions
    - Integration
    - Optimization
    - Linear algebra
    - Statistics
- **Scikit-Learn:** Machine learning
    - Supervised learning (regression, classification)
    - Unsupervised learning (clustering, dimensionality reduction)
    - Model evaluation and validation
    - Preprocessing and pipelines
- **Frameworks:**
    - **Django:** Full-stack web development
    - **Flask:** Microframework for web applications
- **Concurrency:**
    - Using `threading` for multi-threading
    - Using `multiprocessing` for parallel processing
    - Asynchronous programming with `asyncio`
- **Testing:**
    - Writing unit tests with `unittest` or `pytest`
    - Test-driven development (TDD)
- **Network Programming:**
    - Using sockets for network communication
    - Making HTTP requests with `requests`
- **Web Scraping:**
    - Extracting data from web pages using `BeautifulSoup` and `Scrapy`
- **Data Serialization:**
    - Working with JSON, XML, and other data formats
- **Design Patterns:**
    - Understanding and implementing common design patterns in Python
- **Database Interaction:**
    - Using SQLite, PostgreSQL, MySQL with Python
    - ORM (Object-Relational Mapping) using SQLAlchemy
- **Security:**
    - Basic security principles
    - Implementing secure coding practices
    - Using cryptographic libraries (e.g., `hashlib`, `cryptography`)
- **GUI Programming:**
    - Creating graphical user interfaces with Tkinter or PyQt
- **Deployment:**
    - Packaging Python applications
    - Using tools like Docker for containerization
    - Deploying to cloud platforms (AWS, Heroku, etc.)
- **Type Hinting and Annotations:**
    - Using type hints for better code clarity and error checking
- **Logging:**
    - Implementing logging for debugging and monitoring
- **Profiling and Performance Tuning:**
    - Using profiling tools to optimize code performance
- **Version Control:**
    - Using Git for version control in Python projects
- **API Development:**
    - Creating RESTful APIs with Flask or Django
- **Microservices:**
    - Designing and implementing microservices architectures
