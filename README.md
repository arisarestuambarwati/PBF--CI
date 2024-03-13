# ARISA RESTU AMBARWATI (220202030)

## Welcome to CodeIgniter4
CodeIgniter adalah alat yang mempercepat pembangunan situs web PHP. Dengan banyaknya perpustakaan yang tersedia, Anda bisa membangun proyek lebih cepat daripada harus menulis kode dari awal. Antarmuka sederhana dan struktur yang logis memudahkan akses perpustakaan tersebut. Dengan CodeIgniter, Anda bisa fokus pada kreativitas Anda dengan meminimalkan jumlah kode yang harus Anda tulis.

## Server Requirements
- PHP dan Ekstensi yang Diperlukan
- Ekstensi PHP Opsional
- Basis Data yang Didukung

    ### PHP dan Ekstensi yang Diperlukan
      Diperlukan PHP versi 7.4 atau lebih baru, dengan ekstensi PHP berikut diaktifkan:
      - internasional
      - mbstring
      - json

    ### Ekstensi PHP Opsional
      Ekstensi PHP berikut harus diaktifkan di server Anda:
      - mysqlnd (jika Anda menggunakan MySQL)
        MySQL Native Driver (mysqlnd) adalah sebuah driver PHP yang menyediakan fungsi-fungsi untuk mengakses MySQL databases secara langsung tanpa menggunakan pustaka tambahan.
      - curl (jika Anda menggunakan CURLRequest )
        Curl adalah alat baris perintah yang digunakan untuk mentransfer data melalui berbagai protokol, seperti HTTP, HTTPS, FTP, dan lainnya.
      - imagick (jika Anda menggunakan kelas Gambar ImageMagickHandler)
      ImageMagick adalah sebuah perangkat lunak open-source yang menyediakan beragam utilitas untuk membuat, mengedit, mengonversi, atau menampilkan gambar.
      - gd (jika Anda menggunakan kelas Gambar GDHandler)
        GD adalah singkatan dari "Graphics Draw", sebuah library yang digunakan untuk manipulasi gambar dalam PHP
      - simplexml (jika Anda memformat XML)
        SimpleXML adalah sebuah ekstensi PHP yang memungkinkan pengolahan XML menjadi lebih mudah dengan menggunakan pendekatan berbasis objek. 

      Ekstensi PHP berikut diperlukan saat Anda menggunakan server Cache:
      - memcache (jika Anda menggunakan kelas Cache MemcachedHandler dengan Memcache)
        Memcache adalah sistem caching yang menyimpan data dalam bentuk pasangan kunci-nilai di dalam memori RAM.
      - memcached (jika Anda menggunakan kelas Cache MemcachedHandler dengan Memcached)
        Memcached, di sisi lain, adalah versi yang diperbarui dari Memcache.
      - redis (jika Anda menggunakan kelas Cache RedisHandler)
        Redis adalah sebuah basis data sumber terbuka yang berkinerja tinggi dan berbasis memori. 

      Ekstensi PHP berikut diperlukan saat Anda menggunakan PHPUnit:
      - dom (jika Anda menggunakan kelas TestResponse )
        DOM adalah singkatan dari Document Object Model, yang merupakan representasi struktur dokumen HTML atau XML sebagai objek, memungkinkan pengaksesan dan manipulasi elemen-elemen di dalam dokumen tersebut.
      - libxml (jika Anda menggunakan kelas TestResponse )
        Libxml adalah sebuah perpustakaan (library) yang menyediakan fungsionalitas pemrosesan XML (eXtensible Markup Language).
      - xdebug (jika Anda menggunakan CIUnitTestCase::assertHeaderEmitted())
        Xdebug adalah sebuah alat debug untuk PHP yang membantu pengembang dalam mengidentifikasi dan memperbaiki kesalahan dalam kode mereka. 

    ### Basis Data yang Didukung
      Basis data yang didukung saat ini adalah:
      * MySQL melalui MySQLidriver (hanya versi 5.1 ke atas)
      * PostgreSQL melalui Postgredriver (hanya versi 7.4 dan lebih tinggi)
      * SQLite3 melalui SQLite3driver
      * Microsoft SQL Server melalui SQLSRVdriver (hanya versi 2005 dan lebih tinggi)
      * Oracle Database melalui OCI8driver (hanya versi 12.1 dan lebih tinggi)

      Tidak semua driver telah dikonversi/ditulis ulang untuk CodeIgniter4. Daftar dibawah ini untuk yang luar biasa.
      * MySQL (5.1+) melalui driver pdo
      * Oracle melalui driver pdo
      * PostgreSQL melalui driver pdo
      * MSSQL melalui driver pdo
      * SQLite melalui sqlite (versi 2) dan driver pdo
      * CUBRID melalui driver cubrid dan pdo
      * Interbase/Firebird melalui driver ibase dan pdo
      * ODBC melalui driver odbc dan pdo (Anda harus tahu bahwa ODBC sebenarnya adalah lapisan abstraksi)

