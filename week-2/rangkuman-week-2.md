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


  


