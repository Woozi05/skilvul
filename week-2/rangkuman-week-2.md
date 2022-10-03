# Rangkuman Week 2
## JavaScript Dasar
### Scope and Function
* ### Scope
  * Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.
  * Blocks adalah code yang berada didalam curly braces {}. Conditional, function, dan  looping menggunakan blocks.
  * Scope ada 2 macam yaitu:
    * Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan diluar Blocks. contohnya:
      ```
      let myName = "Uzi" ; 
    
      function greeting() {
        return myName;
      }

      console.log(myName); //Uzi
      ```
    * Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping. Maka variabel hanya bisa diakses didalam blocks saja. Tidak bisa diakses diluar blocks.
      ```
      function greeting() {
        let myName = "Uzi" ;
        return myName;
      }

      console.log(greeting()) //Uzi
      console.log(myName); //Uncaught ReferenceError: myName is not defined because local scope
      ```
* ### Function
  * Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya. Contohnya:
    ```
    function greeting() {
      return 'Hello World';
    };
    ```
    Cara memanggil function:
    ```
    greeting() // Memanggil nama function-nya
    console.log(greeting()); // Output: 'Hello World'
    };
    ```
  * Parameter Function
    Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas. Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut. Contohnya:
    ```
    function penambahan(a, b) {
      return a + b;
    }
    ```
  * Argumen Function
    Argumen adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya. Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function kita gunakan 2 buah nilai argumen.
    ```
    function penambahan(a, b) {
      return a + b;
    }

    console.log(penambahan (3, 4)) //Output: 7
    ```
  * Default Parameter
    Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function. Default parameters bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen.
    ```
    function greetOnWebsite(name = 'Stranger') {
      return 'Hello ' + name;
    }

    console.log(greetOnWebstite('Uzi')) //Output: 'Hello Uzi'
    console.log(greetOnWebstite()) //Output: 'Hello Stranger'
    ```
  * Function Helper
    Kita bisa menggunakan function yang sudah dibuat pada function lain. Contoh:
    ```
    function multiplyByNineFifths(number) {
      return number * (9/5);
    };

    function getFahrenheit(celcius) {
      return multiplyByNineFifths(celcius) + 32;
    };
    
    getFahrenheit(20) //Returns 68
    ```
   * Arrow Function
     Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version).
     ```
     function greeting = () => {
        return 'Hello World';
     };
     ```
   * Short Syntax Function
     * Zero Parameters
       ```const functionName = () => {};```
     * One Parameter
       ```const functionName = paramOne => {};```
     * Two or More Parameters
       ```const functionName = (paramOne, paramTwo) => {};```
     * Single-Line Block
       ```const sumNumbers = number => number + number;```
     * Multi-Line Block
       ```
       const sumNumbers = number => {
             const sum = number + number;
             return sum; //Return statement
       };
       ```
### Data Type Built in Prototype and Method
* ### Data Type
  * Tipe data adalah jenis data yang dapat disimpan, dimanipulasi, dan digunakan untuk memberi tahu komputer bagaimana menafsirkan nilai atau datanya. Tipe data menentukan jenis data yang dimiliki variabel dan tipe operasi, seperti operasi matematika, logika dan sebagainya. Tipe data di JavaScript dikelompokkan ke dalam dua kategori, yaitu primitif dan non-primitif.
  * Tipe data primitif
    1. Number
       Tipe data Number atau angka di JavaScript mewakili angka positif dan negatif entah itu bulat (integer) maupun desimal (floating-point).
       ```
       const bulatPositif = 10;
       const bulatNegatif = -10;
       const desimalPositif = 4.5;
       const desimalNegatif = -4.5;
       ```
    2. String
       Tipe data String digunakan untuk mewakili data tekstual atau karakter. String dapat dibuat menggunakan petik tunggal atau ganda dan diakhiri dengan petik yang sama.
       ```
       const firstName = 'Uzi'; // petik tunggal
       const lastName = "Fauziah"; // petik ganda
       ```
    3. Boolean
       Boolean adalah tipe data yang hanya memiliki dua nilai, true dan false.
       ```
       const sudahMakan = true;
       const sudahMandi = false;
       ```
    4. undefined
       Undefined adalah nilai yang diberikan ketika variabel dideklarasikan tanpa inisialisasi atau tidak diberi nilai. Ini hanya berlaku untuk variabel let dan var, karena kita tidak dapat mendeklarasikan variabel const tanpa nilai.
       ```
       var nama;
       let umur;
       console.log(nama); // undefined
       console.log(umur); // undefined
       ```
    5. null
       null dapat digunakan untuk mewakili ketidakhadiran yang disengaja dari nilai objek. Kita dapat menetapkan null ke variabel untuk menunjukkan bahwa saat ini variabel tersebut tidak memiliki nilai apa pun, tapi nanti akan memilikinya.
       ```
       let mahasiswa = null;
       console.log(mahasiswa); // null

       mahasiswa = {
           nama: 'Uzi',
           umur: 22,
           jurusan: 'Teknik Informatika',
       };
       console.log(mahasiswa); // {nama: "Uzi", umur: 22, jurusan: "Teknik Informatika"}
       ```
   * Tipe data non-primitif
     1. Object
        Object adalah tipe data yang kompleks yang memungkinkan kita menyimpan kumpulan nilai dengan tipe data yang berbeda. Objek berisi properti yang didefinisikan sebagai pasangan kunci dan nilai (key dan value).
        ```
        const person = {
            nama: 'Uzi',
            umur: 22,
        };
        ```
     2. Array
        Array adalah jenis objek yang dapat digunakan untuk menyimpan beberapa nilai, tanpa properti seperti objek.
        ```
        const arr = ['Uzi', 22, 'Teknik Informatika'];
        ```