## Installation
CodeIgniter memiliki dua metode instalasi yang didukung: download manual, atau menggunakan Composer.

### Installasi Komposer
CodeIgniter4 memerlukan Composer 2.0.14 atau lebih baru.
1. Pastikan Anda telah menginstal Composer di sistem Anda. Jika belum, Anda dapat mengunduh dan menginstalnya dari https://getcomposer.org/.
2. Buka terminal atau command prompt.
3. Jalankan perintah Composer untuk membuat proyek CodeIgniter baru dengan code :
   ``` shell
   composer create-project codeigniter4/appstarter project-root
   ```
   Perintah di atas akan membuat folder root proyek .
4. Pindah direktori ke file yang telah dibuat sebelumnya
   ``` shell
   cd project-root
   ```
6. Upgrading
   Setiap kali ada rilis baru, maka dari baris perintah di root proyek Anda:
   ``` shell
   composer update
   ```
7. Update for Latest Dev
   Pembaruan untuk Pengembang Terbaru
   ``` shell
   php builds development
   ```
8. Revert to Stable Release
   Untuk mengembalikan perubahan, jalankan:
   ``` shell
   php builds release
   ```
### Pro
Instalasi yang relatif sederhana; mudah untuk diperbarui.

### Kontra
Anda masih perlu memeriksa perubahan file di ruang proyek (root, app, public, writeable) setelah memperbarui.

### Structure
Folder di proyek Anda setelah pengaturan:
* aplikasi, publik, tes, dapat ditulis
* vendor/codeigniter4/framework/system

