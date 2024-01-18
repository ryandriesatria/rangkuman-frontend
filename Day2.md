---


---

<h1 id="html">HTML</h1>
<p>Hyper Text Markup Language merupakan struktur dasar halaman web yang berisikan data yang akan ditampilkan.</p>
<h2 id="syntax--structure">Syntax &amp; Structure</h2>
<pre><code>&lt;!DOCTYPE html&gt;  
	&lt;html&gt;  
		&lt;head&gt;  
			&lt;title&gt;Page Title&lt;/title&gt;  
		&lt;/head&gt;  
		&lt;body&gt;  
  
			&lt;h1&gt;This is a Heading&lt;/h1&gt;  
			&lt;p&gt;This is a paragraph.&lt;/p&gt;  
  
		&lt;/body&gt;  
	&lt;/html&gt;
</code></pre>
<p>HTML umumnya berisikan elemen tag pembuka dan penutup. <code>&lt;!DOCTYPE html&gt;</code> menunjukkan halaman tersebut dideklarasikan sebagai halaman HTML.</p>
<h2 id="basic-tags">Basic Tags</h2>
<ul>
<li>Headings - Judul atau title, terdiri dari <code>&lt;h1&gt;</code> sampai <code>&lt;h6&gt;</code></li>
<li>Paragraph - Paragraf yang berisikan kumpulan kalimat atau teks <code>&lt;p&gt;</code></li>
<li>Links - Mengalihkan pengguna ke halaman HTML lain ketika diklik <code>&lt;a&gt;</code></li>
<li>Image - Menampilkan gambar <code>&lt;img&gt;</code></li>
</ul>
<h2 id="list-tags">List Tags</h2>
<p>Mengelompokkan sekumpulan item ke dalam sebuah group.</p>
<ul>
<li>
<p>Unordered List</p>
<pre><code>	&lt;ul&gt;  
		&lt;li&gt;Coffee&lt;/li&gt;  
		&lt;li&gt;Tea&lt;/li&gt;  
		&lt;li&gt;Milk&lt;/li&gt;  
	&lt;/ul&gt;
</code></pre>
</li>
<li>
<p>Ordered List</p>
<pre><code>	&lt;ol&gt;  
		&lt;li&gt;Coffee&lt;/li&gt;  
		&lt;li&gt;Tea&lt;/li&gt;  
		&lt;li&gt;Milk&lt;/li&gt;  
	&lt;/ol&gt;
</code></pre>
</li>
</ul>
<h2 id="table-tags">Table Tags</h2>
<pre><code>&lt;table&gt;  
	&lt;tr&gt;  
		&lt;th&gt;Company&lt;/th&gt;  
		&lt;th&gt;Contact&lt;/th&gt;  
		&lt;th&gt;Country&lt;/th&gt;  
	&lt;/tr&gt;  
	&lt;tr&gt;  
		&lt;td&gt;Alfreds Futterkiste&lt;/td&gt;  
		&lt;td&gt;Maria Anders&lt;/td&gt;  
		&lt;td&gt;Germany&lt;/td&gt;  
	&lt;/tr&gt;  
	&lt;tr&gt;  
		&lt;td&gt;Centro comercial Moctezuma&lt;/td&gt;  
		&lt;td&gt;Francisco Chang&lt;/td&gt;  
		&lt;td&gt;Mexico&lt;/td&gt;  
	&lt;/tr&gt;  
&lt;/table&gt;
</code></pre>
<ul>
<li><code>&lt;table&gt;</code> - Mendefinisikan tabel baru</li>
<li><code>&lt;tr&gt;</code> - Baris baru dalam tabel</li>
<li><code>&lt;th&gt;</code> - Judul dari masing - masing kolom</li>
<li><code>&lt;td&gt;</code> - Isi data dari masing - masing kolom</li>
</ul>
<h2 id="form-tags">Form Tags</h2>
<p>Form <code>&lt;form&gt;</code> digunakan sebagai penerima input dari pengguna untuk diolah menuju server.</p>
<ul>
<li><code>&lt;input&gt;</code> - Terdiri dari berbagai macam bentuk inputan yang disesuaikan dari kebutuhan pengguna seperti text, radio, checkbox, submit dan button</li>
<li><code>&lt;label&gt;</code> - Digunakan untuk mendefinisikan input kepada pengguna</li>
<li><code>&lt;textarea&gt;</code> - Input yang berisikan lebih dari satu kalimat/paragraf</li>
</ul>
<h1 id="semantic-html">Semantic HTML</h1>
<p>Mendeskripsikan elemen HTML sesuai isi dari kontennya.</p>

<table>
<thead>
<tr>
<th align="center">Tag</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><code>&lt;article&gt;</code></td>
<td>Konten independen(artikel)</td>
</tr>
<tr>
<td align="center"><code>&lt;aside&gt;</code></td>
<td>Konten selain konten utama di page</td>
</tr>
<tr>
<td align="center"><code>&lt;main&gt;</code></td>
<td>Konten utama dari dokumen</td>
</tr>
<tr>
<td align="center"><code>&lt;header&gt;</code></td>
<td>Bagian atas atau kepala dari dokumen</td>
</tr>
<tr>
<td align="center"><code>&lt;nav&gt;</code></td>
<td>Navigation bar yang berisikan link</td>
</tr>
<tr>
<td align="center"><code>&lt;section&gt;</code></td>
<td>Bagian tertentu dari dokumen</td>
</tr>
<tr>
<td align="center"><code>&lt;footer&gt;</code></td>
<td>Bagian bawah atau penutup dari dokumen</td>
</tr>
</tbody>
</table><h2 id="iframe">Iframe</h2>
<p>Iframe atau Inline Frame digunakan untuk mencantumkan halaman HTML lain ke dalam dokumen. Contoh Iframe embeded video youtube</p>
<pre><code>&lt;iframe width="560" height="315" src="https://www.youtube.com/embed/bFvjE4ZRtSE?si=VTEMUsG8VXHF0pHq" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen&gt;&lt;/iframe&gt;
</code></pre>
<h2 id="media-source">Media Source</h2>
<ul>
<li>
<p>Video</p>
<pre><code>&lt;video width="320"  height="240"  controls&gt;  
	&lt;source src="movie.mp4"  type="video/mp4"&gt;  
	&lt;source src="movie.ogg"  type="video/ogg"&gt;  
	Your browser does not support the video tag.  
&lt;/video&gt;
</code></pre>
</li>
<li>
<p>Audio</p>
<pre><code>&lt;audio controls&gt;  
	&lt;source src="horse.ogg"  type="audio/ogg"&gt;  
	&lt;source src="horse.mp3"  type="audio/mpeg"&gt;  
	Your browser does not support the audio element.  
&lt;/audio&gt;
</code></pre>
</li>
</ul>
<h2 id="entities">Entities</h2>
<ul>
<li><code>&amp;nbsp;</code> - Non breaking space</li>
<li><code>&amp;copy;</code> - Copyright ©</li>
<li><code>&amp;reg;</code> - Trademark ®</li>
<li><code>&amp;bull;</code> - Dot/Bullet sign •</li>
</ul>

