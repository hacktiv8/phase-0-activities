# ES6 Arrow Function

## Objectives

- ▢ Memanfaatkan Arrow Function sebagai Pengganti Anonymous Function

## Learnings

Kita sebelumnya pernah belajar tentang penggunaan Anonymous function, sebuah function yang "tidak bernama" pada saat kita deklarasikan. Anonymous function ini, berguna baik sebagai fungsi yang akan kita tampung sebagai variabel atau bisa juga untuk sebagai callback function (ini akan kita pelajari besok).

**Bentuk Anonymous Function**
```javascript
function (param1, param2, ...) {
  return ...
}
```

**Contoh Sederhana Anonymous Function**
```javascript
var averageFromTwoNumber = function (param1, param2) {
  return (param1 + param2) / 2;
}

console.log(averageFromTwoNumber(5, 7)); // 6
```

Di ES6, kita bisa mendeklarasikan ulang anonymous function dalam bentuk arrow function. Bentuknya adalah sebagai berikut:

**Bentuk Arrow Function**
```javascript
// Apabila ada 2 parameter atau lebih
(param1, param2, ...) =>{
  return ...
}

// Apabila tidak ada parameter
() => {
  return ...
}

// Apabila menampung 1 parameter, boleh tidak menggunakan kurung ()
param1 => {
  return ...
}
```
