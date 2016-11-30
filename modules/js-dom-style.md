# DOM Style

## Objectives

Dalam web kita, mungkin kita ingin mengubah style/gaya/desain dari web kita berdasarkan interaksi user. CSS hanya mampu membuat style yang pada awal di-render, tidak berdasarkan interaksi dari web.

**DOM**

- ▢ Memahami DOM Style Manipulation

## Learnings

### 1. DOM Style Manipulation

DOM Style Manipulation sangatlah sederhana. Prinsipnya adalah pada saat kita sudah menguasai CSS, kita dapat langsung mengerti cara kerja dari DOM style. Format atau bentuk penulisan dalam DOM style adalah `[namaElement].style.[sintaksCSS]`.

Contoh paling sederhana adalah warna teks. Contoh dibawah akan menggambarkan bagaimana mengubah warna teks menggunakan JavaScript.

### 2. Contoh Sederhana Mengganti Warna

**Sample-1.html**
```html
<html>
  <head>
    <title>Super Simple Web Page</title>
  </head>
  <body>
    <div id="main">
      <h1 id="heading-1">Heading Sample 1</h1> <!-- Secara default, h1 berwarna hitam -->
    </div>
    <script src="change-color.js"></script>
  </body>
</html>
```

**change-color.js**
```javascript
var heading1 = document.getElementById('heading-1');
heading1.style.color = '#D91E18'; // mengubah warna heading1 menjadi merah
```

### 3. Contoh Sederhana Menghilangkan Tulisan Dengan Klik

**Sample-2.html**
```html
<html>
  <head>
    <title>Super Simple Web Page</title>
  </head>
  <body>
    <div id="main">
      <h1 id="heading-1">Akan Hilang Jika Button Di Klik</h1>
      <button id="remove-heading-1">Klik Saya untuk Menghilangkan Heading-1</button>
    </div>
    <script src="change-display.js"></script>
  </body>
</html>
```

**change-display.js**
```javascript
var heading1 = document.getElementById('heading-1');
var removeHeading1Btn = document.getElementById('remove-heading-1');
removeHeading1Btn.addEventListener('click', function() {
  heading1.style.display = 'none'; // Hilangkan <h1> dengan css
});
```

### 3. Contoh Sederhana Menghilangkan/Memunculkan Tulisan Dengan Klik

**Sample-3.html**
```html
<html>
  <head>
    <title>Super Simple Web Page</title>
  </head>
  <body>
    <div id="main">
      <h1 id="heading-1">Akan Hilang Jika Button Di Klik, dan Muncul jika di Klik Lagi</h1>
      <button id="remove-heading-1">Klik Saya</button>
    </div>
    <script src="change-display-2.js"></script>
  </body>
</html>
```

**change-display-2.js**
```javascript
var heading1 = document.getElementById('heading-1');
var removeHeading1Btn = document.getElementById('remove-heading-1');
removeHeading1Btn.addEventListener('click', function() {
  if(heading1.style.display === 'block') { // Jika saat ini <h1> muncul
    heading1.style.display = 'none'; // Hilangkan <h1> dengan css
  }
  else if(heading1.style.display === 'none') { // Jika saat ini <h1> muncul
    heading1.style.display = 'block'; // Munculkan <h1> dengan css
  }
  else if(heading1.style.display === '') { // display = '' sama dengan display = 'block'
    heading1.style.display = 'none'; // Hilangkan <h1> dengan css
  }
});
```
