---


---

<h1 id="javascript-basic">Javascript Basic</h1>
<p>Javascript adalah bahasa pemrograman yang digunakan dalam pengembangan website agar lebih dinamis dan interaktif.</p>
<ol>
<li>
<p><strong>Variable &amp; Primitive Data Type:</strong></p>
<ul>
<li>Variabel digunakan untuk menyimpan data.</li>
<li>Tipe data primitif meliputi String, Number, Boolean, Null, dan Undefined.</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> teks <span class="token operator">=</span> <span class="token string">"Ini adalah String"</span><span class="token punctuation">;</span>
<span class="token keyword">let</span> angka <span class="token operator">=</span> <span class="token number">123</span><span class="token punctuation">;</span>
<span class="token keyword">let</span> isValid <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
<span class="token keyword">let</span> kosong <span class="token operator">=</span> <span class="token keyword">null</span><span class="token punctuation">;</span>
<span class="token keyword">let</span> tidakDidefinisikan<span class="token punctuation">;</span>
</code></pre>
<ol start="2">
<li>
<p><strong>Where to Write:</strong></p>
<ul>
<li>Eksternal: Menulis JavaScript dalam file terpisah.</li>
<li>Internal: Menulis JavaScript di dalam tag <code>&lt;script&gt;</code> di halaman HTML.</li>
<li>Inline Event Handler: Menambahkan JavaScript langsung pada atribut event HTML.</li>
</ul>
</li>
</ol>
<pre class=" language-html"><code class="prism  language-html"><span class="token comment">&lt;!-- Eksternal --&gt;</span>  
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span> <span class="token attr-name">src</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>script.js<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript"></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token comment">&lt;!-- Internal --&gt;</span>  
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
  <span class="token comment">// Kode JavaScript di sini</span>
</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>

<span class="token comment">&lt;!-- Inline Event Handler --&gt;</span> 
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>button</span> <span class="token attr-name">onclick</span><span class="token attr-value"><span class="token punctuation">=</span><span class="token punctuation">"</span>myFunction()<span class="token punctuation">"</span></span><span class="token punctuation">&gt;</span></span>Klik saya<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>button</span><span class="token punctuation">&gt;</span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>script</span><span class="token punctuation">&gt;</span></span><span class="token script language-javascript">
  <span class="token keyword">function</span> <span class="token function">myFunction</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"Hello, World!"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
