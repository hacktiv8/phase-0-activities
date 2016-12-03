# Mengubah ES5 menjadi ES6

## Objectives

- Mampu mengartikan pseudocode ke dalam program

## Directions

1. Ubah semua kode JavaScript dibawah ini ke dalam ES5. (setiap kode satu file JavaScript)

### Tugas 1

Ubahlah seluruh `var` pada kode JavaScript dibawah ini menjadi `let` atau `const`!

```javascript
var phi = 3.14
var power = 2
var radius = 0
var calculateArea = function (radius) {
  return phi * Math.pow(radius, power)
}

radius = 21
var area21 = calculateArea(radius)

radius = 7
var area7 = calculateArea(radius)

console.log('area with 21 radius: %d, and area with 7 radius: %d', area21, area7)
```

### Tugas 2

Ubahlah anonymous functions dibawah ini menjadi ES6 Arrow Function!

```javascript
  const multiply = function (num1, num2) {
    return num1 * num2;
  }

  const divide = function (num1, num2) {
    return num1 / num2;
  }

  console.log(multiply(5,2));
  console.log(divide(10,2));
```
