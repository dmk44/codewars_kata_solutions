# Summing a number's digits
**DESCRIPTION**: Write a function which takes a number as input and returns the sum of the absolute value of each of the number's decimal digits.

For example: (Input --> Output)
```
10 --> 1
99 --> 18
-32 --> 5
```
Let's assume that all numbers in the input will be integer values.
## Solution
```JS
const sumDigits = x => String(Math.abs(x)).split("").reduce((sum, num) => sum + Number(num), 0)
```