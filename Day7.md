---


---

<h1 id="tailwind-css">Tailwind CSS</h1>
<p>Tailwind CSS merupakan framework CSS yang  <em>berbasis utility</em>  untuk membuat UI atau tampilan dari aplikasi web.<br>
<em>Berbasis utility</em> artinya Tailwind cuma terdiri dari 100% utility class dan tidak menggunakan class komponen seperti Navbar, Button, Card, Modal, dll. Komponen-komponen ini kita buat sendiri dengan class utility.</p>
<ol>
<li>
<p><strong>Instalasi dari CDN dan NPM:</strong></p>
<ul>
<li>Tailwind CSS dapat diinstal melalui Content Delivery Network (CDN) atau Node Package Manager (NPM).</li>
<li>Instalasi melalui NPM memungkinkan pengelolaan dependensi proyek dengan lebih baik.</li>
<li>Instalasi melalui CDN:<br>
<code>&lt;link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css"&gt;</code></li>
<li>Instalasi melalui NPM: <code>npm install tailwindcss</code></li>
</ul>
</li>
<li>
<p><strong>Konsep Dasar:</strong></p>
<ul>
<li>Tailwind adalah framework CSS yang memungkinkan pengembang menggunakan kelas utilitas langsung dalam HTML.</li>
<li>Tidak ada gaya pra-didefinisikan; semuanya dibangun melalui kombinasi kelas utilitas.</li>
<li>Tanpa Tailwind:<br>
<code>&lt;div style="margin: 10px; padding: 20px; border: 1px solid #000;"&gt;Konten&lt;/div&gt;</code></li>
<li>Dengan Tailwind:<br>
<code>&lt;div class="m-10 p-20 border-solid border"&gt;Konten&lt;/div&gt;</code></li>
</ul>
</li>
<li>
<p><strong>Box Model Utility Class:</strong></p>
<ul>
<li>Tailwind menyediakan kelas utilitas untuk mengatur properti pada model kotak, seperti margin, padding, dan border.</li>
<li>Margin: <code>m-4</code> (margin 1.5rem)</li>
<li>Padding: <code>p-6</code> (padding 1.5rem)</li>
<li>Border: <code>border</code> (border 1px)</li>
</ul>
</li>
<li>
<p><strong>Tailwind Modifier untuk Pseudo Class:</strong></p>
<ul>
<li>Kombinasi kelas utilitas dan modifier Tailwind memungkinkan penargetan pseudo-class seperti hover atau focus.</li>
<li>Hover Efek: <code>hover:bg-blue-500</code></li>
<li>Focus Efek: <code>focus:outline-none</code></li>
</ul>
</li>
<li>
<p><strong>Tailwind Responsive Modifier:</strong></p>
<ul>
<li>Responsive design diperkuat dengan menggunakan kelas utilitas dan modifier responsif Tailwind, memungkinkan penyesuaian tata letak untuk berbagai ukuran layar.</li>
<li>Responsif pada Layar Kecil: <code>sm:text-lg</code></li>
<li>Responsif pada Layar Besar: <code>lg:text-xl</code></li>
</ul>
</li>
</ol>
<pre class=" language-markdown"><code class="prism  language-markdown">| Breakpoint Prefix | Minimum width | CSS                                |
|-------------------|---------------|------------------------------------|
| sm                | 640px         | @media (min-width: 640px) { ... }  |
| md                | 768px         | @media (min-width: 768px) { ... }  |
| lg                | 1024px        | @media (min-width: 1024px) { ... } |
| xl                | 1280px        | @media (min-width: 1280px) { ... } |
| 2xl               | 1536px        | @media (min-width: 1536px) { ... } |
</code></pre>
<ol start="6">
<li>
<p><strong>Warna &amp; Unit Ukuran:</strong></p>
<ul>
<li>Tailwind menyediakan kelas utilitas untuk warna dan ukuran unit, mempermudah pengaturan properti-properti ini.</li>
<li>Warna Tebal Biru: <code>text-blue-800</code></li>
<li>Ukuran Lebar 50%: <code>w-1/2</code></li>
</ul>
</li>
<li>
<p><strong>Display Flex &amp; Grid Class:</strong></p>
<ul>
<li>Kelas utilitas Tailwind memfasilitasi penggunaan display flex dan grid untuk mengelola tata letak dengan mudah.</li>
<li>Flex Container: <code>flex justify-between items-center</code></li>
<li>Grid Container: <code>grid grid-cols-2 gap-4</code></li>
</ul>
</li>
<li>
<p><strong>Penyesuaian (Customization):</strong></p>
<ul>
<li>Tailwind dapat disesuaikan dengan mengonfigurasi file konfigurasi, memungkinkan penambahan atau penghapusan kelas utilitas sesuai kebutuhan proyek.</li>
</ul>
</li>
</ol>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">module<span class="token class">.exports</span> = </span><span class="token punctuation">{</span>
   <span class="token selector">theme: </span><span class="token punctuation">{</span>
     <span class="token selector">extend: </span><span class="token punctuation">{</span>
       <span class="token selector">colors: </span><span class="token punctuation">{</span>
         <span class="token property">primary</span><span class="token punctuation">:</span> <span class="token string">'#3490dc'</span>,
       <span class="token punctuation">}</span>,
     <span class="token punctuation">}</span>,
   <span class="token punctuation">}</span><span class="token selector">,
   variants: </span><span class="token punctuation">{</span><span class="token punctuation">}</span>,
   <span class="token property">plugins</span><span class="token punctuation">:</span> [],
<span class="token punctuation">}</span>

</code></pre>
<ol start="9">
<li>
<p><strong>Gaya yang Dapat Digunakan Ulang dengan @apply:</strong></p>
<ul>
<li>Menggunakan <code>@apply</code> memungkinkan pengembang menerapkan gaya yang telah ditentukan pada kelas-kelas utilitas untuk meningkatkan keterbacaan dan pemeliharaan kode.</li>
</ul>
</li>
</ol>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector"><span class="token class">.btn-primary</span> </span><span class="token punctuation">{</span> 
	<span class="token atrule"><span class="token rule">@apply</span> bg-blue-500 text-white p-2 rounded<span class="token punctuation">;</span></span> 
<span class="token punctuation">}</span>
</code></pre>
<ol start="10">
<li>
<p><strong>Plugin Tailwind:</strong></p>
<ul>
<li>Tailwind dapat diperluas melalui plugin untuk menambahkan fungsionalitas tambahan sesuai kebutuhan proyek.</li>
<li>Contoh Plugin untuk Gradients:</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token comment">// Install plugin  </span>
<span class="token comment">// npm install tailwindcss-gradients  </span>
module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span> 
	<span class="token comment">// ...  </span>
	plugins<span class="token punctuation">:</span> <span class="token punctuation">[</span> 
		<span class="token function">require</span><span class="token punctuation">(</span><span class="token string">'tailwindcss-gradients'</span><span class="token punctuation">)</span><span class="token punctuation">,</span> 
		<span class="token comment">// ... </span>
	<span class="token punctuation">]</span><span class="token punctuation">,</span> 
<span class="token punctuation">}</span>
</code></pre>
<p>Menggunakan Plugin: <code>bg-gradient-to-r from-blue-500 to-green-500</code></p>
<ol start="11">
<li>
<p><strong>Build untuk Produksi:</strong></p>
<ul>
<li>Sebelum di-deploy, proyek Tailwind dapat dioptimalkan untuk produksi melalui perintah build, yang mengurangi ukuran file CSS dan meningkatkan performa.</li>
<li><code>npx tailwindcss build styles.css -o output.css</code></li>
</ul>
</li>
</ol>

