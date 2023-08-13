# Square(n) Sum

Complete the square sum function so that it squares each number passed into it and then sums the results together.

For example, for `[1, 2, 2]` it should return 9 because 

$$1^2 + 2^2 + 3 ^2 = 9$$

## Solution

```R
square_sum <- function(nums) {
  return(sum(nums ^ 2))
}
```