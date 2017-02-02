# :rocket: Proxytia to Next Level

## Objectives

- Mampu menggunakan variabel dengan benar
- Mampu melakukan operasi aritmatika pada JavaScript
- Mampu mengimplimentasikan perulangan menggunakan `for` atau `while`
- Mampu mengimplimentasikan `if-else if-else` dan mengerti logikanya

## Directions

Masih ingat dengan Proxytia? game yang pernah kamu buat pada tugas sebelumnya. Pada *challenge* kali ini kamu ditantang untuk mengembangkan game ini lebih lanjut. Ada beberapa perubahan yang akan perlu kamu lakukan agar game ini dapat dimainkan. Perhatikan langkah-langkahnya sebagai berikut:

1. Tambahkan variabel `tahunLahir`, variabel ini akan diisi dengan tahun lahir pemain.
2. Isi variabel umur sekarang adalah `2017 - tahunLahir`.
3. Tambahkan variabel `playerHealth`, *assign* variabel ini dengan `tahunLahir X Math.random()`
4. Tambahkan variabel `monsterHealth`, *assign* variabel ini dengan `tahunLahir X Math.random()`
5. Tambahkan variabel `kodeMonster`, *assign* variabel ini dengan `Math.floor(Math.pow(100, Math.random()))`
6. Pada logika `if` terhadap variabel `nama`, apabila pemain tidak mengisi variabel, *assign* variabel `peran` dengan **kacung**
7. Setelah semua pengecekan menggunakan `if` selesai dilakukan, lakukan perulangan sebanyak `tahunLahir`.
8. Di dalam perulangan tersebut, buat sebuah logika `if-else` untuk melakukan pengecekan sebagai berikut:
    * jika indeks perulangan adalah kelipatan `umur`:
        - `console.log(peran + ' ' + nama + ' menyerang monster!')`
        - Kurangi `monsterHealth` dengan `umur`
    * jika indeks perulangan adalah kelipatan `kodeMonster`:
        - `console.log('monster menyerang ' + peran + ' ' + nama + '!')`
        - Kurangi `playerHealth` dengan `kodeMonster`
    * jika indeks perulangan adalah kelipatan `umur` dan `kodeMonster` sekaligus:
        - `console.log('Health keduanya bertambah')`
        - Tambahkan `playerHealth` dengan `kodeMonster`
        - Tambahkan `monsterHealth` dengan `umur`
9. Jika `playerHealth` lebih besar daripada `monsterHealth`:
    * `console.log('Selamat, ' + peran + ' ' + nama + ' memenangkan pertarungan!')`
    * Jika sebaliknya, `console.log('Sayang sekali, ' + peran + ' ' + nama +  ' dikalahkan monster...')`
