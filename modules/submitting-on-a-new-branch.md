# Submit Exercise lewat Git Branch

1. Clone repository tugas yang ingin kamu kumpulkan, contoh ini akan menggunakan repository Damage Calculation

2. Buatlah branch baru dengan menjalankan perintah berikut:
   ```
   git checkout -b <nama_kamu>
   ```
   Contoh:
   ```
   git checkout -b dimitri-wahyudiputra
   ```
3. Check terlebih dahulu apakah kamu sudah masuk ke branch baru dengan memasukkan perintah berikut:
   ```
   git status
   ```
   Yang akan menampilkan output seperti ini:
   ```
   On branch <nama_kamu>
   nothing to commit, working tree clean
   ```
4. Kerjakan tugas Damage Calculation di branch ini dan jika sudah selesai, lakukan `git add` dan `git commit` seperti yang kalian biasa lakukan.

5. Jalankan perintah untuk melakukan push ke branch kamu
   ```
   git push origin <nama_kamu>
   ```

6. Lakukan `Pull Request` dari halaman repository damage-calculation-git dengan cara klik tombol `Compare & pull request`

   ![Pull Request](https://lh4.googleusercontent.com/PwhWPoPc3CLJ5YQmhrFKcgARSv5Ssup50QSvlzkRU1XtWS_j4ItqvCpEUgwrr4dvEiEWMTCCUslluMu5mU58=w3360-h1760-rw "Pull Request")

6. Tambahkan message dan klik button `Create pull request`

   ![Create Pull Request](https://lh4.googleusercontent.com/UkzoIvZlKk6lWn4LCnJ9Jz2jboDWZ7QnrBJ0ihPEt-qg19-8jXht7dIciPFID91nLcZFh6ehGWqbzlEe1N2a=w3360-h1760-rw "Create Pull Request")

7. Selesai! Jika kamu sudah melakukan step ke-8, maka akan redirect ke halaman ini

   ![Done](https://lh4.googleusercontent.com/UkWMAeq-K5Wmmpz1In1Oj4ywKmBh-7qkIllcro54-nOfuE2CbKEKjC21u6HEyJSAJHxHz6ezixl86q3JeLA4=w3360-h1760-rw "Done")
