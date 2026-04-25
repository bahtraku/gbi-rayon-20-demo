# GBI My Home Rayon 20 Prototype
Prototype website statis untuk profil dan distribusi cabang `GBI My Home Rayon 20`, lengkap dengan halaman branch dinamis, detail gereja, dan template admin panel.

## Demo
- Demo Repository: https://github.com/bahtraku/gbi-rayon-20-demo
- LIVE Demo: https://bahtraku.github.io/gbi-rayon-20-demo/

## Ringkasan Fitur
### 1) Website Utama (`index.html`)
- Desain responsif dengan navigasi desktop/mobile.
- Mega menu cabang (dinamis berdasarkan provinsi dari data JSON).
- Integrasi Google Translate custom dropdown (tanpa bar Google di atas halaman).
- Section utama: Hero, Profil, Jadwal, Pelayanan, Event, Persembahan, Distribusi Cabang.
- Galeri video YouTube (4 embed) + link ke channel video lengkap.
- Section musik, kampus masa depan, dan konten pelayanan pendukung.
- Tombol `Back to Top` dengan smooth scroll.
- Modal disclaimer otomatis saat halaman dimuat.
- Footer konsisten dengan format:
  - kiri: copyright
  - kanan: `Powered by Bahtraku.org | Login Admin`

### 2) Website Cabang (`branches.html`)
- Halaman branch dinamis via query parameter `?id=...`.
- Konten hero, profil, jadwal, donasi mengikuti data cabang.
- Mega menu cabang per provinsi (dinamis dari JSON).
- Integrasi translate yang sama dengan halaman utama.
- Animasi pemilihan item navigasi.
- Section galeri gambar (4 kolom x 2 baris).
- Distribusi cabang berbasis peta.
- Tombol `Back to Top` dengan smooth scroll.
- Modal disclaimer otomatis saat halaman dimuat.
- Footer konsisten dengan halaman utama.

### 3) Peta Distribusi Cabang (Leaflet + OSM)
- Menggunakan OpenStreetMap + Leaflet.js.
- Data marker diambil dari `data/gereja.json`.
- Default area Indonesia, auto-fit bounds dari data marker.
- Tiap marker memiliki:
  - label nama gereja (tooltip),
  - popup profil singkat,
  - gambar,
  - link ke halaman detail.

### 4) Halaman Detail Gereja (`gereja-detail.html`)
- Mengambil data gereja berdasarkan query parameter `id`.
- Menampilkan ringkasan profil cabang.
- Tautan aksi ke halaman website cabang terkait.

### 5) Admin Panel (Template)
- `admin-login.html` (form login template, default value simulasi).
- `admin-dashboard.html` (ringkasan statistik dan quick action).
- `admin-database-gereja.html`:
  - tabel data gereja,
  - search + filter provinsi + filter status (live filtering),
  - shortcut ke halaman simulasi CRUD.
- `admin-crud-gereja.html`:
  - form simulasi tambah/edit data,
  - modal konfirmasi simpan,
  - modal konfirmasi hapus,
  - notifikasi hasil aksi simulasi.
- Semua halaman admin menggunakan branding judul `Admin Panel`.

## Data Contoh
- Sumber: `data/gereja.json`
- Berisi 10 contoh data cabang (nama, kota, alamat, koordinat, profil singkat, gambar).

## Teknologi
- HTML5
- Tailwind CSS (CDN)
- JavaScript (Vanilla JS)
- Alpine.js
- Leaflet.js + OpenStreetMap
- Font Awesome
- Google Fonts

## Struktur File Utama
- `index.html` — halaman utama
- `branches.html` — halaman website cabang
- `gereja-detail.html` — halaman detail profil gereja
- `admin-login.html` — login admin (template)
- `admin-dashboard.html` — dashboard admin (template)
- `admin-database-gereja.html` — data gereja + search/filter
- `admin-crud-gereja.html` — simulasi CRUD + modal konfirmasi
- `data/gereja.json` — data contoh cabang gereja

## Menjalankan Project
Karena ini website statis, Anda bisa:
- Membuka `index.html` langsung di browser, atau
- Menjalankan via local static server (disarankan agar proses `fetch` JSON berjalan normal).

## Catatan
- Fitur admin pada project ini bersifat template/simulasi UI (belum terhubung backend/database asli).

## Author
- Bahtraku

## Web Developer
- Janzen Faidiban (082199558191)
- janzenfaidiban.github.io
