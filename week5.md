# **Writing-and-Presentation-Week5**
<h5>24 - 28 Oktober 2022</h5>

## **Web Server dan RESTful API**
---

- **Web Server**
    - `Web Server` adalah sisi dari sebuah komputer yang bertugas untuk menyimpan, memproses dan mengirimkan file ke halaman web browser. Selain itu web server sebagai jembatan antara web browser dengan database.

    - Web server terdiri dari 2 komponen penting yaitu:
        - `Hardware`, dari sisi hardware web server adalah komputer yang fungsinya untuk menyimpan perangkat lunak server web
        - `Software`, dari sisi web server adalah bagian yang mengontrol cara penggunaan web dan mengakses file yang di hosting.

    - Static Web Server
        <div align="justify">Web server statis yang terdiri dari hardware dengan server (HTTP) dimana bertujuan server mengirimkan file yang di hosting apa adanya ke web browser.

    - Dynamic Web Server
        <div align="justify">Server web dinamis terdiri dari server web statis yang dimana di tambah perangkat lunak tambahan seperti aplikasi server dan database, yang bertujuan aplikasi server memperbaharui file yang di hosting sebelum mengirim konten ke web browser melalui HTTP.

    - Server Side Programming
        <div align="justify">Server web menunggu pesan permintaan klien, memprosesnya ketika mereka tiba, dan membalas browser web dengan pesan respons HTTP. Respons berisi baris status yang menunjukkan apakah permintaan berhasil atau tidak (misalnya "HTTP/1.1 200 OK" untuk sukses).

    - Static Sites
        <div align="justify">Static Side adalah situs yang mengembalikan konten berkode keras yang sama dari server setiap kali sumber daya tertentu diminta.

    - Dynamic Site
        <div align="justify">Dynamic Site adalah Situs web dinamis adalah situs web tempat beberapa konten respons dihasilkan secara dinamis.

&nbsp;
- **REST**
    - REST atau `REpresentational State Transfer`, adalah gaya arsitektur untuk menyediakan standar antara sistem komputer di web, sehingga memudahkan sistem untuk berkomunikasi satu sama lain.

    - Sending Responses
        - `Content Types`
        - `Response COdes`

&nbsp;
## **Intro & Essential Node JS**
---

- `Node.js` adalah software open-source yang bisa di gunakan untuk membuat aplikasi jaringan dan aplikasi server side yang real time dan scalable atau bisa dikembangkan sesuai kebutuhan. Node.js adalah runtime environment lintas platform single-thread yang dibangun berdasarkan engine JavaScript V8 Chrome.

&nbsp;
- **Node JS Architecture**
    - `Single Thread` adalah eksekusi menjalankan beberapa tugas atau program secara bersamaan. Setiap unit yang mampu mengeksekusi kode disebut thread.
    - `Even Loop`, Dengan menggunakan konsep arsitektur javascript, walaupun menggunakan single thread tetapi kita dapat melihat javascript seperti menggunakan multi thread.
    - `Server Side Scripting` yang dimana NodeJs dapat menjalankan JavaScript di server side menggunakan terminal command line menggunakan perintah "node".

&nbsp;
- **JavaScript for Node JS**
    - Arrow Expression merupakan fitur terbaru dari javascript, yaitu mempermudah membuat sintaks function menggunakan “=>”
        ```js
        // non arrow function
        function countLength(val1, val2){
            return val1.length + val2.length
        }

        // using arrow function 
        const countLengthChar = (val1, val2) => return val1.length + val2.length
        ```
    - Asynchronous memungkinkan mengeksekusi code tanpa berurutan dengan cara “skip” code dan melanjutkan eksekusi code selanjutnya.
        ```js
        console.log('hello');
        selTimeout(() => {
            console.log('JavaScript')
        }, 100) // di tunda selama 100 millisecond
        console.log('Coder');
        ```
    - JSON atau Javascript Object Notation merupakan format yang digunakan untuk menyimpan dan mengirim data menggunakan konsep object di javascript. 
        ```json
        {"users" : [
            {"username" : "Anton", "lokasi": "Bandung"},
            {"username" : "Budi", "lokasi": "Semarang"},
            {"username" : "Nana", "lokasi": "Surabaya"},
            {"username" : "Jamal", "lokasi": "Tangerang"}
        ]}
        ```

