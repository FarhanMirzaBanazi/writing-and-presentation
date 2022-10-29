# **Writing-and-Presentation-Week2**
<h5>26 - 30 September 2022</h5>

## **JavaScript**
---

- ### **Pengertian JavaScript**
    <div align="justify">JavaScript adalah bahasa pemrograman/scripting untuk membuat konten dinamis di halaman atau aplikasi website, game, serta membangun web serves.

    &nbsp;
- ### **Fungsi JavaScript**
    <div align="justify">Bahasa Pemrograman JavaScript berfungsi untuk pengembangan aplikasi website dan mobile, membangun web server dan aplikasi server, membuat website yang interaktif serta selain membuat web JS juga dapet membuat game.

    &nbsp;
- ### **Tipe Data**
    <div align="justify">Tipe data yaitu klasifikasi yang di berikan untuk menampung berbagai macam data yang di gunakan dalam programming. Pada JavaScript ada beberapa jenis tipe data yaitu:

    - ### Number
        Number merupakan tipe data yang merujuk pada sebuah angka baik itu bilangan berbentuk bulat ataupun desimal, Number juga bisa di sebut dengan integer.
    - ### String
        String merupakan tipe data yang merujuk pada sebuah kata atau kalimat, ciri khas tipe data string ini yaitu adanya tanda petik dua/satu ("..." atau '...').
    - ### Boolean
        Boolean merupakan tipe data yang mempresentasikan ebtitas logika. Pada tipe data boolean ini hanya memiliki 2 nilai yaitu True dan False.
    - ### NULL
        NULL ialah tipe data yang tidak memiliki nilai, maka apabila suatu variabel tidak memiliki nilai maka variabel tersebut bernilai NULL.
    - ### Undefined
        Undefined yaitu tipe data yang tidak memiliki nilai namun berbeda dengan null, undefined tidak memiliki object. Perbedaan antara null dan undefined ialah jika null tidak bernilai dengan kondisi yang sudah di rencanakan namun jika undefined tidak memiliki nilai dikarenakan sebuah kesalahan atau eror.

    &nbsp;
- ### **Variabel**
    <div align="justify">Variabel merupakan sebuah tempat dimana yang bertujuan untuk menampung sebuah nilai dengan identitas.

    ```
    Ada 3 cara penggunaan variabel dalam JS:
        - var (versi lama)
        - let (versi terbaru)
        - const (variabel yang nilai nya tidak dapat di ubah)
    ```

    &nbsp;
- ### **JavaScript Conditional**
    <div align="justify">Conditional merupakan statement percabangan yang menggambarkan suatu kondisi. Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut.
    
    Case ini meliputi:
    &nbsp;
    - IF Statement
    - IF ELSE Statement
    - IF ELSE IF Statement
    - Truthly and Falsy
    - Swicth Case Condtional

    Contoh:
    ```js
    // saya ambil contoh case IF ELSE IF
    let lampuLalu = 'merah';

    if (lampuLalu === 'merah'){
        console.log('Berhenti!')
    }else if (lampuLalu === 'kuning'){
        console.log('Hati-hati')
    }else if (lampuLalu === 'hijau'){
        console.log('Jalan')
    }else{
        console.log('Lampu Lalu Lintas rusak')
    }
    // output Berhenti
    ```

    &nbsp;
- ### **Switch Case Conditional**
    <div align="justify">Penggunaan Switch Case jika kondisi dan percabangan terlalu banyak. Switch Case Conditonal

    Contoh:
    ```js
    var buttonPushed = 1;

    switch (buttonPushed){
        case 1:{
            console.log('Matikan TV!'); break
        }
        case 2:{
            console.log('Turunkan volume TV!'); break
        }
        case 3:{
            console.log('Tingkatkan volume TV!'); break
        }
        case 4:{
            console.log('Matikan suara TV!'); break
        }
        default:{
            console.log('Tidak terjadi apa-apa');
        }
    }
    ```

- ### **JavaScript Looping**
    <div align="justify">Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.

    Looping meliputi:
    &nbsp;
    - ### FOR LOOP
    - ### WHILE LOOP
    - ### DO WHILE
    - ### Nested LOOP

    Contoh:
    ```js
    // saya ambil contoh Looping While
    let angka = 1;

    while (angka <= 10>){
        console.log(angka);
        angka++;
    }
    ```

