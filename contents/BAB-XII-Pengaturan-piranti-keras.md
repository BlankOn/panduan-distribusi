<span id="anchor-196"></span> Pengaturan Perangkat Keras
========================================================

Pengaturan perangkat keras yang terpasang di komputer menggunakan
BlankOn sangat mudah sekali. Anda hampir tidak perlu melakukan
pemasangan driver perangkat keras, karena BlankOn sudah menyediakan
hampir semua driver perangkat keras esensial yang ada saat ini.
Sehingga, setelah pemasangan BlankOn, hampir semua perangkat keras
esensial seperti kartu video, kartu suara, dsb bisa berjalan dengan
baik.

Namun untuk memantapkan perangkat keras tersebut, Anda perlu mengetahui
bagaimana melakukan pengaturan perangkat keras yang ada. Semua hal
menyangkut perangkat keras dibahas dalam bab ini.

Walaupun hampir semua perangkat keras esensial mampu digunakan di
BlankOn dengan baik dan out-of-the-box (tanpa perlu pengaturan
mendetail), sampai saat ini masalah driver perangkat keras masih
merupakan masalah dominan dan mengganggu dunia Linux. Tidak semua
produsen perangkat keras merilis driver-nya untuk platform Linux.
Walaupun ada beberapa, itupun tidak Open Source dan masih dikembangkan
secara tertutup. Hampir semua driver yang saat ini ada di Linux
merupakan hasil jerih payah para komunitas tanpa bantuan dari produsen
perangkat keras. Namun, hal ini akan menjadi masalah waktu saja.
Beberapa produsen perangkat keras mulai maju untuk mengembangkan
driver-nya untuk Linux mengingat Linux semakin populer saat ini sebagai
sistem operasi untuk Desktop.

<span id="anchor-197"></span>Konfigurasi Monitor
------------------------------------------------

Konfigurasi monitor di BlankOn sudah diatur sedemikian rupa, sehingga
resolusi layar monitor sesuai dengan kemampuan monitor yang Anda miliki.
Namun jika Anda ingin mengatur resolusi monitor agar lebih optimal, atau
memanfaatkan beberapa monitor yang terpasang di komputer, Anda bisa
melakukannya dengan fitur pengaturan Monitor dengan langkah sebagai
berikut,

Klik **Menu Utama BlankOn =&gt; Preferensi =&gt; Perangkat Keras =&gt;
Tampilan**, jendela pengaturan yang tampil, klik gambar layar, maka
segera tampil jendela baru dengan beberapa menu, yaitu:

-   **Ukuran**: menunjukkan ukuran layar pada komputer/laptop yang
    sedang digunakan.
-   **Rasio Aspek**: menunjukkan perbadingan pajang dan lebar dari layar
    yang digunakan
-   **Resolusi**: menunjukkan resolusi pada layar yang sedang digunakan

### <span id="anchor-198"></span>Mengatur Resolusi

Untuk mengatur resolusi lakukan langkah berikut;

-   Klik tanda segitiga kecil pada kotak resolusi, pilih resolusi yang
    diinginkan, kemudian klik tombol **Terapkan**, maka segera muncul
    jendela konfirmasi untuk menerapkan perubahan, klik tombol **Keep
    This Configuration** untuk menerpakan perubahan resolusi pada layar.

##### Catatan:

-   Anda juga dapat menentukan ukuran **Refresh Rate** yang otomatis
    muncul di bawah menu Resolusi ketika mengubah ukuran resolusi
    menjadi paling kecil (misal: 800 x 600)

<span id="anchor-199"></span>Konfigurasi Mesin Pencetak
-------------------------------------------------------

Manajemen mesin pencetak atau printer yang ada di BlankOn diatur oleh
sebuah perangkat lunak server bernama CUPS (Common Unix Printing
System). CUPS bertanggung jawab untuk menerima permintaan pencetakan
baik dari lokal maupun dari jaringan, melakukan job pencetakan dan
mengirim informasi ke printer untuk melakukan pencetakan.

