#

## Objectives

- ▢ TODO

## Directions

### Mengenal Object-Oriented Programming (OOP)

- ▢ Pelajari dari referensi berikut:
  - [Object Oriented Programming, on JavaScript Tutorial](http://javascript.info/tutorial/object-oriented-programming)

### Mengenal Implementasi Class dan Object pada ES6

Berikut sekilas kita ulas sebagai preview saja, bagaimana membuat objek yang berbasiskan akan paradigma OOP. Class dan object di sini bukan untuk disamakan/dipusingkan caranya dengan tipe data objek (`{}`), karena lebih mirip seperti membuat blueprint atau rencana yang bisa dipakai berkali-kali untuk membuat satuan objek.

Sintaksnya seperti berikut.

```javascript
class Square {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}

var kotak = new Square(100, 200);
var kotakLain = new Square(300, 400);

// kotak.height === 100
// kotakLain.width === 400
```

## References

- [Introduction to Object-Oriented JavaScript, on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
