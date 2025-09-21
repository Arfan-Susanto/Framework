# Instagram Cloning
Pada studi kasus membuat Instagram Cloning, saya memakai program:
- **HTML5🗒️**
- **Tailwind CSS🍃**
---
## Pengertian Tailwind CSS🍃 
Tailwind CSS merupakan sebuah framework *Cascading Style Sheet* yang digunakan untuk mengkustom atau mendesain user interface pada sebuah web. Framework ini berbasis utility yang hanya terdiri dari utility class dan tanpa utility komponen lainnya.
---
## Feature On Cloning Instagram ❔
- **Responsif pada website**
    - 📱 Mobile yang berukuran grid-cols-1 1 Foto 📷
    - 💻 Desktop yang berukuran grid-cols-3 3 Foto 📷
    - 📲 Tablet yang berukuran grid-cols-4 4 FOto 📷
- **Tema Terang pada website**
- **Button Edit Profile dan Follow**
- **Tata letak postingan mirip Instagram asli**
---
## Struktur Penempatan File + Cara menjalankan website
1. Pastikan penempatan file dan folder dengan benar. dalam folder `assets` berisikan gambar ekstensi jpeg dan jpg.
```
Proyek UI Cloning Instagram/
├── index.html
├── assets
    └── Gambar 1 sampai 12.jpg
    └── guest.jpeg
```
2. Selanjutnya, bisa dibuka file `index.html` dengan cara klik kiri dua kali, akan tertuju ke *Google Chrome*, *Opera*, ataupun *browser* lainnya.
---
## Penjelasan Desain 🧷
1. Bagian Navbar memiliki desain sederhana dengan logo instagram pada kiri atas yang bertujuan untuk memberikan identitas pada website ini
2. Profil User memiliki Avatar bulat, setting icon, status dan bio yang bertujuan menampilkan info utama profil.
3. Tombol pada (Edit Profile/View Archive) memiliki tombol horizontal pada desktop, dan vertikal pada mobile yang bertujuan memberikan interaksi utama bagi user untuk mengubah profile foto
4. Circle "New" memiliki desain lingkaran pada simbol + yang bertujuan menandakan tombol untuk menambahkan konten baru.
5. Tab Menu (Feed/Reels/Saved) memiliki desain tiga tombol horizontal untuk navigasi konten yang bertujuan untuk memudahkan user memilih kategori konten.
6. Grid Gallery memiliki 12 foto dengan overlay nama saat hover yang bertujuan menampilkan konten utama user dalam format visual grid dengan tertata rapi.
## Pertanyaan Reflektif 🔍
1. Bagaimana desain ini terlihat di layar kecil (mobile) dibandingkan desktop?
2. Apakah warna teks dan backgorund tidak membuat mata cepat lelah?
3. Elemen mana yang pertama kali menarik perhatian user? Apakah hierarchy ini sesuai dengan prioritas informasi? 
## Component Tailwind CSS🍃
1. **Navbar ↗️**
    - `border-b` bagian border bawah.
    - `bg-white` background putih.
    - `max-w-5xl` center container secara horizontal..
    - `px-4 py-3` set padding horizontal 4, vertikal 3.
    - `flex items-center` flex container dengan elemen center secara vertikal.
    - `h-8 w-auto` set tinggi logo 8 dan set auto lebar yang menjaga rasio.
Kodenya:
```html
<nav class="border-b bg-white">
  <div class="max-w-5xl mx-auto px-4 py-3 flex items-center">
    <a href="#" onclick="alert('Ini adalah tampilan website instagram')" class="flex items-center">
      <img src="https://upload.wikimedia.org/wikipedia/commons/9/95/Instagram_logo_2022.svg" 
           alt="Instagram" class="h-8 w-auto">
    </a>
  </div>
</nav>
```
---
2. **Header🗣️**
    - `flex flex-col sm:flex-row` layout kolom di mobile, row di sm.
    - `sm:items-start` align item start di sm.
    - `gap-6` jarak antar avatar dan info set 6.
    - `w-24 h-24 sm:w-32 sm:h-32` ukuran avatar responsif set tinggi 24, lebar 24, sm:lebar 32 dan sm:tinggi 32.
    - `rounded-full` Membentuk lingkaran.
    - `object-cover` gambar menutupi area, menjaga rasio.
    - `shadow-md` memberikan bayangan.
    - `flex-1` info mengambil sisa ruang.
    - `order-2 sm:order-1` avatar dan info berganti urutan di sm.
    - `text-xl`, `font-semibold`, `text-sm` mengatur ukuran font dan ketebalan..
    - `cursor-pointer` kursor berubah saat hover.