&nbsp;
- ### **JavaScript-Scope**
    <div align="justify">Scope adalah konsep dalam flow data variabel, yang fungsi nya untuk menentukan suatu variabel bisa di akses pada scope tertentu atau tidak.

    <div align="justify">Analoginya seperti kita bisa melihat bintang-bintang di langit karena bumi bersifat global. Namun jika kamu tinggal di surabaya maka kamu tidak bisa melihat monas, dikarenakan monas bersifat local yaitu di jakarta.

    &nbsp;
    <div align="justify">Contoh JavaScript-Scope ada 2 yaitu:

    - ### Global Scope
        <div align="justify">Global Scope adalah variabel yang kita buat dapat di akses di manapun dalam suatu file. Agar menjadi Global Scope, suatu variabel harus dideklarasikan di luar Blocks.

        Contoh:
        ```js
        let nama = 'Aru';

        function greeting() {
            return nama; // Aru
        }

        console.log(nama); // output Aru
        ```
    
    &nbsp;
    - ### Local Scope
        <div align="justify">Local Scope yaitu mendeklarasikan variabel di dalam blocks seperti function, conditional atau looping. maka variabel hanya dapat di akses di dalam blocks itu saja dan tidak bisa di akses di luar blocks.

        Contoh:
        ```js
        function greeting() {
            let nama = 'Aru';
            return nama; // Aru
        }

        console.log(greeting()) // Aru
        console.log(nama); // eror 
        ```
    
    &nbsp;
- ### **JavaScript-Function**
    <div align="justify">Fuction adalah sebuah block kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur. Saat kita membutuhkan fitur tersebut nantinya, kita bisa kembali menggunakannya.
    
    Membuat Function:
    ```js
    function greeting(){
        return 'Hello World!'
    }
    ```
    
    Memanggil Fuction:
    ```js
    greeting() // memanggil nama fuction
    console.log(greeting()) // output 'Hello World!'
    ```

    &nbsp;
- ### **Parameter dan Argumen**
    - ### Parameter
        <div align="justify">Parameter ialah sebuah inputan data yang terletak di dalam sebuah function dan menggunakannya untuk melakukan .

        Contoh:
        ```js
        function penambahan(a, b){
            return a + b;
        }
        // a dan b di dalam function penambahan di namakan parameter
        ```
    
    &nbsp;
    - ### Argumen
        <div align="justify">Argumen adalah nilai yang di gunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameter nya.

        Contoh:
        ```js
        function penambahan(a, b){
            return a + b;
        }

        console.log(penambahan(5, 4)) // output 9
        ```
    
    &nbsp;
- ### **Dafault Parameters**
    <div align="justify">Default parameters di gunakan untuk memberikan nilai awal/default pada parameter function, selain itu default parameters bisa digunakan jika kita ingin menjaga function agar tidak eror saat di panggil tanpa argumen.

    Contoh:
    ```js
    function greetOnWebsite(name = 'User'){
        return 'Hello ' + name;
    }
    console.log(greetOnWebsite('Aru')); // output 'Hello Aru'
    console.log(greetOnWebsite()); // output 'Hello User'
    ```

&nbsp;
- ### **Function Helper**
    <div align="justify">Function Helper memungkinkan kita dapat menggunakan function yang sudah di buat pada function lain.

    Contoh:
    ```js
    function multiplyBynineFifths(number){
        return number * (9/5);
    };

    function getFahrenheit(celcius){
        return multiplyBynineFifths(celcius) + 32;
    };
    getfahrenheit(15); // return 59
    ```

&nbsp;
- ### **Arrow Function**
    <div align="justify">Arrow Function adalah cara lain untuk menuliskan function. Arrow Function adalah fitur terbaru yang ada pada ES6 (JacaScript Version).

    Contoh:
    ```js
    const greeting = () => {
        return 'Hello World';
    };

    const penambahan = (a, b) => {
        return a + b;
    };
    ```

