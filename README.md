1. Identitas Praktikum
- Nama : Anggun Kusuma Wardani
- Nim : 312510045
- Mata Kuliah: Pemrograman Web
- Praktikum: 4 — CSS Layout
- Topik: Box Element, CSS Float, Clearfix, HTML5 Semantic Elements, dan Layout Website
- Repository: Lab4Web
Sesuaikan identitas jika diperlukan. Screenshot pada README ini merujuk ke gambar yang disimpan di folder Screenshot/. Pastikan nama file gambar sesuai dengan nama yang ditulis di bawah setiap bagian.

2. Tujuan Praktikum
Berdasarkan modul Praktikum 4: CSS Layout, tujuan praktikum ini adalah:
1. Mahasiswa mampu memahami struktur dasar pembuatan layout.
2. Mahasiswa mampu memahami konsep box element.
3. Mahasiswa mampu memahami CSS floating.
4. Mahasiswa mampu memahami HTML5 semantic elements.
5. Mahasiswa mampu membuat layout web sederhana.

3. Struktur Folder
File praktikum disusun dengan struktur berikut:
Lab4Web/

├── lab4_box.html

├── Lab4_Layout

│   ├── home.html

│   ├── style.css

│   ├── about.html

│   └── kontak.html

├── Screenshot

│   ├── 01.png

│   ├── 02.png


│   ├── 03.png

│   ├── 04.png

│   ├── 05.png

│   ├── 06.png


│   ├── 07.png

│   ├── 08.png

│   ├── 09.png

│   ├── tugas1-about.png

│   └── tugas2-contact.png

└── README.md

4. Membuat Dokumen Box Element
Langkah Pengerjaan: 
Contoh HTML untuk tiga kotak:
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
</section>
CSS yang digunakan:
div {
    float: left;
    padding: 10px;
}

.div1 {
    background: red;
}

.div2 {
    background: yellow;
}

.div3 {
    background: green;
}
Penjelasan
Elemen div digunakan sebagai kotak untuk menampung konten. Properti padding: 10px memberikan ruang di dalam kotak, sedangkan float: left membuat elemen mengambang ke kiri sehingga kotak dapat tersusun berjajar. Properti background memberi warna berbeda pada setiap kotak.

5. Mengatur Clearfix dengan Properti clear
Langkah Pengerjaan
1. Buka kembali file lab4_box.html.
2. Tambahkan elemen keempat setelah div3:
<div class="div4">Div 4</div>
3. Tambahkan CSS berikut:
.div4 {
    background-color: blue;
    clear: left;
    float: none;
}
4. Simpan file dan refresh browser.
5. Coba ganti nilai clear menjadi both dan right, kemudian amati perubahannya.
Penjelasan
Properti clear mengatur posisi elemen terhadap elemen sebelumnya yang menggunakan float. Nilai clear: left mencegah elemen berada di samping elemen yang mengambang ke kiri. float: none membuat elemen keempat mengikuti aliran normal. Kotak keempat diberi warna biru agar mudah dibedakan.

6. Membuat Kerangka Layout Website
Langkah Pengerjaan
1. Buat folder lab4_layout.
2. Di dalamnya, buat file home.html dan style.css.
3. Hubungkan CSS dengan HTML menggunakan kode berikut di dalam <head>:
<link rel="stylesheet" href="style.css">
4. Buat kerangka website menggunakan elemen semantik:
<div id="container">
    <header>
        <h1>Layout Sederhana</h1>
    </header>

    <nav>
        <a href="home.html" class="active">Home</a>
        <a href="artikel.html">Artikel</a>
        <a href="about.html">About</a>
        <a href="kontak.html">Kontak</a>
    </nav>

    <section id="hero"></section>

    <section id="wrapper">
        <section id="main"></section>
        <aside id="sidebar"></aside>
    </section>

    <footer>
        <p>&copy; 2026 - Praktikum Web</p>
    </footer>
</div>
5. Tambahkan CSS dasar:
* {
    margin: 0;
    padding: 0;
}

body {
    line-height: 1;
    font-size: 100%;
    font-family: Arial, sans-serif;
    color: #5a5a5a;
}

#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

header {
    padding: 20px;
}

header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
6. Simpan dan buka home.html di browser untuk memeriksa kerangka halaman.
Penjelasan
Elemen <header> digunakan untuk bagian judul, <nav> untuk navigasi, <section> untuk mengelompokkan konten, <aside> untuk bagian samping, dan <footer> untuk bagian bawah halaman. #container menjadi pembungkus seluruh layout dan margin: 0 auto membuatnya berada di tengah halaman.
Screenshot

