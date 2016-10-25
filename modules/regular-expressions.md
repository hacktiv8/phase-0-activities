# Explore Regular Expressions!

## Objectives

Regular Expressions adalah ...
Regular Expressions, atau disingkat menjadi Regex, di kalangan programmer, kadang dianggap menjadi satu hal yang sangat menyeramkan, dikarenakan nature mereka yang membuat kita harus menghapal berbagai simbol yang tersusun dengan sangat abstrak. Namun, pada saat kita telah mampu menulis pattern regex kita sendiri, akan sangat mudah memahaminya. Kamu tidak mau kan, harus meng-googling setiap pattern regex dan mencoba satu per satu?


- ▢ Mengetahui Kegunaan Regular Expressions
- ▢ Memahami simbol-simbol yang digunakan pada Regular Expressions

## Learnings

### Mengetahui Kegunaan Regular Expressions

Kuncinya untuk memahami Regular Expressions adalah mampu menghapal simbol-simbol dibawah ini, beserta kegunaannya. Untuk memudahkanmu, kamu bisa mencatat, membuat semacam cheatsheet, atau membuat jembatan keledai dengan caramu sendiri untuk memudahkanmu.

```javascript
. // - Mencocokan karakter apapun, kecuali line breaks(jeda baris/enter).
* // - Mencocokan 0 atau lebih dari karakter terdahulu.
+ // - Mencocokan 1 atau lebih dari karakter terdahulu.
? // - Karakter terdahulu menjadi opsional. Mencocokan 0 atau 1.
\d // - Mencocokan digit apapun
\w // - Mencocokan karakter pada sebuah kata (alphanumeric dan underscore/garis bawah).
[XYZ] // - Matches any single character from the character class.
[XYZ]+ // - Matches one or more of any of the characters in the set.
$ // - Mencocokan ujung dari sebuah string.
^ // - Mencocokan awal dari sebuah string.
[^a-z] // - Ketika didalam sebuah class karakter, tanda ^ artinya NOT; dalam kasus ini, regex akan mencocokan apapun yang bukan karakter lowercase.
```

### Penggunaan Regular Expressions dalam JavaScript

#### Menulis Regex

Menulis Regex dalam javascript bisa dalam 2 bentuk, yaitu antara dengan membuat Regex object dengan menggunakan `new RegExp()`, atau menggunakan nilai literal yang diapit oleh karakter flash (/).

```javascript
var regexContohSatu = new RegExp("abc");
var regexContohDua = /abc/;
```

#### Test
Fungsi `test()` akan mengembalikan nilai `true` atau `false`, sesuai dengan pattern regex yang dibuat.

**Menggunakan Literal Value**
```javascript
var message = 'Regex itu Mudah!';
console.log(/[A-Z]/.test(message));
// mengembalikan nilai true karena minimal satu karakter memenuhi pattern A-Z

var messageAllLowerCase = 'regex itu mudah';
console.log(/[A-Z]/.test(messageAllLowerCase));
// mengembalikan nilai false karena tidak ada satupun karakter yang memenuhi pattern A-Z
```

**Menggunakan RegExp object**

```javascript
var regexPattern = new RegExp('[A-Z]');

var message = 'Regex itu Mudah!';
console.log(regexPattern.test(message));
// mengembalikan nilai true karena minimal satu karakter memenuhi pattern A-Z

var messageAllLowerCase = 'regex itu mudah';
console.log(regexPattern.test(messageAllLowerCase));
// mengembalikan nilai false karena tidak ada satupun karakter yang memenuhi pattern A-Z
```

#### Split
Fungsi `split()` akan memecah setiap pattern yang ditemui ke dalam bentuk array. Fungsi `split()` ini
pernah kita gunakan sebelumnya dalam memecah string menjadi array.

```javascript
var str = 'belajar regex itu menyenangkan';
console.log(str.split(/\s/));
// mengembalikan nilai "belajar, regex, itu, menyenangkan" karena \s adalah sebuah pattern untuk satu spasi.
```

#### Replace
Fungsi `replace()` akan mengganti seluruh sebuah blok tertentu dalam sebuah teks, dan menggantinya dengan karakter atau teks lain.

```javascript
var stringAwal = 'Regex itu sangat susah!';
stringHasil = stringAwal.replace(/susah/, 'mudah');
console.log(stringHasil); // mengembalikan nilai "Regex itu sangat mudah!"
```

#### Match
Fungsi `match()` akan mengembalikan dalam bentuk array setiap kali sebuah kecocokan dengan pattern ditemukan di dalam teks.

**Contoh 1 Penggunaan Match - Mencocokan Karakter**
```javascript
var message = 'Regex seru!';
console.log(message.match(/e/));
// menampilkan "e", namun hanya sekali

console.log(message.match(/e/g));
// menampilkan "e" untuk setiap "e" yang terdapat di dalam teks. `g` menandakan pencarian secara global, tidak hanya satu kali
```

**Contoh 2 Penggunaan Match - Mencocokan Karakter dan Mengecualikan Punctuation atau Simbol**
```javascript
var string = 'Walaupun regex banyak mengandung simbol, tapi tidak serumit seperti !@#%^%#$*( , ^%&*!!^& dan !#*#$&*@%#';
console.log(string.match(/[a-z]+/gi));
//menampilkan ["Walaupun", "regex", "banyak", "mengandung", "simbol", "tapi", "tidak", "serumit", "seperti", "dan"]
```

Simbol-simbol diatas, sering disebut sebagai Punctiation. Seringkali dalam beberapa kasus, kita mau menghapus semua simbol-simbol diatas.

Jika kamu teliti, kamu pasti menemukan simbol `+` dibelakang `[a-z]`. Simbol `+` disini berarti match akan menyatukan seluruh karakter yang cocok dengan pattern a-z hingga menemukan pattern lain diluar pattern tersebut. Dalam kasus contoh di atas, setiap kali menemukan spasi, contohya pada `Walaupun regex` match akan memisahkan `Walaupun` dan `regex` karena ditemukannya spasi tersebut. Apabila kamu penasaran, cobalah hapus simbol `+` dari code diatas, dan jalankanlah kembali. Hasilnya akan berbeda!



### Mengetest Kemampuan Regular Expressions

Ada sebuah platform yang cocok untuk melatih kamu dalam menggunakan regex, yaitu [regexr.com](http://regexr.com/)

## References

- [HTML, CSS & JS Frameworks and when to use them, by Chris Wharton](https://chriswharton.me/2016/05/html-css-and-js-frameworks-use)
- [Front-end Hyperpolyglot, by Jeff Carp](https://jeffcarp.github.io/frontend-hyperpolyglot)
- [What is Semantic Versioning (SemVer)?, by AbdulFattaah Popoola](https://abdulapopoola.com/2015/10/26/what-is-semver)
