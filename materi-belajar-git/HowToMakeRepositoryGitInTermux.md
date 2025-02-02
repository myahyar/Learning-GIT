# How to make a repository git in termux
1. Install Git di Termux

Jika Git belum terpasang, jalankan perintah:
```
pkg update && pkg upgrade
pkg install git
```
2. Konfigurasi Git (Opsional, tapi direkomendasikan)

Jika ini pertama kali kamu menggunakan Git, atur nama dan email:
```
git config --global user.name "NamaKamu"
git config --global user.email "email@example.com"
```
3. Buat Folder Repository

Pilih lokasi penyimpanan dan buat folder proyek:
```
mkdir nama_repo
cd nama_repo
```
4. Inisialisasi Repository

Jalankan perintah berikut untuk menjadikan folder sebagai repository Git:
```
git init
```
Ini akan membuat folder tersembunyi .git yang menyimpan konfigurasi repository.

5. Tambahkan File ke Repository

Buat file baru atau tambahkan file yang sudah ada, misalnya:
```
echo "Hello, Git!" > README.md
git add .
```
6. Commit Perubahan
```
git commit -m "Inisialisasi repository"
```
7. Hubungkan ke GitHub (Opsional, untuk push ke GitHub)

Jika belum memiliki token GitHub, buat di GitHub Personal Access Token.

Lalu jalankan perintah berikut untuk menambahkan remote repository:

```
git remote add origin https://github.com/username/nama_repo.git
```
Push commit ke GitHub:

```
git push -u origin main
```
Jika diminta username dan password, masukkan username GitHub dan token GitHub (bukan password).

Sekarang repository Git sudah dibuat dan bisa digunakan di Termux!
