## Rangkuman Week 4
* ### JavaScript Intermediate - Asyncrhonous
  * #### Async-Await
    Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise. Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.
    Cara penulisan Async/await menggunakan ES6 dan tidak menggunakan ES6:
    ```
    async function hello(){
        let result = await 'Hello'
        return result
    }
    // ES6
    const hello1 = async () {
        let result = await 'Hello'
        return result
    }
    ```
  * #### Fetch
    Fetch adalah native web API untuk melakukan HTTP calls dari external network. fetch() memiliki parameter utama yaitu URL/endpoint API, dan parameter kedua yaitu options, options ini berisi method, headers dan body. Contoh fetch() dengan parameter URL:
    ```
    let URL = "https://digimon-api.vercel.app/api/digimon"
    fetch(URL)
    ```
* ### Git dan GitHub Lanjutan
  * Branch adalah cabang dari repository yang dapat digunakan untuk membuat perubahan. Fitur ini wajib digunakan jika berkolaborasi dengan developer atau dalam tim Untuk menghindari conflict code yang dikembangkan.
  * Jika ingin membuat fitur baru, maka harus membuat branch baru (tidak boleh di branch utama atau master). Kemudian jika tim ingin berkolaborasi dalam sebuah project maka harus dikerjakan di branch masing-masing.
  * Untuk membuat branch, gunakan perintah berikut ini:
    ```
    git branch <branch>
    ```
    Melihat branch
    ```
    git branch
    ```
    Pindah branch
    ```
    git checkout <nama_branch>
    ```
    Menghapus branch
    ```
    git branch -d <branch>
    ```
  * Untuk menyatukan branch cabang fitur yang telah dikembangka, gunakan perintah seperti berikut:
    1. Pindah dahulu ke branch master
       ```
       git checkout master
       ```
    2. Lakukan merge
       ```
       git merge <branch>
       ```
   * git fetch adalah command yang digunakan untuk mengambil perubahan pada remote repository tanpa menggabungkan perubahan tersebut ke local repository.
   * git pull adalah command yang digunakan untuk mengambil perubahan pada remote repository dan menggabungkan perubahan tersebut ke local repository.
   * Pull request adalah fitur untuk mengajukan request perubahan kita dari branch yang sedang kita kerjakan ke branch tertentu pada Github.
   * Siapapun yang memiliki akses push ke dalam repository dapat melakukan merge dari pull request yang ada.

* ### Responsive Web Design
  * Responsive Web Design bertujuan untuk membuat design website dapat diakses oleh device apapun, seperti laptop/PC, tablet, dan smartphone.
  * Agar web responsif harus ditambahkan meta viewport pada HTML
  * Menggunakan max-width pada styling web, contohnya:
    ```
    <img style="max-width: 100% src="nature.jpg" alt="image">
    ```
    Dengan styling tersebut panjang image tidak akan overflow karena menyesuaikan dengan device
  * Media query digunakan untuk membuat beberapa styles tergantung pada jenis device. Ada 2 cara dalam menggunakan media query:
    1. Membuat file CSS berbeda untuk masing-masing device.
    2. Menggabungkan 1 file CSS untuk setting styling berbagai device.
  * Breakpoint adalah perubahan yang terjadi pada tampilan saat berganti device atau ukuran width.
  * Jika ingin menerapkan tampilan pada range tertentu, kita bisa membuatnya menjadi range media query. Contoh menggunakan media query min dan max:
    ```
    @media screen and (min-width: 481px) and (max-width: 768px) {
      body {
          background-color: blue;
      }
    }
    ```
* ### Bootstrap 5
  * Bootstrap 5 adalah salah satu framework CSS terpopuler di dunia. Bootstrap 5 merupakan versi terbaru dari versi sebelumnya yaitu bootstrap 4. Bootstrap 5 hadir untuk menyelesaikan masalah pada bootstrap 4 yang dinilai terlalu berat dan memperlambat kinerja website.
  * Bootstrap ditemukan oleh developer twitter yang bernama Mark Otto dan Jacob Thornton.
  * Kelebihan bootstrap 5:
    1. Membuat website mobile-friendly
    2. Menghemat waktu pembuatan website
    3. Fitur kustomisasi yang berlimpah
    4. Meningkatkan konsistensi desain
    5. Ketersediaan resource & dukungan
  * Menggunakan bootstrap menggunakan CDN:
    Membuat tag link menuju CSS dari Bootstrap di head
    ```
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    ```
  * Container adalah struktur paling dasar di dalam Bootstrap. Jika kita ingin memakai Bootstrap grid system, seluruh kode HTML harus berada di dalam container. Cara pembuatan container sangat sederhana, cukup tambah class .container ke dalam sebuah tag HTML:
    ```
    <div class="container">
     ...
     ...
    </div>
    ```
    Jika yang dipakai adalah class=”container-fluid”, maka kotak container akan menggunakan seluruh lebar jendela web browser 100%. Ketika jendela web browser berubah, lebar container juga akan menyesuaikan diri (fluid-width container).