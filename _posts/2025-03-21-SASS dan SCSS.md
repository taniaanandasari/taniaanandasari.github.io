---
layout: post
title: <div class="bubble-effect blog-title">SASS DAN SCSS</div>
---

penjelasan tentang SASS DAN SCSS

![HTML link dan list]

---

🎨 Materi Lengkap SASS & SCSS
1️⃣ Apa Itu SASS & SCSS?
SASS (Syntactically Awesome Stylesheets) adalah preprocessor CSS yang memperluas kemampuan CSS dengan:

Variabel

Nested rules

Mixins

Functions

Inheritance

💡 SCSS adalah sintaks modern dari SASS yang lebih mirip CSS.

2️⃣ SASS vs SCSS
SASS	SCSS
Lebih lama / original	Sintaks yang lebih baru
Tidak pakai {} & ;	Pakai {} & ; seperti CSS
Ekstensi file: .sass	Ekstensi file: .scss

Contoh SASS:

sass
Copy
Edit
$primary-color: #333

body
  color: $primary-color
Contoh SCSS:

scss
Copy
Edit
$primary-color: #333;

body {
  color: $primary-color;
}
3️⃣ Kenapa Pakai SASS/SCSS?
✅ Mengelola CSS besar jadi mudah
✅ Bisa pakai variabel (warna, font dsb)
✅ Ada mixin & function → DRY (Don't Repeat Yourself)
✅ Bisa nesting (lebih rapi)

4️⃣ Fitur Utama
🔹 Variables
Menyimpan warna, font, ukuran dsb.

scss
Copy
Edit
$main-color: #3498db;
$padding: 20px;

.container {
  background: $main-color;
  padding: $padding;
}
🔹 Nesting
Menulis CSS lebih rapi.

scss
Copy
Edit
.navbar {
  ul {
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    text-decoration: none;
  }
}
🔹 Mixin
Seperti function untuk reusable code.

scss
Copy
Edit
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.box {
  @include flex-center;
  height: 100px;
}
🔹 Extend (Inheritance)
Berbagi properti.

scss
Copy
Edit
%btn-shared {
  padding: 10px 20px;
  border-radius: 5px;
}

.btn-primary {
  @extend %btn-shared;
  background: blue;
  color: white;
}

.btn-secondary {
  @extend %btn-shared;
  background: gray;
}
🔹 Operators
Bisa hitung langsung.

scss
Copy
Edit
.container {
  width: 100% - 20px;
}
🔹 Partials & Import
Pisah file → lebih rapi.

_header.scss

_footer.scss

Di file utama:

scss
Copy
Edit
@import 'header';
@import 'footer';
5️⃣ Instalasi & Compile
🔧 Pakai npm (Node.js)
1️⃣ Install:

bash
Copy
Edit
npm install -g sass
2️⃣ Compile:

bash
Copy
Edit
sass style.scss style.css
🔧 Langsung di VS Code
Install extension Live Sass Compiler.

Klik tombol “Watch Sass” → auto compile!

6️⃣ Kode HTML + SASS/SCSS (Contoh Lengkap)
📂 Struktur:
diff
Copy
Edit
index.html
style.scss
📄 index.html
html
Copy
Edit
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Contoh SASS</title>
    <link rel="stylesheet" href="style.css" />
</head>
<body>
    <div class="container">
        <h1>Halo SASS!</h1>
        <button class="btn-primary">Klik Aku</button>
        <button class="btn-secondary">Atau Aku</button>
    </div>
</body>
</html>
🖋️ style.scss
scss
Copy
Edit
$main-color: #3498db;
$secondary-color: #2ecc71;
$font-stack: Arial, sans-serif;

%btn-shared {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  font-family: $font-stack;
  cursor: pointer;
}

.container {
  text-align: center;
  padding: 50px;

  h1 {
    color: $main-color;
  }

  .btn-primary {
    @extend %btn-shared;
    background-color: $main-color;
    color: white;

    &:hover {
      background-color: darken($main-color, 10%);
    }
  }

  .btn-secondary {
    @extend %btn-shared;
    background-color: $secondary-color;
    color: white;

    &:hover {
      background-color: darken($secondary-color, 10%);
    }
  }
}
7️⃣ Cara Compile
Jika pakai Live Sass Compiler, klik "Watch Sass" di VS Code.
Atau terminal:

bash
Copy
Edit
sass style.scss style.css
8️⃣ Kelebihan & Kekurangan
✅ Lebih terstruktur
✅ DRY (Don't Repeat Yourself)
✅ Lebih scalable untuk proyek besar

❌ Butuh compile
❌ Bisa over-nesting kalau berlebihan

🔑 Kesimpulan
SASS/SCSS adalah alat bantu yang powerful untuk mengelola stylesheet. Sangat berguna saat proyek makin besar karena:

Kode lebih rapi & modular

Gampang ubah tema (cukup ubah variabel)

➡️ Cocok banget untuk developer web yang ingin meningkatkan workflow CSS!

![HTML Link dan Lists](/assets/images/gambar sass dan scss.png)