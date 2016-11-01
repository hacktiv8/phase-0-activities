# Learn the Basics of HTML Forms

## Objectives

- ▢ Mengulas dasar-dasar HTML forms.

## Learnings

Form pada HTML adalah satu dari banyak cara untuk berinteraksi di sebuath website atau web app dengan pengguna (users). Dengan cara ini, pengguna dapat memasukkan (input) beberapa teks atau data/informasi yang dibutuhkan oleh pemilik website, kemudian diproses atau diterima oleh form tersebut, yang pada akhirna dikirim ke server. Sering juga dapat menghasilkan keluaran (output) yang dihasilkan oleh server dan form secara bersamaan. Kadang data tesebut bisa diatur oleh form tanpa bantuan server.

Form tidak dapat berdiri sendiri, butuh berbagai elemen penyusun yang bisa juga disebut widget; seperti text fields (satu atau beberapa baris), label, select box, button, radio button, checkbox, datalist, option dan lain sebagainya. Kebanyakan masukan/input memerlukan label agar lebih jelas data apa yang harus kita masukkan.

Ada beberapa elemen yang dapat bekerja dengan `form`:

- `fieldset`: kumpulan atau koleksi input field yang memiliki tujuan yang sama
  - `legend`: penjelasan tentang simbol atau elemen form, seperti label untuk `fieldset`
  - `label`: penjelasan pada widget spesifik, label untuk `input`
  - `input`: kontrol interaktif (interactive controls) dengan berbagai tipe atribut seperti:
    - text
    - number
    - url
    - email
    - tel (telephone)
    - password
    - file
    - range
    - date
    - time
    - datetime
    - button
  - `textarea`: beberapa baris text input
  - `button`: tombol aksi (action button) yang bisa diklik, untuk menginformasikan melalukan sesuatu selanjutnya
  - `select`: select box atau combo box, kolom untuk memilih satu atau lebih nilai (value) yang sudah didefinisikan
  - `datalist`: daftar dari data atau nilai yang telah diatur (list of preset data or values), biasanya juga untuk text field
  - `optgroup`: kumpulan pilihan (options)
    - `option`: pilihan yang dapat dipilih pengguna

Biasanya, form memiliki atribut aksi (action) dan metode (method) agar dapat bekerja dengan baik. Kita akan membahas ini lebih lanjut jika sudah terbiasa. Untuk sementara waktu, kita cukup mempelajari HTML saja tanpa berinteraksi dengan sebuah server.

```html
<form action="/api/contact" method="post">
  <!-- form elements -->
</form>
```

Inilah beberapa contoh kode yang dapat membantu kamu membuat formulir kontak.

### Form dengan fieldset, legend, label, dan berbagai input

```html
<form>
  <fieldset>
    <legend>Personal Information</legend>
    <p>
      <label for="full-name">Full Name</label>
      <input name="full-name" type="text">
    </p>
    <p>
      <label for="email">Email Address</label>
      <input name="email" type="email">
    </p>
  </fieldset>
  <fieldset>
    <legend>Work Information</legend>
    <!-- some other inputs -->
  </fieldset>
</form>
```

### Form dengan label, input, dan beberapa daftar/list data

```html
<form>
  <p>
    <label for="programming">Your preferred programming languages?</label>
    <input type="text" name="programming" list="programmingLangs" />
    <datalist id="programmingLangs">
      <label for="suggestion">or pick one</label>
      <select id="suggestion" name="altProgrammingLangs">
        <option value="javascript">JavaScript</option>
        <option value="java">Java</option>
        <option value="ruby">Ruby</option>
        <option value="python">Python</option>
      </select>
    </datalist>
  </p>
</form>
```

### Form dengan radio button

```html
<form>
  <label for="gender">Gender:</label>
  <input type="radio" name="gender" value="male">Male
  <input type="radio" name="gender" value="female">Female
</form>
```

### Form dengan masukan tombol di akhir

```html
<form>
  <label for="skill">Skill:</label>
  <input type="checkbox" name="skill" value="writing">Writing
  <input type="checkbox" name="skill" value="reading">Reading
  <input type="submit" value="Submit">
</form>
```

## References

- [Learn to Code HTML & CSS, by Shay How](http://learn.shayhowe.com/html-css/building-forms) (lesson 10: Building Forms)
- [Forms in HTML, by MDN](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms_in_HTML)
- [HTML5 forms introduction and new attributes, on HTML5 Doctor](http://html5doctor.com/html5-forms-introduction-and-new-attributes)
- [Making Forms Fabulous with HTML5, on HTML5 Rocks](http://www.html5rocks.com/en/tutorials/forms/html5forms)
- [HTML5 - Web Forms 2.0, on TutorialsPoint](http://www.tutorialspoint.com/html5/html5_web_forms2.htm)
- [Design Better Forms, by Andrew Coyle on UXDesign.cc](https://uxdesign.cc/design-better-forms-96fadca0f49c)
