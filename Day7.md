# Tailwind CSS

Tailwind CSS merupakan framework CSS yang  _berbasis utility_  untuk membuat UI atau tampilan dari aplikasi web.
_Berbasis utility_ artinya Tailwind cuma terdiri dari 100% utility class dan tidak menggunakan class komponen seperti Navbar, Button, Card, Modal, dll. Komponen-komponen ini kita buat sendiri dengan class utility.

1.  **Instalasi dari CDN dan NPM:**
    
    -   Tailwind CSS dapat diinstal melalui Content Delivery Network (CDN) atau Node Package Manager (NPM).
    -   Instalasi melalui NPM memungkinkan pengelolaan dependensi proyek dengan lebih baik.
    -   Instalasi melalui CDN: 
    `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css">`
	-   Instalasi melalui NPM: `npm install tailwindcss`
	
2.  **Konsep Dasar:**
    
    -   Tailwind adalah framework CSS yang memungkinkan pengembang menggunakan kelas utilitas langsung dalam HTML.
    -   Tidak ada gaya pra-didefinisikan; semuanya dibangun melalui kombinasi kelas utilitas.
    -   Tanpa Tailwind:
     `<div style="margin: 10px; padding: 20px; border: 1px solid #000;">Konten</div>`
	-   Dengan Tailwind: 
	`<div class="m-10 p-20 border-solid border">Konten</div>`
	
3.  **Box Model Utility Class:**
    
    -   Tailwind menyediakan kelas utilitas untuk mengatur properti pada model kotak, seperti margin, padding, dan border.
    -   Margin: `m-4` (margin 1.5rem)
	-   Padding: `p-6` (padding 1.5rem)
	-   Border: `border` (border 1px)
    
4.  **Tailwind Modifier untuk Pseudo Class:**
    
    -   Kombinasi kelas utilitas dan modifier Tailwind memungkinkan penargetan pseudo-class seperti hover atau focus.
    -   Hover Efek: `hover:bg-blue-500`
	-   Focus Efek: `focus:outline-none`
    
5.  **Tailwind Responsive Modifier:**
    
    -   Responsive design diperkuat dengan menggunakan kelas utilitas dan modifier responsif Tailwind, memungkinkan penyesuaian tata letak untuk berbagai ukuran layar.
    -   Responsif pada Layar Kecil: `sm:text-lg`
	-   Responsif pada Layar Besar: `lg:text-xl`
```markdown
| Breakpoint Prefix | Minimum width | CSS                                |
|-------------------|---------------|------------------------------------|
| sm                | 640px         | @media (min-width: 640px) { ... }  |
| md                | 768px         | @media (min-width: 768px) { ... }  |
| lg                | 1024px        | @media (min-width: 1024px) { ... } |
| xl                | 1280px        | @media (min-width: 1280px) { ... } |
| 2xl               | 1536px        | @media (min-width: 1536px) { ... } |
```
    
6.  **Warna & Unit Ukuran:**
    
    -   Tailwind menyediakan kelas utilitas untuk warna dan ukuran unit, mempermudah pengaturan properti-properti ini.
    -   Warna Tebal Biru: `text-blue-800`
	-   Ukuran Lebar 50%: `w-1/2`
    
7.  **Display Flex & Grid Class:**
    
    -   Kelas utilitas Tailwind memfasilitasi penggunaan display flex dan grid untuk mengelola tata letak dengan mudah.
    -   Flex Container: `flex justify-between items-center`
	-   Grid Container: `grid grid-cols-2 gap-4`
    
8.  **Penyesuaian (Customization):**
    
    -   Tailwind dapat disesuaikan dengan mengatur file konfigurasi, memungkinkan penambahan atau penghapusan kelas utilitas sesuai kebutuhan.
    - Arbitrary value memungkinkan pengguna untuk menggunakan nilai custom terhadap sebuat properti. Contohnya `w-[162px]` atau `bg-[#dcdcdc]`
    - Layer dasar (base) untuk mengubah aturan dasar atau style bawaan yang diterapkan pada elemen HTML biasa.
	- Layer komponen (component) untuk membuat kelas berbasis komponen menggunakan gabungan kelas - kelas utility yang ada.
	- Layer utilitas (utility) untuk memodifikasi atau membuat kelas yang dimana kelas tersebut belum tersedia pada kelas utility di Tailwind.
   ```css
module.exports = {
	  theme: {
	    extend: {
	      colors: {
	        primary: '#3490dc',
	      },
	    },
	  },
	  variants: {},
	  plugins: [],
}
   ```
 ```css
 @layer base  {  
	 h1  {  
		 @apply text-2xl;  
	 }  
	 h2  {  
		 @apply text-xl;  
	 }  
	 /* ... */  }

@layer components  {  
	.btn-primary { 
			@apply bg-blue-500 text-white p-2 		rounded; 
		}
}

@layer utilities  {  
	.content-auto  {  
			content-visibility: auto;  
	}  
}
```

9.  **Gaya yang Dapat Digunakan Ulang dengan @apply:**
    
    -   Menggunakan `@apply` memungkinkan pengembang menerapkan gaya yang telah ditentukan pada kelas-kelas utilitas untuk meningkatkan keterbacaan dan pemeliharaan kode.
```css
@layer components{
	.btn-primary { 
		@apply bg-blue-500 text-white p-2 	rounded; 
	}
}
```
    
10.  **Plugin Tailwind:**
    
	   -   Tailwind dapat diperluas melalui plugin untuk menambahkan fungsionalitas tambahan sesuai kebutuhan proyek.
	   - Contoh Plugin untuk Gradients:
```js
// Install plugin  
// npm install tailwindcss-gradients  
module.exports = { 
	// ...  
	plugins: [ 
		require('tailwindcss-gradients'), 
		// ... 
	], 
}
```
Menggunakan Plugin: `bg-gradient-to-r from-blue-500 to-green-500`
    
11.  **Build untuk Produksi:**
    
	    -   Sebelum di-deploy, proyek Tailwind dapat dioptimalkan untuk produksi melalui perintah build, yang mengurangi ukuran file CSS dan meningkatkan performa.
	    - `npx tailwindcss build styles.css -o output.css`
   
