# tugas-SO-nabil
: membuat folder untuk 3 departemen/ marekting, enginering,HR

1. https://drive.google.com/file/d/1s7iQadP-RLDqXu5mYjUG4hlFMowbj5XQ/view?usp=drivesdk

mkdir project_file_manajement_server

Membuat direktori baru bernama project_file_manajement_server di direktori saat ini.
cd project_file_manajement_server

Berpindah ke direktori project_file_manajement_server yang baru dibuat.
```
mkdir -p marketing/document marketing/archiveS
```

Membuat direktori dan subdirektori secara berjenjang:
marketing/document
marketing/archives
Opsi -p membuat direktori induk jika belum ada (dalam kasus ini, marketing).
```
mkdir -p enginering/document enginering/archives
```

Membuat direktori dan subdirektori secara berjenjang:
enginering/document
enginering/archives
Opsi -p juga memastikan direktori induk enginering dibuat jika belum ada.
```
mkdir -p HR/document HR/archives
```
Membuat direktori dan subdirektori secara berjenjang:
HR/document
HR/archives
Opsi -p membuat direktori induk HR jika belum ada.

2. https://drive.google.com/file/d/1MBO0Uy1Plen3UGi1XA-4shjHUNEG5rmW/view?usp=drivesdk

```
: mv /home/nabilbouato/project_file_manajement/documenttxt \
   /home/nabilbouato/project_file_manajement_server/marketing/document/
```
 Apa itu perintah mv?
mv adalah perintah Linux untuk memindahkan atau mengganti nama file/direktori.

 Penjelasan bagian-bagiannya:
mv
Perintah untuk memindahkan (move).

/home/nabilbouato/project_file_manajement/document/txt
➜ Ini adalah sumber (source).
Bisa berupa file bernama txt atau folder bernama txt.

/home/nabilbouato/project_file_manajement_server/marketing/document/
➜ Ini adalah tujuan (destination), yaitu folder tempat file/direktori akan dipindahkan.

3. https://drive.google.com/file/d/16OTL5-zHQVaj9TUTNb9a1hZ2tmrwxuIz/view?usp=drivesdk

```
cp -r /home/nabilbouato/project_file_manajement_server/marketing/document/ \
      /home/nabilbouato/project_file_manajement_server/marketing/archives/
```
cp
Perintah copy di Linux untuk menyalin file atau folder.
 -r
Singkatan dari recursive.
Berarti: menyalin folder beserta seluruh isinya, termasuk sub-folder dan file di dalamnya.
Tanpa -r, kamu tidak bisa menyalin direktori.

4. https://drive.google.com/file/d/1MJeFg5pgmahZ6_Ge2CZbarLrK3sV4VCh/view?usp=drivesdk
```
   sudo adduser adminmarketing
```
Membuat user baru bernama adminmarketing.
Proses yang terjadi:
Sistem membuat UID/GID untuk user.
Sistem membuat group baru bernama adminmarketing.
Sistem membuat direktori home:
/home/adminmarketing
Sistem meminta kamu memasukkan password.
Sistem meminta informasi tambahan seperti:
Full Name
Room Number
Work Phone
Home Phone
(kamu bisa tekan ENTER untuk melewati semuanya)
Setelah selesai, user adminmarketing berhasil dibuat. 2. Perintah:
sudo chown -R adminmarketing /home/nabilbouato/project_file_manajement_server/marketing/
Fungsinya:
Mengubah kepemilikan folder:
/home/nabilbouato/project_file_manajement_server/marketing/
➡ menjadi milik user adminmarketing
Penjelasan parameter:
sudo → menjalankan perintah dengan hak administrator
chown → change owner (mengubah pemilik file/folder)
-R → recursive (mengubah kepemilikan seluruh isi folder, termasuk subfolder dan file)
Artinya:
User adminmarketing menjadi pemilik resmi folder marketing dan semua file di dalamnya.
 3. Perintah:
chmod -R 700 /home/nabilbouato/project_file_manajement_server/marketing/
 Fungsinya:

Mengatur permission (izin akses) folder marketing.
Arti angka 700:
7 = full access untuk owner
→ read (4) + write (2) + execute (1) = 7
0 = no access untuk group
0 = no access untuk others
Jadi hasilnya:
Hanya pemilik folder (yaitu adminmarketing, dari perintah sebelumnya) yang bisa:
membaca
menulis
menjalankan (akses folder)
Sedangkan pengguna lain tidak bisa:
melihat isi folder
mengakses file
membuka folder
Ini membuat folder tersebut sangat aman / privat.

