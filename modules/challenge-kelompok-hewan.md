# Logic Challenge - Mengelompokkan Hewan

## Problem

Diberikan sebuah function groupAnimals(arr) yang menerima satu parameter berupa array yang berisi string. Function akan me-return array multidimensi dimana array tersebut berisikan kategori/kelompok array yang dikumpulkan sesuai dengan abjad depannya. Abjad harus berurut dari a-z (jika ada). Untuk kasus ini, anggap saja semua text lowercase.

 Contoh jika `animals` adalah `["ayam", "kucing", "bebek", "bangau", "zebra"]`
 
 maka akan menampilkan output: `[ [ "ayam" ], [ "bebek", "bangau" ], [ "kucing ], [ "zebra" ] ]`

Urutan hewan dalam array setiap pengelompokan huruf tidak penting.

## Code

```JavaScript
function groupAnimals(animals) {
  // you can only write your code here!
}

// TEST CASES
console.log(groupAnimals(['cacing', 'ayam', 'kuda', 'anoa', 'kancil']));
// [ ['ayam', 'anoa'], ['cacing'], ['kuda', 'kancil'] ]
console.log(groupAnimals(['cacing', 'ayam', 'kuda', 'anoa', 'kancil', 'unta', 'cicak' ]));
// [ ['ayam', 'anoa'], ['cacing', 'cicak'], ['kuda'], ['unta'] ]
```
