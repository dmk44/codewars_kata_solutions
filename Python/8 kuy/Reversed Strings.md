# Reversed Strings

Complete the solution so that it reverses the string passed into it.

`'world'  =>  'dlrow'`

`'word'   =>  'drow'`

## Solution

```python
def solution(string):
    string = string[::-1]
    return string
```