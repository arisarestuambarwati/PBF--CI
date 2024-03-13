# ARISA RESTU AMBARWATI (220202030)

## Welcome to CodeIgniter4
CodeIgniter adalah alat yang mempercepat pembangunan situs web PHP. Dengan banyaknya perpustakaan yang tersedia, Anda bisa membangun proyek lebih cepat daripada harus menulis kode dari awal. Antarmuka sederhana dan struktur yang logis memudahkan akses perpustakaan tersebut. Dengan CodeIgniter, Anda bisa fokus pada kreativitas Anda dengan meminimalkan jumlah kode yang harus Anda tulis.

## Server Requirements
- PHP dan Ekstensi yang Diperlukan
- Ekstensi PHP Opsional
- Basis Data yang Didukung

### PHP dan Ekstensi yang Diperlukan
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
- memcached (jika Anda menggunakan kelas Cache MemcachedHandler dengan Memcached) 
- redis (jika Anda menggunakan kelas Cache RedisHandler)
        
Ekstensi PHP berikut diperlukan saat Anda menggunakan PHPUnit:
- dom (jika Anda menggunakan kelas TestResponse )
- libxml (jika Anda menggunakan kelas TestResponse )
- xdebug (jika Anda menggunakan CIUnitTestCase::assertHeaderEmitted())

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
Tambahkan mengikuti kode ke model anda

``` shell
public function getNews($slug = false)
    {
        if ($slug === false) {
            return $this->findAll();
        }

        return $this->where(['slug' => $slug])->first();
    }
```

## Display the News
Sekarang setelah kueri ditulis, model harus dikaitkan dengan tampilan yang akan menampilkan item berita kepada pengguna.

### Adding Routing Rules
Ubah file app/Config/Routes.php Anda, sehingga terlihat sebagai berikut:

``` shell
<?php

// ...

use App\Controllers\News; // Add this line
use App\Controllers\Pages;

$routes->get('news', [News::class, 'index']);           // Add this line
$routes->get('news/(:segment)', [News::class, 'show']); // Add this line

$routes->get('pages', [Pages::class, 'index']);
$routes->get('(:segment)', [Pages::class, 'view']);
```

### Create News Controller
Buat pengontrol baru di app/Controllers/News.php.

``` shell
<?php

namespace App\Controllers;

use App\Models\NewsModel;

class News extends BaseController
{
    public function index()
    {
        $model = model(NewsModel::class);

        $data['news'] = $model->getNews();
    }

    public function show($slug = null)
    {
        $model = model(NewsModel::class);

        $data['news'] = $model->getNews($slug);
    }
}
```

### Complete News::index() Method
Ubah metode agar terlihat seperti ini:

``` shell
<?php

namespace App\Controllers;

use App\Models\NewsModel;

class News extends BaseController
{
    public function index()
    {
        $model = model(NewsModel::class);

        $data = [
            'news'  => $model->getNews(),
            'title' => 'News archive',
        ];

        return view('templates/header', $data)
            . view('news/index')
            . view('templates/footer');
    }

    // ...
}
```

### Create news/index View File
Buat app/Views/news/index.php dan tambahkan potongan kode berikutnya.

``` shell
<h2><?= esc($title) ?></h2>

<?php if (! empty($news) && is_array($news)): ?>

    <?php foreach ($news as $news_item): ?>

        <h3><?= esc($news_item['title']) ?></h3>

        <div class="main">
            <?= esc($news_item['body']) ?>
        </div>
        <p><a href="/news/<?= esc($news_item['slug'], 'url') ?>">View article</a></p>

    <?php endforeach ?>

<?php else: ?>

    <h3>No News</h3>

    <p>Unable to find any news for you.</p>

<?php endif ?>
```

### Complete News::show() Method
Tambahkan beberapa kode ke pengontrol dan buat tampilan baru. Kembali ke pengontrol dan perbarui metode dengan yang berikut:

``` shell
<?php

namespace App\Controllers;

use App\Models\NewsModel;
use CodeIgniter\Exceptions\PageNotFoundException;

class News extends BaseController
{
    // ...

    public function show($slug = null)
    {
        $model = model(NewsModel::class);

        $data['news'] = $model->getNews($slug);

        if (empty($data['news'])) {
            throw new PageNotFoundException('Cannot find the news item: ' . $slug);
        }

        $data['title'] = $data['news']['title'];

        return view('templates/header', $data)
            . view('news/view')
            . view('templates/footer');
    }
}
```
### Create news/view View File
Satu-satunya hal yang tersisa untuk dilakukan adalah membuat tampilan yang sesuai di app/Views/news/view.php. Masukkan kode berikut dalam file ini.

