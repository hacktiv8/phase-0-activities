# Get to Know The Latest JavaScript, Node.js, and Transpilation

## Objectives

TODO

## Directions

### Mengenal ECMAScript 2015 (ES6)

![ECMAScript 2015 (ES6)](assets/es6-logo.png)

Terkait dengan perkenalan pada JavaScript, ES2015/ES6 dengan nama lain ES6 Harmony, secara sederhana merupakan versi terbaru dan paling baik untuk sekarang ini dalam menggunakan JavaScript. Karenanya, kita direkomendasikan untuk mengadopsi penggunaannya sesegera mungkin.

Kemudian sambil kita review kembali, ketahui bahwa ECMAScript itu pun memiliki banyak fitur yang tercakup antara lain:

- Sintaks atas bahasanya
- Mekanisme pengendalian error
- Tipe dan struktur data
- Object global beserta method-nya
- Inheritance dengan prototype
- Strict mode

Lalu terdapat berbagai fitur baru yang ada pada ES6 antara lain:

- Class (`class`) untuk membuat objek dan module
- Function dengan fat arrow (`=>`)
- Default parameter
- Block scope yang lebih baik
- Variabel `let` dan `const`
- Ekspresi generator
- Decorator (`@`)
- Data biner
- Array bertipe
- Collection (`maps` dan `sets`)
- Promise untuk mengelola operasi asynchronous
- dan masih banyak lainnya

Support atau dukungan terhadap ES6 sudah ada untuk beberapa browser modern seperti Chromium/Chrome dan Firefox, namun belum hingga 100%. Untuk sekarang, kita cukup tahu saja, belum harus digunakan sekarang. Bahkan untuk mencobanya pada periode sekarang pun, kita mesti [mengetahui tentang transpilation](#transpilation-dan-transpiler) terlebih dahulu.

### Mengenal Class dan Object

Berikut sekilas kita ulas sebagai preview saja, bagaimana membuat objek yang berbasiskan akan paradigma pemrograman berbasis objek (Object-Oriented Programming atau OOP). Class dan object di sini bukan untuk disamakan/dipusingkan caranya dengan tipe data objek (`{}`), karena lebih mirip seperti membuat blueprint atau rencana yang bisa dipakai berkali-kali untuk membuat satuan objek.

Sintaksnya seperti berikut.

```javascript
class Square {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}

var kotak = new Square(100, 200);
var kotakLain = new Square(300, 400);

// kotak.height === 100
// kotakLain.width === 400
```

### Mengenal Node.js

![Node.js Logo](assets/nodejs-logo.png)

Pada dasarnya merupakan implementasi JavaScript sebagai platform di backend atau server. Secara teknis, adalah sebuah runtime JavaScript yang berjalan dengan Chrome V8 JavaScript engine. Fitur utamanya adalah model event-driven dan non-blocking Input/Output (I/O) yang ringan dan efisient. Node.js memiliki pengatur paket atau modul aplikasi yang disebut npm, yang juga merupakan ekosistem library open source.

Mayoritas tools yang akan temukan ke depan, bahkan dari berbagai pedoman di sini, sebenarnya membutuhkan instalasi Node.js. Tapi untuk sementara waktu, gunakan Node.js jika sudah siap saja. Beberapa hal yang kita kenalkan saja tanpa harus digunakan segera.

### Mengenal Transpilation dan Transpiler

Apa itu transpilasi (transpilation)? Spesifik di JavaScript, sederhananya adalah menerjemahkan bahasa tertentu misalnya JavaScript versi ES6 menjadi bahasa JavaScript versi sekarang (ES5). Kita perlu melakukan penerjemahan karena masalah ES6 belum sepenuhnya dapat dijalankan di berbagai browser.

Namun pada saat yang sama, kita ingin menggunakan fitur-fitur pada ES6 tadi. Dengan transpilasi, kita bisa menggunakan berbagai fitur ES6 dalam periode sekarang juga namun dengan sintaks ES5 yang setelah diterjemahkan terlebih dahulu.

Karena transpilasi membutuhkan tool spesifik, kita antara harus menginstal tool tersebut atau mengandalkan sebuah website untuk melakukannya. Tool untuk melakukan transpilasi disebut transpiler. Transpiler paling populer adalah [Babel](http://babeljs.io). Kita bisa langsung menggunakan Babel melalui [website REPL-nya](http://babeljs.io/repl).

![Babel.js](assets/babel-logo.png)

Contoh saat transpilasi sudah dilakukan pada kode tadi...

```javascript
class Square {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
var kotak = new Square(100, 200);
```

akan menjadi...

```javascript
"use strict";

function _classCallCheck(instance, Constructor) { if (!(instance instanceof Constructor)) { throw new TypeError("Cannot call a class as a function"); } }

var Square = function Square(height, width) {
  _classCallCheck(this, Square);
  this.height = height;
  this.width = width;
};

var kotak = new Square(100, 200);
```

yang kemudian bisa kita buktikan bahwa kode tersebut bekerja...

```javascript
> console.log(kotak.height)
> 100

> console.log(kotak.weight)
> 200
```

Atau contoh lain, dalam pembuatan function dengan fat arrow...

```javascript
const plusOne = (n) => n + 1
```

menjadi...

```javascript
"use strict";

var plusOne = function plusOne(n) {
  return n + 1;
};
```

Dapat kita lihat jadi sebenarnya transpilasi sesederhana menambahkan secara otomatis fungsi atau fitur yang belum ada di JavaScript versi sebelumnya. Secara wajar, kalau belum ditranspilasi maka kode yang awal tadi tidak dapat bekerja.
