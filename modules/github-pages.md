# Create Free Website with GitHub Pages

## Objectives

Saatnya membuat website sederhana yang akan ditaruh/di-host secara gratis dengan GitHub Pages. Kamu akan bisa melakukan clone, add, commit, pull, dan push dari/ke GitHub. Website sederhana ini akan kita update secara berkala seiring waktu, yang juga menjadi pusat mengumpulkan berbagai kegiatan yang sudah kamu kerjakan.

**Catatan:** Perlu diketahui dan diingat selalu bahwa website di GitHub Page ini akan kamu gunakan sebagai salah satu bentuk portofolio atau profil online kamu. Jadi, kamu bisa mulai bayangkan dan rancang sebagai website pribadi.

## Directions

### 1. Membuat repositori untuk website di GitHub

- ▢ [Sign in ke GitHub](https://github.com/login).
- ▢ Buat repositori publik baru dengan format nama `[USERNAME].github.io` dan deskripsi sesukamu.
- ▢ Centang "Initialize this project with a README".
- ▢ Pilih "Create repository"

Seperti yang telah kamu pelajari, repositori bersifat distributif, yang berarti bisa ada di berbagai komputer sekaligus. Sekarang repositori tersebut hanya ada di GitHub. Untuk menambahkan dan mengedit file/folder, kamu perlu menduplikasikannya ke komputermu. Hal ini disebut cloning repositori ke local. Repositori local adalah copy yang ada di komputer pribadi, sedangkan repositori remote ada di sebuah komputer lain atau server (misalnya GitHub).

### 2. Clone repositori dari GitHub ke local dengan command line

- ▢ Di komputermu, bukalah terminal atau command prompt.
- ▢ Pindah ke direktori di mana kamu akan menaruh semua repositori. (`cd Documents/hacktiv8/phase-0/week-1`)
- ▢ Copy `GIT SSH URL` dari halaman depan repositori. (`https://github.com/[USERNAME]/[USERNAME].github.io`)
- ▢ Lakukan `git clone [GIT SSH URL]`. (`git clone git@github.com:[USERNAME]/[USERNAME].github.io.git`)
- ▢ Pindah ke direktori hasil clone tersebut. (`cd [USERNAME].github.io`)

Mulai sekarang hingga seterusnya, kami menyarankan untuk kamu mengorganisir folder berdasarkan nomor phase dan pekan.

### 3. Membuat halaman website sederhana

Oke saatnya beraksi secara lebih nyata!

- ▢ Dalam code editormu, buatlah file `index.html` dalam folder `[USERNAME].github.io`.
- ▢ Isilah file HTML tersebut sesukamu kemudian simpan. Bahkan isinya bisa seminimal `<html><body>Hello World!</body></html>`.
- ▢ Add file tersebut ke Git dengan `git add index.html` atau `git add -A` (add semua file).
- ▢ Commit dengan `git commit -m "Menambah file index.html"`.
- ▢ Jika perlu, [ulas lagi alur merekam perubahan ke repositori ](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository).
- ▢ Kirim atau push commit pertama kalinya ke GitHub dengan `git push -u origin master`. Perintah push berikutnya bisa cukup dengan `git push` saja.
- ▢ Bukalah `[USERNAME].github.io`, lalu saksikanlah halaman website kamu! Selamat! :tada:

Cek kembali `https://github.com/[USERNAME]/[USERNAME].github.io`, kamu dapat melihat file `index.html` yang juga sudah muncul di situ.

### 4. Beritahu website kamu

- ▢ Share hasilnya di grup Slack yang memberi tahu kamu sudah punya website dengan URL `http://[USERNAME].github.io`

### 5. (Opsional) Generator

Kamu bisa saja men-generate halaman website pada repositori dengan "Automatic Page Generator" yang terdapat di settings-nya. ( `https://github.com/[USERNAME]/[USERNAME].github.io/settings`). Di situ kamu bisa mengubah konten, memilih tema, kemudian mempublikasikannya

## References

- [Naming files and folders, short guide by University of Leicester](http://www2.le.ac.uk/services/research-data/organise-data/naming-files)
- [Naming Conventions, PDF guide from Harvard](http://library.harvard.edu/sites/default/files/NamingConventions.pdf)
- [GitHub Pages](https://pages.github.com)
- [Build a Web Portfolio from Scratch with GitHub Pages](https://dannguyen.github.io/github-for-portfolios)

**Additional**

- [Publishing your website, BY Mozilla Developer Network](https://developer.mozilla.org/en-US/Learn/Getting_started_with_the_web/Publishing_your_website)
- [Build A Blog With Jekyll And GitHub Pages, by Barry Clark on Smashing Magazine](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages)
