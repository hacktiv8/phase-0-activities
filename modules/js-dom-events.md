# DOM Events

## Objectives

Dalam membuat sebuah aplikasi web, interaktivitas dengan user menjadi satu hal yang sangat penting. Untuk membuat user dapat berinteraksi dengan DOM, kita perlu menggunakan events yang merupakan fitur pada DOM.

**DOM**

- ▢ Memahami DOM Events
- ▢ Membuat DOM yang interaktif

## Learnings

### 1. Mengenal Events

Events merupakan hal penting dalam JavaScript, karena JavaScript sendiri merupakan event-driven programming language. Kunci dari cara kerja events adalah dengan membuat
event handling/listener yang dipasangkan ke salah satu komponen di aplikasi kita.

DOM events sangat banyak dan ditujukan untuk berbagai komponen web yang berbeda, mulai
dari button, input, form, dan juga ada yang melibatkan interaksi user menggunakan mouse,
keyboard, touch, dan lain-lain.

Di JavaScript, untuk membuat user dapat berinteraksi dengan DOM, kamu harus membuat DOM tersebut mampu menghandle/mendengarkan sebuah event. Pada saat DOM tersebut telah mampu
menghandle event tersebut, apabila user melakukan interaksi yang sesuai dengan event yang
telah di handle, sebuah interaksi akan terjalin.

### 2. Event Listener

Kamu dengan mudah dapat membuat sebuah DOM menghandle event tersebut dengan fungsi `addEventListener()` pada javascript. Untuk contoh langsung yang lebih jelas, pertama kita
bisa mencoba menyusun halaman HTML kita dulu, yang memiliki beberapa element yang akan kita uji coba untuk menghandle event tersebut.

**js-dom-events.html**
```html
<html>
  <head>
    <title>Learn JS DOM Event</title>
    <style>
      body {
        margin: 0;
        padding: 50px;
        font-family: 'arial';
      }
      .btn {
        background: #446CB3;
        color: #FFFFFF;
        padding: 10px 20px;
        border: 0;
        outline: none;
        font-size: 2em;
        border-radius: 8px;
        border-bottom: 5px solid #34495E;
        cursor: pointer;
        margin: 10px;
        width: 90%;
      }
      .btn:hover {
        border-bottom: 2px solid #34495E;
        margin-top: 13px;
      }
      input[type=text] {
        width: 90%;
        padding: 15px 30px;
        font-size: 1.5em;
        margin: 10px;
        border-radius: 8px;
        border: 1px solid rgba(0,0,0, .2);
        outline: none;
      }
      p {
        margin: 10px;
        font-size: 1.5em;
      }
      form {
        margin: 10px;
        padding: 10px;
        width: 90%;
      }
      span {
        color: #019875;
      }
    </style>
  </head>
  <body>
    <div id="container">
      <button id="alert-on-click-button" class="btn">Click Me to Alert!</button>

      <button id="log-on-hover-button" class="btn">Hover Me to Log!</button>

      <button id="log-on-leave-button" class="btn">Leave Me to Log!</button>

      <form id="main-form">
        <fieldset>
          <legend>Contoh Form</legend>
          <p>Isi Input (berubah setiap di ketik): <span id="on-input-content"></span></p>
          <input id="on-input" name="myValue" type="text" placeholder="Type on me!" />

          <p>Isi Input (berubah setiap keluar dari input): <span id="on-blur-content"></span></p>
          <input id="on-blur" type="text" placeholder="Type on me, then click outside!" />

          <input type="submit" class="btn" value="Submit Form" />
        </fieldset>
      </form>
    </div>
    <script src="js-dom-events-script.js"></script>
  </body>
</html>
```

Lalu kita mulai membuat script JS yang akan menambahkan event listener ke DOM kita.
Pertama, kita akan mencoba membuat sebuah button mampu menghandle click event, dimana
berarti pada saat kita mengklik button tersebut, kita dapat menjalankan sebuah function.

**js-dom-events-script.js (Part 1)**
```javascript
// Select <button> dengan id alert-on-click-button
var alertOnClickButton = document.getElementById('alert-on-click-button');

// Tambahkan Event Listener ke <button> alertOnClickButton, dengan trigger atau pemicu nya adalah click dan memanggil function sebagai parameter kedua.
alertOnClickButton.addEventListener('click', function() {
  alert('Hello There!');
  // Mengakses Salah satu nilai input dari form
});
```

Selanjutnya, kita akan mencoba membuat event handler yang akan menghandle apabila kita menghover/meletakkan mouse pointer kita ke atas sebuah DOM. Selain itu, kita juga akan sekaligus membuat event handler lain yang menghandle apabila mouse pointer kita keluar dari sebuah DOM.

