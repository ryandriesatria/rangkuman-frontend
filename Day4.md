---


---

<h1 id="css-advanced">CSS Advanced</h1>
<ol>
<li>
<p><strong>Advanced Selector:</strong></p>
<ul>
<li>CSS menyediakan pemilih lanjutan seperti pemilih atribut, pseudo-class, dan pseudo-element.</li>
<li>Pemilih atribut menargetkan elemen berdasarkan atribut mereka, sementara pseudo-class menargetkan keadaan tertentu seperti hover atau fokus. Contohnya <code>::before</code> dan <code>::after</code></li>
<li>Pseudo-element mengatur gaya bagian tertentu dari elemen, seperti baris pertama atau huruf pertama. Contohnya <code>:hover</code></li>
</ul>
</li>
<li>
<p><strong>Cascading Order and Specificity Hierarchy:</strong></p>
<ul>
<li>CSS mengikuti urutan bertingkat di mana gaya dapat diwarisi dari elemen induk dan ditimpa oleh aturan yang lebih spesifik.</li>
<li>Hirarki spesifikitas sangat penting untuk menentukan gaya mana yang berlaku saat konflik terjadi.</li>
<li>Gaya inline, ID, dan kelas memiliki tingkat spesifikitas yang berbeda.</li>
</ul>
</li>
<li>
<p><strong>Display Flex:</strong></p>
<ul>
<li>Flexbox adalah model tata letak yang menyederhanakan desain tata letak kompleks.</li>
<li><code>display: flex;</code> diterapkan pada kontainer, dan elemen di dalamnya menjadi item yang fleksibel.</li>
<li><code>flex-direction</code> digunakan untuk menentukan arah flex item yang ada dalam container.</li>
</ul>
<iframe class="interactive is-default-height" height="200" src="https://interactive-examples.mdn.mozilla.net/pages/css/flex-direction.html" title="MDN Web Docs Interactive Example"></iframe>
-   Flexbox menyediakan properti seperti `justify-content`, `align-items`, dan `flex` untuk mengontrol tata letak dan penyejajaran.
</li>
<li>
<p><strong>Media Query &amp; Responsive Design:</strong></p>
<ul>
<li>Media query memungkinkan desain responsif dengan menerapkan gaya berdasarkan karakteristik perangkat seperti lebar layar, tinggi, atau orientasi.</li>
<li>Fitur media query umum termasuk penyesuaian ukuran font, struktur tata letak, dan menyembunyikan/menampilkan elemen untuk ukuran layar yang berbeda.</li>
</ul>
</li>
<li>
<p><strong>Shadow Properties:</strong></p>
<ul>
<li>CSS memungkinkan pembuatan bayangan menggunakan properti <code>box-shadow</code> dan <code>text-shadow</code>.</li>
<li>Bayangan dapat meningkatkan daya tarik visual elemen dan memberikan kedalaman pada desain.</li>
</ul>
</li>
<li>
<p><strong>Transform Properties:</strong></p>
<ul>
<li>Properti <code>transform</code> memungkinkan manipulasi elemen dalam ruang 2D dan 3D.</li>
<li>Transformasi melibatkan translasi, rotasi, penskalaan, dan memiringkan, meningkatkan presentasi elemen web.</li>
</ul>
</li>
<li>
<p><strong>Transition Property:</strong></p>
<ul>
<li>Transisi CSS meratakan animasi perubahan properti selama durasi yang ditentukan.</li>
<li>Ini meningkatkan pengalaman pengguna dengan memberikan perubahan gaya secara bertahap, membuat antarmuka lebih interaktif.</li>
</ul>
</li>
<li>
<p><strong>Overflow &amp; Opacity Property:</strong></p>
<ul>
<li>Properti <code>overflow</code> mengontrol apa yang terjadi ketika konten melampaui kotaknya.</li>
<li>Properti <code>opacity</code> menyesuaikan transparansi elemen, memungkinkan efek desain yang kreatif.</li>
</ul>
</li>
<li>
<p><strong>Display Grid:</strong></p>
<ul>
<li>CSS Grid Layout menyederhanakan pembuatan tata letak kompleks.</li>
<li><code>display: grid;</code> diterapkan pada kontainer, dan elemen anak menjadi item grid.</li>
<li>Properti grid seperti <code>grid-template-columns</code> dan <code>grid-template-rows</code> mendefinisikan struktur grid.</li>
</ul>
</li>
</ol>

