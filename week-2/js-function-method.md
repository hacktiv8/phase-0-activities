# JavaScript Function and Method

## Objectives

- ▢ Memahami pembuatan dan kegunaan function
- ▢ Memahami scope (global/local)
- ▢ Memahami recursion
- ▢ Melakukan type conversion
- ▢ Memahami exception and error handling

## Learnings

### Fungsi (Function)

Fungsi atau metode (metode) tentunya kita sudah pakai beberapa kali saat berlatih dengna tipe data dan objek. Ia bekerja baik dengan statement kondisi, sehingga kkita tidak perlu repot berulang kali memanggil/menulis beberapa baris kode yang sama atau berpola berulang kali.

Sebuah fungsi dibuat dengan ekspresi yang dimulai dengan kata kunci `function`. Fungsi dapat memiliki beberapa parameter (or argumen), atau bahkan tanpa parameter sama sekali. Fungsi dalam JS juga merupakan pendefinisian variabel umum yang mana nilainya adalah `function`.

```javascript
var printPrint = function() { // without parameter
  console.log("Print")
};
printPrint() // call it

var printStarred = function(text) { // with parameter
  console.log("★★★ " + text + " ★★★")
};
printStarred("Super Star")

function printCircle(text) { // shorthand to create function
  console.log("○○○ " + text + " ○○○")
}
printCircle("Circling Circle")
```

Wajarnya adalah fungsi perlu mengembalikan nilai (`return` a value) yang bisa kita ambil berikutnya. Seringkali kita ingin untuk mendapatkan nilai yang dikembalikan tersebut, maka kita assign ke sebuah variabel, di luar `function`.

```javascript
var timesTwo = function(x) {
  return x * 2;
};
var result = timesTwo(8) // 16
console.log(result)
```

Karena kebanyakan di JavaScript adalah object, kita tahu bahwa memungkinkan untuk mengakses beberapa dari hal-hal yang built-in seperti properties, functions, atau methods.

```javascript
> "This string".length
> "That string".charAt(0);  // access character
> "Hello world".substring(0, 5); // access more atau slice characters
> "x y z".split(" ") // split the string, producing an array of strings
```

Secara default inilah beberapa objek JS yang paling populer digunakan, beserta property atau method yang bisa kita akses.

- `Math`: `random()`, `PI`, `Math.max(a,b,...)`, dll
- `Date`: `getDate()`, `getDay()`, `getTime()`, dll

Temukan informasi lebih lanjut di referensi ya. :glasses:

### Cakupan (Scope)

JavaScript membedakan antara variabel global dan lokal. Function bisa dibuat di dalam function yang lain, menjadikan adanya beberapa derajat lokalitas (locality).

```javascript
var animal = function(food, water) {
  var eat = function(amount) {
    for (var food = 0; food < amount; food++)
      console.log("eating food")
  }
  var drink = function(amount) {
    for (var drink = 0; drink < amount; drink++)
      console.log("drinking")
  }
  eat(food)
  drink(water)
}
animal(3, 5) // outputs eating 3x dan drinking 5x
```

### Rekursi (Recursion)

Kita bisa membuat function yang memanggil dirinya sendiri, disebut recursion. Memungkinkan kita untuk menulis fungsi dengan ekspektasi hasil yang sama namun cara/gayanya berbeda. Ini akan berhubungan nanti tentang bagaimana kita menstrukturkan langkah logika kita, atau algorithm.

```javascript
// Fibonacci
function fib(n) {
  if (n == 0)
    return 0;
  if (n <= 2)
    return 1;
  return this.fib(n-1) + this.fib(n-2);
}
console.log(fib(8)) // 0, 1, 2, 3, 5, 8, 13, 21

// Perpangkatan
function power(base, exponent) {
  if (exponent == 0)
    return 1;
  else
    return base * power(base, exponent - 1);
}
console.log(power(3, 3)); // 3 ** 3 = 27
```

### Konversi Tipe Data (Type Conversion)

Telah kita ketahui bahwa kita bisa mengubah tipe data antara Number dan String dengan mudah hanya dengan assign nilai baru atau dengan operator. Ada cara lain yang lebih baik seperti menggunakan fungsi atau mendapatkan angka dari string dengan operator plus `+` (unary plus).

```javascript
> myNumber // 10.5
> myNumber.toString()  // "10.5"
> parseInt(myNumber)   // 10
> parseFloat(myNumber) // 10.5
> "8.8" + "8.8" // "8.88.8"
> (+"8.8") + (+"8.8") // 17.6
```

### Pengecualian (Exception) dan Penangan Galat (Error Handling)

Terkait dengan pengkondisian, kadang kala kita perlu menangani errot (juga disebut exception). Alur ini terdiri dari dua hal utama:

- `throw`: Melempar pengecualian (throw an exception), kita spesifikasikan ekspresi yang berisi nilai yang dingin kita lempar. Berguna untuk membuat error yang bisa kita buat sendiri(custom errors)
- `try...catch`: menandai blok statement untuk mencoba (`try`) sesuatu, dan menspesifikasikan satu atau lebih response yang akan menangkap exception. Maka jika exception dilempar, `try...catch` akan menangkapnya
  - `try`: mencoba atau mengetes block kode akan error
  - `catch`: menangani error
  - `finally`: menjalankan kode setelah `try` dan `catch`, dengan menghiraukan hasilnya

```javascript
try {
  throw "exception";
}
catch (e) {
  // statements to handle any exceptions
  console.error(e); // pass exception object to error handler
}
```

Bandingkan kedua kode berikut:

```javascript
function getMonthName(mo) {
  mo = mo - 1;
  var months = ["Jan","Feb","Mar","Apr","May","Jun","Jul",
                "Aug","Sep","Oct","Nov","Dec"];
  if (months[mo]) {
    return months[mo];
  } else {
    console.log("Invalid month number");
  }
}

var monthName = getMonthName(myMonth);
console.log(monthName)
```

dan

```javascript
function getMonthName(mo) {
  mo = mo - 1;
  var months = ["Jan","Feb","Mar","Apr","May","Jun","Jul",
                "Aug","Sep","Oct","Nov","Dec"];
  if (months[mo]) {
    return months[mo];
  } else {
    throw "InvalidMonthNo"; // throw an error
  }
}

try { // statements to try
  monthName = getMonthName(myMonth); // function that could throw exception
  console.log(monthName)
}
catch (e) {
  monthName = "unknown";
  console.error(e.message); // pass exception object to error handler, customize it
}
finally {
  console.log("Finished these logics!");
}
```

### References

- [Six ways to declare JavaScript functions by Dmitri Pavlutin](https://rainsoft.io/6-ways-to-declare-javascript-functions)
- [Learn JavaScript in Y Minutes](http://learnxinyminutes.com/docs/javascript)
- [JavaScript cheat sheet, by Marijn Haverbeke](http://marijnhaverbeke.nl/js-cheatsheet.html)
- [Javascript Cheat Sheet on OverAPI](http://overapi.com/javascript)
- [DevDocs JavaScript API Documentation](http://devdocs.io/javascript)
- [Understanding Asynchronous JavaScript Callbacks Through Household Chores, by Stephen Mayeux](https://medium.freecodecamp.com/understanding-asynchronous-javascript-callbacks-through-household-chores-e3de9a1dbd04)
