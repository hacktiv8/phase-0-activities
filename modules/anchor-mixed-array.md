# Menggunakan Built-in Function pada Array

Array pada JavaScript memiliki sekumpulan *built-in function* yang digunakan untuk mempermudah developer untuk mengolah data di dalamnya. Beberapa fungsi yang sering digunakan antara lain `join`, `split`, `slice`, `splice`, dan `sort`. Kerjakanlah tantangan ini untuk memperkuat pengertian kamu tentang *built-in function* tersebut.

## Objectives

- Mengerti Kegunaan dari *Built-in Function* yang dimiliki Array
- Mampu Menggunakan *Built-in Function* yang dimiliki Array
- Memperkuat Pemahaman Terhadap Array Multidimensi

## Directions

```javascript
//contoh output
[ 
    [ '0001', '0002', '0003', '0004' ],   
    [ 'Roman Alamsyah', 'Dika Sembiring', 'Winona', 'Bintang Senjaya' ],
    [ 'Bandar Lampung', 'Medan', 'Ambon', 'Martapura' ],     
    [ '21/05/1989', '10/10/1992', '25/12/1965', '6/4/1970' ],
    [ 'Membaca', 'Bermain Gitar', 'Memasak', 'Berkebun' ]
]  
```

Pada tantangan [sebelumnya](modules/anchor-loop-array.md) kamu sudah mengerjakan sebuah fungsi yang menghasilkan keluaran kurang lebih seperti yang di atas. Tantangan kali ini adalah untuk mengolah lebih lanjut data keluaran tersebut. Untuk mengerjakan tantangan kali ini, kamu bebas untuk membuat fungsi baru atau tidak.

- Simpan keluaran dari fungsi `dataHandling` ke dalam sebuah variabel.
- Gunakan fungsi `splice` untuk memodifikasi variabel tersebut agar menjadi seperti array dibawah.

```javascript
[
    [ '0001', '0002', '0003', '0005', '0006', '0007' ],
    [ 'Roman Alamsyah', 'Dika Sembiring', 'Winona', 'I Made Sanadhi Sutandi', 'Nufus', 'Sani' ],
    [ 'Bandar Lampung', 'Medan', 'Ambon', 'Denpasar', 'Muaro Bungo', 'Jakarta' ],
    [ '21/05/1989', '10/10/1992', '25/12/1965', '13/9/1994', '10/8/1994', '19/7/1994' ],
    [ 'Membaca', 'Bermain Gitar', 'Memasak', 'Belajar', 'Melukis', 'Touring' ]
]

```

- Berdasarkan array yang berisikan tanggal lahir, ambil angka bulan dan buat sebuah array baru yang berisikan nama bulan sesuai dengan angka tersebut.
    - Gunakan `split` untuk mengambil angka bulan.
    - Gunakan [`push`](http://www.w3schools.com/jsref/jsref_push.asp) untuk menyimpan nama bulan pada array baru.
    - Buat sebuah array berisikan nama-nama bulan masehi untuk membantu kamu mengerjakan tantangan ini.
    - Format tanggal pada data adalah `dd-mm-YYYY`

- Tuliskan data-data yang sudah diolah seperti contoh dibawah:
    - Urutkan semua data sebelum ditampikan. Gunakan `sort`
    - Khusus daftar nama, tampilkan 15 karakter pertama saja. Gunakan `slice`.
    - Gunakan `join` untuk menampilkan data yang tidak berbentuk list

```
Daftar Nama
1 - Dika Sembiring
2 - I Made Sanadhi
3 - Nufus
4 - Roman Alamsyah
5 - Sani
6 - Winona

Semua Tempat Lahir:
Ambon,Bandar Lampung,Denpasar,Jakarta,Medan,Muaro Bungo

Semua Bulan Kelahiran:
Agustus,Desember,Juli,Mei,Oktober,September

Semua Hobi:
Belajar,Bermain Gitar,Melukis,Memasak,Membaca,Touring 
```

### Hint

- Gunakan `console.log()` untuk mengeluarkan isi array dan *debugging* 
- Kebenaran solusi tidak hanya dilihat dari hasil akhir melainkan program yang dibuat.