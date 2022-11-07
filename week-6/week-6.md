## Rangkuman Week 6
* ### Database MySQL Basic
  * Database merupakan sekumpulan tabel yang berisikan informasi untuk diolah yang kemudian data tersebut bisa digunakan di dalam sebuah sistem.
  * Untuk membuat Database diperlukan sebuah software yang dinamakan dengan DBMS (Database Management System).
  * DBMS adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada dalam media penyimpanan.
  * MySQL adalah sebuah sistem manajemen database yang berguna untuk mengelola database di dalam website.
  Macam-macam istilah yang ada pada database:
  1. Tabel
     Table adalah kumpulan value yang dibangun oleh baris dan kolom, yang didalamnya berisikan atribut dari sebuah data.
  2. Field
     Field adalah kolom dari sebuah tabel dimana masing-masing field memiliki tipe data masing-masing.
  3. Record
     Record merupakan kumpulan nilai yang saling terkait. Record merupakan isi dari sebuah tabel.
  4. SQL
     SQL atau Structured Query Language merupakan suatu bahasa (Language) yang digunakan untuk melakukan interaksi di RDMS (Relational Database Management System). RDMS merupakan sistem yang mendukung adanya hubungan atau relationship antar tabel pada suatu database.
     - Membuat, Menampilkan dan menghapus data didalam database.
     - Mengatur “Permission” (siapa saja yang bisa mengakses data).
     - Membuat dan menghapus Database.

  * DDL (Data Definition Language) merupakan kumpulan perintah SQL yang digunakan untuk membuat, mengubah dan menghapus struktur dan definisi metadata dari objek-objek Database.
    Macam-macam perintah DDL:
    1. Create Database: Membuat database baru
       Contohnya:
       ```
       CREATE DATABASE nama_database;
       ```
    2. Create Table: Membuat tabel pada database
       Contohnya:
       ```
       CREATE TABLE table_mahasiswa (
       column1 datatype,
       column2 datatype,
       column3 datatype,
       ....
       );
       ```
    3. Rename Table: Digunakan untuk mengganti nama tabel
       Contohnya:
       ```
       RENAME TABLE peserta_didik to mahasiswa;
       ```
    4. Alter Table:	Mengubah struktur tabel
       Contohnya:
       ```
       ALTER TABLE mahasiswa ADD tgl_lahir DATE;
       ```
       Perintah tersebut digunakan untuk menambahkan kolom tanggal lahir pada tabel mahasiswa.
    5. Drop Database: Menghapus database
       Contohnya:
       ```
       DROP DATABASE kampus;
       ```
    6. Drop Table: Menghapus tabel  pada database
       Contohnya:
       ```
       DROP TABLE data_mahasiswa;
       ```
  * DML (Data Manipulation Language) adalah perintah SQL untuk memanipulasi data dalam database.
    macam-macam perintah DML:
    1. Select : Menampilkan record pada sebuah tabel
       Contohnya:
       ```
       SELECT * FROM mahasiswa;
       ```
    2. Insert : Menambahkan record baru pada tabel
       ```
       INSERT INTO mahasiswa (nim, nama) values (“105200”, “Uzi”);
       ```
    3. Update : Mengubah data
       ```
       UPDATE mahasiswa SET nama=”Uzi” WHERE nim=”105200”;
       ```
    4. Delete : Menghapus data
       ```
       DELETE FROM mahasiswa WHERE nim =”105200”;
       ```
   * Tipe data SQL:
     1. String: tipe data berupa kumpulan karakter termasuk karakter simbol. Contohnya char, varchar, text, enum, dan lain-lain.
     2. Number: data yang berisi kumpulan karakter angka. Contohnya int, float, decimal
     3. Boolean: Tipe ini hanya menyimpan 2 tipe data yaitu TRUE dan FALSE, dan dapat di convert menjadi int dengan representasi TRUE = 1, dan FALSE = 0
     4. Date time: tipe data untuk menyimpan tanggal dan waktu. Contohnya date, datetime, time, timestamp
     5. tipe data lain yaitu DEFAULT untuk set default value jika tidak di assign dengan value dan NULL yaitu tipe data kosong atau tipe data yang belum di assign dengan value / data.
   * Primary Key atau Kunci Primer digunakan sebagai identifikasi untuk membedakan satu baris dengan baris lainnya dalam suatu tabel.
   * Foreign Key atau Kunci Asing adalah sebuah atribut atau gabungan atribut yang terdapat dalam suatu tabel yang digunakan untuk menciptakan hubungan (relasi) antara dua tabel.

