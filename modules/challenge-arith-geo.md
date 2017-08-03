# Logic Challenge - Arith Geo

## Problem

Have the function ArithGeo(arr) take the array of numbers stored in arr and return the string "Arithmetic" if the sequence follows an arithmetic pattern or return "Geometric" if it follows a geometric pattern. If the sequence doesn't follow either pattern return -1. An arithmetic sequence is one where the difference between each of the numbers is consistent, where as in a geometric sequence, each term after the first is multiplied by some constant or common ratio. Arithmetic example: [2, 4, 6, 8] and Geometric example: [2, 6, 18, 54]. Negative numbers may be entered as parameters, 0 will not be entered, and no array will contain all the same elements.

## Code

```JavaScript
function ArithGeo(num) {
  // you can only write your code here!
}

// TEST CASES
console.log(ArithGeo([1, 2, 3, 4, 5, 6])); // "Arithmetic"
console.log(ArithGeo([2, 4, 6, 12, 24])); // "Geometric"
console.log(ArithGeo([2, 4, 6, 8])); // "Arithmetic"
console.log(ArithGeo([2, 6, 18, 54])); // "Geometric"
console.log(ArithGeo([1, 2, 3, 4, 7, 9])); // -1
```
