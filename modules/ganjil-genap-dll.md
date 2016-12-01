# Angka Ganjil dan Genap

## Objectives

- Mengaplikasikan Syntax `for`
- Mengaplikasikan Syntax `if-else`

## Directions

1. Buatlah sebuah perulangan 1 - 100 dengan pertambahan indeks sebanyak 1
2. Di dalam perulangan, periksa setiap angka indeks:
    - Apabila angka indeks adalah angka genap, tuliskan **GENAP**
    - Apabila angka indeks adalah angka ganjil, tuliskan **GANJIL**
3. Buatlah 3 perulangan baru dari 1 - 100, dengan pertambahan indeks sebesar 2, 5, dan 9.
4. Pada 3 perulangan baru ini periksa setiap angka indeks:
    - Apabila bukan kelipatan yang ditentukan tidak perlu menuliskan apa-apa
    - Apabila angka indeks adalah kelipatan (pertambahan index + 1), tuliskan:
    - `"[index]" + "KELIPATAN [pertambahan_index + 1]"`


### Contoh output

```javascript
//contoh - ganjil genap
//indeks sekarang = 1,
//output
"GANJIL"
//index sekarang = 2,
//output
"GENAP"
// dan seterusnya :)

//contoh - untuk pertambahan indeks 2
//indeks sekarang = 1, 
//output
"" 
//indeks sekarang = 3, 
//output
"3 KELIPATAN 3" 
// dan seterusnya :)

//contoh - untuk pertambahan indeks 5
//indeks sekarang = 1, 
//output
"" 
//indeks sekarang = 6, 
//output
"6 KELIPATAN 6" 
// dan seterusnya :)

//contoh - untuk pertambahan indeks 9
//indeks sekarang = 1, 
//output
"" 
//indeks sekarang = 10, 
//output
"10 KELIPATAN 10" 
// dan seterusnya :)
```