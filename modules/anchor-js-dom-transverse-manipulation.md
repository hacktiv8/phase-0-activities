#Manipulasi DOM Sederhana dengan DOM Transversing di JavaScript

Setelah mengetahui tentang DOM selection dan manipulation serta DOM transversing, kita akan mencoba memanipulasi DOM kembali, tapi memanfaatkan penjelajahan DOM berdasarkan hubungan parent-child.

## Objectives

- Mengetahui Cara Menjelajah DOM
- Mengetahui Cara Memanipulasi DOM yang Dijelajahi

## Directions

- Buatlah suatu halaman HTML seperti berikut:

**index.html**
```html
<html>
  <head>
    <title>Tugas Anchor DOM!</title>
  </head>
  <body>
    <div id="eldest-parent">
      <div>
        Saya Adalah Keturunan Pertama
      </div>
      <div>
        <div>
          <div>Saya adalah Generasi Termuda, yang paling Tua</div>
          <div id="a-child"></div>
          <div>Saya adalah Generasi Termuda, yang Paling Muda</div>
        </div>
      </div>
      <div>
        Saya adalah Generasi yang Cukup Tua
      </div>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

- Buatlah sebuah **script.js** yang berada relatif di sebelah index.html. Dengan memanfaatkan `children`, `parentNode`, `nextElementSibling`, `previousElementSibling`, dan `innerHTML()`, buat perubahan berikut di file **script.js** untuk memanipulasi halaman HTML kita dan mengubah nilai berikut dengan mengakses `<div>` yang sesuai:

  - `Saya Adalah Keturunan Pertama` menjadi `Diakses Melalui Eldest Parent`
  - `Saya adalah Generasi Termuda, yang paling Tua` menjadi `Diakses Melalui a Child`
  - `Saya adalah Generasi Termuda, yang Paling Muda` menjadi `Diakses Melalui a Child`
  - `Saya adalah Generasi yang Cukup Tua` menjadi `Diakses Melalui a Child`
