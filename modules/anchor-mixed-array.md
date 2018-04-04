# Menggunakan Built-in Function pada Array

Array pada JavaScript memiliki sekumpulan *built-in function* yang digunakan untuk mempermudah developer untuk mengolah data di dalamnya. Beberapa fungsi yang sering digunakan antara lain `join`, `split`, `slice`, `splice`, dan `sort`. Kerjakanlah tantangan ini untuk memperkuat pengertian kamu tentang *built-in function* tersebut.

## Objectives

- Mengerti Kegunaan dari *Built-in Function* yang dimiliki Array
- Mampu Menggunakan *Built-in Function* yang dimiliki Array

## Directions

```javascript
//contoh output
["0001", "Roman Alamsyah", "Bandar Lampung", "21/05/1989", "Membaca"]  
```
- Buatlah sebuah _function_ dengan nama `dataHandling2` yang akan menerima input array seperti di atas.

- Gunakan fungsi `splice` untuk memodifikasi variabel tersebut agar menjadi seperti array dibawah. Lalu `console.log` array yang baru seperti di bawah.

```javascript
["0001", "Roman Alamsyah Elsharawy", "Provinsi Bandar Lampung", "21/05/1989", "Pria", "SMA Internasional Metro"]  
```

- Berdasarkan elemen yang berisikan tanggal/bulan/tahun (elemen ke-4), ambil angka bulan dan `console.log` nama bulan sesuai dengan angka tersebut.
    - Gunakan `split` untuk memisahkan antara tanggal, bulan, dan tahun.
    - Format tanggal pada data adalah **dd-mm-YYYY**
    - Misal angka bulan 01, tuliskan "Januari"
    - Gunakan `switch case` untuk menuliskan bulan di atas.

- Pada array hasil `split` dari tanggal/bulan/tahun, lakukan *sorting* secara *descending* dan `console.log` array yang sudah di-sort.

- Masih pada array hasil `split` dari elemen tanggal/bulan/tahun, gabungkan semua elemen menggunakan `join` dan pisahkan dengan karakter strip (-) lalu `console.log` hasilnya.

- Nama (elemen ke-2), harus dibatasi sebanyak 15 karakter saja. Gunakan `slice` untuk menghapus kelebihan karakter dan `console.log` nama yang sudah di-slice, sebelum di-slice pastikan Nama (elemen ke-2) sudah dalam bentuk `String` agar bisa di-slice.

### Test-case

Untuk memastikan program kamu sudah bekerja dengan benar, gunakan *test-case* dibawah.

```javascript
var input = ["0001", "Roman Alamsyah ", "Bandar Lampung", "21/05/1989", "Membaca"];
dataHandling2(input);

/**
 * keluaran yang diharapkan (pada console)
 *
 * ["0001", "Roman Alamsyah Elsharawy", "Provinsi Bandar Lampung", "21/05/1989", "Pria", "SMA Internasional Metro"]
 * Mei
 * ["1989", "21", "05"]
 * 21-05-1989
 * Roman Alamsyah
 */
```
