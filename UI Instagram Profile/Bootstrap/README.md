# Instagram Cloning
Pada studi kasus membuat Instagram Cloning, saya memakai program:
- **HTML5🗒️**
- **CSS3⚓**
- **Bootstrap 5🅱️**
---
## Pengertian Bootstrap 🅱️
Bootstrap merupakan framework front-end  yang menyediakan komponen-komponen siap pakai berupa *HTML*, *CSS*, maupun *JavaScript* untuk membantu pengembang membuat situs web dan aplikasi yang responsif dan menarik secara visual.
---
## Feature On Cloning Instagram ❔
- **Responsif pada website**
    - 📱 Mobile yang berukuran <= 576px 1 Foto 📷
    - 💻 Desktop yang berukuran >= 992px 3 Foto 📷
    - 📲 Tablet yang berukuran >= 768px 4 Foto 📷
- **Tema Gelap pada website**
- **Button Edit Profile dan Follow**
- **Tata letak postingan mirip Instagram asli**
---
## Build/Run Bootstrap Lewat CDN </>
1. Salin Kode Ini
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
```
2. Paste di kode bagian Head sesudah title
Contohnya:
```html
<title>...</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
```
## Struktur Penempatan File + Cara menjalankan website
1. Pastikan penempatan file dan folder dengan benar. dalam folder `assets` berisikan ekstensi css dan gambar ekstensi jpeg dan jpg.
```
Proyek UI Cloning Instagram/
├── index.html
├── assets
    └── Gambar 1 sampai 12.jpg
    └── guest.jpeg
    └── style.css
```
2. Selanjutnya, bisa dibuka file `index.html` dengan cara klik kiri dua kali, akan tertuju ke *Google Chrome*, *Opera*, ataupun *browser* lainnya.
---
## Depedensi Pada Bootstrap 🅱️
1. HTML5 doctype `<!DOCTYPE html>` diperlukan agar browser mengikuti elemen dan css modern
2. `<meta name="viewport" content="width=device-width, initial-scale=1">` agar layout responsif mobile-first bekerja.
---
## Component Bootstrap 🅱️
1. **Navbar ↗️**
    - `navbar` Navbar Pada Komponen Navigasi Utama.
    - `navbar-dark` Teks dan Ikon(logo) Berwarna Putih, Dengan Background Gelap.
    - `bg-black` Pewarnaan Background Hitam.
    - `border-bottom border-secondary` Garis tipis Bawah *Navigation Bar* Warna Abu-Abu.
    - `container`Untuk Membungkus Isi Navigasi Bar Agar Rapi.
    - `navbar-brand` Navbar Untuk Logo.
    - `d-flex align-items-center` *Flexbox utility* Buat Menyusun Konten Sejajar Secara Vertikal.
Kodenya:
```html
<nav class="navbar navbar-dark bg-black border-bottom border-secondary">
  <div class="container">
    <a class="navbar-brand d-flex align-items-center" href="#" onclick="alert('Coming Soon!')">
      <img src="..." height="40" alt="Instagram Logo">
    </a>
  </div>
</nav>
```
---
2. **Container🏗️**
    - `container` Memberikan padding (jarak antara isi dengan tepi) kanan atau kiri untuk tidak berdekatan layar.
    - `my-4` Memberikan margin (jarak antara elemen dengan elemen lain) dengan vertikal (atas bawah) dengan set `4` unit spacing.
Kodenya:
```html
<div class="container my-4">
```
---
3. **Grid System (Row dan Col)📏**
    - `row` Baris Pada Grid.
    - `col-12` Kolom Penuh Pada Mobile (1 gambar).
    - `col-md 4` Kolom Mengambil 1/3 Lebar (3 gambar).
    - `col-lg-3` Kolom Mengambil 1/4 Lebar (4 gambar).
    - `g-3` Gutter Spacing Antar Kolom Atau Baris (GAP), Angka `3` Berkorespondensi Dengan Spacing Unit Bootstrap.
    - `align-items-center` Secara Vertikal dan Deretan Pada Baris (*Flexbox*)
Kodenya:
```html
<div class="row align-items-center">
  <div class="col-12 col-md-4">...</div>
  <div class="col-12 col-md-8">...</div>
