# Get Advised on Testing and Performance

## Objectives

Dalam pembuatan aplikasi yang baik, kita akan perlu memperhatikan tahap pengetesan (testing) dan pengukuran performa/kecepatan. Hal ini berpengaruh pada waktu dan keefektifan pekerjaan kita, serta hasil jadi aplikasi yang akan dipakai oleh pengguna. Dengen pengetahuan akan metode berikut, manajemen proyek dan aplikasi kita akan lebih mudah dikelola, aman, dan baik.

## Directions

### Mengetahui Code Testing

Secara tersirat ketika kita membuat website ataupun aplikasi, pastinya setelah itu kita melakukan percobaan apakah hasil jadinya sesuai ekspektasi kita. Percobaan atau pengetesan ini jika secara profesional, memerlukan teknik yang termasuk proses yang fokus menjalankan program dengan tujuan menemukan error atau kesalahan. Sehingga idealnya, tahap pengembangan dan testing dilakukan secara terpisah namun tetap berdekatan. Eksekusi atau menjalankan testing juga sebaiknya dispesifikasikan, komponent apa yang akan dievaluasi property dan sifatnya.

**QUnit**

Terdapat berbagai library dan framework untuk melakukan testing. Tapi kali ini kita sebut satu saja. Yaitu [QUnit](https://qunitjs.com) yang dibuat oleh team jQuery, sebuah framework unit testing yang powerful dan mudah digunakan. Berguna untuk mengetes code generic bahkan QUnit itu sendiri.

### Mengetahui Cara Mengetes Performa dan Kecepatan

Berikut berbagai tool gratis yang bisa kita gunakan untuk mengetes performa dan kecepatan kita.

**Website Speed**

[PageSpeed](https://developers.google.com/speed/pagespeed) dan browser extension-nya [PageSpeed Insights](https://chrome.google.com/webstore/detail/pagespeed-insights-with-p/lanlbpjbalfkflkhegagflkgcfklnbnh), berguna untuk menganalisis performa website kita dan optimisasi berdasarkan best practice yang dianjurkan.
Pengukurannya berdasarkan mobile dan desktop device, jadi kita bisa tahu perbandingan kemampuan website kita di lingkungan yang berbeda. Setelah mendapatkan report, terdapat berbagai penjelasan dan rekomendasi yang bisa kita pahami dan gunakan.

[WebPagetest](http://webpagetest.org) adalah pengetes performa dan optimisasi website juga. Kita bisa melihat hasil test yang dilakukan dari berbagai lokasi di dunia menggunakan browser yang nyata. Banyak fitur lebih yang bermanfaat untuk mencek pengaruh konten dan multimedia terhadap website kita.

[Pingdom Website Speed Test](http://tools.pingdom.com/fpt)
memungkinkan kita untuk mengetes load time dari halaman, lalu menganalisanya serta menemukan ganggunan/bottleneck yang ada. Dengan ini berbagai pengaruh dari konten juga bisa diukur.

[GTmetrix](https://gtmetrix.com) menganalisis kecepatan website dan performa agar bisa optimal. Insight yang didapat juga menyediakan rekomendasi yang bisa kita lakukan untuk optimisasi.

Terdapat alternatif lainnya seperti [Varvy Pagespeed](https://varvy.com/pagespeed).

**Kompresi Aset (Assets Compression)**

Berbagai aset penting seputar gambar atau foto mayoritas berformat JPG dan PNG. Aset-aset ini biasanya berukuran besar, atau medium bahkan, yang mana bisa memperlambat load time dari website kita. Untuk itu, direkomendasikan untuk mengkompres ukurannya agar bisa meningkatkan kecepatan website kita. Ingat bahwah al ini mengecilkan ukuran byte namun tidak mengubah ukuran piksel. Misalnya file `contoh.jpg` berukuran 1 MB dapat dikompresikan menjadi 500 KB saja.

Ada beberapa tools untuk melakukan ini antara lain:

- [JPEGmini](http://jpegmini.com)
- [PNG Crush](http://pngcrush.com)
- [ImageAlpha: Image minifier (like JPEG with transparency!)](https://pngmini.com)
- [Trimage (lossless) image compressor](https://trimage.org)
