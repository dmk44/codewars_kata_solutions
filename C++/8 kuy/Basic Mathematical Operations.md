# Basic Mathematical Operations

**DESCRIPTION:**

Your task is to create a function that does four basic mathematical operations.

The function should take three arguments - operation(string/char), value1(number), value2(number).
The function should return result of numbers after applying the chosen operation.

**Examples**
(Operator, value1, value2) --> output

`('+', 4, 7) --> 11`

`('-', 15, 18) --> -3`

`('*', 5, 5) --> 25`

`('/', 49, 7) --> 7`

## Solution

```c++
int basicOp(char op, int a, int b) {
  switch (op) {
    case '+':
    return a+b;
    break;
    case '-':
    return a-b;
    break;
    case '/':
    return a/b;
    break;
    case '*':
    return a*b;
    break;
  }
}
```
