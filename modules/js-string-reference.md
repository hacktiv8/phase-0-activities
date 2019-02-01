# String pada JavaScript

## Objectives

- Memahami Tipe Data String pada JavaScript
- Mengetahui Property dan Method yang Dimiliki String
- Mengetahui Cara Menggunakan Property dan Method yang Dimiliki String
- Mengetahui Konversi Tipe Data Lain ke String dan Sebaliknya

## Learnings
 - [More About String](js-string-reference.md#more-about-string)
 - [String Properties](js-string-reference.md#string-properties)
 - [String Methods](js-string-reference.md#striing-methods)
 - [Typecasting To and From String](js-string-reference.md#typecasting-to-and-from-string)

### More About String

String adalah tipe data yang yang berisikan karakter-karakter alfanumerik yang dibungkus dengan karakter kutip (`'` dan `"`). karakter-karakter pada string dapat diakses menggunakan indeks atau posisi, dimana dimulai dari angka 0.

```javascript
var title = 'Your Name';

// mengambil huruf pertama dari string
console.log(title[0]); // 'Y'

// mengambil huruf terakhir dari string. Apa itu length? Penjelasan .length di section selanjutnya :)
console.log(title[title.length - 1]); // 'e'

// "memaksa" perubahan nilai di posisi 0
title[0] = 'T';
// tidak akan ada perubahan
console.log(title); // 'Your Name'

title = 'My name';
// ada perubahan, karena assign keseluruhan string
console.log(title); // 'My name'

// menambahkan string dengan simbol '+'
title = title + ' is Bento';

console.log(title); // 'My name is Bento'
```

Pada JavaScript, tipe data primitif seperti String diperlakukan seperti objek. Oleh karena itu, String memiliki *property* dan *method*. Apabila kamu belum mendengar tentang Objek pada JavaScript (dan memang seharusnya belum), kamu tidak perlu pusing dengan kedua istilah tersebut. Secara sederhana, *property* dan *method* adalah kemampuan milik String yang dapat digunakan untuk mempermudah kita dalam melakukan pemrograman. Kamu cukup menggunakan apa yang dimanakan dengan method. Method, akan lebih dalam dibahas di materi *JavaScript Function*.

### String Properties

#### `.length`

Mengembalikan panjang dari suatu string; perhitungan dimulai dari 1.

```javascript
var name = 'Uvuvwevwevwe Onyetenyevwe Ugwemubwem Ossas';
console.log(name.length); // 42
```

### String Methods

#### `.charAt([indeks])`

Mengembalikan karakter pada indeks yang diinginkan

```javascript
console.log('i am a string'.charAt(3)); // 'm'
```

#### `.concat([string])`

Menggabungkan beberapa string dan mengembalikannya menjadi string baru.

```javascript
var string1 = 'good';
var string2 = 'luck';
console.log(string1.concat(string2)); // goodluck
```

#### `.indexOf([string/karakter])`

Mengembalikan indeks dari string/karakter yang dicari, yang pertama kali ditemukan, atau -1 apabila tidak ditemukan.

```javascript
var text = 'dung dung ces!';
console.log(text.indexOf('dung'));  // 0
console.log(text.indexOf('u'));     // 1
console.log(text.indexOf('jreng')); // -1
```

<!-- #### `.match([regular-expressions])`

Mencari string yang memenuhi syarat pada suatu *[regular expression](regular-expressions.md)* dan menemukan string yang ditemukan ke dalam sebuah array.

```javascript
var wordTest = 'Can you can a can as a canner can can a can?';
var foundCan = wordTest.match(/can/g);
console.log(foundCan); //["can", "can", "can", "can", "can", "can"]
```

#### `.replace([string/regex], [string untuk ditukar])`

Mencari string tertentu atau *[regular expression](regular-expressions.md)* pada parameter pertama di dalam suatu string dan mengembalikan string baru dimana isinya adalah parameter pertama (bila ditemukan) sudah ditukar dengan parameter kedua. Bila menggunakan regex(regular expression), semua string yang ditemukan akan ditukar. Bila menggunakan string saja, hanya yang pertama ditemukan yang akan ditukar.

```javascript
var rockYou    = 'dung dung ces, dung dung ces';
var newRockYou = rockYou.replace(/ces/g, 'pret');
console.log(newRockYou); // dung dung pret, dung dung pret
var rockYou    = newRockYou.replace('dung', 'dum');
console.log(rockYou); // dum dung pret, dung dung pret
```

#### `.slice([indeks awal], [indeks akhir (optional)])`

Mengembalikan potongan string mulai dari indeks pada parameter pertama sampai dengan indeks pada parameter kedua. Bila parameter kedua tidak ditentukan, maka secara otomatis berakhir pada karakter terakhir. Karakter pada indeks yang ditentukan pada parameter kedua tidak diikutkan sebagai output.

```javascript
var car1 = 'Lykan Hypersport';
var car2 = car1.slice(0, 4);
console.log(car2); // Lyka
```
#### `.split([karakter pemisah], [limit (opsional)])`

Mengembalikan array dari potongan-potongan string yang dipisah dengan karakter separator yang sudah ditentukan pada parameter.

```javascript
var story    = 'Once_upon_a_time';
var splitted = story.split('_');
console.log(splitted); // ['Once', 'upon', 'a', 'time']
``` -->

#### `.substring([indeks awal], [indeks akhir (optional)])`

Mengembalikan potongan string mulai dari indeks pada parameter pertama sampai dengan indeks pada parameter kedua. Bila parameter kedua tidak ditentukan, maka secara otomatis berakhir pada karakter terakhir. Karakter pada indeks yang ditentukan pada parameter kedua tidak diikutkan sebagai output.

```javascript
var car1 = 'Lykan Hypersport';
var car2 = car1.substr(6);
console.log(car2); // Hypersport
```

#### `.substr([indeks awal], [jumlah karakter yang diambil (optional)])`

Mendapatkan potongan string mulai dari indeks pada parameter pertama dengan jumlah indeks pada parameter kedua. Bila parameter kedua tidak ditentukan, maka secara otomatis berakhir pada karakter terakhir. Karakter pada indeks yang ditentukan pada parameter kedua tidak diikutkan sebagai output.

```javascript
var motor1 = 'zelda motor';
var motor2 = car1.substr(2, 2);
console.log(motor2); // ld
```

#### `.toUpperCase()`

Mengembalikan string baru dengan semua karakter yang diubah menjadi huruf kapital.

```javascript
var letter = 'This Letter Is For You';
var upper  = letter.toUpperCase();
console.log(upper); // THIS LETTER IS FOR YOU
```

#### `.toLowerCase()`

Mengembalikan string baru dengan semua karakter yang diubah menjadi huruf kecil

```javascript
var letter = 'This Letter Is For You';
var lower  = letter.toLowerCase();
console.log(upper); // this letter is for you
```

#### `.trim()`

Mengembalikan string baru yang sudah dihapus karakter *whitespace* pada awal dan akhir string tersebut.

```javascript
var username    = ' administrator ';
var newUsername = username.trim(); // 'newUsername = 'administrator'
```

<!-- **Semua contoh kode diatas dapat diakses [disini](http://jsbin.com/goleva/edit?js,console)** -->

### Typecasting To and From String

**Typecasting** berarti mengubah data dari suatu tipe data ke tipe data yang lain. Pada JavaScript, typecasting sering dilakukan pada string, baik dari suatu tipe data menjadi string atau sebaliknya. Berikut beberapa cara yang bisa dilakukan untuk melakukan typecasting terhadap string.

#### `String([angka/array])`

Fungsi global `String()` dapat dipanggil kapan saja pada program JavaScript dan akan mengembalikan String dari parameter yang diberikan.

```javascript
var int  = 12;
var real = 3.45;
var arr  = [6, 7, 8];

var strInt  = String(int);
var strReal = String(real);
var strArr  = String(arr);

console.log(strInt);  // '12'
console.log(strReal); // '3.45'
console.log(strArr);  // '6,7,8'
```

#### `.toString()`

Mengonversi tipe data lain menjadi string. Bila data tersebut adalah array, setiap nilai akan dituliskan dan dipisah dengan karakter koma.

```javascript
var number = 21;
console.log(number.toString()); // '21'
var array = [1,2];
console.log(array.toString());  // '1,2'

```

#### `Number([String])`

Fungsi global `Number()` mengonversi tipe data string menjadi angka. Data yang diberikan pada parameter harus berupa karakter angka saja, dengan titik bila angka adalah bilangan desimal. Bila parameter berisi karakter selain angka dan/atau titik,  `Number()` akan mengembalikan **NaN** ***(Not a Number)***.

```javascript
var number1 = Number("90");   // number1 = 90
var number2 = Number("1.23"); // number2 = 1.23
var number3 = Number("4 5");  // number3 = NaN
```

#### `parseInt([String])` dan `parseFloat([String])`

Fungsi global `parseInt([String])` dan `parseFloat([String])` mengembalikan angka dari string. Bila angka adalah bilangan desimal maka gunakan `parseFloat()`, bila tidak bilangan dibelakang koma akan diabaikan.

```javascript
var int  = '89';
var real = '56.7';

var strInt_1 = parseInt(int);  // strInt_1 = 89
var strInt_2 = parseInt(real); // strInt_2 = 56

var strReal_1 = parseFloat(int); // strReal_1 = 89
var strReal_2 = parseFloat(int); // strReal_2 = 56.7
```

<!-- **Semua contoh kode diatas dapat diakses [disini](http://jsbin.com/xacujej/edit?js,console** -->

### Additional References

- [String by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)
- [JavaScript String Reference by W3School](http://www.w3schools.com/jsref/jsref_obj_string.asp)
- [JavaScript Type Conversion](http://www.w3schools.com/js/js_type_conversion.asp)