7. Mengatur Navigasi
Langkah Pengerjaan
1. Pastikan elemen <nav> sudah tersedia pada home.html.
2. Tambahkan CSS navigasi berikut ke style.css:
nav {
    display: block;
    background-color: #1f5faa;
}

nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}

nav a.active,
nav a:hover {
    background-color: #2b83ea;
}
3. Simpan file dan refresh browser.
4. Arahkan kursor ke menu untuk melihat perubahan warna hover.
Penjelasan
Navigasi digunakan untuk menyediakan tautan ke halaman lain. display: inline-block membuat tautan tersusun berjajar dan memungkinkan padding diterapkan. text-decoration: none menghilangkan garis bawah tautan. Class active menandai menu yang sedang dipilih, sedangkan :hover mengubah warna menu ketika kursor berada di atasnya

8. Membuat Hero Panel
Langkah Pengerjaan
1. Pada home.html, ganti <section id="hero"></section> dengan:
<section id="hero">
    <h1>Hello World!</h1>
    <p>
        Selamat datang di website praktikum CSS Layout.
        Halaman ini dibuat untuk mempelajari struktur
        dan tata letak website menggunakan HTML dan CSS.
    </p>.
    <a href="about.html" class="btn btn-large">Learn more &raquo;</a>
</section>
2. Tambahkan CSS berikut ke style.css:
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}

#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}

#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}

.btn {
    display: inline-block;
    padding: 8px 15px;
    background-color: #2b83ea;
    color: white;
    text-decoration: none;
    border-radius: 3px;
}

.btn:hover {
    background-color: #1f5faa;
}
3. Simpan dan refresh browser.
Penjelasan
Hero panel merupakan bagian pengenalan website yang berisi judul, deskripsi, dan tombol. Warna latar membedakan panel dari bagian lain. Padding mengatur ruang di dalam panel, sedangkan margin memberi jarak dengan elemen setelahnya.
Screenshot
(Screenshot/05.png)

9. Mengatur Main Content dan Sidebar
Langkah Pengerjaan
1. Pada home.html, isi bagian section id="wrapper" dengan konten utama dan sidebar:
<section id="wrapper">
    <section id="main">
        <h2>Konten Utama</h2>
        <p>Bagian ini berisi informasi utama website.</p>
    </section>

    <aside id="sidebar">
        <div class="widget-box">
            <h3 class="title">Widget Header</h3>
            <ul>
                <li><a href="#">Widget Link 1</a></li>
                <li><a href="#">Widget Link 2</a></li>
                <li><a href="#">Widget Link 3</a></li>
                <li><a href="#">Widget Link 4</a></li>
                <li><a href="#">Widget Link 5</a></li>
            </ul>
        </div>

        <div class="widget-box">
            <h3 class="title">Widget Text</h3>
            <p>Bagian sidebar berisi informasi tambahan.</p>
        </div>
    </aside>
</section>
2. Tambahkan CSS untuk kolom:
#wrapper {
    margin: 0;
}

#main {
    float: left;
    width: 640px;
    padding: 20px;
    box-sizing: border-box;
}

#sidebar {
    float: left;
    width: 340px;
    padding: 20px;
    box-sizing: border-box;
}
3. Tambahkan CSS untuk widget:
.widget-box {
    border: 1px solid #eee;
    margin-bottom: 20px;
}

.widget-box .title {
    padding: 10px 16px;
    background-color: #428bca;
    color: #fff;
}

.widget-box ul {
    list-style-type: none;
}

.widget-box li {
    border-bottom: 1px solid #eee;
}

.widget-box li a {
    padding: 10px 16px;
    color: #333;
    display: block;
    text-decoration: none;
}

.widget-box li:hover a {
    background-color: #eee;
}

.widget-box p {
    padding: 15px;
    line-height: 25px;
}
4. Simpan dan refresh browser.
Penjelasan
Main content merupakan area konten utama, sedangkan sidebar berisi informasi tambahan seperti widget dan tautan. Properti float: left meletakkan kedua bagian berdampingan. box-sizing: border-box membuat padding termasuk dalam perhitungan lebar kolom.


