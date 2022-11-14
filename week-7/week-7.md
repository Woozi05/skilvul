## Rangkuman Week 7
* ### Build Web Services and RESTful API with Express & Sequelize
  1. Pertama kita perlu melakukan inisialisasi di project kita terlebih dahulu agar dapat melakukan generate code
     ```
     npx sequelize-cli init
     ```
  2. Setting connection database
     ```
     const Sequelize = require("sequelize");

     const sequelize = new Sequelize("database", "username", "password" , {
        host: "localhost",
        dialect: "mysql"
     })
     ```
  3. Generate model. Misalnya membuat tabel user
     ```
     npx sequelize-cli model:generate --name user --attributes
     name:string,email:string,password:string
     ```
     Datanya akan menjadi sebuat class (OOP) dan dapat kita gunakan untuk membuat Rest API menggunakan express.
  4. Setelah itu kita bisa menjalankannya menggunakan :
     ```
     npx sequelize-cli db:migrate
     ```
     Jika ada yang salah, kita bisa mengembalikan (undo) menggunakan :
     ```
     npx sequelize-cli db:migrate:undo
     ```
   * Generate seed
     Seed adalah data awal atau data dummy yang bisa kita gunakan untuk mengisi data di database untuk keperluan awal project menggunakan sequelize.
     ```
     npx sequelize-cli seed:generate --name demo-user
     ```
     Ketika sudah berhasil melakukan generate maka kita dapat melakukan pengisian data seed didalam file seed generator. Terdapat 2 data yang diisi yaitu “up” untuk mengisi data di db, dan “down” untuk drop atau menghapus semua data seed di db.
     Menjalankan generate seed menggunakan sequelize :
     ```
     npx sequelize-cli db:seed:all 
     ```
     Jika ada yang salah, kita bisa mengembalikan (undo) menggunakan :
     ```
     npx sequelize-cli db:seed:undo
     ```
* ### MongoDB
  * MongoDB adalah sistem basis data berorentasi dokumen dan berjenis NoSQL yang dikembangkan dengan bahasa pemrograman C++.  Arti dari NoSQL yaitu kita bisa mengolah database dengan fleksibel dan tidak membutuhkan Query. Jika SQL menyimpan data menggunakan relasi tabel, MongoDB menggunakan dokumen dengan format JSON.
  * Database adalah wadah untuk menyimpan berbagai macam Collection. 
  * Collection adalah tempat kumpulan dari berbagai macam document, sehingga collection sering disamakan dengan tabel pada SQL. 
  * Document adalah unit terkecil yang berada pada MongoDB.
  **Connect NodeJS and MongoDB**
  Install dotenv untuk menampung variabel environment database dan juga install MongoDB
  ```
  npm install dotenv --save
  npm install mongodb --save
  ```
  Buat satu file .env untuk menyimpan variabel database
  ```
  // .env
  MONGODB_URL=mongodb://localhost27017
  mongodb_database=namaDatabase
  ```
  Untuk menambahkan Collection baru kita bisa gunakan
  ```
  db.createCollections(“movies”)
  ```
  Untuk menambahkan data pada Collection kita bisa gunakan
  ```
  db.movies.insert({
      judul: "Spiderman",
      genre: "sci-fi"
  })
  ```
  Untuk melihat data kita gunakan
  ```
  db.movies.find()
  ```
* ### Mongoose
* Mongoose adalah sebuah module pada NodeJS yang di install menggunakan npm, berfungsi sebagai penghubung antara NodeJS dan database nosql MongoDB.
  Untuk menggunakan mongoose kita bisa menginstallnya menggunakan :
  ```
  npm install mongoose
  ```
  Pastikan NodeJS dan MongoDB juga sudah terinstall.
  Membuat koneksi dengan menggunakan MongoDB database, yang diletakkan di .env
  ```
  const mongoose = require('mongoose');
  require('dotenv').config()

  const url = process.env.MONGOOSE_URL

  mongose.connect (url, {
    useNewUrlParser: true,
    useUnifiedTopology: true,
    useDindAndModify: false
  })
  ```
  masukkan url db ke file .enf
  ```
  MONGOOSE_URL=mongodb://localhost:27017/dbmongoose
  ```
  Kita membiasakan diri dengan menggunakan file .env untuk menyimpan URL atau data rahasia yang tidak perlu dilihat di public.
  **Membuat Skema di Mongoose**
  ```
  import mongoose from 'mongoose';
  const { Schema } = mongoose;

  const blogSchema = new Schema({
     title:  String,
     author: String,
     body:   String,
   }
  });
  ```
* ### Docker
  Docker adalah software yang menjalankan suatu aplikasi menggunakan container. Docker men-sharing kernel dari host OS, serta meng-container-kan suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja. Aplikasi yg berjalan di dalam container docker tidak terpengaruh oleh faktor luar karena terisolasi.
  **Cara Kerja Docker**
  Docker adalah sistem operasi untuk kontainer. Mirip dengan cara mesin virtual, perbedaannya VM memakan banyak resource dan waktu utk booting karena melakukan virtualisasi pada host hardware-nya. Sedangkan container kebalikannya dari vm, container melakukan virtualisasi pada host OS-nya. Docker diinstal di setiap server dan memberikan perintah sederhana yang dapat digunakan untuk membuat, memulai, atau menghentikan kontainer.
  **Perintah Dasar**
  * docker pull: Download image dari docker hub
  * docker images: Melihat kumpulan images yang sudah ter download
  * docker run: Menjalankan container
  * docker ps: Melihat container yang berjalan













