# Replace With Alphabet Position
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
function alphabetPosition(text) {
    const alpha = new Array(26).fill(1).map((_, i) => String.fromCharCode(97 + i));
    text = text.toLowerCase().split("").filter((x => x.toLowerCase() != x.toUpperCase()));
    return text.map(x => alpha.indexOf(x) + 1).join(" ");
}
```