Secara default, driver mesin pencetak akan langsung terpasang di BlankOn
jika mesin pencetak tersebut sudah tersedia di sistem pada saat printer
pertama kalinya dipasang ke komputer. Anda akan melihat pesan notifikasi
bahwa printer baru telah ditambahkan. Namun, jika mesin pencetak Anda
tidak terdeteksi sama sekali atau printer terbagi di jaringan, Anda bisa
membuka alat konfigurasi mesin pencetak yang Anda bisa buka melalui
**menu utama BlankOn** =&gt; **Menu Utama BlankOn =&gt; Administrasi
=&gt; Print Setting**.

### <span id="anchor-200"></span>Menambahkan Pencetak

Berikut adalah langkah-langkah penambahan mesin pencetak melalui menu
pengaturan printer :

Klik tombol Add atau **tombol + (tambah)**, Maka segera tampil jendela
untuk menambahkan printer disertai dengan konfirmasi untuk memasukkan
**sandi**, ketik **sandi Administrator** komputer Anda, kemudian klik
tombol **Authenticate**.

Langkah selanjutnya adalah memilih jenis printer yang tersabung ke
komputer, apakah menggunakan **Port USB, LPT, nirkabel**, **atau melalui
Jaringan,** klik **Forward** untuk menambahkan printer sesungguhnya.

Sesaat setelah Anda menekan tombol Forward, maka muncul jendela
Deskripsi Pencetak yang akan Anda tambahkan disertai jendela konfirmasi
bahwa penggerak (driver) untuk pencetak yang akan Anda tambahkan sudah
sesuai, jika sudah sesuai klik tombol **Cance**l, namun jika belum
sesuai klik tombol **Find in Software** atau **OK** untuk mencari
penggerak secara langsung lewat Internet.

Klik tombol **Apply** pada jendela **Deskripsi Pencetak** untuk
melanjutkan ke proses berikutnya, ketika tampil jendela konfirmasi untuk
memasukkan sandi, ketik sandi Administrator Anda, kemudian tekan tombol
**Authenticate.**

Sekarang Pencetak sudah berhasil ditambahkan, jika muncul jendela
konfirmasi **Cetak halaman uji?**, Anda dapat langsung menguji pencetak
yang terhubung dengan komputer Anda degnan klik tombol **Cetak Halaman
Uji.**

##### Catatan:

-   Selain cara di atas Anda juga dapat menambahkan Pencentak dengan
    cara klik **Menu Utama BlankOn =&gt; Preferensi =&gt; Pengaturan
    =&gt; Perangkat Keras =&gt; Pencetak**

### <span id="anchor-201"></span>Pengaturan Mesin Cetak 

Untuk melakukan pengaturan mesin cetak agar hasilnya sesuai dengan
keinginan Anda, klik **Menu Utama BlankOn =&gt; Administrasi =&gt; Print
Setting**, klik kanan mesin cetak yang terpasang pilih **Propert**i,
maka akan segera muncul beberapa menu untuk melakukan pengaturan pada
mesin cetak yang terpasang.

Lakukan pengaturan sesuai keinginan Anda, sebagai contoh untuk melakukan
pengaturan kualitas warna klik** Opsi Pencetak =&gt; Print Quality**,
pilih sesuai hasil warna dan kualitas hasil pencetak yang di kehendaki,
setelah sesuai dengan keinginan, klik tombol **Terapkan (Apply) =&gt;
Oke**, baru lakukan pencetakan.

<span id="anchor-202"></span> Warna
-----------------------------------

Manjemen warna adalah suatu proses pengambilan warna menggunakan
perangkat input, kemudian ditampilkan pada layar yang terhubung dengan
mesin cetak (printer), tujuannya adalah mengelola warna agar hasilnya
ketika dicetak pada berbagai media akan tetap baik.

Di bawah ini adalah contoh penerapan manajemen warna dengan menggunakan
gambar burung pada hari yang dingin ketika musim salju.

Ketika gambar burung tersebut dibuka secara langsung dengan penampil
gambar pada komputer, maka tampilannya terlihat lebih biru dan sedikit
redup.

