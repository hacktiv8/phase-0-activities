# JavaScript Data Types

## Objectives

Tipe data ataupun struktur data adalah konsep penting dalam mengkategorisasikan beberapa hal/jenis berbeda pada unit, pengukuran, juga memungkinkan kita untuk beroperasi pada variabel.

Standar ECMAScript terbaru mendefinisikan tipe data berikut:

- `null`: Keyword spesial yang menunjukkan nilai `null`, tidak sah atau tiada. Karena ada aturan case sensitive, `null` tidak sama dengan `Null`, `NULL`, atau varian lainnya.
- `undefined`: Properti tingkat teratas yang nilainya tidak terdefinisi (`undefined`).
- Number: nilai integer (bulat) atau desimal
- String: kumpulan karakter yang dapat berupa huruf saja atau kata atau kalimat
- Boolean: pernyataan `true` dan `false`
- Arrray: sekumpulan nilai data yang dimuat ke dalam satu variabel
- Symbol (baru di ES6): instansi (instance) yang unik dan tidak dapat berubah (immutable).
- Object, dengan JavaScript Object Notation (JSON)

Kita harus senantiasa memahami perbedaan kegunaan antara tipe data tersebut sesuai keadaan dan kebutuhan.

## Learnings

### Angka (Number)

Angka tentu saja tipe paling populer di dunia, semua bahasa pemrograman pasti dapat mengolah angka. Mari kita coba melakukan matematika dasar! Kita bisa gunakan console sebagai kalkulator sederhana yang memanfaatkan nilai dengan tipe data angka dan operator matematis seperti plus `+`, minus `-`, multiply `*`, divide `/`, modulus `%`, increment `++`, decrement `--`. Beberapa bahkan nilai spesial yang bukan angka sungguhan.

```javascript
> 8
> -8          // negative
> 8.00        // decimal
> 3 + 5       // addition
> 2 * 5 - 2   // multiple operation
> 2 * (1 + 3) // with parenthesis
> -88 * 1.23  // fractional
> 8 % 6
> 8 % 2+      // beware!
> 1e8 * 8     // amazing exponent
> 7++
> (9--)
> ++7         // watch out!
> 4 + 3++     // what!?
> 3+ +5       // wow!
> 5- -3
> 0/1
> 1/0         // Infinity
> -1/0        // -Infinity
> 0/0         // NaN // Not a Number
```

Berhati-hatilah beberapa statement tidak dapat dijalankan atau akan menghasilkan error karena melanggar aturan matematis ataupun sintaks.

### String (Deretan)

String (seringkali untuk Text) dapat berisi rankaian karakter alfanumerik (lowercase `a` to `z`, uppercase `A` to `Z`, number `0` to `9`, symbol `!` to `*`, dll) yang berguna untuk mengkomunikasikan informasi polos (plain)
Kita perlu tanda petik (single quote `'` atau double quote `"`) yang membungkus teks untuk menjadikanya sebuah String. Kita bisa menggunakan kedua jenis quote dan mencampurnya, tapi sebaiknya konsisten saja untuk menggunakan salah satu. Kita bisa juga pakai operator dasar yang sebelumnya digunakan untuk angka untuk mengolah String.

```javascript
> "Hello again!"
> "Hello, " + "human!"
> 'Hello, ' + 1 + ' another human!!'
> "Hello, ", "human!!!"
> console.log("Hello, ", "human!!!")
> 10 * 10 + " seconds " + "to launch!"
> "It's the rocket series " + 10 * 10 + " that was damaged " + 1 + 1 + " hour ago!"
> "\"Can we go home now?\", asked him."
> "How long is this String?".length
```

