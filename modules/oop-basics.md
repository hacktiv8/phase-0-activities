# Get to Know Object-Oriented Programming (OOP)

## Objectives

- ▢ Mengetahui salah satu paradigma pemrograman modern yang intuitif dengan dunia nyata.

## Directions

### Mengenal Object-Oriented Programming (OOP)

- [Object Oriented Analysis & Design Tutorial, on TutorialsPoint](http://www.tutorialspoint.com/object_oriented_analysis_design)

**Catatan:** Cukup sekilas saja, tidak perlu dibaca semuanya

### Mengenal Implementasi Class dan Object pada ES6

Berikut sekilas kita ulas, bagaimana membuat objek yang berbasiskan akan paradigma OOP. Class dan object di sini bukan untuk disamakan/dipusingkan caranya dengan tipe data objek (`{}`), karena lebih mirip seperti membuat blueprint atau rencana yang bisa dipakai berkali-kali untuk membuat satuan objek.

Sintaksnya seperti berikut:

**Kerangka Penyusunan Class ES6**

```javascript
class [ClassName] {
  constructor(attributeValue) {
    this.attributeName = attributeValue;
  }

  setterFunctionExample(newValue) {
    this.attributeName = newValue;
  }

  getterFunctionExample() {
    return this.attributeName;
  }
}
```

perhatikan struktur kode diatas (hanya merupakan kerangka dan tidak dapat berfungsi). Untuk memulai pembuatan sebuah class, kita membutuhkan sintaks `class` yang diikuti dengan curly bracket (`{}`). Lalu, di dalam class akan terdapat beberapa fungsi, namun fungsi yang terpenting adalah `constructor`, yang merupakan fungsi yang otomatis akan dijalankan pada saat sebuah instance class dipanggil. Apa itu instance dan object, akan kita bahas sebentar lagi di bawah.

Kita bisa membuat berbagai macam fungsi di dalam `class`, namun terdapat standard dimana fungsi untuk memanggil nilai atribut biasa disebut sebagai getter, dan fungsi untuk mengubah nilai atribut disebut sebagai setter.  

*Tunggu, apa itu instance?*

Untuk memberikan bayangan, class bisa dibilang sebuah blueprint yang menggambarkan susunan atribut dan fungsi dari sebuah object. pada saat sebuah class dibuat menjadi object, kita memanggil sintaks `new` pada class tersebut untuk membuat sebuah object yang disebut juga sebagai instance dari class tersebut. Cara pemanggilannya adalah sebagai berikut:

```javascript
var newObjectFromClass = new ClassName(parametersForConstructor)
```

**Contoh Class Sederhana 1**

```javascript
class Square {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}

let kotak = new Square(100, 200);
let kotakLain = new Square(300, 400);

console.log(kotak.height); // 100
console.log(kotakLain.width); // 400
```

Kamu dapat mencoba kode di atas [disini](http://jsbin.com/taceloj/edit?js,console)

**Contoh Class Sederhana 2, dengan Setter dan Getter**

```javascript
class Square {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  setHeight(newHeight) {
    this.height = newHeight;
  }

  setWidth(newWidth) {
    this.width = newWidth;
  }

  getHeight() {
    return this.height;
  }

  getWidth() {
    return this.width;
  }

  getArea() {
    let area = this.height * this.width;
    return area;
  }
}

let kotak = new Square(100, 200);
let kotakLain = new Square(300, 400);

console.log(kotakLain.getWidth()); // 400
console.log(kotakLain.getArea()); // 120000

console.log(kotak.getHeight()); // 100
kotak.setHeight(200);
console.log(kotak.getHeight()); // 200
console.log(kotak.getArea()); // 40000
```

Kamu dapat mencoba kode di atas [disini](http://jsbin.com/lohawiq/edit?js,console)

## References

- [Introduction to Object-Oriented JavaScript, on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
- [Object Oriented JavaScript: Udacity](https://www.udacity.com/course/object-oriented-javascript--ud015)
