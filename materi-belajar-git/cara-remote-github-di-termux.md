# cara remote with ssh git di termux

Langkah 1: Install Git di Termux

1. Buka Termux di HP Anda.


2. Jalankan perintah untuk meng-update dan meng-install Git:

pkg update && pkg upgrade
pkg install git




---

Langkah 2: Konfigurasi Git

1. Set nama pengguna:

git config --global user.name "NamaPengguna"

Ganti NamaPengguna dengan nama Anda (sebaiknya sama dengan username GitHub Anda).


2. Set email:

git config --global user.email "EmailAnda"

Ganti EmailAnda dengan email yang Anda gunakan untuk GitHub.


3. Cek konfigurasi:

git config --list




---

Langkah 3: Buat Kunci SSH untuk Autentikasi

1. Buat kunci SSH:

ssh-keygen -t ed25519 -C "EmailAnda"

Saat diminta lokasi file, tekan Enter untuk menggunakan lokasi default.

Jika diminta passphrase, Anda bisa mengosongkannya (atau memasukkan password untuk keamanan tambahan).



2. Tampilkan kunci SSH publik:

cat ~/.ssh/id_ed25519.pub

Salin seluruh isi outputnya.


3. Tambahkan kunci SSH ke GitHub:

Buka GitHub > Settings > SSH and GPG keys > New SSH key.

Tempel kunci yang telah Anda salin ke kolom Key.

Beri nama di bagian Title, lalu klik Add SSH key.





---

Langkah 4: Clone Repository GitHub ke Termux

1. Uji koneksi SSH ke GitHub:

ssh -T git@github.com

Jika berhasil, Anda akan melihat pesan seperti:
Hi username! You've successfully authenticated.


2. Clone repository GitHub:

git clone git@github.com:username/repo.git

Ganti username dengan username GitHub Anda dan repo dengan nama repository.


3. Pindah ke folder repository:

cd repo


4. Anda sekarang bisa bekerja dengan repository tersebut, misalnya menambahkan file, commit, dan push perubahan.




---

Langkah 5: Workflow Git

Beberapa perintah Git yang sering digunakan:

Menambah file baru ke Git:

git add nama_file

Commit perubahan:

git commit -m "Pesan commit"

Push ke repository GitHub:

git push


Dengan langkah-langkah ini, Anda sudah bisa meremote GitHub ke Termux.

