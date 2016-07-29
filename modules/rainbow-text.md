# Rainbow Text

## Objectives

- ▢ Memahami DOM dan kaitannya antara HTML, JavaScript, CSS.
- ▢ Mendapatkan objek elemen melalui JavaScript.
- ▢ Mengubah property/attribute pada elemen.
- ▢ Mengetahui API untuk memanipulasi DOM tree.

Mari kita membuat tulisan pelangi dengan cara memodifikasi style pada DOM dengan menggunakan selector JavaScript. Tulisan yang sederetan tiap katanya berubah-ubah warnanya sesuai keinginan kita.

Contohnya seperti ini:

![Tulisan Pelangi](assets/rainbow-text.png)

## Directions

Bukalah Dev Tools, JSBin, atau CodePen bahkan text/code editor untuk mengedit HTML dan JavaScript terlebih dahulu.

### 1. Buatlah tulisan paragraf awal

Masing-masing kata dalam paragraf terpisah menggunakan element `span`.

### 2. Dapatkan semua element `span` dalam paragraf tersebut

### 3. Iterasi tiap element span agar memiliki `style.color` yang beragam

Ragam warna dapat dibuat sebelumnya yang disimpan ke dalam array, ataupun di-generate saat itu juga pada saat melakukan iterasi.

### 4. Gunakan event listener pada suatu tombol

Pergantian warna hanya akan dilakukan pada saat tombol ditekan saja.

**Sebelum diklik:**

![Tulisan Pelangi dengan Button (Sebelum)](assets/rainbow-text-button_before.png)

**Sesudah diklik:**

![Tulisan Pelangi dengan Button (Sesudah)](assets/rainbow-text-button_after.png)

### 5. (Opsional) Buat input form yang dapat memuat berbagai teks

Saat di-submit dengan button, teks tersebut akan dipecah-pecah per-kata, lalu dicetak ke layar dokumen sekaligus diubah warnanya per-kata.

## Submissions

- ▢ Buatlah aplikasi tersebut dalam halaman `rainbow-text.html` pada repo website kamu.
- ▢ Commit dan push file tersebut ke GitHub.
- ▢ Share hasil kamu di Slack.
