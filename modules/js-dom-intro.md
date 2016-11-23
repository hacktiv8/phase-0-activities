# Introduction to Document Object Model (DOM)

## Objectives

Dalam mengembangkan web, kita harus menyadari bahwa kita sekaligus membuat Document Object Model (DOM) yang tersusun dalam dokumen HTML. Dengan pengetahuan DOM, kita bisa secara lebih lengkap mengetahui dan mampu untuk membuat interaksi pada halaman web menggunakan JavaScript.

**DOM**

- ▢ Memahami Document Object Model (DOM)
- ▢ Memahami DOM selector
- ▢ memanipulasi isi HTML dari DOM yang telah di select

## Learnings

### 1. Mengenal DOM

Document Object Model (DOM) merupakan antarmuka pemrograman untuk dokumen HTML dan XML (juga SVG) terkait. Dengan DOM, kita bisa mengetahui dan mengatur struktur representasi dokumen melalui program terutama JavaScript. Program dapat mengolah struktur, style, dan isi dari dokumen tersebut. Maka dari itu DOM membutuhkan dan menghubungkan antara dokumen dan kode pemrograman.

Seperti yang telah diketahui sebelumnya bahwa hampir semua hal di JavaScript adalah objek, maka begitupun pada HTML yang kita ketahui melalui DOM. Kombinasi interaksi antarmuka antara DOM dan JavaScript ini juga dapat dilakukan karena adanya Application Programming Interface (API). API memungkinkan sebuah program berkomunikasi dengan program yang lain dengan cara tertentu.
Dengan API, bahasa selain JavaScript seperti Python dan Ruby jadi bisa juga mengakses dokumen HTML dan XML.

DOM API di HTML umumnya adalah untuk node ataupun objek `element`, `document`, dan `window`. Setiap hal tersebut memiliki berbagai property (nilai) dan method (aksi), bahkan bisa juga dipasang sebuah penangan kejadian (event handler) sehingga jika ada kejadian tertentu dilakukan suatu statement akan dijalankan. Urutan atau strukturnya diatur secara hierarkis seperti pohon berikut.

- `window`: `frame`, `parent`, `self`, `top`
  - `history`
  - `location`
  - `document`
    - `element`: `body`, `h1`, `p`, `button`, dll

![Visualisasi DOM Tree](assets/html-dom.png)

Hubungan antar berbagai "object" tersebut atau yang akan kita sebut seterusnya dengan "node" adalah antara _parent_ untuk yang di atasnya, _children_ untuk yang di bawahnya, dan _sibling_ yang hierarkinya sama.

### 2. Seleksi DOM dari HTML

**Mulai dari bagian ini, snippet atau potongan kode ini akan berlanjut/bersambung.**
Sebelum mencoba melakukan seleksi dan manipulasi, kita coba asumsikan penggunaan
Kita bisa melakukan seleksi terhadap DOM dengan mengunakan beberapa sintaks berikut:

**js-simple-dom.html**
```html
<html>
  <head>
    <title>Contoh Webpage Standard</title>
  </head>
  <body>
    <div id="page-title">Sample Page Title</div>
    <h1>Test Sample Heading</h1>
    <div class="page-box">Page Box 1</div>
    <div class="page-box">Page Box 2</div>
    <div class="page-box">Page Box 3</div>
    <script src="js-simple-dom-script.js"></script>
  </body>
</html>
```

**js-simple-dom-script.js (part 1)**
```javascript
var pageTitleElement = document.getElementById("page-title");
// Menyeleksi DOM berdasarkan Id element dan menampungnya ke dalam variabel. Isinya merupakan object HTML element

var pageBoxElements = document.getElementsByClassName("page-box");
// Menyeleksi DOM berdasarkan nama class element dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element, walau <h1> hanya ada 1.

var pageHeadings = document.getElementsByTagName("h1");
// Menyeleksi DOM berdasarkan tag <h1> dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element
```

