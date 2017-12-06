<span id="anchor-178"></span> Pengenalan Antar Muka Teks
========================================================

Antarmuka dasar untuk pengoperasian sistem operasi Linux sebenarnya
adalah antarmuka berbasis teks, atau sering disebut Command Line.
Antarmuka grafis atau desktop yang ada di dalam Linux sebenarnya
hanyalah alat bantu untuk pengoperasian bagi mereka yang sudah biasa
bekerja dengan Graphical User Interface (GUI) yang terdapat di beberapa
sistem operasi modern. Ini mirip dengan piranti lunak Microsoft Windows
sebelum versi 95 yang hanya merupakan alat bantu pengoprasian berbasis
grafis untuk DOS.

Untuk memberikan suatu perintah pada antarmuka teks, pengguna harus
mengetik nama perintah yang akan dijalankan beserta opsi-opsi atau
parameter yang diperlukan, kemudian menekan tombol Enter untuk
mengeksekusi perintah tersebut. Berbeda dengan antarmuka grafis,
penggunaan mouse secara umum tidak diperlukan karena semua kontrol hanya
dilakukan melalui papan ketik.

Tidak benar jika penggunaan antarmuka teks tidak bisa melakukan
produktivitas. Anda masih bisa berproduktivitas dengan berbagai aplikasi
berbasis teks yang tersedia dan siap Anda gunakan. Bahkan untuk para
administrator, penggunaan antarmuka teks sangat disarankan ketimbang
antarmuka grafis karena memakan sumberdaya CPU dan RAM yang lebih kecil,
sehingga tidak menganggu kinerja komputer pada saat melakukan suatu
tugas administrasi.

Pada bab ini, dijelaskan mengenai dasar pengoperasian antarmuka teks
yang ada pada BlankOn Linux. Sasaran pembaca tidak hanya bagi Anda yang
pengguna lanjut, melainkan juga para pemula/newbie yang ingin
mempelajari Linux lebih lanjut.

<span id="anchor-179"></span>Membuka Antarmuka Teks 
----------------------------------------------------

Ada dua jenis antarmuka teks yang bisa Anda buka, yaitu **Terminal** dan
**Virtual Console**. **Terminal** merupakan antarmuka teks yang berjalan
di dalam desktop dan berupa jendela aplikasi, sedangkan **Virtual
Console** merupakan antarmuka teks yang berjalan secara mandiri di luar
desktop.

### <span id="anchor-180"></span>Membuka Terminal Console 

Untuk membuka terminal, terdapat icon di bagian bawah dari desktop, atau
anda dapat melakukannya dari menu *Aplikasi =*&gt; *Aksesoris =*&gt;
*Root Terminal *pada BlankOn, kemudian isikan katakunci yang anda
miliki.

Jendela terminal akan muncul di dalam desktop.

### <span id="anchor-181"></span>Terminal 

Jika Anda ingin membuka sesi kerja yang baru, Anda bisa membuat tab baru
seperti layaknya fitur tabbed browsing pada peramban web dengan mengklik
menu ***File =&gt; Buka Tab***, atau Anda bisa tekan tombol
**Ctrl+Shift+T** pada keyboard.

Anda bisa mengkostumisasi penampilan terminal sesuai dengan keinginan
Anda melalui jendela pengaturan yang bisa Anda buka melalui menu Edit
&gt; Preferensi. Jika ingin membuat terminal dalam mode layar penuh,
Anda bisa klik menu Lihat &gt; Layar Penuh atau Anda bisa tekan tombol
F11 pada keyboard.

#### **Membuka Virtual Console** 

Linux telah menyediakan enam sesi antarmuka teks yang bisa Anda buka
dengan cara menekan tombol Ctrl+Alt+F1, Ctrl+Alt+F2 sampai Ctrl+Alt+F6.
Berbeda dengan menggunakan terminal, Anda harus melakukan login terlebih
dahulu sebelum bekerja dengan antarmuka teks. Ketik id pengguna kemudian
tekan enter lalu masukkan sandi (password tidak akan ditampilkan pada
layar) Anda dan tekan enter sekali lagi. Berbeda dengan terminal, Anda
tidak bisa melakukan kustomisasi penampilan agar lebih menarik. Bekerja
disini layaknya bekerja dengan sistem operasi DOS (Disk Operating
Systems).

