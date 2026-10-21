# Business Requirement Document (BRD)

## Sistem Pengendalian Bahan Baku FnB

---

## Business Background
Operasional bisnis di sektor Food and Beverage (FnB) yang menyediakan variasi produk minuman (seperti kopi dan susu) serta makanan (seperti ramen dan kentang goreng) menuntut kecepatan serta ketepatan pengelolaan bahan baku. Saat ini, proses pencatatan stok dan sirkulasi bahan baku masih dilakukan secara konvensional (menggunakan buku besar atau formulir kertas), yang rentan terhadap keterlambatan informasi ketersediaan bahan dan menghambat pengambilan keputusan operasional.

## Problem Statement

- **Ketidakakuratan Data Stok:** Sering terjadi selisih antara jumlah fisik bahan baku di gudang/penyimpanan (storage) dengan pencatatan pembukuan utama.
- **Risiko Human Error:** Tingginya volume transaksi harian serta kelelahan operasional memicu kesalahan pencatatan manual pada buku besar.
- **Kurangnya Transparansi Pengawasan:** Pemilik (Owner / Superadmin) kesulitan melakukan pemantauan secara real-time terhadap arus keluar-masuk bahan baku untuk mencegah potensi selisih maupun pemborosan.

## Project Objectives
- Mengembangkan aplikasi berbasis web yang fleksibel untuk mengotomatisasi pencatatan sirkulasi bahan baku sektor FnB.
- Meningkatkan akurasi, efisiensi, dan transparansi dalam manajemen inventaris harian.
- Meminimalkan risiko human error dan mencegah selisih inventaris melalui validasi sistem stok otomatis.

## Project Scope

### In-Scope
- Pengelolaan data master dasar (Kategori Bahan, Satuan Bahan, Data Bahan Baku, dan Data Supplier).
- Penentuan struktur basis data relasional untuk mendukung transaksi harian.

### Out-of-Scope
- Integrasi POS eksternal di luar modul inventaris internal.

## Business Process Flow

- **Proses Saat Ini (As-Is):** Mengandalkan pencatatan manual menggunakan hardfile atau buku besar, sehingga rekapitulasi inventaris memakan waktu lama dan rawan kesalahan.
- **Proses Usulan (To-Be):** Seluruh pendataan master bahan baku dikelola secara digital, terpusat, dan terstruktur dalam database aplikasi web.
