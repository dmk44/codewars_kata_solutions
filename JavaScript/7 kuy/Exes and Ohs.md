# Exes and Ohs
**DESCRIPTION**: Check to see if a string has the same amount of `'x'`s and `'o'`s. The method must return a boolean and be case insensitive. The string can contain any char.

Examples input/output:
```
XO("ooxx") => true
XO("xooxx") => false
XO("ooxXm") => true
XO("zpzpzpp") => true // when no 'x' and 'o' is present should return true
XO("zzoo") => false
```
## Solution
```JS
function XO(str) {
    str = str.split("");
    return str.map((x => x === "X" || x === "x" ? 1 : 0)).reduce((sum, num) => sum + num, 0) === str.map((x => x === "O" || x === "o" ? 1 : 0)).reduce((sum, num) => sum + num, 0) ;
}
```