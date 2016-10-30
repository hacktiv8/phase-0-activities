# Get to Know Functional Programming (FP)

## Objectives

- ▢ Mengetahui salah satu paradigma pemrograman modern yang intuitif dengan dunia nyata.

## Directions

### Mengenal Functional Programming (FP)

Functional Programming adalah sebuah paradigma programming yang mengedepankan immutability (tidak dapat merubah nilai, namun mengembalikan nilai baru), bebas dari side-effect, dan kemudahan composability dan reusability dari sebuah kode. Namun, kamu tidak perlu memusingkan hal ini terlebih dahulu, karena di materi ini kita hanya akan langsung menggunakan implementasinya di program kita.  

### Mengenal Implementasi Functional Programming

Salah satu implementasi functional programming yang saat ini akan kita gunakan adalah prinsip immutability, atau sebuah prinsip dimana sebuah tindakan tidak boleh mengubah nilai sebuah variabel atau bisa juga disebut state, namun yang lebih baik adalah mengembalikan nilai baru.

Contoh sederhana mengenai mutability dan immutability adalah sebagai berikut:

Kita punya variabel bernama mutableVariable, dan kita mau mengubah nilainya menjadi 10 kali dari normal.

```javascript
let mutableVariable = 5;
mutableVariable *= 10;
console.log(mutableVariable); // 50
```

adapun, dengan prinsip immutability, ketimbang kita mengubah nilai dari variabel tersebut, cara functional programming akan mengassign variabel baru untuk menampung hasil 10 kali lipat tersebut.

```javascript
let immutableVariable = 5;
let newMultipliedVariable = 10 * immutableVariable;
console.log(newMultipliedVariable); // 50
```

Gambaran di atas secara sederhana menjelaskan perbedaan antara mutability dan immutability.

*Kapan kita harus menggunakan functional programming, terutama bagian immutability?*

Contoh kasus akan membuat kita lebih paham kapan harus menggunakan FP. Bayangkan, kita adalah sebuah manager dari sebuah departemen store dan kita menjalankan promo potongan harga 10%. Dengan prinsip mutability, berarti kita mengubah seluruh harga barang dari harga awal menjadi harga yang telah didiskon. Misal harga kemeja adalah 500,000, maka harga kemeja sekarang berubah menjadi 450,000. Pada saat kemeja ini dijual, tentu tidak masalah, namun pada saat kita menghitung laba rugi, tentu kita harus mengetahui harga awal sebelum dikenakan diskon. Apabila kita menggunakan prinsip mutability, maka kita tidak bisa mendapatkan harga awal seluruh barang tersebut, karena harganya telah berubah.

Kemudian bayangkan jika kita menerapkan immutability kepada proses ini, dimana kita memiliki harga awal dan prinsip immutability membuat proses diskon mengembalikan nilai baru dan anggap saja kita tampung dan kita sebut menjadi "harga setelah diskon". dengan ini, kita bisa menjual barang dengan harga yang dikenakan diskon, namun kita tidak kehilangan nilai harga awal barang tersebut.

### Array Map Function
Dalam array, terkadang kita perlu untuk mengubah nilai di dalamnya, namun dengan prinsip immutability, kita ingin mendapatkan hasil perubahan nilai tersebut menjadi nilai baru.

**Contoh Map Sederhana 1**

```javascript
let arr = [1,2,3,4,5,6];
let duaKaliLipat  = arr.map(function(isiArray) {
  return isiArray * 2;
});

console.log(duaKaliLipat); // [2,4,6,8,10,12]
```

**Contoh Map Sederhana 2**

```javascript
let arr = ['bundar', 'kotak', 'segitiga'];
let newArr = arr.map(function(isiArray) {
  return 'Topi saya' + isiArray;
});

console.log(newArr); // ['Topi saya bundar', 'Topi saya kotak', 'Topi saya segitiga']
```

### Array Filter Function
Dalam array, terkadang kita perlu memfilter isi dari array tersebut, dan mengembalikan nilai baru hasil filter tersebut. Kita bisa menggunakan `filter` untuk kasus ini.

**Contoh Filter Sederhana 1**

```javascript
let arr = [1,2,3,4,5,6,7,8,9];
let habisDibagiTiga = arr.filter(function(isiArray) {
  if(isiArray % 3 === 0) {
    return true; // Jika true, isi array tidak akan disaring keluar
  }
  else {
    return false; // Jika true, isi array akan disaring keluar
  }
});

console.log(habisDibagiTiga); // [3,6,9]
```

atau, lebih sederhana dengan:

```javascript
let arr = [1,2,3,4,5,6,7,8,9];
let habisDibagiTiga = arr.filter(function(isiArray) {
  return isiArray % 3 === 0 // akan mengembalikan nilai true atau false
});

console.log(habisDibagiTiga); // [3,6,9]
```

## References

- [Introduction to Object-Oriented JavaScript, on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
- [Object Oriented JavaScript: Udacity](https://www.udacity.com/course/object-oriented-javascript--ud015)
