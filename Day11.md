# Javascript Object

**Object Data Type:**

-   Objek adalah tipe data kompleks yang dapat menyimpan data dalam bentuk pasangan kunci-nilai (key-value).
	```js
	let person = {
	  name: "John",
	  age: 30,
	  isStudent: false
	};
	```
**Method inside Object:**

-   Method dalam objek berfungsi menjadi nilai properti.
	```js
	let person = {
	  name: "John",
	  sayHello: function() {
	    console.log("Hello, " + this.name + "!");
	  }
	};
	person.sayHello();
	```

**THIS Keyword:**

-   `this` digunakan untuk merujuk pada objek saat ini dalam konteks.
	```js
	let person = {
	  name: "John",
	  introduce: function() {
	    console.log("My name is " + this.name);
	  }
	};
	```

**Array Of Object:**

-   Array dapat menyimpan objek sebagai elemennya.
	```js
	let people = [
	  { name: "John", age: 30 },
	  { name: "Alice", age: 25 },
	  { name: "Bob", age: 35 }
	];
	```

**Spread & Rest Operator:**

-   Operator spread digunakan untuk membagi elemen array atau properti pada objek, sehingga elemen array dapat ditambahkan/dimasukan ke dalam array baru.
-   Operator rest berguna untuk menggabungkan semua paramater pada _function_ ke dalam array. Dengan menggunakan _Rest Parameter_ ini dapat membantu kita mendefinisikan _function_ dengan rapi serta memberikan parameter yang tidak terbatas pada sebuah _function_.
	```js
	//spread
	let person = { name: "John", age: 30 };
	let newPerson = { ...person, location: "City" };

	//rest
	function myFunction(...args) {
	  console.log(args);
	}
	myFunction(1, 2, 3);
	```

**Object Destructure:**

-   Objek dapat diuraikan untuk mengambil nilai-nilainya secara terpisah.
	```js
	let person = { name: "John", age: 30 };
	let { name, age } = person;
	```

**Optional Chaining:**

-   Digunakan untuk mengakses properti objek dengan aman, bahkan jika properti tersebut tidak terdefinisi.
	```js
	let person = { name: "John", address: { city: "New York" } };
	let city = person.address?.city;
	```

**Copy by Reference vs by Value:**

-   Objek disalin dengan referensi, sehingga perubahan pada salinan akan memengaruhi objek asli.
-   Nilai primitif disalin dengan nilai, sehingga salinan independen dari nilai aslinya.
	```js
	let obj1 = { name: "John" };
	let obj2 = obj1; // Copy by reference
	let num1 = 5;
	let num2 = num1; // Copy by value
	```

# NPM

 **NPM Introduction:**
    
   -   NPM (Node Package Manager) adalah manajer paket untuk ekosistem Node.js yang digunakan untuk mengelola dan mengunduh paket-paket JavaScript.
    -   Memungkinkan pengembang untuk memanfaatkan ribuan paket perangkat lunak dari komunitas.
 
**Install Package/Library using NPM:**
    
   -   Menggunakan perintah `npm install <package-name>` untuk mengunduh dan menginstal paket dari registry NPM.
	
**Import, Export, Export Default:**

-   **Import:** Digunakan untuk membawa modul atau fungsi dari paket yang diinstal ke dalam file proyek.
	```js
	const lodash = require('lodash');
	```
- **Export:** Digunakan untuk membuat fungsi, variabel, atau objek menjadi dapat diakses dari luar modul.
	```js
	// In file myModule.js
	const myFunction = () => {
	  // ...
	};
	module.exports = myFunction;
	```
- **Export Default:** Mengizinkan satu-satunya objek atau fungsi yang akan diekspor dari modul.
	```js
	// In file myModule.js
	const myFunction = () => {
	  // ...
	};
	export default myFunction;
	```

**package.json Structure (Custom Script):**

-   Berkas `package.json` menyimpan metadata proyek dan daftar dependensi.
	```js
	{
	  "name": "nama-proyek",
	  "version": "1.0.0",
	  "description": "Deskripsi proyek",
	  "scripts": {
	    "start": "node index.js",
	    "test": "mocha test/*.js"
	  },
	  "dependencies": {
	    "lodash": "^4.17.21"
	  }
	}
	```
- **Custom Script:** Menambahkan skrip kustom dalam bagian "scripts".
	```js
	"scripts": {
	  "build": "babel src -d dist",
	  "start": "node dist/index.js"
	```
- Menjalankan skrip: `npm run build`
