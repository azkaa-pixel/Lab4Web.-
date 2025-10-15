<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/26c24ed2-d2eb-4491-b1b9-e144bf02aca5" /># Lab4 - Web

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
![foto]()

#### ```- penjelasan``` :

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
![foto]()

#### ```- penjelasan``` :

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
![foto]()

### 5. Membuat Layout Sederhana  
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
##### Kemudian buat kerangka layout dengan semantics element seperti berikut. 
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
![foto]()


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
![foto]()

#### ```- penjelasan``` :

### 6. Membuat Navigasi  
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

#### ```- hasil```
![foto]()

#### ```- penjelasan``` :

### 7. Membuat Hero Panel 
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
![foto]()

#### ```- penjelasan``` :

### 8. Mengatur Layout Main dan Sidebar 
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.  

```html

```

#### ```- hasil```
![foto]()

#### ```- penjelasan``` :
### 1. 

```html

```

#### ```- hasil```
![foto]()

#### ```- penjelasan``` :
### 1. 

```html

```

#### ```- hasil```
![foto]()

#### ```- penjelasan``` :
### 1. 

```html

```

#### ```- hasil```
![foto]()

#### ```- penjelasan``` :

