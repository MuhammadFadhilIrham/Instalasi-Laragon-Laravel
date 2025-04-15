# A. Instalasi Laragon

## 1. Download Laragon
   
Kunjungi: https://laragon.org/download/

![Screenshot 2025-04-15 121622](https://github.com/user-attachments/assets/eb6aaf2f-fe43-4629-a1ba-4c4d1b6fed32)

Pilih versi Laragon Full (biasanya ada PHP, MySQL, Node.js, Composer, dll).

Unduh dan install seperti biasa (Next → Next → Finish).

## 2. Setelah Install

- Jalankan Laragon.

![Screenshot 2025-04-15 121716](https://github.com/user-attachments/assets/0a6d63e0-0d18-45dd-ab07-2be2d91de95f)

- Klik tombol Start All untuk menjalankan Apache/Nginx dan MySQL.

---

# B. Cek & Install Laravel Requirements
Laravel butuh beberapa hal agar bisa berjalan:


| Requirement              | Keterangan                   |
|--------------------------|------------------------------|
| **Versi PHP**            | 8.1                          |
| **Composer**	            | Dependency manager           |
| **MySQL**	               | Untuk database               |
| **Node.js** _(opsional)_ | Untuk frontend build (Vite)  |

Catatan: Laragon Full sudah menyertakan PHP, Composer, dan MySQL. Tapi kamu bisa update PHP/Composer dari menu Tools > Quick Add > PHP Version, dll.

---

# C. Cara Instalasi Composer di Windows
Sebenarnya Laragon versi Full sudah include Composer, tapi kalau kamu mau install atau update Composer secara manual, ini dia caranya:

## 1. Download Composer Installer

- Buka: https://getcomposer.org/download/

![Screenshot 2025-04-15 203639](https://github.com/user-attachments/assets/761a4761-28cc-42a3-8124-778f47898271)


- Klik Composer-Setup.exe (Windows Installer)

## 2. Jalankan Installer

- Klik 2x Composer-Setup.exe

- Ikuti langkah-langkah berikut:

- Pilih PHP.exe (Laragon biasanya ada di C:\laragon\bin\php\php8.x\php.exe)

- Pilih Next → Next → Finish

## 3. Cek Apakah Composer Sudah Terinstall

Setelah selesai, buka Command Prompt (CMD) atau terminal, lalu ketik:

```bash
composer -V
```

Atau:

```bash
composer --version
```

Jika berhasil, akan muncul versi Composer seperti:

```yaml
Composer version 2.6.5 2024-03-10 12:34:56
```

---

# D. Install Laravel

```bash
composer create-project laravel/laravel nama-proyek
```

Atau jika ingin pakai versi tertentu:

```bash
composer create-project laravel/laravel:^10.0 nama-proyek
```

---

# E. Menjalankan Laravel

Ada dua cara umum untuk menjalankan aplikasi Laravel:

## 1. Jalankan Secara Manual via Terminal (php artisan serve)

Kamu bisa pakai command ini dari direktori project Laravel:

```bash
php artisan serve
```

Output-nya biasanya seperti ini:

```nginx
Starting Laravel development server: http://127.0.0.1:8000
```

Buka browser dan akses: http://127.0.0.1:8000

## 2. Jalankan Otomatis via Laragon (Rekomendasi untuk Pengguna Laragon)

Langkah:

- Pindahkan folder Laravel kamu ke direktori Laragon, contoh:
C:\laragon\www\nama-project

- Jalankan Laragon, lalu klik tombol Start All

- Buka browser dan akses:

```arduino
http://nama-project.test
```

Note: Laragon akan otomatis membuat virtual host .test jika kamu menaruh project di folder www.
