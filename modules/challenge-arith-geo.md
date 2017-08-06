# Logic Challenge - Tentukan Deret

## Problem

Diberikan sebuah function tentukanDeret(arr) yang menerima satu parameter berupa array yang terdiri dari angka. Function tersebut akan mengembalikan `true` jika array dari parameter tersebut merupakan deret aritmatika. Deret aritmatika adalah sebuah deret dimana perbedaan setiap angka di deret tersebut konsisten. Contoh, [2, 4, 6, 8] adalah deret aritmatika dengan pertambahan nilai sebesar 2, dan [2, 4, 6, 9] bukanlah deret aritmatika karena tidak perbedaan selisih antar angka yang tidak konsisten.


## Code

```JavaScript
function tentukanDeret(num) {
  // you can only write your code here!
}

// TEST CASES
console.log(tentukanDeret([1, 2, 3, 4, 5, 6])); // true
console.log(tentukanDeret([2, 4, 6, 12, 24])); // false
console.log(tentukanDeret([2, 4, 6, 8])); // true
console.log(tentukanDeret([2, 6, 18, 54])); // false
console.log(tentukanDeret([1, 2, 3, 4, 7, 9])); // false
```
