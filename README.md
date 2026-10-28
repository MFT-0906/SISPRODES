# Website Profil dan Informasi Desa Marga Agung

Website profil dan informasi Desa Marga Agung: profil desa, transparansi APBDes, potensi pertanian dan UMKM, berita dan agenda, serta ruang aspirasi warga, dilengkapi dashboard admin bagi perangkat desa.

**Status:** tahap perencanaan (SKPL). Proyek Laravel sudah dibuat, fitur belum dikembangkan.

## Teknologi

| Komponen | Spesifikasi |
|---|---|
| Backend | PHP 8.3+ dan Laravel 13 |
| Basis data | MySQL / MariaDB |
| Frontend | HTML5, CSS, JavaScript dengan Tailwind CSS |
| Web server | Apache / Nginx |
| Versi kode | Git |

## Kebutuhan Fungsional

### Modul Publik
| ID | Fitur | Keterangan |
|---|---|---|
| FR-01 | Beranda | Berita terbaru, jumlah penduduk, potensi unggulan, tautan APBDes |
| FR-02 | Profil Desa | Sejarah, visi dan misi, struktur organisasi, letak geografis |
| FR-03 | Transparansi APBDes | Ringkasan pendapatan dan belanja (tabel/diagram) serta unduhan PDF per tahun |
| FR-04 | Potensi Desa | Katalog pertanian dan UMKM beserta kontak WhatsApp |
| FR-05 | Berita dan Agenda | Daftar, detail berita, dan agenda mendatang |
| FR-06 | Ruang Aspirasi | Formulir pertanyaan, keluhan, dan saran (NIK opsional) |

### Modul Admin
| ID | Fitur | Keterangan |
|---|---|---|
| FR-07 | Autentikasi Admin | Login dengan email/username dan kata sandi |
| FR-08 | Manajemen Profil | Sejarah, visi dan misi, struktur organisasi |
| FR-09 | Manajemen APBDes | Unggah PDF, pilih tahun, input ringkasan |
| FR-10 | Potensi dan UMKM | CRUD kelompok tani, komoditas, UMKM |
| FR-11 | Berita dan Agenda | CRUD dengan status draf/terbit |
| FR-12 | Manajemen Aspirasi | Ubah status ("Sudah Dibaca" / "Selesai") dan balasan |

Peran pengguna: **Super Admin** dan **Staf**.

## Kebutuhan Non-Fungsional

| ID | Aspek | Target |
|---|---|---|
| NFR-01 | Kinerja | Halaman utama termuat < 3 detik pada kondisi uji yang ditetapkan |
| NFR-02 | Keamanan | Password di-hash (bcrypt/Argon2), validasi input, perlindungan SQL injection dan XSS, batas percobaan login |
| NFR-03 | Kontrol akses | Hak akses berdasarkan peran (Super Admin, Staf) |
| NFR-04 | Kegunaan | Responsif (mobile-first), bahasa Indonesia baku, teks dasar 14 px |
| NFR-05 | Ketersediaan | Uptime minimal 99% per bulan |
| NFR-06 | Kompatibilitas | Peramban modern, desktop dan smartphone |
| NFR-07 | Pemeliharaan | Pencadangan database dan dokumen secara berkala |

## Kebutuhan Data

| ID | Data | Penanggung jawab |
|---|---|---|
| DR-01 | Profil desa | Pemerintah desa |
| DR-02 | Keuangan (APBDes PDF minimal 2 tahun terakhir dan angka ringkasan) | Pemerintah desa / keuangan |
| DR-03 | Potensi pertanian | Kelompok tani / perangkat desa |
| DR-04 | UMKM (target awal minimal 10 usaha) | Pelaku UMKM / perangkat desa |
| DR-05 | Berita dan agenda | Perangkat desa |
| DR-06 | Aspirasi | Warga dan petugas pengelola |
| DR-07 | Kontak dan lokasi | Pemerintah desa |

## Catatan

- NIK pada formulir aspirasi bersifat opsional dan sebaiknya tidak dikumpulkan kecuali benar-benar diperlukan.
- Unggahan PDF dan gambar divalidasi tipe dan ukurannya.
- Pihak yang berwenang menyetujui publikasi (APBDes, profil, foto perangkat desa, kontak UMKM, balasan aspirasi) perlu dikonfirmasi sebelum pengembangan.

## Tim

| Nama | Peran |
|---|---|
| Baginda | UI/UX Designer |
| Bayu | Backend Developer |
| Faathir | Frontend Developer |
| Angelica | Software Tester |