Untuk memberikan gambaran apa yang didapatkan dan ditampung oleh variabel tersebut, kamu dapat menggunakan `console.log()` di variabel tersebut. variabel pageTitleElement akan menampung object HTML element, sedangkan variabel pageBoxElements akan menampung array dari tiga object HTML element.

### 3. Mengakses isi HTML dari DOM

Kita bisa mengakses isi HTML dari DOM yang telah kita seleksi dengan sintaks berikut:

**js-simple-dom-script.js (part 2)**
```javascript
var pageTitleElement = document.getElementById("page-title");
// Menyeleksi DOM berdasarkan Id element dan menampungnya ke dalam variabel. Isinya merupakan object HTML element

var pageBoxElements = document.getElementsByClassName("page-box");
// Menyeleksi DOM berdasarkan nama class element dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element, walau <h1> hanya ada 1.

var pageHeadings = document.getElementsByTagName("h1");
// Menyeleksi DOM berdasarkan tag <h1> dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element

var pageTitleElementsContent = pageTitleElement.innerHTML;
console.log('isi <div id="page-title"> :' + pageTitleElementsContent);
// isi <div id="page-title"> adalah Sample Page Title

var pageBoxElementsContent = pageBoxElements.innerHTML;
console.log('isi <div class="page-box"> :' + pageBoxElementsContent);
// isi <div class="page-box"> adalah undefined!
```

isi `<div class="page-box">` adalah `undefined`! Kenapa? pageBoxElements adalah array, dan saat kita melakukan `innerHTML` ke array, maka hasilnya adalah undefined!

Kita bisa melakukan perubahan DOM dengan JavaScript seperti berikut:

**js-simple-dom-script.js (part 3)**
```javascript
var pageTitleElement = document.getElementById("page-title");
// Menyeleksi DOM berdasarkan Id element dan menampungnya ke dalam variabel. Isinya merupakan object HTML element

var pageBoxElements = document.getElementsByClassName("page-box");
// Menyeleksi DOM berdasarkan nama class element dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element, walau <h1> hanya ada 1.

var pageHeadings = document.getElementsByTagName("h1");
// Menyeleksi DOM berdasarkan tag <h1> dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element

var pageTitleElementContent = pageTitleElement.innerHTML;
console.log('isi <div id="page-title"> :' + pageTitleElementContent);
// isi <div id="page-title"> adalah Sample Page Title

// Mengambil isi elemen pageBoxElements yang pertama, yaitu index ke 0
var firstPageBoxElement         = pageBoxElements[0];
var firstpageBoxElementContent  = firstPageBoxElement.innerHTML;

// Mengambil isi elemen pageBoxElements yang kedua, yaitu index ke 1
var secondPageBoxElement         = pageBoxElements[1];
var secondpageBoxElementContent  = secondPageBoxElement.innerHTML;

// Mengambil isi elemen pageBoxElements yang ketiga, yaitu index ke 2
var thirdPageBoxElement         = pageBoxElements[2];
var thirdpageBoxElementContent  = thirdPageBoxElement.innerHTML;

// Menampilkan isi elemen dengan console.log
console.log('isi <div class="page-box"> yang pertama:' + firstpageBoxElementContent);
console.log('isi <div class="page-box"> yang kedua:' + secondpageBoxElementContent);
console.log('isi <div class="page-box"> yang ketiga:' + thirdpageBoxElementContent);
```

Agar lebih efisien, kamu bisa mengaksesnya juga menggunakan looping!

**js-simple-dom-script.js (part 4)**
```javascript
var pageTitleElement = document.getElementById("page-title");
// Menyeleksi DOM berdasarkan Id element dan menampungnya ke dalam variabel. Isinya merupakan object HTML element

var pageBoxElements = document.getElementsByClassName("page-box");
// Menyeleksi DOM berdasarkan nama class element dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element, walau <h1> hanya ada 1.

var pageHeadings = document.getElementsByTagName("h1");
// Menyeleksi DOM berdasarkan tag <h1> dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element

var pageTitleElementContent = pageTitleElement.innerHTML;
console.log('isi <div id="page-title"> :' + pageTitleElementContent);
// isi <div id="page-title"> adalah Sample Page Title

// Meloop array pageBoxElements
for(var i = 0; i < pageBoxElements.length; i++) {
  var currentPageBoxElement         = pageBoxElements[i];
  var currentPageBoxElementContent  = currentPageBoxElement.innerHTML;
  console.log('isi <div class="page-box"> index ke ' + i + ': ' + currentPageBoxElementContent);
}
```

