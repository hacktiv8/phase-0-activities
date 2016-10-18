# Halo JavaScript!

## Pengenalan

Mari kita sambut salah satu bahasa pemrograman universal di dunia: JavaScript! Untuk kamu yang belum tahu JavaScript (kadang disebut JS saja); ia adalah bahasa native untuk web yang ringan, interpreted, dan salah satu bahasa pemrograman paling populer yang digunakan oleh developer di seluruh dunia, untuk browser dan web. Bahkan beberapa aplikasi non-browser juga menggunakannya seperti Node.js, MongoDB, dan Apache CouchDB. Lebih lagi, JS adalah bahasa yang dinamis, berbasis prototype, multi-paradigm (mendukung gaya pemrograman berbasis objek, imperatif, dan deklaratif/fungsional). Mungkin kamu sudah tahu, bahwa JavaScript tidak sama dengan Java; namanya mirip tapi aslinya dibuat oleh pihak yang berbeda sehingga juga aturannya, ekosistem, sintaks, semantiknya berbeda. JavaScript pada dasarnya memberi interaksi (seperti, klik, input, animasi) pada halaman HTML (yang biasanya juga menggunakan CSS). Zaman sekarang JavaScript sudah dapat berdiri sendiri, yang dahulunya harus mengandalkan HTML dan CSS agar dapat bekerja dengan semestinya.

## Stuktur Bahasa Program

Pada dasarnya, setiap bahasa pemrograman modern memiliki hal-hal yang tertulis berikut. Hal-hal ini memungkinkan programmer untuk menulis code (computer code) untuk membuat/membangun program yang dapat menyelesaikan masalah seperti menghitung angka, memproses data, membuat aplikasi web, dan banyak lainnya.

- sintaks (syntax) dan pernyataan (statement): terkait bagaimana cara menulis code-nya
- tipe data (data types) dan/atau struktur data (data structure)
- variabel dan operator
- kondisional (conditional) atau percabangan (branching)
- kumpulan/koleksi data (collections) serta perulangan/iterasi (loop/iteration)
- fungsi/metode (function/method)

## Menjalankan Script JavaScript

Spesial untuk JavaScript, kita bisa menggunakan editor code biasa (code editor) untuk mengetikkan JavaScript bersamaan dengan HTML dan CSS; atau kita bisa langsung mengetikkan code ke dalam dev tools (terdapat di Chromium/Chrome dan Firefox) dengan membuka tab `console` (`Ctrl+Shift+J` atau `Cmd+Opt+J` di Chrome, `Ctrl+Shift+K` atau `Cmd+Opt+K` di Firefox). Artinya JavaScript bisa langsung digunakan dan ditulis di dalam browser ataupun editor code.

