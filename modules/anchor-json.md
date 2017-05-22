# Menggunakan JSON

Setelah mengetahui cara membuat object menggunakan `function()`, kamu juga perlu mengetahui mengenai JSON. Format JSON akan sangat sering kamu temui saat mengembangkan aplikasi menggunakan JavaScript. Untuk melatih pemahamanmu tentang JSON, kerjakanlah tantangan ini dengan baik.

## Objectives

- Mengetahui Cara Membuat Object dengan JSON
- Memahami Konsep Object pada JavaScript

## Directions

- Buatlah 3 buah Object secara JSON dengan struktur seperti ini:

```javascript
var Human1 = {
    nama: '',
    hari: '',
    kehadiran: '',
    alasan: ''
}
```

- Isikan ketiga Object tersebut dengan data pada tabel di bawah:


Nama | Hari | Kehadiran | Alasan
---|---|---|---
Tono | Senin | Masuk |
Tono | Rabu | Masuk |
Tono | Jumat | Absen | Dinas Luar


- Masukan ketiga Object tersebut pada sebuah array

- Buatlah sebuah iterasi yang sebanyak jumlah item di dalam array yang berisi ketiga Object.

- Akses setiap Object seperti ketika mengakses sebuah nilai sebuah array.

- Akses property `nama` , `hari` dan `kehadiran` di dalam object

```javascript
//contoh
Array[index].objectProperty;
```

- Dari dalam iterasi, tampilkan informasi seperti berikut:

```
Nama: Tono
Hari: senin
Kehadiran: masuk

Nama: Tono
Hari: rabu
Kehadiran: masuk

Nama: Tono
Hari: jumat
Kehadiran: absen
Alasan: dinas luar
```

- Hitung jumlah hari kerja, jumlah hari masuk, dan jumlah hari absen. Tampilkan informasinya seperti berikut:

```
Total hari kerja minggu ini: 3 hari
Total Masuk: 2 hari
Total Tidak Masuk: 1 hari
```
