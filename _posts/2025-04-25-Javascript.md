---
layout: post
title: <div class="bubble-effect blog-title">JAVASCRIPT</div>
---

penjelasan tentang JAVASCRIPT

![HTML link dan list]

---

📖 Materi Lengkap Tentang JavaScript
1️⃣ Apa Itu JavaScript?
JavaScript adalah bahasa pemrograman tingkat tinggi yang:

Digunakan untuk membuat halaman web interaktif

Dijalankan di browser

Termasuk dalam 3 teknologi utama web:

HTML (struktur)

CSS (tampilan)

JavaScript (fungsi/aksi)

➡️ Contoh: Validasi form, slider gambar, animasi, game, dan aplikasi web seperti Google Maps.

2️⃣ Sejarah Singkat
1995: Dibuat oleh Brendan Eich di Netscape.

Awalnya bernama Mocha, lalu LiveScript, dan akhirnya jadi JavaScript.

ECMAScript: Standar resmi JavaScript (pertama kali rilis 1997).

3️⃣ Jenis-Jenis JavaScript
Sebenarnya bahasa JavaScript itu satu, tapi ada implementasi & penggunaannya yang berbeda:

Client-side JavaScript:
Dijalanin di browser (paling umum).

Server-side JavaScript:
Pakai platform seperti Node.js untuk buat server & backend.

Framework & Library:
Misalnya:

ReactJS (frontend)

Angular, Vue.js

jQuery (lama tapi masih dipakai)

4️⃣ Kelebihan JavaScript
✅ Mudah dipelajari
✅ Didukung semua browser
✅ Bisa fullstack (frontend + backend)
✅ Banyak framework & tools
✅ Interaktif & real-time

5️⃣ Kekurangan JavaScript
❌ Bisa dimatikan di browser (tidak jalan)
❌ Kurang aman jika tidak hati-hati
❌ Berjalan di client (terkadang berat untuk proses besar)

6️⃣ Konsep-Konsep Utama
🛠️ DOM (Document Object Model):
Cara JavaScript berinteraksi & memanipulasi HTML/CSS.

👀 Event-Driven:
Menanggapi aksi user (klik, input, hover).

🔄 Asynchronous (AJAX, Fetch):
Bisa mengambil data tanpa reload halaman.

📦 Modular & Reusable:
Bisa buat fungsi & module yang reusable.

7️⃣ Tipe Data di JavaScript
String

Number

Boolean

Array

Object

Null

Undefined

➡️ Mulai ES6 ada juga Symbol & BigInt.

8️⃣ Penggunaan JavaScript
✨ Frontend:
Validasi form

Animasi & efek visual

Interaksi tombol/menu

🔧 Backend:
Node.js untuk buat server (misalnya: API, database)

💻 Fullstack:
Menggunakan JavaScript di frontend + backend sekaligus (misal: MERN stack = MongoDB, Express, React, Node)

9️⃣ Tools & Framework Populer
Frontend	Backend
ReactJS	Node.js
Vue.js	Express
Angular	NestJS

Library lain: jQuery, D3.js (grafik), Chart.js

🔟 Versi & Fitur Baru (ES6 ke atas)
let & const

Arrow function: () => {}

Template literal: `Halo ${nama}`

Destructuring

Class & Object Enhancements

Promises & Async/Await

🔑 Peran JavaScript di Dunia Web
Tanpa JavaScript, web hanya statis.
JavaScript membuat web:

Lebih hidup

Bisa berinteraksi

Mendukung aplikasi real-time (chat, notifikasi)

📝 Kesimpulan
JavaScript adalah bahasa wajib untuk web developer. Dengan JavaScript, kamu bisa buat:

Website yang interaktif

Aplikasi skala kecil sampai besar

Backend server & API

💡 Tips: Kuasai dasar-dasarnya dulu (DOM, event, function) sebelum lanjut ke framework seperti React/Vue.

Cara Menulis JavaScript
a. Di dalam HTML:
html
Copy
Edit
<script>
  console.log("Halo Dunia!");
</script>
b. Di file terpisah:
html
Copy
Edit
<script src="script.js"></script>
Kelebihan: Kode jadi lebih rapi & mudah di-maintain.

3️⃣ Variabel & Tipe Data
a. Cara Deklarasi:
let (bisa diubah)

const (tetap)

var (lama, jarang dipakai sekarang)

js
Copy
Edit
let nama = "Budi";
const umur = 20;
var aktif = true;
b. Tipe Data:
String: "teks"

Number: 123

Boolean: true/false

Array: ["apel", "jeruk"]

Object: {nama: "Budi"}

Null & Undefined

4️⃣ Operator
Jenis	Contoh
Aritmatika	+ - * / %
Perbandingan	== != > <
Logika	`&&
Penugasan	= += -=

Contoh:

js
Copy
Edit
let a = 5, b = 10;
console.log(a + b);  // 15
console.log(a > b);  // false
5️⃣ Percabangan
Digunakan untuk keputusan.

js
Copy
Edit
let nilai = 80;
if (nilai >= 75) {
  console.log("Lulus");
} else {
  console.log("Tidak Lulus");
}
6️⃣ Perulangan
a. For Loop:
js
Copy
Edit
for (let i = 0; i < 5; i++) {
  console.log(i);
}
b. While Loop:
js
Copy
Edit
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
7️⃣ Function (Fungsi)
Fungsi = blok kode yang bisa dipanggil ulang.

js
Copy
Edit
function sapa(nama) {
  return "Halo " + nama;
}
console.log(sapa("Budi"));
➡️ Bisa juga pakai Arrow Function:

js
Copy
Edit
const sapa = (nama) => "Halo " + nama;
8️⃣ Array & Object
a. Array:
js
Copy
Edit
let buah = ["Apel", "Mangga"];
console.log(buah[0]);  // Apel
b. Object:
js
Copy
Edit
let mahasiswa = {
  nama: "Budi",
  umur: 20
};
console.log(mahasiswa.nama);  // Budi
9️⃣ Event (Interaksi User)
html
Copy
Edit
<button onclick="alert('Tombol diklik!')">Klik Aku</button>
🔟 Manipulasi DOM (Document Object Model)
Tujuan: Mengubah isi/tampilan web secara dinamis.

html
Copy
Edit
<p id="demo">Halo Dunia!</p>
<button onclick="ubah()">Ubah Teks</button>

<script>
function ubah() {
  document.getElementById("demo").innerHTML = "Teks sudah diubah!";
}
</script>
11️⃣ Validasi Form Sederhana
html
Copy
Edit
<form onsubmit="return cekForm()">
  <input type="text" id="nama" placeholder="Masukkan Nama">
  <button type="submit">Submit</button>
</form>

<script>
function cekForm() {
  let nama = document.getElementById("nama").value;
  if (nama === "") {
    alert("Nama wajib diisi!");
    return false;
  }
  alert("Form berhasil disubmit!");
  return true;
}
</script>
12️⃣ Fetch API (Ambil Data Online)
js
Copy
Edit
fetch('https://jsonplaceholder.typicode.com/posts')
  .then(response => response.json())
  .then(data => console.log(data));

  ![HTML Link dan Lists](/assets/images/gambar javascript.jpeg)
