# Gallery Slide

## Objectives

Dengan pengubahan properti sederhana, kita bisa membuat sebuah halaman yang interaktif, misalnya slide galeri yang terdapat tombol sebelum dan selanjutnya.

- ▢ Memahami penggunaan DOM, event object, dan scope.
- ▢ Berkreatifitas sesuka hati.

## Directions

![Slide Galeri](assets/gallery-slide.gif)

(0) Bukalah Dev Tools, JSBin, atau CodePen bahkan text/code editor untuk mengedit HTML dan JavaScript terlebih dahulu.

(1) Buatlah elemen yang akan menjadi tombol `sebelum`/`previous` dan `selanjutnya`/`next`.

(2) Siapkan beberapa gambar JPG. Kami rekomendasikan 3 gambar saja agar mudah mengelolanya. Buat elemen image di antara kedua tombol tadi, sertakan sumber gambar default pada elemen image tersebut.

(3) Siapkan array yang berisi string nama beberapa gambar yang ada.

(4) Buat variabel global untuk nama image yang sekarang (misalnya `currentImage`) dan indeksnya (misalnya `currentIndex`), serta variabel yang akan menyimpan indeks `previous` dan `next`

(5) Buat function yang dapat mengambil value image sekarang dan indeksnya, kedua value tersebut disimpan ke dalam variabel global. Gunakan method berikut jika kesulitan untuk mengambil value property `src` dari `img` tanpa embel-embel path-nya.

```javascript
.src.split("/").pop();
```

(6) Buat dua function yang akan dipanggil ketika terdapat event tombol previous dan next diklik. Masing-masing akan mengetahui value image sekarang dan indeksnya, kemudian tergantung dari indeksnya, akan mengganti `src` gambar, sesuai arah urutannya.

(7) Untuk menjaga kesederhanaan, jika indeks sedang berada di ujung awal atau akhir, tidak perlu mengganti `src` gambar. Bisa saja memberi tahu saat hal tersebut terjadi.

(8) Cek kembali bahwa fungsi sudah terpasang pada event listener kedua button yang akan kita pakai.
