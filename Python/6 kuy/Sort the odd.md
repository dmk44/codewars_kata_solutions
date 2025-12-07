# Sort the odd
**DESCRIPTION**: You will be given an array of numbers. You have to sort the odd numbers in ascending order while leaving the even numbers at their original positions.

Examples
```
[7, 1]  =>  [1, 7]
[5, 8, 6, 3, 4]  =>  [3, 8, 6, 5, 4]
[9, 8, 7, 6, 5, 4, 3, 2, 1, 0]  =>  [1, 8, 3, 6, 5, 4, 7, 2, 9, 0]
```
## Solution
```py
def sort_array(arr):
    nechet = sorted([x for x in arr if x%2==1])
    chet = list(map(lambda x: x if x%2==0 else "_", arr))
    for el in range(len(chet)):
        if chet[el] == "_":
            try:
                chet[el] = nechet.pop(0)
            except:
                continue
    
    return chet
```