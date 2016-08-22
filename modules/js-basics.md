# JavaScript Basics

## Objectives

Mari kita mengetahui hal-hal dasar tentang JavaScript yang diperlukan agar kita bisa memprogram sesuatu. Yang pada ujungnya adalah kita bisa tahu bagaimana cara memberi interaksi pada website yang berisi HTML dan CSS.

Di sini kita mulai ada sesi pemrograman (programming session) sesungguhnya dengan JavaScript yang juga secara tersirat mulai menggunakan struktur data. Pedoman ini didesain agar tidak perlu melibatkan banyak HTML dan CSS dahulu. Sehingga kita bisa lebih fokus ke JavaScript saja agak tidak terlalu membebani.

Berikut adalah beberapa hal yang kamu perlu cek saat mengikuti pedoman ini beserta referensi lainnya.

- ▢ Mengikutkan code JavaScript ke dalam HTML
- ▢ Menjalankan code JavaScript antara dari dalam file HTML atau JS, maupun langsung di console
- ▢ Memahami variabel dan operator beserta konvensi penamaan yang baik
- ▢ Membandingkan perbedaan kegunaan `=` dan `==`
- ▢ Memahami syntax JavaScript dan membuat statement program
- ▢ Memahami expression dan value di JavaScript
- ▢ Mendokumentasikan code program dengan komentar

## Learnings

### Mengenal JavaScript

Mari kita sambut salah satu bahasa pemrograman universal di dunia: JavaScript! Untuk kamu yang belum tahu JavaScript (kadang disebut JS saja); ia adalah bahasa native untuk web yang ringan, interpreted, dan salah satu bahasa pemrograman paling populer yang digunakan oleh developer di seluruh dunia, untuk browser dan web. Bahkan beberapa aplikasi non-browser juga menggunakannya seperti Node.js, MongoDB, dan Apache CouchDB. Lebih lagi, JS adalah bahasa yang dinamis, berbasis prototype, multi-paradigm (mendukung gaya pemrograman berbasis objek, imperatif, dan deklaratif/fungsional). Mungkin kamu sudah tahu, bahwa JavaScript tidak sama dengan Java; namanya mirip tapi aslinya dibuat oleh pihak yang berbeda sehingga juga aturannya, ekosistem, sintaks, semantiknya berbeda. JavaScript pada dasarnya memberi interaksi (seperti, klik, input, animasi) pada halaman HTML (yang biasanya juga menggunakan CSS). Zaman sekarang JavaScript sudah dapat berdiri sendiri, yang dahulunya harus mengandalkan HTML dan CSS agar dapat bekerja dengan semestinya.

![HTML dengan JavaScript](assets/html-js.png)

Kita perlu belajar JavaScript karena ia merupakan sesuatu yang terus-menerus berkembang secara relevan dalam teknologi dan skill yang dibutuhkan di industri modern dan pasar kerja. Juga karena JS hanyalah satu-satunya bahasa pemrograman yang dapat dijalankan secara native (langsung oleh platform browser), maka sekarang bisa digunakan untuk memprogram apapun dari server, mobile device, dan hardware (beberapa Internet of Things).

JavaScript memungkinkan kita untuk menambah atau membuat komponen interaktif pada website seperti galeri foto yang apik, panel dengan tab, atau validasi isian form. Kamu juga mungkin tahu bahwa ia juga sangat bisa digunakan untuk membuat aplikasi web yang kompleks seperti Wikipedia, Gmail, Facebook, Google Maps, Twitter, dll.

Coba lihat beberapa contoh nyata fantastis yang lain:

