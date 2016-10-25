# Node JS

## Objectives

- ▢ Mengenal node.js
- ▢ Meninstall node.js di komputer
- ▢ Memanfaatkan node.js untuk menjalankan JavaScript melalui server-side

## Learnings

### Mengenal Node.js

![Node.js Logo](assets/nodejs-logo.png)

Pada dasarnya merupakan implementasi JavaScript sebagai platform di backend atau server. Secara teknis, adalah sebuah runtime JavaScript yang berjalan dengan Chrome V8 JavaScript engine. Fitur utamanya adalah model event-driven dan non-blocking Input/Output (I/O) yang ringan dan efisient. Node.js memiliki pengatur paket atau modul aplikasi yang disebut npm, yang juga merupakan ekosistem library open source.

Mayoritas tools yang akan temukan ke depan, bahkan dari berbagai pedoman di sini, sebenarnya membutuhkan instalasi Node.js. Tapi untuk sementara waktu, gunakan Node.js jika sudah siap saja. Beberapa hal yang kita kenalkan saja tanpa harus digunakan segera.

### Instalasi Node.js

Kamu bisa menginstall Node.js melalui [website resmi node.js](https://nodejs.org/en/) dan mendownload node.js ke komputer kamu sesuai dengan sistem operasi yang kamu miliki. Ikuti langkah-langkah yang ditunjukkan pada installer dan dalam waktu yang tidak lama, kamu sukses memiliki node.js berjalan di komputermu!

Untuk mengetest apakah node.jsmu sudah berjalan dengan benar, masuk ke Terminal atau Command Prompt di komputermu dan jalankan:

```javascript
> node --version
```

Apabila versi node.js mu keluar, berarti kamu telah menginstall node.js dengan benar! Dengan menginstall node.js, kamu juga secara otomatis telah menginstall Node Package Manager, sebuah tools yang digunakan untuk memaintain semua package yang akan berjalan di atas node.js. Kamu bisa abaikan soal NPM untuk sementara, namun ini akan menjadi senjata utama kita di materi HACKTIV8 yang akan mendatang!

### REPL Node.js

REPL adalah sebuah fitur pada node.js yang memiliki kepanjangan adalah Read Eval Print Loop. Kamu bisa menjalankan berbagai operasi javascript pada Node.js melalui REPL. Untuk mencobanya, kamu hanya perlu menjalankan node, dan memasukkan berbagai instruksi operasi yang mau kamu jalankan.

```javascript
> node
> 1 + 2
3
> 'hello HACKTIV8'
'hello HACKTIV8'
> 'node js is ' + 'cool!'
'node js is cool!'
```

### Menjalankan file JavaScript melalui Terminal dengan Node.js

Dengan node.js, kamu bisa menjalankan file JavaScript tanpa harus melalui client-side (browser), namun dengan server-side (menggunakan terminal atau command prompt). Untuk menjalankan, kamu tinggal menggunakan node <spasi> nama file javascript yang mau kamu jalankan.


**contoh**

test-javascript.js:
```javascript
var message = 'hello! I\'m calling JavaScript using node! W00t!'
console.log(message)
```

CONSOLE:
```javascript
> node test-javascript.js
'hello! I\'m calling JavaScript using node! W00t!'
```
