# Pengendalian Bahan Baku FnB

Sistem pengendalian dan pengawasan bahan baku yang dirancang khusus untuk mengotomatisasi pencatatan sirkulasi bahan baku bisnis Food and Beverage (FnB), meminimalkan selisih stok fisik, serta menghadirkan transparansi arus keluar-masuk bahan baku secara real-time bagi manajemen.

## Disclaimer Privasi

*Catatan:* Repositori ini murni menampilkan dokumentasi perancangan sistem dan analisis bisnis. Seluruh *source code*, konfigurasi server, serta kunci API tidak disematkan untuk mematuhi kebijakan privasi, hak kekayaan intelektual, serta perjanjian kerahasiaan dengan pihak mitra terkait.

## Latar Belakang & Analisa Masalah

- Profil Studi Kasus: **Kafe Momentum Kopi** adalah bisnis Food and Beverage (FnB) yang menyajikan produk minuman berbasis kopi, susu, serta makanan (seperti ramen dan kentang goreng) dengan mobilitas perputaran bahan baku yang cepat dan tinggi.

- Pain Points:
1. **Pengelolaan Konvensional:** Pengelolaan inventaris bahan baku masih mengandalkan pencatatan manual pada formulir atau laporan kertas, yang rentan terhadap keterlambatan informasi ketersediaan bahan baku.
2. **Selisih Stok:** Sering terjadi selisih antara jumlah fisik bahan baku di gudang dengan pencatatan pembukuan utama akibat lemahnya kontrol sirkulasi.
3. **Risiko Human Error & Lemahnya Pengawasan:** Kesalahan pencatatan akibat volume transaksi tinggi serta kesulitan pemilik (*Owner*) dalam memantau arus keluar-masuk bahan secara *real-time*.

## Panduan

Dokumen ini disusun secara sistematis untuk menunjukkan alur kerja dan analisis bisnis menjadi spesifikasi teknis serta perancangan sistem. Dokumen ini dapat ditelusuri melalui urutan alur berikut :

1. Business Requirements Document (BRD): Meninjau batasan ruang lingkup proyek, objektif bisnis, aktor sistem, dan aturan main pengendalian inventaris. [BRD](BRD.txt)
2. Functional Requirement Document (FRD): Menilai daftar kebutuhan fungsional (FR) dan parameter non-fungsional (NFR) untuk spesifikasi perangkat lunak. [FRD](FRD.txt)
3. Pemodelan Sistem (System Modeling): Mempelajari perancangan alur proses (*Flowchart*), batasan sistem (*Diagram Konteks*), dekomposisi aliran data (*DFD Level 1*), hingga struktur basis data relasional (*ERD*). [system modeling](system-modeling.txt)

## Fitur Utama

- **Manajemen Stok:** Fitur tambah, ubah, dan hapus data barang secara terpusat untuk mengatasi keterlambatan informasi serta kesalahan input data manual.
- **Pencatatan Transaksi:** Log otomatis untuk barang masuk dari *supplier* dan barang keluar untuk produksi guna menghilangkan selisih stok (*discrepancy*).
- **Notifikasi Stok Menipis:** Peringatan otomatis jika kuantitas barang berada di bawah batas minimum agar pengadaan dapat dilakukan tepat waktu.
- **Laporan Bulanan & Data Stok:** Ekspor data laporan log pergerakan maupun inventaris stok secara berkala ke format PDF dan Excel untuk memudahkan audit oleh pemilik.
- **Manajemen Pengguna (RBAC):** Pembagian hak akses terstruktur antara Admin, Petugas Gudang (Head Bar), dan Superadmin (Owner) guna memperkuat sistem pengawasan.
