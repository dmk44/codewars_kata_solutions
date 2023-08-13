# Name Shuffler

**DESCRIPTION:**

Write a function that returns a string in which firstname is swapped with last name.

**Example(Input --> Output)**

`"john McClane" --> "McClane john"`

## Solution

```javascript
const nameShuffler = (name) => name.split(' ').reverse().join(" ");
```
