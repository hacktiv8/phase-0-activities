# Website Asset Compression

## Objectives

Meningkatkan kecepatan *loading* aplikasi web dengan memperhatikan aset-aset seperti gambar, css, javascript dan file statik lainnya. Semakin besar ukuran file-file statik diatas, semakin lambat pula web yang kamu kembangkan. Dan semakin banyak pula pengguna yang tidak sabar untuk segera meninggalkan web kamu karena tidak sabar menunggu web kamu untuk *loading*.

Karena itu mempercepat aplikasi web kita adalah hal yang esensial.

## Directions

### 0. Mengukur Performa

Sebelum kita membicarakan bagaimana cara mempercepat aplikasi web yang kita
kembangkan, hal pertama yang harus kita sadari adalah bagaimana cara
mengukur performa dari aplikasi kita. Bagaimana kita tahu aplikasi kita
cepat atau lola a.k.a loading lama? :)

Dan untuk mengukur performa, silakan menuju ke [materi sebelumnya tentang
kecepatan website](./website-speed.md).

### 1. Memahami dan mengoptimalisasi HTTP Request

Penting untuk memperhatikan jumlah keseluruhan *HTTP Request* pada sebuah web. Bahkan ketika tidak ada data apapun yang dikirim, misalnya halaman *under construction* atau halaman **404**, *HTTP request* tetap butuh waktu untuk tampil dihadapan pengguna.

Ditambah lagi browser seperti chrome, firefox dan lainnya memiliki
keterbatasan dalam membuat koneksi secara paralel sehingga proses *loading*
aset dan request lainnya pun jadi terbatas. Sehingga kita harus sebisa
mungkin mengurangi jumlah HTTP request untuk meningkatkan performa.

Baca [artikel berikut](http://blog.hubspot.com/marketing/reduce-http-requests) untuk mengetahui bagaimana mengurangi *request* dari dan ke web kita.

### 2. Optimalisasi ukuran gambar

Gambar atau *image* hampir selalu menjadi kontributor terbesar dalam menghabiskan bandwidth. Aplikasi web yang umum pasti memiliki HTML, CSS dan JavaScript, akan tetapi gambar seperti foto atau *artwork* biasanya lima atau sepuluh kali lebih besar ukurannya.

Saat proses development aplikasi web sangat penting untuk tetap secara hati-hati memilih gambar yang harus ditampilkan dan dengan format, kompresi dan resolusi yang bagaimana agar gambar tetap optimal tanpa mengorbankan kecepatan *loading*.

Berikut beberapa langkah yang dapat ditempuh untuk mengoptimalkan gambar
dalam sebuah aplikasi web:

* Sebaiknya gunakan format SVG. Format gambar SVG relatif lebih kecil dalam
  ukuran dibandingkan format lainnya. Kita sudah mempelajari tentang [SVG
  ini di topik minggu ke-tiga](./svg.md).
* Ubah ukuran (*resize*) dan lakukan kompresi gambar. Gambar yang digunakan
  sebaiknya sudah di *resize* dan di kompresi terlebih dahulu.

### 3. Optimalisasi CSS

Ada beberapa pedoman dan teknik untuk mengoptimalkan CSS. Yang paling umum
dan ampuh digunakan adalah dua teknik berikut:

1. [Hindari penggunaan `@import`](https://developers.google.com/speed/pagespeed/service/FlattenCssImports) di dalam CSS. Karena penggunaan `@import` akan menyebabkan browser melakukan beberapa request ke server.
2. Gunakan *service hosting* yang memiliki spesialisasi dan kecepatan yang lebih baik, terutama untuk penggunaan *custom font*. Service seperti ini contohnya [Google fonts](https://fonts.google.com/). Dengan menggunakan [Google fonts](https://fonts.google.com/), kita mendapatkan kecepatan dan kehandalan dari Google dalam konteks penggunaan dan *loading custom font*. Alternatif lainnya, seperti [TypeKit](https://typekit.com/).

TODO

- [ ] Mampu mengukur kecepatan dari sebuah website menggunakan DevTools
- [ ] Mampu 
- [ ]

## References

-
