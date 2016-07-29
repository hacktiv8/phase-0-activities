# Create a Simple Gallery Slide

## Objectives

- ▢ Memahami penggunaan DOM, event object, dan scope.
- ▢ Berkreatifitas sesuka hati.

Dengan pengubahan properti sederhana, kita bisa membuat sebuah halaman yang interaktif, misalnya slide galeri yang terdapat tombol sebelum dan selanjutnya.

Contohnya seperti ini:

![Slide Galeri](assets/gallery-slide.gif)

## Directions

Bukalah Dev Tools, JSBin, atau CodePen bahkan text/code editor untuk mengedit HTML dan JavaScript terlebih dahulu.

### 1. Buat elemen tombol

Buatlah elemen yang akan menjadi tombol `sebelum`/`previous` dan `selanjutnya`/`next`.

### 2. Siapkan gambar

Gambar berupa beberapa gambar JPG. Kami rekomendasikan 3 gambar saja agar mudah mengelolanya. Buat elemen image terletak di antara kedua tombol tadi, sertakan sumber gambar default pada elemen image tersebut.

### 3. Siapkan array nama gambar

Array berisi string nama beberapa gambar yang ada.

### 4. Buat beberapa variabel global

Buat variabel global untuk nama image yang sekarang (misalnya `currentImage`) dan indeksnya (misalnya `currentIndex`), serta variabel yang akan menyimpan indeks `previous` dan `next`.

### 5. Buat function untuk mendapatkan value image dan indeks

Function akan dapat mengambil value image sekarang dan indeksnya, kedua value tersebut disimpan ke dalam variabel global.

Gunakan method berikut jika kesulitan untuk mengambil value property `src` dari `img` tanpa embel-embel path-nya.

```javascript
.src.split("/").pop();
```

### 6. Beri fungsi agar tombol previous dan next dapat bekerja

Buat dua function yang akan dipanggil ketika terdapat event tombol previous dan next diklik. Masing-masing akan mengetahui value image sekarang dan indeksnya, kemudian tergantung dari indeksnya, akan mengganti `src` gambar, sesuai arah urutannya.

### 7. Kasih tahu jika indeks sedang di ujung

Untuk menjaga kesederhanaan, jika indeks sedang berada di ujung awal atau akhir, tidak perlu mengganti `src` gambar. Bisa saja cukup memberi tahu saat hal tersebut terjadi.

### 8. Cek fungsionalitas program

Cek kembali bahwa fungsi sudah terpasang pada event listener kedua button yang akan kita pakai.

## Submissions

- ▢ Buatlah aplikasi tersebut dalam halaman `gallery-slide.html` pada repo website kamu.
- ▢ Commit dan push file tersebut ke GitHub.
- ▢ Share hasil kamu di Slack.
