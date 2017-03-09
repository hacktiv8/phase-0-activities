# Menggunakan Object dalam JavaScript 1

JavaScript mendukung konsep pemrograman berorientasi objek. Untuk melatih pemahaman kamu tentang Object pada JavaScript, kerjakanlah tantangan ini dengan baik :smile:

## Objectives

1. Mengerti Cara Membuat Object dengan Syntax `function()`
2. Mengerti Cara Mengakses Property dalam Object
3. Mengerti Cara *Assignment* Property dalam Object
4. Mengerti Tentang Method di dalam Object

## Directions

- Buatlah sebuah object **Mobil** seperti contoh di bawah ini

```javascript
var Mobil = function() {
}
```

- **Mobil** menerima parameter `pabrikan`, `model`, dan `warna`.
- Simpan parameter-parameter tersebut pada *property* dengan nama yang sama
    - hint: `this`
- Buatlah sebuah method di dalam **Mobil** dengan nama `maju()`. Method ini menuliskan seperti yang dicontohkan dibawah.
    - hint: gunakan property dari object

```javascript
var mobilku = new Mobil('Tesla', 'Ludicrous', 'Merah');
mobilku.maju();
//output: Mobil Tesla Ludicrous Merah , bergerak maju!
```

- Di akhir kodemu, uji coba dengan meletakkan potongan kode berikut

```javascript
var mobil1 = new Mobil('Honda', 'Accord', 'Hitam');
var mobil2 = new Mobil('Honda', 'Civic', 'Silver');

console.log('Mobil 1 adalah ' + mobil1.pabrikan + ' ' + mobil1.model + ' ' + mobil1.warna);
mobil1.maju();
mobil1.warna = 'Silver';
mobil1.maju();
console.log('Mobil 2 adalah ' + mobil2.pabrikan + ' ' + mobil2.model + ' ' + mobil2.warna);
mobil2.maju();
```

- Apabila keluaran dari program-mu seperti di bawah ini, selamat! kamu sudah menyelesaikan tantangan ini dengan baik :smile:

```
Mobil 1 adalah  Honda Accord Hitam
Mobil Honda Accord Hitam , bergerak maju!
Mobil Honda Accord Silver , bergerak maju!
Mobil 2 adalah Honda Civic Silver
Mobil Honda Civic Silver , bergerak maju!  
```

### Important Keywords

- Property: variabel di dalam Object
- Method: function di dalam Object
