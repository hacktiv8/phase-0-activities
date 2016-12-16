# JavaScript Object and JSON

## Objectives

- ▢ Memahami pembuatan dan kegunaan pasangan key-value dalam sebuah object.
- ▢ Mengenal JSON dan perbedaannya dengan object biasa.

## Learnings
- [Object](js-object-json.md#object)
- [JSON](js-object-json.md#json)

### Object

Objek adalah kumpulan tidak berurut yang merangkai beberapa kunci-nilai (key-value pairs). Kita bisa tulis dengan kurung kurawal (curly braces), yang mana propertinya ditulis seperti `keyName: value`, dipisah dengan koma. Kuncinya adalah string, tapi tanda petik tidak diharuskan jika identifer yang ditulis valid. Objek mirip dengan "dictionaries" atau "maps" di bahasa pemrograman lain. Agak mirip dengan array, tapi lebih kaya akan data. Berikutnya kamu juga akan tahu bahwa hampir semua hal di JavaScript juga merupakan objek.

```javascript
> var myAnimalsName = {lion:"Simba", "tiger":"Tigress", count:2}
> var myVehiclesName = {
    phanter:"Bagheera",
    color:"black"
  }
> myAnimalsName["lion"] // Atribut objek juga bisa diakses dengan sintaks subscript
> myAnimalsName.lion // atau menggunakan sintaks titik (dot) jika kuncinya merupakan identifier yang valid
> myAnimalsName.lion = Mufasa
> myAnimalsName.extra = myVehiclesName
> myAnimalsName.extra.color
```

Selain menggunakan kurung kurawal, objek bisa dibuat menggunakan **constructor function**. Constructor function sama seperti function pada JavaScript pada umumnya, namun function akan di-*instantiate* menjadi objek menggunakan sintaks `new`. Keuntungan membuat objek dari constructor function adalah kita dapat membuat objek yang sama berkali-kali dengan isi yang *value* yang berbeda-beda, sedangkan membuat objek menggunakan kurung kurawal hanya bisa membuat satu objek.

**Contoh Penggunaan Constructor Function**
```javascript
// contoh constructor function
function Human(humanName, humanAge) {
  this.name   = humanName;
  this.age    = humanAge;
  this.talk   = function(otherHumanName) {
    console.log('Hi, ' + otherHumanName + '!');
    console.log('My name is ' +this.name);
    console.log('I am ' + this.age + ' years old');
  }
}

// melakukan instantiate
var mario = new Human('Mario', 34);
var luigi = new Human('Luigi', 32);

console.log(mario.name); // 'Mario'
console.log(luigi.age);  // 32

mario.talk(luigi.name);
// Hi, Luigi!
// My name is Mario
// I am 34 years old
```

Kamu dapat mencoba kode di atas [di sini](http://jsbin.com/rudopup/1/edit?js,console)

Konsep membuat object dari constructor function sama seperti membuat objek dari *class* pada bahasa pemrograman lain. Class adalah sebuah **blueprint** atau abstraksi dari objek, oleh karena itu blueprint masih perlu direalisasikan (di-*instantiate*) agar menjadi sebuah objek. Kita juga bisa membuat objek dengan membuat *class* terlebih dahulu pada JavaScript. Materi *class* akan didapatkan saat kamu mempelajari tentang ES6 pada Week 6.

### JSON

Apa yang sudah kita buat juga merupakan JSON (JavaScript Object Notation) sederhana. JSON itu sendiri adalah format pertukaran data (data-interchange) yang ringan (lightweight), mudah bagi manusia untuk membaca dan menulisnya, mudah juga bagi mesin/komputer untuk mengurai (parse) dan hasilkan (generate). Win win! :star2:

JSON dibasiskan sebagai subset dari JavaScript.
Walaupun berhubungan, JSON adalah format teks yang independen tapi menggunakan konvensi atau aturan yang familiar untuk programmer dari bahasa keluarga C seperti C++, C#, Java, JavaScript, Perl, Python, dan banyak lainnya. Jadi kita bisa gunakan JSON tanpa JavaScript.
Properti ini menjadikan JSON bahasa pertukaran data yang ideal, mampu untuk menyimpan maupun mentransfer/mengirim data ke mana saja. Keren! :sunglasses:

Mari kita ulang sebentar. Seperti object JavaScript, JSON dibuat dengan dua struktur yang mirip:

- Kumpulan/koleksi pasangan nama kunci dan nilai. Dalam beberapa bahasa, ini dibuat sebagai object, record, struct, dictionary, hash table, keyed list, atau associative array. Maka dari itu ada berbagai cara untuk membuat JSON, selain di JavaScript.
- Deretan nilai yang berurutan. Dalam kebanyakan bahasa, bisa dibuat sebagai array, vector, list, atau sequence.

JSON juga merupakan objek biasa yang berisi dua fungsi utama:

- `parse()`: parse atau translate, untuk menerjemahkan atau menganalisis JSON dalam hal in terms of aturan tata bahasa, mengidentifikasi bagian perkataan, hubungan secara sintaks, dll.
- `stringify()`: membuat teks JSON.

Dalam JSON, kita bisa gunakan tipe data apapun juga. Kombinasikan String, Number, Array, dan lainnya. Buatlah nama kunci sebaiknya sebagai String.

```javascript
{
  "animals": [
    {
      "species": "lion",
      "rank": 1,
      "alive": true
    },
    {
      "species": "tiger",
      "rank": 2,
      "alive": true
    },
    {
      "species": "jaguar",
      "rank": 3,
      "alive": false
    },
    {
      "species": "leopard",
      "rank":null,
      "alive":null
    }
  ]
}
```

contoh lain:

```javascript
{
  "id": "1a2b3c",
  "name": "Superman",
  "age": 200,
  "favorites": [
    "coding",
    "reading",
    {
      "sports": ["parkour", "hill climbing"]
    }
  ],
  "address":{}
}
```

Dengan bentuk penulisan seperti di atas, sekarang saatnya kita mencoba membuat contoh object!

```javascript
var supermanObj = {
  id: "1a2b3c",
  name: "Superman",
  age: 200,
  favorites: [
    "coding",
    "reading",
    {
      sports: ["parkour", "hill climbing"]
    }
  ],
  address: {}
};

console.log(supermanObj.name); // "Superman"
console.log(supermanObj.age); // 200
console.log(supermanObj.favorites[0]); // "coding"
console.log(supermanObj.favorites[2].sports); // ["parkour", "hill climbing"]
console.log(supermanObj.favorites[2].sports[0]); // "parkour"
```

Kamu dapat mencoba kode di atas [di sini](http://jsbin.com/cowuvog/1/edit?js,console)

### References

- [JavaScript Objects on W3Schools](http://www.w3schools.com/js/js_objects.asp)
- [Working with objects, on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
- [JSON.org](http://json.org)
- [JSON Parser Online](http://json.parser.online.fr)