* ### Property String: String.length
  String.length merupakan property satu-satunya untuk String. Property ini akan mengembalikan nilai panjang karakter dari sebuah String.
  ```
  let nama = 'Uzi Fauziah';
  console.log(nama.length); //Output: 11
  ```
* ### Method String:
  1. toUpperCase() - Ubah String ke Huruf Besar
     ```
     const nama = 'Uzi';
     console.log(nama.toUpperCase()); // UZI
     ```
  2. toLowerCase() - Ubah String ke Huruf Kecil
     ```
     const nama = 'Uzi';
     console.log(nama.toLowerCase()); // uzi
     ```
  3. charAt() - Mengambil sebuah karakter dari String.
     ```
     const nama = 'Uzi';
     console.log(nama.charAt(1)); // z
     ```
  4. includes() - Melakukan pencarian (peka huruf besar/kecil) apakah string berisi atau mengandung karakter yang ditentukan.
     ```
     const nama = 'Uzi';
     console.log(nama.includes('z')); // true
     ```
  5. split() - Pecah String dan Ubah Menjadi Array
     ```
     const nama = 'Uzi Fauziah Azhari';

     console.log(nama.split()); // ["Uzi Fauziah Azhari"]
     console.log(nama.split(' ')); // ["Uzi", "Fauziah", "Azhari"]
     console.log(str.split(' ', 2)); //  ["Uzi", "Fauziah"]
     ```
* ### Number
  * Kita bisa membuat data angka menggunakan sintaks literal, fungsi constructor Number(), maupun objek Number.
    * Number literal
      ```
      const a = 22;
      console.log(a); // 19
      ```
    * Number()
      ```
      const b = Number(22);
      console.log(b); // 22
      ```
    * new Number()
      Membuat data angka menggunakan metode ini menghasilkan nilai non-primitif atau objek.
      ```
      const a = new Number(1);
      console.log(a); // Number {1}
      ```
  * Number Method
    1. toFixed() - memformat angka ke notasi fixed-point.
       ```
       let angka = 3.12345
       console.log(angka.toFixed(1)) // 3.1
       console.log(angka.toFixed(2)) // 3.12
       ```
    2. Number.isNaN() - mengecek aapakah suatu nilai adalah NaN atau bukan.
       ```
       console.log(isNaN(2131)) // false
       console.log(isNaN("dawdf")) // true
       ```
    3. toPrecision() - memformat angka agar memiliki panjang yang ditentukan.
       ```
       (2).toPrecision(3); // 2.00
       (2.2543).toPrecision(3); // 2.25
       (2.26).toPrecision(2); // 2.3
       (2.23).toPrecision(1); // 2
       ```
    4. toString() - mengonversi angka menjadi string.
       ```
       (19).toString(); // '19'
       ```
    5. Number.isInteger() - mengecek apakah suatu nilai bilangan bulat atau bukan.
       ```
       Number.isInteger(2.4); // false
       Number.isInteger(3); // true
       ```
* ### Math
  * Properties
    1. Math.PI : Berisi nilai dari pi (π) dengan nilai 3.141592653589793
    2. Math.E: Berisi nilai dari logaritma natural e, dengan nilai 2.718281828459045
    3. Math.LN10 : Berisi nilai dari logaritma natural 10, dengan nilai 2.302585092994046
    4. Math.SQRT1_2: Berisi hasil dari 1 dibagi dengan akar kuadrat 2, dengan nilai 0.707106781186
  * Method
    1. Math.abs() - berfungsi untuk menghasilkan nilai absolut (nilai negatif akan menjadi positif, sedangkan nilai positif akan tetap positif).
       ```
       Math.abs(-5)      // hasilnya: 5
       Math.abs(5)       // hasilnya: 5
       ```
    2. Math.ceil() - berfungsi untuk pembulatan keatas dari sebuah nilai desimal.
       ```
       Math.ceil(1.99);    // hasilnya: 2
       Math.ceil(1.01);    // hasilnya: 2
       Math.ceil(1.0);     // hasilnya: 1
       Math.ceil(-1.99);   // hasilnya: -1
       ```
    3. Math.floor() - berfungsi untuk pembulatan kebawah dari sebuah nilai desimal.
       ```
       Math.floor(1.99);    // hasilnya: 1
       Math.floor(1.01);    // hasilnya: 1
       Math.floor(1.0);     // hasilnya: 1
       Math.floor(-1.01);   // hasilnya: -2
       ```
    4. Math.round() - berfungsi untuk membulatkan nilai angka ke bilangan terdekat.
       ```
       Math.round(1.56);    // hasilnya: 2
       Math.round(1.44);    // hasilnya: 1
       Math.round(1.0);     // hasilnya: 1
       Math.round(-1.6);    // hasilnya: -2
       ```
     5. Math.random() - berfungsi untuk menghasilkan angka acak dalam setiap pemanggilan.
        ```
        Math.random();    // hasilnya: 0.2605599395465106
        Math.random();    // hasilnya: 0.6355015402659774
        ```
