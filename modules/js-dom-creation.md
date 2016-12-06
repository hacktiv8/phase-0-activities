# DOM Creation

## Objectives

Dalam aplikasi web, kita tidak terbatas memanfaatkan DOM untuk dimanipulasi atau ditambahkan event-event tertentu. Kita juga dapat membuat DOM baru menggunakan JavaScript. Bahkan, kita dapat membuat sebuah halaman web yang full dengan element HTML namun script HTML kita sangt sedikit, dan hampir seluruhnya di render menggunakan JavaScript. Prinsip inilah yang dilakukan oleh Angular, React, dan teknologi front-end lainnya untuk merender DOM.

**DOM**

- ▢ Memahami DOM Creation
- ▢ Menyusun Layout Web dengan JavaScript

## Learnings

### 1. Mengenal DOM Creation

Kita dapat membuat atau menyusun DOM menggunakan JavaScript, dan membangun DOM tree kita sendiri. DOM tree bisa dibilang sebagai hubungan parent-child antar satu element dengan element lainnya.

Contoh Sederhana HTML
```html
<html>
  <head>
    <title>Super Simple Web Page</title>
  </head>
  <body>
    <div id="main">
      <div id="inside-main">
        <h1>Heading Sample 1</h1>
        <button>Click Me!</button>
      </div>
    </div>
  </body>
</html>
```

Kita akan mencoba membuat halaman isi dari body tersebut dengan dinamis menggunakan JavaScript. Kita akan memulai dengan membuat HTML "kosong" terlebih dahulu.

**js-dom-creation.html**
```html
<html>
  <head>
    <title>Super Simple Web Page - Fresh From the JS</title>
  </head>
  <body>
    <!-- it's empty, just contain a js file -->
    <script src="js-dom-creation-script.js"></script>
  </body>
</html>
```

Selanjutnya, kita akan membuat element HTML di dalam `<body>` satu per satu dengan beberapa sintaks.

**js-dom-creation-script.js (Part 1)**
```javascript
// Pertama, kita seleksi terlebih dahulu <body>
var body = document.body;

// Kemudian, kita buat sebuah element HTML <div> menggunakan createElement
var mainDiv = document.createElement('div');

// Untuk membuat <div id="main">, maka kita harus membuat HTML attribute id
var mainDivAttrId = document.createAttribute('id');

// Untuk memberikan nilai kepada id, maka kita gunakan .value
mainDivAttrId.value = "main";

// id="main" kita sudah siap. Sekarang kita harus menambahkan attribute tersebut ke mainDiv
mainDiv.setAttributeNode(mainDivAttrId);

// mainDiv kita sudah menjadi <div id="main">. Saatnya kita tambahkan ke dalam <body>
// Karena Kita akan meletakkan <div id="main"> di dalam <body>, maka kita gunakan appendChild
body.appendChild(mainDiv);
```

Kita berhasil membuat `<div id="main">` di dalam `<body>`! Selanjutnya, kita akan mencoba membuat `<div>` di dalamnya.

**js-dom-creation-script.js (Part 2)**
```javascript
// Pertama, kita seleksi terlebih dahulu <body>
var body = document.body;

// Kemudian, kita buat sebuah element HTML <div> menggunakan createElement
var mainDiv = document.createElement('div');

// Untuk membuat <div id="main">, maka kita harus membuat HTML attribute id
var mainDivAttrId = document.createAttribute('id');

// Untuk memberikan nilai kepada id, maka kita gunakan .value
mainDivAttrId.value = "main";

// id="main" kita sudah siap. Sekarang kita harus menambahkan attribute tersebut ke mainDiv
mainDiv.setAttributeNode(mainDivAttrId);

// mainDiv kita sudah menjadi <div id="main">. Saatnya kita tambahkan ke dalam <body>
// Karena Kita akan meletakkan <div id="main"> di dalam <body>, maka kita gunakan appendChild
body.appendChild(mainDiv);

// Selanjutnya, kita akan mengulangi hal yang serupa untuk menambahkan <div id="inside-main">
var insideMainDiv = document.createElement('div');

// Selain menggunakan .value kemudian setAttributeNode, kita bisa menggunakan shorthand berikut
insideMainDiv.setAttribute('id', 'inside-main');

// <div id="inside-main"> kita sudah siap, saatnya di append sebagai child ke <div id="main">
mainDiv.appendChild(insideMainDiv);
```

Kita telah selesai membuat div di dalam div lain. Kita berhasil membuat secara dinamis element HTML dengan hubungan parent-child! Selanjutnya, kita akan membuat `<h1>` di dalam `<div id="inside-main">` yang baru saja kita buat.

