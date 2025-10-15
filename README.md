# Lab4 - Web

Nama : Ghefira Azka Fardani 

NIM : 312410521

Kelas : TI.24.A5

### 1. Langkah-langkah Praktikum 
Persiapan membuat dokumen HTML dengan nama file lab4_box.html seperti berikut. 

```html
<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>Box Element</title> 
</head> 
<body> 
    <header> 
        <h1>Box Element</h1> 
    </header> 
</body> 
</html> 
```

### 2. Membuat Box Element 
Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut. 

```html
<section> 
    <div class="div1">Div 1</div> 
    <div class="div2">Div 2</div> 
    <div class="div3">Div 3</div>       
</section> 
```
#### ```- penjelasan``` : 
Kode tersebut berfungsi untuk membuat satu bagian halaman web menggunakan tag ```<section>``` yang berisi tiga kotak ```<div>``` bernama ```div1```, ```div2```, dan ```div3```. Setiap kotak bisa diatur tampilannya secara terpisah menggunakan class pada CSS, misalnya untuk memberi warna, ukuran, atau posisi yang berbeda.

### 3. CSS Float Property 
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut. 

```html
<style>     div {         float:left;         padding: 10px;  
    }     .div1 { 
        background: red; 
    }     .div2 { 
        background: yellow; 
    }     .div3 { 
        background: green; 
    } 
</style> 
```

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/bf07d2f2ceef39aa6f48ebcc2d4ba120777e35cb/praktikum%204/1.jpeg)

#### ```- penjelasan``` :
Kode tersebut digunakan untuk mengatur tampilan tiga elemen ```<div>```. Semua ```<div>``` diberi gaya agar posisinya sejajar ke kiri ```(float: left)``` dan memiliki jarak dalam kotak ```(padding: 10px)```. Lalu setiap class diberi warna berbeda: .div1 berwarna merah, .div2 berwarna kuning, dan .div3 berwarna hijau.

### 4. Mengatur Clearfix Element 
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk mengaturnya. 

Tambahkan element div lainnya seteleah div3 seperti berikut. 

```html
<section> 
    <div class="div1">Div 1</div> 
    <div class="div2">Div 2</div> 
    <div class="div3">Div 3</div>   
    <div class="div4">Div 4</div>    
</section> 
```
##### Kemudian atur property clear pada CSS, seperti berikut. 
```html
.div4 { 
    background-color: blue; 
    clear: left;     float: none; 
} 
```
#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/bf07d2f2ceef39aa6f48ebcc2d4ba120777e35cb/praktikum%204/2.jpeg)

#### ```- penjelasan``` :
Kode tersebut mengatur tampilan untuk elemen dengan class ```.div4```. Warna latar belakangnya dibuat biru (```background-color: blue```), lalu diberi properti ```clear: left``` agar posisinya tidak sejajar dengan elemen sebelumnya yang menggunakan ```float: left```, melainkan tampil di bawahnya. Properti float: none digunakan untuk menonaktifkan efek float sehingga kotak ```.div4``` berada di baris baru.

### Lakukan eksperimen terhadap penggunaan property clear dengan nilai lainnya (left, both, right), dan amati perubahannya.  

```html
 <style>  
            div {
            float: both;
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

        .div4 {
            background-color: blue;
            clear: right;
            float: none;
        }   
    </style> 
```

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/bf07d2f2ceef39aa6f48ebcc2d4ba120777e35cb/praktikum%204/3.jpeg)

# Membuat Layout Sederhana  

Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama home.html, dan file css dengan nama style.css. 

```html
<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>Layout Sederhana</title> 
    <link rel="stylesheet" href="style.css"> 
</head> 
<body> 
    <div id="container"> 
         
    </div> 
</body> 
</html> 
```
##### Kemudian tulis kode berikut

```html
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
    <p>&copy; 2021 - Universitas Pelita Bangsa</p> </footer> 
```
#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/bf07d2f2ceef39aa6f48ebcc2d4ba120777e35cb/praktikum%204/4.jpeg)

### Kemudian tambahkan kode CSS untuk membuat layoutnya.  

