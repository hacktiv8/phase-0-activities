# ES6 for JS Scope

## Objectives

- ▢ Memanfaatkan `let` dan `const` di JavaScript ES6

## Learnings

Seperti yang telah kita pelajari di referensi sebelumnya, kita telah mengenal local dan global scope. Tentunya dengan menggunakan `var`, hal ini akan menjadi masalah karena `var` sifatnya selalu global, dan tentu saja tetap bisa kita panggil di luar scope yang ada. Ataupun kita juga mengalami situasi dimana kita ingin mempertahankan supaya `var` kita immutable atau tidak dapat diubah, namun akibat dari kode kita, mungkin variabel kita tidak sengaja terubah dan kita harus menelusuri code yang telah dibuat sekian banyaknya.

**Contoh Pengaruh var dan Scope**
```javascript
var i = 0;
for(var i = 1; i < 9; i++) {
  // Looping 8 kali, i terakhir menjadi 9
}
var x = 5;
console.log(x + i); // 14, 5 + 9
```

Apabila kita mau mempertahankan nilai i sebagai 1, tidak dipengaruhi oleh looping tersebut, kita bisa menggunakan sintaks `let` yang menggantikan `var`. Bahkan, banyak pendapat bahwa `let` 100% menjadi pengganti `var`.

**Contoh Penggunaan let**
```javascript
let i = 0;
for(let i = 1; i < 9; i++) {
  // Looping 8 kali, i terakhir DALAM SCOPE menjadi 9
}
let x = 5;
console.log(x + i); // 5, 5 + 0
```

Tambahannya adalah, ada juga yang dinamakan `const`, yang merupakan variabel yang sekali kita definisikan, tidak bisa lagi kita ubah.

**Contoh Penggunaan const**
```javascript
const pi = 3.14;
let radius = 5;
let circleArea1 = pi * Math.pow(radius, 2);
console.log(circleArea1);
radius = 7;
let circleArea2 = pi * Math.pow(radius, 2);
console.log(circleArea2);
```

pada saat kita mengubah pi tersebut, akan muncul error: `TypeError: Assignment to constant variable.`.