10. Menambahkan Tiga Kotak Konten
Langkah Pengerjaan
1. Di dalam section id="main", buat elemen div dengan class row.
2. Tambahkan tiga elemen dengan class box. Setiap kotak berisi gambar, judul, deskripsi, dan tautan detail. Contoh:
<div class="row">
    <div class="box">
        <img src="https://dummyimage.com/120/db7d25/fff.png"
             alt="Ilustrasi HTML" class="image-circle">
        <h3>HTML</h3>
        <p>HTML digunakan untuk menyusun struktur halaman web.</p>
        <a href="#" class="btn btn-default">View detail</a>
    </div>

    <div class="box">
        <img src="https://dummyimage.com/120/3e73e6/fff.png"
             alt="Ilustrasi CSS" class="image-circle">
        <h3>CSS</h3>
        <p>CSS digunakan untuk mengatur tampilan halaman web.</p>
        <a href="#" class="btn btn-default">View detail</a>
    </div>

    <div class="box">
        <img src="https://dummyimage.com/120/71e6d4/fff.png"
             alt="Ilustrasi Layout" class="image-circle">
        <h3>Layout</h3>
        <p>Layout membantu mengatur posisi elemen website.</p>
        <a href="#" class="btn btn-default">View detail</a>
    </div>
</div>
3. Tambahkan CSS berikut:
.box {
    display: block;
    float: left;
    width: 33.333333%;
    box-sizing: border-box;
    padding: 0 10px;
    text-align: center;
}

.box h3 {
    margin: 15px 0;
}

.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}

.box img {
    border: 0;
    vertical-align: middle;
}

.image-circle {
    border-radius: 50%;
}

.row {
    margin: 0 -10px;
    box-sizing: border-box;
}

.row::before,
.row::after,
.entry::before,
.entry::after {
    content: "";
    display: table;
}

.row::after,
.entry::after {
    clear: both;
}
4. Simpan dan refresh browser.
Penjelasan
Class .row menjadi pembungkus tiga kotak. Setiap .box menggunakan lebar sekitar sepertiga area agar ketiganya tersusun sejajar. text-align: center membuat konten berada di tengah, sedangkan border-radius: 50% membuat gambar berbentuk lingkaran.


11. Mengatur Footer
Langkah Pengerjaan
1. Pastikan elemen <footer> berada di bagian akhir #container pada home.html.
2. Tambahkan CSS berikut ke style.css:
footer {
    clear: both;
    background-color: #1d1d1d;
    padding: 20px;
    color: #eee;
    margin-top: 20px;
}
3. Simpan dan refresh browser.
Penjelasan
Footer merupakan bagian bawah website yang dapat berisi informasi hak cipta atau identitas situs. background-color memberi latar gelap, padding memberi ruang di dalam footer, dan clear: both memastikan footer berada di bawah elemen yang menggunakan float ke kiri atau kanan.


12. Jawaban Pertanyaan dan Tugas Modul
Tugas 1 — Menambahkan Layout untuk Menu About
Pertanyaan: Tambahkan layout untuk menu About, yaitu membuat single layout yang berisi deskripsi, portofolio, dan lain-lain.
Jawaban:
Halaman About digunakan untuk menampilkan informasi tentang profil, deskripsi diri, portofolio, dan tujuan. Halaman dibuat dalam file about.html dan menggunakan stylesheet style.css yang sama dengan halaman utama.
Buat file about.html di folder lab4_layout dengan kode berikut:
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About - Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>About</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="about.html" class="active">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <section id="hero">
            <h1>Tentang Saya</h1>
            <p>Halaman ini berisi informasi mengenai profil dan portofolio saya.</p>
        </section>

        <section id="main">
            <article class="entry">
                <h2>Deskripsi Diri</h2>
                <p>Saya adalah mahasiswa yang sedang mempelajari pemrograman web, khususnya HTML dan CSS.</p>
            </article>

            <hr class="divider">

            <article class="entry">
                <h2>Portofolio</h2>
                <p>Proyek yang dipelajari meliputi pembuatan halaman HTML, penggunaan CSS, dan pembuatan layout website sederhana.</p>
            </article>

            <hr class="divider">

            <article class="entry">
                <h2>Tujuan</h2>
                <p>Saya ingin meningkatkan kemampuan membuat website yang terstruktur dan mudah digunakan.</p>
            </article>
        </section>

        <footer>
            <p>&copy; 2026 - Praktikum Web</p>
        </footer>
    </div>
</body>
</html>
Cara pengerjaan:
1. Buat file about.html di dalam folder lab4_layout.
2. Hubungkan file dengan style.css.
3. Tambahkan navigasi dan tandai menu About menggunakan class active.
4. Tambahkan hero panel sebagai pengenalan halaman.
5. Gunakan elemen <article> untuk memisahkan deskripsi diri, portofolio, dan tujuan.
6. Simpan file dan buka di browser untuk memeriksa hasilnya.
Penjelasan: Elemen <article> digunakan untuk memisahkan bagian informasi agar lebih terstruktur. Penggunaan CSS yang sama membuat halaman About memiliki gaya yang konsisten dengan halaman Home.
Screenshot: Simpan hasil halaman About sebagai 9-about.png.

