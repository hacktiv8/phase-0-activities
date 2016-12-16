# Object Math pada JavaScript

## Apa Itu Object Math?

Object Math adalah salah satu *Built-in* Object pada JavaScript yang dapat dipanggil setiap saat untuk membantu melakukan perhitungan matematika. Karena Math adalah sebuah objek, maka didalamnya terdapat *property* dan *method* yang dapat digunakan untuk tujuan tertentu. Adapun untuk menggunakan Math cukup dengan memanggil `Math.property` atau `Math.method(parameter)` secara langsung pada program.

```javascript
var angkaPi    = Math.PI       // angkaPi    = 3.141592653589793
var pangkatDua = Math(4,2)     // pangkatDua = 16
var angkaAcak  = Math.random() // angkaAcak  = [angka acak N, 0 < N < 1]
```

## Property di dalam Math

*Property* dapat disamakan dengan variabel yang dimiliki oleh objek. *Property* yang dimiliki Math adalah berupa nilai-nilai konstanta penting yang sering digunakan untuk perhitungan matematika seperti:

- `Math.PI` (konstanta Pi, ~3.142...)
- `Math.E` (angka Euler, ~2.718)
- `Math.LN2` (logaritma natural dari 2, ~0.693)
- `Math.LN10` (logaritma natural dari 10, ~2.303)
- `Math.LOG2E` (logaritma basis 2 dari E, ~1.443)
- `Math.LOG10E` (logaritma basis 10 dari E, ~0.434)
- `Math.SQRT1_2` (akar pangkat 2 dari 1/2, ~0.707)
- `Math.SQRT2` (akar pangkat 2 dari 2, ~1.414)

## Method di dalam Math

*Method* adalah *function* yang dimiliki oleh suatu objek. Adapun method yang dimiliki Math adalah fungsi yang dapat membantu 'menghitung' suatu perhitungan matematika tertentu sehingga kita tidak perlu membuat kodenya lagi. Berikut beberapa method dari Math yang sering digunakan.

### Math.abs(x)

Mengembalikan angka absolut

```javascript
var absolut = Math.abs(-21,5) // absolut = 21.5

```

### Math.ceil(x)

Mengembalikan angka integer dari pembulatan keatas suatu angka

```javascript
var angka2 = Math.ceil(1.99); // angka2 = 2
var angka1 = Math.ceil(0.1);  // angka1 = 1
var angka0 = Math.ceil(-0.1); // angka0 = 0

```

### Math.floor(x)

Mengembalikan angka integer dari pembulatan kebawah suatu angka

```javascript
var angka3 = Math.floor(3.99); // angka3 = 3
var angka4 = Math.floor(4.01); // angka4 = 4
var angka1 = Math.floor(-0.1); // angka1 = -1

```

### Math.round(x)

Mengembalikan angka integer dari pembulatan suatu angka. Bila angka dibelakang koma >= .5 maka akan dibulatkan keatas dan sebaliknya.

```javascript
var roundUp   = Math.round(3.5);  // roundUp   = 4
var roundDown = Math.round(3.49); // roundDown = 3

```

### Math.trunc(x)

Mengembalikan angka integer dengan menghilangkan angka dibelakang koma.

```javascript
var truncated = Math.trunc(Math.PI) // truncated = 3

```

### Math.max(angka1,angka2,[...],angkaN)

Mengembalikan angka terbesar dari beberapa angka (bukan array).

```javascript
var maxTwo   = Math.max(1,2);   // maxTwo   = 2
var maxThree = Math.max(1,2,3); // maxThree = 3

```

### Math.min(angka1,angka2,[...],angkaN)

Mengembalikan angka terkecil dari beberapa angka (bukan array).

```javascript
var minTwo   = Math.min(4,5);      // maxTwo   = 4
var minThree = Math.min(-1,-2,-3); // maxThree = -3

```

### Math.pow(x, y)

Mengembalikan hasil dari `x pangkat y`

```javascript
var pangkat2 = Math.pow(3,2); // pangkat2 = 9
var pangkat3 = Math.pow(2,3); // pangkat3 = 8

```

### Math.random()

Mengembalikan suatu angka acak ***X***, dimana 0 < ***X*** < 1

```javascript
var random = Math.random(); // random = X, dimana 0 < X < 1

```

## Referensi Lanjutkan

- [Math, by Mozilla Developer Network](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Math)

- [Math Reference, by W3Schools](http://www.w3schools.com/js/js_math.asp)

- [Menghitung Nilai Max/Min dari Array](http://www.jstips.co/en/calculate-the-max-min-value-from-an-array/)