``` shell
<h2><?= esc($news['title']) ?></h2>
<p><?= esc($news['body']) ?></p>
```

Arahkan browser Anda ke halaman "berita" Anda, yaitu, localhost:8080/news, Anda akan melihat daftar item berita, yang masing-masing memiliki tautan untuk menampilkan hanya satu artikel.

## CodeIgniter4 Overview
### Models, Views, and Controllers
* What is MVC?
  MVC adalah singkatan dari Model-View-Controller, yang merupakan pola desain (design pattern) yang umum digunakan dalam pengembangan perangkat lunak, terutama dalam pengembangan aplikasi web. Pola ini membagi aplikasi menjadi tiga komponen utama: Model, View, dan Controller. Berikut adalah penjelasan singkat tentang masing-masing komponen:
  
  1. Models
     model adalah mempertahankan satu jenis data untuk aplikasi. Ini mungkin pengguna, posting blog, transaksi, dll. Dalam hal ini, pekerjaan model memiliki dua bagian: menegakkan aturan bisnis pada data saat ditarik dari, atau dimasukkan ke dalam, basis data; dan menangani penyimpanan aktual dan pengambilan data dari database.

    Model biasanya disimpan dalam app/Models, meskipun mereka dapat menggunakan namespace untuk dikelompokkan sesuai kebutuhan Anda.
  
  2. Views
     Tampilan adalah file yang paling sederhana dan biasanya HTML dengan jumlah PHP yang sangat kecil. PHP harus sangat sederhana, Biasanya hanya menampilkan isi variabel, atau mengulang beberapa item dan menampilkan informasinya dalam tabel.

    Views biasanya disimpan dalam app/Views,

  3. Controller
     mereka menerima masukan dari pengguna dan Kemudian tentukan apa yang harus dilakukan dengannya. Ini sering melibatkan meneruskan data ke model untuk menyimpannya, atau meminta data dari Model yang kemudian diteruskan ke tampilan yang akan ditampilkan.

      Controller biasanya disimpan dalam app/Controllers, meskipun mereka dapat menggunakan namespace untuk dikelompokkan Kamu butuh.

## General Topics 
### Helper Functions
What are Helpers?
Helper adalah istilah yang digunakan untuk menggambarkan kumpulan fungsi-fungsi bantuan yang dirancang untuk membantu dalam tugas-tugas tertentu dalam pengembangan aplikasi.
Pembantu biasanya disimpan di direktori system/Helpers atau app/Helpers anda.

Loading a Helper
Memuat file pembantu cukup sederhana menggunakan metode berikut:
``` shell
<?php

helper('name');
```
Kode di atas memuat file name_helper.php.

Misalnya, untuk memuat file Pembantu Cookie, yang diberi nama cookie_helper.php, Anda akan melakukan ini:
``` sheel
<?php

helper('cookie');
```

Loading Multiple Helpers
Jika Anda perlu memuat lebih dari satu helper sekaligus, Anda dapat lulus Array nama file di dan semuanya akan dimuat:
``` shell
<?php

helper(['cookie', 'date']);
```

Loading from Specified Namespace
Di dalam pengontrol kami, kami dapat Gunakan perintah berikut untuk memuat helper untuk kami:
``` shell
<?php

helper('Example\Blog\blog');
```
Anda juga dapat menggunakan cara berikut:
``` shell
<?php

helper('Example\Blog\Helpers\blog');
```
Using a Helper
Misalnya, untuk membuat tautan menggunakan fungsi di salah satu file tampilan Anda, Anda akan melakukan ini:
``` shell
<div>
<?= anchor('blog/comments', 'Click Here') ?>
</div>
```

Creating Custom Helpers
Misalnya, untuk membuat info helper, Anda akan membuat file bernama app/Helpers/info_helper.php, dan menambahkan fungsi ke file:
``` shell
?php

// app/Helpers/info_helper.php
use CodeIgniter\CodeIgniter;

/**
 * Returns CodeIgniter's version.
 */
function ci_version(): string
{
    return CodeIgniter::CI_VERSION;
}
```