</div>

<div class="row g-3">
  <div class="col-12 col-md-4 col-lg-3">post</div>
  ...
</div>
```
---
4. **Utilities Untuk Pengurutan (`order-*`) Dan Responsive Order📐**
    - `order-1` Memberikan Urutan Visual (*Flex Order*) Pada Breakpoint Default.
    - `order-md-0` Menggantikan Nilai Order Pada Breakpoint `md` Set 0.
Kodenya:
```html
<div class="col-12 col-md-4 text-center order-1 order-md-0">...</div>
```
---
5. **🔽Button🔼**
    - `btn` Basisnya Style Tombol.
    - `btn-outline-light` Memberikan Garis Tepi (Border dan Teks) dan Background Transparant.
    - `btn-primary` Memberikan style Utama (*Primary*).
    - `w-100` Tombol Dengan Lebar Penuh (Ini Berguna Pada Mobile).
Kodenya:
```html
<button class="btn btn-outline-light w-100">Edit Profile</button>
<button class="btn btn-primary w-100">Follow</button>
```
---
6. **Nav Tabs🧭**
    - `nav` dan `nav-tabs` Memberikan Tampilan Tab.
    - `nav-item` dan `nav-link` Menstruktur Item Navigasi.
    - `active` Menandakan Tab Berada Aktif.
Kodenya:
```html
<ul class="nav nav-tabs justify-content-center">
  <li class="nav-item">
    <a class="nav-link active" href="#">Feed</a>
  </li>
</ul>
```
---
7. **Gambar Dan Utilitas Gambar🖼️**
    - `w-100` Membuat Gambar Selebar Kontainer Kolom.
    - `rounded` Membentuk Pada Sudut Sedikit Melengkung.
Kodenya:
```html
<img src="assets/Gambar 1.jpg" class="w-100 rounded" alt="Cat 1">
```
---
8. **Utility Posisi dan Overlay Hover⚙️**
    - `position-relative` Bagian *Parent* (Pembungkus Setiap Foto Feed Postingan)
    - `hover-text` Elemen Overlay Yang Muncul Ketika Di Arahkan Kursor Ke Gambar
Kodenya:
```html
<div class="post position-relative">
  <img ...>
  <div class="hover-text">Cat 1</div>
</div>
```
---
## Kekurangan Dan Kelebihan Bootstrap🔭
### Kelebihan
- 1. Banyak Komponen Siap Pakai.
- 2. Dapat menangani tampilan gambar dan responsivitas menggunakan aturan HTML dan CSS yang telah ditentukan.
### Kekurangan
- 1. Berisiko membuat website menjadi lebih lambat.
- 2. Gaya visual hampir selalu sama.
---
## Pertanyaan Dan Jawaban README 📝
1. Mengapa memilih konfigurasi col tertentu untuk tiap breakpoint?
- Jawab: Membuat konten terbaca di layar kecil, maksudnya dengan `col-12`, elemen tiap baris mengambil lebar penuh, sehingga lebih nyaman dibaca.
2. Bagaimana kamu memastikan tombol Follow/ Edit Profile tetap mudah dijangkau di mobile? Jelaskan pendekatannya.
- Jawab: Pada Pengguna Bootstrap seperti `btn btn-primary w-100 py-2` padding tombol tidak terlalu kecil. Memastikan tinggi dan lebar secara visual cukup besar.
3. Jika postingan bertambah jadi 50, apa potensi masalah dan bagaimana solusi gridmu mengatasinya?
- Jawab: Permasalahannya, 50 gambar yang diminta pada server menjadi ukuran total halaman (payload) yang besar dan juga banyak request *HTTP* bisa lambat terutama di koneksi seluler atau *device low-end*. Solusinya, Gunakan atribut `loading="lazy"` di `<img>` agar gambar di luar viewport tidak langsung dimuat dengan browser modern mendukung ini.
