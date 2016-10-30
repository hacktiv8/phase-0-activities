# Membuat ES6 Class Sederhana

## Objectives

- Mampu memanfaatkan Class pada ES6 untuk membangun object JavaScript

## Directions

1. Ubah kasus dibawah ini ke dalam bentuk ES6 Class.

### Tugas 1

Buatlah sebuah Class Fox, yang memiliki atribut berupa name, species (Arctic, Blandford, Cross, Darwin, dan lain-lain), age, dan gender. Buatlah constructor jadi kita akan memasukkan name, species, age, dan gender pada saat kita membuat instance baru (`new`).

Kemudian, buat 3 instance dari class Fox tersebut, dan cobalah akses nama, spesies, umur, dan jenis kelamin masing-masing.

Contoh Output:

```JavaScript
> Fox Name: Mike, Species: Arctic Fox, Age: 10, Gender: Male
> Fox Name: Diane, Species: Blandford Fox, Age: 12, Gender: Female
> Fox Name: Rowan, Species: Cross Fox, Age: 8, Gender: Male
```

### Tugas 2

Buatlah sebuah Class Student, yang memiliki atribut berikut:
- Name,
- Age,
- Date of Birth,
- Gender
- Student ID (bisa berupa angka atau teks), dan
- Hobbies (bisa menampung lebih dari 1 hobi).

Class tersebut juga bisa memanggil fungsi dengan proses sebagai berikut:
- SetName: mengubah nama student dengan mengirimkan satu parameter ke dalam fungsi berupa teks
- SetAge: mengubah nama student dengan mengirimkan satu parameter ke dalam fungsi berupa angka
- SetDateOfBirth: mengubah nama student dengan mengirimkan satu parameter ke dalam fungsi berupa teks
- SetGender: mengubah nama student dengan mengirimkan satu parameter ke dalam fungsi berupa teks, dan hanya bisa menerima nilai `Male` atau `Female`
- addHobby: menambah hobi dengan mengirimkan satu parameter ke dalam fungsi berupa teks
- removeHobby: menghapus list hobi yang ada dengan mengirimkan satu parameter berupa teks, yang merupakan hobi apa yang akan dihapus
- getData: menampilkan seluruh data atribut murid
