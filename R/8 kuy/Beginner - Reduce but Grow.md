# Beginner - Reduce but Grow
**DESCRIPTION:**

Given a non-empty array of integers, return the result of multiplying the values together in order. Example:
```
[1, 2, 3, 4] => 1 * 2 * 3 * 4 = 24
```
## Solution

```R
grow <- function(arr) {
  prod = 1
  for (i in arr) prod <- prod * i
    return(prod)
  }
```