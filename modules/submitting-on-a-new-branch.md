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

   ![Pull Request](https://lh5.googleusercontent.com/g54bSlL0yK1Y0OVcUFeSeOGtbCGTuJ042t2hDjFyE2ilVHp3Lezj8y91XtsH0VzPix5KrUMVZqQjiQALQz4i=w3360-h1760-rw "Pull Request")

6. Tambahkan message dan klik button `Create pull request`

   ![Create Pull Request](https://lh6.googleusercontent.com/Etr9M-RNc0xbnvqskK615m7UXwBBooiP_k_xrgKAGxfaZAn4k8AmBKNzghryFHqhyI_3eQdnM0n9VFyXemXE=w3360-h1760-rw "Create Pull Request")

7. Selesai! Jika kamu sudah melakukan step ke-8, maka akan redirect ke halaman ini

   ![Done](https://lh5.googleusercontent.com/MwTXxobK1mlev4X96ujHiHPmjSwFM8BIVRLnjtytGnFq7vs4jSKMx3TuDpKihxQakz8fhqebsBRR0lmo9E3u=w3360-h1760-rw "Done")