Untuk kembali ke desktop, Anda bisa tekan tombol Ctrl+Alt+F7 sampai
Ctrl+Alt+F12. Bergantung dari sesi desktop yang digunakan (Secara
default menggunakan Ctrl+Alt+F7 jika Anda tidak memanfaatkan fitur
pindah pengguna untuk mengaktifkan lebih dari satu sesi desktop).

#### <span id="anchor-182"></span>Pengenalan Antarmuka Teks 

Setelah Anda membuka terminal atau login di dalam virtual console, Anda
akan diminta untuk memasukkan perintah yang ingin Anda jalankan. Tempat
Anda mengetik berada pada kursor/penanda yang berkedip-kedip. Pada
bagian kiri kursor tersebut, Anda akan melihat teks seperti berikut :

-   Teks tersebut memiliki berbagai informasi sebagai berikut :
-   Teks ***tambora*** sebelum tanda at (@) merupakan nama id login
    pengguna yang menggunakan antarmuka teks,
-   Teks ***blankon ***setelah tanda at (@) merupakan nama komputer yang
    digunakan pada saat bekerja,
-   Teks ***\~*** setelah tanda titik dua (:) menunjukan lokasi
    direktori tempat bekerja. Folder **\~** secara umum berada pada
    lokasi home/user yaitu pada contoh diatas adalah ***home/tambora***.
-   Tanda ***\$*** pada bagian akhir menunjukkan posisi bekerja pada
    tingkatan pengguna umum. Apabila bekerja dalam mode administratif,
    maka tanda tersebut akan berubah menjadi ***\#***.
-   Untuk menjalankan suatu perintah, dimulai dengan mengetikkan baris
    perintah lalu diikuti dengan menekan tombol ***Enter*** ( ¿ ).
    Sebagai contoh, untuk menampilkan isi suatu folder/direktori,
    dimulai dengan mengetikkan ketik perintah ***ls*** lalu diikuti
    dengan tombol ***Enter*** ( ¿ ). Hasil yang didapat akan tampak
    seperti berikut.

Untuk menjalankan perintah yang bersifat administratif, dapat dilakukan
dengan menggunakan perintah ***sudo ***sebelum perintah yang ingin
dijalankan. Untuk menjalankan perintah tersebut pengguna harus memiliki
wewenang berupa password *root*. Misalnya, jika ingin menghapus berkas
***blankon.txt*** pada folder /Document (Dalam hal ini, Anda tidak
memiliki hak untuk mengelola folder /opt), Anda bisa ketik perintah
“sudo rm blankon.txt”.

##### PERHATIAN: 

-   Meskipun pengguna memiliki hak akses untuk menjalankan bersifat
    administratif (yaitu root), secara default pengguna tidak dapat
    menggunakan hak akses tersebut untuk login. Anda bisa login ke
    ***root ***dengan cara mengetik perintah ***sudo su -***.
-   Dengan perintah tersebut tanda \$ untuk suatu user akan berganti
    dengan tanda \# sebagai penanda pengguna hak akses root

#### <span id="anchor-183"></span>Perintah-perintah dalam Antarmuka Teks 

Berikut adalah berbagai penjelasan dari perintah-perintah dalam
pengelolaan berkas secara sederhana menggunakan antarmuka teks.

#### <span id="anchor-184"></span>Berpindah Folder/Direktori (cd) 

