# JavaScript Data Types - Array

## Objectives

Tipe data ataupun struktur data adalah konsep penting dalam mengkategorisasikan beberapa hal/jenis berbeda pada unit, pengukuran, juga memungkinkan kita untuk beroperasi pada variabel.

## Learnings

### Array

Array adalah kumpulan dari berbagai data. Kita bisa tulis dengan kurung kotak (square brackets) dan butir-butirnya dipisah dengan koma. Indeks array berbasis-nol yang berarti urutan awalnya merupakan `[0]`, keduanya `[1]`, dan seterusnya.
Kita juga bisa memasukkan (insert), memperbarui/mengubah (update/change), atau bahkan meniadakan (undefine) nilai yang ada di dalam array. Spesifik di JS, kita bisa gunakan beberapa tipe data berbeda di dalam suatu array. Bahkan memasukkan array ke dalam array!

```javascript
> var animals = ["Lion", "Tiger", "Puma"]
> animals
> animals[0]
> animals[3] = "Jaguar"
> animals[8] = "Leopard"
> animals[1] = undefined
> animals
> animals[5]
> animals[0] = 100
> animals[1] = true
> animals
> animals[3] = ["Zero", 1, "Two"]
> animals[3][3] = "Three"
```

Array seperti tumpukan data. Bayangkan sebuah botol atau toples yang berisi beberapa lapis biskuit di dalamnya. Kita bisa mendorong (push) seperti memasukkan yang baru, mengeluarkan (pop) yang paling terakhir atau teratas, atau bahkan mengambil beberapa lapis data.

```javascript
> animals.push("Dragon")
> animals.pop()
> animals.slice(0, 2)
```

### Array Built-in functions

- push: menambah 1 nilai ke array ke index paling belakang
- pop: menghapus 1 nilai dari array index paling belakang
- unshift: menambah 1 nilai ke array index paling depan (index 0)
- shift: menghapus 1 nilai dari array index paling depan (index 0)
- join: menggabungkan seluruh element array menjadi sebuah string dan mengambil parameter sebagai simbol penyambung antar elemen
- sort: mengurutkan elemen di dalam array sesuai alphabet
- slice: mengambil beberapa lapis data
- splice: mengubah nilai array dengan menghapus dan/atau menambah nilai baru ke array
- split: memecah string dan mengembalikan array sesuai dengan separator / pemisah yang didefinisikan

**Penggunaan Built-in Function Array secara singkat**

```javascript
var animalsArray = ["lion", "horse"];
animalsArray.push("duck"); // menambahkan 1 nilai ke array bagian paling belakang
console.log(animalsArray); // ["lion", "horse", "duck"]
animalsArray.pop(); // menghapus 1 nilai array terbelakang
console.log(animalsArray); // ["lion", "horse"]
animalsArray.unshift("dog");
console.log(animalsArray); // ["dog", "lion", "horse"]
animalsArray.shift();
console.log(animalsArray);  // ["lion", "horse"]
animalsArray.sort();
console.log(animalsArray);  // ["horse", "lion"]
animalsArray.join(" and ");
console.log(animalsArray); // "horse and lion"
```
