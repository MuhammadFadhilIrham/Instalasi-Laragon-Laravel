A. Instalasi Laragon

1. Download Laragon
   
Kunjungi: https://laragon.org/download/

![Screenshot 2025-04-15 121622](https://github.com/user-attachments/assets/eb6aaf2f-fe43-4629-a1ba-4c4d1b6fed32)

Pilih versi Laragon Full (biasanya ada PHP, MySQL, Node.js, Composer, dll).

Unduh dan install seperti biasa (Next → Next → Finish).

2. Setelah Install
Jalankan Laragon.

Klik tombol Start All untuk menjalankan Apache/Nginx dan MySQL.

B. Cek & Install Laravel Requirements
Laravel butuh beberapa hal agar bisa berjalan:


Requirement	Keterangan
PHP	Versi >= 8.1
Composer	Dependency manager
MySQL	Untuk database
Node.js (opsional)	Untuk frontend build (Vite)
Catatan: Laragon Full sudah menyertakan PHP, Composer, dan MySQL. Tapi kamu bisa update PHP/Composer dari menu Tools > Quick Add > PHP Version, dll.

C. Cara Instalasi Composer di Windows
Sebenarnya Laragon versi Full sudah include Composer, tapi kalau kamu mau install atau update Composer secara manual, ini dia caranya:

1. Download Composer Installer
Buka: https://getcomposer.org/download/

Klik Composer-Setup.exe (Windows Installer)

2. Jalankan Installer
Klik 2x Composer-Setup.exe

Ikuti langkah-langkah berikut:

Pilih PHP.exe (Laragon biasanya ada di C:\laragon\bin\php\php8.x\php.exe)

Pilih Next → Next → Finish

3. Cek Apakah Composer Sudah Terinstall
Setelah selesai, buka Command Prompt (CMD) atau terminal, lalu ketik:

bash
Salin
Edit
composer -V
Atau:

bash
Salin
Edit
composer --version
Jika berhasil, akan muncul versi Composer seperti:

yaml
Salin
Edit
Composer version 2.6.5 2024-03-10 12:34:56

D. Install Laravel
bash
Salin
Edit
composer create-project laravel/laravel nama-proyek
Atau jika kamu ingin pakai versi tertentu:

bash
Salin
Edit
composer create-project laravel/laravel:^10.0 nama-proyek
