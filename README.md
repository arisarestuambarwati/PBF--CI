# ARISA RESTU AMBARWATI (220202030)

## Welcome to CodeIgniter4
CodeIgniter adalah alat yang mempercepat pembangunan situs web PHP. Dengan banyaknya perpustakaan yang tersedia bisa membangun proyek lebih cepat daripada harus menulis kode dari awal. Antarmuka sederhana dan struktur yang logis memudahkan akses perpustakaan tersebut. Dengan CodeIgniter, Anda bisa fokus pada kreativitas Anda dengan meminimalkan jumlah kode yang harus Anda tulis.

## Server Requirements
- PHP dan Ekstensi yang Diperlukan
- Ekstensi PHP Opsional
- Basis Data yang Didukung

### PHP dan Ekstensi yang Diperlukan
Diperlukan PHP versi 7.4 atau lebih baru, dengan ekstensi PHP berikut diaktifkan:
- internasional
- mbstring
- json

### Ekstensi PHP Opsional
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

### Basis Data yang Didukung
Basis data yang didukung saat ini adalah:
* MySQL melalui MySQLidriver (hanya versi 5.1 ke atas)
* PostgreSQL melalui Postgredriver (hanya versi 7.4 dan lebih tinggi)
* SQLite3 melalui SQLite3driver
* Microsoft SQL Server melalui SQLSRVdriver (hanya versi 2005 dan lebih tinggi)
* Oracle Database melalui OCI8driver (hanya versi 12.1 dan lebih tinggi)

Tidak semua driver telah dikonversi/ditulis ulang untuk CodeIgniter4. Daftar :
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
1. Pastikan Anda telah menginstal Composer. Jika belum, Anda dapat mengunduh dan menginstalnya dari https://getcomposer.org/.
2. Buka terminal atau command prompt.
3. Jalankan perintah Composer untuk membuat proyek CodeIgniter baru dengan code :
   ``` shell
   composer create-project codeigniter4/appstarter project-root
   ```
   Perintah di atas akan membuat folder root proyek .
5. Pindah direktori ke file yang telah dibuat sebelumnya
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
Baris perintah berikut di direktori utama:
``` shell
php spark serve
```
Server pengembangan lokal dapat disesuaikan dengan tiga opsi baris perintah:
* Opsi CLI untuk menentukan host yang berbeda untuk menjalankan aplikasi di:--host
  ``` shell
  php spark serve --host example.dev
  ```
* Secara default, server berjalan pada port 8080 tetapi Anda mungkin memiliki lebih dari satu situs yang berjalan, atau sudah memiliki aplikasi lain yang menggunakan port itu. Anda dapat menggunakan opsi CLI untuk menentukan yang berbeda
  ``` shell
  php spark serve --port 8081
  ```
* Opsi CLI, dengan nilainya atur ke jalur eksekusi PHP yang ingin Anda gunakan:
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
   Di sini, aturan kedua dalam objek cocok dengan permintaan GET ke jalur URI /pages, dan memetakan ke metode kelas.$routesindex()Pages
   Aturan ketiga dalam objek cocok dengan permintaan GET ke segmen URI menggunakan placeholder , dan meneruskan parameter ke metode kelas.$routes(:segment)view()Pages
   
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
Buat dua "tampilan" (template halaman) yang bertindak sebagai footer dan header halaman kami.

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

1. Untuk memuat halaman-halaman itu, Anda harus cek apakah halaman yang diminta benar-benar ada. Ketikkan kode : 

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
1. Buat database yang dapat digunakan, kemudian mengkonfigurasi CodeIgniter untuk menggunakannya
2. Sambungkan ke database Anda dan jalankan perintah SQL di bawah ini (MySQL):
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
Tambahkan mengikuti kode kedalam model anda

``` shell
public function getNews($slug = false)
    {
        if ($slug === false) {
            return $this->findAll();
        }

        return $this->where(['slug' => $slug])->first();
    }
```

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

