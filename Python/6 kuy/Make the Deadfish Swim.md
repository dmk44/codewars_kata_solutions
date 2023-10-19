# Make the Deadfish Swim
**DESCRIPTION:**

Write a simple parser that will parse and run Deadfish.

Deadfish has 4 commands, each 1 character long:

* i increments the value (initially 0)
* d decrements the value
* s squares the value
* o outputs the value into the return array

Invalid characters should be ignored.
```
parse("iiisdoso")  ==>  [8, 64]
```

## Solution
```Python
def parse(data):
    ms = []
    ch = 0
    for s in data:
        
        
        if s == "i": 
            ch += 1
            continue
        if s == "d": 
            ch -= 1
            continue
        if s == "s": 
            ch = ch ** 2
            continue
        if s == "o": 
            ms.append(ch)
            continue
    return ms
```