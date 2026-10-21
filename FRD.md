# Functional Requirement

| ID | MODUL/FITUR | PERILAKU SISTEM |
| :--- | :--- | :--- |
| FR-01 | Autentikasi Login | Sistem menyediakan halaman autentikasi terpusat untuk memvalidasi *username*, *password*, dan mendeteksi hak akses (*Role-Based Access Control* / RBAC) bagi Superadmin, Admin, dan Petugas sebelum mengarahkan ke *dashboard* masing-masing. |
| FR-02 | Manajemen Pengguna | Superadmin memiliki kewenangan penuh untuk melakukan penambahan, pembaruan, verifikasi, serta pengaturan status aktif akun untuk level Admin dan Petugas. |
| FR-03 | Manajemen Data Master | Admin dapat melakukan operasi CRUD (*Create, Read, Update, Delete*) pada data master yang mencakup: Data Supplier, Data Bahan Baku, Kategori Bahan, dan Satuan Bahan. |
| FR-04 | Pencatatan Bahan Masuk | Admin dapat mencatat transaksi penerimaan bahan dari supplier dengan mengisi formulir lengkap yang mencakup: ID Transaksi, Pemilihan Bahan, Pemilihan Supplier, Nama Pengirim, Jumlah, Satuan, dan Tanggal Masuk. |
| FR-05 | Pencatatan Bahan Keluar | Petugas (*Head Bar*) dapat mencatat transaksi pengeluaran bahan untuk keperluan produksi dengan mengisi formulir: ID Transaksi, Pemilihan Bahan, Jumlah Keluar, Satuan, dan Tujuan Penggunaan (*target produksi/divisi*). |
| FR-06 | Log & Audit Stok Otomatis | Sistem secara otomatis merekam setiap perubahan inventaris ke dalam tabel log (`log_bahan_masuk` dan `log_bahan_keluar`) sebagai riwayat audit transparan yang dapat dipantau oleh Superadmin. |
| FR-07 | Unduh & Ekspor Laporan | Sistem menyediakan fitur filter rentang tanggal dan tombol unduh/ekspor laporan data bahan masuk, bahan keluar, serta rekapitulasi stok akhir dalam format standar (*PDF/Excel*). |

# Non-Functional Requirement

| ID | KATEGORI | PARAMETER KEBUTUHAN NON-FUNGSIONAL |
| :--- | :--- | :--- |
| NFR-01 | Usability (Kegunaan) | Antarmuka pengguna (*user interface*) dirancang intuitif dan responsif sehingga mudah dioperasikan oleh staf kafe/operasional tanpa memerlukan pelatihan teknis tingkat lanjut. |
| NFR-02 | Performance (Performa) | Waktu muat halaman (*page load time*) dan pemrosesan transaksi (penyimpanan data atau pengunduhan laporan) rata-rata di bawah 2 detik dalam kondisi jaringan standar/lokal. |
| NFR-03 | Security (Keamanan) | Penerapan *Role-Based Access Control* (RBAC) yang ketat; perlindungan terhadap sesi pengguna (*Session Management*) serta pencegahan akses URL langsung tanpa melalui proses login yang sah. |
| NFR-04 | Compatibility (Kompatibilitas) | Sistem harus kompatibel dan dapat diakses dengan baik melalui berbagai peramban web modern (*Google Chrome, Mozilla Firefox, Microsoft Edge, Safari*) pada perangkat desktop maupun seluler (*mobile*). |
| NFR-05 | Reliability & Availability (Keandalan & Ketersediaan) | Basis data harus dirancang terstruktur dengan menerapkan batasan relasional (*Foreign Key Constraints* pada MySQL) untuk mencegah duplikasi data, anomali data yatim (*orphan records*), serta memastikan integritas stok tetap terjaga secara konsisten. |
