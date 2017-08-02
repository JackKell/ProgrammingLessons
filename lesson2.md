# Lesson 2 - Lists and Control Flow

## Overview

### Lists

#### Creating Lists

To create a `list` from scratch simply:
 ```python
 # listName = [element1, element2, ..., elementN]
 aEmptyList = []
 aListOfEvenNumbers = [2, 4, 6, 8]
 aListOfNames = ["Jimmy", "Bob", "Frank"]
 aListOfLists = [aListOfEvenNumbers, aListOfNames]
```

Note that lists can contain any data type `integers`, `floats`, `strings`, and even `lists`. Additionally, Python 
provides a unique feature where lists do no need even need to be comprised of the same data type. 

```python
aListOfABunchOfStuff = ["Cat", 42, 1.743532, [1, 2, 3]]
```
Although one *can* create `lists` of a bunch of stuff of different data types it is normally bad practice to create a 
list that hold many different types of information. There are much better  ways to organize complex information that
will get into later.

#### How Lists Work
An example of a lists that we have already worked with is a `string`.
```python
name = "Jimmy"
# position   1    2    3    4    5 
# index      0    1    2    3    4 
# element   'J', 'i', 'm', 'm', 'y'
```
Each `character` in the `string` can be refereed to as an `element` in the `list`. 
The `position` of an `element` describes its point in the list using standard english. So if you said, "Give me the 1st
`element` in the `list`" it would return `'J'`. Now in most programming languages the position for elements starts at 0 
instead of 1. This number is called an `index` and it is what is used to communicate the position to the computer. 

#### Indexing
So one wanted the first `element` in the `list` one would have to provide an `index` of 0 to get the 
value of `'J'`.

To actually retrieve an `element` from a `list`:
```python
name = "Jimmy"
# listName[index]
name[0]
# 'J'
```

## Control Flow

Control flow gives a program the ability to run code in a more complex order than simple top to bottom. A good way to 
think about is codes is like a cooking recipe that you give to a computer. You can design the recipe to be completed one 
each step at a time completing each step in order but often it is easier to write things into the recipe like: 

+ "If potato is large then cut it into 8ths instead of 4ths"
+ "Go to step 5"
+ "Cook until golden brown"
+ "Repeat steps 3 through 5 until cooked"
+ "Do steps 1 and 2 four times for each batch".

All of these cooking example represent the control that a writer (the programmer) has to control what the reader 
(computer) to determine does next.

### If Else

An `if` statement is used to make a decision. An `if` statement takes a `boolean` as input and uses it to determine 
which `code block` should be executed. If the condition is `True` it will enter `code block` otherwise the code will not
be run at all.

```python
condition = True

if condition:
    print("Enter here if condition is True")
# No matter what decision is made the code continues running from this point onward after the if block is done
```

Additionally an `else` statement can be used after a `if` statement to run a different code in the event that the
condition for the `if` statement is `False`

```python
condition = True

if condition:
    print("Enter here if condition is True")
else:
    print("Enter here if condition is False")
# No matter what decision is made the code continues running from this point onward after the if block is done
```

Furthermore one can add a `elif` statement to check more than one state of the condition.

```python
iceCreamChoice = "Strawberry"

if iceCreamChoice == "Chocolate":
    print("CHOCOLATE!!!!!")
elif iceCreamChoice == "Vanilla":
    print("Yay vanilla is pretty good")
elif iceCreamChoice == "Strawberry":
    print("Strawberry is the best")
else:
    print("On I have not heard of that ice cream type before. :/")
```

Note that the order is important, the `if` must come first, all `elif`s must come after the `if` and before the `else` 
and have their own conditional statements, and the `else` statement must come last. Also the `else` statement will only
run if none of the `if` or `elif` conditions are met.

#### Examples

Simple example

```python
personAge = 16

# Determine if the person is old enough to go watch the R-rated movie
if personAge >= 17:
    print("Sure have fun")
else:
    print("No you can't see the movie")
```

More complex example

```python
personAge = 16

# Determine what the person should pay for the movie based on their age
if personAge <= 13:
    print("That will be $3 chum")
elif personAge <= 18:
    print("That will be $7 bud")
elif personAge <= 64:
    print("That will be $12 there friend")
else:
    print("It's only $4")
```

### Foreach
`Foreach` loops are used when one has a predefined list of things and you want go through each `element` individually.
To use the cooking metaphor again, a `Foreach` statement is similar to saying:

 > "Take each egg and crack it open into the bowl."

A `Foreach` loop takes a variable name that represents the current `element` and a list of items to iterate through.
Note that in Python there is **not** a true "*Foreach*" keyword. In Python, the `for` keyword is used, but it has a very
similar behaviour to how `foreach` loops function in other languages.
```python
for element in elements:
    # do something with the element
```

#### Examples
Printing a list of numbers.

```python
aListOfNumbers = [1, 2, 3]

for number in aListOfNumbers:
    print(number)
```
Output
```
1
2
3
```

Finding a total from a list of numbers
```python
prices = [5.99, 20.00, 16.53]
total = 0
for price in prices:
    total += price
print("$", total)
```

Output

```
$42.52
```


### For Loop

`For` loops are generally used when one has a predefined list of things to iterate through but the position of each element is
needed. Normally to create a "traditional" `for` loop one uses the `range()` function which creates a list of numbers
from a given starting value to a given ending value minus 1.
```python
print(list(range(0, 10)))
```
Output:
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

A Basic `for` loop.

```python
for i in range(0, 5):
    print(i)
```

Output:

```
0
1
2
3
4
```

#### Examples
Print the numbers in a list using a `for` loop. Note: That the `len()` is used to get the length of any given list. So 
if the `len()` function was given the list `[8, 9, 3, 2, 6, 7]` the length function would return `6`.
```python
aListOfNumbers = [2, 1, 4, 3, 7, 8, 9, 3]
for i in range(0, len(aListOfNumbers)):
    print(aListOfNumbers[i])
```

### While
`While` loops are used when the number of times a code block needs to be repeated is unknown. A `while` loop is repeated
if the condition within the `while` statement is `true`. 

Something that is really easy to do with a `while` is to create an infinite loop. An infinite loop is a type of loop
that never ends. The resulting example would print "Hey" to the screen forever. If you do run this code in your command
line to end it you can use `crlt + c` to cancel the program.
```python
# WARNING: Infinite loop incoming
condition = True

while condition:
    print("Hey")
```

#### Examples 
````python
counter = 0
while counter < 10:
    counter += 1
    print(counter)
````