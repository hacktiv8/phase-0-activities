# Challenge !! Promo credit card

## Objectives

Hari ini kita akan mengembangkan lagi task yang telah dibuat sebelumnya, oleh karena itu, task yang kemarin harus diselesaikan juga :bowtie:.

## Tugas
1. Buatlah method baru bernama ccBilling (boleh copy dari method promoBilling kemarin)
2. Saat ini restaurant memiliki promo tambahan, KHUSUS pembayaran menggunakan credit card, hari senin - jumat semua makanan diskon 25% dan hari sabtu-minggu semua makanan diskon 50% ! <br>
Masukan data order sbb : <br>
1 nasi goreng <br>
1 teh <br>
2 jus buah <br>
3. Buatlah sebuah function yang dapat menerima parameter hari.
3. Setelah selesai, kirim hasil code kamu dengan gist, dengan nama file : ccBilling.js. Share gist kamu melalui private message slack ke instructor yang sedang in charge.

## Example
Pesanan Customer : 1 nasi goreng, 1 teh, 2 jus buah.
Cek dahulu metode pembayaran customer apakah cash atau credit card?
Buatlah function yang dapat menghasilkan total nya dengan benar dari berbagai kondisi !

## Output
Ketika code Js kamu di run, akan menghasilkan seperti ini di console :
```
  "add order : nasi goreng"
  "add order : teh"
  "add order : jus buah"

  "daftar pesanan : "
  "1 nasi goreng"
  "1 teh"
  "2 jus buah"
  
```

Apabila hari senin - jumat :
```
  "total setelah promo weekdays : 73750"
```

Apabila hari sabtu / minggu :
```
  "total setelah promo weekend : 67500"
```
