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
