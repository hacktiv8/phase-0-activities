# Learn Logic Flow in JavaScript

## Objectives

- ▢ Memahami kegunaan dan perbedaan operator `&&`, `||`, dan `!`.
- ▢ Mendeskripsikan percabangan (branching) atau alur kendali (control flow) menggunakan `if`, `else if`, dan `else`.
- ▢ Mendeskripsikan iterasi atau perulangan (loop) dan menjelaskan bagaimana beberapa perulangan yang berbeda bekerja untuk `for`, `while`, dan `do`.

## Learnings

### Pengkondisian (Conditionals)

Program bukan apa-apa tanpa kasus pengkondisian. Komputer semestinya tau apa saja kemungkinan yang diekspektasi sesuai keingingan programmer. Dalam kata lain, ini memungkinkan kita untuk melakukan alur kendali (control flow). Melakukan tindakan berbeda untuk keputusan yang berbeda terhadap keadaan/kondisi. Kondisi bisa merupakan statement yang punya evaluasi `true` atau `false`. Kebanyakan kondisi menggunakan kurang lebih hal-hal berikut:

- percabangan (branching): `if`, `else if`, `else`, dan `switch`
- perulangan (loop/repeating/iteration): `for`, `while`, dan `do`
- perbandingan (comparison): `===`, `!==`, `&&`, `||`, `!`, dll

**Catatan**: Jika kamu mengalami masalah di console, gunakan Scratch JS atau JSBin. Karena pastinya di console sangat sulit mengatur beberapa baris kode.

### Percabangan (Branching)

Menggunakan if, else if, dan else:

```javascript
if (true) {
  console.log("Alright!")
}

if (Infinity > 0) {
  console.log("That's right!")
} else {
  console.log("That's wrong!")
}

var number
if (!number) {
  console.log("There is no number!")
}
```

```javascript
var age, hello;
age = 22;
if (age < 14) {
  hello = "boys dan girls";
} else if (age < 20) {
  hello = "teenage boys dan girls";
} else {
  hello = "ladies dan gentlemen";
}
console.log("Hello, " + hello + " !");
```

Dikombinasikan dengan nested conditional (kondisi bersarang), kondisi di dalam kondisi!

```javascript
var color, comment;

color = prompt("Color name?");

if (!!color) {
  if ((color === "black") || (color === "white")) {
    comment = "monochrome!";
  } else if (color === ("red" || "orange" || "yellow" || "green" || "blue" || "purple")) {
    comment = "rainbow!";
  } else {
    comment = "speechless!"
  }
} else {
  console.log("Please mention your first color");
}

console.log(comment);
```

Menggunakan `switch`, `case`, dan `break`:

```javascript
var fruitName = prompt("Fruit name?");
switch (fruitName) {
  case "apple" || "Apple":
    console.log("Red atau green fruit!");
    break;
  case "banana" || "Banana":
    console.log("Yellow atau green fruit!");
    break;
  case "orange" || "Orange":
    console.log("Orange fruit");
    break;
  default:
    console.log("I don't know that fruit");
}
```

```javascript
switch (new Date().getDay()) {
  case 1:
  case 2:
  case 3:
  default:
    text = "Working days";
    break;
  case 4:
  case 5:
    text = "Weekend soon!";
    break;
  case 0:
  case 6:
    text = "Weekend!";
}
```

### Perulangan (Loop)

Statement iterasi yang berdasarkan kondisi yang diinginkan. Menggunakan `for` memerlukan tahap inisialisasi, kelanjutan, dan ekspresi akhir (final) dari iterasi. Ekspresi blok berikut di bagian atasnya juga opsional.

```javascript
for (var i = 0; i <= 8; i++){
  console.log(i);
}
```

yang sama saja dengan...

```javascript
var i = 0
for (;;) {
  if (i > 8) break
  console.log(i)
  i++
}
```

`continue` digunakan untuk menjalankan iterasi selanjutnya...

```javascript
var i = 1, j = 100
while (i < 8) {
  i++;
  console.log(i)
  if (i === 5) {
    continue;
  }
  j += i;
  console.log(j)
}
```

Kita bisa gunakan `for...in` untuk iterasi terhadap properti yang dapat dihitung (enumerable properties) dari sebuah objek, dalam urutan yang terserah kita yang mana tiap properti yang berbeda, suatu statement bisa dijalankan.

```javascript
var animals = {lion:1000, tiger:2000};
for (var number in animals) {
  console.log(animals[number]);
}
```

Dengan catatan lain yaitu `for...of` digunakan untuk membuat perulangan yang beriterasi/lewat berkali-kaliterhadap objek yang dapat diiterasi (iterable objects) termasuk Array, String, arguments object, dan lainnya. Spesifik untuk koleksi/kumpulan data saja daripada semua objek. Memanggil (invoking) kaitan iterasi dengan statement yang akan dijalankan untuk tiap nilai pada properti yang berbeda.

```javascript
let numbers = [1, 2, 3];
for (let value of numbers) {
  console.log(value);
}

let text = "foobar";
for (let character of text) {
  console.log(character);
}
```

Menggunakan `while` dan `do` dapat menampakkan eksekusi tak terbatas (infinite/unlimited), kecuali digunakan berhenti paksa (`break`). Biasanya digunakan unlimited condition untuk melihat (watching) atau mendengarkan (listening) sesuatu seperti kejadian (`event` yang akan kita bahas pekan depan).

```javascript
while (true) {
  // An infinite loop!
  console.log("unlimited true")
}

while (true) {
  console.log("true")
  break; // break the loop
}
```

```javascript
var input;
do {
  input = getInput();
} while (!isValid(input))
```

### References

- [Learn JavaScript in Y Minutes](http://learnxinyminutes.com/docs/javascript)
- [JavaScript cheat sheet, by Marijn Haverbeke](http://marijnhaverbeke.nl/js-cheatsheet.html)
- [Javascript Cheat Sheet on OverAPI](http://overapi.com/javascript)
- [DevDocs JavaScript API Documentation](http://devdocs.io/javascript)
