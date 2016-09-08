# Challenge !! Restaurant

## Objectives

Di minggu ke-2 kita sudah mempelajari mengenai array, loop, dan cara membuat function.. di minggu ke 3 pun kita sudah membuat beberapa challenge untuk melatih materi yang didapatkan.

Sebelum melanjutkan minggu ke 4 ini, pastikan kamu sudah paham materi di minggu-minggu sebelumnya. Di minggu 4 ini kita akan bermain dengan class dan recursive.

Baca tentang javascript class disini : https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Classes

## :sunny: Tugas 1
Kita akan membangun sistem kasir restaurant sederhana. Restaurant selalu memiliki menu, kemudian pesanan dari pelanggan, dan juga total yang harus dibayar oleh pelanggan.

1. Buatlah sebuah class bernama Restaurant
2. Buatlah sebuah method bernama "addMenu" untuk memasukkan data menu restaurant. Menu ini memiliki atribut nama, jenis, dan harga. <br>
Masukan data menu dengan data sbb :
  - nasi goreng | makanan | 25000
  - ayam goreng | makanan | 12000
  - tahu        | makanan | 5000
  - teh         | minuman | 5000
  - coca cola   | minuman | 15000
  - jus buah    | minuman | 25000
3. Kemudian, buatlah sebuah method untuk menampilkan list dari menu restaurant di atas.
4. Setelah selesai, kirim hasil code kamu dengan gist, dengan nama file : menuRestaurant.js. Share gist kamu melalui private message slack ke instructor yang sedang in charge.

##Output
Ketika code Js kamu di run, akan menghasilkan seperti ini di console :

```
  "add new menu : nasi goreng"
  "add new menu : ayam goreng"
  "add new menu : tahu"
  "add new menu : teh"
  "add new menu : coca cola"
  "add new menu : jus buah"
  "daftar menu : "
  [[object Object] {
    harga: 25000,
    jenis: "makanan",
    nama: "nasi goreng"
  }, [object Object] {
    harga: 12000,
    jenis: "makanan",
    nama: "ayam goreng"
  }, [object Object] {
    harga: 5000,
    jenis: "makanan",
    nama: "tahu"
  }, [object Object] {
    harga: 5000,
    jenis: "minuman",
    nama: "teh"
  }, [object Object] {
    harga: 15000,
    jenis: "minuman",
    nama: "coca cola"
  }, [object Object] {
    harga: 25000,
    jenis: "minuman",
    nama: "jus buah"
  }]
```


## :sunny: Tugas 2
1. Buatlah sebuah method bernama "addOrder", fungsinya untuk memasukkan order dari customer. Masukan data order sbb : <br>
1 nasi goreng
1 teh
2. Kemudian buat method untuk menampilkan list dari order di atas
3. Setelah selesai, kirim hasil code kamu dengan gist, dengan nama file : menuRestaurant.js. Share gist kamu melalui private message slack ke instructor yang sedang in charge.

##Output
Ketika code Js kamu di run, akan menghasilkan seperti ini di console :

```
  "add order : nasi goreng"
  "add order : teh"

  "daftar pesanan : "
  "1 nasi goreng"
  "1 teh"
```


## :sunny: Tugas 3
1. Buatlah sebuah method bernama "billing", fungsinya menghasilkan total dari seluruh order customer di atas !
2. Setelah selesai, kirim hasil code kamu dengan gist, dengan nama file : billing.js. Share gist kamu melalui private message slack ke instructor yang sedang in charge.

## Output
ketika method billing dipanggil, akan menampilkan total dari order customer di atas (tugas 2) !
##Output
Ketika code Js kamu di run, akan menghasilkan seperti ini di console :

```
  "total billing normal : 30000"
```
