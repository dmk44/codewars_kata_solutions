# Multiplication table
**DESCRIPTION**: Your task, is to create N×N multiplication table, of size provided in parameter.

For example, when given size is `3`:
```
1 2 3
2 4 6
3 6 9
```
For the given example, the return value should be:
```
[[1,2,3],[2,4,6],[3,6,9]]
```
## Solution
```JS
function multiplicationTable(size) {
    let multiplicationTable = [];
  
    Array.from({ length: size }).forEach((_, i) => {
      let row = [];
      Array.from({ length: size }).forEach((_, j) => {
        row.push((i + 1) * (j + 1));
      });
      multiplicationTable.push(row);
    });
  
    return multiplicationTable;
  }
```