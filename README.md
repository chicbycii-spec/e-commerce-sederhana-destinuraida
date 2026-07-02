# ChicByCii — Your Daily Outfit Goals

Landing page e-commerce fashion satu halaman (single-page) untuk brand **ChicByCii**, lengkap dengan katalog produk, keranjang belanja, dan alur checkout — dibangun murni dengan HTML, CSS, dan JavaScript vanilla (tanpa framework/build tool).

## ✨ Fitur

- **Navbar sticky** dengan pencarian produk dan ikon keranjang (badge jumlah item).
- **Hero section** dengan statistik brand (outfit terkirim, rating, item baru per bulan).
- **Katalog produk** dengan:
  - Filter berdasarkan kategori (atasan, bawahan, dress, outer, dll).
  - Pengurutan berdasarkan harga.
  - Pencarian produk secara global.
  - Badge produk (`sale`, `bestseller`, `new`).
- **Keranjang belanja (cart sidebar)**:
  - Tambah, kurangi, dan hapus item.
  - Perhitungan subtotal otomatis.
  - Ongkos kirim otomatis menjadi **gratis** untuk belanja ≥ Rp200.000.
  - Data keranjang **persisten** menggunakan `localStorage`.
- **Modal checkout**:
  - Form data pengiriman dengan validasi (nama, email, no. WhatsApp, alamat, dll).
  - Pilihan metode pembayaran (Transfer Bank, QRIS, GoPay, OVO, DANA, COD).
  - Ringkasan pesanan otomatis (termasuk info gratis ongkir).
  - Simulasi proses pembayaran dan nomor pesanan acak setelah submit.
- **Section testimoni** pelanggan.
- **Section "Kenapa Pilih Kami"** (value proposition brand).
- **Footer** dengan informasi kontak.
- **Responsive design** — mendukung tampilan desktop dan mobile (termasuk menu hamburger).
- Terintegrasi dummy **Google Analytics** untuk pelacakan metrik (bounce rate, conversion rate, dsb).

## 🛠️ Teknologi

- **HTML5** — struktur halaman.
- **CSS3** — custom design tokens (warna, tipografi) menggunakan CSS variables, tanpa framework CSS.
- **JavaScript (Vanilla)** — seluruh logika interaktif (filter, cart, checkout, validasi form).
- **Google Fonts** — `Playfair Display` (display/heading) & `Inter` (body text).
- **localStorage** — penyimpanan data keranjang di sisi klien.

Tidak ada dependency eksternal maupun proses build — cukup satu file `index.html` yang mandiri (self-contained), termasuk gambar produk yang di-embed sebagai base64.

## 📁 Struktur Proyek

```
.
├── index.html   # Seluruh markup, styling (CSS), dan logic (JS) dalam satu file
└── README.md
```

## 🚀 Cara Menjalankan

Karena tidak ada dependency atau proses build, cukup buka file secara langsung di browser:

1. Clone atau unduh repository ini.
2. Buka file `index.html` dengan browser (double click, atau drag-drop ke browser).

Atau jalankan dengan local server sederhana (opsional, disarankan agar `localStorage` bekerja konsisten):

```bash
# Menggunakan Python
python3 -m http.server 8000

# Menggunakan Node.js (http-server)
npx http-server .
```

Lalu buka `http://localhost:8000` di browser.

## 🛒 Konfigurasi Bisnis

Beberapa parameter bisnis diatur langsung di dalam script pada `index.html`:

| Parameter | Nilai | Keterangan |
|---|---|---|
| `SHIPPING_COST` | Rp15.000 | Ongkos kirim standar |
| `FREE_SHIPPING_THRESHOLD` | Rp200.000 | Minimal belanja untuk gratis ongkir |

Data produk (nama, kategori, harga, gambar, deskripsi, badge) juga didefinisikan langsung di dalam array `products` pada bagian script.

## ⚠️ Catatan

- Halaman ini adalah **prototipe front-end**. Proses checkout dan pembayaran hanya **simulasi** (tidak terhubung ke payment gateway atau backend sungguhan).
- Snippet Google Analytics yang disertakan bersifat **dummy** (ID placeholder) dan perlu diganti dengan ID GA yang valid untuk penggunaan produksi.
- Untuk penggunaan produksi, disarankan untuk memisahkan HTML/CSS/JS ke file terpisah dan menghubungkan form checkout ke backend/payment gateway sungguhan.

## 📄 Lisensi

Belum ditentukan — tambahkan lisensi sesuai kebutuhan proyek Anda.
