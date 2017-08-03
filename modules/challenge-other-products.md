# Logic Challenge - Other Products

## Problem

Have the function OtherProducts(arr) take the array of numbers stored in arr and return a new list of the products of all the other numbers in the array for each element. For example: if arr is [1, 2, 3, 4, 5] then the new array, where each location in the new array is the product of all other elements, is [120, 60, 40, 30, 24]. The following calculations were performed to get this answer: [(2*3*4*5), (1*3*4*5), (1*2*4*5), (1*2*3*5), (1*2*3*4)]. You should generate this new array. The array will contain at most 10 elements and at least 1 element of only positive integers.

## Code

```JavaScript
function otherProducts(arr) {
  // you can only write your code here!
}

// TEST CASES
console.log(otherProducts([2, 4, 6])); // [24, 12, 8]
console.log(otherProducts([1, 2, 3, 4, 5])); // [120, 60, 40, 30, 24]
console.log(otherProducts([1, 4, 3, 2, 5])); // [120, 30, 40, 60, 24]
console.log(otherProducts([1, 3, 3, 1])); // [9, 3, 3, 9]
console.log(otherProducts([2, 1, 8, 10, 2])); // [160, 320, 40, 32, 160]
```