“Extending” Helpers
Misalnya, untuk memperluas Array Helper asli, Anda akan membuat file bernama app/Helpers/array_helper.php, dan tambahkan atau ganti Fungsi:
``` shell
<?php

// any_in_array() is not in the Array Helper, so it defines a new function
function any_in_array($needle, $haystack)
{
    $needle = is_array($needle) ? $needle : [$needle];

    foreach ($needle as $item) {
        if (in_array($item, $haystack, true)) {
            return true;
        }
    }

    return false;
}

// random_element() is included in Array Helper, so it overrides the native function
function random_element($array)
{
    shuffle($array);

    return array_pop($array);
```

## Controllers
What is a Controller?

Constructor
``` shell
<?php

namespace App\Controllers;

use CodeIgniter\HTTP\RequestInterface;
use CodeIgniter\HTTP\ResponseInterface;
use Psr\Log\LoggerInterface;

class Product extends BaseController
{
    public function initController(
        RequestInterface $request,
        ResponseInterface $response,
        LoggerInterface $logger
    ) {
        parent::initController($request, $response, $logger);

        // Add your code here.
    }

    // ...
}
```

Helpers
``` shell
<?php

namespace App\Controllers;

class MyController extends BaseController
{
    protected $helpers = ['url', 'form'];
}
```

forceHTTPS
``` shell
<?php

if (! $this->request->isSecure()) {
    $this->forceHTTPS();
}
```

``` shell
<?php

if (! $this->request->isSecure()) {
    $this->forceHTTPS(31536000); // one year
}
```

Validating Data
``` shell
<?php

namespace App\Controllers;

class StoreController extends BaseController
{
    public function product(int $id)
    {
        $data = [
            'id'   => $id,
            'name' => $this->request->getPost('name'),
        ];

        $rule = [
            'id'   => 'integer',
            'name' => 'required|max_length[255]',
        ];

        if (! $this->validateData($data, $rule)) {
            return view('store/product', [
                'errors' => $this->validator->getErrors(),
            ]);
        }

        // ...
    }
}
```

``` shell
<?php

namespace App\Controllers;

class UserController extends BaseController
{
    public function updateUser(int $userID)
    {
        if (! $this->validate([
            'email' => "required|is_unique[users.email,id,{$userID}]",
            'name'  => 'required|alpha_numeric_spaces',
        ])) {
            // The validation failed.
            return view('users/update', [
                'errors' => $this->validator->getErrors(),
            ]);
        }

        // The validation was successful.

        // Get the validated data.
        $validData = $this->validator->getValidated();

        // ...
    }
}
```

``` shell
<?php

namespace App\Controllers;

class UserController extends BaseController
{
    public function updateUser(int $userID)
    {
        if (! $this->validate('userRules')) {
            // The validation failed.
            return view('users/update', [
                'errors' => $this->validator->getErrors(),
            ]);
        }

        // The validation was successful.

        // Get the validated data.
        $validData = $this->validator->getValidated();

        // ...
    }
}
```
Protecting Methods
``` shell
<?php

namespace App\Controllers;

class Helloworld extends BaseController
{
    protected function utility()
    {
        // some code
    }
}
```

Let’s try it: Hello World!
``` shell
<?php

namespace App\Controllers;

class Helloworld extends BaseController
{
    public function getIndex()
    {
        return 'Hello World!';
    }
}
```
Methods
Normal Methods
``` shell
<?php

namespace App\Controllers;

class Helloworld extends BaseController
{
    public function getIndex()
    {
        return 'Hello World!';
    }

    public function getComment()
    {
        return 'I am not flat!';
    }
}
```
Defining a Default Controller
``` shell
public string $defaultController = 'Helloworld';
```

``` shell
$routes->get('/', 'Home::index');
```
Default Method Fallback
``` shell
<?php

namespace App\Controllers;

class Product extends BaseController
{
    public function getIndex($id = null, $action = '')
    {
        // ...
    }
}
```
Fallback to Default Controller
``` shell
<?php

namespace App\Controllers\News;

use App\Controllers\BaseController;

class Home extends BaseController
{
    public function getIndex($id = null)
    {
        // ...
    }
}
```

Let’s try it: Hello World! (Legacy)
``` shell
<?php

namespace App\Controllers;

class Helloworld extends BaseController
{
    public function index()
    {
        return 'Hello World!';
    }
}
```


































