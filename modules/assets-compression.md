# Website Asset Compression

## Objectives

Meningkatkan kecepatan *loading* aplikasi web dengan memperhatikan aset-aset seperti gambar, CSS, JavaScript, dan file statiC lainnya. Semakin besar ukuran file-file statiC diatas, semakin lambat pula web yang kamu kembangkan. Dan semakin banyak pula pengguna yang tidak sabar untuk segera meninggalkan web kamu karena tidak sabar menunggu web kamu untuk *loading*. Karena itu mempercepat aplikasi web kita adalah hal yang esensial.

- ▢ Mampu mengoptimalkan proses *loading* JavaScript
- ▢ Memahami alasan mengapa kita butuh metode *minifying* dan *combining*.

## Directions

### 0. Mengukur Performa

Sebelum kita membicarakan bagaimana cara mempercepat aplikasi web yang kita kembangkan, hal pertama yang harus kita sadari adalah bagaimana cara mengukur performa dari aplikasi kita. Bagaimana kita tahu aplikasi kita cepat atau lola a.k.a loading lama? :)

Terkait untuk mengukur performa, silakan menuju ke [materi sebelumnya tentang
kecepatan website](./website-speed.md).

### 1. Optimalisasi ukuran gambar

Gambar atau *image* hampir selalu menjadi kontributor terbesar dalam menghabiskan bandwidth. Aplikasi web yang umum pasti memiliki HTML, CSS dan JavaScript, akan tetapi gambar seperti foto atau *artwork* biasanya lima atau sepuluh kali lebih besar ukurannya.

Saat proses development aplikasi web sangat penting untuk tetap secara hati-hati memilih gambar yang harus ditampilkan dan dengan format, kompresi dan resolusi yang bagaimana agar gambar tetap optimal tanpa mengorbankan kecepatan *loading*.

Berikut beberapa langkah yang dapat ditempuh untuk mengoptimalkan gambar dalam sebuah aplikasi web:

* Sebaiknya gunakan format SVG. Format gambar SVG relatif lebih kecil dalam ukuran dibandingkan format lainnya.
* Ubah ukuran (*resize*) dan lakukan kompresi gambar. Gambar yang digunakan sebaiknya sudah di *resize* dan di kompresi terlebih dahulu.

### 2. Optimalisasi JavaScript

Script JavaScript yang kita kombinasikan dengan halaman HTML dapat di-load dibagian bawah dari halaman HTML kita. Apa bedanya dengan me-load dibagian atas? Web browser me-load halaman mulai dari tag paling atas hingga ke paling bawah. Apabila script kita letakkan di bagian atas, maka browser akan me-load script terlebih dahulu sebelum me-load elemen-elemen HTML lainnya.

Hal ini menjadi signifikan di mata pengguna karena disaat browser me-load script, maka halaman masih terlihat halaman kosong. Akibat jangka panjangnya adalah pengguna bingung, dan lebih parah akan segera meninggalkan website kamu.

Sebaliknya, apabila script diletakkan dibagian bawah, maka halaman website akan di load terlebih dahulu baru kemudian menyusul script-script yang kita butuhkan di-load dibagian akhir.

Contoh load JavaScript yang kurang optimal:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title></title>
  <script src="asset/script.js"></script>
</head>
<body>
  <h1>Ini adalah website yang super keren!</h1>
</body>
</html>
```

Dan berikut contoh dengan lebih optimal:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title></title>
</head>
<body>
  <h1>Ini adalah website yang super keren!</h1>
  <script src="asset/script.js"></script>
</body>
</html>
```

### 3. Minify aset

Aset juga dapat di kompresi ukurannya dengan cara *minifying* file CSS dan JavaScript. Metode ini biasanya juga diiringi dengan mengkombinasikan seluruh CSS menjadi satu file saja. Begitu juga dengan JavaScript. Sehingga jumlah HTTP request yang terjadi akan menjadi lebih sedikit.

Beberapa *tools* yang biasa digunakan untuk *minifying* dan *combine* ini adalah sebagai berikut:

* [Google Closure Compiler Service](http://closure-compiler.appspot.com/home)
* [CSS Minifier](http://cssminifier.com)