\
5. https://drive.google.com/file/d/1oEChKFREOm7O6zK3ANEdi-03KwsJxFqJ/view?usp=drivesdk

```
sudo adduser adminengineering
```
Fungsinya:
Membuat user baru bernama adminengineering.
Proses yang terjadi:
Sistem membuat akun user baru
Sistem membuat group dengan nama yang sama (adminengineering)
Sistem membuat home dirctory:
/home/adminengineering


Sistem meminta password user

Sistem meminta informasi tambahan (Full Name, Room Number, dll)

Setelah dikonfirmasi, user berhasil dibuat

Catatan:

Pesan “BAD PASSWORD: The password is shorter than 8 characters” berarti password terlalu pendek, tapi masih diterima setelah diulang.

 2. Perintah:
sudo chown -R adminengineering /home/nabilbouato/project_file_manajement_server/engineering/

 Fungsinya:

Mengubah kepemilikan (ownership) folder engineering menjadi milik user adminengineering.

Penjelasan:

sudo → hak admin

chown → mengubah pemilik file/folder

-R → recursive, artinya:
semua file
semua subfolder
di dalam folder engineering/ ikut berubah pemiliknya
Mulai sekarang, user adminengineering menjadi pemilik folder engineering
 3. Perintah:
sudo chmod -R 700 /home/nabilbouato/project_file_manajement_server/engineering/
Fungsinya:
Mengatur izin akses (permission) folder engineering.
Arti permission 700:
7 → pemilik (owner): punya full access
read
write
execute
0 → group: tidak punya akses apa pun
0 → others: tidak punya akses apa pun
Dengan kata lain:
 Hanya user adminengineering yang dapat mengakses folder engineering.
Semua user lain:  tidak bisa membaca, membuka, atau mengedit


6.https://drive.google.com/file/d/1eHpw2USRgMj1tm8Ie3SP54af2aL0rBQP/view?usp=drivesdk
```
sudo adduser adminhr
```
Tujuan: Membuat pengguna baru bernama adminhr.

sudo: Digunakan untuk menjalankan perintah dengan hak akses super-user (administrator), yang diperlukan untuk tugas administrasi sistem seperti membuat pengguna.

adduser: Perintah untuk menambahkan pengguna ke sistem.

Apa yang terjadi (output Info:):

Sistem memilih ID pengguna (UID) dan ID grup (GID) yang tersedia (misalnya, 1004).

Membuat grup baru bernama adminhr.

Membuat home directory untuk pengguna baru di /home/adminhr.

Menyalin file konfigurasi awal dari /etc/skel ke home directory baru.

Tindakan Lanjutan: Perintah ini kemudian meminta Anda untuk memasukkan kata sandi (New Password, Retype new password) dan informasi pengguna tambahan (Full Name, Room Number, dll.).

2. Konfigurasi Kata Sandi dan Info Pengguna
Setelah pengguna dibuat, sistem meminta Anda untuk:

Membuat Kata Sandi: Anda memasukkan kata sandi, tetapi sistem menunjukkan peringatan BAD PASSWORD: The password is shorter than 8 characters. Meskipun ada peringatan, kata sandi tetap diperbarui (passwd: password updated successfully).

Memasukkan Informasi Detail: Anda mengisi (atau mengosongkan) detail seperti nama lengkap, nomor ruangan, dsb., lalu mengkonfirmasi informasi tersebut dengan y (Is the information correct? [Y/n] y).

3. Penambahan Grup
Info: Adding new user 'adminhr' to supplemental / extra groups 'users' ...: Setelah informasi dikonfirmasi, sistem secara otomatis menambahkan pengguna adminhr ke grup tambahan (users).

4. Perintah chown (Mengubah Kepemilikan)
Perintah yang Gagal:
sudo chown -R adminhr /home/nabilbouato/project_file_management_server/hr

Tujuan: Mencoba mengubah pemilik dan grup dari direktori/file secara rekursif (-R) menjadi pengguna adminhr.

chown: Perintah untuk mengubah pemilik file atau direktori.

-R (Recursive): Menerapkan perubahan pada direktori yang ditentukan dan semua isi di dalamnya.