```html
/* import google font */ 
@import 
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400 ;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap'); 
@import 
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0 ,300;0,700;1,300&display=swap'); 
 
/* Reset CSS */ 
* {     margin: 0;     padding: 0; 
}  body { 
    line-height:1;     font-size:100%; 
    font-family:'Open Sans', sans-serif;     color:#5a5a5a; 
} 
 
#container {     width: 980px;     margin: 0 auto; 
    box-shadow: 0 0 1em #cccccc; 
} 
 
/* header */ header { 
    padding: 20px; 
}  
header h1 { 
    margin: 20px 10px;     color: #b5b5b5; 
} 
```

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/bf07d2f2ceef39aa6f48ebcc2d4ba120777e35cb/praktikum%204/5.jpeg)

#### ```- penjelasan``` :
- ```@import``` digunakan untuk mengambil dua jenis font dari Google Fonts (```Open Sans``` dan ```Open Sans Condensed```) agar teks terlihat lebih menarik.
  
- Bagian ```* { margin: 0; padding: 0; }``` disebut reset CSS, fungsinya menghapus jarak bawaan dari semua elemen supaya tata letak lebih konsisten.
  
- ```body``` mengatur tampilan dasar seluruh halaman, seperti tinggi baris (```line-height```), ukuran huruf (```font-size```), jenis font, dan warna teks.
  
- ```#container``` berfungsi sebagai pembungkus utama seluruh isi halaman dengan lebar tetap (```width: 980px```), berada di tengah (```margin: 0 auto```), dan diberi efek bayangan halus (```box-shadow```).
  
- ```header``` dan ```header h1``` mengatur bagian kepala halaman, memberi jarak dalam (```padding``` dan ```margin```) serta memberi warna abu-abu muda pada teks judul.

### Membuat Navigasi  
Kemudian selanjutnya mengatur navigasi. 
```html
/* navigasi */ nav { 
    display: block; 
    background-color: #1f5faa; 
}  nav a { 
    padding: 15px 30px;     display: inline-block;     color: #ffffff;     font-size: 14px;     text-decoration: none;     font-weight: bold; 
}  nav a.active, nav a:hover { 
    background-color: #2b83ea; } 
```

#### ```- penjelasan``` :
- ```nav``` dibuat tampil sebagai blok penuh (```display: block```) dan diberi warna latar biru tua (```background-color: #1f5faa```).
  
- ```nav a``` mengatur tampilan setiap tautan di dalam navbar, seperti memberi jarak (```padding: 15px 30px```), menampilkan secara horizontal (```display: inline-block```), memberi warna teks putih, ukuran huruf 14px, huruf tebal (```font-weight: bold```), dan menghilangkan garis bawah (```text-decoration: none```).
  
- ```nav a.active, nav a:hover``` memberi efek saat tautan sedang aktif atau disorot kursor, yaitu mengubah warna latarnya menjadi biru lebih terang (```#2b83ea```) agar terlihat interaktif.

### Membuat Hero Panel 
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut. 
 
```html
<section id="hero"> 
    <h1>Hello World!</h1> 
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p> 
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a> </section> 
```
```html
/* Hero Panel */ #hero { 
    background-color: #e4e4e5;     padding: 50px 20px;     margin-bottom: 20px; 
} 
 #hero h1 {     margin-bottom: 20px;     font-size: 35px; 
} 
 #hero p { 
    margin-bottom: 20px;     font-size: 18px;     line-height: 25px; 
} 
```

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/f90d1dcaccc69a26fb6fe2fdab22f8f104c184d8/praktikum%204/6.jpeg)

#### ```- penjelasan``` :
- ```#hero`` mengatur seluruh area hero dengan warna latar abu-abu muda (```background-color: #e4e4e5```), memberi jarak dalam (```padding: 50px 20px```), dan jarak bawah (```margin-bottom: 20px```) agar terpisah dari bagian lain.

- ```#hero h1``` mengatur judul di dalam hero agar lebih menonjol, dengan jarak bawah (margin-bottom: 20px) dan ukuran huruf besar (font-size: 35px).

- #hero p mengatur paragraf deskripsi di dalam hero dengan jarak bawah (```margin-bottom: 20px```), ukuran huruf sedang (```font-size: 18px```), dan tinggi baris (```line-height: 25px```) supaya teks mudah dibaca.

### Mengatur Layout Main dan Sidebar 
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.  

```html
/* main content */ 
#wrapper {     margin: 0; } 
 #main {     float: left;     width: 640px;     padding: 20px; 
} 
 
/* sidebar area */ #sidebar {     float: left;     width: 260px;     padding: 20px; 
} 
```

#### ```- penjelasan``` :
- ```#wrapper``` menjadi pembungkus utama untuk bagian konten dan sidebar, dengan ```margin: 0``` agar tidak ada jarak luar.

