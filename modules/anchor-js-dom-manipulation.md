#Manipulasi DOM Sederhana dengan JavaScript

Setelah mengetahui tentang DOM selection dan manipulation, kita akan coba berlatih tentang ini.

## Objectives

- Mengerti Tentang DOM
- Mengetahui Cara Menseleksi DOM
- Mengetahui Cara Memanipulasi DOM

## Directions

- Buatlah suatu halaman HTML seperti berikut:

**index.html**
```html
<html>
  <head>
    <title>Tugas Anchor DOM!</title>
  </head>
  <body>
    <div id="container">
      <h1 id="fill-me"></h1>
      <p class="change-all-of-me"></p>
      <p class="change-all-of-me"></p>
      <p class="change-all-of-me"></p>
      <p class="change-all-of-me"></p>
      <h2>Change the Inside of H2!</h2>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

- Buatlah sebuah **script.js** yang berada relatif di sebelah index.html. Dengan memanfaatkan `getElementById()`, `getElementsByClassName()`, `getElementsByTagName()`, `innerHTML()`, dan teknik looping, buat perubahan berikut di file **script.js** untuk memanipulasi halaman HTML kita:

  - `<h1 id="fill-me"></h1>` menjadi `<h1 id="fill-me">HALO!</h1>`
  - `<p className="change-all-of-me"></p>` menjadi `<p className="change-all-of-me">HALO JUGA!</p>`
  - `<h2>Change the Inside of H2!</h2>` menjadi `<h2>Apa Kabar!</h2>`