### 3. Memanipulasi isi HTML dari DOM

Setelah kita dapat mengakses isi HTML dari sebuah DOM, kita juga dapat memanipulasi isinya. Cara manipulasinya serupa dengan mengakses, tapi kita menggunakan operator assignment `=`.

**js-simple-dom-script.js (part 5)**
```javascript
var pageTitleElement = document.getElementById("page-title");
// Menyeleksi DOM berdasarkan Id element dan menampungnya ke dalam variabel. Isinya merupakan object HTML element

var pageBoxElements = document.getElementsByClassName("page-box");
// Menyeleksi DOM berdasarkan nama class element dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element, walau <h1> hanya ada 1.

var pageHeadings = document.getElementsByTagName("h1");
// Menyeleksi DOM berdasarkan tag <h1> dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element

var pageTitleElementContent = pageTitleElement.innerHTML;
console.log('isi <div id="page-title"> :' + pageTitleElementContent);
// isi <div id="page-title"> adalah Sample Page Title

// Meloop array pageBoxElements
for(var i = 0; i < pageBoxElements.length; i++) {
  var currentPageBoxElement         = pageBoxElements[i];
  var currentPageBoxElementContent  = currentPageBoxElement.innerHTML;
  console.log('isi <div class="page-box"> index ke ' + i + ': ' + currentPageBoxElementContent);
}

// Mengubah isi pageTitleElement
pageTitleElement.innerHTML = 'Updated Content of Page Title Element';
var newPageTitleElementContent = pageTitleElement.innerHTML;
console.log('isi baru dari <div id="page-title"> :' + newPageTitleElementContent);
```

Kamu juga bisa mengisi innerHTML tidak hanya dengan teks, namun juga dengan element HTML.

**js-simple-dom-script.js (part 6)**
```javascript
var pageTitleElement = document.getElementById("page-title");
// Menyeleksi DOM berdasarkan Id element dan menampungnya ke dalam variabel. Isinya merupakan object HTML element

var pageBoxElements = document.getElementsByClassName("page-box");
// Menyeleksi DOM berdasarkan nama class element dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element, walau <h1> hanya ada 1.

var pageHeadings = document.getElementsByTagName("h1");
// Menyeleksi DOM berdasarkan tag <h1> dan menampungnya ke dalam variabel. Isinya merupakan array dari object HTML element

var pageTitleElementContent = pageTitleElement.innerHTML;
console.log('isi <div id="page-title"> :' + pageTitleElementContent);
// isi <div id="page-title"> adalah Sample Page Title

// Meloop array pageBoxElements
for(var i = 0; i < pageBoxElements.length; i++) {
  var currentPageBoxElement         = pageBoxElements[i];
  var currentPageBoxElementContent  = currentPageBoxElement.innerHTML;
  console.log('isi <div class="page-box"> index ke ' + i + ': ' + currentPageBoxElementContent);
}

// Mengubah isi pageTitleElement dengan tag HTML
pageTitleElement.innerHTML = '<h2>Updated Content of Page Title Element</h2>';
var newPageTitleElementContent = pageTitleElement.innerHTML;
console.log('isi baru dari <div id="page-title"> :' + newPageTitleElementContent);
```

Kamu telah bisa menggunakan selector untuk memilih dan mengakses sebuah element HTML. Kamu juga telah bisa mengubah isi HTML dari element yang telah kamu pilih. Saatnya mulai latihan tentang selector dan askes nilai! :smile:
