## Javascript Asynchronous
JavaScript Asynchronous memungkinkan eksekusi kode berlanjut tanpa harus menunggu operasi selesai.
**Callback Function:**
   - **Callback Function:** Callback adalah fungsi yang dipassing sebagai argumen ke fungsi lain.
     ```javascript
     function fetchData(callback) {
       setTimeout(() => {
         callback('Data berhasil diambil');
       }, 2000);
     }

     function processData(data) {
       console.log(data);
     }

     fetchData(processData);
     ```
   - **Arrow Function:** Fungsi panjang yang diubah menjadi fungsi arrow.
     ```javascript
     fetchData((data) => {
       console.log(data);
     });
     ```

**Konsep Asynchronous :**
   - **SetTimeout():** Fungsi `setTimeout()` digunakan untuk menjalankan sebuah fungsi setelah waktu tertentu berlalu.
     ```javascript
     setTimeout(() => {
       console.log('Waktu habis!');
     }, 3000);
     ```

**Promise Data Type:**
   - **Promise:** Objek yang merepresentasikan penyelesaian atau kegagalan dari sebuah operasi asynchronous.
     ```javascript
     const fetchData = new Promise((resolve, reject) => {
       setTimeout(() => {
         resolve('Data berhasil diambil');
       }, 2000);
     });

     fetchData.then(data => console.log(data));
     ```

**Async Await:**
   - **Async Function:** Fungsi yang mengembalikan Promise.
     ```javascript
     async function fetchData() {
       return new Promise((resolve, reject) => {
         setTimeout(() => {
           resolve('Data berhasil diambil');
         }, 2000);
       });
     }

     async function processData() {
       const data = await fetchData();
       console.log(data);
     }

     processData();
     ```

**Try Catch Finally Block:**
   - **Try Catch:** Digunakan untuk menangkap kesalahan dalam blok kode.
     ```javascript
     try {
       // Kode yang mungkin melemparkan kesalahan
     } catch (error) {
       // Menangkap dan menangani kesalahan
     } finally {
       // Blok yang akan dieksekusi baik kode tersebut mengalami kesalahan atau tidak
     }
     ```

## REST API

JavaScript Rest API memungkinkan pengembang untuk mengintegrasikan aplikasi web dengan berbagai layanan dan sumber daya eksternal. Dengan menggunakan konsep JSON, HTTP, dan alat-alat seperti Axios, pengembang dapat membuat aplikasi web yang berinteraksi dengan berbagai API dengan mudah dan efisien.

**JSON Introduction & Syntax:**
   - **JSON (JavaScript Object Notation):** Format pertukaran data ringan yang digunakan untuk mentransfer data antara server dan browser.
   - **Syntax JSON:** Terdiri dari pasangan nama-nilai yang dipisahkan oleh koma, diawali dengan `{` dan diakhiri dengan `}`.
     ```json
     {
       "name": "John",
       "age": 30,
       "city": "New York"
     }
     ```

**JSON Property Value:**
   - **String:** Nilai dalam tanda kutip.
   - **Number:** Nilai numerik.
   - **Array:** Kumpulan nilai yang dipisahkan oleh koma dan diapit oleh tanda kurung siku.
   - **Object:** Koleksi pasangan nama-nilai yang dipisahkan oleh koma dan diapit oleh tanda kurung kurawal.

**JSON Parse & JSON Stringify:**
   - **JSON Parse:** Mengubah string JSON menjadi objek JavaScript.
     ```javascript
     const jsonStr = '{"name":"John","age":30}';
     const jsonObj = JSON.parse(jsonStr);
     ```
   - **JSON Stringify:** Mengubah objek JavaScript menjadi string JSON.
     ```javascript
     const obj = { name: 'John', age: 30 };
     const jsonStr = JSON.stringify(obj);
     ```

 **API Introduction:**
   - **API (Application Programming Interface):** Sekumpulan aturan, protokol, dan alat yang memungkinkan perangkat lunak untuk berkomunikasi satu sama lain.
   - **REST API (Representational State Transfer):** Gaya arsitektur perangkat lunak yang digunakan dalam pengembangan API.

**HTTP Status Code:**
   - **Status Code:** Kode numerik yang diberikan oleh server HTTP dalam tanggapan terhadap permintaan klien.
   - **Contoh Status Code:**
     - 200 OK: Permintaan berhasil.
     - 404 Not Found: Sumber daya tidak ditemukan.
     - 500 Internal Server Error: Terjadi kesalahan di server.

. **Consume API using Axios:**
   - **Axios:** Library HTTP client yang digunakan untuk melakukan permintaan HTTP dari browser atau Node.js.
   - **Contoh Penggunaan Axios:**
     ```javascript
     axios.get('https://api.example.com/data')
       .then(response => console.log(response.data))
       .catch(error => console.error('Error:', error));
     ```