Kodenya:
```html
<div class="flex flex-col sm:flex-row sm:items-start gap-6">
  <img src="guest.jpeg" alt="Profile"
       class="w-24 h-24 sm:w-32 sm:h-32 rounded-full object-cover shadow-md">

  <div class="flex-1 order-2 sm:order-1">
    <div class="flex flex-col sm:flex-row sm:items-center sm:gap-3">
      <h2 class="text-xl font-semibold">Suka_Kucing</h2>
      <span class="text-xl cursor-pointer">⚙️</span>
    </div>
    <div class="flex gap-6 mt-2 text-sm">
      <span><strong>12</strong> Posts</span>
      <span><strong>100</strong> Followers</span>
      <span><strong>200</strong> Following</span>
    </div>
    <p class="mt-2 text-sm">Saya suka kucing semuanya 🐱</p>
  </div>
</div>

```
---
3. **Tombol Aksi (Edit Profile/View Archive)🔲**
    - `flex flex-col sm:flex-row` tombol vertikal di mobile, horizontal di sm.
    - `gap-3` jarak antar tombol set 3.
    - `justify-center sm:justify-start` center di mobile, start di sm.
    - `mt-4` margin top set 4.
    - `px-4 py-2` padding tombol set x = 4 dan y = 2.
    - `border rounded-md` border dan border-radius.
    - `text-sm font-medium` font kecil, medium.
    - `hover:bg-gray-100` efek hover.
    - `sm:w-auto w-full` full width mobile, auto di sm.
Kodenya:
```html
<div class="flex flex-col sm:flex-row gap-3 justify-center sm:justify-start mt-4">
  <button class="px-4 py-2 border rounded-md text-sm font-medium hover:bg-gray-100 sm:w-auto w-full" onclick="alert('Coming Soon!')">
    Edit Profile
  </button>
  <button class="px-4 py-2 border rounded-md text-sm font-medium hover:bg-gray-100 sm:w-auto w-full" onclick="alert('Coming Soon!')">
    View Archive
  </button>
</div>
```
---
4. **Circle "New"⭕**
    - `text-center` teks berada di tengah.
    - `mt-6` margin top set 6.
    - `w-20 h-20` ukuran kotak set lebar 20 dan tinggi 20.
    - `border-2 border-gray-400` border tebal 2px, warna abu.
    - `rounded-full` membentuk lingkaran.
    - `flex items-center justify-center` posisi plus di tengah dalam lingkaran.
    - `mx-auto` center horizontal.
    - `shadow` bayangan.
    - `text-3xl text-gray-600` ukuran dan warna font.
Kodenya:
```html
<div class="text-center mt-6">
  <div class="w-20 h-20 border-2 border-gray-400 rounded-full flex items-center justify-center mx-auto shadow">
    <span class="text-3xl text-gray-600">+</span>
  </div>
  <p class="text-sm mt-1">New</p>
</div>
```
---
5. **Tab Menu (Feed / Reels / Saved)📑**
    - `flex justify-center` container flex, center.
    - `border-t mt-6` border top, margin top set 6.
    - `px-6 py-3` padding tombol.
    - `text-sm font-medium` ukuran font kecil, medium.
    - `border-b-2 border-black` underline tab aktif.
    - `text-gray-500 hover:text-black` warna tab non-aktif, hover berubah warna.
Kodenya:
```html
<div class="flex justify-center border-t mt-6">
  <button class="px-6 py-3 text-sm font-medium border-b-2 border-black" onclick="alert('Ini adalah tampilan feed instagram')">Feed</button>
  <button class="px-6 py-3 text-sm font-medium text-gray-500 hover:text-black" onclick="alert('Coming Soon!')">Reels</button>
  <button class="px-6 py-3 text-sm font-medium text-gray-500 hover:text-black" onclick="alert('Coming Soon!')">Saved</button>
</div>
```
---
6. **Gallery Item🖼️ + Hover Overlay🏹**
    - `grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4` responsive grid.
    - `gap-1 mt-2` jarak grid, margin top.
    - `relative` parent posisi relatif.
    - `group` agar child bisa mendeteksi hover parent.
    - `col-span-1` item menempati 1 kolom.
    - `w-full` gambar penuh parent.
    - `aspect-[4/5]` rasio gambar 4:5.
    - `object-cover`cover area.
    - `absolute inset-0` overlay menutupi seluruh gambar set 0.
    - `flex items-center justify-center` teks overlay di tengah.
    - `bg-gray-200/70` background abu transparan.
    - `opacity-0 group-hover:opacity-100 transition` efek hover overlay muncul halus (karena ada *transition*).
    - `text-gray-700 font-semibold` style teks overlay.
