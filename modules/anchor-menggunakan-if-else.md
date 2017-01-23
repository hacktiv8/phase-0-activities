# Menggunakan If Else 

## Objectives

* Mengerti Cara Menggunakan `If-Else`
* Mengerti Logika `If-Else`
* Mengerti Cara Menggunakan Operator Evaluasi `===`, `!==`

## Directions

Kamu diminta untuk memprogram suatu game sederhana, Proxytia namanya. Untuk memulai game itu diperlukan 2 variabel (untuk sekarang), yaitu `nama` dan  `peran`. Variabel `nama` harus memiliki isi data, bila kosong pemain akan diberikan peringatan. Terdapat 3 `peran` berbeda yaitu **Ksatria**, **Tabib**, dan **Penyihir**. Tugas Anda adalah untuk membuat program yang mengecek isi variabel `nama` dan `peran` serta mengeluarkan respon sesuai isi variabel tersebut.

### Hints

* Variabel tetap di-input secara manual.
* Variabel `nama` dan `peran` dapat diisi apa saja.
* Nama tidak perlu dicek sama persis seperti contoh input/output
* Buat 2 `If-Else` berbeda masing-masing untuk mengecek `nama` dan `peran`

### Input

```javascript
//[NAMA] dapat berupa string apa saja
//Contoh input 1
nama = ' '
peran = ' '
//Contoh input 2
nama = [NAMA]
peran = 'Ksatria'
//Contoh input 3
nama = [NAMA]
peran = 'Tabib'
//Contoh input 4
nama = [NAMA]
peran = 'Penyihir'
```

### Output

```javascript
//Output untuk Input 1
"Nama tidak boleh kosong"
"Pilih peranmu untuk memulai game"
//Output untuk Input 2
"Selamat datang di Dunia Proxytia, [NAMA]"
"Halo Ksatria [NAMA], kamu dapat menyerang dengan senjatamu!"
//Output untuk Input 3
"Selamat datang di Dunia Proxytia, [NAMA]"
"Halo Tabib [NAMA], kamu akan membantu temanmu yang terluka."
//Output untuk Input 4
"Selamat datang di Dunia Proxytia, [NAMA]"
"Halo Penyihir [NAMA], ciptakan keajaiban yang membantu kemenanganmu!"
```