* ### Database MySQL Lanjutan
  * JOIN merupakan perintah di MySQL untuk menggabungkan 2 table atau lebih berdasarkan kolom yang sama
    JOIN di MySQL dibagi menjadi 3 cara:
    1. INNER JOIN: membandingkan record di setiap table untuk dicek apakah nilai sama atau tidak. Jika nilai kedua table sama maka akan terbentuk table baru yang hanya menampilkan record yang sama dari kedua table.
       Cara penulisannya:
       ```
       SELECT *
       FROM table1
       INNER JOIN table2
       ON table1.field = table2.field;
       ```
    2. LEFT JOIN: menghasilkan nilai berdasarkan table kiri (table1) dan nilai yang sama di table kanan (table2). Jika table kanan tidak nilainya ada maka akan diisi nilai NUL.
       Cara penulisannya:
       SELECT *
       FROM table1
       LEFT JOIN table2
       ON table1.field = table2.field;
    3. RIGHT JOIN: hampir sama seperti LEFT JOIN hanya yang menjadi master adalah table kanan (table 2). Jika table kiri tidak nilainya ada maka akan diisi nilai NULL.
       Cara penulisannya:
       ```
       SELECT *
       FROM table1
       RIGHT JOIN table2
       ON table1.field = table2.field;
       ```
  * Dalam SQL terdapat aggregate functions atau fungsi agregat. Fungsi agregat adalah fungsi yang menerima koleksi nilai dan mengembalikan nilai tunggal sebagai hasilnya.
    Macam-macam fungsi agregat:
    1. COUNT: untuk menghitung jumlah record.
       Contoh:
       menghitung jumlah record pada tabel buku
       ```
       SELECT COUNT(*)
       FROM buku;
       ```
    2. SUM: untuk menghitung total nilai dari kolom tertentu.
       Contoh:
       Menghitung total harga
       ```
       SELECT SUM(harga) AS total_harga 
       FROM buku;
       ```
    3. AVG: untuk menampikan nilai rata-rata dari suatu kolom
       Contoh:
       Menampilkan rata-rata harga
       ```
       SELECT AVG(harga) AS harga_rerata
       FROM buku;
       ```
    4. MAX: untuk menampikan nilai tertinggi dari suatu kolom
       Contoh:
       Menampilkan harga tertinggi
       ```
       SELECT MAX(harga) AS harga_tertingi
       FROM buku;
       ```
    5. MIN: untuk menampikan nilai terendah dari suatu kolom
       Contoh:
       Menampilkan harga terendah
       ```
       SELECT MIN(harga) AS harga_terendah
       FROM buku;
       ```
  * GROUP BY
    Mengelompokkan baris yang memiliki nilai yang sama ke dalam baris ringkasan. Sering digunakan dengan fungsi agregat untuk mengelompokkan kumpulan hasil dengan satu atau lebih kolom.
    Cara penulisannya:
    ```
    SELECT nama_kolom
    FROM nama_tabel
    WHERE kondisi
    GROUP BY nama_kolom;
    ```
  * HAVING
    HAVING ditambahkan ke SQL karena kata kunci WHERE tidak dapat digunakan dengan aggregate functions.
    Cara penulisannya:
    ```
    SELECT nama_kolom
    FROM nama_tabel
    WHERE kondisi
    GROUP BY nama_kolom
    HAVING kondisi
    ORDER BY nama_kolom;
    ```
  * LIKE
    Operator LIKEyang digunakan dalam klausa WHERE untuk mencari pola yang ditentukan pada kolom / field.
    Ada dua wildcard yang sering digunakan bersama dengan operator LIKE:
    * Tanda persen (%) mewakili nol, satu, atau beberapa karakter
    * Tanda garis bawah (_) mewakili satu karakter tunggal
    Cara penulisannya:
    ```
    SELECT column1, column2, ...
    FROM table_name
    WHERE columnN LIKE pattern;
    ```
    Salah satu contoh penggunaannya:
    ```
    SELECT nama
    FROM mahasiswa
    WHERE nama LIKE 'a%';
    ```
    Mencari nilai apapun pada field nama yang dimulai dengan huruf "a"
