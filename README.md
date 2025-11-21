```markdown
# 📚 Modul Praktikum Basis Data - Bab 1 & 2

## 🎯 BAB 1 - Review Konversi ER Diagram ke Skema Relasi

### **Tujuan Pembelajaran**
- Memahami konversi diagram ER ke skema relasi dan tabel
- Memudahkan transformasi dari level konseptual ke level fisik basis data

### 📋 Topik Utama
1. Konversi ER → Skema Relasi → Diagram Relationship
2. Studi Kasus Skema Pembayaran Apotik

### 🔧 Aturan Konversi Penting

| Komponen ERD | Hasil Konversi | Keterangan |
|-------------|----------------|------------|
| **Entitas Kuat** | Tabel | Atribut menjadi kolom, PK tetap PK |
| **Atribut Komposit** | Multiple Kolom | Contoh: alamat → jalan, kota, provinsi |
| **Atribut Multivalue** | Tabel Terpisah | Wajib buat tabel baru |
| **Relasi 1:N** | FK di sisi 'many' | Tambah FK yang refer ke PK tabel 'one' |
| **Relasi N:N** | Tabel Penghubung | Buat tabel junction dengan FK dari kedua tabel |
| **Entitas Lemah** | Tabel + FK | Include FK yang refer ke entitas kuat |

### 📝 Evaluasi
- **Test Awal**: Identifikasi komponen ERD dan konversi sederhana
- **Test Akhir**: Konversi ERD kompleks ke kumpulan tabel

---

## 🚀 BAB 2 - Pengantar Basis Data & DDL

### **Tujuan Pembelajaran**
- Mengenal MySQL dan aplikasi pendukung
- Dapat mengakses MySQL dan memahami tipe data
- Menguasai perintah DDL dasar

### 💻 Teknis MySQL

#### **Akses MySQL via Command Line**
```bash
# Login ke MySQL
mysql -u root -p

# Perintah dasar
SHOW DATABASES;
USE nama_database;
```

Struktur File Database

OS Lokasi Database Lokasi PHP
Windows C:\xampp\mysql\data c:\xampp\htdocs
Linux /opt/lampp/var/mysql/ /opt/lampp/htdocs

📊 Tipe Data MySQL

Tipe Data Keterangan Format/Range
INT Angka bulat -2147483648 s/d 2147483647
FLOAT Angka desimal -
DATE Tanggal YYYY-MM-DD
DATETIME Tanggal & Waktu YYYY-MM-DD HH:MM:SS
VARCHAR(n) String 1-255 karakter
CHAR(n) String fixed 1-255 karakter

🛠️ Perintah DDL Dasar

```sql
-- Membuat database
CREATE DATABASE praktikum;

-- Melihat semua database
SHOW DATABASES;

-- Menggunakan database
USE praktikum;

-- Menghapus database
DROP DATABASE praktikum;
```
