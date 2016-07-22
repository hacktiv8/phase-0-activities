# JavaScript Object and JSON

## Objectives

- ▢ Memahami pembuatan dan kegunaan pasangan key-value dalam sebuah object.
- ▢ Memahami JSON dan perbedaannya dengan object biasa.

## Learnings

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

Dalam JSON, kita bisa gunakan tipe data apapun juga. Kombinasikan String, Number, Array, dan lainnya. Buatlah nama kunci sebaiknya sebagai String. (Catan: Kita akan hilangkan tanda `>` dari sekarang, karena kebanyakan kode akan menjadi beberapa baris)

```javascript
{
"animals": [
  { "species":"lion", "rank":1, "alive":true },
  { "species":"tiger", "rank":2, "alive":true },
  { "species":"jaguar", "rank":3, "alive":false },
  { "species":"leopard", "rank":null, "alive":null }
]
}
```

contoh lain:

```javascript
{"id":"1a2b3c","name":"Superman","age":200,"favorites":["coding","reading",{"sports":["parkour","hill climbing"]}],"address":{}}
```

### References

- [JSON.org](http://json.org)
- [JSON Parser Online](http://json.parser.online.fr)
