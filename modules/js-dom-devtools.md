# Learn DOM and More on Dev Tools

## Objectives

Dalam mengembangkan web, kita harus menyadari bahwa kita sekaligus membuat Document Object Model (DOM) yang tersusun dalam dokumen HTML. Dengan pengetahuan DOM, kita bisa secara lebih lengkap mengetahui dan mampu untuk membuat interaksi pada halaman web menggunakan JavaScript.

Selain itu, selama menggunakan Chrome Dev Tools kemungkinan kita kebanyakan hanya berkutat di Console saja. Beberapa dari kita mungkin sudah secara tidak sengaja mengecek tab Elements Inspector. Sekarang saatnya kita mengetahui lebih jelas apa saja yang ada di Dev Tools tersebut dan kegunaannya.

**DOM**

- ▢ Memahami Document Object Model (DOM) serta hubungannya dengan HTML, CSS, dan JavaScript.
- ▢ Mengetahui berbagai DOM API.
- ▢ Mengintegrasikan DOM dengan HTML dan CSS.
- ▢ Menjelajahi DOM dengan JavaScript.
- ▢ Memanipulasi DOM dengan JavaScript.
- ▢ Menggayakan (styling) DOM dengan CSS.
- ▢ Mengetahui node property, value, attributes.

**Dev Tools**

- ▢ Mengenal Chrome DevTools lebih lanjut.
- ▢ Menavigasikan dan mengedit halaman HTML serta aturan CSS menggunakan Dev Tools Elements Inspector.
- ▢ Menggunakan DevTools untuk memanipulasi elements yang ada pada DOM.
- ▢ Mengidentifikasi aset/media yang dapat memperlambat page load.

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

Umumnya kita bisa melakukan perubahan DOM dengan JavaScript seperti berikut:

```javascript
document.getElementsByTagName("h1")[0].innerHTML = "Article Title";
document.getElementsById("title").innerHTML = "Article Title";
document.getElementsByClassName("title").innerHTML = "Article Title";
```

Mirip dengan cara mencetak JavaScript ke halaman web!

```javascript
document.write("Hello!");
```

### 2. Menjelajahi DOM (DOM Traversing)

Bayangkan rangkaian kaitan DOM seperti sebuah pohon yang terbalik. Pada dasarnya HTML dimulai dari node `html` sebagai ujung/akar paling awal (root), kemudian lanjut ke cabang lainnya seperti `head` (masuk ke `title`, `link`, dll) yang bersebelahan dengan `body` yang di dalamnya terdapat berbagai elemen umum seperti `div`, `h1`, `p`, `ul` (yang bisa berisi `li`), `table` (berisi `tr`, `td`), serta lain sebagainya.

Berbagai properti node yang umum digunakan antara lain:

- ke atas: `parentNode`
- ke bawah: `children`, `childNodes`, `firstChild`, `lastChild`
- ke samping kiri/kanan: `previousSibling`, `nextSibling`

Misalkan terdapat DOM seperti ini

```html
<html>
<head>
</head>
<body>
  <div>
    <img id="roof" class="long" src="roof.png">
    <img id="logo" class="small" src="hacktiv8.png">
  </div>
</body>
</html>
```