### Complete News::index() Method
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
Tambahkan beberapa kode ke pengontrol dan buat tampilan baru. Kembali ke pengontrol dan perbarui metode menjadi :

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
Kemudian buat tampilan yang sesuai di app/Views/news/view.php. Masukkan kode berikut dalam file ini.

``` shell
<h2><?= esc($news['title']) ?></h2>
<p><?= esc($news['body']) ?></p>
```

Arahkan browser Anda ke halaman "berita" Anda, yaitu, localhost:8080/news, Anda akan melihat daftar item berita.

## CodeIgniter4 Overview
### Models, Views, and Controllers
#### What is MVC?
  MVC adalah singkatan dari Model-View-Controller, yang merupakan pola desain (design pattern) yang umum digunakan dalam pengembangan perangkat lunak, terutama dalam pengembangan aplikasi web. Pola ini membagi aplikasi menjadi tiga komponen utama: Model, View, dan Controller. Berikut adalah penjelasan singkat tentang masing-masing komponen:
  
  1. Models
     Komponen ini bertanggung jawab untuk mengelola logika bisnis dan data aplikasi.Model biasanya disimpan dalam app/Models.
  
  2. Views
     Komponen ini bertanggung jawab untuk menampilkan informasi kepada pengguna dan menanggapi input dari mereka. Views biasanya disimpan dalam app/Views,

  3. Controller
     Komponen ini bertanggung jawab untuk menerima input dari pengguna, memprosesnya, dan mengirimkan instruksi kepada model atau view. Controller biasanya disimpan dalam app/Controllers

## General Topics 
### Helper Functions
#### What are Helpers?
Helper adalah istilah yang digunakan untuk menggambarkan kumpulan fungsi-fungsi bantuan yang dirancang untuk membantu dalam tugas-tugas tertentu dalam pengembangan aplikasi.
Pembantu biasanya disimpan di direktori system/Helpers atau app/Helpers anda.

#### Loading a Helper
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

#### Loading Multiple Helpers
Jika Anda perlu memuat lebih dari satu helper sekaligus, Anda dapat lulus Array nama file di dan semuanya akan dimuat:
``` shell
<?php

helper(['cookie', 'date']);
```

#### Loading from Specified Namespace
Di dalam controller kami, kami dapat Gunakan perintah berikut untuk memuat helper untuk kami:
``` shell
<?php

helper('Example\Blog\blog');
```
Anda juga dapat menggunakan cara berikut:
``` shell
<?php

helper('Example\Blog\Helpers\blog');
```
#### Using a Helper
Misalnya, untuk membuat tautan menggunakan fungsi di salah satu file tampilan Anda, Anda akan melakukan ini:
``` shell
<div>
<?= anchor('blog/comments', 'Click Here') ?>
</div>
```

#### Creating Custom Helpers
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

#### “Extending” Helpers
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
### What is a Controller?
Komponen ini bertanggung jawab untuk menerima input dari pengguna, memprosesnya, dan mengirimkan instruksi kepada model atau view. 
### Constructor
Jika Anda ingin mengganti , jangan lupa untuk menambahkan metode:
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

### Helpers
Anda dapat menentukan array file pembantu sebagai properti kelas.  dapat menggunakan metode mereka di mana saja Di dalam pengontrol:

<?php
``` shell
<?php

namespace App\Controllers;

class MyController extends BaseController
{
    protected $helpers = ['url', 'form'];
}
```

### forceHTTPS
Metode kenyamanan untuk memaksa metode diakses melalui HTTPS tersedia dalam semua Controller:
``` shell
<?php

if (! $this->request->isSecure()) {
    $this->forceHTTPS();
}
```

#### Validating Data
Untuk mempermudah pengecekan data, controller juga menyediakan metode kenyamanan.
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

Anda dapat mengganti array dengan nama grup seperti yang didefinisikan dalam app/Config/Validation.php:
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

## Methods
### Normal Methods
Tambahkan metode baru ke pengontrol Anda:
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
### Defining a Default Controller
Untuk menentukan pengontrol default, buka file app/Config/Routing.php Anda dan atur properti ini:
``` shell
public string $defaultController = 'Helloworld';
```

