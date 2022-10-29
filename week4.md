# **Writing-and-Presentation-Week4**
<h5>10 - 14 Oktober 2022</h5>

## **Asycnhronous**
---

<div align="justify">Konsep Asynchronous yaitu dimana konsep website meminta data baru dari server dari server tanpa melakukan reload.

- ### Promise

```js
   function GetUser(id) {
     return new Promise((resolve, reject) => {
    if (id !== "" && id !== undefined) {
     resolve (id);
    } else {
    reject ("ID Harus di Isi");
     }
   });
  }
  
  GetUser( ) // memanggil fungsinya GetUser
  .then((response) => {
   console.log(response);
   })
  .catch((error) => {
  console.log(error);
  });
```

- ### Fetch

```js
  fetch("https://pokeapi.co/api/v2/pokemon/pikachu/", {
  method: "GET"
  })
   .then(async (response) => {
  let convertData = await response.json();
  console.log(convertData);
  })
  .catch((error) => {
  console.log(error);
  });
```
- HTTP Request yaitu sebagai alat komunikasi frontend dengan backend
- HTTP Request Method
    - GET untuk mengambil data
    - POST untuk mengirimkan data
    - PUT untuk mengirimkan atau memperbaharui data
    - DELETE untuk menghapus data

&nbsp;
## **Responsive Website Design**
---

### Pengertian 
<div align="justify">Responsive  website Design yaitu suatu tampilan website yang dapat menyesuaikan dengan perangkat yang digunakan. Bisa di sebut juga sebagai teknik untuk layout atau tampilan website yang kita buat dapat menyesuaikan diri dengan ukutan layar device yang kita buat.

&nbsp;
### Mengapa kita perlu responsive ?
<div align="justify">Saat kita membuat sebuah tampilan website yang responsive pastinya memiliki manfaat nya, antara lain :
    - Memudahkan user dalam menggunakan web yang telah kita buat
    - Waktu dalam mengembangkan situs web menjadi lebih cepat
    - Dalam merawat web responsive jadi lebih mudah

&nbsp;
### Media Query
<div align="justify">Media Query adalah salah satu cara untuk mengatur suatu website agar bisa terdiri dari beberapa jenis.

- Penggunaan media query yang umum digunakan adalah min-width dan max-width
- Contoh penerapan media query
```css
@media screen and (max-width: 500px)
```
- Cara mengkondisikan Media Query ada 2 cara yaitu:
    - Memisahkan beberapa file css sesuai dengan tampilan device yang ingin di buat
    - Menggabungkan semua styling css device menjadi
- Breakpoint yaitu istilah saat terjadi nya perubahan ukuran pada suatu website ketika berganti ke device
- FlexBox bertujuan untuk membuat sebuah website yang lebih rapih dan efisien dalam mengatur serta menata item pada sebuah website.
- Properti pada FlexBox : 
  - Flex Direction
  - Flex Wrap
  - Flex Flow
  - Align Item
- Grid adalah sitem layout atau tata letak dua dimensi.
- Jenis pada Grid :
  - Grid Container
  - Grid Item

&nbsp;
## **Bootstrap**
---

- Pengertian Bootstrap adalah salah satu framework opensource yang mempunyai fungsi untuk membuat suatu responsive website.

- Komponen utama bootstrap:
  - bootstrap.css
  - bootstrap.js
  
- Cara config bootstrap:
  - Membuat tag boostrap pada tag head, dengan cara memanggil css bootstrap pada platformnya menggunakan href lalu mengganti href css dengan link bootstrap.

- Container adalah blok pembungkus bootstrap yang terdiri dari contain, padding dan alilgn yang menyelarkan konten website dalam perangkat atau area tertentu.

- Grid system adalah struktur dua demensi yang terdiri dari sumbu horisontal dan sumbu vertikal sehingga akan tersusun kolom dan baris.

- Grid system pada bootstrap:
  - .col-lg untuk mengatur grid pada ukuran monitor dengan size besar
  - .col-md untuk mengatur grid pada ukuran monitor dengan size sedang
  - .col-sm untuk mengatur monitor pada tablet
  - .col-xs digunakan untuk mengatur monitor pada handphone