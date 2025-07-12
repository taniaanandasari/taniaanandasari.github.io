---
layout: post
title: <div class="bubble-effect blog-title">Koneksi DataBase MySQL dengan PHP</div>
---

penjelasan tentang Koneksi DataBase MySQL dengan PHP

![HTML link dan list]

---

📌 PENGERTIAN KONEKSI DATABASE MYSQL DENGAN PHP
Koneksi database adalah proses menghubungkan aplikasi (dalam hal ini PHP) ke sistem manajemen basis data (dalam hal ini MySQL), agar aplikasi bisa mengakses, menyimpan, mengubah, atau menghapus data.

PHP (Hypertext Preprocessor) menyediakan berbagai cara untuk berinteraksi dengan MySQL, salah satunya adalah dengan MySQLi atau PDO (PHP Data Objects).

📘 TEKNIK KONEKSI DATABASE MYSQL DENGAN PHP
Terdapat dua metode umum:

✅ 1. MySQLi (MySQL Improved)
MySQLi hanya dapat digunakan untuk MySQL saja.

🔧 Contoh Koneksi:
php
Copy
Edit
<?php
$host = "localhost";     // Alamat server database
$user = "root";          // Username MySQL
$pass = "";              // Password MySQL (default XAMPP kosong)
$db   = "nama_database"; // Nama database

// Membuat koneksi
$conn = mysqli_connect($host, $user, $pass, $db);

// Cek koneksi
if (!$conn) {
    die("Koneksi gagal: " . mysqli_connect_error());
} else {
    echo "Koneksi berhasil!";
}
?>
✅ 2. PDO (PHP Data Objects)
PDO mendukung berbagai jenis database, lebih fleksibel dan aman dengan fitur prepared statement.

🔧 Contoh Koneksi:
php
Copy
Edit
<?php
$host = "localhost";
$db   = "nama_database";
$user = "root";
$pass = "";

try {
    $conn = new PDO("mysql:host=$host;dbname=$db", $user, $pass);
    // Set mode error menjadi exception
    $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    echo "Koneksi berhasil!";
} catch(PDOException $e) {
    echo "Koneksi gagal: " . $e->getMessage();
}
?>
📂 PENJELASAN SETIAP BAGIAN
Bagian	Penjelasan
$host	Alamat dari server database, biasanya localhost saat development
$user	Username untuk login ke database, default-nya root untuk XAMPP/MAMP
$pass	Password untuk user MySQL. Default di XAMPP seringkali kosong ""
$db	Nama database yang ingin dihubungkan
mysqli_connect	Fungsi PHP untuk membuat koneksi ke database MySQL
PDO	Class PHP yang digunakan untuk koneksi fleksibel ke banyak jenis database

📌 CONTOH PENGGUNAAN QUERY SETELAH TERHUBUNG
🔍 SELECT (menampilkan data)
php
Copy
Edit
$result = mysqli_query($conn, "SELECT * FROM mahasiswa");

while($row = mysqli_fetch_assoc($result)) {
    echo $row['nama'] . "<br>";
}
✍️ INSERT (menambah data)
php
Copy
Edit
mysqli_query($conn, "INSERT INTO mahasiswa (nama, nim) VALUES ('Tania', '20230101')");
⚠️ HAL YANG HARUS DIPERHATIKAN
Database harus sudah dibuat di phpMyAdmin atau CLI MySQL.

Nama database, tabel, dan kolom harus sesuai dengan yang di kode.

Gunakan prepared statement untuk keamanan (terutama untuk input dari user).

Cek error menggunakan mysqli_connect_error() atau try...catch jika pakai PDO.

Jangan lupa tutup koneksi jika sudah selesai (mysqli_close($conn);).

✅ KELEBIHAN DAN KEKURANGAN MYSQLi vs PDO
Fitur	MySQLi	PDO
Mendukung database	Hanya MySQL	Banyak jenis DB (MySQL, SQLite, PostgreSQL, dll)
Prepared Statement	Ya	Ya
Orientasi objek	Ya (OOP & prosedural)	Ya (OOP)
Keamanan	Cukup	Lebih baik
Kelebihan utama	Simpel	Fleksibel dan aman

📌 KESIMPULAN
Koneksi database adalah hal wajib dalam aplikasi web berbasis PHP.

PHP menyediakan dua metode koneksi utama: MySQLi dan PDO.

Gunakan PDO jika ingin aplikasi yang lebih fleksibel dan aman.

Pastikan parameter koneksi (host, user, password, dbname) benar agar tidak gagal koneksi.

![HTML Link dan Lists](/assets/images/gambar koneksi database.png)