Perintah ***cd (change directory) ***dapat dipergunakan untuk berpindah
dari satu direktori ke direktori lainnya. Secara umum perintah yang
digunakan adalah ***cd** *lalu diikuti dengan nama direktori yang akan
dibuka. Sebagai contoh, apabila hendak berpindah menuju direktori
***Document ***pada folder ***home***, gunakan perintah ***cd
Documents/***. Namun apabila sedang tidak berada di direktori home dapat
mengunakan perintah ***cd \~/Documents/***.

Apabila akan berpindah ke direktori satu tingkat diatas direktori saat
ini dapat mengunakan perintah ***cd ..***

<span id="anchor-185"></span>

#### Melihat Isi Folder/Direktori (ls) 

Untuk melihat isi dari suatu direktori yang aktif, gunakan perintah
***ls (list)***.

Perintah ls juga dapat digunakan untuk menampilkan lokasi folder
tertentu. Sebagai contoh untuk menampilkan isi direktori usr pada
hirarki tertinggi, gunakan perintah ***ls /usr. ***

Untuk menampilkan informasi lebih detail mengenai suatu direktori, dapat
ditambahkan perintah tambahan ***-l***, sehingga perintah lengkap untuk
menampilkan keterangan dari direktori /usr adalah ***ls -l /usr.***

#### <span id="anchor-186"></span>Membuka Berkas 

Selain menggunakan ***Menu ***untuk membuka suatu berkas dengan aplikasi
tertentu, dengan menjalankan perintah di terminal juga dapaat membuka
berkas tersebut. Sebagai contoh apabila hendak membuka berkas
***dokumentasi\_tambora.odt*** dengan aplikasi LibreOffice, dapat
menggunakan perintah ***soffice dokumentasi\_tambora.odt***.

##### 

##### CATATAN:

-   Apabila hendak menjalankan aplikasi berbasis grafis, maka diharuskan
    menggunakan antarmuka teks yang berada di pada mode grafis alias
    terminal emulator. Jika tidak, maka akan muncul pesan kesalahan.
-   Pada saat aplikasi sedang dijalankan, Jangan menutup atau mengakhiri
    sesi antarmuka teks, karena akan menyebabkan aplikasi yang dibuka
    tertutup secara paksa dan menyebabkan kehilangan berkas.

#### <span id="anchor-187"></span>Membuat Direktori (mkdir) 

Untuk membuat direktori, Anda bisa menggunakan perintah ***mkdir (make
directories) ***dengan format ***mkdir &lt;nama\_direktori&gt;.
***Sebagai contoh akan dibuat sebuah direktori dengan nama latihan. Maka
perintah yang digunakan adalah ***mkdir latihan***.

#### <span id="anchor-188"></span>Menghapus Direktori (rmdir) 

Untuk menghapus suatu direktori, digunakan perintah ***rmdir
&lt;nama\_direktori&gt;***. Syarat yang harus dipenuhi untuk menghapus
suatu direktori adalah direktori tersebut harus kosong tidak berisi
direktori maupun berkas.

#### Membuat berkas baru (cat)

Perintah ***cat (concatenate)*** berfungsi untuk menampilkan isi suatu
berkas dilayar. Selain itu perintah **cat **dapat digunakan untuk
membuat berkas baru berbasis teks. Untuk membuat berkas baru digunakan
perintah cat &gt; **&lt;nama\_berkas&gt; **sebagai contoh ***cat &gt;
blankon.txt***. Sedangkan untuk menampilkan isi dari berkas tersebut
dapat digunakan perintah ***cat blankon.txt.***

#### <span id="anchor-189"></span>Menghapus Berkas (rm) 

Untuk menghapus suatu berkas, gunakan perintah ***rm (remove files or
directories) *** lalu diikuti dengan nama berkas atau dilengkapi dengan
path (alamat lengkapnya) jika diperlukan.

##### Peringatan:

-   Setelah Anda menjalankan perintah ini, berkas akan dihilangkan
    begitu saja tanpa konfirmasi. Jadi, hati-hati dalam menggunakannya.

Jika ingin menghapus suatu isi folder sampai isinya secara rekursif,
Anda juga bisa gunakan perintah ini dengan menambahkan opsi “-R”. Sekali
lagi, hati-hati dalam menggunakan perintah ini.

#### <span id="anchor-190"></span>Menggandakan Berkas (cp) 

Untuk menggandakan berkas, dapat menggunakan perintah ***cp (copy)
***dengan format ***cp &lt;berkas-sumber&gt;
&lt;nama-berkas-baru&gt;***”. Apabila diperlukan dapat ditambahkan
lokasi dari ***&lt;berkas -sumber&gt;*** dan lokasi
***&lt;nama-berkas-baru&gt;. ***Contoh yang diberikan apabila ingin
menggandakan berkas ***blankon.txt ***ke berkas
***blankon\_jadi\_dua.txt ***dengan perintah ***cp blankon.txt
blankon\_jadi\_dua.txt.***

Sama dengan perintah ***rm***, Anda bisa manfaatkan opsi ***-R***
apabila ingin menggandakan suatu folder secara rekursif. Dalam contoh
ditampilkan user menggandakan semua berkas dalam direktori ***blankon
***ke direktori baru bernama ***tambora***

#### <span id="anchor-191"></span>**Memindahkan Berkas/Folder** ***(mv)*** 

Ada kalanya pengguna perlu untuk memindahkan suatu berkas atau
direktori. Untuk melakukan hal tersebut dapat menggunakan perintah mv
***(move). ***Format penulisan hampir sama dengan perintah ***cp
***memindahkan berkas/folder. Pada contoh ditunjukkan pengguna memindah
berkas ***blankon\_rote.txt ***pada direktori ***blankon ***menuju ke
direktori ***tambora*** dengan nama berkas yang sama

#### <span id="anchor-192"></span>**Mengubah Nama Berkas/Folder** ***(mv)*** 

Selain untuk memindahkan suatu berkas atau direktori. Perintah mv dapat
digunakan untuk mengubah nama berkas atau direktori. Cara penggunaan
sama dengan cara memindahkan berkas atau direktori. Contoh: apabila
ingin mengubah nama blankon\_jadi\_dua.txt menjadi blankon\_tambora.txt,
maka penulisan baris perintah yaitu ***mv blankon\_jadi\_dua.txt
blankon\_tambora.txt.***

#### <span id="anchor-193"></span>**Mengubah Hak Akses Berkas/Folder** ***(chmod) ***

***chmod (change file mode bits)*** digunakan untuk mengubah hak akses
berkas/direktori. Penggunaan perintah ini mengikuti format ***chmod
&lt;\*\*\*&gt; &lt;nama\_berkas&gt;.*** **&lt;\*\*\*&gt;** Merupakan hak
akses yang terdiri dari tiga angka oktal (angka 0 hingga angka 7). Angka
ke-1 merupakan hak untuk pemilik, angka ke-2 merupakan hak untuk grup
dan angka ke-3 merupakan hak untuk selain pemilik dan grup.
Masing-masing bagian diisi dengan angka basis 8, dimana hak baca
bernilai 4, hak tulis bernilai 2, hak eksekusi bernilai 1.

Sebagai contoh, untuk mengubah berkas ***blankon\_tambora.txt ***agar
mendapat hak baca (4) ,tulis (2) dan eksekusi (1) untuk pemilik (total
7), sedangkan yang untuk grup serta lainnya hanya memiliki hak baca(2)
dan eksekusi(1) , perintah yang digunakan adalah ***chmod 755
blankon\_tambora.txt***.

Untuk memberikan suatu hak akses secara rekursif pada suatu folder, Anda
bisa menambahkan opsi “-R”. Misalnya, jika ingin memberikan hak mutlak
(hak baca,tulis,eksekusi untuk semua aspek) pada direktori tambora, Anda
bisa ketik perintah ***chmod 777 -R tambora/***.

Untuk menampilkan hak akses suatu berkas/folder, Anda bisa manfaatkan
perintah “ls -l”. Kemudian, Anda akan melihat seperti karakter yang
dicetak tebal yang merupakan hak akses dari berkas tersebut. Keenam
karakter itu dibagi menjadi tiga, *bagian pertama *merupakan hak akses
pemilik, *bagian kedua *merupakan hak akses grup dan *bagian terakhir
*merupakan hak akses selain pemilik dan grup.

##### Keterangan:

-   r : Hak Baca, w : Hak tulis, x : Hak eksekusi

#### Mengubah ID Pemilik atau Grup pada Berkas/Folder (chown) 

Untuk mengubah id pemilik atau grup pada berkas/folder, gunakan perintah
***chown (change file owner and group)*** dengan format ***chown
&lt;id-pengguna&gt;:&lt;id-grup&gt; &lt;nama\_berkas&gt; . ***

Sebagai contoh, apabila ingin mengubah kepemilikan pengguna dan grup
dari berkas blankon\_tambora.txt menjadi kepemilikan www-data baik
pengguna maupun grup, maka perintah yang digunakan adalah sudo chown
www-data:www-data blankon\_tambora.txt.

##### Catatan : 

-   www-data adalah standar hak akses untuk berkas web publik yang
    sering digunakan oleh web server.

#### <span id="anchor-194"></span>Membuat Berkas Tar (tar) 

***Tar (tape or disc archive) ***merupakan program yang berfungsi untuk
menyatakan beberapa berkas atau direktori ke dalam satu berkas yang
disebut dengan *tarfile/tarball*. Perintah ini sangat berguna untuk
melakukan backup.

Untuk membuat berkas tar, selain melalui aplikasi pengelola arsip pada
desktop, Anda juga bisa gunakan perintah tar dengan format “***tar -f
&lt;nama\_berkas.tar&gt; &lt;nama\_berkas\_1/direktori\_1&gt;
&lt;nama\_berkas\_2/direktori\_2&gt; .....***. Format yang sering
digunakan adalah perintah ***tar -czf &lt;nama\_berkas.tar.gz&gt;
&lt;nama\_berkas&gt;***

Sedangkan untuk membongkar kembali dan melakukan dekompresi, dapat
digunakan perintah dengan format ***tar zxf &lt;nama\_berkas.tar.gz&gt;
-C &lt;direktori tujuan&gt;***.

#### <span id="anchor-195"></span>Pencarian Berkas (find) 

Untuk mencari berkas, gunakan perintah ***find ***dengan format ***find
&lt;direktori&gt; -name &lt;nama\_berkas&gt;***. Sebagai contoh, apabila
diinginkan untuk melakukan pencarian berkas dengan nama ***blankon***,
maka dapat dilakukan dengan perintah ***find \~ -name blankon***. Ingat
tanda \~ menunjukkan posisi berkas berada di home.

Pencarian juga dapat dilakukan apabila mengetahui ekstensi dari berkas
yang diinginkan, misal ekstensi txt untuk berkas file teks. Maka
perintah yang dapat dilakukan adalah find \~ -name \*txt

##### Catatan:

-   Jika ingin menuliskan nama berkas/direktori lebih cepat, dapat
    dilakukan dengan mengetik satu/beberapa huruf awal dari nama
    berkas/direktori tersebut, kemudian diikuti dengan tombol Tab pada
    papan ketik. Sebagai contoh, jika ingin mengetik nama berkas
    “blankon.txt” lebih cepat, pengguna dapat mengetik huruf “b” saja
    atau “bl”, kemudian diikuti dengan menekan tombol Tab. Secara
    otomatis, nama berkas akan dilengkapi (a***uto complete)***.

Sebenarnya, masih banyak lagi perintah-perintah untuk antarmuka teks
yang bisa Anda gunakan untuk bekerja. Untuk melakukan otomatisasi kerja,
pengguna juga dapat membuat sebuah berkas yang berisi baris perintah
dengan hak akses eksekusi. Berkas tersebut dinamakan dengan *shell
script*. Otomatisasi pekerjaan sangat penting bagi administrator untuk
memperingan dan mempercepat pekerjaannya dalam jaringan. Untuk
mempelajari shell script lebih lanjut, dapat membaca buku tentang Bash
Scripting atau mencari referensi melalui internet.