&nbsp;
- **Install Node JS**
    - Link untuk menginstall node.js
        > https://nodejs.org/en/
    - Untuk mengetes apakah berhasil terinstall
        > node -v
    - NodeJS ini juga dilengkapi dengan NPM (node package manager) dan dapat mengeceknya 
        > npm -v
    - Running Node JS
        > node 

&nbsp;
- **Node JS for Back End Development**
    Build in Module Node JS
    - `Console` merupakan module bawaan dari javascript yang ada di node JS untuk digunakan sebagai debug atau menampilkan code secara interface
    - `Process` adalah modules yang digunakan untuk menampilkan dan mengontrol prosess Node JS yang sedang dijalankan.
    - `OS` merupakan module yang digunakan untuk menyediakan informasi terkait sistem operasi komputer yang digunakan user.
    - `Util` merupakan alat bantu / utilities untuk mendukung kebutuhan internal API di Node JS
    - `Events`
    - `Errors` merupakan modules yang dapat digunakan untuk mendefinisikan error di Node JS sehingga lebih informatif.
    - `Buffer`  merupakan modules yang digunakan untuk mengakses, mengelola dan mengubah tipe data raw atau tipe data bytes
    - `FS atau “file system”` merupakan module yang dapat membantu berinteraksi dengan file yang ada diluar code. 
    - `Timers` merupakan modules yang digunakan untuk melakukan scheduling atau mengatur waktu pemanggilan fungsi yang dapat diatur di waktu tertentu.

&nbsp;
- **Membuat Web server dengan Node JS**
    - Node JS Web Server
        <div align="justify">Node.js memiliki built-in modul yang disebut HTTP, built-in modul ini memungkinkan Node JS mentransfer data melalui Hyper Text Transfer Protocol (HTTP).

        - Untuk menggunakan modul HTTP, gunakan require()
        - Gunakan method createServer() untuk membuat server HTTP
        - Callback function yang digunakan pada method http.createServer(), akan dijalankan ketika seseorang mencoba mengakses komputer pada port 8080.

    &nbsp;
    - Menambahkan HTTP Header
        - Kita bisa menggunakan method res.writeHead() untuk menambahkan header HTTP.
        - Argumen pertama dari method res.writeHead() adalah status code, 200 berarti semuanya OK
        - Argumen kedua adalah objek yang berisi header respons.
        - Contoh : 
        Jika respons dari server HTTP seharusnya ditampilkan sebagai HTML, maka kita harus menambahkan header HTTP dengan tipe konten yang benar
        ```js
        const http = require('http');

        http.createServer(fucntion (req, res) {
            res.writeHead(200, {'Content-Type' : 'text/html'});
            res.write('Hello Friends');
            res.end();
        }).listen(8080);
        ```
        - Respons yang dikembalikan dari HTTP web server bisa dalam berbagai format.
        - Contohnya, Kita bisa mengembalikan response dalam format JSON dan HTML, namun kita juga dapat mengembalikan format teks lain seperti XML dan CSV.
        - Selain itu web server dapat mengembalikan data non-teks seperti PDF, file zip, audio, dan video.
        - Format ini harus ditambahkan kedalam HTTP Header.
    
    &nbsp;
    - Membaca Query String 
        - Callback function pada method http.createServer() memiliki argumen req yang mewakili request dari klien, sebagai objek (objek http.IncomingMessage).
        - Objek ini memiliki sebuah properti yang disebut "url" yang menyimpan informasi url yang sedang mengakses.
        ```js
        const http = required('http');

        http.createServer(function (req, res) {
            res.writeHead(200, {'Content-Type' : 'text/html'});
            res.write(req.url);
            res.end();
        }).listen(8080);
        ```
    
    &nbsp;
    - Split Query String
        - Ada build-in module yang bisa kita gunakan untuk split query string menjadi beberapa bagian yang dapat dibaca.
        -Build-in modulenya adalah URL Module.