* ### Date
  JavaScript memiliki Object Date yang dapat digunakan untuk memformat waktu. Object Date memiliki berbagai method yang dapat digunakan untuk menampilkan tahun, bulan, hari, bahkan waktu.
  ```
  let date = new Date()
  console.log(date.getDay()); // 1
  console.log(date.getFullYear()); // 2022
  console.log(date.getMonth()); // 9
  console.log(date.getDate()); // 3
  ```
## DOM (Document Object Model)
   Dom adalah jembatan supaya bahasa pemrograman dapat berinteraksi dengan dokumen HTML. Dengan DOM, JavaScript dapat memanipulasi HTML. DOM bukan bagian dari JavaScript, melainkan browser (Web API)
   * Memanipulasi Element HTML
     * Mencari Element HTML
       ```
       //Mencari 1 element dengan id tertentu
       document.getElementById("header")

       //Mencari beberapa element sekaligus dengan class tertentu
       document.getElementsByClassName("Container")

       //Mencari element menggunakan kombinasi selector (seperti di CSS)
       document.querySelector("#header p span")
     * Mengubah Konten Element
       * Element.textContent
         document.getElementById("header").textContent = "Teks Heading"
         ![contoh .textContent](https://github.com/Woozi05/skilvul/blob/988aa56e7d40c293e39bc60918a2b47fc508348e/week-2/gambar/dom.png)
       * Element.innerHTML
         document.getElementById("header").innerHTML = "```<h1>Hello World</h1>```"
     * Membuat Element HTML
       ```
       // Jika ada element ini di file HTML
       <div id="header"></div>

       // Lalu kita gunakan kode JavaScript ini untuk membuat sebuah element heading
       const heading = document.createElement("h1")
       heading.textContent = "Ini Heading"

       document.getElementByID("header").appendChild(heading)

       // Hasilnya akan sama seperti jika kita menulis
       <div id="header">
          <h1>Ini Heading</h1>
       </div>
       ```
       .createElement() -> .textContent untuk mengubah kontennya -> .appendChild() untuk menambahkan ke DOM

       ```
       // append vs appendChild
       // appendChild tidak bisa input data string
       app.append("menggunakan append")
       app.appendChild("appendChild") // error
       ```
     * Remove Element
       ```
       let end = document.getElementById("end")
       end.remove()
       ```
     * Attributes
       ```
       console.log(link.attributes) // [] list attribute
       console.log(link.getAttribute("href")); // ambil isi attribute
       link.setAttribute("id", "google") // add attribute
       ```
     * Memberikan Style
       ```
       link.style.color = "black"
       link.style.border = "1px solid black"
       link.style.padding = "5px 20px"
       link.style.backgroundColor = "aqua"
       link.style.removeProperty("border") // menghapus style property
       ```
     * Mendapatkan Style dari Element
       ```
       let tess = document.getElementById("tess")
       let tessStyle = getComputedStyle(tess)
       console.log(tessStyle.height)
       ```
     * Class
       ```
       let container = document.getElementsByClassName("container")[0]
       console.log(container.classList); // [] list of class
       container.classList.add("home") // menambahnkan class
       container.classList.remove("container") // menghapus class
       ```
    * Interaksi User (Events)
      User experience itu bersifat dua arah: selain menampilkan element HTML, halaman web juga harus bisa menangkap interaksi user. Misalnya seperti: User melakukan scroll, User melakukan klik pada elemen tertentu, Halaman web di-load, Form di-submit, dan sebagainya.
    * Ada dua cara yang biasanya dilakukan untuk handle event di Javascript.
      * Cara Pertama: Menggunakan Atribut
        HTML memiliki atribut event untuk menentukan fungsi yang akan dijalankan saat event terjadi.
        ```
        <button onclick="Hello()">Klik Me</button>
        ```
        **onclick** adalah atribut HTML untuk menentukan aksi saat event klik pada sebuah elemen. Atribut ini bisa diisi dengan nama fungsi atau ekspresi javascript.
      * Cara Kedua: Method addEventListener()
        Method addEventListerner() merupakan method yang terdapat pada object DOM. Object ini mewakili sebuah elemen HTML di Javascript.
        ```
        button.addEventListener('click', function(e){
  
        });
        ```
        






