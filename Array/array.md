# Penjelasan

array adalah object, mutable
In JavaScript, arrays use numbered indexes.
In JavaScript, objects use named indexes.

> jangan gunakan new Array(), lebih baik let var = []

## Identifikasi array

Penggunaan `typeof` pada array akan menghasilkan object.

```js
Array.isArray(var)
var instanceof Array
```

## Cek panjang array

arr.length

## Konversi ke string

- `arr.toString()` separator otomatis koma `array baru`
- `arr.join('*')` separator custom `array baru`

## Modifikasi array

- `arr.push('asd')` => menambahkan data ke posisi akhir **`mutate`**
- `arr.unshift('asd')` => menambahkan data ke posisi awal **`mutate`**
- `arr.pop()` => menghapus data terakhir dan mengembalikan data tersebut **`mutate`**
- `arr.shift()` => menghapus data pertama dan mengembalikan data tsb **`mutate`**
- `arr.concat(array2, array3)` => uraikan array dan gabung
- `arr.slice(start, end)` => mengambil array dari index start sampai sebelum end
- `arr.splice(i_start, i_remove, add...)` => menghapus element setelah start dan menambahkan element lain (params 3, 4, ...) `mutate`
- `arr.toSpliced(i_start, i_remove, add...)` => menghapus element setelah start dan menambahkan element lain (params 3, 4, ...)
- `arr.includes(search_item)` => return boolean item ada/tidak di array

### find element

- `arr.find(callback)` mengambalikan nilai pertama yang memenuhi callback function (start from first index)
- `arr.findLast(callback)`
- `arr.findIndex(callback)`
- `arr.findLastIndex(callback)`

## Sort

### sort array of string

```js
arr.sort(); // mutate
arr.toSort(); // no mutate

// kombinasikan dengan reverse untuk descendant
arr.reverse(); // mutate
arr.toReverse(); // no mutate
```

### sort number

```js
const arr = [40, 100, 1, 5, 25, 10];
arr.sort(function(a, b){return a - b});
```

sort number tersebut dapat digunakan untuk menentukan min/max, dengan mengambil index akhir/awal. Nilai a dan b merupakan nilai dari member array yang diiterasi.

## Advance method (for senior)

- `arr.filter(callback)` return bentuk element yang sama yang hasil callback `true`
- `arr.reduce((acc, currVal)=>val, initAcc)` return total acc dari return iterasi semua nilai
- `arr.find(callback)` return element pertama yang hasil callback `true` / `undefined` jika tidak ada
- `arr.map(callback)` return array baru dengan element bernilai hasil callback
- `arr.flatMap(callback)` return array baru dengan element bernilai `flat 1 level` hasil callback
- `arr.some(callback)` return true/false apabila ada satu element yang memenuhi callback