/home/nabilbouato/project_file_management_server/hr: Jalur (path) direktori target.

Output Kegagalan: chown: cannot access '/home/nabilbouato/project_file_management_server/hr': No such file or directory

Penjelasan: Perintah ini gagal karena direktori atau file dengan jalur tersebut tidak ditemukan di sistem.

Perintah yang Dicoba Lagi (Asumsi Perbaikan Pengetikan):
sudo chown -R adminhr /home/adminhr/project_file_management_server/HR

Tujuan: Mencoba mengubah pemilik dan grup dari direktori/file secara rekursif (-R) menjadi pengguna adminhr.

Catatan: Jalur direktori di sini berubah dari yang sebelumnya gagal, yaitu dari /home/nabilbouato/.../hr menjadi /home/adminhr/.../HR.

Apa yang terjadi: Perintah ini tampaknya berhasil (tidak ada pesan kesalahan seperti sebelumnya). Ini berarti direktori /home/adminhr/project_file_management_server/HR sekarang dimiliki oleh pengguna adminhr.

5. Perintah chmod (Mengubah Izin Akses)
sudo chmod -R 700 /home/adminhr/project_file_management_server/HR

Tujuan: Mengubah izin akses direktori/file secara rekursif (-R) menjadi 700.

chmod: Perintah untuk mengubah izin akses.

700: Ini adalah notasi numerik untuk izin akses.

Angka 7 (Pemilik/User): Memberikan izin Baca (4) + Tulis (2) + Eksekusi (1).

Angka 0 (Grup): Tidak memberikan izin apa pun.

Angka 0 (Lain-lain/Others): Tidak memberikan izin apa pun.

Efek: Setelah perintah ini, hanya pengguna adminhr yang dapat membaca, menulis, dan masuk ke direktori /home/adminhr/project_file_management_server/HR, sementara anggota grup lain dan pengguna lain tidak memiliki akses sama sekali.


7.https://drive.google.com/file/d/1x9Pv-Efe8KxeIJYyO4Z_fNN2e797RT0k/view?usp=drivesdk
```
Perintah: cd marketing/
```
cd: Singkatan dari Change Directory. Perintah ini digunakan untuk berpindah dari direktori tempat Anda berada saat ini ke direktori lain.

marketing/: Ini adalah nama direktori tujuan yang ingin dimasuki oleh pengguna.

Kesalahan yang Muncul: bash: cd: marketing/: Permission denied
Penyebab: Kesalahan Permission denied (Izin ditolak) muncul karena pengguna yang sedang aktif, nabilbouato, tidak memiliki izin eksekusi (x) untuk direktori marketing/.

Izin Eksekusi (x) pada Direktori: Pada Linux, izin eksekusi pada sebuah direktori diperlukan untuk dapat masuk (traverse) ke dalam direktori tersebut dan melihat isinya.

Jika Anda memiliki izin baca (r) tetapi tidak memiliki izin eksekusi (x), Anda dapat melihat nama file di dalamnya, tetapi Anda tidak bisa masuk dengan perintah cd.

Jika Anda tidak memiliki izin eksekusi (x), sistem akan menolak perintah cd. * Konteks: Kemungkinan besar, direktori marketing/ diatur sedemikian rupa (misalnya, izinnya 644 atau 744, tetapi pengguna nabilbouato bukan pemilik atau anggota grup yang diizinkan) sehingga hanya pengguna tertentu (mungkin root atau pengguna lain) yang boleh masuk ke dalamnya.

 Solusi (Asumsi)
Untuk memperbaiki kesalahan ini, pengguna yang memiliki hak akses (biasanya pemilik direktori atau administrator dengan sudo) perlu menggunakan perintah chmod untuk memberikan izin eksekusi (x) kepada pengguna nabilbouato atau kelompok yang dimiliki nabilbouato.


8.https://drive.google.com/file/d/18yHaeiERSCnedXsoYFHUqF5vVDmci1_0/view?usp=drivesdk
cd engineering/
cd: Singkatan dari Change Directory. Perintah ini digunakan untuk berpindah dari direktori kerja saat ini (/home/nabilbouato/project_file_management_server) ke direktori tujuan.

engineering/: Ini adalah nama direktori yang ingin dimasuki.

