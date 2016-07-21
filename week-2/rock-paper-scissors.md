# Create a Local Rock, Paper, Scissors Game

## Objectives

Membuat permainan suit lokal yang mengumpamakan jempol, telunjuk, dan kelingking sebagai aksi dari pemain. Jempol dapat mengalahkan telunjuk, telunjuk dapat mengalahkan kelingking, kelingking dapat mengalahkan jempol.

- ▢ Membuat fungsi dengan JavaScript `function`.
- ▢ Menggunakan operator perbandingan.
- ▢ Memungkinkan pengguna menentukan aksi.
- ▢ Memungkinkan lawan yaitu komputer menentukan aksi juga dengan acak (random).

## Directions

Bukalah Dev Tools, JSBin, atau CodePen bahkan text/code editor untuk mengedit HTML dan JavaScript terlebih dahulu.

### 1. Buatlah fungsi pilihan aksi pengguna

Pilihan aksi akan menanyakan "Jempol / Telunjuk / Kelingking?". Lalu jika pengguna menulis "Telunjuk" maka dicetak "telunjuk" pada console. Kita dapat memanggil fungsi aksi tersebut seperti berikut, yang akan disimpan dalam sebuah variabel.

```javascript
var pengguna = pilihanPengguna() // pengguna mengisi pilihan
// misalnya "telunjuk"
```

### 2. Buatlah fungsi acak yang akan digunakan otomatis oleh lawan

Fungsi acak akan mencetak antara "jempol" / "telunjuk" / "kelingking". Fungsi tersebut akan dipanggil seperti berikut, yang akan disimpan dalam sebuah variabel juga. Akan menghasilkan string "jempol" jika nilanya antara 0-0.33, string "telunjuk" jika nilainya antara 0.34-0.66, string "kelingking" jika nilainya antara 0.67-1. Gunakan percabangan if/else.

```javascript
var lawan = pilihanLawan() // lawan mengacak angka antara 0 hingga 1
// lalu menghasilkan string misalnya "kelingking"
```

### 3. Buatlah fungsi bertarung yang akan membandingkan pilihan pengguna dan lawan. Pemenang ditentukan sesuai aturan suit lokal, gunakan percabangan if/else ataupun switch/case. Lalu nama pemenang akan ditampilkan di akhir.

```javascript
bertarung(pengguna, lawan)
// menghasilkan string "Pemenangnya adalah: Pengguna" atau "Pemenangnya adalah: Komputer"
```
