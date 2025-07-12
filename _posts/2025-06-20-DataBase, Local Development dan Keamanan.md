---
layout: post
title: <div class="bubble-effect blog-title">DataBase, Local Development dan Keamanan</div>
---

penjelasan tentang DataBase, Local Development dan Keamanan

![HTML link dan list]

---

📘 1. DATABASE
✅ Pengertian
Database (basis data) adalah kumpulan data yang terorganisir, disimpan secara sistematis, dan dapat diakses, dikelola, serta diperbarui secara efisien.

✅ Fungsi Database
Menyimpan data secara terstruktur.

Memudahkan pencarian dan manipulasi data.

Menjamin konsistensi dan integritas data.

Menghindari duplikasi data.

Meningkatkan efisiensi dalam pengelolaan data aplikasi.

✅ Jenis-Jenis Database
Jenis Database	Keterangan
Relasional (RDBMS)	Menggunakan tabel (MySQL, PostgreSQL, SQL Server)
Non-relasional (NoSQL)	Data fleksibel, tidak menggunakan tabel (MongoDB, Firebase)
Cloud Database	Dihosting di cloud (Google Cloud SQL, Amazon RDS)
Local Database	Dijalankan di komputer lokal (SQLite, MySQL XAMPP)

✅ Istilah Penting dalam Database
Istilah	Penjelasan
Tabel	Struktur tempat menyimpan data dalam baris dan kolom
Field (Kolom)	Atribut atau kategori data (misal: nama, umur)
Record (Baris)	Satu data lengkap untuk satu entitas
Primary Key	Kolom unik yang membedakan setiap record
Foreign Key	Kolom yang menghubungkan satu tabel dengan tabel lain
Query	Perintah SQL untuk mengakses/memanipulasi data

🖥️ 2. LOCAL DEVELOPMENT
✅ Pengertian
Local development adalah proses membangun dan menguji aplikasi pada komputer lokal (offline) sebelum dipublikasikan ke internet (server produksi).

✅ Tujuan Local Development
Mengembangkan aplikasi dengan cepat dan aman.

Menguji fitur tanpa mengganggu sistem online.

Menghemat biaya hosting selama pengembangan.

Mengurangi risiko bug di server asli.

✅ Tools Populer untuk Local Development
Tool	Fungsi
XAMPP / MAMP / WAMP	Server lokal yang menyediakan Apache, PHP, dan MySQL
VS Code / Sublime Text	Code editor
phpMyAdmin	Antarmuka grafis untuk mengelola MySQL
Git / GitHub	Kontrol versi dan kolaborasi
Node.js	Untuk aplikasi JavaScript di sisi server

✅ Struktur Umum Project Lokal (XAMPP)
pgsql
Copy
Edit
htdocs/
│
├── projekku/
│   ├── index.php
│   ├── koneksi.php
│   └── proses.php
🔐 3. KEAMANAN DATABASE DAN APLIKASI
✅ Mengapa Keamanan Penting?
Karena data bisa berisi informasi pribadi, rahasia perusahaan, transaksi, dll. Tanpa keamanan, data bisa dicuri, diubah, atau dihapus.

✅ Ancaman Umum pada Database dan Aplikasi
Ancaman	Penjelasan
SQL Injection	Teknik hacker memasukkan SQL berbahaya ke input form
XSS (Cross-Site Scripting)	Menyisipkan script jahat ke halaman web
Brute-force Attack	Menebak password secara otomatis
Data Leakage	Kebocoran data karena konfigurasi yang salah

✅ Praktik Keamanan yang Harus Dilakukan
🔒 1. Gunakan Prepared Statement
Untuk mencegah SQL Injection:

php
Copy
Edit
$stmt = $conn->prepare("SELECT * FROM users WHERE email = ?");
$stmt->bind_param("s", $email);
$stmt->execute();
🔒 2. Validasi & Sanitasi Input
Pastikan data dari user sudah diperiksa:

php
Copy
Edit
$username = htmlspecialchars($_POST['username']);
🔒 3. Gunakan Password Hashing
Jangan simpan password asli:

php
Copy
Edit
$hash = password_hash($password, PASSWORD_DEFAULT);
🔒 4. Batasi Akses Database
Jangan gunakan user root untuk aplikasi publik.

Buat user khusus dengan hak terbatas.

🔒 5. Jangan Simpan Info Sensitif di Kode
Simpan konfigurasi rahasia seperti password DB di file .env (kalau pakai framework) atau file terpisah yang tidak ditampilkan ke user.

🔒 6. Gunakan HTTPS (di server publik)
Enkripsi koneksi antara pengguna dan server agar data tidak disadap.

✅ KESIMPULAN
Topik	Inti
Database	Tempat menyimpan dan mengelola data aplikasi secara terstruktur.
Local Development	Cara mengembangkan aplikasi secara lokal sebelum dipublikasikan.
Keamanan	Upaya melindungi aplikasi dan data dari serangan dan kebocoran.

👉 Untuk menjadi web developer yang profesional, penting untuk memahami database, bekerja secara efisien di lingkungan lokal, dan selalu menjaga keamanan aplikasi sejak tahap pengembangan.

![HTML Link dan Lists](/assets/images/gambar database development.png)