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
       <a href="#">Home</a>
       <a href="#">About</a>
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
     ```
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
## Algorithm
* Algoritma adalah sederetan langkah-langkah logis yang disusun secara sistematis untuk memecahkan suatu masalah. Disebut Logis karena setiap langkah bisa diketahui dengan pasti. Algoritma lebih merupakan alur pemikiran untuk menyelesaikan suatu pekerjaan atau suatu masalah.
* Struktur data adalah cara penyimpanan, pengorganisasian , dan pengaturan data di dalam media penyimpanan komputer sehingga data tersebut dapat digunakan secara efisien.
* Manfaat Algoritma dan Struktur Data:
  * Membantu menyelesaikan suatu masalah dengan logika dan juga sistematis.
  * Mempermudah pembuatan program yang dapat menyelesaikan masalah tertentu.
  * Indeks pada struktur data mempercepat proses pencarian data tertentu.
  * Struktur data bisa berpengaruh ke tingkat efektifitas algoritma.
* Contoh Algoritma sederhana
  Algoritma menghitung luas persegi panjang
  Analisis :
  Input : p (panjang) dan l (lebar)
  Luas Persegi Panjang  L = p*l
  Algoritma :
  Inputkan panjang
  Inputkan lebar
  Rumus untuk menghitung L  yaitu L= p*l
  Nilai  L (Luas ) akan dicetak sebagai output ke perangkat output (keluaran)
* Menerapkan algoritma dengan JavaScript
  ````
  let panjang = 10
  let lebar = 5
  let luas = panjang*lebar
  console.log(luas)

  //outputnya 50
  ````
## JavaScript Dasar - Intro JavaScript
* Javascript adalah bahasa pemograman yang digunakan untuk logic pada sebuah website. Javascript juga dapat membuat website menjadi interaktif dan dinamis.
* Javascript dijalankan melalui browser pada device setiap user.
* Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming. Ada 6 tipe data fundamental pada Javascript:
  * number
    Tipe data number adalah tipe data yang mengandung semua angka termasuk angka desimal. Contoh: 2, 4, 1200, 23.42
  * string
    Tipe data string adalah grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya. Harus diawali dan diakhiri dengan single quotes ‘ … ‘ ataupun double quotes “ … “.
  * boolean
    Tipe data boolean adalah tipe data yang hanya mempunyai 2 buah nilai. 2 buah nilai tersebut adalah TRUE (benar) or FALSE (salah).
  * null
    Tipe data null adalah tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai.
  * undefined
    Tipe data undefined adalah tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. Undefined berbeda dengan null. Undefined didapat dari hasil berikut:
     * Nilai dari pemanggilan variabel yang belum didefinisikan
     * Nilai dari pemanggilan element array yang tidak ada
     * Nilai dari pemanggilan property objek yang tidak ada
     * Nilai dari pemanggilan fungsi yang tidak mengembalikan nilai (return)
     * Nilai dari parameter fungsi yang tidak memiliki argumen
  * object
    Tipe data object adalah koleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya). Tipe data object mempunyai key dan value.
* Operator pada JavaScript
  * Assignment Operator (=)
    Assignment operator digunakan untuk menyimpan sebuah nilai pada variabel.
    ```
    let nama = "Uzi"
    ```
  * Mathematical Assignment Operator
    ```
    let a = 5
    a += 1   // sama dengan a = a + 1
    console.log(a)
    //output 6
    ```
    * Selain itu ada juga -=, *= dan /=
  * Increment dan Decrement
    Gunakan increment atau decrement untuk menambah atau mengurangi sebesar 1 nilai.
    ```
    let a = 3
    a++   
    console.log(a)
    //output 4
    ```
    ```
    let a = 3
    a--   
    console.log(a)
    //output 2
    ```
  * Arithmetic Operator
    * Arithmetic operator adalah operator yang melibatkan operasi matematika.
    * Tambah (+)
    * Kurang (-)
    * Perkalian (*)
    * Pembagian (/)
    * Modulus (%)
  * Comparison Operator
    Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara true or false. Simbol comparison operator:
    * Lebih kecil dari : <
    * Lebih besar dari: >
    * Lebih kecil atau sama dengan: <=
    * Lebih besar atau sama dengan: >=
    * Sama dengan: ===
    * Tidak sama dengan: !==
  * Logical Operator
    Logical operator biasa digunakan untuk sebuah CONDITIONAL pada pemograman. Menghasilkan nilai BOOLEAN yaitu TRUE or FALSE. Simbol dari Logical Operator adalah sebagai berikut:
    AND operator : &&
    OR operator: ||
    NOT operator: !
- ### JavaScript - Conditional
  Conditional merupakan statement percabangan yang menggambarkan suatu kondisi. Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut. Yang dicek adalah apakah kondisi tersebut TRUE (benar). Jika TRUE maka code didalam kondisi tersebut dijalankan. Contoh Conditional:
  * If Statement
    ```
    if (true){
        console.log("Pesan ini akan tampil")
    }
    //output "Pesan ini akan tampil"
    ```
  * IF … ELSE Statement
    ```
    let haus = false
    if (haus){
        console.log("ambil minum")
    }else {
        console.log("tidak ambil minum")
    }
    //output "tidak ambil minum"
    ```
   * IF .. ELSE IF Statement
     ```
     let lampuLaluLintas = "kuning"
     if (lampuLaluLintas === "merah"){
         console.log("berhenti")
     }else if (lampuLaluLintas === "kuning"){
         console.log("hati-hati")
     }else if (lampuLaluLintas === "hijau"){
         console.log("maju")
      }else {
         console.log("lampu rusak")
     }
     //output "hati-hati"
     ```
   * Truthy and Falsy
     Truthy and falsy digunakan untuk mengecek apakah variabel telah terisi namun tidak mementingkan nilainya.
     ```
     let a = "kucing"
     if (a){
        console.log(a)
     }else {
        console.log("Variabel tidak ada")
     }
     //output "kucing"
     ```
   * Switch Case Conditional
     Gunakan switch case jika kondisi dan percabangan terlalu banyak.
     ```
     var warna = "merah";
     switch (warna){
	 case "hitam":
		teks = "warna hitam";
		break;
	 case "merah":
		teks = "Warna merah";
		break;
	 case "hijau":
		teks = "Warna hijau";
		break;
	 default:
	    teks = "Warna tidak terdeteksi";
     }
     //output "Warna merah"
     ```
   * Ternary Operator
     Ternary operator merupakan short-syntax dari statement if … else.
     ```
     let isNowSale = true
     isNowSale ? console.log("lets shopping now") : console.log("shopping later")
     ```
- ### JavaScript - Looping
  Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.
  * FOR LOOP
    FOR LOOP merupakan instruksi pengulangan yang dapat kita berikan pada program yang kita kembangkan. Gunakan FOR LOOP jika kita tahu seberapa banyak nilai pasti untuk pengulangannya
    ```
    let nilai = 1 ; 
    for (nilai; nilai <= 10 ; nilai++){
        console.log(nilai) 
    } 
    ```
  * WHILE LOOP
    WHILE LOOP akan menjalankan instruksi pengulangan kondisi bernilai TRUE. Gunakan WHILE LOOP jika kita tidak mengetahui jumlah pasti pengulangan.
    ```
    let count = 1 ; 
    while (count < 10){
        console.log(count);
        count ++ ;
    ```
   * DO WHILE LOOP
     Perulangan do/while akan melakukan perulangan sebanyak 1 kali terlebih dahulu, lalu mengecek kondisi yang ada di dalam kurung while.
    ```
    count = 1 ;
    do {
        console.log(count);
        count ++ ;
    } while (count <= 10)
    ```
   * NESTED LOOP
     Nested loop digunakan untuk membuat perulangan bersarang atau perulangan di dalam perualangan.