**js-dom-creation-script.js (Part 3)**
```javascript
// Pertama, kita seleksi terlebih dahulu <body>
var body = document.body;

// Kemudian, kita buat sebuah element HTML <div> menggunakan createElement
var mainDiv = document.createElement('div');

// Untuk membuat <div id="main">, maka kita harus membuat HTML attribute id
var mainDivAttrId = document.createAttribute('id');

// Untuk memberikan nilai kepada id, maka kita gunakan .value
mainDivAttrId.value = "main";

// id="main" kita sudah siap. Sekarang kita harus menambahkan attribute tersebut ke mainDiv
mainDiv.setAttributeNode(mainDivAttrId);

// mainDiv kita sudah menjadi <div id="main">. Saatnya kita tambahkan ke dalam <body>
// Karena Kita akan meletakkan <div id="main"> di dalam <body>, maka kita gunakan appendChild
body.appendChild(mainDiv);

// Selanjutnya, kita akan mengulangi hal yang serupa untuk menambahkan <div id="inside-main">
var insideMainDiv = document.createElement('div');

// Selain menggunakan .value kemudian setAttributeNode, kita bisa menggunakan shorthand berikut
insideMainDiv.setAttribute('id', 'inside-main');

// <div id="inside-main"> kita sudah siap, saatnya di append sebagai child ke <div id="main">
mainDiv.appendChild(insideMainDiv);

// Selanjutnya, kita akan mencoba membuat sebuah <h1> dengan isi teks didalamnya.
var h1 = document.createElement('h1');

// Untuk membuat isi teks di dalam h1, kita bisa menggunakan createTextNode
var h1Text = document.createTextNode('Heading Sample 1');

// Kita append text ke dalam <h1>
h1.appendChild(h1Text);

// Kemudian, kita append h1 sebagai child dari <div id="inside-main">
insideMainDiv.appendChild(h1);
```

`<h1>` selesai dibuat! yang terakhir, kita akan membuat `<button>` dengan cara yang serupa, dan juga menambahkan event ke dalam button tersebut agar user dapat mengklik button tersebut!

**js-dom-creation-script.js (Part 4)**
```javascript
// Pertama, kita seleksi terlebih dahulu <body>
var body = document.body;

// Kemudian, kita buat sebuah element HTML <div> menggunakan createElement
var mainDiv = document.createElement('div');

// Untuk membuat <div id="main">, maka kita harus membuat HTML attribute id
var mainDivAttrId = document.createAttribute('id');

// Untuk memberikan nilai kepada id, maka kita gunakan .value
mainDivAttrId.value = "main";

// id="main" kita sudah siap. Sekarang kita harus menambahkan attribute tersebut ke mainDiv
mainDiv.setAttributeNode(mainDivAttrId);

// mainDiv kita sudah menjadi <div id="main">. Saatnya kita tambahkan ke dalam <body>
// Karena Kita akan meletakkan <div id="main"> di dalam <body>, maka kita gunakan appendChild
body.appendChild(mainDiv);

// Selanjutnya, kita akan mengulangi hal yang serupa untuk menambahkan <div id="inside-main">
var insideMainDiv = document.createElement('div');

// Selain menggunakan .value kemudian setAttributeNode, kita bisa menggunakan shorthand berikut
insideMainDiv.setAttribute('id', 'inside-main');

// <div id="inside-main"> kita sudah siap, saatnya di append sebagai child ke <div id="main">
mainDiv.appendChild(insideMainDiv);

// Selanjutnya, kita akan mencoba membuat sebuah <h1> dengan isi teks didalamnya.
var h1 = document.createElement('h1');

// Untuk membuat isi teks di dalam h1, kita bisa menggunakan createTextNode
var h1Text = document.createTextNode('Heading Sample 1');

// Kita append text ke dalam <h1>
h1.appendChild(h1Text);

// Kemudian, kita append h1 sebagai child dari <div id="inside-main">
insideMainDiv.appendChild(h1);

// Selanjutnya, kita akan mencoba membuat sebuah <button> dengan isi teks. Langkahnya sama dengan sebelumnya.
var button = document.createElement('button');

var buttonText = document.createTextNode('Click Me!');

button.appendChild(buttonText);

// Lalu, kita akan mencoba membuat button tersebut saat di klik meng-alert sebuah pesan
button.addEventListener('click', function() {
  alert('Hello!');
});

// Terakhir, kita mengappend button tersebut ke dalam insdieMainDiv
insideMainDiv.appendChild(button);
```

Selamat, kamu telah berhasil membuat webpage yang dibentuk dinamis menggunakan JavaScript!

Tambahan: Untuk menghapus element, kita bisa menggunakan removeChild!

```javascript
// Dari awal kita mencoba menambahkan element baru. Bagaimana dengan menghapusnya?
insideMainDiv.removeChild(h1);
```