&nbsp;
## **Express JS**
> Back End Web Application framework 
---

- **Apa itu Express JS**
    <div align="justify">Express JS adalah salah satu framework yang berasal dari bahasa pemrograman JavaScript yang dirancang secara fleksibel dan minimalis, untuk pengembangan aplikasi back-end.

&nbsp;
- **Back End Web Application**
    <div align="justify">Back end app adalah aplikasi yang berjalan di server-side yang bekerja untuk memberikan informasi berupa data sesuai request dari client / browser / front end app.

    <div align="justify">Kelebihan dari framework ini terletak pada fitur caching, support dengan Google V8 Engine, JavaScript, serta didukung oleh komunitas dan skalabilitas aplikasi yang baik.

&nbsp;
- **REST API**
    <div align="justify">RESTful API / REST API merupakan penerapan dari API (Application Programming Interface). 

    <div align="justify">Sedangkan REST (Representional State Transfer) adalah sebuah arsitektur metode komunikasi yang menggunakan protokol HTTP untuk pertukaran data dimana metode ini sering diterapkan dalam pengembangan aplikasi.

    Komponen penting pada RESTFUL API :
    - URL Design
    - HTTP Verbs
    - HTTP Response Code
    - Format Response

&nbsp;
- **Basic Routes**
    - `Routes` : Kita bisa menjalankan aplikasi sederhana kita dengan cara menggunakan “node”. Dan aplikasi kita akan berjalan di alamat ‘http://localhost:3000’
    - `Method` : Kita dapat menggunakan method yang dalam REST API seperti POST, PUT, PATCH dan DELETE
    - `Response` : Di dalam route kita dapat mengirim response menggunakan parameter dari route express.js yaitu “res.Send()” untuk mengirim plain text ketika kita mengakses route tersebut.
    - `Status Code` : sebagai informasi apakah route yang kita akses berjalan sebagaimana mestinya dan tidak terjadi error.
    - `Query `: merupakan parameter yang digunakan untuk membantu menentukan tindakan yang lebih spesifik daripada hanya sekedar router biasa.
    - `Nested Route` : digunakan ketika terdapat banyak route yang memiliki nama yang sama atau ingin membuat route yang lebih mendalam

&nbsp;
- **Express Middleware**
    - `Middleware Function` : sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle.
    - Fungsi next biasanya di berikan nama variable next.
    - Cara kerja Middleware : Fungsi next biasanya di berikan nama variable next.
    - Kegunaan Middleware : 
        - Menjalankan kode apapun.
        - Memodifikasi Object Request dan Object Response.
        - Menghentikan request-response cycle.
        - Melanjutkan ke middleware function selanjutnya atau ke handler function dalam suatu request response cycle.
    - Jenis Express Middleware
        - Application Level Middleware
        - Router Level Middleware
        - Error Handling Middleware

&nbsp;
## **Design Database With MySQL**
---

- **Pengertian**
    - `MySQL` adalah sebuah implementasi dari sistem manajemen basis relational (RDBMS).
    - Kepanjangan `SQL` adalah Structure Query Language merupakan sebuah konsep pengoperasian basis data.
    - `Entitas` (entity) adalah suatu objek yang dapat di kenali dari objek lain, contohnya : mahasiswa, perusahaan, tanaman dan lain sebagainya.
    - `Atribute` adalah isi dari entitas, dimana entity di tampilkan oleh sekumpulan atribute contoh : id_mahasiswa, nama, umur, alamat dan lain sebagainya.
    - `Relasi` adalah kesesuaian antar beberapa entitas
    - Jumlah entitas ke entitas lain bisa di hubungkan melalui relasi set, yaitu:
        - One to One (1:1)
        - One to Many (1:m)
        - Many to Many (m:1)
    - Contoh membuat table user menggunakan CREATE
        ```sql
        create table 'user' {
            'id_user' int not null AUTO_INCREMENT,
            'name' varchar(25) not null default,
            'age' int not null default;
        }
        ```