Tugas 2 — Menambahkan Layout untuk Menu Contact
Pertanyaan: Tambahkan layout untuk menu Contact yang berisi form isian nama, email, message, dan lain-lain.
Jawaban:
Halaman Contact menyediakan formulir agar pengunjung dapat memasukkan nama, email, subjek, dan pesan. Buat file kontak.html di folder lab4_layout dengan kode berikut:
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact - Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Contact</h1>
        </header>

        <nav>
            <a href="home.html">Home</a>
            <a href="about.html">About</a>
            <a href="kontak.html" class="active">Contact</a>
        </nav>

        <section id="hero">
            <h1>Hubungi Saya</h1>
            <p>Silakan isi formulir berikut untuk menyampaikan pertanyaan atau pesan.</p>
        </section>

        <section id="main">
            <h2>Formulir Kontak</h2>

            <form>
                <label for="nama">Nama Lengkap:</label>
                <input type="text" id="nama" name="nama"
                       placeholder="Masukkan nama lengkap" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email"
                       placeholder="Masukkan alamat email" required>

                <label for="subjek">Subjek:</label>
                <input type="text" id="subjek" name="subjek"
                       placeholder="Masukkan subjek pesan">

                <label for="pesan">Pesan:</label>
                <textarea id="pesan" name="pesan" rows="5"
                          placeholder="Tuliskan pesan kamu" required></textarea>

                <button type="submit">Kirim Pesan</button>
            </form>
        </section>

        <footer>
            <p>&copy; 2026 - Praktikum Web</p>
        </footer>
    </div>
</body>
</html>
Tambahkan CSS formulir berikut di bagian paling bawah style.css:
form {
    max-width: 500px;
    padding: 20px 0;
}

form label {
    display: block;
    margin: 15px 0 8px;
    font-weight: 600;
}

form input,
form textarea {
    width: 100%;
    box-sizing: border-box;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-family: inherit;
}

form textarea {
    resize: vertical;
}

form button {
    margin-top: 15px;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    background-color: #1f5faa;
    color: white;
    cursor: pointer;
}

form button:hover {
    background-color: #2b83ea;
}
Cara pengerjaan:
1. Buat file kontak.html.
2. Hubungkan file dengan style.css.
3. Tambahkan navigasi dan tandai menu Contact menggunakan class active.
4. Buat formulir menggunakan elemen <form>.
5. Tambahkan kolom nama, email, subjek, dan pesan.
6. Tambahkan tombol Kirim Pesan.
7. Tambahkan CSS untuk mengatur ukuran kolom, jarak, border, dan warna tombol.
8. Simpan dan buka halaman di browser, lalu uji pengisian formulir.
Penjelasan: Elemen <input type="text"> digunakan untuk nama dan subjek, sedangkan <input type="email"> digunakan untuk alamat email. Elemen <textarea> digunakan untuk pesan yang lebih panjang. Atribut required membuat kolom tertentu wajib diisi sebelum browser mengizinkan pengiriman formulir.
Catatan: Formulir ini baru menyediakan tampilan dan validasi dasar di browser. Pesan belum benar-benar dikirim ke email atau server karena belum menggunakan backend atau layanan pengiriman formulir.
Screenshot: Simpan hasil halaman Contact sebagai 10-contact.png.

13. Kesimpulan
Pada Praktikum 4: CSS Layout, saya mempelajari cara membuat layout website menggunakan HTML dan CSS. Praktikum dimulai dengan pembuatan box element serta penggunaan properti float dan clear untuk mengatur posisi elemen. Selanjutnya, saya membuat kerangka layout website yang terdiri dari header, navigasi, hero panel, main content, sidebar, kotak konten, dan footer.
Pada bagian tugas, saya membuat halaman About yang berisi deskripsi diri, portofolio, dan tujuan, serta halaman Contact yang menyediakan formulir nama, email, subjek, dan pesan. Saya juga mempelajari penggunaan elemen HTML semantik, penghubungan CSS eksternal, serta pentingnya mengambil screenshot sebagai dokumentasi setiap tahap pengerjaan.
Melalui praktikum ini, saya memahami bahwa HTML digunakan untuk membangun struktur halaman, sedangkan CSS digunakan untuk mengatur tampilan dan tata letak. Keduanya dapat digunakan bersama untuk membuat website yang lebih terstruktur dan mudah dipahami.