- ```#main``` adalah area konten utama, diletakkan di sebelah kiri dengan ```float: left```, lebar 640px, dan diberi jarak dalam (```padding: 20px```) agar isi teks tidak menempel ke tepi.

- #sidebar adalah area samping (sidebar) yang juga diletakkan di kiri menggunakan float: left, memiliki lebar 260px, dan jarak dalam (padding: 20px) untuk memberi ruang di sekitar isi sidebar.

### Membuat Sidebar Widget 
Kemudian selanjutnya menambahkan element lain dalam sidebar.  

```html
<aside id="sidebar"> 
    <div class="widget-box"> 
        <h3 class="title">Widget Header</h3> 
        <ul> 
            <li><a href="#">Widget Link</a></li> 
            <li><a href="#">Widget Link</a></li> 
            <li><a href="#">Widget Link</a></li> 
            <li><a href="#">Widget Link</a></li> 
            <li><a href="#">Widget Link</a></li> 
        </ul> 
    </div> 
    <div class="widget-box"> 
        <h3 class="title">Widget Text</h3> 
        <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p> 
    </div> 
</aside> 
```
##### Kemudian tambahkan CSS. 
```html
/* widget */ .widget-box { 
    border:1px solid #eee;     margin-bottom:20px; 
} 
 
.widget-box  .title {     padding:10px 16px;     background-color:#428bca;     color:#fff; 
} 
 
.widget-box ul { 
    list-style-type:none; 
} 
 
.widget-box li { 
    border-bottom:1px solid #eee; 
} 
 
.widget-box li a {     padding:10px 16px;     color:#333;     display:block;     text-decoration:none; 
} 
 
.widget-box li:hover a {     background-color:#eee; 
} 
 
.widget-box p {     padding:15px;     line-height:25px; 
} 
```

#### ```- penjelasan``` :
- ```.widget-box``` memberi bingkai tipis dan jarak bawah antar widget.

- ```.widget-box .title`` membuat judul berlatar biru dengan teks putih.

- ```.widget-box ul``` menghapus tanda bullet pada daftar.

- ```.widget-box li``` menambahkan garis pemisah antar item.

- ```.widget-box li``` a menata tautan dengan jarak, warna abu tua, dan tanpa garis bawah.

- ```.widget-box li:hover a``` memberi efek abu-abu saat kursor diarahkan.

- ```.widget-box p``` mengatur teks paragraf dengan jarak dan spasi agar mudah dibaca.


### Mengatur Footer 
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer. 
 
```html
/* footer */ footer {     clear:both; 
    background-color:#1d1d1d;     padding:20px;     color:#eee; 
} 
```

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/f90d1dcaccc69a26fb6fe2fdab22f8f104c184d8/praktikum%204/7.jpeg)

#### ```- penjelasan``` :
Kode tersebut digunakan untuk mengatur tampilan bagian footer pada halaman web. Footer diberi warna latar hitam keabu-abuan (```#1d1d1d```), teks berwarna abu muda (```#eee```), serta jarak dalam (```padding: 20px```). Properti ```clear: both``` digunakan agar footer tampil di bawah semua elemen yang menggunakan ```float```.

### Menambahkan Elemen lainnya pada Main Content  

```html
<section id="main"> 
    <div class="row"> 
        <div class="box"> 
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">             <h3>Heading</h3> 
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p> 
            <a href="#" class="btn btn-default">View detail</a> 
        </div> 
        <div class="box"> 
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">             <h3>Heading</h3> 
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p> 
            <a href="#" class="btn btn-default">View detail</a> 
        </div> 
        <div class="box"> 
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">             <h3>Heading</h3> 
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p> 
            <a href="#" class="btn btn-default">View detail</a> 
        </div> 
    </div> 
</section> 
```
##### Kemudian tambahkan CSS. 
``` html
/* box */ .box { 
    display:block;     float:left;     width:33.333333%;     box-sizing:border-box;     -moz-box-sizing:border-box; 
    -webkit-box-sizing:border-box; 
    padding:0 10px;     text-align:center; 
} 
 
.box h3 { 
    margin: 15px 0; 
} 
 
.box p { 
    line-height: 20px;     font-size: 14px;     margin-bottom: 15px; 
}  box img {     border: 0; 
    vertical-align: middle; 
} 
 
.image-circle { 
    border-radius: 50%; 
} 
 .row { 
    margin: 0 -10px;     box-sizing: border-box;     -moz-box-sizing: border-box; 
    -webkit-box-sizing: border-box; 
} 
 
.row:after, .row:before, .entry:after, .entry:before {     content:'';     display:table; 
} 
 
.row:after, .entry:after {     clear:both; 
} 
```

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/f90d1dcaccc69a26fb6fe2fdab22f8f104c184d8/praktikum%204/8.jpeg)