- [Here is Today](http://hereistoday.com)
- [IBM Design](http://ibm.com/design)
- [Run4Tiger](http://run4tiger.com)

Aturan standar untuk JavaScript aslinya bernama ECMAScript atau ES. Dimulai pada 2009, hingga pada 2012 semua browser modern sepenuhnya mendukung ES versi 5 atau ES5. Lalu yang paling signifikan, pada 17 Juni 2015, ECMA International yang merupakan badan standarnya, mempublikasikan versi 6 dari ES yang secara resmi dinamai ECMAScript 2015, walaupun secara umum lebih dikenal sebagai ECMAScript 6 atau ES6. Diekspektasikan standar tersebut dirilis secara berkala tahunan. Penting untuk diketahui beberapa fitur ES2015/ES6 belum diimplementasikan di beberapa platform/browser.

Pada dasarnya, setiap bahasa pemrograman modern memiliki hal-hal yang tertulis berikut. Hal-hal ini memungkinkan programmer untuk menulis code (computer code) untuk membuat/membangun program yang dapat menyelesaikan masalah seperti menghitung angka, memproses data, membuat aplikasi web, dan banyak lainnya.

- sintaks (syntax) dan pernyataan (statement): terkait bagaimana cara menulis code-nya
- tipe data (data types) dan/atau struktur data (data structure)
- variabel dan operator
- kumpulan/koleksi data (collections) serta perulangan/iterasi (loop/iteration)
- kondisional (conditional) atau percabangan (branching)
- fungsi/metode (function/method)

Spesial untuk JavaScript, kita bisa menggunakan editor code biasa (code editor) untuk mengetikkan JavaScript bersamaan dengan HTML dan CSS; atau kita bisa langsung mengetikkan code ke dalam dev tools (terdapat di Chromium/Chrome dan Firefox) dengan membuka tab `console` (`Ctrl+Shift+J` atau `Cmd+Opt+J` di Chrome, `Ctrl+Shift+K` atau `Cmd+Opt+K` di Firefox). Artinya JavaScript bisa langsung digunakan dan ditulis di dalam browser ataupun editor code.

Kamu juga bisa gunakan extension browser untuk editor JavaScript yang lebih dari sekadar console di dev tools seperti [Chrome Scratch JS](https://chrome.google.com/webstore/detail/scratch-js/alploljligeomonipppgaahpkenfnfkn), [JSBin](http://jsbin.com), ataupun [CodePen](https://codepen.io). Apapun tools yang dipakai, yang terpenting adalah kita dapat mengakses editor atau console yang akan menjalankan sintaks JavaScript.

### Sintaks (Syntax) dan Pernyataan (Statement)

Sintaks itu seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemrograman. Merupakan kata-kata dan perintah (command) pada bahasa yang juga merupakan instruksi untuk disusun menjadi sebuah program yang dibuat atau dikembangkan. Kita gunakan sintaks tertentu untuk membuat statement program, instruksi untuk dijalankan/dieksekusi oleh web browser, compiler, ataupun interpreter. Dalam JavaScript, ada berbagai sintaks yang polanya seperti `alert();`, `console.log();`, `document.write();`, dan masih banyak lagi. Kesimpulannya, sintaks dan statement adalah ekspresi (expression) apapun yang biasanya diikuti dengan titik koma (semicolon `;`) ataupun hal-hal yang bisa dieksekusi oleh penjalan code (executor).

Kebutuhan editing program JavaScript dapat seminimal mungkin hanya menggunakan console di dev tools tanpa program lain. Karena akses yang mudah ini, kamu bisa langsung mempraktikkan contoh-contoh code yang terdapat di sini.

- ▢ Buatlah file `try.html` di sebuah repositori kosong lalu inisialisasi dengan Git
- ▢ Bukalah file tersebut. Lalu gunakan dev tools console untuk menulis beberapa statement berikut, lihatlah apa yang terjadi. Catatan bahwa kamu tidak perlu menyertakan tanda/simbol `>` karena ini hanya menandakan area masukan/isian console.

```javascript
> "Hello!";
> document.write("Hello you too!");
> console.log("Hello, computer!");
> alert("Hello, human!");
> prompt("What is your name?");
> console.log("Multiline\n text!");
```

Kamu akan melihat berbagai hasil respon atau keluaran (output) dari browser dan console berupa berbagai macam teks:

![JS Console Challenge](assets/js-console.png)

Pahamilah perbedaan apa saja yang ada pada berbagai statemen tersebut. Mereka punya berbagai kegunaan yang berbeda. Ada yang untuk menulis ke HTML, pencatatan atau menulis/mencetak log ke console (logging), alert, dan meminta masukan dari pengguna. Kita baru saja menjalankan/memanggil beberapa fungsi berbeda dan/atau ekspresi yang memungkinkan kita untuk mencetak teks dengan berbagai cara. Bahkan ada juga yang memunculkan form isian teks agar pengguna dapat juga menentukan teks yang akan dicetak.

Perlu diketahui sebenarnya JavaScript tidak punya fungsi cetak (print) atau display secara built-in. Seringkali kita antara harus cetak ke browser atau console. Sehingga JavaScript selalu membutuhkan aplikasi lain, tidak dapat berdiri sendiri.

Baris-baris pada code program juga disebut ekspresi (expression), sejumlah nilai (values), variabel (variables), dan penghubung (operators) yang saat diinterpretasi akan mengembalikan sebuah nilai (return a value). Sebagai contoh:

- `"Hello!"` adalah ekspresi yang berevaluasi menjadi `Hello!` di console.
- `1 + 1` adalah ekspresi yang berevaluasi menjadi `2`.

Kita juga bisa menghapus (clear) jendela console (console window) dengan `Ctrl+L`. Lalu untuk ganti baris atau masuk ke baris baru saat mengetikkan code, tekan `Shift` sambil `Return`/`Enter`.

Modern ini, kita bisa menulis statement JavaScript tanpa titik coma (`;`).
Agar penulisan code kita sederhana, kita tidak perlu pakai titik koma. Tapi juga ada beberapa aturan yang memerlukannya, berarti kita perlu mengikutkannya. Titik koma tersebut biasanya digunakan untuk mengakhiri (terminate) sebuah statement. Kita bisa memiliki kumpulan campuran (composited) atau gabungan (combined) statement seperti berikut, dibungkus dengan kurung kurawal, biasa disebut statement blok (block statement). Amati perbedaannya:

```javascript
> console.log("Try"); console.log("again");
> console.log("Try") console.log("again")
> { console.log("Try"); console.log("again"); }
> {
    console.log("Try");
    console.log("again");
  }
```

### JavaScript dalam HTML

JavaScript memiliki banyak cara untuk dapat digunakan dalam HTML selain lewat console. Perhatikan contoh berikut.

```html
<html>
  <head>
    <script src="example.js"> <!-- cara pertama -->
  </head>
  <body>
    <h1 onClick="changeColor('red')">Something</h1> <!-- cara kedua -->
    <script>
       document.write("Tulisan"); <!-- cara ketiga -->
    </script>
  </body>
</html>
```

- Cara pertama merupakan mengikutkan file JavaScript secara external.
- Yang kedua menggunakan code JavaScript dalam element HTML tertentu.
- Kemudian yang terakhir adalah meng-embed code JavaScript langsung di element `script`.

### Komentar (Comments)

Cara unik untuk menambahkan beberapa penjelasan dan membuatnya lebih mudah terbaca seringkali digunakan oleh programmer yang baik. Bisa juga digunakan untuk mencegah eksekusi code, saat mencoba-coba atau mengetes code alternatif atau yang belum berjalan.

```javascript
> // We can use single line of comment
> /* atau multi line of comment
     that often used to explain a long statements */
> /* The multi-line style can be used as as single line as well */
> // console.log("Try me!"); // This code would not run
```

Berikutnya di berbagai contoh yang ada, kita tidak perlu mengetikkan komentar untuk menjalankan statement. Hanya dibaca sebagai keterangan.

### Variabel (Variable)

Variabel bisa memegang atau berisi hampir semua tipe data yang tersedia. Variabel memungkinkan kita untuk memuat atau menyimpan nilai data ke dalam sesuatu. Biasanya bersifat sementara saat program dijalankan.

Mari kita gunakan beberapa angka:

```javascript
> var x = 8
> x
> var y
> y = x + 2
> var z = x - 2
> x = 5 + 1
> y++
> y
> z = x + y
> x = z / 2
> var abc
> var a, b, c
```

lalu beberapa teks/tulisan:

```javascript
> var planetName, completeLocation
> planetName = "Earth"
> completeLocation = "Planet " + planetName
```

Seperti aljabar, kita gunakan variabel (seperti `x` atau `y`) utnuk menyimpan nilai dan ekspresi matematis (`z = x + y`). Setelah kita inisialisasi atau deklarasikan variabel dengan kata kunci (keyword) `var`, kita bisa langsung menetapkan/menentukan nilai pada variabel tersebut.
Variabel harus diidentifikasi dengan nama yang unik, hindari nama yang sama atau membingungkan atau yang sulit dibaca. Variabel yang memiliki nama unik ini disebut identifier, namanya bisa pendek (seperti `a`) atau lebih jelas/deskriptif (`name`, `age`, `totalVolume`).

Kita juga bisa deklarasikan tanpa nilai (seperti `abc` tadi). Secara biasa (default) itu akan bernilai `undefined`.
Dengan cara ini itu bisa menjadi bernilai sesuatu yang harus dihitung terlebih dahulu atau yang akan disediakan nanti pada saat ada masukan/isian pengguna (user input). Lebih lagi kita bisa deklarasikan beberapa variabel sekaligus dalam satu baris (seperti `a`, `b`, `c` tadi).

Ada beberapa varian gaya penamaan yang bisa kita gunakan untuk menggabungkan beberapa huruf/kata ke dalam satu nama variabel:

```javascript
// Hyphens atau Kebab Case:
> first-name, last-name, planet-blue-earth

// Underscore:
> first_name, last_name, planet_blue_earth

// Camel Case dengan Title Case
> FirstName, LastName, PlanetBlueEarth
// Camel Case with lowercase first
> with lowercase first: firstName, lastName, planetBlueEarth

// All Uppercase:
> SWITCH, ENABLE, GRAVITY
```

Gaya penamaan sebenarnya bebas dan terserah. Tapi di JavaScript kami merekomendasikan untuk menggunakan camel case dengan lowercase di huruf pertama nama variabel ataupun fungsi/metode. Untuk penamaan semuanya uppercase biasanya digunakan untuk nilai konstanta (constant) yang selalu tetap dan tidak akan diganti. Aturan umum dalam membuat nama variabel adalah:

- Nama dimulai dengan sebuah huruf
- Nama dapat berisi karakter/huruf, angka/digit, simbol
- Nama bisa dimulai dengan `$` dan `_`, tapi sementara kita hindari dulu
- Penamaan itu case sensitive `x` dan `X` berbeda
- Kata-kata yang sudah dipesan (reserved words) oleh JavaScript seperti kata kunci `var`, `function`, `for`; tidak bisa digunakan untuk nama variabel

### Operator

Kamu sudah tahu beberapa aritmatika dasar dan operator penugasan (assignment operators) dari aktifitas sebelumnya dengan variabel. Mari kita coba lebih jauh!! Assignment operator memungkinkan kita untuk mengkombinasikan tanda sama dengan (equal sign `=`) dengan tanda aritmetis untuk membuat statement. Variabel (`a`) atau angka (`10`) disebut operand dan operasi yang akan dilakukan oleh dua operand didefinisikan dengan operator (`=` atau `+=`).

```javascript
> var a=0,b=1,c=2,d=3,e=4,f=5,g=6,h=7,i=8,j=9,k=10,l=11,m=12
> a = b
> c += d  // same as c = c + d
> e -= f  // e = e - f
> g *= h  // g = g * h
> j /= k  // and so on
> l %= m
> a += 10
> b *= 20
```

Operasi perbandingan dan logis memungkinkan kita untuk membandingkan atau mengecek kondisi para operand. Biasanya menghasilkan antara betul (`true`) atau salah (`false`).

```javascript
==   // equal to
===  // equal value dan equal type
!=   // not equal
!==  // not equal value atau not equal type
>    // greater than
<    // less than
>=   // greater than atau equal to
<=   // less than atau equal to
?    // ternary operator

> var x=10,y=20,z=30
> x == y
> y === 20
> x != 1.0
> y !== 200
> z > x
> y <= z
> z == (x + y)
```

Operator tipe data memungkinkan kita untuk mengecek sesuatu tentang variabel atau objek.

```javascript
typeof	    // Returns the type of a variable
instanceof	// Returns true if an object is an instance of an object type
```

Operator pendahulu untuk konsiderasi (precedence) mendeskripsikan sususan/urutan yang operasinya diprioritaskan untuk dilakukan (performed) dalam sebuah ekspresi. Untuk contoh sederhana seperti matematika zaman sekolah, perkalian (multiplication) dan pembagian (division) dilakukan pertama kali. Tanda kali (`*`) dan bagi (`/`) memilki precedence yang lebih tinggi dari tanda tambah (`+`) dan kurang (`-`). Precedence juga bisa dipaksa dengan tanda kurung biasa (parentheses). Saat ada precedence yang sama, maka akan dihitung/dikomputasi dari kiri ke kanan. Ini ada tabel contekan yang menggambarkan nilai precedence dari paling tinggi ke rendah (tidak perlu diingat semua, yang penting-penting saja).

|Value|Operator| Descriptions and Example |
|-----|--------|--------------------------|
| 19  | `( )`  | Expression grouping: `(8 + 2)`
| 18  | `.`    | Member: `person.name`
| 18  | `[]`   | Member: `person["name"]`
| 17  | `()`   | Function call: `myFunction()`
| 17  | `new`  | Create an object: `new Date()`
| 16  | `++`   | Postfix Increment: `i++`
| 16  | `--`   | Postfix Decrement: `i--`
| 15  | `++`   | Prefix Increment: `++i`
| 15  | `--`   | Prefix Decrement: `--i`
| 15  | `!`    | Negation, logical not: `!(x==y)`
| 15  | `typeof`     | Check type: `typeof abc`
| 15  | `instanceof` | Check instance: `instanceof person`
| 14  | `*`    | Multiplication: `10 * 5`
| 14  | `/`    | Division: `10 / 5`
| 14  | `%`    | Modulo division: `10 % 5`
| 14  | `**`   | Exponentiation: `10 ** 2`
| 13  | `+`    | Addition: `10 + 5`
| 13  | `-`    | Subtraction: `10 - 5`
| 12  | `<<`   | Shift left: `x << 2`
| 12  | `>>`   | Shift right: `x >> 2`
| 11  | `<`    | Less than: `x < y`
| 11  | `<=`   | Less than atau equal: `x <= y`
| 11  | `>`    | Greater than: `x > y`
| 11  | `>=`   | Greater than atau equal: `x >= y`
| 10  | `==`   | Equal: `x == y`
| 10  | `===`  | Strict equal: `x === y`
| 10  | `!=`   | Unequal: `x != y`
| 10  | `!==`  | Strict unequal: `x !== y`
| 6   | `&&`   | dan: `x && y`
| 5   | `||`   | Or: `x || y`
| 3   | `=`    | Assignment: `x = y`
| 3   | `+=`   | Assignment: `x += y`
| 3   | `-=`   | Assignment: `x -= y`
| 3   | `*=`   | Assignment: `x *= y`
| 3   | `/=`   | Assignment: `x /= y`

## References

**Programming**

- [The Beginner’s Guide to Learning to Program, article by Scott H Young](https://www.scotthyoung.com/blog/2012/09/09/learn-to-program)
- [Programming 101: The 5 Basic Concepts of any Programming Language, article by Trevor Page](https://howtoprogramwithjava.com/programming-101-the-5-basic-concepts-of-any-programming-language)
- [Programming Concepts: A Brief Tutorial for New Programmers, article by Richard Holowczak](http://holowczak.com/programming-concepts-tutorial-programmers)
- [Bahasa Pemrograman Apa yang Cocok untuk Dipelajari Pertama Kali? oleh Rian Yulianto W di CodePolitan](https://www.codepolitan.com/bahasa-pemrograman-apa-cocok-dipelajari-pertama-kali)

**JavaScript**

- [Learning to Code? Why You Should Learn JavaScript First, on General Assembly](https://generalassemb.ly/blog/learning-to-code-why-you-should-learn-javascript-first)
- [5 Alasan Mengapa Kamu Harus Belajar Bahasa Pemrograman JavaScript, via Tech in Asia](https://id.techinasia.com/5-alasan-mengapa-kamu-harus-belajar-javascript)
- [JavaScript.com](http://javascript.com)
- [JavaScript (Original) on Codecademy](https://www.codecademy.com/en/tracks/javascript-original)
- [JavaScript on Codecademy](https://www.codecademy.com/learn/javascript)
- [CS101 Introduction to Computing Principles](https://web.stanford.edu/class/cs101) (Week 1 and 2)
- [JavaScript Guide, by Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [JavaScript Guide, by Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- [Belajar javascript untuk pemula, di Sekolah Koding](https://sekolahkoding.com/kelas/belajar-javascript-untuk-pemula)
- [What Makes Javascript Weird...and AWESOME (YouTube videos by LearnCode.academy)](https://www.youtube.com/watch?list=PLoYCgNOIyGABI011EYc-avPOsk1YsMUe_&v=JEq7Ehw-qk8)
