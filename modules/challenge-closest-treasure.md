# Logic Challenge - Nearest Treasure

## Problem

Have the function nearestTreasure(arr) take the array of numbers stored in arr and from the position in the array where a 1 is, return the number of spaces either left or right you must move to reach a treasure which is represented by a 2. For example: if arr is [0, 0, 1, 0, 0, 2, 0, 2] then your program should return 3 because the closest treasure (2) is 3 spaces away from the 1. The array will contain any number of 0's and 2's, but only a single 1. It may not contain any 2's at all as well, where in that case your program should return a 0.

## Code

```JavaScript
function nearestTreasure(num) {
  // you can only write your code here!
}

// TEST CASES
console.log(nearestTreasure([0, 0, 1, 0, 0, 2, 0, 2])); // 3
console.log(nearestTreasure([1, 0, 0, 0, 2, 2, 2])); // 4
console.log(nearestTreasure([2, 0, 0, 0, 2, 2, 1, 0])); // 1
console.log(nearestTreasure([0, 0, 1, 0])); // 0
console.log(nearestTreasure([0, 1, 0, 2, 2, 0, 0, 2])); // 2
```
