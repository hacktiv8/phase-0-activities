# Mengenal Penggunaan Function

## Objectives

- Mampu memahami serta mengimplementasi penggunaan function pada JavaScript

## Directions

1. Lanjutkan kode berikut ini hingga dapat menampilkan nilai / output yang diminta!

### Tugas 1

Buatlah sebuah fungsi bernama shoutOut(), yang mengembalikan nilai berupa "Halo Function!", yang kemudian
akan ditampilkan di console.

```JavaScript
/*
 BUATLAH KODE FUNCTION DISINI
*/

console.log(shoutOut()) // Menampilkan "Halo Function!" di console
```

### Tugas 2

Buatlah sebuah fungsi bernama calculateMultiply(), yang mengembalikan nilai berupa hasil kali dari dua parameter yang dikirim.

```JavaScript
/*
 BUATLAH KODE FUNCTION DISINI
*/

var num1 = 5;
var num2 = 6;

var hasilPerkalian = calculateMultiply(num1,num2);
console.log(hasilPerkalian); // Menampilkan angka 30
```

### Tugas 3

Buatlah sebuah fungsi bernama processSentence(), yang akan memproses seluruh parameter yang diinput menjadi satu kalimat berikut: "Nama saya [Name], umur saya [Age] tahun, alamat saya di [Address], dan saya punya hobby yaitu [hobby]!"

```JavaScript
/*
 BUATLAH KODE FUNCTION DISINI
*/

var name = "Agus";
var age = 30;
var address = "Jln. Malioboro, Yogjakarta";
var hobby = "gaming";

var fullSentence = processSentence(name,age,address,hobby);
console.log(fullSentence); // Menampilkan "Nama saya Agus, umur saya 30 tahun, alamat saya di Jln. Malioboro, Yogjakarta, dan saya punya hobby yaitu gaming!"
```
