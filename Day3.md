---


---

<h1 id="css-basic">CSS Basic</h1>
<p>Cascade Style Sheet (CSS) merupakan bahasa yang digunakan dalam pemrograman web untuk mengatur tampilan sehingga terlihat lebih menarik.</p>
<h2 id="css-syntax--structure">CSS Syntax &amp; Structure</h2>
<pre class=" language-css"><code class="prism  language-css"><span class="token selector">h1 </span><span class="token punctuation">{</span>
    <span class="token property">color</span><span class="token punctuation">:</span> red<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre>
<ul>
<li>Selektor - Memilih elemen HTML yang akan diberi style</li>
<li>Properti - Atribut pada elemen yang ingin diubah stylenya. Contohnya font size, font family dsb.</li>
<li>Value - Nilai yang diberikan pada atribut, nilainya tergantung atribut yang diubah.</li>
</ul>
<h2 id="selector">Selector</h2>
<ul>
<li>Internal CSS - Ditulis di dalam tag <code>&lt;style&gt;</code> pada file html.</li>
<li>Inline CSS - Ditulis di dalam atribut elemen html.</li>
<li>Eksternal CSS - Ditulis di dalam file CSS yang kemudian di import menggunakan <code>&lt;link&gt;</code>.</li>
</ul>
<h2 id="typography-properties">Typography Properties</h2>
<ul>
<li><code>font-size</code> - Mengatur ukuran teks.</li>
<li><code>font-style</code> - Mengatur style dari teks seperti bergaris miring (italic).</li>
<li><code>font-weight</code> - Mengatur ketebalan dari teks.</li>
<li><code>font-family</code> - Mengatur jenis font yang digunakan.</li>
</ul>
<h2 id="color-properties">Color Properties</h2>
<ul>
<li><code>color</code> - Memberikan warna pada teks.</li>
<li><code>background-color</code> - Memberikan warna latar pada elemen.</li>
</ul>
<p>Warna dapat dideklarasikan menggunakan :</p>
<ol>
<li>Nama warna (red, green, yellow, etc)</li>
<li>Kode heksadesimal (#rrggbb) dimana masing-masing nilai r, g dan b berisikan nilai heksadesimal dari 0 sampai f.</li>
<li>Nilai rgb <code>rgb(0,0,0)</code> dimana masing-masing nilai pada parameter merepresentasikan komposisi warna red, green dan blue.</li>
</ol>
<h2 id="box-model">Box Model</h2>
<ul>
<li><code>padding</code> - Mengatur ruang disekitar konten.</li>
<li><code>border</code> - Mengatur batasan yang mengelilingi konten dan padding.</li>
<li><code>margin</code> - Mengatur ruang di luar elemen.</li>
<li><code>height</code> - Mengatur ketinggian dari elemen.</li>
<li><code>width</code> - Mengatur kelebaran dari elemen.</li>
</ul>
<h2 id="display-properties">Display Properties</h2>
<p>Display CSS adalah properti yang menentukan bagaimana elemen HTML harus ditampilkan di halaman web.</p>
<ul>
<li><code>inline</code> - Elemen ditampilkan sejajar dengan elemen lain atau dengan teks di sekitarnya, tanpa memulai baris baru.</li>
<li><code>block</code> - Memulai baris baru dan mengambil seluruh lebar yang tersedia pada container parent-nya.</li>
<li><code>inline-block</code> - Elemen untuk diletakkan sejajar dengan elemen lain (seperti inline), namun tetap bisa mengatur lebar dan tinggi secara eksplisit (seperti block).</li>
</ul>
<h2 id="position-properties">Position Properties</h2>
<p>Properti position berguna untuk mengatur letak dan posisi masing-masing elemen sesuai dengan yang kita inginkan.</p>
<ul>
<li>
<p><code>static</code><br>
Posisi dan letak elemen akan mengalur seperti apa adanya alur halaman html (offset tidak mempengaruhi).</p>
</li>
<li>
<p><code>relative</code><br>
Sama seperti <code>static</code> namun <code>box-offset</code> mempengaruhi menggunakan nilai top, bottom, left atau right.</p>
</li>
<li>
<p><code>absolute</code><br>
Elemen yang bernilai Absolute akan bersifat <code>relative</code> pada position parentnya. Jadi jika ada sebuah elemen yang memiliki <code>position:absolute</code> letak atau posisi elemen tersebut akan bargantung atau mengikuti elemen parentnya.</p>
</li>
<li>
<p><code>fixed</code><br>
Position fixed memiliki kesamaan dengan <code>absolute</code>. Perbedaan terletak pada element parent relative dari element yang menerapkan position <code>fixed</code>. Jika pada <code>absolute</code> kita dapat mengatur siapa elemen parentnya untuk position <code>fixed</code> kali ini bergantung pada elemen parent yaitu halaman itu sendiri. Atau bersifat menempel/sticky pada tampilan halaman browser.</p>
</li>
<li>
<p><code>sticky</code><br>
Sticky merupakan position yang memadukan antara nilai position <code>relative</code> dan <code>fixed</code>, yang bergantung pada scroll position. Elemen akan bernilai relative hingga melewati tampilan halaman browser akan menempel/sticky.</p>
</li>
<li>
<p><code>z-index</code><br>
Properti <code>z-index</code> ini berguna untuk mengatur elemen mana yang ada di bagian depan dan belakang, biasa digunakan ketika ada elemen yang saling tumpang tindih. Namun untuk bisa menggunakan ini, perlu menggunakan properti <code>position</code> selain <code>static</code>.</p>
</li>
</ul>

