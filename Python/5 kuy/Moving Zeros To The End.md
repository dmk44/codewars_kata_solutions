# Moving Zeros To The End
**DESCRIPTION:**
Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.
```
move_zeros([1, 0, 1, 2, 0, 1, 3]) # returns [1, 1, 2, 1, 3, 0, 0]
```

## Solution
```Python
def move_zeros(lust):
    cunt = lust.count(0)

    while cunt:
        lust.append(lust.pop(lust.index(0)))
        cunt -=1


    return lust
```