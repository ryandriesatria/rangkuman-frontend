# React JS
React.js adalah library JavaScript yang memudahkan pengembangan antarmuka pengguna yang dinamis dan responsif. Dengan JSX dan konsep-konsep seperti kondisional rendering dan list rendering, React mempermudah pembangunan aplikasi web modern dan efisien.
## Installation
-   **CDN (Content Delivery Network):**
    Menggunakan React melalui CDN memungkinkan penggunaan React tanpa konfigurasi proyek yang rumit.
    ```html
	<!-- React -->
	<script src="https://unpkg.com/react@17/umd/react.production.min.js"></script>
	<!-- React DOM -->
	<script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js"></script>
    ```
-   **Create React App (CRA):**
Tools React yang sudah dikonfigurasi dengan baik.
Mempercepat proses pengaturan dan pengembangan proyek React.
	```bash
	npx create-react-app my-react-app
	cd my-react-app
	npm start
	```    
-   **Vite:**
Alternatif modern untuk pengembangan aplikasi web dengan kinerja cepat.
	```bash
	npm create vite my-react-app --template react
	cd my-react-app
	npm install
	npm run dev
	```
## JSX
-   **JSX Curly Braces:**
Digunakan untuk mengekspresikan ekspresi JavaScript dalam JSX.
	```jsx
	const name = "John";
	const element = <p>Hello, {name}!</p>;
	```
-   **Conditional Rendering:**
Menggunakan kondisi untuk merender elemen berdasarkan keadaan tertentu.
	```jsx
	function Greeting({ isLoggedIn }) {
	  return isLoggedIn ? <p>Welcome back!</p> : <p>Please log in.</p>;
	}
	```
    
- **List Rendering:**
Merender list elemen dengan memetakan setiap elemen dari array ke elemen JSX.
	```jsx
	const items = ['Apple', 'Banana', 'Orange'];
	const listItems = items.map((item, index) => <li key={index}>{item}</li>);
	```

## Component
**Component Type:**

-   Dibagi menjadi dua jenis: Functional Component dan Class Component.
-   Komponen fungsional menggunakan fungsi, sedangkan kelas komponen menggunakan kelas.
	```jsx
	function Greeting(props) {
	  return <p>Hello, {props.name}!</p>;
	}
	```
	```jsx
	class Greeting extends React.Component {
	  render() {
	    return <p>Hello, {this.props.name}!</p>;
	  }
	}
	```
**Props:**

-   Menerima data sebagai properti dan memungkinkan komponen untuk menerima input.
	```jsx
	function Welcome(props) {
	  return <h1>Hello, {props.name}</h1>;
	}
	```
**Component Separation:**

-   Memisahkan komponen menjadi bagian-bagian kecil untuk meningkatkan keterbacaan dan pemeliharaan.
	```jsx
	function Header() {
	  return <header>Header content</header>;
	}

	function MainContent() {
	  return <main>Main content</main>;
	}
	```
## **Event:**
   **Handle Event Menggunakan Fungsi Anonim:**
   - Mendefinisikan fungsi langsung di dalam atribut event pada elemen JSX.
     ```jsx
     <button onClick={() => alert('Tombol diklik!')}>Klik saya</button>
     ```
**Handle Event Menggunakan Referensi Fungsi:**
   - Mendefinisikan fungsi terpisah dan merujuknya dari atribut event.
     ```jsx
     function handleClick() {
       alert('Tombol diklik!');
     }

     <button onClick={handleClick}>Klik saya</button>
     ```
**Meneruskan Parameter Menggunakan Panggilan Fungsi di Dalam Fungsi Anonim:**
- Meneruskan parameter ke dalam fungsi event.
     ```jsx
     function handleClick(name) {
       alert(`Halo, ${name}!`);
     }

     <button onClick={() => handleClick('John')}>Klik saya</button>
     ```

## **State:**
**useState Hooks:**
   - Menggunakan Hooks `useState` untuk membuat dan mengelola state dalam komponen fungsional.
     ```jsx
     import React, { useState } from 'react';

     function Counter() {
       const [count, setCount] = useState(0);

       return (
         <div>
           <p>Kamu menekan tombol sebanyak {count} kali</p>
           <button onClick={() => setCount(count + 1)}>Tambah</button>
         </div>
       );
     }
     ```
**Mengubah State pada Event Handler:**
 - Menggunakan fungsi `setState` untuk mengubah nilai state.

**Mendapatkan Nilai State Sebelumnya dari Fungsi Panggilan di Dalam `setState`:**
- Menggunakan callback pada `setState` untuk mendapatkan nilai state sebelumnya.
	```jsx
	function Counter() {
	  const [count, setCount] = useState(0);

	  function increment() {
	    setCount(prevCount => prevCount + 1);
	  }

	  return (
	    <div>
	      <p>Kamu menekan tombol sebanyak {count} kali</p>
	      <button onClick={increment}>Tambah</button>
	    </div>
	  );
	}
	```

**Objek pada Nilai State Awal:**
 - Menginisialisasi state dengan objek.
	```jsx
	const [state, setState] = useState({ count: 0, name: 'John' });
	```

**Fungsi pada Nilai State Awal:**
- Menginisialisasi state dengan fungsi.
	```jsx
	const [state, setState] = useState(() => {
	  const initialState = someExpensiveComputation();
	  return initialState;
	});
	```

## **Lifecycle:**
**Functional Component Lifecycle:**
 - Komponen fungsional tidak memiliki siklus hidup, tetapi dapat menggunakan Hooks `useEffect` untuk menangani efek samping.

**useEffect Hooks:**
- Digunakan untuk menjalankan efek samping dalam komponen fungsional.
	```jsx
	import React, { useEffect } from 'react';

	function MyComponent() {
	  useEffect(() => {
	    // Efek samping disini
	    return () => {
	      // Membersihkan efek samping disini
	    };
	  }, [dependency]);
	}
	```

 **Multiple useEffect dalam Satu Komponen:**
- Menggunakan Hooks `useEffect` beberapa kali dalam satu komponen.
	```jsx
	useEffect(() => {
	  // Efek samping pertama
	}, [dependency1]);

	useEffect(() => {
	  // Efek samping kedua
	}, [dependency2]);
	```


