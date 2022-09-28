# Rangkuman Week 1
## Unix Command Line
- ### Shell
    Shell adalah program yang menghubungkan user dengan sistem operasi. Shell akan menerima perintah, kemudian meneruskan perintah tersebut ke system untuk dieksekusi.
      Shell ada 2 macam, yaitu:
    * Shell berbasis grafis -> GUI (Graphical User Interface)
    * Shell berbasis teks -> CLI (Command Line Interface)
- ### File System Structure
  File System Structure yaitu sebuah filesystem yang mengatur bagaimana data disimpan di dalam sebuah system. Contoh dalam Sistem Operasi Windows struktur file yang disimpan menggunakan struktur yang bentuknya mirip sebuah pohon seperti gambar dibawah
  ![filesystem windows](https://github.com/Woozi05/skilvul/blob/8dac168f9f49839936349966e720aad2df78ab46/week-1/gambar/filesystem%20windows.png)
- ### CLI (Command Line Interface)
  Command Line Interface (CLI) adalah antarmuka pengguna berbasis teks yang digunakan untuk menjalankan program, mengelola file komputer, dan berinteraksi dengan komputer. CLI menerima perintah (command) yang dimasukkan oleh keyboard; perintah yang dipanggil pada prompt perintah kemudian dijalankan oleh komputer.
  Aplikasi yang digunakan untuk mengakses CLI adalah Terminal Emulator. Contoh CLI yaitu sh, bash, zsh dan cmd.exe
- #### Command
  - **pwd** (print working directory), untuk melihat current working directory
  - **ls** (lists), melihat isi sebuah directory 
  - **cd** (change directory), untuk berpindah directory
  - **head**, **tail**, dan **cat** untuk melihat isi files di awal, akhir, dan keseluruhan.
  - **touch**, untuk membuat sebuah file
  - **mkdir** (make directory), untuk membuat directory
  - **cp** (copy), untuk menyalin file atau directory
  - **mv** (move), untuk memindahkan atau me-rename file dan direktori 
  - **rm** untuk menghapus file, **rm -d** untuk menghapus directory

## Git & GitHub Dasar
- ### Apa itu Git dan GitHub?
  * Git adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file.
  * GitHub adalah layanan cloud yang berguna untuk menyimpan dan mengelola sebuah project yang dinamakan repository (repo git).
**Perbedaannya**:
Git adalah alat yang digunakan untuk membuat hidup programmer lebih mudah, sementara GitHub adalah tempat atau layanan yang digunakan untuk meng-host proyek Git.
- ### Mengapa Git dan GitHub Wajib Digunakan?
  Karena dengan Git dan GitHub kita bisa berkolaborasi mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate.
  Kita juga tidak perlu menunggu rekan dalam satu tim menyelesaikan suatu program dahulu untuk berkolaborasi. Kita bisa membuat file didalam projek yang sama atau membuat code di file yang sama dan menyatukannya saat sudah selesai.
- ### Alur Kerja Git dan GitHub
  * Setup Awal
    ``` 
    git config --global user.name "Uzi Fauziah"
    git config --global user.email "uzifauziah34@gmail.com"
    ```
   * Membuat Repository
     ```
     git init proyek01
     ```
     Jika folder sudah ada sebelumnya gunakan ini:
     ```
     git init .
     ```
   * Git Status
     **git status**, digunakan untuk mengetahui sebuah status dari sebuah repository lokal.
   * Git Add
     **git add .**, adalah perintah yang digunakan untuk menambahkan file baru di repository yang dipilih.
   * Git Commit
     **git commit -m "Tambahkan pesan"**, digunakan untuk menyimpan perubahan yang sudah dilakukan, namun tidak ada perubahan yang terjadi pada remote repository.
   * Git Remote
     **git remote**, digunakan untuk membuat user terhubung ke remote repository.
   * Git Push
     **git push**, digunakan dalam mengirimkan perubahan file yang dilakukan setelah di commit ke remote repository.
   * Git Clone
     **git clone**, perintah yang digunakan untuk membuat salinan repository lokal.
## HTML
   * HTML adalah singkatan dari Hypertext Markup Language yang digunakan untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet.
   * Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML yaitu browser (contohnya google chrome) dan code editor (contohnya visual studio code)
   * HTML Structure
     ```
     <!DOCTYPE html>
     <html lang="en">
     <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>My Blog</title>
        <link href="coba.css" type="text/css" rel="stylesheet"/>
     </head>
     <body>
        Hello, This is My Website
     </body>
     </html>
     ```
   * HTML Anatomy
     ```<p>Hello World!</p>```disebut element 
     ```<p>``` disebut opening tag
     ```</p>``` disebut closing tag
     Tulisan "Hello World!" disebut content
   * HTML Attributes
     Attribute adalah properties dari sebuah HTML Element. Semua HTML Element memiliki attribute. Contohnya id, class, scr, href, dan lain-lain.
   * HTML Tag
     * Single Tag
       ```<br/>``` untuk memasukkan satu baris putus
       ```<img src=" " alt=" " />``` untuk menampilkan gambar
     * Double Tag
       ```<p></p>``` untuk membuat paragraf
       ```<h1></h1>``` untuk membuat heading
       ```<ol></ol>``` untuk membuat list berurutan
       ```<ul></ul>``` untuk membuat list tidak berurutan
       ```<li></li>```untuk membuat sebuah item daftar
       ```<div></div>``` untuk mengelompokkan elemen atau bermacam-macam tag agar menjadi suatu grup.
       ```<video></video>``` untuk menampilkan video
       ```<table></table>``` untuk membuat tabel
   * Semantic HTML
     Menggunakan elemen HTML sesuai dengan kebutuhan konten. Contohnya yaitu header,  nav, section, main, footer, dll.
     ```
     <body>

     <header>
       <h1>My Website</h1>
     </header>

     <nav>
       <a href="#">Home</a> |
       <a href="#">About</a> |
       <a href="#">Contact</a>
     </nav>

     <article>
        <h1>Welcome To My Website!</h1>
     <p>Hello, My name is Uzi Fauziah Azhari</p>
     </article>

     <footer>
       Copyright; 2022 by woozi05
     </footer>

     </body>
   * Deploy HTML
     Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang. Untuk melakukan hal tersebut kita bisa menggunakan layanan yang bernama Netlify.
## CSS
* CSS adalah bahasa yang digunakan untuk mendesain halaman website. Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.
* Ada 3 cara menyisipkan CSS ke dalam HTML:
  Inline Tag : menggunakan CSS langsung di atribute elemnt html
  ```<p style="color: blue;">Hello</p>```
  Internal Tag : menggunakan tag ```<style></style>``` di bagian head
  External Tag : menggunakan file CSS terpisah dengan HTML
* CSS Syntax adalah syntax yang digunakan untuk menunjuk atau memilih HTML element mana yang ingin diberi style (dihias). CSS syntax terdiri dari selector, property, dan value.
Syntaxnya seperti ini:
  ```
  selector {
     property: value;
  }
  ```
  Misalnya kita memiliki element paragraf ```<p>``` yang ingin diubah menjadi warna biru
  ```
  <!-- Pada file HTML -->
   <p>Hello World!</p>
  ```
  ```
  <!-- Pada file CSS -->
  p {
     color: blue;
  }
  ```
* Flexbox adalah cara untuk mengatur layout. Flexbox memiliki kemampuan untuk menyesuaikan layout secara otomatis. Macam-macam property flex:
  * Properti **flex-direction** digunakan untuk mengatur letak item child. Ada 4 value flex-direction:
    * row (default): secara default letak item child membentuk sebuah baris dari kiri ke kanan.
    * row-reverse: letak item child membentuk sebuah baris dari kanan ke kiri
    * column: letak item child membentuk sebuah baris dari atas ke bawah
    * column-reverse: letak item child membentuk sebuah baris dari bawah ke atas
  * Defaultnya, item pada flex akan mencoba masuk atau fit ke dalam satu baris atau row. Kita bisa membuat item yang berlebihan untuk lanjut ke baris atau kolom berikutnya menggunakan property **flex-wrap**. Property ini memiliki 3 value:
    * Nowrap (default): semua item akan berada di satu baris
    * Wrap: item flex akan pindah ke baris selanjutnya apabila tidak muat, dari atas ke bawah
    * Wrap-reverse: sama seperti wrap, tetapi arah nya dari bawah ke atas.
  * Properti **flex-flow** digunakan sebagai shortcut untuk set up flex-direction dan flex-wrap bersamaan. Ada 4 value pada flex-flow:
    * row nowrap
    * column wrap
    * column reverse
    * row-reverse wrap-reverse
  * Properti **justify-content** digunakan untuk mengatur tata letak dan space antar item child secara horizontal atau main axis. Justify-content memiliki beberapa value yaitu:
    * Flex- start: posisi item akan dikemas pada bagian awal “flex-direction”
    * Flex-end: posisi item akan dikemas pada bagian akhir “flex-direction”
    * Center: posisi item akan dikemas ke bagian tengah baris
    * Space-between: letak item akan didistribusikan secara merata, item pertama ada pada bagian start dan item terakhir pada bagian end.
    * Space-around: letak item akan didistribusikan secara merata dengan space/ruang yang ada diantara item.

