# Change Text Style with Event Listener

## Objectives

- ▢ Mengoptimalkan code kita menggunakan event listener daripada menggunakan event handler tradisional sebelumnya.
- ▢ Memasang function pada event listener.
- ▢ Mendapatkan objek event dan mengolahnya.
- ▢ Menempatkan listener tergantung konteksnya.

Context menu yang akan kita buat sesederhana untuk mengubah gaya font pada text yang kita klik. Ditampilkan seperti berikut.

Keadaan sebelum:

![Style sebelum](assets/style-event.png)

Setelah diklik kiri:

![Style klik kiri](assets/style-event_left.png)

Setelah diklik kanan:

![Style klik kanan](assets/style-event_right.png)

## Directions

Bukalah Dev Tools, JSBin, atau CodePen bahkan text/code editor untuk mengedit HTML dan JavaScript terlebih dahulu.

### 1. Buatlah berbagai teks/tulisan yang kamu mau

Bisa pakai `h1`, `p`, `span`, ataupun `button`.

### 2. Buatlah event listener untuk elemen tersebut

Event listener akan beraksi jika ada klik kiri (`click`/`mousedown`) dan klik kanan (`contextmenu`). Bisa juga memberi event listener pada element yang berbeda. Jadi misalnya tombol memiliki event yang dapat mengganti sifat element tulisan.

### 3. Buat fungsi untuk mengganti style

Di baris sebelum menambah event listener, buatlah fungsi untuk mengganti style dari tulisan, misalnya `makeBold()` dan `makeItalic()`.

### 4. Cek fungsionalitas program

Cobalah untuk klik kanan dan kiri untuk mengubah tulisan tersebut

## Submissions

- ▢ Buatlah aplikasi tersebut dalam halaman `text-style-event.html` pada repo website kamu.
- ▢ Commit dan push file tersebut ke GitHub.
- ▢ Share hasil kamu di Slack.
