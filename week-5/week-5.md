## Rangkuman Week 5
* ### Web Server & RESTFul API
  * #### Web Server
    * Web server terdiri dari 2 komponen penting:
      * Hardware
        Di sisi hardware, web server adalah komputer yang menyimpan web server software dan file komponen website. (misalnya, dokumen HTML, gambar, CSS stylesheet, dan file JavaScript). Web server terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web.
      * Software
        Di sisi software, web server mencakup beberapa bagian yang mengontrol bagaimana pengguna web mengakses file yang dihosting. Minimal, ini adalah server HTTP. Server HTTP adalah perangkat lunak yang memahami URL (alamat web) dan HTTP (protokol yang digunakan browser untuk melihat halaman web). Server HTTP dapat diakses melalui nama domain situs web yang disimpannya, dan mengirimkan konten situs web yang dihosting ini ke perangkat pengguna akhir.
    * Server side programming atau pemrograman sisi server adalah suatu program yang berjalan di server yang menangani pembuatan konten halaman website. Contoh bahasa pemrograman untuk sisi server yaitu Node.js, PHP, Java, Python dan Ruby.
    * Website Statis (Static Website) adalah sebuah website yang kontennya statis / tidak berubah-ubah. Website tersebut tidak dapat diubah kecuali diubah secara manual melalui pengubahan bahasa pemograman website tersebut.
    * Dinamis (Dynamic Website) adalah jenis halaman web yang kontennya dapat berubah-ubah. Dengan kata lain, adanya program yang berjalan untuk mengatur perubahan data yang ditampilkan dalam website Dinamis tersebut.
  * #### REST
    REST adalah arsitektur software yang digunakan untuk pertukaran data antar aplikasi atau sistem. RESTful merupakan sebutan untuk web services yang menerapkan arsitektur REST. Bisa juga disebut sebagai API (application program interface) karena digunakan untuk menjembatani antara sistem yang berbeda (client dan server). 
    
    API atau Application Program Interface sendiri merupakan antarmuka yang menjadi perantara antara sistem aplikasi yang berbeda. Ada 5 method request HTTP yang sangat umum digunakan pada arsitektur REST ini, yaitu :
    1. GET : untuk mengakses data atau membaca data yang ada pada resource.
    2. PUT : untuk men-create atau membuat sebuah resource baru.
    3. DELETE : untuk menghapus resource.
    4. PATCH : untuk mengupdate kumpulan data (field) yang ada di dalam resource.
    5. POST : untuk memperbaharui sebuah resource, atau menambahnya.
* ### Node.js
  Node.js adalah runtime environment untuk JavaScript yang bersifat open-source dan cross-platform. Dengan Node.js kita dapat menjalankan kode JavaScript di mana pun, tidak hanya terbatas pada lingkungan browser.

  Node.js menjalankan V8 JavaScript engine (yang juga merupakan inti dari Google Chrome) di luar browser. Ini memungkinkan Node.js memiliki performa yang tinggi.

  Node.js juga menyediakan banyak library/module JavaScript yang membantu menyederhanakan pengembangan aplikasi web.

  **Cara Membuat Proyek Node.js**
  1. Buat folder baru
  2. Buka folder tersebut di VSCode
  3. Untuk membuat proyek JavaScript, klik Terminal pada VSCode. kemudian tuliskan perintah: **npm init**
  4. Setelah menuliskan perintah di atas, akan ada beberapa pertanyaan untuk mengisi *nilai package name, version, description*. Semua itu merupakan informasi dasar dari aplikasi yang akan dibuat.
  5. Setelah mengisi seluruh pertanyaan yang diberikan, akan diberitahu untuk melihat hasil akhir yang dibuat pada berkas package.json. Jika sudah sesuai, klik Enter.

  **Modul Built-in Nodejs**
  Beberapa contoh modul bawaan (built-in) pada nodejs:
  - **http** : untuk melakukan HTTP Request dan membuat server HTTP.
  - **fs** : untuk bekerja dengan file sistem.
  - **url** : untuk parsing string dari URL.
  - **event** : untuk membuat sebuah event dan menangkapnya.
  - **os** : menyediakan informasi tentang sistem operasi.
  Cara mengimpor modul build-in ke dalam aplikasi adalah menggunakan fungsi **require()**
  ```
  const http = require('http');
  ```

  **Modul dari NPM**
  Sebelum menggunakan modul dari NPM, harus menginstall terlebih dahulu modul tersebut menggunakan NPM. Contohnya: ```npm install moment ```

