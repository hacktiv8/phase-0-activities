# Transversing in Document Object Model (DOM)

## Objectives

Di layout HTML yang cukup kompleks, kita akan bertemu dengan banyak element HTML yang memiliki hubungan parent-child yang dalam, dan pada saat kita menggunakan JavaScript untuk menseleksi atau memanipulasinya, tidak mungkin kita harus memberikan id atau class ke semua element-nya. Kita bisa menseleksi element HTML dari parent atau dari childnya. Untuk lebih dalam memahami hal ini, kamu harus telah mengerti hierarki parent-child yang terjadi di susunan HTML. Tapi tenang saja, kita akan mengulas ulang hal tersebut.

**DOM Transversing**

- ▢ mereview Hierarki Parent-Child di HTML
- ▢ menjelajah DOM dengan hubungan Parent, Child, dan Sibling

## Learnings

### 1. Hierarki Layout HTML

Hierarki layout HTML adalah bagaimana sebuah element HTML saling terkait satu sama lain. Untuk beberapa element, dapat terkandung di dalam element HTML lain. Hal inilah yang disebut sebagai element parent-child. Element HTML yang terkandung di dalam element HTML lain, adalah child/anak dari element induk nya tersebut.

![Hierarki dalam Layout HTML](assets/html-hierarcy.gif)

Contoh gambar di atas merupakan gambaran sederhana dari sebuah layout HTML. Apabila layout di atas kita coba konversikan ke dalam kode HTMl, akan seperti kode di bawah ini (untuk kebutuhan kode, ditambahkan id untuk beberapa div):

```html
<html>
  <head></head>
  <body>
    <h1></h1>
    <div id="contoh-div-1">
      <p id="contoh-p-1">
        <strong></strong>
        <em></em>
      </p>
    </div>
    <div id="contoh-div-2">
      <h2></h2>
      <p id="contoh-p-2"></p>
      <ul>
        <li></li>
        <li></li>
      </ul>
    </div>
  </body>
</html>
```

Bisa kita lihat seperti visualisasi layout web page dan code di atas, satu element HTML menjadi child untuk yang lainnya. Terkait relasi parent-child, ada juga relasi yang dinamakan sibling. Sibling adalah "saudara" dari sebuah child, yang memiliki parent yang sama. Jika kita analogikan dalam sebuah keluarga sebagai seorang anak atau sebuah child, sibling adalah adik atau kakak kandung kita, dan parent adalah orang tua kandung kita. Di bawah ini di jelaskan peran masing-masing element HTML di atas dalam susunan hierarki nya.

- `<html>`                  : merupakan parent paling atas
- `<head>`                  : merupakan child dari `<html>`
- `<body>`                  : merupakan child dari `<html>`, sibling dari `<head>`
- `<h1>`                    : merupakan child dari `<body>`
- `<div id="contoh-div-1">` : merupakan child dari `<body>`, sibling dari `<h1>`
- `<p id="contoh-p-1"> `    : merupakan child dari `<div id="contoh-div-1">`
- `<strong>`                : merupakan child dari `<p id="contoh-p-1">`
- `<em>`                    : merupakan child dari `<p id="contoh-p-1">`, sibling dari `<strong>`
- `<div id="contoh-div-2">` : merupakan child dari `<body>`, sibling dari `<h1>` dan `<div id="contoh-div-1">`
- `<h2>`                    : merupakan child dari `<div id="contoh-div-2">`
- `<p id="contoh-p-2">`     : merupakan child dari `<div id="contoh-div-2">`, sibling dari `<h2>`
- `<ul>`                    : merupakan child dari `<div id="contoh-div-2">`, sibling dari `<h2>` dan `<p id="contoh-p-2">`
- `<li>`                    : merupakan child dari `<ul>`
