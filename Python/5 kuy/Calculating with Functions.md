# Calculating with Functions

**DESCRIPTION:**

This time we want to write calculations using functions and get the results. Let's have a look at some examples:
```
seven(times(five())) # must return 35
four(plus(nine())) # must return 13
eight(minus(three())) # must return 5
six(divided_by(two())) # must return 3
```
**Requirements:**

There must be a function for each number from 0 ("zero") to 9 ("nine")
There must be a function for each of the following mathematical operations: `plus`, `minus`, `times`, `divided_by`
Each calculation consist of exactly one operation and two numbers
The most outer function represents the left operand, the most inner function represents the right operand
Division should be integer division. For example, this should return `2`, not `2.666666...`:

`eight(divided_by(three()))`

## Solution

```python
def plus(x):
    return lambda y: x + y

def minus(x):
    return lambda y: y - x

def times(x):
    return lambda y: y * x

def divided_by(x):
    return lambda y: y // x


def zero(f = None): 
    if f == None:
        return 0
    else: return f(0)
    
def one(f = None): 
    if f == None:
        return 1
    else: return f(1)

def two(f = None): 
    if f == None:
        return 2
    else: return f(2)

def three(f = None): 
    if f == None:
        return 3
    else: return f(3)

def four(f = None): 
    if f == None:
        return 4
    else: return f(4)

def five(f = None): 
    if f == None:
        return 5
    else: return f(5)

def six(f = None): 
    if f == None:
        return 6
    else: return f(6)

def seven(f = None): 
    if f == None:
        return 7
    else: return f(7)

def eight(f = None): 
    if f == None:
        return 8
    else: return f(8)

def nine(f = None): 
    if f == None:
        return 9
    else: return f(9)
```