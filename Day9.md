# Javascript Basic
Javascript adalah bahasa pemrograman yang digunakan dalam pengembangan website agar lebih dinamis dan interaktif.

1.  **Variable & Primitive Data Type:**
    
    -   Variabel digunakan untuk menyimpan data.
    -   Tipe data primitif meliputi String, Number, Boolean, Null, dan Undefined.
```js
var teks = "Ini adalah String";
let angka = 123;
const isValid = true;
let kosong = null;
let tidakDidefinisikan;
```
2.  **Where to Write:**
    
    -   Eksternal: Menulis JavaScript dalam file terpisah.
	- Internal: Menulis JavaScript di dalam tag `<script>` di halaman HTML.

```html
<!-- Eksternal -->  
<script src="script.js"></script>

<!-- Internal -->  
<script>
  // Kode JavaScript di sini
</script>

<!-- Inline Event Handler --> 
<button onclick="myFunction()">Klik saya</button>
<script>
  function myFunction() {
    alert("Hello, World!");
  }
</script>
```
3.  **Output:**
    
    -   `console.log()`: Menampilkan output ke konsol pengembangan.
    -   `document.write()`: Menulis langsung ke dokumen HTML.
    -   `alert()`: Menampilkan dialog peringatan kepada pengguna.
    - 
4.  **Function:**
    
    -   Fungsi memiliki cakupan (scope) yang mendefinisikan akses variabel.
    -   Fungsi dapat mengembalikan nilai dengan menggunakan `return`.
```js
function tambah(a, b) {
  return a + b;
}
let hasil = tambah(3, 4);
console.log("Hasil penambahan:", hasil);
```
5.  **Array Data Type:**
    
    -   Mendapatkan panjang array dengan `length`.
    -   Melooping elemen-elemen array.
    -   Mengubah array menggunakan `push()`, `pop()`, `splice()`.
```js
let fruits = ["Apple", "Banana", "Orange"];
console.log("Jumlah buah:", fruits.length);

for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

fruits.push("Mango");
fruits.pop();
fruits.splice(1, 1, "Grapes");
```

6.  **Condition:**
    
    -   Operator Ternary: Singkat untuk menyatakan kondisi if-else.
    -   Operator Logika satu baris: Memanfaatkan && atau || untuk ekspresi singkat.

```js
let nilai = 80;
let status = nilai >= 70 ? "Lulus" : "Tidak Lulus";
console.log(status);

let isLoggedIn = true;
isLoggedIn && console.log("User sudah login");
```
7.  **Loop:**
    
    -   `for in/of`: Melooping properti atau nilai dalam objek atau array.
    -   `.map()`: Membuat array baru dengan hasil pemanggilan fungsi pada setiap elemen array.
```js
const person = { nama: "John", umur: 25 };
for (let key in person) {
  console.log(key, person[key]);
}

const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
```

8.  **Built-in Method:**
    
    -   Metode String: `substring()`, `replace()`, `toUpperCase()`, dll.
    -   Metode Number: `toString()`, `toFixed()`, dll.
    -   Metode Array: `push()`, `pop()`, `sort()`, `join()`, `map()`, `filter()`, `find()`, dll.


9.  **String Template Literal:**
    
    -   Menggabungkan string dan variabel dengan menggunakan backticks (`).
```js
let nama = "Alice";
let umur = 30;
console.log(`Halo, nama saya ${nama} dan saya berumur ${umur} tahun.`);
```
10.  **JS Scope & Hoisting Concept:**
    
	 - Scope: Menentukan di mana suatu variabel dapat diakses.
	 - Hoisting: Membawa deklarasi variabel ke atas, sehingga dapat diakses sebelum dideklarasikan.

```js
let x = 10; // Variabel global

function tambah() {
  let y = 5; // Variabel lokal dalam fungsi
  return x + y;
}

console.log(tambah()); // Output: 15

//hoisting
console.log(z); // Output: undefined
var z = 5;
```
