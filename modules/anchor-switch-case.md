# Menggunakan Switch-Case

## Objectives

* Mengerti Cara Menggunakan `Switch-Case`
* Mengerti Logika `Switch-Case`

## Directions

Kamu ingin membuat seseorang terkesan? coba lakukan trik ini! Tebak hari lahir orang tersebut berdasarkan tanggal kelahirannya. Sayangnya trik ini sedikit rumit dan butuh sedikit hapalan. Untuk membantumu melakukan trik ini, buatlah suatu program di JavaScript. Dan bersiaplah menjadi pusat perhatian!

- Setiap bulan memiliki kode tertentu:
  - Januari, Oktober = 0
  - Mei = 1
  - Agustus = 2
  - Februari, Maret, November = 3
  - Juni = 4
  - September, Desember = 5
  - April, Juli = 6

- Tapi kamu tidak perlu khawatir, untuk menentukan `kodeBulan` sudah dibuatkan bagian program-nya (di bawah). Yang perlu kamu lakukan adalah melanjutkan isi program tersebut.

- Buatlah variabel dengan nama `tahunLahir`, variabel ini akan menyimpan 2 digit terakhir dari variabel `tahun`
  - gunakan modulus 100 untuk mendapatkan 2 digit terakhir dari `tahun`

- Buatlah variabel dengan nama `tahunLahirBagi4`. Isi dari variabel ini adalah angka bulat dari pembagian `tahunLahir` dengan 4
  - gunakan `Math.floor()` untuk mendapatkan angka bulat dari hasil pembagian

- Buatlah variabel dengan nama `jawaban`, variabel ini akan menampung hasil perhitungan dari:
  - (`tahunLahir` + `tahunLahirBagi4` + `tanggal` + `kodeBulan`) **modulus** 7

- Buatlah variabel dengan nama `tebakan`. Variabel ini akan digunakan untuk menampung tebakan hari lahir.

- Tentukan isi `tebakan` berdasarkan isi dari `jawaban` menggunakan **switch-case** dengan ketentuan sebagai berikut:
  - 0 => Minggu
  - 1 => Senin
  - 2 => Selasa
  - 3 => Rabu
  - 4 => Kamis
  - 5 => Jumat
  - 6 => Sabtu

## Source Code

```javascript
var tanggal; //masukkan tanggal lahir disini
var bulan; //masukkan bulan lahir disini
var tahun; //masukkan tahun lahir disini

var kodeBulan = 0;

switch (bulan) {
  case 'Januari':
  case 'Oktober':
    kodeBulan = 0;
    break;
  case 'Mei':
    kodeBulan = 1;
    break;
  case 'Agustus':
    kodeBulan = 2;
    break;
  case 'Februari':
  case 'Maret':
  case 'November':
    kodeBulan = 3;
    break;
  case 'Juni':
    kodeBulan = 4;
    break;
  case 'September':
  case 'Desember':
    kodeBulan = 5;
    break;
  default:
    kodeBulan = 6;
}

//Lanjutkan kode dari sini

console.log(tebakan);

```

### Notice

Trik ini hanya dapat digunakan untuk seseorang yang lahir sebelum tahun 2000. Untuk tanggal lahir dengan tahun 2000 keatas, kurangi angka hasil perhitungan dengan 1.