* ### Express.js
  Express.js adalah framework web app untuk Node.js yang ditulis dengan bahasa pemrograman JavaScript untuk membangun aplikasi dari sisi back end secara efektif dan optimal.

  **Menginstall Express.js**
  ```
  npm install express --save
  ```
  Agar mempermudah develop server side application, maka perlu menginstall beberapa modul seperti nodemon (agar dapat restart application otomatis selama proses development)
  ```
  npm install --save-dev nodemon
  ```
  Karena hanya digunakan saat development, maka disimpan di dev.

  **Syntax Dasar Express.js**
  ```
  const express = require ('express')
  const app = express()
  const port = 3000

  app.get('/', (req, res) => {
    res.send('Hello World!')
  })

  app.listen(port)
  ```

  **Routing**
  Routing mengacu pada bagaimana endpoint sebuah website/aplikasi (URIs) merespons permintaan client.

  Cara menentukan rute yaitu menggunakan metode Express yang sesuai dengan metode HTTP. Misal app.get(), app.post(), app.all(), dan juga ap.use().
  Beberapa contohnya yaitu :
  ```
  app.use(express.json())
  ```
  ```
  app.post('/users/:id', => (req, res) {
    res.send("Posting success")
  })  
  ```

  **Middleware**
  Middleware function adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle. Contoh middleware :
  ```
  const express = require ('express');
  const app = express();
  const port = 3000;

  const logger = (req, res, next) => {
  console.log("Hello, welcome");
  next();
  };

  app.use(logger);

  app.get('/', (req, res) => {
    res.send('Hello World!')
  });

  app.listen(port);
  ```

* ### Design Database With MySQL
  Sebelum membuat sebuah aplikasi backend yang sangat terikat dengan yang namanya database, alangkah baiknya kita membuat sebuah desain suatu database. Mendesain suatu database memudahkan kita untuk mengembangkan suatu aplikasi backend dengan adanya desain kita tidak kebingungan dalam menentukan relasi antar entitasnya, dan akan mengurangi terjadinya sebuah anomali data.

  **ERD** 
  Entity Relationship Diagram atau diagram hubungan entitas adalah sebuah diagram yang digunakan untuk perancangan suatu database dan menunjukan relasi atau hubungan antar objek atau entitas beserta atribut-atributnya secara detail.
  Komponen dalam ERD:
  1. Entitas
     Entitas merupakan sekumpulan objek yang dapat diidentifikasi secara unik dan berbeda satu dengan yang lainnya. Entitas ini biasanya digambarkan dengan lambang persegi panjang.
  2. Atribut
     Setiap entitas pasti memiliki atribut yang berfungsi untuk menjelaskan atau mendeskripsikan karakteristik dari entitas tersebut. Jenis-jenis atribut:
     - Atribut Kunci
     - Atribut simple
     - Atribut multinilai
     - Atribut gabungan
     - Atribut derivatif
  3. Relasi
     Relasi dalam ERD adalah hubungan yang terjadi antara satu atau lebih entitas. Jenis-jenis relasi:
      * One to one
        One to one berarti setiap entitas hanya dapat memiliki relasi dengan satu entitas lain. Contohnya seperti data mahasiswa dengan NIM (Nomor Induk Siswa).

      * One to many
        One to many adalah satu entitas dapat memiliki relasi dengan beberapa entitas, begitu pula sebaliknya. Contohnya adalah jurusan dengan mahasiswanya.

      * Many to many
        Many to many adalah setiap entitas yang ada dapat memiliki relasi dengan entitas lain, begitu pula sebaliknya. Contohnnya adalah mahasiswa dengan UKM (Unit Kegiatan Mahasiswa).

  **Normalisasi**
  Normalisasi adalah tahap dimana mengorganisaksikan sebuah data ke dalam tabel agar data tersebut tidak redundant, mudah dicari, dan tidak terjadi anomali.

  Ada 3 tahap atau tingkatan dalam melakukan normalisasi yaitu:
  - 1NF
    1. Tidak ada urutan dalam penyimpanan data
    2. harus menggunakan tipe data yang sama pada 1 kolom
    3. harus ada primary key
    4. tiap kolom harus berisi nilai tunggal
  - 2NF
    1. harus dalam bentuk 1NF
    2. tidak ada partial depedenct (atribut yang tidak ada hubungan dengan primary key akan dipisah)
  - 3NF
    1. harus dalam bentuk 3NF
    2. tidak ada transitif dependecy (setiap atribut harus bergantung pada primary key supaya tidak terjadi transiitif depedency)