**js-dom-events-script.js (Part 2)**
```javascript
// Select <button> dengan id alert-on-click-button
var alertOnClickButton = document.getElementById('alert-on-click-button');

// Tambahkan Event Listener ke <button> alertOnClickButton, dengan trigger atau pemicu nya adalah click dan memanggil function sebagai parameter kedua.
alertOnClickButton.addEventListener('click', function() {
  alert('Hello There!');
});

// Select <button> dengan id alert-on-click-button
var logOnHoverButton = document.getElementById('log-on-hover-button');

// Tambahkan Event Listener ke <button> alertOnHoverButton, dengan trigger atau pemicu nya adalah mouseenter dan memanggil function sebagai parameter kedua.
logOnHoverButton.addEventListener('mouseenter', function() {
  console.log('Hello, saya sedang melakukan hover atau mouseenter ke button!');
});

// Select <button> dengan id alert-on-leave-button
var logOnLeaveButton = document.getElementById('log-on-leave-button');

// Tambahkan Event Listener ke <button> alertOnHoverButton, dengan trigger atau pemicu nya adalah mouseenter dan memanggil function sebagai parameter kedua.
logOnLeaveButton.addEventListener('mouseleave', function() {
  console.log('Hello, saya sedang kelar dari button!');
});
```

Selamat! Kamu telah mencoba membuat tiga macam button dengan tiga jenis event yang berbeda! Selanjutnya, kita akan mencoba membuat event yang berkaitan dengan form, misalnya pada saat sebuah input dari form diubah, di-blur (keluar dari input form), ataupun mentrigger atau memicu event pada saat kita mensubmit form kita.

```javascript
// Select <button> dengan id alert-on-click-button
var alertOnClickButton = document.getElementById('alert-on-click-button');

// Tambahkan Event Listener ke <button> alertOnClickButton, dengan trigger atau pemicu nya adalah click dan memanggil function sebagai parameter kedua.
alertOnClickButton.addEventListener('click', function() {
  alert('Hello There!');
});

// Select <button> dengan id alert-on-click-button
var logOnHoverButton = document.getElementById('log-on-hover-button');

// Tambahkan Event Listener ke <button> alertOnHoverButton, dengan trigger atau pemicu nya adalah mouseenter dan memanggil function sebagai parameter kedua.
logOnHoverButton.addEventListener('mouseenter', function() {
  console.log('Hello, saya sedang melakukan hover atau mouseenter ke button!');
});

// Select <button> dengan id alert-on-leave-button
var logOnLeaveButton = document.getElementById('log-on-leave-button');

// Tambahkan Event Listener ke <button> alertOnHoverButton, dengan trigger atau pemicu nya adalah mouseenter dan memanggil function sebagai parameter kedua.
logOnLeaveButton.addEventListener('mouseleave', function() {
  console.log('Hello, saya sedang kelar dari button!');
});

// Select <input> dengan id on-input
var onChangeInput = document.getElementById('on-input');

// Select <span id="on-input-content">
var inputContent = document.getElementById('on-input-content');

onChangeInput.addEventListener('input', function(event) {
  inputContent.innerHTML = event.target.value;
});

// Select <input> dengan id on-blur
var onBlurInput = document.getElementById('on-blur');

// Select <span id="on-blur-content">
var blurContent = document.getElementById('on-blur-content');

// Tambahkan Event Listener dengan trigger blur ke input dengan id on-blur
onBlurInput.addEventListener('blur', function(event) {
  blurContent.innerHTML = event.target.value;
});

// Select <form> dengan id main-form
var mainForm = document.getElementById('main-form');

// Tambahkan Event Listener dengan trigger submit ke <form id="main-form">
mainForm.addEventListener('submit', function() {
  alert('Sukses Submit!');
});
```
Kamu bisa "menahan" atau "mencegah" form agar tidak di-redirect ke halaman lain dengan menambahkan `event.preventDefault();` seperti contoh potongan kode di bawah ini:

```javascript
mainForm.addEventListener('submit', function(event) {
  event.preventDefault();
  alert('Sukses Submit!');
});
```

**Note Tambahan**
Apabila kamu mau mengambil value atau nilai dari input form, kamu bisa gunakan DOM selector dan mendapatkan valuenya.

Contoh:

HTML
```html
<input id="username" value="Budi Roni" />
```

JS
```javascript
var usernameInput = document.getElementById(username);
var usernameValue = usernameInput.value;
console.log(usernameValue); // Budi Roni
```

Selamat, kamu telah berhasil mencoba beberapa DOM events!


## References

[DOM Event](https://en.wikipedia.org/wiki/DOM_events)