Kamu juga bisa gunakan extension browser untuk editor JavaScript yang lebih dari sekadar console di dev tools seperti [Chrome Scratch JS](https://chrome.google.com/webstore/detail/scratch-js/alploljligeomonipppgaahpkenfnfkn), [JSBin](http://jsbin.com), ataupun [CodePen](https://codepen.io). Apapun tools yang dipakai, yang terpenting adalah kita dapat mengakses editor atau console yang akan menjalankan sintaks JavaScript.

Untuk saat ini, mari kita gunakan [JSBin](http://jsbin.com?js,console).

### Sintaks (Syntax) dan Pernyataan (Statement)

Sintaks itu seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemrograman. Merupakan kata-kata dan perintah (command) pada bahasa yang juga merupakan instruksi untuk disusun menjadi sebuah program yang dibuat atau dikembangkan. Kita gunakan sintaks tertentu untuk membuat statement program, instruksi untuk dijalankan/dieksekusi oleh web browser, compiler, ataupun interpreter. Dalam JavaScript, ada berbagai sintaks yang polanya seperti `alert();`, `console.log();`, `document.write();`, dan masih banyak lagi. Kesimpulannya, sintaks dan statement adalah ekspresi (expression) apapun yang biasanya diikuti dengan titik koma (semicolon `;`) ataupun hal-hal yang bisa dieksekusi oleh penjalan code (executor).

#### Menjalankan JavaScript melalui console

```javascript
> "Hello!";
> document.write("Hello you too!");
> console.log("Hello, computer!");
> alert("Hello, human!");
> prompt("What is your name?");
> console.log("Multiline\n text!");
```

Bukalah [JSBin](http://jsbin.com?console), dan cobalah kode di atas pada tab **console**

#### Menjalankan JavaScript dengan script JavaScript dan menampilkannya pada console

```javascript
> "Hello!";
> document.write("Hello you too!");
> console.log("Hello, computer!");
> alert("Hello, human!");
> prompt("What is your name?");
> console.log("Multiline\n text!");
```

Bukalah [JSBin](http://jsbin.com?js,console), dan cobalah kode di atas pada tab **javascript**

#### Data Type

Data Type, atau dalam bahasa Indonesia kita sebut sebagai Tipe Data, adalah sekumpulan data dengan nilai yang memiliki karakteristik berbeda. Beberapa contoh dari tipe data adalah:

- Integer: tipe data dengan nilai berupa angka
- Character: tipe data dengan nilai berupa sebuah karakter
- String: tipe data dengan nilai berupa kumpulan atau set dari beberapa karakter
- Boolean: tipe data dengan nilai berupa `true` atau `false`.  

**Variable**

Variable, atau dalam bahasa Indonesia kita sebut variabel, bisa memegang atau berisi hampir semua tipe data yang tersedia. Variabel memungkinkan kita untuk memuat atau menyimpan nilai data ke dalam sesuatu. Biasanya bersifat sementara saat program dijalankan.

```javascript
var tampung = 5;
console.log(tampung); // 5
```

```javascript
var angkaGanjil = 1, angkaGenap = 2;
```

Waspada pemanggilan variable yang tidak bernilai!
```javascript
var tampungBaru;
console.log(tampungBaru); // UNDEFINED
```

#### Operator

Operator adalah karakter yang merepresentasikan sebuah tindakan. Kita sering menemukan operator seperti + (tambah),
 x (kali), dan lain-lain. Namun, di dunia programming, operasi tambah kita gantikan dengan simbol * (asterisk) dan operasi bagi dengan simbol / (slash)

Operator dibagi menjadi beberapa tipe:

**Arithmetic Operator**
Arithmetic operator adalah operator yang melibatkan operasi matematika, seperti penambahan, pengurangan, perkalian, dan lain-lain.

- Tambah (+)
- Kurang (-)
- Kali (\*)
- Bagi (/)
- Modulus (%)

Bagi kamu yang baru kali ini mendengar tentang modulus, modulus adalah sisa bagi. Misalkan kita membagi 7 dengan 2. Hasil bagi nya adalah 3, namun sisa dari hasil baginya adalah 1. Bilangan yang memang habis dibagi, sisa hasil baginya adalah 0.

Contoh sederhana penggunaan modulus:

```javascript
> 4 % 2 // 4 modulus 2
> 0 // bilangan 4 habis dibagi 2, sehingga 4 modulus 2 menghasilkan nilai 0
> 5 % 2 // 5 modulus 2
> 0 // bilangan 5 habis tidak habis dibagi 2, sehingga 5 modulus 2 menghasilkan nilai 1, sisa dari hasil pembagian
```

**Assignment Operator**
Assignment operator adalah operator yang meng-"assign", atau memberikan nilai. Biasanya, assignment operator digunakan untuk memberikan nilai kepada sebuah variable.

```javascript
var bilangan
bilangan = 5; //Contoh assignment value 5 ke sebuah variable
```

#### Conditional

Conditional adalah...

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
```

```javascript
var tampung = 5
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
else {
  console.log("angka yang ditampung bukan 5!");
}
```

#### Loop/Iteration

Loop/Iteration adalah...

```javascript
var jalankanLooping = true;
while(jalankanLooping) {
  console.log("looping berjalan!");
  jalankanLooping = false;
}
```

Waspadai Forever Looping!

```javascript
var jalankanLooping = true;
while(jalankanLooping) {
  console.log("looping berjalan!");
}
```

#### Function/Method

Function adalah...

Contoh fungsi sederhana

```javascript
function tampilkan() {
  console.log("tampilkan!")
}

tampilkan()
```

Pengiriman argument sebagai parameter

```javascript
function tampilkanAngka(angka) {
  console.log(angka)
}

tampilkan(5)
```

Pengiriman parameter lebih dari satu

```javascript
function tampilkanAngka(angkaPertama, angkaKedua) {
  console.log(angkaPertama + angkaKedua)
}

tampilkan(5,3)
```

Inisialisasi parameter dengan nilai default

```javascript
function tampilkanAngka(angka = 1) {
  console.log(angka)
}

tampilkan()
```

Menampung function sebagai variable dengan anonymous function

```javascript
var fungsiPerkalian = function(angkaPertama, angkaKedua) {
  console.log(angkaPertama * angkaKedua)
}

fungsiPerkalian(2,4)
```
