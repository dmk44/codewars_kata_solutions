# Next bigger number with the same digits
**DESCRIPTION**: Create a function that takes a positive integer and returns the next bigger number that can be formed by rearranging its digits. For example:
```
  12 ==> 21
 513 ==> 531
2017 ==> 2071
```
If the digits can't be rearranged to form a bigger number, return -1 (or nil in Swift, None in Rust):
```
  9 ==> -1
111 ==> -1
531 ==> -1
```
## Solution
```py
def next_bigger(n):
    digs = list(str(n))
    

    i = len(digs) - 2
    while i >= 0 and digs[i] >= digs[i + 1]:
        i -= 1
    
    if i == -1: return -1

    j = len(digs) - 1
    while digs[j] <= digs[i]:
        j -= 1
    
    digs[i], digs[j] = digs[j], digs[i]
    
    digs = digs[:i + 1] + sorted(digs[i + 1:])
    
    return int(''.join(digs))
```