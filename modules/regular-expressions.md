# Explore Regular Expressions!

## Objectives

Regular Expressions adalah ...
Regular Expressions, atau disingkat menjadi Regex, di kalangan programmer, kadang dianggap menjadi satu hal yang sangat menyeramkan, dikarenakan nature mereka yang membuat kita harus menghapal berbagai simbol yang tersusun dengan sangat abstrak. Namun, pada saat kita telah mampu menulis pattern regex kita sendiri, akan sangat mudah memahaminya. Kamu tidak mau kan, harus meng-googling setiap pattern regex dan mencoba satu per satu?


- ▢ Mengetahui Kegunaan Regular Expressions
- ▢ Memahami simbol-simbol yang digunakan pada Regular Expressions

## Learnings

### Mengetahui Kegunaan Regular Expressions

Kuncinya untuk memahami Regular Expressions adalah mampu menghapal simbol-simbol dibawah ini, beserta kegunaannya. Untuk memudahkanmu, kamu bisa mencatat, membuat semacam cheatsheet, atau membuat jembatan keledai dengan caramu sendiri untuk memudahkanmu.

. - Mencocokan karakter apapun, kecuali line breaks(jeda baris/enter).
* - Mencocokan 0 atau lebih dari karakter terdahulu.
+ - Mencocokan 1 atau lebih dari karakter terdahulu.
? - Karakter terdahulu menjadi opsional. Mencocokan 0 atau 1.
\d - Mencocokan digit apapun
\w - Mencocokan karakter pada sebuah kata (alphanumeric dan underscore/garis bawah).
[XYZ] - Matches any single character from the character class.
[XYZ]+ - Matches one or more of any of the characters in the set.
$ - Mencocokan ujung dari sebuah string.
^ - Mencocokan awal dari sebuah string.
[^a-z] - Ketika didalam sebuah class karakter, tanda ^ artinya NOT; dalam kasus ini, regex akan mencocokan apapun yang bukan karakter lowercase.

### Mengetest Kemampuan Regular Expressions

Ada sebuah platform yang cocok untuk melatih kamu dalam menggunakan regex, yaitu [regexr.com](http://regexr.com/)

## References

- [HTML, CSS & JS Frameworks and when to use them, by Chris Wharton](https://chriswharton.me/2016/05/html-css-and-js-frameworks-use)
- [Front-end Hyperpolyglot, by Jeff Carp](https://jeffcarp.github.io/frontend-hyperpolyglot)
- [What is Semantic Versioning (SemVer)?, by AbdulFattaah Popoola](https://abdulapopoola.com/2015/10/26/what-is-semver)
