# Animation Using CSS and JS

## Objectives

Tahukah kamu, bahwa kita bisa membuat animasi sederhana dengan CSS dan HTML? Ada sebuah sintaks CSS yang dinamakan `pseudo-class` dan juga `transition` yang bisa kamu manfaatkan untuk membuat efek "delay" pada saat sebuah element HTML mengalami perubahan style di CSS. Lalu, dengan memanfaatkan JS, kita bisa mengubah style CSS tersebut dengan dinamis!

**DOM**

- ▢ Memahami CSS Pseudo-class Selector
- ▢ Memahami CSS transition
- ▢ Memahami JS SetTimeout function

## Learnings

### 1. CSS Pseudo-class Selector

Seringkali saat kita melihat website-website, banyak efek yang terlihat pada saat kita meng-hover (meletakkan mouse pointer diatas) sebuah element. Pasti setelah mempelajari JS DOM event, ini bisa di solve dengan addEventListener dan menambahkan action type berupa mouseenter atau mouseover. Namun, dengan CSS pun sekarang kita bisa melakukannya!

**contoh-pseudoclass.html**
```html
<html>
  <head>
    <link href="contoh-pseudoclass-style.css" ref="stylesheet" />
  </head>
  <body>
    <div id="saya-bisa-di-hover">Hover Saya!</div>
  </body>
</html>
```

**contoh-pseudoclass-style.css**
```css
#saya-bisa-di-hover {
  height: 100px;
  width: 100px;
  background: black;
}

#saya-bisa-di-hover:hover {
  background: green;
}
```

Contoh di atas akan menunjukkan saat div hover saya di hover, warna nya akan berubah dari hitam menjadi hijau, dengan menambahkan css style baru dan memberikan `:hover`. Gambarannya dari apa yang terjadi disini adalah kita punya dua style css: #saya-bisa-di-hover dan #saya-bisa-di-hover:hover. Ini adalah dua style berbeda, dimana menunjukkan style mana yang akan digunakan saat element HTML memiliki state/status tertentu. Secara default, kotak akan menggunakan style #saya-bisa-di-hover. Namun, saat di hover (mengalami perubahan state/status), style akan terupdate menggunakan :hover.

### 2. CSS Transition

Dari contoh sebelumnya, kita bisa membuat efek berubah style pada kotak saat di hover. Namun tidak hannya sampai sana, kita juga bisa membuat animasi perubahan warna tersebut menggunakan css. Caranya adalah menambahkan sintaks `transition: [x]s` dengan x adalah berapa lama transisi/delay diberikan. Contoh penggunaan transisi, kita gunakan contoh sebelumnya.

**contoh-transition.html**
```html
<html>
  <head>
    <link href="contoh-transition-style.css" ref="stylesheet" />
  </head>
  <body>
    <div id="saya-bisa-di-hover-dengan-animasi">Hover Saya!</div>
  </body>
</html>
```

**contoh-transition-style.css**
```css
#saya-bisa-di-hover-dengan-animasi {
  height: 100px;
  width: 100px;
  background: black;
  transition: 0.5s;
}

#saya-bisa-di-hover-dengan-animasi:hover {
  background: green;
  transition: 0.5s;
}
```

### 3. Contoh Penggunaan setTimeout di JavaScript

Terkadang kita membutuhkan sebuah instruksi code yang ingin dijalankan setelah waktu tertentu. Disini, kita dapat menggunakan fungsi `setTimeout()` di JavaScript.

Function `setTimeout()` mengambil dua parameter, dimana parameter pertama merupakan fungsi yang akan dijalankan pada saat waktu telah mencapai yang ditentukan, dan parameter kedua merupakan berapa lama fungsi di dalam setTimeout tersebut akan dijalankan.

Contoh Penggunaan `setTimeout()`
```javascript
setTimeout(function() {
  alert('HALO!');
}, 2000);
// Potongan kode ini akan meng-alert HALO di HTML kita setelah 2 detik berlalu.
```

### 4. Menggabungkan Transition dan setTimeout di JavaScript

Terakhir, untuk mencoba menggabungkan yang telah kita pelajari sebelumnya, kita akan lihat contoh di bawah ini:

**contoh-gabungan.html**
```html
<html>
  <head>
    <title>Contoh Gabungan Simple</title>
  </head>
  <body>
    <div id="black-box" style="transition: 0.5s; width: 100px; height: 100px; background: black;"></div>
    <button id="box-jump">Loncat!</button>
    <script src="contoh-gabungan-style.js"></script>
  </body>
</html>
```

**contoh-gabungan-style.js**
```js
var blackBox = document.getElementById('black-box');
var jumpBox = document.getElementById('box-jump');
jumpBox.addEventListener('click', function() {
  blackBox.style.background = 'green';
  blackBox.style.width = '400px';
  setTimeout(function() {
    blackBox.style.background = 'black';
    blackBox.style.width = '100px';
  }, 500);
});
```
