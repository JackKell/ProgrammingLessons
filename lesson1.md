# Lesson 1 - Basic Operators, Primitive Data Types, and Intro to Variables

## Summary
// TODO: write summary of the lesson


## Understanding the Examples
Note that the examples in this lesson will be written to emulate Python's IDLE. IDLE is a application that enables a user to directly interact with the Python interpreter in real time. IDLE is used in these examples because it allows you to jump right into programming in Python without needing to understand how to run a Python file (all of that will come in later lessons). 

To run idle your self follow these instructions:

1. Click in Window's Search bar
2. Type, "IDLE"
3. Click, "IDLE" application or press enter
4. Idle will come up and you will be able to simply type Python syntax into the shell as is shown in the examples.

Example example:
```python
>>>  1 + 1
2
```

## Primitive/Simple Data Types
In Python (and most other programming languages) data is categorized into several different types. The type of the data determines how much space it takes up in memory and how different operations affect data.
### Types
#### Integer
**Integer**s or **int**s can be thought of as the standard counting numbers [... -3, -2, -1, 0, 1, 2, 3, ...]. 
```python
>>> type(3)
<class 'int'>
>>> type(-4)
<class 'int'>
```
#### Float
**Floats** (sometimes called **single**s) represent decimal numbers such as 0.5, 1.0, or -12.34.
```python
>>> type(1.9)
<class 'float'>
>>> type(0.5)
<class 'float'>
>>> type(2.0)
<class 'float'>
```
#### Boolean
**Boolean**s or **bool**s are used when data can either be **True** or **False**. In the internals of Python, things that are **True** are represent by a **1** where as things that are **False** are represented by a **0**.
```python
>>> type(True)
<class 'bool'>
>>> type(False)
<class 'bool'>
```
#### String
**String**s or **str**s in the simplest terms are used to represent words and symbols. In more *programmery* terms, a string is a list of **character**s and a **character** (also called a **char**) is a single symbol normally in the [ASCII](https://en.wikipedia.org/wiki/ASCII) or [UNICODE](https://en.wikipedia.org/wiki/Unicode) sets. Although in Python, a **character** is 	*not* a data type, instead a **string** is composed of a given number of **string**s that each have a length of 1. Additionally, although **character**s are not true data types in Python they are still important to understand how **string**s works and for understanding **character**s in other programming languages.  

When **string**s are made the standard is to use ""s (double quotes) even though in Python **string**s can also be created using ''s (single quotes) but, in most languages ''s are reserved for creating **character**s and not **string**s. For this reason, I recommend sticking with ""s for making **string**s in Python and when you want to treat something *like* a **character** use double quotes. Although there are a few **character**s that you cannot simply type in a string and these characters are know as, "[Escape Characters](https://docs.python.org/3.6/reference/lexical_analysis.html#literals)" but we will get into those a bit later. 
```python
>>> type("")
<class 'str'>
>>> type("Hello World")
<class 'str'>
>>> type("Cat")
<class 'str'>
>>> type("1234567890 Hey $5@#")
<class 'str'>
```
#### NoneType
The only value in Python that has a data type of **NoneType** is the keyword constant **None**. **None** is used when one wants to show that a given piece of data has no value. 
```python
>>> type(None)
<class 'NoneType'>
```
Note that **None** should not be confused with something 0 (a common mistake to make). In Python, **None** is meant to represent the idea of having no value whereas 0 has a value of 0 not nothing (if that makes sense). No need to worry about it too much now (if you don't understand) we will get more into it more later. 

#### Other Data Types
Now there are several other data types that I have omitted here as other data types are a bit more complex and require their own explanations later but, if you are interested in seeing them now or more detailed information about the data types that have already been mention check out the documentation [here](https://docs.python.org/3.6/library/stdtypes.html).

## Operators

### Basic Arithmetic Operators
Python, like almost all programming languages, have most of the basic mathematical operators built into the language.  For example:

#### Addition:
```python
>>> 5 + 5
10
```
#### Subtraction
```python
>>> 5 - 5
0
```
#### Multiplication
```python
>>> 5 * 5
25
```
#### Division
```python
>>> 5 / 5
1.0
```

#### Exponents
```python
>>> 5 ** 2
25
```

### Logical Operators
Logical operators compare two Booleans (data that is either true or false) and returns a Boolean.

#### And
The add operator will only return True when both Boolean operators are True. The and operator is represented by using the **and** keyword or the **&** (ampersand) symbol. I recommend using the **&** as it is more comparable to other programming languages.
```python
>>> True and True
True
>>> True & True
True
>>> True & False
False
>>> False & True
False
>>> False & False
False
```

#### Or
```python
>>> True or True
True
>>> True | True
True
>>> True | False
True
>>> False | True
True
>>> False | False
False
```

#### Not
```python
>>> not True
False
>>> not False
True
```

### Comparison Operators
Comparison operators take two similar things like two number and returns a Boolean of True or False.

#### Greater Than (>)
```python
>>> 4 > 5
False
>>> 5 > 5
False
>>> 5 > 6
False
>>> 6 > 5
True
```
#### Less Than (<)
```python
>>> 4 < 5
True
>>> 5 < 5
False
>>> 5 < 6
False
>>> 6 < 5
False
```
#### Equal Too (==)
```python
>>> 5 == 5
True
>>> 6 == 5
False
```
#### Not Equal To (!=)
```python
>>> 5 != 5
False
>>> 6 != 5
True
```
#### Greater Than Or Equal To (>=)
```python
>>> 4 >= 5
False
>>> 5 >= 5
True
>>> 5 >= 6
False
>>> 6 >= 5
True
```
#### Less Than Or Equal To (<=)
```python
>>> 4 <= 5
True
>>> 5 <= 5
True
>>> 5 <= 6
True
>>> 6 <= 5
False
```

## Variables
In simple terms a variable is named location in a computer's memory that holds a value. 

### Creating a Variable
A variable can be created by doing something like the following example:
```python
>>> foo = 5
```
Where, "foo" is the name of the variable and "5" is the value (or the data) that the variable holds.

### Using Variables
After a variable has been created (or instantiated to use those *programmery* terms again) it can be 
 
### Assignment Operators
Assignment operators allow one to set or change the value of a variable. 
 
#### Equals (=)
The equal sign is used to set the value of a variable equal to whatever is return on the right side of the equals sign (As seen in the section, "Creating a Variable"). This is an operator that is used often in most programming languages so it is important to become comfortable with its use. The following are all examples of how to use the **=** operator.
```python
>>> a = 5
>>> b = 2 + 3
>>> c = "234"
>>> d = False
```

#### Add Equals (+=)
```python

```

#### Subtract Equals (-=)
```python
```

#### Multiply Equals (*=)
```python
```

#### Divide Equals (/=)
```python
```

### Naming Variables
The name of a variable can be anything as long as it: 
- does **not** contain special characters (such as &, $, %, +, etc.),
- contains **no** spaces,
- or **starts** with a **number**.

#### Invalid Name Examples
For example all of the following variable names below are not permitted:
```python
>>> 555foo = 10
SyntaxError: invalid syntax
>>> fo&o = 10
SyntaxError: can't assign to operator
>>> foo\ = 10
SyntaxError: unexpected character after line continuation character
>>> $foo = 10
SyntaxError: invalid syntax
>>> foo bar = 1321
SyntaxError: invalid syntax
```

#### Valid Name Examples
```python
>>> foo1 = 10
>>> bar = 10
>>> aNewVariable = 123
```

#### Best Practices
1. In Python it is normally good practice to name variables using [camel case](https://en.wikipedia.org/wiki/Camel_case) where the beginning of each word (expect for the first word) is capitalized.
```python
thisIsCamelCase
thisisnotcamelcase
```
2. Additionally, When naming variables it is important to make sure that the variable's names makes sense as to what kind of information the variable is holding. A general rule of thumb is when a variable is holding a certain data type the name of that variable should invoke the idea of that data type.</br>For example, if one wanted to store the number of apples that a person had what should the variable be called? As a programmer, is it totally your decision what to call the variable and there are no wrong answers (but some answers are often more right than others). Some good names for this variable could be, "totalApples" or "numberOfApples" or something to that effect. These names to single to other developers (and yourself later) that this variable is in fact holding a number.

##### Good Variable Name Examples:
 ```python
 >>> numberOfDogs = 2
 >>> isRunning = True
 >>> playerName = "Jimmy"
```
