# Logic Challenge: Melee Ranged Grouping

Diberikan function meleeRangedGrouping yang menerima 1 parameter berupa string, implementasikan
meleeRangedGrouping agar dapat menghasilkan multidimensional array seperti yang diminta.

Format string yang diberikan adalah:
<nama_hero>-<tipe_hero>,<nama_hero>-<tipe-hero>, ...

Output yang diharapkan:
[ [ <daftar hero dengan tipe ranged> ], [ <daftar hero dengan tipe melee> ] ]

Jika input adalah string kosong ('') maka return array kosong

```JavaScript
function meleeRangedGrouping (str) {
  //your code here
}

// TEST CASE

console.log(meleeRangedGrouping('Razor-Ranged,Invoker-Ranged,Meepo-Melee,Axe-Melee,Sniper-Ranged'));
// [ ['Razor', 'Invoker', 'Sniper'], ['Meepo', 'Axe'] ]

console.log(meleeRangedGrouping('Drow Ranger-Ranged,Chen-Ranged,Dazzle-Ranged,Io-Ranged'));
// [ ['Drow Ranger', 'Chen', 'Dazzle', 'Io'], [] ]

console.log(meleeRangedGrouping('')); // []
```
