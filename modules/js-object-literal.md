# JavaScript Object Literal

## Objectives

- ▢ Memahami pembuatan object sebagai pair key: value tanpa menggunakan class

### Object

JavaScript merupakan bahasa pemrograman yang berbasis simple-object (Objek sederhana). Objek adalah kumpulan tidak berurut yang merangkai beberapa property dan property memiliki nama/key dan value (key-value pairs).

Objek dalam JavaScript, sama seperti banyak bahasa pemrograman lainnya, bisa dibandingkan dengan objek dalam kehidupan nyata.

Untuk membuat sebuah object literal bisa dengan cara menuliskan kurung kurawal (curly braces) kemudian menuliskan nama property yang harus memiliki keyName dan value.

```javascript
var myObj = {
  myKey: 'myValue'
};
```


Value dalam object literal selain string bisa juga dengan memasukkan value array bahkan value object literal lainnya.

Kita bisa coba dengan kode berikut:

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
  address: {
    street: "Planet Krypton",
    zipCode: 54213
  }
};

console.log(supermanObj.name); // "Superman"
console.log(supermanObj.age); // 200
console.log(supermanObj.favorites[0]); // "coding"
console.log(supermanObj.favorites[2].sports); // ["parkour", "hill climbing"]
console.log(supermanObj.favorites[2].sports[0]); // "parkour"
console.log(supermanObj.address); // {street: "Planet Krypton", zipCode: 54213}
console.log(supermanObj.address.zipCode); //54213
```

Kamu dapat mencoba kode di atas [di sini](http://jsbin.com/diruxiq/edit?js,console)

<!-- ### BONUS: JSON

JSON adalah format pertukaran data (data-interchange) yang ringan (lightweight), mudah bagi manusia untuk membaca dan menulisnya, mudah juga bagi mesin/komputer untuk mengurai (parse) dan hasilkan (generate). Win win! :star2:

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
``` -->



### References

- [JavaScript Objects on W3Schools](http://www.w3schools.com/js/js_objects.asp)
- [Working with objects, on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
<!-- - [JSON.org](http://json.org)
- [JSON Parser Online](http://json.parser.online.fr) -->
