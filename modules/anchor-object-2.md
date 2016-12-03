# Menggunakan Object dalam JavaScript 2

Terkadang suatu method dari object tidak menerima parameter berupa data biasa, object juga dapat dijadikan argumen untuk method (atau function biasa). Pada tantangan ini kamu akan membuat suatu object untuk semacam permainan peran (role play game) sederhana. Object akan memiliki method yang menerima object.

## Objectives

1. Memahami Cara Membuat Object dengan Syntax `function()`
2. Memahami Cara Mengakses Property dalam Object
3. Memahami Cara *Assignment* Property dalam 
4. Memahami Cara Membuat Method untuk Object
5. Mengetahui Passing Argument Berupa Object

## Directions

- Buatlah sebuah object **Teman** seperti contoh di bawah ini

```javascript 
var Teman = function() {
}
```

- **Teman** menerima parameter `nama`, `kabar`, dan `pekerjaan`.
- Simpan parameter-parameter tersebut pada *property* dengan nama yang sama
- Buatlah method `sapa()`, method ini menerima parameter string nama dan akan menuliskan

> Halo `<parameter>` , apa kabar?

- Buatlah method `balasSapa()`, method ini menerima parameter string nama dan akan menuliskan

> Halo `<parameter>` , kabarku `<property kabar>`

- Buatlah method `tanyaPekerjaan()`, method ini tidak menerima parameter dan akan menuliskan

> Apa pekerjaanmu saat ini?

- Buatlah method `balasPekerjaan()`, method ini tidak menerima parameter dan akan menuliskan

> Pekerjaanku saat ini adalah `<property pekerjaan>`

- Terakhir, buatlah method `berpisah()`, method ini menerima parameter berupa Object Teman dan akan menuliskan

> Senang bertemu denganmu `<parameterObject.nama>` , semoga kamu sukses sebagai `<parameterObject.pekerjaan>`

- Untuk menguji kebenaran implementasi object-mu, gunakan **test case** di bawah dengan cara menambahkannya diakhir program. Apabila keluaran program-mu seperti **output**, selamat! kamu sudah menyelesaikan tantangan ini dengan baik! :smile:


### Test Case

```javascript
var budi = new Teman('Budi', 'baik', 'developer');
var tono = new Teman('Tono', 'baik', 'chef');

budi.sapa(tono.nama);
tono.balasSapa(budi.nama);
budi.tanyaPekerjaan();
tono.balasPekerjaan();
budi.berpisah(tono);
```

### Output

```
Halo Tono, apa kabar?
Halo Budi, kabarku baik
Apa pekerjaanmu saat ini? 
Pekerjaanku saat ini adalah chef
Senang bertemu denganmu Tono, semoga kamu sukses sebagai chef
```
