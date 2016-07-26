# Learn JavaScript Code Style dan Guide

## Objectives

Seperti yang tertera pada bagian referensi pekan ini, ada beberapa hal yang perlu kita perhatikan agar praktik code dan hasil kerja kita baik dan berkualitas.

## Learnings

### 1. Memahami cara penulisan JavaScript yang baik

- ▢ Pahami berbagai aturan penulisan JavaScript di sini:
- ▢ Cek berbagai pedoman penulisan code berikut:
  - [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
  - [Google JavaScript Style Guide](https://google.github.io/styleguide/javascriptguide.xml)
  - [Code Conventions for the JavaScript, by Douglas Crockford](http://javascript.crockford.com/code.html)
  - [The Zen Approach: JavaScript Styleguide](https://github.com/nijikokun/the-zen-approach)

### 2. Menggunakan tiap bahasa sesuai fungsi utamanya

Ini saran klasik yang sudah seharusnya diketahui semua developer. Tiap bahasa yang sudah kita ketahui saja misalnya:

- HTML dibuat untuk menstrukturkan halaman web
- CSS dibuat untuk styling halaman
- JavaScript untuk memberi interaksi dan fungsi halaman

Maka dari itu misalnya jangan paksakan JavaScript untuk mengubah style halaman web dengan fungsi yang mirip dan sebenarnya CSS sudah bisa lakukan. Ketahuilah kehandalan masing-masing bahasa agar tujuan kita bisa tercapai dengan tepat.

### 3. Membuat kode program yang mudah dibaca

Kode yang baik sederhananya adalah kode yang mudah dibaca oleh manusia. Termasuk penamaan variable maupun function yang mudah dibaca dan digunakan.

Contoh kurang baik atau buruk:

```javascript
var coba = "andi";
var cobacoba = "ruben";
cobaSesuatu = function(a, b) {
  console.log(a + b)
}
cobaSesuatu(coba, cobacoba)
```

Contoh baik:

```javascript
// Initiate name variables
var firstName, lastName, fullName;

/*
 * Concatinate first name and last name
 * to create full name
 *
 * @param firstName String
 * @param lastName String
 */
var concateFullName = function(firstName, inputLastName) {
  return `${firstName} ${lastName}`;
}

inputFirstName = "Andi";
inputLastName = "Ruben";

// Do concatination
fullName = concateFullName(inputFirstName, inputLastName);

// Log/print full name to the console
console.log(fullName);
```

Kode kedua memang lebih panjang, namun lebih jelas dan terbaca dengan nyaman. Bahkan orang lain pun dapat mengerti maksud kode tersebut. Tentu saja dalam menulis code pun, tak ada yang hitam putih, namun abu-abu. Seiring pengalaman, kamu akan mengetehui mana saja pertimbangan yang harus diambil dalam mendesain dan menulis code.

### 4. Mengenal Style Checking dan Hinting/Linting

Dalam penulisan code apalagi JavaScript, akan ada sangat banyak variasi cara dan gaya penyusunannya. Maka dari itu, kode kita bisa saja rentan berantakan dan tidak sesuai dengan good/best practice yang sudah kita pelajari. Manusia tak luput dari kesalahan, salah ketik (type), dan lainnya. Maka dari itu kita bisa andalkan alat pengecek code style bahkan potensi error/masalah, aksesoris bernama hinter atau linter. Hinter atau linter ini akan melakukan proses hinting and linting, menganalisis code kita tanpa menjalankannya.

Berikut beberapa hinter/linter yang paling populer:

- [JSLint: The JavaScript Code Quality Tool](http://jslint.com)
- [JSHint: A JavaScript Code Quality Tool](http://jshint.com)
- [JSCS: Code style linter and formatter for your style guide](http://jscs.info)
- [ESLint: Pluggable JavaScript linter](http://eslint.org)