Kesalahan yang Muncul: bash: cd: engineering/: Permission denied
Penyebab: Pesan kesalahan Permission denied (Izin ditolak) muncul karena pengguna yang sedang menjalankan perintah (adminmarketing@nabilbouato atau pengguna yang sedang aktif) tidak memiliki izin yang diperlukan untuk masuk ke dalam direktori bernama engineering/.

Izin yang Diperlukan: Untuk dapat masuk ke (menjelajahi) sebuah direktori menggunakan cd, pengguna harus memiliki izin eksekusi (x) untuk direktori tersebut.

Implikasi: Izin akses direktori engineering/ diatur sehingga menolak akses masuk bagi pengguna aktif, meskipun pengguna mungkin memiliki izin untuk membaca nama file di dalamnya (izin baca, r).

 Solusi Singkat
Untuk mengatasi masalah ini, pengguna dengan hak administratif (pemilik direktori atau root melalui sudo) harus menggunakan perintah chmod untuk memberikan izin eksekusi (x) pada direktori engineering/ untuk pengguna yang sedang aktif atau untuk grup di mana pengguna aktif menjadi anggotanya.

9.https://drive.google.com/file/d/1WObkot5aItJOHTV9vi4N2nRTy2z1f9Sc/view?usp=drivesdk
```
erintah: cd HR
```
cd: Singkatan dari Change Directory. Fungsinya adalah untuk mengubah direktori kerja saat ini ke direktori tujuan.

HR: Ini adalah nama direktori tujuan yang ingin dimasuki oleh pengguna. Perintah ini dieksekusi dari direktori /home/nabilbouato/project_file_management_server.

Kesalahan yang Muncul: bash: cd: HR: Permission denied
Penyebab: Kesalahan Permission denied (Izin ditolak) muncul karena pengguna yang sedang aktif (yaitu, adminengineer@nabilbouato) tidak memiliki izin eksekusi (x) untuk direktori bernama HR.

Izin Eksekusi pada Direktori: Pada Linux, untuk dapat masuk ke dalam direktori menggunakan perintah cd, pengguna harus memiliki izin eksekusi (x). Tanpa izin ini, sistem akan menolak akses masuk, meskipun pengguna mungkin memiliki izin baca (r).

Konteks Tambahan: Ini adalah pola kesalahan yang sama dengan perintah sebelumnya (cd marketing/ dan cd engineering/), menunjukkan bahwa struktur izin (permissions) pada direktori HR dan direktori lainnya di dalam project_file_management_server diatur untuk membatasi akses masuk bagi pengguna aktif tersebut.

 Solusi
Untuk mengatasi masalah ini, pengguna harus memastikan bahwa pengguna adminengineer atau grup di mana pengguna tersebut menjadi anggotanya memiliki izin eksekusi (x) pada direktori HR. Hal ini biasanya dilakukan oleh pemilik direktori atau administrator (root) menggunakan perintah chmod.


10. https://drive.google.com/file/d/174F4Q8_fDMNBmUrcgbkulFchzSQwWInT/view?usp=drivesdk
    
```
.Perintah find
find /home/nabilbouato/project_file_management/ -type f -name "*.pdf" -exec sh -c 'echo {} >> daftar_pdf.txt' \;
```
Catatan: Dalam screenshot, perintah ini terlihat disingkat: find /home/nabilbouato/project_file_management/ -type f -name "*.pdf" > daftar_pdf.txt Namun, secara fungsional, tujuannya adalah mencari dan mencatat file PDF. Saya akan menjelaskan sintaks yang umum dan yang terlihat.

find: Perintah ini digunakan untuk mencari file dan direktori dalam hierarki direktori.

/home/nabilbouato/project_file_management/: Ini adalah lokasi awal pencarian.

-type f: Membatasi hasil pencarian hanya pada file biasa (bukan direktori atau link).

-name "*.pdf": Kriteria pencarian; mencari file yang namanya berakhiran dengan ekstensi .pdf.

> daftar_pdf.txt (Dugaan Berdasarkan Hasil): Ini adalah operator pengalihan (redirection). Output dari perintah find (yaitu, daftar lengkap jalur file PDF yang ditemukan) dialihkan dan disimpan ke dalam file baru bernama daftar_pdf.txt di direktori kerja saat ini.

Tujuan: Mencari semua file PDF yang ada di dalam direktori /home/nabilbouato/project_file_management/ (dan subdirektori di dalamnya) dan mencatat daftar jalurnya ke dalam file daftar_pdf.txt.

