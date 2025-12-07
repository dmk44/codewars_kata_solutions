# Build Tower
**DESCRIPTION**: Build Tower
Build a pyramid-shaped tower, as an array/list of strings, given a positive integer number of floors. A tower block is represented with "*" character.

For example, a tower with 3 floors looks like this:
```
[
  "  *  ",
  " *** ", 
  "*****"
]
```
And a tower with 6 floors looks like this:
```
[
  "     *     ", 
  "    ***    ", 
  "   *****   ", 
  "  *******  ", 
  " ********* ", 
  "***********"
]
```
Go challenge Build Tower Advanced once you have finished this :)
## Solution
```JS
function towerBuilder(floors) {
  let tower = [];
  for (let i = 0; i < floors; i++) {
    let spaces = " ".repeat(floors - i - 1);
    let stars = "*".repeat(2 * i + 1);
    tower.push(spaces + stars + spaces);
  }
  return tower;
}
```