Kita bisa memperoleh value `src` pada elemen `img` urutan kedua tersebut (`#logo.small) dengan berbagai cara yakni...

```html
document.getElementsByTagName("img")[1].src;
document.getElementsByClassName("small")[0].src;
document.getElementById("logo").src;
```

Mereka serupa tapi tak sama! Karena sebab-sebab berikut:

- Tag name tidak unik, bisa terdapat banyak tag yang sama dari sebuah dokumen. Sehingga `getElementsByTagName` menghasilkan array dengan dua butir `img`, yang bisa kita ambil indeks `1` untuk `img` kedua.
- Class name juga tidak untuk, bisa ada banyak tag dengan class yang sama. Sehingga `getElementsByTagName` menghasilkan array juga, yang kebetulan hanya ada satu butir class `small`, yang bisa kita ambil indeksnya `0` saja.
- ID name pasti dan harus unik, jadi kita bisa langsung ambil elemen beserta properti dan nilainya.

Cara-cara lain seperti...

```javascript
document.getElementsByTagName("div")[0].childNodes[3].src;
document.getElementsByTagName("div")[0].childNodes[2].nextElementSibling.src;
```

Bahkan kita bisa gunakan kueri (query) untuk mencari dan menemukan node yang kita spesifikasikan melalui selector seperti CSS.

```javascript
document.querySelector("div > img");
document.querySelectorAll("div > img:first-child");
```

Perbedaan cara dan metode tersebut akan sangat berguna pada saat kita harus sangat spesifik mendefinisikan atau mengekspresikan node yang kita mau/perlukan. Untuk contoh sederhana, mungkin kita tinggal pilih saja yang paling mudah tanpa harus berumit-rumit.

### Node Property, Value, Attributes

Terdapat berbagai property dan value yang bisa kita dapat dari sebuah node, seperti:

- `nodeType`: tipe node yang biasanya bernilai `1` untuk elemen, `3` untuk node text
- `nodeName` dan `tagName`: nama tag dengan huruf all uppercase
- `innerHTML`: isi dari node elemen, value-nya dapat di-assign ulang
- `nodeValue`: isi dari node text, value-nya dapat di-assign ulang juga

Property dan attribute agak mirip tapi secara teknis berbeda. Property terdapat pada setiap node, sedangkan attribute khusus ada pada node elemen.

Kemudian attribute tiap node pasti memiliki value, antara bertipe string, number, atau boolean. Kita pun bisa mendapatkan akses ke attribute node yang dipilih untuk mendapatkan data atau mengubah value dengan berbagai method seperti:

- `elementName.hasAttribute(name)`
- `elementName.getAttribute(name)`
- `elementName.setAttribute(name, value)`
- `elementName.removeAttribute(name)`

`name` attribute sudah pasti string, namun tidak case sensitive, juga biasanya muncul jika kita panggil dengan `innerHTML`.

Beberapa property dan attribute yang kita butuhkan biasanya terdapat pada element adalah:

- `id`
- `class` atau `className`
- `href`
- `value`
- `src`

Untuk lebih mudah dan tidak membingungkan, kita hindari penggunaan attribute, gunakan property saja.

### 3. Pengubahan DOM (DOM Manipulation)

Pengubahan ataupun modifikasi bisa dilakukan sesederhana meng-assign value baru pada sebuah property.

```javascript
document.getElementById("logo").src = "new-image.png";
document.getElementById("opening").innerHTML = "<h1>Hello!</h1>";
```

atau dengan method yang tersedia...

```javascript
var anElement = document.getElementById("aTarget");
var aNode = document.createElement("span");
var aText = "Exclusively New!";
anElement.appendChild(aNode);
aNode.appendChild(document.createTextNode(aText));

var anUnusedElement = document.getElementById("unused");
anUnusedElement.parentNode.removeChild(anUnusedElement);

var aBrokenElement = document.getElementById("broken");
var aFixedElemen = document.createElement("aside");
aBrokenElement.replaceChild(aBrokenElement, aFixedElement);
```

Khusus untuk element `table` dan `form`, terdapat beberapa property istimewa yang bisa kita gunakan:

- `table`
  - `rows`: array berisi element `tr`
  - `celss`: array berisi elemen `td` pada `tr`
- `form`
  - `elements`: array berisi berbagai element `input` yang juga berisi...
    - `value`: nilai dari property/attribute input

Property `name` pada element `form` dan `input`, serta `option` pada `select`, juga bisa langsung dipanggil langsung seperti property biasa.

```html
<form name="contact">
  <input name="fullName" value="your name">
  <select name="favorite">
    <option name="javascript" value="javascript">JavaScript</option>
    <option name="cpp" value="c++">C++</option>
  </select>
  <input name="submit" value="submit">
</form>
```

```javascript
document.forms.contact;
document.forms[0];
document.forms.contact.elements.fullName;
document.forms.contact.elements.submit.value;
document.forms.contact.elements["favorite"].options[0];
```

### 4. DOM Style

Terdapat berbagai property dan method DOM yang berkaitan dengan CSS:

- `className`
- `style`
- `cssText`
- `getComputedStyle()`
- `currentStyle()`

Untuk kali ini bisa dieksplorasi sendiri melalui referensi, mirip dengan cara mengelola property DOM sebelum-sebelumnya.

Silakan coba-coba secara mandiri dengan bantuan Dev Tools Console dan Elements serta referensi DOM API, untuk mengelola HTML DOM dan mengaitkannya dengan JavaScript dan CSS.