Apa yang terjadi jika digunakan operator plus atau bahkan tanda koma (`,`) adalah perangkaian String (concatenation), menggabungkan beberapa String bersama. Dalam String kita bisa gunakan tanda petik yang berbeda berganti-ganti, atau jika ingin mereka bisa digunakan bersama, gunakan karakter pembatal/escape (`\`). Yang lucu di JavaScript adalah bagaimana angka dan string diperlakukan bersama sesuai dengan precedence dan urutannya. Bahkan karena `var` tipe data menjadi dinamis, dapat diganti kapanpun.

```javascript
> var a        // undefined
> a = 8        // Number
> a = "Eight"  // String
> a = ""       // empty value but still a String
```

Baru saja variabel `a` berganti dari tipe data angka menjadi string. Seperti `\n`, ada beberapa karakter spesial yang bisa digunakan dalam string. Mereka memiliki escape character.

```
\0	Null Byte
\b	Backspace
\f	Form feed
\n	New line
\r	Carriage return
\t	Tab
\v	Vertical tab
\'	Apostrophe atau single quote
\"	Double quote
\\	Backslash character
```

Untuk karakter yang tidak terdapat di tabel, garis miring ke belakang (backslash) akan diabaikan, walau cara ini sebaiknya dihindari karena sudah usang (deprecated)
Namun dengan ES6, kita bisa gunakan template literal untuk membuat literal string dan penyisipan (interpolation) string. Yang mana akan memudahka nkita memiliki string yang diformat tanpa escape character. Hal tersebut menyajikan fitur tambahan dalam menggunakan sintaks untuk membuat string. Mirip dengan fitur interpolasi string yang ada di berbagai bahasa pemrograman modern. Sintaks ini menggunakan simbol `.

```javascript
> `"Earth's day is coming tomorrow", he said.\n"Let's prepare!"`
> var creature="human", task="coding", days=5
> `Hello ${creature}, will you be ${task} in ${days} days?`
> `Good work,
  let's go beyond!	Yay!`
```

Dapat terlihat kita bisa memasukkan nilai variabel secara langsung dalam string.

### Boolean

Layaknya "pagi dan malam", "satu dan nol", ada "benar (true) dan salah (false)". Kita bisa artikan juga sebagai "ya dan tidak" atau "nyala (on) dan mati (off)". Dua nilai yang kontras satu sama lain.

```javascript
> true
> false
```

Tunggu, begitu doang kayaknya ga berguna ya? Baiklah mari kita coba lagi menggunakan beberapa operator yang kita tahu dapat menghasilkan nilai boolean.

```javascript
> 1 == 1
> 1 === 1
> 1 == 2
> 2 != 1
> 2 >= 1
> "B" > "A"
> !true
> true === !false
> confirm("Are you sure?")
```

Yang terakhir bahkan merupakan dialog yang pengguna bisa pilih dan mengembalikan (return) nilai `true` atau `false`.

### Array

Array adalah kumpulan dari berbagai data. Kita bisa tulis dengan kurung kotak (square brackets) dan butir-butirnya dipisah dengan koma. Indeks array berbasis-nol yang berarti urutan awalnya merupakan `[0]`, keduanya `[1]`, dan seterusnya.
Kita juga bisa memasukkan (insert), memperbarui/mengubah (update/change), atau bahkan meniadakan (undefine) nilai yang ada di dalam array. Spesifik di JS, kita bisa gunakan beberapa tipe data berbeda di dalam suatu array. Bahkan memasukkan array ke dalam array!

```javascript
> var animals = ["Lion", "Tiger", "Puma"]
> animals
> animals[0]
> animals[3] = "Jaguar"
> animals[8] = "Leopard"
> animals[1] = undefined
> animals
> animals[5]
> animals[0] = 100
> animals[1] = true
> animals
> animals[3] = ["Zero", 1, "Two"]
> animals[3][3] = "Three"
```

Array seperti tumpukan data. Bayangkan sebuah botol atau toples yang berisi beberapa lapis biskuit di dalamnya. Kita bisa mendorong (push) seperti memasukkan yang baru, mengeluarkan (pop) yang paling terakhir atau teratas, atau bahkan mengambil beberapa lapis data.

```javascript
> animals.push("Dragon")
> animals.pop()
> animals.slice(0, 2)
```

## References

- [JavaScript (Original) on Codecademy](https://www.codecademy.com/en/tracks/javascript-original)
- [JavaScript on Codecademy](https://www.codecademy.com/learn/javascript)
- [JavaScript on Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Belajar javascript untuk pemula, di Sekolah Koding](https://sekolahkoding.com/kelas/belajar-javascript-untuk-pemula)
- [Data type, article on Wikipedia](https://en.wikipedia.org/wiki/Data_type)