#### ```- penjelasan``` :
Kode tersebut digunakan untuk menampilkan tiga kotak konten utama di dalam bagian <```section id="main"```>.
Setiap kotak berada di dalam <```div class="box"```> yang berisi gambar berbentuk lingkaran, judul (h3), paragraf teks penjelasan, dan tombol tautan bertuliskan “View detail”. Ketiga kotak ini biasanya ditampilkan berdampingan secara horizontal menggunakan CSS agar terlihat seperti tiga fitur utama di halaman web.

### Menambahkan Content Artikel 
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content. 
```html
<hr class="divider" /> 
<article class="entry"> 
    <h2>First featurette heading.</h2> 
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""> 
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p> 
</article> 
<hr class="divider" /> 
<article class="entry"> 
    <h2>First featurette heading.</h2> 
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img"> 
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p> 
</article> 
```
##### Kemudian tambahkan CSS

```html
.divider {     border:0; 
    border-top:1px solid #eeeeee;     margin:40px 0; 
} 
 
/* entry */ .entry { 
    margin: 15px 0; 
} 
 
.entry h2 { 
    margin-bottom: 20px; 
} 
 .entry p { 
    line-height: 25px; 
} 
 
.entry img {     float: left;     border-radius: 5px;     margin-right: 15px; 
} 
 
.entry .right-img {     float: right; 
} 
```

#### ```- hasil```
![foto](https://github.com/azkaa-pixel/Lab4Web.-/blob/f90d1dcaccc69a26fb6fe2fdab22f8f104c184d8/praktikum%204/9.jpeg)

#### ```- penjelasan``` :
Kode tersebut digunakan untuk menambahkan dua bagian artikel (featurette) di halaman web. Setiap artikel berada dalam tag ```<article class="entry">``` dan berisi judul (h2), gambar, serta teks paragraf sebagai isi artikel. Tag ```<hr class="divider" />``` berfungsi sebagai garis pemisah antarartikel. Gambar pada artikel kedua diberi class ```right-img```, yang biasanya digunakan untuk meletakkan gambar di sisi kanan teks menggunakan CSS.

# Pertanyaan dan Tugas 

1.	Tambahkan Layout untuk menu About 
=> buat single layout yang berisi deskripsi, portfolio, dll 
2.	Tambahkan layout untuk menu Contact 
=> yang berisi form isian: nama, email, message, dll 

### 1.
```html
<section id="about">
        <h2>Tentang Kami</h2>
        <p>
          Website ini dibuat untuk menampilkan contoh layout sederhana dengan
          HTML dan CSS. Halaman ini berisi deskripsi singkat serta portofolio.
        </p>
        <div class="row">
          <div class="box">
            <img
              src="https://dummyimage.com/150/3e73e6/fff.png"
              class="image-circle"
              alt="Project 1"
            />
            <h3>Project 1</h3>
            <p>Deskripsi singkat tentang project pertama.</p>
          </div>
          <div class="box">
            <img
              src="https://dummyimage.com/150/71e6d4/fff.png"
              class="image-circle"
              alt="Project 2"
            />
            <h3>Project 2</h3>
            <p>Deskripsi singkat tentang project kedua.</p>
          </div>
        </div>
      </section>
```

#### ```- hasil```
![foto]()

#### ```- penjelasan``` :

### 2.
```html
      <section id="kontak">
        <h2>Hubungi Kami</h2>
        <p>
          Silakan isi form di bawah ini untuk mengirim pesan atau pertanyaan.
        </p>

        <form>
          <label for="nama">Nama:</label>
          <input type="text" id="nama" name="nama" required />

          <label for="email">Email:</label>
          <input type="email" id="email" name="email" required />

          <label for="pesan">Pesan:</label>
          <textarea id="pesan" name="pesan" rows="5" required></textarea>

          <button type="submit">Kirim Pesan</button>
        </form>
      </section>
```

#### ```- hasil```
![foto]()

#### ```- penjelasan``` :

