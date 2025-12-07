# Snail
**DESCRIPTION**: Snail Sort
Given an n x n array, return the array elements arranged from outermost elements to the middle element, traveling clockwise.
```
array = [[1,2,3],
         [4,5,6],
         [7,8,9]]
snail(array) #=> [1,2,3,6,9,8,7,4,5]
```
For better understanding, please follow the numbers of the next array consecutively:
```
array = [[1,2,3],
         [8,9,4],
         [7,6,5]]
snail(array) #=> [1,2,3,4,5,6,7,8,9]
```
## Solution 1
```JS
function snail(array) {

    let result = new Array();

    let up = 0;
    let down = array.length - 1;
    let left = 0;
    let right = array[0].length - 1;

    while (up <= down & left <= right) {
        for (var i = left; i<=right; i++) result.push(array[up][i]);
        up += 1;

        for (var i=up; i<=down; i++) result.push(array[i][right]);
        right -= 1;

        if (up <= down) {
            for (var i = right; i>= left; i--) result.push(array[down][i]);
            down -= 1;
        }

        if (left <= right) {
            for (var i = down; i>= up; i--) result.push(array[i][left]);
            left += 1;
        }
            
    }
    return result;
}
```

## Solution 2
```js
function snail(array) {

    let result = new Array();

    let up = 0;
    let down = array.length - 1;
    let left = 0;
    let right = array[0].length - 1;

    while (up <= down & left <= right) {
        for (var i = left; i<=right; i++) result.push(array[up][i]);
        up += 1;

        for (var i=up; i<=down; i++) result.push(array[i][right]);
        right -= 1;

        if (up <= down) {
            for (let i = right; i>= left; i--) result.push(array[down][i]);
            down -= 1;
        }

        if (left <= right) {
            for (let i = down; i>= up; i--) result.push(array[i][left]);
            left += 1;
        }
            
    }
    return result;
}
```