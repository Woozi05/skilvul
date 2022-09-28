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
    git config --global user.email "example@email.com"
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
     ![git status]()
   * Git Add
     **git add .**, adalah perintah yang digunakan untuk menambahkan file baru di repository yang dipilih.
     ![git add]()
   * Git Commit
     **git commit -m "Tambahkan pesan"**, digunakan untuk menyimpan perubahan yang sudah dilakukan, namun tidak ada perubahan yang terjadi pada remote repository.
     ![git commit]()
   * Git Remote
     **git remote**, digunakan untuk membuat user terhubung ke remote repository.
   * Git Push
     **git push**, digunakan dalam mengirimkan perubahan file yang dilakukan setelah di commit ke remote repository.
   * Git Clone
     **git clone**, perintah yang digunakan untuk membuat salinan repository lokal.