* ### Authentication and Authorization
  * Authentication
    Authentication atau Autentikasi adalah satu metode untuk melakukan konfirmasi pengguna atau user pada suatu layanan, aplikasi, sistem pembayaran, atau sistem penyimpanan, bahwa pengguna tersebut adalah orang yang sah dan memiliki hak akses atas informasi tertentu.
    Authentication ada dua faktor, yaitu:
    1. Single-Factor Authentication yaitu autentikasi yang hanya mengandalkan pada satu jenis faktor pengamanan saja. Dalam konteks username dan password, satu faktor tersebut adalah kepingan informasi rahasia yang juga dikenal dengan istilah Something You Know.
    2. Multi-Factor Authentication, biasanya dalam bentuk sesuatu benda khusus yang hanya dimiliki si pemilik akun saja, misal sebuah smartphone atau kartu khusus, biasa juga disebut dengan faktor Something You Have. Salah satu opsi lain untuk faktor ini adalah penggunaan biometrik seperti sidik jari (fingerprint) atau bola mata (iris atau retina) yang juga dikenal dengan faktor Something You Are.
    Cara autentikasi:
    Jika sudah install express, buat folder rotes kemudian buat file auth.js di dalamnya. Jika sudah masukkan kode seperti di bawah ini
    ```
    const express = require("express");
    const router = express.Router();
    const jwt = require("jsonwebtoken"); //install terlebih dahulu jsonwebtoken pada terminal

    const users = [
      { id: 1, email: "zi05@gmail.com", password: "123" },
    ];

    const KEY = "jbasjbfajbl"; //buat key untuk token (bebas)

    // http://localhost:3000/auth/login
    router.post("/login", (req, res) => {
      const { email, password } = req.body;

      const userData = users.find(
        (item) => email === item.email && password === item.password
      );

      const token = jwt.sign(
        {
          id: userData.id,
        },
        KEY
      );

      if (userData) {                                  
        res.json({
          message: "success login",
          token,
        });
      } else {
        res.status(401).json({
          message: "email or password are incorrect",
        });
      }
    });

    module.exports = router;
    ```
    Kemudian jalankan pada terminal **npm run dev**. Lalu pada thunder client masukkan endpoint ```http://localhost:3000/auth/``` dengan method POST. Setelah itu masukkan username dan password pada body json. Kita akan mendapatkan sebuah token acak, lalu masukkan token di kolom auth -> bearer -> dan isikan pada kotak bearer token. Jika sesuai maka kita akan mendapatkan respon status 200 dan id berhasil didapatkan.

  * Authorization adalah proses menentukan hak akses yang akan menentukan layanan apa saja yang kita terima setelah identitas kita terverifikasi, contohnya adalah ketika kita mengakses sosmed dan sudah melewati tahap autentifikasi maka kita akan masuk ke sistem dan dapat mengkases akun kita, selanjutnya sistem akan melakukan proses autorisasi hak akses apa saja yang kita peroleh.
* ### Sequelize
  * Sequelize adalah ORM (Object Relational Mapping) Node JS yang berbasis promise. Sequelize mendukung sebagian besar relational Database seperti MySQL, PostgresQL, MariaDB, SQLite dan Miscrosoft SQL Server. Dengan fitur fitur di Sequelize, kita bisa mengelola dan mengatur data di database kita dengan cepat, dan efisien.
  * ORM adalah suatu metode/teknik pemrograman yang digunakan untuk mengkonversi data dari lingkungan bahasa pemrograman berorientasi objek (OOP) dengan lingkungan database relational.
  ```
  // install sequelize cli globally
  npm i -g sequelize-cli

  // install in local project
  npm install sequelize

  // install driver vendor database
  npm i mysql2

  // init sequelize in local project
  npx sequelize-cli init

  //create model
  npx sequelize-cli model:generate --name User --attributes email:string,password:string

  //migrate
  npx sequelize-cli db:migrate
  ```






   
 
