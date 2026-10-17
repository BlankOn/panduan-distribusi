\newpage

# Manajemen Pengguna Dan Kelompok

Komputer yang memakai BlankOn biasanya dipakai oleh lebih dari satu
orang: Anda sendiri, anggota keluarga, rekan kerja, atau teman.
Agar setiap orang punya ruang kerja sendiri-sendiri yang tidak
saling mengganggu, BlankOn menyediakan fitur **pengguna** (*user*)
dan **kelompok** (*group*). Pada bab ini Anda akan mempelajari
pengertian pengguna dan kelompok, cara menambah, mengubah, dan
menghapus pengguna lewat Pengaturan GNOME maupun lewat terminal,
serta beberapa kebiasaan aman yang sebaiknya Anda terapkan.

## <span id="anchor-220"></span>Apa Itu Pengguna dan Kelompok

**Pengguna** adalah identitas setiap orang yang memakai komputer.
Setiap pengguna punya nama pengguna (*username*), kata sandi
(*password*), dan folder rumah (*home directory*) sendiri, misalnya
`/home/budi`. Berkas-berkas di folder rumah seorang pengguna tidak
bisa dibaca atau diubah oleh pengguna lain, kecuali pemiliknya
mengizinkan. Dengan begitu, dokumen Anda tetap rahasia dari pengguna
lain di komputer yang sama.

Ada dua jenis pengguna di BlankOn:

-   **Administrator**: pengguna yang boleh melakukan tugas-tugas
    administratif, seperti memasang aplikasi, mengubah pengaturan
    sistem, serta menambah atau menghapus pengguna lain. Di
    BlankOn, administrator melaksanakan tugas administratif dengan
    perintah `sudo`, yaitu menjalankan perintah biasa tetapi
    didahului kata `sudo` dan dimintai kata sandi miliknya sendiri.
-   **Standar**: pengguna biasa yang hanya boleh memakai komputer
    untuk bekerja sehari-hari (mengetik dokumen, menjelajah
    internet, memutar musik) tanpa bisa mengubah pengaturan sistem.

**Kelompok** adalah kumpulan pengguna. Kelompok dipakai untuk memberi
hak akses yang sama kepada beberapa pengguna sekaligus. Misalnya,
kelompok `sudo` berisi pengguna-pengguna yang boleh menjalankan
perintah administratif. Menjadikan seseorang administrator pada
dasarnya berarti memasukkannya ke dalam kelompok `sudo`.

Beberapa berkas penting menyimpan daftar pengguna dan kelompok di
sistem. Anda tidak perlu mengubahnya langsung, tetapi ada baiknya
tahu keberadaannya:

-   `/etc/passwd`: daftar seluruh pengguna beserta informasi
    dasarnya, seperti nama pengguna, nomor identitas (UID), folder
    rumah, dan program yang dijalankan saat login.
-   `/etc/group`: daftar seluruh kelompok beserta anggotanya.
-   `/etc/shadow`: menyimpan kata sandi yang sudah diacak
    (*terenkripsi*), hanya bisa dibaca oleh sistem.

Anda bisa mengintip isi dua berkas pertama dengan perintah
`cat /etc/passwd` dan `cat /etc/group` di terminal. Jangan mengubah
isinya secara manual; gunakan perintah-perintah khusus yang dibahas
di bawah.

##### CATATAN:

-   Pengguna pertama yang dibuat saat pemasangan BlankOn otomatis
    menjadi administrator (masuk kelompok `sudo`).
-   Pastikan selalu ada minimal satu pengguna administrator di
    komputer. Tanpa administrator, Anda tidak bisa memasang
    aplikasi atau mengubah pengaturan sistem.

## <span id="anchor-221"></span>Mengelola Pengguna Lewat Pengaturan

Cara termudah mengelola pengguna adalah lewat aplikasi
**Pengaturan** (*Settings*) di desktop Praya/BlankOn.

### <span id="anchor-222"></span>Membuka Panel Pengguna

1.  Buka **Pengaturan** dari menu aplikasi atau dengan mengeklik
    ikon roda gigi di sudut kanan atas layar, lalu pilih
    **Pengaturan**.
2.  Pada panel kiri, gulir ke bawah lalu klik **Pengguna**
    (*Users*). Akan tampil daftar pengguna yang ada di komputer
    beserta foto dan tipe akunnya.

![](Gambar/BAB-14-panel-pengguna.png)

### <span id="anchor-223"></span>Membuka Kunci Pengaturan

