## **Materi Perkuliahan: Bootstrap Layout dan Konten**

### **1. Pendahuluan: Apa itu Bootstrap?**

**Bootstrap** adalah framework open-source yang digunakan untuk mengembangkan situs web responsif dan mobile-first. Framework ini mencakup template desain berbasis HTML, CSS, dan JavaScript, serta menyediakan komponen UI yang siap pakai untuk membuat halaman web yang menarik dan fungsional. 

Bootstrap mengatur layout dan elemen-elemen di dalamnya agar tampak konsisten pada berbagai perangkat dan resolusi layar. Ada dua konsep utama yang akan dibahas di sini: **Layout** dan **Konten**.

---

### **2. Bootstrap Layout**

Bootstrap Layout bertanggung jawab untuk mengatur struktur halaman agar responsif di berbagai perangkat. Dalam Bootstrap, layout dapat diatur dengan **Grid System**, **Container**, dan **Utilities**.

#### **2.1. Grid System**

Bootstrap menggunakan **Grid System** yang membagi halaman menjadi kolom-kolom yang fleksibel. Sistem ini dibagi menjadi 12 kolom, yang memungkinkan kita untuk membuat layout dengan berbagai variasi.

**Contoh Struktur Grid:**

```html
<div class="container">
    <div class="row">
        <div class="col-4">
            <!-- Kolom 1 -->
        </div>
        <div class="col-4">
            <!-- Kolom 2 -->
        </div>
        <div class="col-4">
            <!-- Kolom 3 -->
        </div>
    </div>
</div>
```

- **`.container`**: Menyediakan ruang untuk layout yang responsif. 
- **`.row`**: Digunakan untuk mendefinisikan baris dalam grid.
- **`.col`**: Kolom dalam grid. Jumlah kolom dapat disesuaikan (misalnya `.col-4` untuk 4 kolom).

**Responsif**: Dalam Bootstrap 4 dan seterusnya, grid dapat disesuaikan dengan kelas seperti `.col-sm-*`, `.col-md-*`, `.col-lg-*`, yang menunjukkan ukuran kolom berdasarkan lebar layar.

**Contoh Responsif Grid:**

```html
<div class="container">
    <div class="row">
        <div class="col-sm-6 col-md-4 col-lg-3">
            <!-- Kolom 1: Lebar berbeda tergantung ukuran layar -->
        </div>
        <div class="col-sm-6 col-md-4 col-lg-3">
            <!-- Kolom 2 -->
        </div>
        <div class="col-sm-6 col-md-4 col-lg-3">
            <!-- Kolom 3 -->
        </div>
    </div>
</div>
```

- `.col-sm-6`: Kolom akan mengambil 6 kolom (setengah dari 12) pada layar kecil (sm).
- `.col-md-4`: Kolom akan mengambil 4 kolom (seperempat dari 12) pada layar medium (md).
- `.col-lg-3`: Kolom akan mengambil 3 kolom pada layar besar (lg).

#### **2.2. Containers**

- **`.container`**: Membatasi lebar konten dan memastikan layout responsif dengan margin otomatis.
- **`.container-fluid`**: Membuat kontainer mengambil seluruh lebar layar (tanpa batasan).

```html
<div class="container">
    <p>Konten dalam container dengan lebar terbatas.</p>
</div>

<div class="container-fluid">
    <p>Konten dalam container fluid dengan lebar penuh.</p>
</div>
```

#### **2.3. Offset dan Alignment**

- **Offset** digunakan untuk memberi ruang di awal kolom.
  
```html
<div class="col-md-4 offset-md-2">
    <!-- Kolom ini akan di-offset 2 kolom dari kiri -->
</div>
```

- **Alignment** untuk menata posisi kolom dalam baris.

```html
<div class="row justify-content-center">
    <div class="col-md-4">
        <!-- Kolom di tengah -->
    </div>
</div>
```

- **.align-items-center**: Untuk meratakan item dalam baris secara vertikal.

---

### **3. Bootstrap Konten**

Konten dalam Bootstrap mencakup berbagai elemen HTML yang sudah di-styling dengan kelas-kelas Bootstrap untuk menghasilkan tampilan yang rapi dan fungsional.

#### **3.1. Typography**

Bootstrap menyediakan kelas-kelas untuk memformat teks secara cepat:

- **Heading (Judul)**: 
  - `<h1 class="display-1">` hingga `<h1 class="display-4">` untuk berbagai ukuran judul.
  - `<h1>`, `<h2>`, `<h3>`, dll., untuk heading standar.

```html
<h1 class="display-1">Judul Utama</h1>
<p class="lead">Ini adalah paragraf lead yang lebih besar dan menonjol.</p>
```

#### **3.2. Lists**

- **List group**: Untuk menampilkan item dalam bentuk daftar dengan desain yang konsisten.

```html
<ul class="list-group">
    <li class="list-group-item">Item 1</li>
    <li class="list-group-item">Item 2</li>
    <li class="list-group-item">Item 3</li>
</ul>
```

- **Ordered and Unordered Lists**:

```html
<ul class="list-unstyled">
    <li>Item tanpa bullet</li>
    <li>Item lainnya</li>
</ul>

<ol class="list-decimal">
    <li>Item terurut 1</li>
    <li>Item terurut 2</li>
</ol>
```

#### **3.3. Tables**

- **Table**: Menampilkan data dalam format tabel.

```html
<table class="table table-striped">
    <thead>
        <tr>
            <th>#</th>
            <th>Nama</th>
            <th>Alamat</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>John</td>
            <td>Jakarta</td>
        </tr>
    </tbody>
</table>
```

- **Kelas tabel**:
  - `.table`: Untuk tabel standar.
  - `.table-striped`: Menambahkan garis selang-seling.
  - `.table-bordered`: Menambahkan garis tepi.
  - `.table-hover`: Menambahkan efek hover.

#### **3.4. Forms**

Bootstrap menyediakan berbagai elemen untuk membuat form yang responsif dan mudah digunakan.

```html
<form>
  <div class="mb-3">
    <label for="name" class="form-label">Nama</label>
    <input type="text" class="form-control" id="name" placeholder="Masukkan nama">
  </div>
  <button type="submit" class="btn btn-primary">Kirim</button>
</form>
```

- **Form-control**: Untuk mengatur input form agar sesuai dengan desain Bootstrap.
- **btn btn-primary**: Untuk tombol dengan gaya utama.

#### **3.5. Media Objects**

Untuk menampilkan gambar atau video dengan teks yang menyertainya.

```html
<div class="media">
  <img src="gambar.jpg" class="mr-3" alt="Gambar">
  <div class="media-body">
    <h5 class="mt-0">Judul Media</h5>
    <p>Deskripsi atau teks yang terkait dengan media ini.</p>
  </div>
</div>
```

---

### **4. Penutup**

- **Layout** dalam Bootstrap memungkinkan kita untuk membuat halaman yang fleksibel dan responsif dengan menggunakan sistem grid dan container.
- **Konten** dalam Bootstrap, termasuk elemen seperti typography, tabel, dan form, dapat dimanfaatkan untuk membuat halaman web yang lebih interaktif dan dinamis dengan sedikit kode.

Sebagai latihan, coba buatlah sebuah halaman web sederhana yang mencakup berbagai elemen layout dan konten yang telah dijelaskan. Mulailah dengan struktur grid, kemudian tambahkan tabel, form, dan list untuk mengatur konten.

---

### **5. Referensi**

- [Dokumentasi Resmi Bootstrap](https://getbootstrap.com/)
- Buku: "Bootstrap 4: Web Development with HTML, CSS, and JavaScript"

---

Semoga materi ini membantu!
