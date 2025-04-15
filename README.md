A. Instalasi Laragon

1. Download Laragon
   
Kunjungi: https://laragon.org/download/

Pilih versi Laragon Full (biasanya ada PHP, MySQL, Node.js, Composer, dll).

Unduh dan install seperti biasa (Next → Next → Finish).

2. Setelah Install
Jalankan Laragon.

Klik tombol Start All untuk menjalankan Apache/Nginx dan MySQL.

✅ B. Cek & Install Laravel Requirements
Laravel butuh beberapa hal agar bisa berjalan:


Requirement	Keterangan
PHP	Versi >= 8.1
Composer	Dependency manager
MySQL	Untuk database
Node.js (opsional)	Untuk frontend build (Vite)
Catatan: Laragon Full sudah menyertakan PHP, Composer, dan MySQL. Tapi kamu bisa update PHP/Composer dari menu Tools > Quick Add > PHP Version, dll.

✅ C. Install Laravel Baru (Jika Tidak dari GitHub)
bash
Salin
Edit
composer create-project laravel/laravel nama-proyek
Atau jika kamu ingin pakai versi tertentu:

bash
Salin
Edit
composer create-project laravel/laravel:^10.0 nama-proyek
✅ D. Install Laravel dari GitHub (Clone Proyek)
1. Clone dari GitHub
bash
Salin
Edit
git clone https://github.com/username/repo-laravel.git
cd repo-laravel
2. Install Dependencies
bash
Salin
Edit
composer install
3. Copy File .env
bash
Salin
Edit
cp .env.example .env
4. Generate App Key
bash
Salin
Edit
php artisan key:generate
5. Set Database di .env
Contoh:

dotenv
Salin
Edit
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nama_db
DB_USERNAME=root
DB_PASSWORD=
6. Buat Database
Buka phpMyAdmin dari Laragon: http://localhost/phpmyadmin

Buat database sesuai nama di .env

7. Migrasi dan Seeding (jika ada)
bash
Salin
Edit
php artisan migrate
php artisan db:seed
8. Jalankan Server
bash
Salin
Edit
php artisan serve
Atau jika pakai Laragon, cukup simpan project di C:\laragon\www\nama-project, lalu akses via:

arduino
Salin
Edit
http://nama-project.test
