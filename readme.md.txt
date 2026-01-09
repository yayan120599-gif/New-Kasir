☕ Nara Coffee POS

Nara Coffee POS adalah aplikasi Kasir (Point of Sales) berbasis web yang dirancang dengan arsitektur Single File Application. Aplikasi ini sangat ringan, responsif (Mobile-First), dan dapat berjalan secara offline tanpa memerlukan backend server yang kompleks.

Aplikasi ini dioptimalkan untuk penggunaan pada perangkat mobile (iPad/Tablet Android) dengan dukungan untuk pencetakan struk thermal dan manajemen stok sederhana.

✨ Fitur Utama

1. 📱 Antarmuka Pengguna (UI/UX)

Mobile First Design: Tampilan responsif yang menyesuaikan layar HP/Tablet.

Touch Friendly: Tombol dan interaksi dioptimalkan untuk layar sentuh.

PWA Ready: Mendukung "Add to Home Screen" di iOS dan Android (Manifest terintegrasi).

2. 🏪 Transaksi & Kasir

Manajemen Menu: Tampilan grid menu dengan indikator stok.

Keranjang Belanja: Tambah/kurang item dengan perhitungan real-time.

Pembayaran: Input nominal tunai, tombol uang pas, dan perhitungan kembalian otomatis.

Indikator Stok: Peringatan visual jika stok menipis atau habis ("SOLD OUT").

3. 🖨️ Pencetakan Struk (Thermal Printer)

Dukungan Printer Bluetooth/USB: Menggunakan fitur window.print() browser yang dikustomisasi.

Ukuran Kertas Dinamis: Dapat memilih ukuran kertas:

58mm (Standard Struk)

57mm

80mm (Printer Besar)

Reprint: Kemampuan mencetak ulang struk dari riwayat transaksi.

4. 📊 Manajemen & Laporan

Manajemen Stok: Edit jumlah stok barang secara langsung.

Riwayat Transaksi: Melihat daftar transaksi yang tersimpan.

Laporan Harian:

Filter berdasarkan tanggal.

Perhitungan Omzet Kotor (Bruto).

Perhitungan PPN (11%).

Perhitungan Pendapatan Bersih (Netto).

Export Excel: Unduh laporan penjualan ke format .xlsx dengan styling otomatis.

5. 💾 Penyimpanan Data

Local Storage: Semua data (menu, stok, riwayat) tersimpan di browser pengguna.

Backup & Restore: Fitur untuk mengunduh data (JSON) sebagai cadangan.

🛠️ Teknologi yang Digunakan

Aplikasi ini dibangun tanpa framework berat, menjadikannya sangat cepat dan mudah dimodifikasi.

HTML5 & CSS3: Struktur utama aplikasi.

Tailwind CSS (CDN): Untuk styling antarmuka yang modern dan cepat.

Vanilla JavaScript: Logika aplikasi (tanpa jQuery atau React/Vue).

FontAwesome 6: Ikon antarmuka.

SheetJS (xlsx-js-style): Library untuk generate dan export file Excel.

LocalStorage API: Database sisi klien.

🚀 Cara Penggunaan

Instalasi

Tidak perlu instalasi khusus. Karena ini adalah Single File Application:

Download file index.html.

Buka file tersebut menggunakan browser modern (Chrome, Safari, Edge).

Login Default

Berdasarkan kode sumber, sistem menggunakan kredensial login sederhana (Base64 encoded):

Role

Username

Password

Admin

Administration

Administration123

Menjalankan sebagai Aplikasi (PWA)

Untuk pengalaman terbaik layaknya aplikasi native:

iOS (Safari): Buka web -> Klik tombol Share -> Pilih "Add to Home Screen".

Android (Chrome): Buka web -> Klik menu titik tiga -> Pilih "Install App" atau "Add to Home Screen".

🖨️ Panduan Mencetak Struk

Aplikasi ini menggunakan CSS Media Query @media print untuk mengatur tampilan cetak.

Lakukan transaksi.

Pada halaman pratinjau struk, pilih ukuran kertas yang sesuai dengan printer Anda (Default: 58mm).

Klik tombol Cetak.

Jendela print browser akan muncul. Pastikan:

Printer termal sudah terpilih.

Margin diset ke None atau Minimum.

Scale diset ke 100%.

⚠️ Catatan Penting

Penyimpanan Data: Karena menggunakan localStorage, data akan hilang jika Anda melakukan "Clear Cache/Data" pada browser. Sangat disarankan untuk melakukan backup data (Klik tombol "Simpan" di menu header) secara berkala.

Keamanan: Sistem login hanya validasi sisi klien (client-side). Sangat aman untuk penggunaan offline/lokal, tetapi tidak disarankan untuk di-hosting di internet publik tanpa perlindungan tambahan jika data bersifat sensitif.

📝 Lisensi

Copyright © Nara Coffee.