Kodenya:
```html
<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-1 mt-2">
  <div class="relative group col-span-1">
    <img src="Gambar 1.jpg" class="w-full aspect-[4/5] object-cover">
    <div class="absolute inset-0 flex items-center justify-center bg-gray-200/70 opacity-0 group-hover:opacity-100 transition">
      <span class="text-gray-700 font-semibold">Cat 1</span>
    </div>
  </div>
  <!-- Gambar 2-12 sama, hanya berbeda src dan text -->
</div>
```
---
## Kekurangan Dan Kelebihan Bootstrap🔭
### Kelebihan
- 1. Pengembang dapat membangun UI dengan cepat karena adanya kelas-kelas utilitas yang sudah siap pakai untuk berbagai gaya.
- 2. Kelas utilitas yang terdefinisi mempromosikan penggunaan nilai desain yang konsisten di seluruh proyek, membantu menjaga harmonisasi tampilan.
### Kekurangan
- 1.  Berbeda dengan framework lain seperti Bootstrap, Tailwind tidak menyediakan komponen UI siap pakai seperti tombol atau modal, sehingga pengembang harus membangunnya sendiri menggunakan kelas utilitas.
- 2. Penggunaan banyak kelas utilitas dapat membuat kode HTML menjadi sangat panjang dan penuh, yang dapat mengurangi kebersihan dan keterbacaan kode.
---
## Pertanyaan Dan Jawaban README 📝

1. Jelaskan keputusan grid-cols/gap di tiap breakpoint — kenapa begitu?
Jawab: 
- `grid-cols-1` Mobile punya layar sempit. 1 kolom membuat setiap gambar terlihat jelas dan mudah di-klik/tap.
- `md:grid-cols-3` Tablet/layar menengah (≥768px). 3 kolom membuat grid terlihat rapi dan memanfaatkan ruang lebih baik.
- `lg:grid-cols-4` Desktop/laptop besar (≥1024px). 4 kolom memaksimalkan tampilan gambar sekaligus menjaga ukuran gambar tetap nyaman dilihat.
- `gap-1` memberi jarak minimal sehingga gambar tidak menempel dan menjaga grid rapi.

2. Bagaimana kamu memanfaatkan utility responsive Tailwind untuk memecahkan masalah layout yang muncul di mobile?
Jawab:
```html
<div class="flex flex-col sm:flex-row sm:items-start gap-6">
```
- Mobile: Solusi ini memudahkan scroll, elemen jelas, dan tidak menempel.
- Desktop: Solusi ini layout horizontal memanfaatkan lebar layar.
```html
<div class="flex flex-col sm:flex-row gap-3 justify-center sm:justify-start mt-4">
  <button class="px-4 py-2 border rounded-md text-sm font-medium hover:bg-gray-100 sm:w-auto w-full">Edit Profile</button>
  <button class="px-4 py-2 border rounded-md text-sm font-medium hover:bg-gray-100 sm:w-auto w-full">View Archive</button>
</div>
```
- Solusi ini tombol tetap mudah dijangkau di mobile, estetika tetap terjaga di desktop
``html
<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-1 mt-2">
```
- Solusi ini, gambar tetap terlihat jelas, layout tidak kacau saat resize.
```html
<h2 class="text-xl font-semibold">Suka_Kucing</h2>
<img class="w-24 h-24 sm:w-32 sm:h-32 rounded-full object-cover shadow-md">
```
- Solusi ini Teks dan gambar proporsional di semua device.

3. Jelaskan trade-off antara memakai banyak utility classes vs membuat component CSS tersendiri!
Jawab:
- Keuntungan Trade-off memakai banyak utitlity classes.
1. Mempercepat proses styling tanpa menulis CSS tambahan.
2. Menggunakan breakpoint seperti sm:, md:, lg: untuk membuat desain responsif tanpa menulis media queries secara manual.
- Kekurangan Trade-off memakai banyak utitlity classes.
1. HTML dapat menjadi panjang dan sulit dibaca karena banyaknya kelas utility
2. Memerlukan pemahaman mendalam tentang kelas-kelas Tailwind.
- Keuntungan membuat component CSS tersendiri.
1. HTML lebih bersih dan mudah dibaca tanpa banyak kelas utility
2. Memisahkan struktur dan presentasi, meningkatkan keterbacaan kode
- Kerugian membuat component CSS tersendiri.
1. Memerlukan waktu lebih untuk menulis dan memelihara CSS.
2. Tanpa sistem seperti Tailwind, konsistensi desain bisa sulit dijaga.