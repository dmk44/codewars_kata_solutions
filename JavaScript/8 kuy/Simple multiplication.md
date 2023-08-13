# Simple multiplication

This kata is about multiplying a given number by eight if it is an even number and by nine otherwise.

## Solution

```javascript
const simpleMultiplication = number => !(number % 2) ? number * 8 : number * 9;
```