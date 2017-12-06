# Learn Git and GitHub Basics

## Objectives

Git merupakan tool utama yang pasti akan kamu gunakan setiap hari, sepanjang karirmu sebagai developer. Dengan ini kamu dapat tahu apa saja yang kamu lakukan setiap saat dan berkolaborasi dengan rekan lainnya juga. Anggaplah Git sebagai mesin waktu untuk berbagai kerjaan dan file/folder yang kamu kelola.

Sedangkan GitHub merupakan tempat sekaligus komunitas untuk para developer berbagai code dan berkolaborasi dalam berbagai project software. Bahkan modern ini, profil GitHub dapat menggantikan resume/CV untuk melamar pekerjaan!

Kami ingin untuk kamu nyaman menggunakan Git dan GitHub sesegera mungkin. Semoga kamu juga bakal ketagihan dan bahkan nggak bisa bayangin hidup tanpa Git dan GitHub!

Kini kamu akan melalukan instalasi dan konfigurasi Git di komputermu, mampu menjelaskan dan membedakan Git dan GitHub, serta memahami manfaat dan kekuatan version control system (VCS) atau nama lainnya source code management (SCM).

## Directions

### 1. Pastikan kamu siap akan pakai Git dengan command-line

- ▢ Kamu perlu pengetahuan terminal atau command prompt serta CLI. Kamu harus sudah bisa:
  - ▢ Navigasi ke berbagai directory/folder
  - ▢ Membuat file dan folder baru
  - ▢ Menghapus file dan folder
  - ▢ Melihat berbagai file yang ada di folder
  - ▢ Mengetahui lokasi folder di mana kita berada
  - ▢ Memindahkan file ke berbagai folder
  - ▢ Menyalin file atau folder ke tempat berbeda
  - ▢ Membuka atau mengubah file ke dalam editor teks/code

  Kamu bisa menggunakan referensi dibawah ini untuk mempelajari command line:
  - [Command Line Reference 1](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
  - [Command Line Reference 2](https://www.codecademy.com/learn/learn-the-command-line)
  - [Command Line Reference 3](https://www.learnenough.com/command-line-tutorial)

### 2. Buat akun GitHub

- ▢ Tonton [How to Create a GitHub Account • A Quick Look](https://www.youtube.com/watch?v=ezxRcdJ8glM)
- ▢ [Bergabung ke GitHub di sini](https://github.com/join)
- ▢ Tentukan username kamu yang baik, jelas, mudah diingat dan dibaca; dengan huruf kecil (misalnya `andiruben` atau `andir` atau `aruben`). Kalau bisa, samakan dengan username di Slack.
- ▢ Konfirmasi email akun GitHub di inbox kamu.
- ▢ Kunjungi <https://github.com/settings/profile> lalu lengkapi profil kamu.
- ▢ "Update profile" kamu.

Jika nanti kamu melihat `[USERNAME]`, artinya perlu diganti dengan username-kamu. Misalnya username kamu adalah `andiruben`, berarti `github.com/[USERNAME]` menjadi `github.com/andiruben`.

### 3. Pelajari manfaat Git dan GitHub

Kamu bisa memilih manapun media dan sumber yang kamu mau. Yang penting adalah kamu paham mengapa menggunakan, bagaimana cara pakai, dan apa saja terkait VCS/SCM serta Git dan GitHub.

Membaca beberapa resource berikut:

- [Version Control, by Skillcrush](http://skillcrush.com/2013/02/11/version-control)
- [Git, by Skillcrush](http://skillcrush.com/2013/02/18/git)
- [Get started working with Git, by Skillcrush](http://skillcrush.com/2013/02/20/get-started-working-with-git)
- [Git Beginner's Guide for Dummies, on Backlog](https://backlogtool.com/git-guide/en)
- [git - the simple guide](http://rogerdudler.github.io/git-guide)
- [GitHub For Beginners: Don’t Get Scared, Get Started - ReadWrite](http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1)
- [GitHub For Beginners: Commit, Push And Go - ReadWrite](http://readwrite.com/2013/10/02/github-for-beginners-part-2)
- [Is Git the Same Thing as Github!?, by Andrew McWilliams](https://jahya.net/blog/git-vs-github)

Menonton salah satu playlist video berikut:

- [Playlist Git Basics, by GitHub](https://www.youtube.com/playlist?list=PLg7s6cbtAD165JTRsXh8ofwRw0PqUnkVH)
- [Playlist GitHub & Git Foundations, by GitHub](https://www.youtube.com/playlist?list=PLg7s6cbtAD15G8lNyoaYDuKZSKyJrgwB-)
- [Playlist Belajar Git Version Control System, oleh Sekolah Koding](https://www.youtube.com/playlist?list=PLCZlgfAG0GXATLIO3kp405u6TyFPQ9Kjy)
- [Playlist Apa Itu GitHub, oleh Sekolah Koding](https://www.youtube.com/playlist?list=PLCZlgfAG0GXCtwnagWsUzZum1CFZYqrB5)

Mengikuti tutorial interaktif berikut:

- [Try Git: Git Tutorial, by GitHub](http://try.github.io)

### 4. Lakukan instalasi dan konfigurasi Git dan SSH di komputermu

- ▢ [Ikuti petunjuk "Setting up Git"](https://help.github.com/articles/set-up-git/#setting-up-git). Bisa juga langsung [download Git di situs resminya](https://git-scm.com/downloads)
- ▢ Buka terminal atau command prompt. Khusus di Windows, buka "Git Bash"
- ▢ [Ikuti petunjuk "Generating a new SSH key"](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#generating-a-new-ssh-key)
  - SSH digunakan sebagai pengganti HTTPS saat clone repository. Benefit utamanya adalah lebih aman, serta kita tidak perlu entry username dan password berkali-kali saat push dan pull.
  - Mengapa SSH bukan HTTPS? [Which remote URL should I use?](https://help.github.com/articles/which-remote-url-should-i-use)
  - Kalau terlalu lama mencoba berkutik dengan SSH masih ada masalah, boleh saja pakai HTTPS.

Setelah semua persiapan sudah selesai, kita akan bisa lanjut membuat website sederhana dan menaruhnya gratis dengan GitHub Pages!

## References

**CLI**

- [A Command Line Primer for Beginners, article on Lifehacker](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Learn Enough Command Line to Be Dangerous, book by Michael Hartl](https://learnenough.com/command-line-tutorial)

**Git and GitHub**

- [Official website of Git SCM](https://git-scm.com)
- [GitHub website](https://github.com)
- [Let’s Git Started: A Beginner’s Guide to Version Control Software « Flatiron School](http://blog.flatironschool.com/lets-git-started-a-beginners-guide-to-version-control-software)
- [How to Use Git and GitHub, interactive course on Udacity](https://www.udacity.com/course/how-to-use-git-and-github--ud775)
- [Git Tutorials and Training, by Atlassian](https://www.atlassian.com/git/tutorials)
- [A Beginner’s Git and GitHub Tutorial, on Udacity](http://blog.udacity.com/2015/06/a-beginners-git-github-tutorial.html)
- [Git Tracks on Bento.io](https://bento.io/git)
- [A Guide to Developer Collaboration with GitHub (Ebook)](https://smartbear.com/ppc/ebooks/guide-to-developer-collaboration-with-github)
