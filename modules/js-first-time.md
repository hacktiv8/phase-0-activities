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

Kamu juga bisa gunakan extension browser untuk editor JavaScript yang lebih dari sekadar console di dev tools seperti [Chrome Scratch JS](https://chrome.google.com/webstore/detail/scratch-js/alploljligeomonipppgaahpkenfnfkn), [https://repl.it/languages/javascript](repl.it/languages/javascript), ataupun [CodePen](https://codepen.io). Apapun tools yang dipakai, yang terpenting adalah kita dapat mengakses editor atau console yang akan menjalankan sintaks JavaScript.

Untuk saat ini, mari kita gunakan [Repl.it](https://repl.it/languages/javascript).

### Sintaks (Syntax) dan Pernyataan (Statement)

Sintaks itu seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemrograman. Merupakan kata-kata dan perintah (command) pada bahasa yang juga merupakan instruksi untuk disusun menjadi sebuah program yang dibuat atau dikembangkan. Kita gunakan sintaks tertentu untuk membuat statement program, instruksi untuk dijalankan/dieksekusi oleh web browser, compiler, ataupun interpreter. Dalam JavaScript, ada berbagai sintaks yang polanya seperti `alert();`, `console.log();`, `document.write();`, dan masih banyak lagi. Kesimpulannya, sintaks dan statement adalah ekspresi (expression) apapun yang biasanya diikuti dengan titik koma (semicolon `;`) ataupun hal-hal yang bisa dieksekusi oleh penjalan code (executor).

#### Menjalankan JavaScript dengan script JavaScript dan menampilkannya pada console

```javascript
> "Hello!";
> document.write("Hello you too!");
> console.log("Hello, computer!");
> alert("Hello, human!");
> prompt("What is your name?");
> console.log("Multiline\n text!");
```

Bukalah [Repl](repl.it/languages/javascript), dan cobalah kode di atas pada tab **console**

### Data Type

Data Type, atau dalam bahasa Indonesia kita sebut sebagai Tipe Data, adalah sekumpulan data dengan nilai yang memiliki karakteristik berbeda. Beberapa contoh dari tipe data adalah:

- Number: tipe data dengan nilai berupa angka
- String: tipe data dengan nilai berupa kumpulan atau set dari beberapa karakter
- Boolean: tipe data dengan nilai berupa `true` atau `false`.

### Variable

Variable, atau dalam bahasa Indonesia kita sebut variabel, bisa memegang atau berisi hampir semua tipe data yang tersedia. Variabel memungkinkan kita untuk memuat atau menyimpan nilai data ke dalam sesuatu. Biasanya bersifat sementara saat program dijalankan.

```javascript
var tampung = 5;
console.log(tampung); // 5
```

```javascript
var angkaGanjil = 1;
var angkaGenap = 2;
console.log(angkaGanjil); // 1
console.log(angkaGenap); // 2
```

:warning: Waspadai pemanggilan variable yang tidak bernilai!
```javascript
var tampungBaru;
console.log(tampungBaru); // undefined
```

### Operator

Operator adalah karakter yang merepresentasikan sebuah tindakan. Kita sering menemukan operator seperti + (tambah),
 x (kali), dan lain-lain. Namun, di dunia programming, operasi kali kita gantikan dengan simbol * (asterisk) dan operasi bagi dengan simbol / (slash)

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
> 1 // bilangan 5 habis tidak habis dibagi 2, sehingga 5 modulus 2 menghasilkan nilai 1, sisa dari hasil pembagian
```

**Assignment Operator**
Assignment operator adalah operator yang meng-"assign", atau memberikan nilai. Biasanya, assignment operator digunakan untuk memberikan nilai kepada sebuah variable.

```javascript
var bilangan;
bilangan = 5; // Contoh assignment value 5 ke sebuah variable
```

**Comparison Operator**
Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara 'true' atau 'false'.

- Equal operator (==)

```javascript
var angka = 8;
console.log(angka == 8); // true
console.log(angka == 1); // false
```

- Not Equal operator (!=)

```javascript
var angka = 8;
console.log(angka != 7); // true
console.log(angka != 8); // false
```

- Strict Equal operator (===)

Sedikit berbeda dengan equal operator, strict operator `===` mewajibkan nilai yang dibandingkan sama dan tipe data nya pun harus sama. Sedangkan pada `==`, `8` dan `"8"` akan dianggap sama, karena itu menghasilkan nilai `true`.

```javascript
var angkaBeda = "8";
console.log(angkaBeda == 8); // true
console.log(angkaBeda === 8); // false
console.log(angkaBeda === "8"); // true
```

- Strict Not Equal operator (!==)

Sedikit berbeda dengan not equal operator, strict not equal operator `!==` mewajibkan nilai yang dibandingkan tidak sama dan tipe data nya pun harus sama. Sedangkan pada `!=`, `8` dan `"8"` akan dianggap sama, karena itu menghasilkan nilai `false`.

```javascript
var angkaBeda = "8";
console.log(angkaBeda != 7); // true
console.log(angkaBeda !== 7); // true
console.log(angkaBeda !== 8); // true
console.log(angkaBeda !== "8"); // false
```

- Less Than (<) / Greater Than (>)

operator selanjutnya adalah `<`, yaitu kurang dari sekian, dan `>`, yaitu lebih dari sekian.

```javascript
var angka = 8;
console.log(angka > 7); // true
console.log(angka < 6); // false
console.log(angka <= 8); // true
```

**Conditional Operator**
Conditional operator adalah operator yang akan mengevaluasi kebenaran dari nilai yang dikomputasi.

- OR (||): akan menghasilkan nilai `true` jika salah satu premis mengandung `true`

```javascript
console.log(true || true); // true
console.log(true || false); // true
console.log(true || false || false); // true
console.log(false || false); // false
```

- AND (&&): akan menghasilkan nilai `true` jika kedua premis `true`.

```javascript
console.log(true && true); // true
console.log(true && false); // false
console.log(false && false); // false
console.log(false && true && true); // false
console.log(true && true && true); // true
```

### Conditional

Kondisional adalah sebuah metode dimana kode akan mengecek apakah sebuah premis benar atau tidak.
Jika kondisi sesuai, maka kode dalam kondisional akan dijalankan.

**Contoh Conditional 1** Menjalankan proses apabila statement kondisi `true`.

```javascript
if(true) {
  console.log("Jalankan kode"); // baris kode ini akan di panggil
}
```

**Contoh Conditional 2** Tidak menjalankan proses di dalam block/scope conditional apabila statement kondisi `false`.

```javascript
if(false) {
  console.log("Jalankan kode"); // baris kode ini tidak di panggil
}
```

**Contoh Conditional 3** Conditional dengan statement yang akan menghasilkan nilai `true` atau `false`

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
```

Di dalam conditional, kita juga mengenal dengan yang dinamakan dengan branching. Branching, atau dalam bahasa indonesia berarti pencabangan, kita menjalankan potongan kode kita sesuai dengan "cabang" atau "jalur" yang memenuhi kondisi tersebut.

Contoh sangat sederhana-nya adalah sebuah kasus berikut ini:

Seorang anak diminta oleh ibunya untuk membeli telur di supermarket dan langsung pulang ke rumah. Jika di supermarket tersebut kehabisan telur, maka anak itu harus menelepon ibunya dan mengabari kalau supermarket kehabisan telur. Anak tersebut akan datang ke supermarket dan menemukan kondisi yang bercabang:

- Jika di supermarket terdapat telur, anak itu akan membeli telur itu dan pulang, atau
- Jika di supermarket tidak terdapat telur, anak itu akan menelepon ibunya.

pada JavaScript dan berbagai bahasa pemrograman, "jika tidak terdapat telur", atau bisa dibilang kondisi yang terjadi diluar "ekspektasi", terdapat `else` yang akan menjalankan proses lain jika `if` bernilai `false`. Contoh lebih jelas bisa dilihat dari contoh dibawah ini:

**Contoh Conditional 4** Branching Sederhana (If-else)

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
else {
  console.log("angka yang ditampung bukan 5!");
}
```

Tidak hanya sampai situ, kondisional bisa juga bersifat bertumpuk, atau biasanya disebut juga sebagai nested-if.

**Contoh Conditional 5** Branching Bertumpuk Sederhana (If-else)

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
else {
  if(tampung < 5) {
    console.log("angka yang ditampung bukan 5, tapi lebih kecil dari 5.");
  }
  else {
    console.log("angka yang ditampung bukan 5, tapi lebih besar dari 5.");
  }
}
```

Contoh di atas juga bisa dibuat dalam bentuk lain, yaitu `else if`. `else-if` adalah sebuah kondisional, dimana statement `else if` akan dijalankan apabila `if` tidak memenuhi kondisi / `false`, dan dijalankan sebelum statement `else`.

**Contoh Conditional 5** Branching Bertumpuk Sederhana (If-else)

```javascript
var tampung = 5;
if(tampung == 5) {
  console.log("angka yang ditampung adalah 5!");
}
else if(tampung < 5) {
    console.log("angka yang ditampung bukan 5, tapi lebih kecil dari 5.");
}
else {
  console.log("angka yang ditampung bukan 5, tapi lebih besar dari 5.");
}
```

Selain menggunakan if-else, ada satu cara lagi untuk melakukan conditional, yaitu switch-case. Switch case ini biasanya lebih sering digunakan untuk skenario yang melibatkan banyak kondisi atau branching yang banyak. Contoh sederhananya adalah dengan sebuah remote TV.

```javascript
var buttonPushed = 1;
switch(buttonPushed) {
  case 1:   { console.log('matikan TV!'); break; }
  case 2:   { console.log('turunkan volume TV!'); break; }
  case 3:   { console.log('tingkatkan volume TV!'); break; }
  case 4:   { console.log('matikan suara TV!'); break; }
  default:  { console.log('Tidak terjadi apa-apa'); }
}
```  

Seperti dilihat di kode di atas, `switch` akan mengambil nilai, dan `case` adalah skenario apa saja yang memungkinkan untuk menjalankan satu proses. Kamu mungkin menyadari ada 1 sintaks baru yang kamu temukan: `break;`. Break memungkinkan kamu untuk "berhenti" dari proses kondisional/switch-case, dengan tujuan agar proses tidak berlanjut ke case selanjutnya. untuk eksperimenmu, kamu bisa mencoba menghapus `break` dan perhatikan apa yang terjadi.

Kamu bisa eksperimen dan mencoba kode di atas [disini](http://jsbin.com/qucoma/edit?js,console)

### Loop/Iteration

Loop/Iteration adalah tindakan mengulang / merepetisi sebuah proses, dengan tujuan untuk mendapatkan
deret hasil, atau dengan tujuan mendapatkan hasil tertentu dengan repetisi. Setiap proses repetisi
ini disebut sebagai Iteration atau Looping.

Untuk melakukan looping/iteration, JavaScript menyediakan beberapa jenis iteration, yaitu:

- while-loop
- for-loop

#### While-loop

While-loop adalah iterasi yang akan mengulang sebuah proses dengan sebuah kondisi tertentu.

Berikut adalah cara atau struktur penulisan while-loop:

```javascript

while([Kondisi]) { // Kondisi yang menentukan apakah program akan melakukan iterasi. Berupa boolean atau true/false.
  [Proses] // Merupakan proses yang akan dijalankan dalam satu iterasi
}
```

Pada while-loop, statement `while` akan mengambil sebuah nilai `true` atau `false` dari hasil kondisi yang diberikan.
Apabila statement `while` mendapatkan nilai `true`, maka proses yang berada didalam curly bracket (`{ }`)
akan dijalankan. Looping akan terus dilakukan selama kondisi while-loop masih `true`.

Untuk mencegah looping berjalan terus-menerus, dilakukan sebuah proses yang akan mengubah kondisi yang sedemikian rupa
yang bertujuan untuk menghentikan looping dengan menghasilkan kondisi yang `false`.

**Contoh Looping While-loop 1** Looping Angka 1-9 Sederhana

```javascript
var flag = 1;
while(flag < 10) { // Loop akan terus berjalan selama nilai flag masih dibawah 10
  console.log('Iterasi ke-' + flag); // Menampilkan nilai flag pada iterasi tertentu
  flag++; // Mengubah nilai flag dengan menambahkan 1
}
```
Kamu bisa mencoba kode di atas [disini](https://jsbin.com/pahure/1/edit?js,console)

**Contoh Looping While-loop 2** Looping Mengembalikan Angka Total

```javascript
var deret = 5;
var jumlah = 0;
while(deret > 0) { // Loop akan terus berjalan selama nilai deret masih di atas 0
  jumlah += deret; // Menambahkan nilai variable jumlah dengan angka deret
  deret--; // Mengubah nilai deret dengan mengurangi 1
  console.log('Jumlah saat ini: ' + jumlah)
}

console.log(jumlah);
```
Kamu bisa mencoba kode di atas [disini](https://jsbin.com/nolocam/edit?js,console)

#### For-loop

For-loop adalah bentuk lain dari iterasi, dimana statement `for` menjadi kontrol atas loop yang dilakukan.
Hal ini yang menjadi pembeda antara for-loop dengan while-loop.

Berikut adalah cara atau struktur penulisan for-loop:

```javascript

for([Inisialisasi], [Kondisi], [Incremental/Decremental]) {
  [Proses] // Merupakan proses yang akan dijalankan dalam satu iterasi
}
```

Pada for-loop, statement `for` akan menampung tiga parameter, yaitu sebut saja inisialisasi, kondisi, dan
incremental/decremental. Ketiga parameter ini akan menjadi kontrol kapan loop ini harus berhenti.
Pada parameter pertama, yaitu inisialisasi, sebuah variable diberikan nilai awal atau default.
Pada parameter kedua, yaitu kondisi, for-loop akan terus berjalan selama kondisi ini masih terpenuhi, dengan
kata lain, mengandung nilai `true`.
Pada parameter kedua, yaitu incremental/decremental, variabel yang menjadi kontrol terhadap loop ini akan diubah nilainya.

:thumbsup: *Best Practice:*
Walaupun memang for-loop dapat mengubah kondisi di dalam proses,
namun best practice dari penggunaan for-loop adalah seluruh kendali atau kontrol dari looping ditentukan
oleh variable yang diinisialisasi, di increment/decrement, dan juga kondisi for-loop pun menggunakan variable
tersebut.

Untuk memudahkan kamu mendapatkan gambaran jelas tentang penggunaan for-loop, mari kita gunakan kedua
contoh while-loop dan kita tulis ulang dalam bentuk for-loop.

**Contoh Looping For-loop 1** Looping Angka 1-9 Sederhana

```javascript
for(var angka = 1; angka < 10; angka++) {
  console.log('Iterasi ke-' + angka);
}
```
Kamu bisa mencoba kode di atas [disini](https://jsbin.com/dijukel/edit?js,console)

**Contoh Looping For-loop 2** Looping Mengembalikan Angka Total

```javascript
var jumlah = 0;
for(var deret = 5; deret > 0; deret--) {
  jumlah += deret;
  console.log('Jumlah saat ini: ' + jumlah);
}

console.log('Jumlah terakhir: ' + jumlah);
```
Kamu bisa mencoba kode di atas [disini](https://jsbin.com/xukega/edit?js,console)

**Contoh Looping For-loop 3** Looping Dengan Increment dan Decrement Lebih dari 1

```javascript

for(var deret = 0; deret < 10; deret += 2) {
  console.log('Iterasi dengan Increment counter 2: ' + deret);
}

console.log('-------------------------------');

for(var deret = 15; deret > 0; deret -= 3) {
  console.log('Iterasi dengan Decrement counter : ' + deret);
}
```
Kamu bisa mencoba kode di atas [disini](https://jsbin.com/fovoyun/edit?js,console)


:warning: Waspadai Forever Looping!

Dengan sengaja atau sengaja, kode kamu mungkin dapat menghasilkan forever looping,
atau looping yang tidak akan pernah berhenti. Bila ini terjadi, segera periksa
statement kondisi kamu.

```javascript
var flag = 1;
while(flag < 10) { // Loop akan terus berjalan, karena nilai flag tidak pernah berubah
  console.log('Iterasi ke-' + flag);
}
```

### Function/Method

Function adalah sebuah blok kode yang disusun sedemikian rupa untuk menjalankan sebuah tindakan.
Blok kode ini dibuat untuk dapat bisa digunakan kembali. Cara atau bentuk penulisan function adalah
sebagai berikut:

```javascript
function nama_function(parameter 1, parameter 2, ...) {
  [Isi dari function berupa tindakan]
  return [expression];
}
```

Kode di atas tidak dapat kita copy-paste kan langsung, melainkan hanya sebuah bentuk penulisan `function`.
Sebuah `function`, umumnya melakukan tindakan dan sebelum `function` berakhir, `function` bisa
mengembalikan nilai dengan cara menambahkan sintaks return.

Kita juga dapat mengirimkan nilai ke dalam sebuah `function` dengan mencantumkannya ke dalam tanda kurung
dalam penulisan `function`. Untuk mengirimkan nilai lebih dari satu, gunakan tanda `,` sebagai pemisah.

**Contoh Function 1:** Function sederhana tanpa return

```javascript
function tampilkan() {
  console.log("halo!");
}

tampilkan();
```

**Contoh Function 2:** Function sederhana dengan return

```javascript
function munculkanAngkaDua() {
  return 2
}

var tampung = munculkanAngkaDua();
console.log(tampung)
```

**Contoh Function 3:** Function dengan parameter

```javascript
function kalikanDua(angka) {
  return angka * 2
}

var tampung = kalikanDua(2);
console.log(tampung)

```

**Contoh Function 4:** Pengiriman parameter lebih dari satu

```javascript
function tampilkanAngka(angkaPertama, angkaKedua) {
  return angkaPertama + angkaKedua
}

console.log(tampilkanAngka(5,3))
```

**Contoh Function 5:** Inisialisasi parameter dengan nilai default

```javascript
function tampilkanAngka(angka = 1) {
  return angka
}

console.log(tampilkanAngka(5)) // 5, sesuai dengan nilai parameter yang dikirim
console.log(tampilkanAngka()) // 1, karena default dari parameter adalah 1
```

:warning: Waspadai pengiriman parameter yang UNDEFINED!

Kita juga dapat menampung function sebagai variable dengan sebuah bentuk function
yang dinamakan Anonymous Function.

```javascript
var fungsiPerkalian = function(angkaPertama, angkaKedua) {
  return angkaPertama * angkaKedua
}

console.log(fungsiPerkalian(2,4))
```