### Installasi Manual
1. Unduh [versi terbaru], di link (https://github.com/CodeIgniter4/framework/releases/tag/v4.4.6) dan ekstrak file tersebut ke dalam direktori utama proyek Anda.
2. Setelah link dibuka kemudian scroll ke bawah sampai menemukan bagian Assets kemudian download folder Source Code (zip)
3. Setelah berhasil di download lalu ekstrak file tersebut.

### Pro
Unduh dan jalankan.

### Kontra
Anda perlu memeriksa perubahan file di ruang proyek (root, aplikasi, publik, tes, dapat ditulis) dan menggabungkannya sendiri.

### Structure
Folder di proyek Anda setelah disiapkan:
- aplikasi, publik, tes, dapat ditulis, sistem

### Local Development Server
Anda dapat meluncurkannya, dengan baris perintah berikut di direktori utama:
``` shell
php spark serve
```
Server pengembangan lokal dapat disesuaikan dengan tiga opsi baris perintah:
* Anda dapat menggunakan opsi CLI untuk menentukan host yang berbeda untuk menjalankan aplikasi di:--host
  ``` shell
  php spark serve --host example.dev
  ```
* Secara default, server berjalan pada port 8080 tetapi Anda mungkin memiliki lebih dari satu situs yang berjalan, atau sudah memiliki aplikasi lain yang menggunakan port itu. Anda dapat menggunakan opsi CLI untuk menentukan yang berbeda
  ``` shell
  php spark serve --port 8081
  ```
* Anda juga dapat menentukan versi PHP tertentu untuk digunakan, dengan opsi CLI, dengan nilainya atur ke jalur eksekusi PHP yang ingin Anda gunakan:
  ``` shell
  php spark serve --php /usr/bin/php7.6.5.4
  ```

## Build Your First Application

### Setting Routing Rules
Perutean mengaitkan URI dengan metode pengontrol. 

1. Buka file rute yang terletak di app/Config/Routes.php.
   ``` shell
   <?php

   use CodeIgniter\Router\RouteCollection;

   /**
   * @var RouteCollection $routes
   */
   $routes->get('/', 'Home::index');
   ```
2. Tambahkan baris berikut, setelah direktif rute untuk .'/'
   ``` shell
   use App\Controllers\Pages;

   $routes->get('pages', [Pages::class, 'index']);
   $routes->get('(:segment)', [Pages::class, 'view']);
   ```
3. Di sini, aturan kedua dalam objek cocok dengan permintaan GET ke jalur URI /pages, dan memetakan ke metode kelas.$routesindex()Pages
4. Aturan ketiga dalam objek cocok dengan permintaan GET ke segmen URI menggunakan placeholder , dan meneruskan parameter ke metode kelas.$routes(:segment)view()Pages
   
### Let’s Make our First Controller
Hal berikutnya yang akan Anda lakukan adalah menyiapkan pengontrol untuk ditangani halaman statis.

1. Buat file di app/Controllers/Pages.php dengan yang berikut ini kode.
   ``` shell
   <?php

   namespace App\Controllers;

   class Pages extends BaseController
   {
       public function index()
       {
          return view('welcome_message');
       }

       public function view($page = 'home')
       {
           // ...
       }
   }
   ```
### Create Views
Kami akan membuat dua "tampilan" (template halaman) yang bertindak sebagai footer dan header halaman kami.

1. Buat header di app/Views/templates/header.php dan tambahkan kode berikut:
   ``` shell
   <!doctype html>
<html>
<head>
    <title>CodeIgniter Tutorial</title>
</head>
<body>

    <h1><?= esc($title) ?></h1>
    ```
2. Sekarang, buat footer di app/Views/templates/footer.php itu termasuk kode berikut:
   ``` shell
   <em>&copy; 2022</em>
</body>
</html>
```

### Halaman Lengkap::view() Metode

1. Untuk memuat halaman-halaman itu, Anda harus memeriksa apakah yang diminta halaman benar-benar ada. Ketikkan kode : 

``` shell
<?php

namespace App\Controllers;

use CodeIgniter\Exceptions\PageNotFoundException; // Add this line

class Pages extends BaseController
{
    // ...

    public function view($page = 'home')
    {
        if (! is_file(APPPATH . 'Views/pages/' . $page . '.php')) {
            // Whoops, we don't have a page for that!
            throw new PageNotFoundException($page);
        }

        $data['title'] = ucfirst($page); // Capitalize the first letter

        return view('templates/header', $data)
            . view('pages/' . $page)
            . view('templates/footer');
    }
}
```
2. Jalankan aplikasi menggunakan server bawaan PHP dan ketikkan kode :
   ``` shell
   php spark serve
   ```

## News Section

### Create a Database to Work with
1. Anda perlu membuat database yang dapat digunakan untuk tutorial ini, dan kemudian mengkonfigurasi CodeIgniter untuk menggunakannya
2. Menggunakan klien database Anda, sambungkan ke database Anda dan jalankan perintah SQL di bawah ini (MySQL):
   ``` shell
   CREATE TABLE news (
    id INT UNSIGNED NOT NULL AUTO_INCREMENT,
    title VARCHAR(128) NOT NULL,
    slug VARCHAR(128) NOT NULL,
    body TEXT NOT NULL,
    PRIMARY KEY (id),
    UNIQUE slug (slug)
    );
    ```
3. Masukkan beberapa data di SQL seperti :
   ``` shell
   INSERT INTO news VALUES
    (1,'Elvis sighted','elvis-sighted','Elvis was sighted at the Podunk internet cafe. It looked like he was writing a CodeIgniter app.'),
    (2,'Say it isn\'t so!','say-it-isnt-so','Scientists conclude that some programmers have a sense of humor.'),
    (3,'Caffeination, Yes!','caffeination-yes','World\'s largest coffee shop open onsite nested coffee shop for staff only.');
   ```

### Connect to Your Database
Pastikan Anda telah mengonfigurasi database Anda dengan benar seperti yang dijelaskan dalam Konfigurasi Database:
``` shell
   database.default.hostname = localhost
   database.default.database = ci4tutorial
   database.default.username = root
   database.default.password = root
   database.default.DBDriver = MySQLi
```

### Create NewsModel
Buka direktori app/Models dan buat file baru bernama NewsModel.php dan tambahkan kode berikut.
``` shell
<?php

namespace App\Models;

use CodeIgniter\Model;

class NewsModel extends Model
{
    protected $table = 'news';
}
```

### Add NewsModel::getNews() Method
``` shell
public function getNews($slug = false)
    {
        if ($slug === false) {
            return $this->findAll();
        }

        return $this->where(['slug' => $slug])->first();
    }
```














