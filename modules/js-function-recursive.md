# JavaScript Recursive Function

## Objectives

- ▢ Mengenal pembuatan dan cara kerja fungsi Rekursif
- ▢ Memahami cara membuat fungsi rekursif sederhana

## Learnings

### Fungsi (Function) Review

Sedikit kita review apa yang telah kita pelajari minggu lalu, fungsi atau metode (metode) tentunya kita sudah pakai beberapa kali saat berlatih dengna tipe data dan objek. Ia bekerja baik dengan statement kondisi, sehingga kita tidak perlu repot berulang kali memanggil/menulis beberapa baris kode yang sama atau berpola berulang kali.

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

Nah, berdasarkan apa yang telah kita review mengenai function, saatnya kita masuk ke dalam rekursi, atau fungsi rekursif.

### Rekursi (Recursion)

Kita bisa membuat function yang memanggil dirinya sendiri, disebut recursion. Memungkinkan kita untuk menulis fungsi dengan ekspektasi hasil yang sama namun cara/gayanya berbeda. Ini akan berhubungan nanti tentang bagaimana kita menstrukturkan langkah logika kita, atau algorithm.

Mungkin rekursif bagi sebagian orang menjadi satu hal yang dianggap mengerikan atau membingungkan. Tapi apabila kita sudah mengenal bagaimana cara atau alur dari fungsi rekursif, ketakutan atau kebingungan itu pasti bisa hilang.

Berikut ini contoh paling sederhana dalam implementasi fungsi rekursif:

```javascript
function numberSum(num) {
  if(num == 1) {
    return 1;
  }
  else {
    return num + numberSum(num - 1);
  }
}

console.log(numberSum(5)); // 5 + 4 + 3 + 2 + 1 = 15
```

Fungsi di atas akan mengembalikan nilai berupa hasil penambahan dari 5 + 4 + 3 + 2 + 1. Bagaimana cara kita melakukannya dengan fungsi di atas, hanya berbekal satu parameter yaitu angka 5? Jika diperhatikan, fungsi numberSum akan memanggil kondisi. Jika angka yang diinput adalah 1, maka fungsi akan selesai dan mengembalikan angka 1. Namun, jika lebih dari satu, fungsi akan mengembalikan nilai berupa value dari variabel `num`, dan menambahkannya dengan `numberSum(num - 1)`. Mungkin beberapa akan bingung sejenak tentang apa yang terjadi. Jadi, inilah kenapa fungsi ini disebut rekursif, atau sebuah fungsi yang memanggil dirinya sendiri. Untuk dapat mendapatkan hasil yang dibutuhkan, maka pemanggilan ulang fungsi tersebut wajib dilakukan, namun jangan lupa untuk mengubah nilai parameternya.

Jika kita pecah fungsi di atas secara proses, maka fungsi yang berjalan adalah `numberSum(5)`, kemudian mengembalikan nilai `5 + numberSum(4)`, yang akan mengembalikan nilai `4 + numberSum(3)`, dan seterusnya hingga mengembalikan nilai `1` dan keluar dari rekursif, sehingga pada akhirnya akan menghasilkan nilai 5 + 4 + 3 + 2 + 1.

:warning: seperti layaknya looping, waspadai juga pemanggilan rekursif yang tidak akan pernah selesai!

Kamu bisa mencoba kode diatas [disini](http://jsbin.com/hacogo/edit?js,console).

*Kenapa kita menggunakan fungsi rekursif? Bukankah hal ini bisa kita selesaikan dengan looping for atau while saja?*

Tentu, kamu bisa menyelesaikan kasus di atas dengan looping. Namun, banyak kasus yang sangat membutuhkan rekursif, atau beberapa kasus akan menjadi lebih efisien dari segi jumlah baris kode apabila menggunakan kode rekursif.

Dibawah ini ada contoh fungsi rekursif yang lebih advanced, kamu bisa coba dua contoh dibawah untuk memperkuat pemahaman kamu tentang rekursif!

**Contoh Fungsi Rekursif Untuk Kasus Perpangkatan**

```javascript
// Perpangkatan
function power(base, exponent) {
  if (exponent == 0)
    return 1;
  else
    return base * power(base, exponent - 1);
}
console.log(power(3, 3)); // 3 ** 3 = 27
```

<!-- ### Tambahan: Konversi Tipe Data (Type Conversion)

Telah kita ketahui bahwa kita bisa mengubah tipe data antara Number dan String dengan mudah hanya dengan assign nilai baru atau dengan operator. Ada cara lain yang lebih baik seperti menggunakan fungsi atau mendapatkan angka dari string dengan operator plus `+` (unary plus).

```javascript
> myNumber // 10.5
> myNumber.toString()  // "10.5"
> parseInt(myNumber)   // 10
> parseFloat(myNumber) // 10.5
> "8.8" + "8.8" // "8.88.8"
> (+"8.8") + (+"8.8") // 17.6
``` -->

<!---
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

--->