Dan komentari baris di app/Config/Routes.php:
``` shell
$routes->get('/', 'Home::index');
```
### Default Method Fallback
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

## Views
Tampilan hanyalah halaman web, atau fragmen halaman, seperti header, footer, sidebar, dll. 

### Creating a View
Menggunakan editor teks Anda, buat file bernama blog_view.php dan masukkan ini ke dalamnya:
``` shell
<html>
    <head>
        <title>My Blog</title>
    </head>
    <body>
        <h1>Welcome to my Blog!</h1>
    </body>
</html>
```
Kemudian simpan file di direktori app/Views Anda.

#### Displaying a View
Untuk memuat dan menampilkan file tampilan tertentu, Anda akan menggunakan kode berikut di pengontrol Anda:
``` shell
return view('name');
```
Sekarang, buat file bernama Blog.php di direktori app/Controllers, dan taruh ini di dalamnya:
``` shell
<?php

namespace App\Controllers;

class Blog extends BaseController
{
    public function index()
    {
        return view('blog_view');
    }
}
```
Buka file perutean yang terletak di app/Config/Routes.php, dan cari "Route Definitions". Tambahkan kode berikut:
``` shell
use App\Controllers\Blog;

$routes->get('blog', [Blog::class, 'index']);
```
### Loading Multiple Views
Misalnya, Anda mungkin ingin memiliki tampilan header, tampilan menu, a tampilan konten, dan tampilan footer. Itu mungkin terlihat seperti ini:
``` shell
<?php

namespace App\Controllers;

use CodeIgniter\Controller;

class Page extends Controller
{
    public function index()
    {
        $data = [
            'page_title' => 'Your title',
        ];

        return view('header')
            . view('menu')
            . view('content', $data)
            . view('footer');
    }
}
```

### Namespaced Views
Setelah ini misalnya, Anda dapat memuat file blog_view.php dari example/blog/Views dengan menambahkan namespace ke view name:
``` shell
<?php

return view('Example\Blog\Views\blog_view');
```

### Adding Dynamic Data to the View
Data dilewatkan dari controller ke view melalui array di parameter kedua fungsi. Berikut contohnya:
``` shell
$data = [
    'title'   => 'My title',
    'heading' => 'My Heading',
    'message' => 'My Message',
];

return view('blog_view', $data);
```
``` shell
<?php

namespace App\Controllers;

class Blog extends BaseController
{
    public function index()
    {
        $data['title']   = 'My Real Title';
        $data['heading'] = 'My Real Heading';

        return view('blog_view', $data);
    }
}
```
Mari kita coba dengan file controller Anda. Buka dan tambahkan kode ini:
``` shell
<html>
    <head>
        <title><?= esc($title) ?></title>
    </head>
    <body>
        <h1><?= esc($heading) ?></h1>
    </body>
</html>
```
### The saveData Option
``` shell
$data = [
    'title'   => 'My title',
    'heading' => 'My Heading',
    'message' => 'My Message',
];

return view('blog_view', $data, ['saveData' => false]);
```
Anda dapat mengatur ke di app/Config/Views.php
### Creating Loops
Berikut contoh sederhananya. Tambahkan ini ke pengontrol Anda:
``` shell
<?php

namespace App\Controllers;

class Blog extends BaseController
{
    public function index()
    {
        $data = [
            'todo_list' => ['Clean House', 'Call Mom', 'Run Errands'],
            'title'     => 'My Real Title',
            'heading'   => 'My Real Heading',
        ];

        return view('blog_view', $data);
    }
}
```
``` shell
<html>
<head>
    <title><?= esc($title) ?></title>
</head>
<body>
    <h1><?= esc($heading) ?></h1>

    <h2>My Todo List</h2>

    <ul>
    <?php foreach ($todo_list as $item): ?>

        <li><?= esc($item) ?></li>

    <?php endforeach ?>
    </ul>

</body>
</html>
```
















































