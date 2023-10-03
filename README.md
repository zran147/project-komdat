<h6 align="center"><img src="screenshot/logo-itod-small.png"></h6>

# IT Today 2023 Official Website

[Sekilas Tentang](#sekilas-tentang) | [Instalasi](#instalasi) | [Konfigurasi](#konfigurasi) | [Otomatisasi](#otomatisasi) | [Cara Pemakaian](#cara-pemakaian) | [Pembahasan](#pembahasan) | [Referensi](#referensi)
:---:|:---:|:---:|:---:|:---:|:---:|:---:

## Sekilas Tentang
IT Today merupakan acara tahunan yang diselenggarakan oleh Himpunan Mahasiswa Ilmu Komputer (HIMALKOM) IPB dan Departemen Ilmu Komputer IPB. Tahun ini, IT Today 2023 menghadirkan serangkaian acara menarik, seperti seminar komunitas, workshop, kompetisi, seminar nasional, dan awarding. **IT Today 2023 Official Website** ini merupakan aplikasi *Management Information System* (MIS) berbasis website yang dirancang untuk memberikan informasi lengkap mengenai seluruh rangkaian acara IT Today. Selain informasi acara yang lengkap, peserta acara IT Today dapat mendaftarkan dirinya langsung melalui website ini untuk mengikuti acara maupun kompetisi yang diselenggarakan. 

# Instalasi

### Kebutuhan sistem :
- OS: Linux/Windows
- Apache Web server 2.4.57
- PHP 8.0.29
- MySQL CE 8.0.34
- Dewa Cloud
- phpMyAdmin

### Proses instalasi :
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


- Kemudian, kita menjalankan command berikut dan mengubah isi `.env`
    ```
    cp .env.example .env
    ```

  <img src="screenshot/ss-komdat-8.jpg">


- Kemudian, kita menjalankan command command berikut
    ```
    composer install --ignore-platform-reqs
    composer update
    php artisan storage:link
    php artisan key:generate
    php artisan migrate:fresh --seed
    ```


##  Maintenance

**Backup database**
- Untuk memelihara database, digunakan *Notion* untuk membuat salinan data sekaligus menghubungi pendaftar/tim untuk melakukan pembayaran.

  <img src="screenshot/ss-komdat-16.jpg">

**Menunggu berkas**
- Admin harus login ke website secara berkala, untuk mengecek dan menverifikasi berkas-berkas pendaftar/tim.
  
  <img src="screenshot/ss-komdat-17.jpg">
  
  <img src="screenshot/ss-komdat-18.jpg">


## Cara Pemakaian

1. Home Page
   
   Home Page ini merupakan page pertama yang akan dijumpai pengguna, baik itu *user* ataupun admin ketika mengakses website. Terdapat *navigation bar* yang berisikan berbagai navigasi bagi pengguna yang ingin mengakses fitur lainnya. Di dalam Home Page juga terdapat berbagai fitur dan informasi lainnya, seperti _events_ yang terdapat _carousel image_ berupa informasi singkat dari _event_ yang akan dilaksanakan oleh IT Today, _competitions_ berisikan _carousel image_ informasi singkat mengenai kompetisi yang akan diadakan, _about us_ berisikan informasi singkat mengenai IT Today, sponsor yang tergabung di dalam acara, _reach us_ yang digunakan sebagai kontak dari penyelenggara, dan juga _footer_ yang berisikan identitas atau alamat dari penyelenggara _event_.
     
     <img src="screenshot/komdat-tampilan1.png">
     <img src="screenshot/komdat-tampilan2.png">
     <img src="screenshot/komdat-tampilan3.png">
     <img src="screenshot/komdat-tampilan4.png">
     <img src="screenshot/komdat-tampilan5.png">
     <img src="screenshot/komdat-tampilan6.png">
     <img src="screenshot/komdat-tampilan7.png">

2. Events Page
     Events Page berisikan informasi _event_ apa saja yang akan dilaksanakan. Berbeda dengan fitur events pada Home Page, fitur ini ditampilkan pada _navigation bar_, berisikan penjelasan detail untuk setiap kegiatan yang akan dilaksanakan.

    <img src="screenshot/komdat-tampilan8.png">

   
3. Competitions Page

    Berisikan informasi detail mengenai kompetisi yang akan dilaksanakan.
  
    <img src="screenshot/komdat-tampilan9.png">
  
4. Register Page
   
     Digunakan untuk melakukan registerasi saat membuat akun pertama kali.

     <img src="screenshot/komdat-tampilan10.png">
   
5. Login Page
   
     Digunakan untuk melakukan _log in_ pada akun menggunakan email dan _password_ yang telah dibuat.

     <img src="screenshot/komdat-tampilan11.png">

***AS USER***
  1. Melakukan registrasi pada _registration page_
     
     <img src="screenshot/as-user1.png">
     
  2. Setelah melakukan registrasi, pengguna akan diarahkan menuju home page
     
     <img src="screenshot/as-user2.png">
     
  3. Pengguna melakukan verifikasi account. Verifikasi akan dilakukan melalui email yang dikirimkan
     
     <img src="screenshot/as-user3.png">
     
  4. Setelah melakukan verifikasi, pengguna akan diarahkan menuju profile page. Pada page tersebut, pengguna akan melihat daftar event dan kompetisi yang diikuti. Jika belum mendaftar maka tampilan akan kosong.
     
     <img src="screenshot/as-user4.png">
     <img src="screenshot/as-user5.png">
     
  5. Selanjutnya, menuju competitions page untuk melakukan pendaftaran kompetisi.
     
      <img src="screenshot/as-user6.png">
      
  6. Pengguna akan diarahkan agar mengisikan identitas tim yang akan diregistrasi.
      
      <img src="screenshot/as-user7.png">
      
  7. Setelah itu, pengguna akan mengisikan masing-masing identitas anggota timnya.
      
      <img src="screenshot/as-user8.png">
      
  8. Setelah melakukan submit, registrasi tim dan anggota akan diverifikasi oleh admin.
      
      <img src="screenshot/as-user9.png">
      <img src="screenshot/as-user10.png">

  9. Peserta akan mendapatkan email dari admin jika persyaratan berkas telah terpenuhi setelah pengecekan.
      
     <img src="screenshot/as-user11.png">
     <img src="screenshot/as-user12.png">
     
  10. Setelah peserta, menekan klik pada email verifikasi, akan di bawa menuju login page.

      <img src="screenshot/as-user15.png">
      
  11. Akhirnya, status peserta sudah terverifikasi dan dapat diselesaikan dengan melakukan pembayaran.

      <img src="screenshot/as-user13.png">
      <img src="screenshot/as-user14.png">

***AS ADMIN***
  1. Masuk ke akun admin dan akan menampilkan halaman depan web versi admin. Selanjutnya, klik menu `dashboard`.
     
     <img src="screenshot/ss-komdat-9.jpg">

  2. Pada menu `dashboard`, Admin dapat melihat jumlah pendaftar pada kompetisi.
     
     <img src="screenshot/ss-komdat-10.jpg">

  3. Admin memilih salah satu kompetisi, misal `Hacktoday`. Maka akan tampil list pendaftar/tim dari kompetisi. Klik `detail` untuk melihat detail informasi tim.
     
     <img src="screenshot/ss-komdat-11.jpg">

  4. Halaman ini berisi detail informasi tim, status verifikasi tim, dan berkas registrasi yang *di-submit* oleh tim. 
     
     <img src="screenshot/ss-komdat-12.jpg">

  5. Kemudian, Admin akan melakukan verifikasi berkas dengan `acc verification` atau `refuse verification`.
     
     <img src="screenshot/ss-komdat-13.jpg">

  6. Setelah melakukan verifikasi, Admin dapat mengirim pesan melalui email untuk memberikan feedback ke pendaftar/tim.
     
     <img src="screenshot/ss-komdat-14.jpg">

  7. Setelah verifikasi *di-acc*. Akan muncul kolom pembayaran dan Admin dapat melakukan `acc payment` atau `refuse payment` terhadap bukti pembayaran yang *di-upload* pendaftar/tim.
     
     <img src="screenshot/ss-komdat-15.jpg">

## Pembahasan
**IT Today 2023 Official Website** merupakan aplikasi *Management Information System* (MIS) berbasis website yang digunakan oleh mahasiswa sarjana Departemen Ilmu Komputer IPB dalam mengadakan rangkaian acara IT Today. Website ini digunakan sebagai media informasi mengenai berbagai *event* seperti seminar dan juga informasi kompetisi. Selain itu, IT Today juga digunakan untuk melakukan manajemen pendaftaran peserta kompetisi. Aplikasi ini dibangun dengan menggunakan HTML, CSS, JavaScript, dan bantuan *framework* Bootstrap sebagai pengembangan *front end*. Pengembangan *back end* dikembangkan dengan menggunakan bahasa PHP melalui *framework* Laravel dan Livewire. Database yang digunakan ialah *relational database management system*, dengan menggunakan MySQL. **IT Today** memiliki berbagai kelebihan yang dapat memberikan value yang lebih bagi pengguna, di antaranya adalah 

- Memiliki panel administrasi yang juga terbagi menjadi *role* bagi masing-masing admin, sehingga memudahkan dalam memanajemen *task* yang diperlukan. 
- Memiliki tampilan UI yang sangat menarik dan interaktif, sehingga tidak membuat bosan pengguna.
- Memiliki navigasi yang cukup jelas, sehingga tidak membuat pengguna menjadi kebingungan.
- Dari segi *responsivity*, aplikasi dikembangkan dengan cukup responsif, sehingga tampilannya dapat diakses dengan mudah dan nyaman di berbagai ukuran *device*.
- Berbasis bahasa Inggris dan Indonesia, sehingga memudahkan banyak pengguna.
- Berbagai fitur disediakan dan dengan jelas terbagi oleh masing-masing *role*, sehingga memudahkan penggunaannya dan keamanannya data juga terjaga.
- Memiliki keaamanan yang dikembangkan dengan sangat baik di berbagai fitur dan layanannya.
- Terdapat fitur pengiriman email secara otomatis.

Di samping itu, **IT Today 2023 Official Website** memiliki beberapa kekurangan di antaranya ialah

- Tidak dapat mengatur atau melakukan *sorting* terhadap urutan peserta kompetisi pada *dashboard*.
- Konfirmasi/verifikasi berkas dan bukti pembayaran yang masih dilakukan secara manual oleh admin.
- Backup database masih dilakukan secara manual melalui *Notion*.
- Admin harus login ke web secara berkala untuk mengecek berkas pendaftar/tim sudah terupload atau belum.

Jika dibandingkan dengan *Management Information System (MIS)* sejenisnya seperti **Compfest**, **IT Today** memiliki keunggulan dan kekurangan. Berikut adalah perbandingan antara kedua MIS tersebut:

1. Fitur yang disediakan oleh **Compfest** jauh lebih banyak dibandingkan pada **IT Today**.
2. **Compfest** memiliki *light mode* dan *night mode*, sehingga pengguna dapat menyesuaikan preferensinya.
3. **Compfest** dapat melakukan _authentication_ menggunakan Google Account.

## Referensi

1. [Website IT Today](http://it-today.user.cloudjkt01.com/) - IT Today
2. [Website Compfest](https://recruitment.compfest.id/) - Compfest
