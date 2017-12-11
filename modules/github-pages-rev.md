# WEEKLY PROJECT - Website yang dihosting dengan Github Pages

## Objectives

Saatnya membuat website sederhana yang akan ditaruh/di-host secara gratis dengan GitHub Pages. Kamu akan bisa melakukan clone, add, commit, pull, dan push dari/ke GitHub. Website sederhana ini akan kita update secara berkala seiring waktu, yang juga menjadi pusat mengumpulkan berbagai kegiatan yang sudah kamu kerjakan.

**Catatan:** Perlu diketahui dan diingat selalu bahwa website di GitHub Page ini akan kamu gunakan sebagai salah satu bentuk portofolio atau profil online kamu. Jadi, kamu bisa mulai bayangkan dan rancang sebagai website pribadi.

## Directions

### 1. Membuat repositori untuk website di GitHub

- [Sign in ke GitHub](https://github.com/login).
- Buat repositori publik baru dengan format nama `[USERNAME].github.io` dan deskripsi sesukamu.
- Centang "Initialize this project with a README".
- Pilih "Create repository"

Seperti yang telah kamu pelajari, repositori bersifat distributif, yang berarti bisa ada di berbagai komputer sekaligus. Sekarang repositori tersebut hanya ada di GitHub. Untuk menambahkan dan mengedit file/folder, kamu perlu menduplikasikannya ke komputermu. Hal ini disebut cloning repositori ke local. Repositori local adalah copy yang ada di komputer pribadi, sedangkan repositori remote ada di sebuah komputer lain atau server (misalnya GitHub).

### 2. Clone repositori dari GitHub ke local dengan command line

- Di komputermu, bukalah terminal atau command prompt.
- Pindah ke direktori di mana kamu akan menaruh semua repositori. (contoh: `cd Documents/hacktiv8/phase-0/week-1`)
- Copy `GIT HTTPS URL` dari halaman depan repositori. (`https://github.com/[USERNAME]/[USERNAME].github.io`)
- Lakukan `git clone [GIT SSH URL]`. (`git clone https://github.com/[USERNAME]/[USERNAME].github.io.git`)
- Pindah ke direktori hasil clone tersebut. (`cd [USERNAME].github.io`)

### 3. Membuat halaman website sederhana

Oke saatnya beraksi secara lebih nyata!

- Buatlah sebuah project website pribadi kamu dan buatlah ke dalam folder `[USERNAME].github.io`. **Sekarang saatnya kamu mengubah web dan desainnya sesukamu** karena ini akan ditampilkan di web, dan tentunya semakin bagus akan semakin menarik!
- Add file-file tersebut ke Git dengan `git add .` atau `git add -A` (add semua file).
- Commit dengan `git commit -m "Menambah file index.html"`.
- Jika perlu, [ulas lagi alur merekam perubahan ke repositori ](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository).
- Kirim atau push commit pertama kalinya ke GitHub dengan `git push -u origin master`. Perintah push berikutnya bisa cukup dengan `git push` saja.
- Bukalah `[USERNAME].github.io`, lalu saksikanlah halaman website kamu! Selamat! :tada:

Cek kembali `https://github.com/[USERNAME]/[USERNAME].github.io`, kamu dapat melihat file `index.html` yang juga sudah muncul di situ.

### 4. Beritahu website kamu

- Share hasilnya di grup Slack yang memberi tahu kamu sudah punya website dengan URL `http://[USERNAME].github.io`

### 5. Submit di FoxHub

- Submit tugas di platform FoxHub dalam bentuk link menuju github repositori. Contoh: `https://github.com/adhywiranata/adhywiranata.github.io`.

## References

- [GitHub Pages](https://pages.github.com)
- [Build a Web Portfolio from Scratch with GitHub Pages](https://dannguyen.github.io/github-for-portfolios)

**Additional**

- [Publishing your website, BY Mozilla Developer Network](https://developer.mozilla.org/en-US/Learn/Getting_started_with_the_web/Publishing_your_website)