Pengaturan pengguna dilindungi agar tidak diubah sembarangan.
Sebelum menambah atau menghapus pengguna, Anda harus membuka
kuncinya terlebih dahulu:

1.  Klik tombol **Buka Kunci** (*Unlock*) di sudut kanan atas
    panel Pengguna.
2.  Ketik kata sandi administrator Anda, lalu klik
    **Otentikasi** (*Authenticate*).

![](Gambar/BAB-14-buka-kunci-pengaturan.png)

Setelah terbuka, tombol-tombol **Tambah Pengguna**, **Hapus**,
dan pengaturan tipe akun menjadi aktif.

### <span id="anchor-224"></span>Menambah Pengguna Baru

1.  Klik tombol **Tambah Pengguna...** (*Add User...*).
2.  Pilih **Tipe Akun**: **Standar** untuk pengguna biasa, atau
    **Administrator** jika pengguna tersebut boleh mengelola
    sistem.
3.  Isi **Nama Lengkap** (misalnya *Siti Rahma*) dan **Nama
    Pengguna** (misalnya *siti*). Nama pengguna sebaiknya huruf
    kecil tanpa spasi.
4.  Tentukan cara login: biarkan pengguna mengatur kata sandinya
    sendiri saat pertama login, atau langsung tetapkan kata sandi
    sekarang.
5.  Klik **Tambah**. Pengguna baru langsung muncul di daftar dan
    bisa dipakai untuk login.

![](Gambar/BAB-14-tambah-pengguna.png)

##### PERHATIAN:

-   Hanya beri tipe **Administrator** kepada orang yang benar-benar
    Anda percaya dan paham mengelola komputer. Administrator bisa
    menghapus berkas siapa pun dan mengubah seluruh sistem.

### <span id="anchor-225"></span>Mengubah Tipe Akun dan Kata Sandi

-   **Mengubah tipe akun**: klik nama pengguna di daftar, lalu
    ubah pilihan **Tipe Akun** antara **Standar** dan
    **Administrator**. Perubahan langsung berlaku.
-   **Mengganti kata sandi sendiri**: klik nama Anda di daftar
    pengguna, klik kolom **Kata Sandi**, masukkan kata sandi lama
    lalu kata sandi baru dua kali, dan klik **Ubah**.
-   **Mereset kata sandi pengguna lain** (khusus administrator):
    buka kunci panel, klik nama pengguna yang bersangkutan, klik
    kolom **Kata Sandi**, lalu tetapkan kata sandi baru.

### <span id="anchor-226"></span>Menghapus Pengguna

1.  Buka kunci panel Pengguna seperti dijelaskan di atas.
2.  Klik nama pengguna yang akan dihapus.
3.  Klik tombol **Hapus Pengguna...** (*Remove User...*).
4.  Akan muncul pilihan: **Simpan Berkas** (*Keep Files*) untuk
    menyimpan folder rumah pengguna tersebut, atau **Hapus
    Berkas** (*Delete Files*) untuk menghapus seluruh datanya.
    Pilih sesuai kebutuhan, lalu konfirmasi.

![](Gambar/BAB-14-hapus-pengguna.png)

##### Peringatan:

-   Menghapus pengguna dengan pilihan **Hapus Berkas** akan
    menghilangkan seluruh dokumen, gambar, dan pengaturan milik
    pengguna tersebut secara permanen. Pastikan sudah ada
    cadangannya (*backup*) bila datanya penting.

## <span id="anchor-227"></span>Mengelola Pengguna Lewat Terminal

Selain lewat Pengaturan, pengguna dan kelompok juga bisa dikelola
lewat terminal. Cara ini berguna bila Anda mengelola komputer dari
jarak jauh atau ingin mengotomatisasi pekerjaan. Semua perintah di
bawah dijalankan dengan `sudo` karena bersifat administratif.

### <span id="anchor-228"></span>Menambah Pengguna Baru (adduser)

Perintah `adduser` di BlankOn (berbasis Debian) bersifat
interaktif dan mudah dipakai:

    sudo adduser siti

Sistem akan menanyakan kata sandi untuk pengguna baru, lalu
informasi tambahan seperti nama lengkap (boleh dikosongkan dengan
menekan Enter). Folder rumah `/home/siti` dibuat otomatis.

### <span id="anchor-229"></span>Mengubah Pengguna (usermod)

Perintah `usermod` dipakai untuk mengubah sifat pengguna, misalnya
menjadikannya administrator dengan memasukkannya ke kelompok
`sudo`:

    sudo usermod -aG sudo siti

