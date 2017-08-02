# Lesson 3 - Functions

## Overview

### Functions
Functions are reusable named sections of code that can take input and perform a particular action and can return new
information.

#### Creating functions
Functions are created by using the `def` keyword then providing a valid name and a list of `parameters`. If something
needs to be returned from the function use the `return` keyword followed by the value to be returned.

```python
def functionName(parameter1, parameter2, ..., paramterN):
    # code goes here
    return value
```

Note: that once `return` is reached the function will immediately end. Also `return` does not require a value.

#### Calling Functions
// TODO: write more about calling functions

```python
def printHelloWorld():
    print("Hello World")
    
printHelloWorld()
```

#### Parameters and Arguments
When defining a `function`, `parameters` for that function can also be defined. A `parameter` is a variable that will
be given a value when the function is called.
```python
def hello(name):
    print("Hello,", name)
    
def helloAdvanced(name1, name2):
    print("Hello,", name1, "I am", name2)
    
hello("Jojo")
# Hello, Jojo

helloAdvanced("Jojo", "Dio")
# "Hello, Jojo I am Dio
```

// TODO: write more about parameters and arguments
  
#### Examples
```python
def addTwoNumbers(number1, number2):
    return number1 + number2

def solveTriangle(a, b):
    c = (a ** 2 + b ** 2) ** 0.5
    return c

def getBanana():
    return "Banana"

def main():
    print(addTwoNumbers(2, 2))
    print(solveTriangle(3, 4))
    print(getBanana())
```

#### Best Practices
Functions should:
- be small, 1 to 20 ish lines
- only do one thing
- named like verbs or actions

### Dictionary

// TODO: Write about dictionaries