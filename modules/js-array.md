# JavaScript Data Types

## Objectives

Tipe data ataupun struktur data adalah konsep penting dalam mengkategorisasikan beberapa hal/jenis berbeda pada unit, pengukuran, juga memungkinkan kita untuk beroperasi pada variabel.

## Learnings

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
