# Simple Fun #159: Middle Permutation
**DESCRIPTION**:
You are given a string `s`. Every letter in `s` appears once.

Consider all strings formed by rearranging the letters in s. After ordering these strings in dictionary order, return the middle term. (If the sequence has a even length n, define its middle term to be the (n/2)th term.)

Example

For `s = "abc"`, the result should be `"bac"`.

 The permutations in order are: `"abc", "acb", "bac", "bca", "cab", "cba"` So, The middle term is `"bac`".

Input/Output
`[input]` string `s`
unique letters `(2 <= length <= 26)`

`[output] `a string
middle permutation.
## Solution
```py
import math

def middle_permutation(s):
    from math import factorial
    s = sorted(s)
    n = len(s)
    mid_index = factorial(n) // 2 - 1
    result = []
    for i in range(n):
        fact = math.factorial(n - 1)
        index = mid_index // fact
        result.append(s.pop(index))
        mid_index %= fact
        n -= 1
    return ''.join(result)
```