</span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>script</span><span class="token punctuation">&gt;</span></span>
</code></pre>
<ol start="3">
<li>
<p><strong>Output:</strong></p>
<ul>
<li><code>console.log()</code>: Menampilkan output ke konsol pengembangan.</li>
<li><code>document.write()</code>: Menulis langsung ke dokumen HTML.</li>
<li><code>alert()</code>: Menampilkan dialog peringatan kepada pengguna.</li>
<li></li>
</ul>
</li>
<li>
<p><strong>Function:</strong></p>
<ul>
<li>Fungsi memiliki cakupan (scope) yang mendefinisikan akses variabel.</li>
<li>Fungsi dapat mengembalikan nilai dengan menggunakan <code>return</code>.</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">function</span> <span class="token function">tambah</span><span class="token punctuation">(</span>a<span class="token punctuation">,</span> b<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">return</span> a <span class="token operator">+</span> b<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token keyword">let</span> hasil <span class="token operator">=</span> <span class="token function">tambah</span><span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">4</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Hasil penambahan:"</span><span class="token punctuation">,</span> hasil<span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ol start="5">
<li>
<p><strong>Array Data Type:</strong></p>
<ul>
<li>Mendapatkan panjang array dengan <code>length</code>.</li>
<li>Melooping elemen-elemen array.</li>
<li>Mengubah array menggunakan <code>push()</code>, <code>pop()</code>, <code>splice()</code>.</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> fruits <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"Apple"</span><span class="token punctuation">,</span> <span class="token string">"Banana"</span><span class="token punctuation">,</span> <span class="token string">"Orange"</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"Jumlah buah:"</span><span class="token punctuation">,</span> fruits<span class="token punctuation">.</span>length<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> i <span class="token operator">=</span> <span class="token number">0</span><span class="token punctuation">;</span> i <span class="token operator">&lt;</span> fruits<span class="token punctuation">.</span>length<span class="token punctuation">;</span> i<span class="token operator">++</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>fruits<span class="token punctuation">[</span>i<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

fruits<span class="token punctuation">.</span><span class="token function">push</span><span class="token punctuation">(</span><span class="token string">"Mango"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
fruits<span class="token punctuation">.</span><span class="token function">pop</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
fruits<span class="token punctuation">.</span><span class="token function">splice</span><span class="token punctuation">(</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">,</span> <span class="token string">"Grapes"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ol start="6">
<li>
<p><strong>Condition:</strong></p>
<ul>
<li>Operator Ternary: Singkat untuk menyatakan kondisi if-else.</li>
<li>Operator Logika satu baris: Memanfaatkan &amp;&amp; atau || untuk ekspresi singkat.</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> nilai <span class="token operator">=</span> <span class="token number">80</span><span class="token punctuation">;</span>
<span class="token keyword">let</span> status <span class="token operator">=</span> nilai <span class="token operator">&gt;=</span> <span class="token number">70</span> <span class="token operator">?</span> <span class="token string">"Lulus"</span> <span class="token punctuation">:</span> <span class="token string">"Tidak Lulus"</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>status<span class="token punctuation">)</span><span class="token punctuation">;</span>

<span class="token keyword">let</span> isLoggedIn <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
isLoggedIn <span class="token operator">&amp;&amp;</span> console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token string">"User sudah login"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ol start="7">
<li>
<p><strong>Loop:</strong></p>
<ul>
<li><code>for in/of</code>: Melooping properti atau nilai dalam objek atau array.</li>
<li><code>.map()</code>: Membuat array baru dengan hasil pemanggilan fungsi pada setiap elemen array.</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">const</span> person <span class="token operator">=</span> <span class="token punctuation">{</span> nama<span class="token punctuation">:</span> <span class="token string">"John"</span><span class="token punctuation">,</span> umur<span class="token punctuation">:</span> <span class="token number">25</span> <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token keyword">for</span> <span class="token punctuation">(</span><span class="token keyword">let</span> key <span class="token keyword">in</span> person<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>key<span class="token punctuation">,</span> person<span class="token punctuation">[</span>key<span class="token punctuation">]</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">const</span> numbers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
<span class="token keyword">const</span> doubled <span class="token operator">=</span> numbers<span class="token punctuation">.</span><span class="token function">map</span><span class="token punctuation">(</span>num <span class="token operator">=&gt;</span> num <span class="token operator">*</span> <span class="token number">2</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ol start="8">
<li>
<p><strong>Built-in Method:</strong></p>
<ul>
<li>Metode String: <code>substring()</code>, <code>replace()</code>, <code>toUpperCase()</code>, dll.</li>
<li>Metode Number: <code>toString()</code>, <code>toFixed()</code>, dll.</li>
<li>Metode Array: <code>push()</code>, <code>pop()</code>, <code>sort()</code>, <code>join()</code>, <code>map()</code>, <code>filter()</code>, <code>find()</code>, dll.</li>
</ul>
</li>
<li>
<p><strong>String Template Literal:</strong></p>
<ul>
<li>Menggabungkan string dan variabel dengan menggunakan backticks (`).</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> nama <span class="token operator">=</span> <span class="token string">"Alice"</span><span class="token punctuation">;</span>
<span class="token keyword">let</span> umur <span class="token operator">=</span> <span class="token number">30</span><span class="token punctuation">;</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token template-string"><span class="token string">`Halo, nama saya </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>nama<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> dan saya berumur </span><span class="token interpolation"><span class="token interpolation-punctuation punctuation">${</span>umur<span class="token interpolation-punctuation punctuation">}</span></span><span class="token string"> tahun.`</span></span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
<ol start="10">
<li>
<p><strong>JS Scope &amp; Hoisting Concept:</strong></p>
<ul>
<li>Scope: Menentukan di mana suatu variabel dapat diakses.</li>
<li>Hoisting: Membawa deklarasi variabel ke atas, sehingga dapat diakses sebelum dideklarasikan.</li>
</ul>
</li>
</ol>
<pre class=" language-js"><code class="prism  language-js"><span class="token keyword">let</span> x <span class="token operator">=</span> <span class="token number">10</span><span class="token punctuation">;</span> <span class="token comment">// Variabel global</span>

<span class="token keyword">function</span> <span class="token function">tambah</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">let</span> y <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span> <span class="token comment">// Variabel lokal dalam fungsi</span>
  <span class="token keyword">return</span> x <span class="token operator">+</span> y<span class="token punctuation">;</span>
<span class="token punctuation">}</span>

console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span><span class="token function">tambah</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Output: 15</span>

<span class="token comment">//hoisting</span>
console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>z<span class="token punctuation">)</span><span class="token punctuation">;</span> <span class="token comment">// Output: undefined</span>
<span class="token keyword">var</span> z <span class="token operator">=</span> <span class="token number">5</span><span class="token punctuation">;</span>
</code></pre>

