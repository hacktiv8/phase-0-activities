# Relearn JavaScript Scope

## Objectives

- ▢ Mengulas kembali dan memahami scope lebih lanjut.

## Learnings

Cakupan atau scope pada JavaScript berhubungan erat dengan konsep global dan local. Global dan local ini dipengaruhi oleh lokasi saat kita deklarasikan. Variabel local bisa saja memiliki identifier yang sama dengan variabel global, tapi konteksnya berbeda. Jika kita ganti nilai suatu variabel yang namanya sama namun konteksnya berbeda, pengaruh hanya terjadi pada variabel dalam konteks yang kita perlakukan.

```javascript
// global scope
var example = "Global";

function testExample() {
  // local scope
  var example = "Local";
  return example;
}

console.log(example); // Global
console.log(testExample()); // Local
```

Dengan kode di atas, jika kita tidak/belum mendeklarasikan variabel `example` pada scope global, kita tidak bisa melakukan `console.log(example)` karena variabel terkait dianggap tidak tercapai.

Selain variabel bahkan kita bisa mengatur scope function seperti...

```javascript
// global scope
var functionA = function() {
  // local scope in functionA
  var functionB = function() {
    // local scope in functionB, in functionA
  };
};
```

Hukum global dan local adalah hal atau objek global dapat diakses di local, namun tidak sebaliknya.

```javascript
var example = "Example"
var functionA = function() {
  console.log(example + " in A");
  var functionB = function() {
    console.log(example + " in B"); // it's possible
  };
  functionB();
};
functionA();
```

Scope juga berkaitan dengan `this` yang sudah kita gunakan sebelumnya.

```javascript
var functionA = function() {
  console.log(this); // global Window object
}

var sampleObject = {};
sampleObject.functionB = function() {
  console.log(this); // Object of sampleObject
}

functionA();
sampleObject.functionB();
```

Maka dari itu, perhatikanlah dan berhati-hatilah waktu dan letak kita mendeklarasikan variabel atau function.
Untuk memperkuat pemahaman kamu, bacalah referensi yang disertakan berikut.

## References

- [JavaScript Scope, on W3Schools](http://www.w3schools.com/js/js_scope.asp)
- [Everything you wanted to know about JavaScript scope, by Todd Motto](https://toddmotto.com/everything-you-wanted-to-know-about-javascript-scope)
- [Demystifying JavaScript Variable Scope and Hoisting, by Ivaylo Gerchev on SitePoint](https://sitepoint.com/demystifying-javascript-variable-scope-hoisting)
- [Understand JavaScript’s “this” With Clarity, and Master It - JavaScript.isSexy](http://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it)
- [JavaScript Variable Scope and Hoisting Explained - JavaScript.isSexy](http://javascriptissexy.com/javascript-variable-scope-and-hoisting-explained)
- [16 JavaScript Concepts JavaScript Professionals Must Know Well - JavaScript.isSexy](http://javascriptissexy.com/16-javascript-concepts-you-must-know-well)
