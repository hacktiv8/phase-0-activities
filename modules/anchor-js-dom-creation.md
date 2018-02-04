# Menyusun Halaman HTML Dinamis di JavaScript

Setelah mengetahui tentang DOM selection dan manipulation serta DOM transversing, kita akan mencoba memanipulasi DOM kembali, tapi memanfaatkan penjelajahan DOM berdasarkan hubungan parent-child.

## Objectives

- Mengetahui Cara create DOM
- Mereview Cara menggunakan DOM Event

## Directions

- Buatlah suatu halaman HTML yang dinamis dibuat dari HTML "kosong" seperti berikut:

**index.html (Gunakan file index.html ini)**
```html
<html>
  <head>
    <title>Tugas Anchor DOM!</title>
  </head>
  <body>
    <div id="main">
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

Dan dengan teknik `createElement`, susunlah dengan dinamis menggunakan **script.js** untuk menjadikan HTML menjadi seperti di bawah ini:

**HASIL AKHIR**
```html
<html>
  <head>
    <title>Tugas Anchor DOM!</title>
  </head>
  <body>
    <div id="main">
      <div id="content">
        <div class="content-post">
          <h1>Judul Post</h1>
          <span>Published on 12 May 2016</span>
          <p>
            Lorem Ipsum Dolor Sit Amet
          </p>
          <button class="share-post-btn">Share this Post</button>
        </div>
        <div class="content-post">
          <h1>Judul Post 2</h1>
          <span>Published on 13 May 2016</span>
          <p>
            Lorem Ipsum Dolor Sit Amet
          </p>
          <button class="share-post-btn">Share this Post</button>
        </div>
      </div>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

Note: `<button class="share-post-btn">` apabila di click, harus meng-alert 'You have shared this post'!

- Buatlah sebuah **script.js** yang berada relatif di sebelah index.html. Dengan memanfaatkan (dan tidak terbatas pada) `createElement()`, `createAttribute()`, `setAttribute()`, `createTextNode()`, `addEventListener()`, `alert()`, dan `appendChild()`, buat perubahan berikut di file **script.js** untuk memanipulasi halaman HTML dan membuat layout seperti contoh hasil akhir di atas!
