# Analisis Wisatawan Mancanegara ke Bali 2025

## Identitas
- **Nama:** Maria Indriani Lelu
- **NIM:** 2501010335
- **Kelas:** F

## Deskripsi Proyek
Proyek ini menganalisis kunjungan wisatawan mancanegara ke Bali selama Januari - Desember 2025, berdasarkan total kunjungan dari BPS Provinsi Bali dan distribusinya per negara asal.

## Struktur Folder
- `data/raw/download.csv` : Data utama wisatawan mancanegara
- `data/raw/data_cuaca.csv` : Data cuaca harian Bali dari Open-Meteo
- `data/raw/data_tempat_wisata.csv` : Daftar tempat wisata di Bali
- `catatan_provenance.csv` : Daftar sumber data
- `Proses/` : Catatan proses cleaning dan analisis

## Isi Data Utama (download.csv)
File ini berisi 132 baris data (12 bulan x 11 kategori negara).

Kolom:
- `tahun` : 2025
- `bulan` : 1-12 (Januari - Desember)
- `negara_asal` : Australia, India, China, Singapura, Korea Selatan, Inggris, Prancis, Amerika Serikat, Malaysia, Jepang, Lainnya
- `jumlah_wisatawan_mancanegara` : Jumlah kunjungan per negara per bulan
- `sumber` : BPS Provinsi Bali - Total kunjungan per bulan

Total kunjungan 2025: 6.948.754 kunjungan
Bulan tertinggi: Juli 2025 (697.107 kunjungan)
Bulan terendah: Februari 2025 (450.697 kunjungan)
Negara asal terbanyak: Australia

## Sumber Data
- Total kunjungan per bulan: BPS Provinsi Bali (https://bali.bps.go.id)
- Rincian per negara: Estimasi dari share / proporsi negara asal BPS, karena BPS tidak mempublikasikan rincian per negara per bulan secara terbuka.
- Cuaca: Open-Meteo Historical Weather API
- Tempat wisata: Wikipedia - Pariwisata di Bali & Daftar Kabupaten dan Kota di Bali

## Cara Menjalankan
1. Buka file CSV di Excel / Google Sheets
2. Filter berdasarkan `bulan` atau `negara_asal` untuk analisis

## Catatan / Keterbatasan
- Total per bulan adalah data real dari BPS.
- Rincian per negara adalah estimasi dari proporsi, bukan angka resmi per negara dari BPS.
- Data cuaca diambil untuk titik Denpasar (latitude -8.65, longitude 115.2167).