Dan ketika dicetak secara langsung tanpa manajemen warna hasilnya tidak
sesuai, coba perhatikan dengan teliti gambar di bawah ini, bagian warna
putih tidak bisa sempurna atau tidak benar-benar putih, selain itu warna
hitam pada mata terlihat coklat tua.

Printer standar kantoran **tidak mempunyai tinta warna putih**, sehingga
kualitas warna putih pada gambar hasil cetak kurang baik, atau dengan
kata lain warna putihnya sesuai **warna kertas**. Dengan Pengaturan
Warna kita dapat mengatur profil warna untuk layar dan pencetak sehingga
warna yang dihasilkan sesuai dengan yang direncanakan.

### <span id="anchor-203"></span>Mengatur Warna

Berikut ini adalah langkah-langkah untuk mengatur Warna;

Klik **menu utama BlankOn =&gt; Preferensi =&gt; Pengaturan**, atau bisa
juga dengan klik **menu utama BlankOn =&gt; Pengaturan**, pada jendela
yang tampil pilih kelompok Perangakt Keras, kemudian klik **Warna**
sehingga muncul panel **Pengaturan Warna**

Maka segera muncul jendela untuk mengatur warna, jendela tersebut berisi
beberapa keterangan perangkat keras yang sedang digunakan maupun mesin
pencentak (printer) yang terhubung dengan komputer/laptop, misalnya
Jenis Layar Laptop dan seri printer yang terhubung dengan Laptop.

##### Catatan

-   Kita dapat membaca keterangan lebih detail tentang pengaturan warna
    pada **Bantuan GNOME** yang dapat diakses dengan mengeklik tulisan
    **Pelajari lebih jauh**.

#### <span id="anchor-204"></span>Menambah Profil Warna

Profil warna adalah kumpulan data yang mencirikan suatu perangkat atau
ruang warna. Sebagian besar profil warna berupa berkas kecil dengan
ekstensi **.ICC** atau **.ICM**. Profil warna berfungsi untuk memastikan
bahwa pengguna melihat warna yang sama pada perangkat berbeda. Berikut
ini langkah-langkah menambah profil warna;

Pada panel Pengaturan Warna, pilih perangkat yang akan diatur (Layar
Laptop atau Pencetak)

Pada gambar di atas, terlihat Layar Laptop menggunakan profil warna
**Otomatis-Inspiron 1420** (bawaan laptop).

Untuk menambahkan profil warna, klik tombol **Add profile** di bagian
bawah-kanan panel, maka segera muncul jendela Tambah Profil. Pilih
profil warna (misalnya Best RGB) pada jendela **Tambah Profil**. Klik
tombol **Tambah,** jika ingin menggunakan berkas profil warna di luar
daftar yang tersedia, kita dapat mengeklik tombol **Import File...**

### <span id="anchor-205"></span>Ganti Profil Warna

1.  Pada jendela Pengaturan Warna, pilih perangkat yang akan diatur
    (Layar Laptop atau Pencetak) sehingga muncul daftar profil yang
    sudah ditambahkan.
2.  Pilih profi warna yang ingin dipakai, klik tombol **Enable** pada
    pojok kiri-bawah jendela

### <span id="anchor-206"></span>Hapus Profil Warna

1.  Pada jendela **Pengaturan Warna**, pilih perangkat yang akan diatur
    (Layar Laptop atau Pencetak) sehingga muncul daftar profil yang
    sudah ditambahkan.
2.  Pilih profi warna yang ingin dihapus, kemudian klik tombol **Remove
    Profile** pada pojok kanan-bawah jendela.

<span id="anchor-207"></span>Penganalisa Penggunaan Disk 
---------------------------------------------------------

Untuk menganalisa penggunaan disk dalam komputer, Anda bisa menggunakan
bantuan aplikasi Penganalisa Penggunaan Disk. Aplikasi ini berbasis
grafis untuk menganalisa penggunaan disk pada lingkungan GNOME, aplikasi
ini akan dengan mudah memindai semua struktur pohon filesistem, atau
direktori khusus sesuai dengan pilihan Anda. Aplikasi ini bisa diakses
melalui **Menu Utama BlankOn =&gt; Perkakas Sistem =&gt; Penganalisa
Penggunaan Disk. **