&nbsp;
- ### **DOM HTML**
    - DOM merupakan singkatan dari **Document Object Model**. Yang artinya dokumen HTML yang dimodelkan dalam sebuah objek. Dengan menguasai DOM kita bisa berinteraksi dengan HMTL dan CSS melalui JavaScript. Perlu di ingat bahawa DOM bukan bagian JavaScript melainkan browser(web API).
    - Cara memanggil DOM dengan value yaitu:
        - Memanggil tag HTML pada atribute ID
            ```js
            console.log(document.getElementByID("header"))
            ```
        - Memanggil tag HTML pada atribute Class Name
            ```js
            console.log(document.getElementByClassName("text"))
            ```
        - Memanggil tah HTML berdasarkan query selector
            ```js
            console.log(document.querySelector("#header"))
            console.log(document.querySelector(".text"))
            ```
    
    - ### Memanipulasi content :
        - Mendeklarasi variabel header sebagai wadah untuk menyimpan tag HTML

            ``let header = document.getElementById("header")``

        - Memenipulasi content pada header dengan id header

            ``document.getElementById("header").textContent = "Heading"``

        - Memanipulasi content di dalam element dengan .innerHtml

            ```
            <ul id="list"></ul>

            document.getElementById("list").innerHMTL = "<li>List pertama</li> <li>List kedua</li>"
            ```
    
    - ### Membuat element

        ```js
        // jika ada element di bawah ini pada
        <div id="header"></div>

        // lalu kita gunakan kode Js ini
        // untuk membuat sebuah element heading
        const heading = document.createElement("h1")
        heading.textContent = "Ini Heading"

        document.getElementById("header").appendChild(heading)

        // hasilnya akan sama seperti jika kita menulis
        <div id="header">
            <h1>Ini Heading</h1>
        </div>
        ```
    
    &nbsp;
    - ### Interaksi User (Event)
        <div align="justify">User experience itu bersifat dua arah: selain menampilkan element HTML halaman web juga harus bisa menangkap interaksi user.

        Contoh HTML DOM Event:
        - Menangkap Interaksi User
            - element.addEventListener("event")
            - element.oneevent

        - EventListener
            <br/>
            Dengan cara Element.addEventListener("event")
            - Bisa dihilangkan.
            - Bisa ada beberapa event listener yang sama untuk 1 element
            - Memiliki argument tambahan {options}
        
        - EventListener - Click
            Misalkan mempunyai element 
            ``<input id=”user-input” />`` dan
            ``<button id=”alert-button”>show</button>``
            Kita ingin menampilkan pop up berupa teks di dalam input tadi.
            ```js
            // cari dulu kedua element tersebut berdasarkan id-nya
            const input = document.getElementById(“user-input”)
            const button = document.getElementById(“alert-button”)

            // baru tambahkan event listener
            button.addEventListener(“click”, function() {
	            alert(input.value)
            })
            // atau
            button.onclick = function() { alert(input.value) }
            ```
        
        - EventListener - Blur
            <div align="justify">“Blur”, lawan dari “focus”, adalah event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element) <br/>
            
            Misalkan kita ingin memvalidasi isi dari 
            ``<input id="username"/>`` agar panjangnya minimal 6 karakter

            ```js
            // cari dulu element tersebut berdasarkan id-nya
            const input = document.getelementById("username")

            // tambahkan event listener
            input.addEventListener("blur", () => {
                if(input.value.length < 6>) alert("Panjang username minimal 6")
            })
            ```
        
        - EventListener - Form Submission
            
            Misalkan kita mempunyai element beberapa input dalam sebuah form ``<input name=”email />`` dan 
            ``<input type=”password” name=”password” />``. Bagaimana caranya  kita mendapatkan isi dari kedua input tersebut saat submit form?
            <br/>
            Ada 2 cara:

            - Pasang event listener di kedua input dan tombol submit, lalu saat tombol diklik, baca value dari kedua input tersebut. 
            - Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input
            <br>
            <div align="justify">Pasang event listener di form, lalu gunakan FormData untuk mengambil data dari masing-masing input
            
            ```js
            const form = document.getElementById("form")

            form.addEventListener("submit", function(event) {
                // cegah page refresh
                event.preventDefault()

                const formData = new Formdata(form)
                const value = Object.fromEntries(formData) // {email: ....}
            })
            ```