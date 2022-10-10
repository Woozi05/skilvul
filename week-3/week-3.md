## Rangkuman Week 3
### JavaScript Intermediate
* ### Array & Multidimensional Array
  * Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.
  * Array didefinisikan menggunakan square brackets. Contohnya :
    ```
    let buah = ['semangka', 'manggis', 'salak'];
    console.log(buah)
    ```
  * Array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0.
    ```
    let buah = ['semangka', 'manggis', 'salak'];
    console.log(buah[0]) //output: semangka
    ```
  * Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype. Salah satu contohnya property length yang akan mengembalikan nilai dari jumlah panjang data suatu array:
    ```
    let buah = ['semangka', 'manggis', 'salak'];
    console.log(buah.length) //output: 3
    ```
  * Array memiliki method atau biasa disebut built-in methods. Contoh Array Built-in Methods
    * .push()
      Menambahkan array pada index terakhir
    * .pop()
      Menghapus array pada index terakhir
    * .shift()
      Menghapus array pada index pertama
    * .unshift()
      Menambahkan array pada index pertama
    * .sort()
      Mengurutkan array secara ascending maupun descending
  * Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach() 
    * .forEach() adalah method untuk melakukan looping pada setiap elemen array.
    * .map() melakukan perulangan/looping dengan membuat array baru.
  * Multidimensional Array bisa dianalogikan dengan array of array. Ada array didalam array. Contohnya:
    ```
    let inventory = [
      ['Kaos Polos', 9],
      ['Jaket', 3],
      ['Topi', 1],
      ['Celana', 5],
    ];
    console.log(inventory);
    ```
* ### Object & Array of Object
  * Object adalah benda mati maupun benda hidup adalah object. Pada programming object adalah sebuah tipe data pada variabel yg menyimpan properti dan fungsi (method)
  * Properti adalah data lengkap dari sebuah object
  * Method adalah action dari sebuah object.
  * Contoh Object:
    ```
    let person = {
        nama: 'Uzi',
        umur: '22',
        domisili: 'cianjur',
    }
    console.log(person)
    ```
  * Object sama seperti Array yang bisa menyimpan banyak data. Kita dapat menggunakan array of object untuk data yang lebih dari satu.
  * Looping pada Data array of object siswa
    ```
    let siswa = [
        {
         nama: 'Uzi',
         umur: '17',
         kelas: 'IPA-7',
        }
        {
         nama: 'Ananda',
         umur: '27',
         kelas: 'IPA-4',
        }
        {
         nama: 'Anisa',
         umur: '18',
         kelas: 'IPS-1',
        }
    ];

    siswa.forEach((listSiswa) => {
        console.log(listSiswa);
    })
    ```
* ### Rekursif & Modules
  * Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.
  * Contoh kasus rekursif:
    ```
    // mencari angka faktorial
    // 5!
    // 5 x 4 x 3 x 2 x 1

    // cari solusi paling kecil
    // 1! -> 1
    // 2! -> 2 x 1
    function faktorial(n) {
        if (n == 1) {
        return 1
      } else {
        return n * faktorial(n - 1)
      }
    }
    console.log(faktorial(5))
    ```
  * Modules adalah file Javascript yang di dalamnya terdapat value dari objects, functions, dan variables. Kemudian file tersebut dapat diexport dan diimport oleh file lain. Yang mana file lain yang mengimportnya dapat menggunakan values yang ada di file tersebut. Beberapa tindakan yang ada di dalam modules:
    - Export
    - Import
    - Export as
    - Import as
    - Export Default

* ### Asynchronous
  * Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous.
  * Kita bisa membuat Javascript menjadi asynchronous secara simulasi artinya tidak murni asynchronous dengan beberapa cara, yaitu callback, promises dan async/await.
  * Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya. Contohnya:
    ```
    console.log("CALLBACK")
    console.log("A")

    // butuh proses yg memakan waktu
    // callback -> function yg dijadikan sbg argumen
    setTimeout(() => {
        console.log("B")
    }, 1000)

    console.log("C")
    ```
  * Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API. Contoh promise:
    ```
    console.log("PROMISES dari function")
    let nonton = (kondisi) => {
       return new Promise((resolve, reject) => {
          if (kondisi == "jalan") {
            resolve("nonton terpenuhi")
           }
           reject("batal nonton")
       })
    }

    nonton("jalan")
    .then(result => {
      console.log(result)
    })
    .catch(err => {
       console.log(err);
    })
    ```
* ### Web Storage
  * Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. Data ini dimanfaatkan oleh situs web tersebut untuk merekam kebiasaan pengguna agar dapat memberikan rekomendasi sesuai preferensi si pengguna tersebut.
  * Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB).
  * Dengan memanfaatkan local storage dan session storage, kita dapat menyimpan data lebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web.

   
