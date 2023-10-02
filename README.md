<h1 align="center"><img src="https://images.squarespace-cdn.com/content/v1/61d85b007f3a131e371c47a7/b7a232c6-28f2-4a91-8142-72cb3818d984/Noted_Logo_Navy.png?format=1500w"></h1>

# Aplikasi Web "Noted"

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:|:---:|:---:

## Sekilas Tentang
**Noted** merupakan aplikasi berbasis website yang bertujuan sebagai pencatatan keuangan dan penyimpan catatan. Aplikasi ini tidak hanya menyediakan fungsi dasar pencatatan transaksi, tetapi juga dilengkapi dengan fitur visualisasi yang memungkinkan pengguna melihat data keuangan mereka dalam bentuk grafik. Dengan Noted, pengguna dapat dengan mudah melacak dan memahami pola pengeluaran dan pemasukan mereka melalui representasi visual yang jelas dan informatif sehingga memudahkan pengguna untuk mengelola keuangan pribadi dengan lebih efisien.

## Instalasi

#### Kebutuhan sistem :
    - Sistem Operasi : Linux atau Windows

#### Proses instalasi :
- Membuat environment baru dengan application server apache versi terbaru dengan **php versi 8.0.29**

<img src="screenshot/ss-komdat-1.jpg">

- Selain application server, digunakan database server berupa database mysql. Dan mengubah domain menjadi [it-today.user.cloudjkt01.com](it-today.user.cloudjkt01.com), setelah menekan tombol `create`, ditunggu beberapa menit agar environment tercipta

<img src="screenshot/ss-komdat-2.jpg">

- Deploy menggunakan git dan memasukkan link repository github beserta token sebagai autentikasi untuk repository privat

<img src="screenshot/ss-komdat-3.jpg">

- Auto-resolve conflicts dimatikan dan tombol `deploy` ditekan

<img src="screenshot/ss-komdat-4.jpg">

- Berikutnya adalah membuat database baru pada `phpmyadmin`

<img src="screenshot/ss-komdat-5.jpg">

- Selanjutnya adalah membuat file `.htaccess` pada `~/webroot/ROOT`

<img src="screenshot/ss-komdat-6.jpg">


## Konfigurasi (opsional)

Setting server tambahan yang diperlukan untuk meningkatkan fungsi dan kinerja aplikasi, misalnya:
- batas upload file
- batas memori
- dll

Plugin untuk fungsi tambahan
- login dengan Google/Facebook
- editor Markdown
- dll


##  Maintenance (opsional)

Setting tambahan untuk maintenance secara periodik, misalnya:
- buat backup database tiap pekan
- hapus direktori sampah tiap hari
- dll


## Otomatisasi (opsional)

Skrip shell untuk otomatisasi instalasi, konfigurasi, dan maintenance.


## Cara Pemakaian

- Tampilan aplikasi web
- Fungsi-fungsi utama
- Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot


## Pembahasan
**Noted** merupakan aplikasi berbasis website yang ditulis dengan menggunakan HTML, CSS, JavaScript, dan bantuan *framework* Bootstrap sebagai pengembangan *front end*. Pengembangan *back end* dikembangkan dengan menggunakan bahasa PHP melalui *framework* Laravel. Database yang digunakan ialah *relational database management system*, dengan menggunakan MySQL. Noted memiliki berbagai kelebihan yang dapat memberikan value yang lebih bagi pengguna, di antaranya adalah 

- Dari segi *responsivity*, aplikasi dikembangkan dengan cukup responsif, sehingga tampilannya dapat diakses dengan mudah dan nyaman di berbagai ukuran *device*.
- Berbasis bahasa Indonesia sehingga memudahkan bagi pengguna Indonesia.
- Aplikasi ini memiliki fitur yang interaktif dengan adanya *chart* yang melakukan visualisasi terhadap input yaitu laporan keuangan dan juga catatan lainnya.
- Penggunaan memori yang kecil karena merupakan *information system application* berskala kecil.
- Setiap pengguna dapat mengakses aplikasi dan juga berbagai fitur yang disediakan dengan gratis, sehingga biaya tidak menjadi kendala bagi pengguna.

Di samping itu, Noted memiliki beberapa kekurangan di antaranya ialah

- Tidak adanya panel administrasi dikarenakan fokus dari pengembangan aplikasi ini lebih difokuskan terhadap *client side*.
- Saat ini, Noted hanya dikembangkan dengan *single language*, sehingga terdapat *language barrier* bagi pengguna yang tidak dapat berbahasa Indonesia dan akan mengalami kesulitan dalam mengakses aplikasi.
- Terdapat beberapa fitur yang memiliki tujuan secara implisit, sehingga akan membingungkan bagi pengguna yang tidak diberikan petunjuk penggunaannya, terutama bagi pengguna baru.

Jika dibandingkan dengan *Money Management System (MMS)* sejenisnya seperti **Actual**, **Noted** memiliki keunggulan dan kekurangan. Berikut adalah perbandingan antara kedua MMS tersebut:

1. **Actual** menyediakan tampilan UI yang fleksibel dan simpel dengan fitur dropdown yang interaktif, sehingga pengguna bisa lebih nyaman menggunakannya. Sedangkan **Noted** hanya menyediakan tampilan yang biasa, namun tetap mengedepankan segi manfaat penggunaannya.
2. Fitur yang disediakan oleh **Actual** jauh lebih banyak dibandingkan pada **Noted**.
3. **Actual** menyediakan *multifile* untuk mencatat kebutuhan keuangan yang berbeda (*misalnya: personal, bisnis, dll*), sedangkan pada **Noted** masih *singlefile*.
4. **Actual** memiliki fitur *Schedules* sehingga dapat melakukan penjadwalan untuk memanajemen keuangan pengguna, sementara **Noted** belum menyediakan fitur tersebut.

## Referensi

Cantumkan tiap sumber informasi yang anda pakai.
