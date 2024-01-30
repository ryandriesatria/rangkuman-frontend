
# Javascript DOM

1.  **HTML DOM Introduction:**
    
   -   DOM (Document Object Model) adalah representasi struktur dokumen HTML yang memungkinkan JavaScript berinteraksi dengan HTML.
    -   Dokumen dianggap sebagai pohon objek, di mana setiap elemen adalah simpul (node).
2.  **Selecting Element:**
    
   -   `getElementById`: Mendapatkan elemen berdasarkan ID.
```js
    let myElement = document.getElementById("myId");
```
   -   `querySelector`: Mendapatkan elemen menggunakan selector CSS.
```js
let myElement = document.querySelector(".myClass");
```
3.  **Manipulating HTML Element:**
    
   -   `innerHTML`: Mengambil atau mengatur HTML dalam elemen.
```js
document.getElementById("myId").innerHTML = "Hello, World!";
```
   -   `appendChild`: Menambahkan elemen sebagai anak dari elemen lain.
```js
let newElement = document.createElement("p");
newElement.innerHTML = "New Paragraph";
document.getElementById("container").appendChild(newElement);
```
4.  **Manipulating Form:**
    
   -   Menggunakan properti `.value` untuk mendapatkan atau mengatur nilai elemen formulir seperti input.
```js
let userInput = document.getElementById("username").value;
console.log("Username:", userInput);
```
5.  **Manipulating Element Attribute:**
    
   -   Menggunakan metode seperti `getAttribute` dan `setAttribute` untuk mendapatkan dan mengatur nilai atribut elemen.
```js
let link = document.getElementById("myLink");
let hrefValue = link.getAttribute("href");
link.setAttribute("href", "https://www.example.com");
```
6.  **Manipulating Element CSS:**
    
   -   Menggunakan properti `style` atau `classList` untuk mengubah gaya CSS elemen.
```js
document.getElementById("myElement").style.color = "blue";
```
   -   `element.style.property = "value"` atau `element.classList.add/remove("class")`.
```js
document.getElementById("myElement").classList.add("highlight");
```
7.  **DOM Event:**
    
   -   Inline event: Menambahkan event langsung ke elemen HTML menggunakan atribut event seperti `onclick`.
```js
<button onclick="myFunction()">Click me</button>
<script>
  function myFunction() {
    alert("Button clicked!");
  }
</script>
```
   -   `addEventListener()`: Menambahkan event secara dinamis menggunakan JavaScript untuk meningkatkan fleksibilitas dan pemeliharaan kode.
```js
let myButton = document.getElementById("myButton");
myButton.addEventListener("click", function() {
  alert("Button clicked!");
});
```