Opsi `-aG` artinya *tambahkan* (`-a`, *append*) pengguna ke
kelompok (`-G`) yang disebutkan, dalam hal ini `sudo`.
Pengguna harus keluar (*logout*) lalu masuk kembali agar
perubahan kelompok berlaku.

Untuk memeriksa kelompok apa saja yang diikuti seorang pengguna,
gunakan perintah:

    groups siti

atau `id siti` untuk melihat UID, GID, dan daftar kelompoknya
sekaligus.

### <span id="anchor-230"></span>Menghapus Pengguna (userdel)

Untuk menghapus pengguna:

    sudo userdel siti

Perintah di atas menghapus pengguna tetapi **membiarkan folder
rumahnya**. Untuk menghapus sekaligus seluruh berkas miliknya,
tambahkan opsi `-r`:

    sudo userdel -r siti

##### Peringatan:

-   Opsi `-r` menghapus permanen seluruh isi `/home/siti`. Gunakan
    hanya bila Anda yakin datanya sudah tidak diperlukan.

### <span id="anchor-231"></span>Mengatur Kata Sandi (passwd)

Untuk mengganti kata sandi pengguna lain (khusus administrator):

    sudo passwd siti

Untuk mengganti kata sandi **Anda sendiri**, cukup ketik tanpa
`sudo` dan tanpa nama pengguna:

    passwd

Sistem akan meminta kata sandi lama, lalu kata sandi baru dua
kali. Ketikan kata sandi tidak ditampilkan di layar; itu normal.

### <span id="anchor-232"></span>Mengelola Kelompok (groupadd)

Membuat kelompok baru:

    sudo groupadd keluarga

Memasukkan pengguna ke kelompok tersebut:

    sudo usermod -aG keluarga siti

Menghapus kelompok (kelompok harus sudah kosong dari anggota
atau anggotanya akan kehilangan kelompok tersebut):

    sudo groupdel keluarga

## <span id="anchor-233"></span>Pengguna vs Administrator Sehari-hari

Bekerja sehari-hari sebaiknya memakai akun **Standar** atau akun
administrator biasa, bukan masuk sebagai `root`. Di BlankOn,
akun `root` memang ada tetapi tidak diberi kata sandi untuk login
langsung; tugas administratif dilakukan lewat `sudo`.

Saat Anda menjalankan perintah administratif, misalnya memasang
aplikasi:

    sudo apt install nama-aplikasi

sistem meminta **kata sandi milik Anda sendiri**, bukan kata sandi
khusus. Ini sengaja dirancang sebagai jeda berpikir: setiap kali
kata sandi diminta, tanyakan pada diri sendiri apakah Anda yakin
dengan perintah yang akan dijalankan.

Beberapa kebiasaan aman yang disarankan:

-   **Gunakan kata sandi yang kuat**: gabungan huruf besar, huruf
    kecil, angka, dan simbol, minimal 12 karakter. Jangan memakai
    tanggal lahir atau nama anggota keluarga.
-   **Satu orang, satu akun**: jangan berbagi satu nama pengguna
    untuk beberapa orang. Akun terpisah membuat tanggung jawab
    jelas dan data tidak tercampur.
-   **Kunci layar saat pergi**: tekan **Super+L** (tombol Windows+L)
    atau pilih **Kunci** dari menu sudut kanan atas sebelum
    meninggalkan komputer, walau hanya sebentar.
-   **Hati-hati dengan login otomatis**: fitur masuk otomatis
    tanpa kata sandi memang praktis, tetapi siapa pun yang
    menyalakan komputer bisa langsung memakai akun Anda.
    Pertimbangkan mematikannya di panel Pengguna bila komputer
    dipakai bersama.
-   **Perbarui sistem secara rutin**: pembaruan keamanan menutup
    celah yang bisa disalahgunakan. Jalankan pembaruan lewat
    Pengaturan atau perintah `sudo apt update && sudo apt upgrade`.
-   **Jangan menjalankan perintah dari internet tanpa
    memahami isinya**: perintah `sudo` yang disalin dari situs
    asing bisa merusak sistem atau mencuri data. Pahami dulu,
    jalankan kemudian.

Dengan memahami pengguna dan kelompok, Anda sudah menguasai salah
satu fondasi keamanan Linux: setiap orang hanya bisa menyentuh
miliknya sendiri, dan perubahan pada sistem hanya bisa dilakukan
oleh mereka yang diberi wewenang. Pada bab berikutnya, buku ini
ditutup dengan rangkuman dan ajakan untuk ikut mengembangkan
BlankOn bersama komunitas.