2. Perintah ls
ls

ls: Singkatan dari List. Perintah ini digunakan untuk menampilkan daftar isi (konten) dari direktori kerja saat ini.

Output:

daftar_pdf.txt engineering HR marketing
Penjelasan: Output ini menunjukkan bahwa di direktori kerja saat ini terdapat empat item: file daftar_pdf.txt yang baru dibuat, dan tiga direktori (engineering, HR, dan marketing).

3. Perintah cat
cat daftar_pdf.txt

cat: Singkatan dari Concatenate. Ketika digunakan dengan satu file, perintah ini berfungsi untuk menampilkan seluruh isi file tersebut di terminal.

Output (Contoh Tiga Baris Terakhir):

/home/nabilbouato/project_file_management/archives/file18.pdf
/home/nabilbouato/project_file_management/archives/file17.pdf
/home/nabilbouato/project_file_management/archives/file16.pdf
Penjelasan: Ini adalah isi dari file daftar_pdf.txt, yang memuat jalur lengkap dari file-file PDF yang ditemukan oleh perintah find sebelumnya.

11. https://drive.google.com/file/d/1dfb-8ojpppJWp0DNPMQxu8MCveSAHmJ5/view?usp=drivesdk
```
 Perintah: du -sh
```
du: Singkatan dari Disk Usage. Perintah ini digunakan untuk memperkirakan penggunaan ruang disk oleh file atau direktori yang diberikan. Jika tidak ada direktori yang ditentukan, ia akan memeriksa direktori kerja saat ini (dalam hal ini, /projek_sistem_operasi_A/projek_based_learning).

-s (Summarize): Opsi ini memastikan bahwa du hanya menampilkan total keseluruhan untuk argumen yang diberikan, bukan menampilkan ukuran untuk setiap subdirektori di dalamnya.

-h (Human-readable): Opsi ini membuat hasil keluaran menjadi lebih mudah dibaca oleh manusia. Misalnya, daripada menampilkan ukuran dalam byte atau kilobyte, ia akan menggunakan unit seperti KB, MB, atau GB.

12.https://drive.google.com/file/d/1sKcuNQtC5bIxFvA51pdfb_yJrfeWheRN/view?usp=drivesdk
```
nano
```
nano: Ini adalah perintah untuk menjalankan editor teks berbasis terminal bernama GNU nano.

Tanpa Argumen: Ketika perintah nano dijalankan tanpa menentukan nama file setelahnya, nano akan terbuka dengan buffer kosong, siap untuk membuat file baru. Anda kemudian dapat menulis, menyimpan file tersebut, atau keluar dari editor.

Konteks:

Perintah nano di baris pertama dijalankan, kemudian pengguna mungkin keluar (menggunakan Ctrl+X) untuk kembali ke terminal sebelum menjalankan perintah berikutnya (ls).

Perintah nano di baris terakhir menunjukkan pengguna berencana untuk membuka atau mengedit file lagi.

2. Perintah ls (Baris 2)
ls

ls: Singkatan dari List. Perintah ini digunakan untuk mencantumkan atau menampilkan konten (direktori dan file) dari direktori kerja saat ini.

 Output: Daftar Isi Direktori
Output dari perintah ls adalah daftar yang panjang, yang menunjukkan banyak file dan direktori dalam direktori kerja saat ini:

Direktori (biasanya berwarna biru/biru muda di terminal):

archives, Downloads, logs, Desktop, Documents, DOKUMEN, images, latihan1, Music, Pictures, Public, snap, Templates, Videos.

File (berwarna lainnya, tergantung tipe file):

File Gambar (.jpg): file10.jpg, file11.jpg, file12.jpg, file13.jpg, file14.jpg, file15.jpg, file16.jpg.

File Teks/Konfigurasi/Skrip (.tx, .pdf, .sh): file1.tx hingga file9.tx, file16.pdf20, file17.pdf19, file17.pdf20, file18.pdf20, file18.pdf19, repor.sh, dan lainnya.

Tujuan: Tujuan dari perintah ls adalah untuk memeriksa file dan subdirektori apa saja yang ada sebelum pengguna memutuskan tindakan selanjutnya (misalnya, mengedit file dengan nano, menghapus, atau masuk ke direktori lain).
