# SkincareStore - PHP Native

Proyek ini adalah aplikasi web sederhana berbasis **PHP Native** untuk toko skincare.
Dapat dijalankan menggunakan **Laragon** atau **XAMPP**.

---

## 🚀 Instalasi

### 1. Persiapan

* Pastikan sudah menginstal **Laragon** atau **XAMPP**.
* Pastikan **Git** sudah terpasang (opsional, jika ingin clone langsung).
* Aktifkan **Apache** dan **MySQL** dari control panel.

---

### 2. Clone Repository

Masuk ke direktori `www` (untuk Laragon) atau `htdocs` (untuk XAMPP).

**Laragon:**

```bash
cd C:\laragon\www
```

**XAMPP:**

```bash
cd C:\xampp\htdocs
```

Clone project:

```bash
git clone https://github.com/mdikifahriza/skincarestore.git
```

---

### 3. Buat Database

1. Buka [http://localhost/phpmyadmin](http://localhost/phpmyadmin).
2. Klik **New** → buat database dengan nama:

   ```
   db_skincare
   ```
3. Pilih database `db_skincare` → masuk tab **Import**.
4. Pilih file SQL di:

   ```
   skincarestore/database/db_skincare.sql
   ```
5. Klik **Go**.

---

### 4. Sesuaikan Koneksi Database

Buka file `koneksi.php` pada project, pastikan isinya seperti berikut:

```php
<?php
$server   = "localhost";
$username = "root";
$password = "";
$database = "db_skincare";

$conn = mysqli_connect($server, $username, $password, $database);

// cek koneksi
if (!$conn) {
    die('Koneksi Database Gagal : ' . mysqli_connect_error());
}
?>
```

Jika kamu menggunakan username/password MySQL yang berbeda, silakan sesuaikan pada variabel di atas.

---

### 5. Jalankan Project

* Buka browser.
* Akses:

  ```
  http://localhost/skincarestore
  ```
* Jika menggunakan Laragon, bisa langsung dengan:

  ```
  http://skincarestore.test
  ```

---

## ⚠️ Troubleshooting

* **Error mysqli connect** → cek `username` dan `password` MySQL di `koneksi.php`.
* **CSS/JS tidak tampil** → pastikan base URL sesuai.
* **Database kosong** → pastikan import file SQL sudah berhasil.

---

## 📂 Struktur Direktori

```
skincarestore/
│── database/
│   └── db_skincare.sql
│── assets/
│── koneksi.php
│── index.php
│── ...
```
username : dini
password : dini
---

## ✨ Teknologi yang Digunakan

* PHP Native
* MySQL
* HTML, CSS, JavaScript
