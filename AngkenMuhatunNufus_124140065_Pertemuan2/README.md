# Personal Dashboard

Personal Dashboard adalah aplikasi berbasis HTML, CSS, dan JavaScript yang dibuat untuk membantu mahasiswa mengatur tugas kuliah, jadwal kelas, dan catatan. Aplikasi ini juga menampilkan informasi cuaca dan kutipan harian.

Aplikasi ini tidak menggunakan framework atau build tool. Untuk menjalankannya, cukup buka file `index.html` melalui browser.

## Fitur

### Tugas Kuliah

- Menambah, mengedit, menghapus, dan menandai tugas sebagai selesai.
- Menyimpan judul tugas, mata kuliah, prioritas, dan tenggat waktu.
- Menampilkan informasi tenggat, termasuk tugas yang terlambat.
- Mencari, memfilter, dan mengurutkan daftar tugas.
- Menampilkan jumlah tugas dan progres penyelesaian.

### Jadwal Kuliah

- Menambah, mengedit, dan menghapus jadwal kuliah.
- Menyimpan mata kuliah, hari, jam, ruang, dan nama dosen.
- Mengelompokkan jadwal berdasarkan hari.
- Menandai jadwal kuliah pada hari ini.
- Memeriksa agar jam selesai tidak lebih awal dari jam mulai.

### Catatan

- Membuat, mengedit, dan menghapus catatan.
- Menampilkan catatan dari yang terbaru.

### Cuaca dan Kutipan

- Mengambil informasi cuaca dari Open-Meteo.
- Mengambil kutipan harian dari DummyJSON.
- Menyimpan hasil cuaca sementara agar masih dapat ditampilkan ketika koneksi bermasalah.

### Pengaturan dan Penyimpanan

- Menyediakan tema gelap dan terang.
- Menampilkan jam, tanggal, dan sapaan sesuai waktu.
- Menyimpan data menggunakan `localStorage`.
- Menyediakan fitur ekspor dan impor data dalam format JSON.
- Menyediakan opsi untuk mengatur ulang data.
- Mendukung tampilan desktop, tablet, dan ponsel.

## Cara Menjalankan

Cara paling sederhana adalah membuka file `index.html` di browser.

Untuk menjalankan melalui server lokal, buka terminal di folder proyek dan jalankan perintah berikut:

```
python -m http.server 5500
```

Kemudian buka alamat `http://localhost:5500` di browser.

Alternatifnya, kamu bisa menggunakan ekstensi Live Server di Visual Studio Code.

## Data Awal

Saat pertama kali dibuka, aplikasi menyediakan beberapa data contoh, yaitu:

- Tiga tugas kuliah.
- Sembilan jadwal kuliah.
- Dua catatan.

Data tersebut dapat diubah atau dihapus melalui aplikasi. Gunakan fitur ekspor untuk menyimpan salinan data sebelum berpindah browser atau perangkat, karena data disimpan secara lokal di browser yang digunakan.

## Struktur Folder

```
Jarkom Minggu3/
├── index.html
├── css/
│   └── styles.css
├── js/
│   ├── utils.js
│   ├── models.js
│   ├── storage.js
│   ├── api.js
│   └── app.js
├── docs/
└── README.md
```

Keterangan file:

- `index.html` berisi struktur halaman.
- `css/styles.css` mengatur tampilan aplikasi.
- `js/utils.js` berisi fungsi-fungsi bantu.
- `js/models.js` berisi model untuk tugas, catatan, dan jadwal.
- `js/storage.js` mengatur penyimpanan data di browser.
- `js/api.js` menangani permintaan ke layanan cuaca dan kutipan.
- `js/app.js` mengatur interaksi dan tampilan aplikasi.
- `docs/` digunakan untuk menyimpan screenshot jika diperlukan.

File JavaScript dimuat secara berurutan menggunakan `defer`, yaitu `utils.js`, `models.js`, `storage.js`, `api.js`, lalu `app.js`.

## Teknologi yang Digunakan

- HTML untuk struktur halaman.
- CSS untuk tampilan dan tata letak.
- JavaScript ES6+ untuk logika dan interaksi.
- `localStorage` untuk menyimpan data.
- Open-Meteo untuk informasi cuaca.
- DummyJSON untuk kutipan harian.

## Fitur JavaScript yang Digunakan

Beberapa fitur JavaScript yang digunakan dalam proyek ini:

- `let` dan `const`.
- Arrow function.
- Template literals.
- Class dan inheritance.
- `async`/`await` dan Promise.
- Destructuring.
- Spread dan rest operator.
- Default parameter.
- Optional chaining dan nullish coalescing.
- Method array seperti `map`, `filter`, `find`, dan `sort`.
- `fetch` dan `AbortController`.
- `localStorage`.
- Elemen `<dialog>` untuk formulir modal.
- Event delegation.

## API yang Digunakan

Aplikasi ini menggunakan dua API publik.

Open-Meteo digunakan untuk mengambil informasi cuaca berdasarkan koordinat yang diatur dalam file `js/api.js`.

DummyJSON digunakan untuk mengambil kutipan secara acak.

Kedua layanan tersebut dapat digunakan tanpa API key. Jika permintaan gagal, aplikasi tetap dapat digunakan untuk mengelola tugas, jadwal, dan catatan.

## Penyimpanan Data

Data tugas, jadwal, catatan, profil, pengaturan, dan cache cuaca disimpan di browser menggunakan `localStorage`. Perubahan data akan disimpan ketika pengguna melakukan tindakan di aplikasi.

Data tidak otomatis berpindah ke browser atau perangkat lain. Untuk memindahkannya, gunakan fitur ekspor dan impor JSON.

Fitur reset dapat digunakan untuk menghapus data aplikasi yang tersimpan.

## Pengembangan Selanjutnya

Beberapa fitur yang dapat ditambahkan ke aplikasi ini antara lain pengingat tenggat waktu, tampilan kalender bulanan, pencarian untuk seluruh bagian aplikasi, dan sinkronisasi data melalui backend.

## Pembuat

Dibuat oleh Angken untuk tugas praktikum HTML, CSS, dan JavaScript ES6+.
