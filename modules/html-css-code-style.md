# Learn Coding Style Guide

## Objectives

Dalam menulis code yang profesional, diperlukan berbagai aturan atau standar yang sangat dianjurkan untuk diikuti. Selain code kita bisa lebih rapi, mudah dibaca, dan komprehensif; tentunya kita juga akan lebih produktif.

## Directions

### 1. Memahami cara penulisan HTML dan CSS yang baik

- ▢ Pahami berbagai aturan penulisan HTML dan CSS di ini: [Writing Your Best Code](http://learn.shayhowe.com/html-css/writing-your-best-code)
- ▢ Cek berbagai pedoman penulisan code berikut:
  - [Code Guide by @mdo](http://codeguide.co)
  - [CSS Style Guides, on CSS Tricks](https://css-tricks.com/css-style-guides)
  - [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.xml)

### 2. Memperhatikan meta data lebih lanjut

Memberi data dan informasi yang berguna bagi browser bahkan juga pengguna adalah kegunaan meta data. Meta data dapat berupa judul website, deskripsi tentang website, kata kunci terkait, serta gambar icon.

Modern ini terdapat meta data yang sangat bermanfaat bagi kita dan pengguna agar lebih memuat informasi yang jelas bagi platform media sosial serta search engine, seperti alamat, nomor telepon, foto-foto, dan lainnya. Untuk itu perlu disertakan tag meta data Facebook OpenGraph, Twitter Card, dan Google JSON-LD; namun akan kita bahas lain waktu saja.

Contoh umum menggunakan meta data `title`, `description`, `author`, `icon`.

```html
<title>Hacktiv8 - Menjadi Full Stack Web Developer</title>
<meta name="description" content="Hacktiv8 adalah sebuah pelatihan coding fulltime di Jakarta yang membantu pemula untuk menjadi fullstack developer dalam 12 minggu.">
<meta name="keywords" content="hacktiv8, coding, bootcamp, javascript, web, developer">
<meta name="author" content="Hacktiv8 Team">
<link rel="icon" href="//favicon.ico" type="image/x-icon"/>
```

### 3. Merapikan penulisan code HTML dan CSS sebelumnya

Update berbagai file HTML dan CSS yang sudah ada:

- ▢ Struktur dokumen HTML harus lengkap.
- ▢ Penulisan sintaks diorganisir dengan rapi.
  - Perhatikan indentasi ataupun spacing.
  - Sebaiknya quote yang digunakan semuanya adalah double quote.
  - Gunakan lowercase untuk penamaan element, attributes, dan values.
- ▢ Update penamaan `id` dan `class` yang belum rapi. `id` tidak boleh ada yang redundant.
- ▢ Pindahkan attribute `style` dari tag HTML, jadikan semua styling lewat `id` atau `class`.
- ▢ Gunakan element secara semantic, tidak menyalahi aturan.
- ▢ Gunakan attribute `alt` pada gambar.
- ▢ Berilah komentar pada berbagai segmen element HTML dan rule CSS.
- ▢ Aturan CSS ditulis secara multiline.

Harap menyadari cara dan hasil penulisan code kamu. Pada berbagai kegiatan berikutnya, dianjurkan untuk udah bisa mengimplementasikannya secara alami.

### 4. Kirim berbagai perubahan yang ada ke website kamu

- ▢ Add, commit, dan push perubahan ke GitHub.
  - `git add -A`
  - `git commit -m "Tidy up my code"`
  - `git push`
- ▢ Cek halaman dan source code kamu yang sudah lebih rapi.
- ▢ Share hasil kamu di Slack.

## References

- [The Essential Meta Tags for Social Media, on CSS Tricks](https://css-tricks.com/essential-meta-tags-social-media)
