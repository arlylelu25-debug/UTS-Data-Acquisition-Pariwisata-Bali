# UTS Data Acquisition & Management
## Akuisisi dan Pengolahan Data Destinasi Pariwisata di Bali

### 1. Identitas

- Nama: Maria Indriani Lelu
  
- NIM: 2501010335

- Program Studi: Informatika

- Mata Kuliah: Data Acquisition & Management
  
- Institusi: INSTIKI
  
- Semester: Ganjil

### 2. Deskripsi Projek
Projek ini membahas proses pengumpulan, pemeriksaan, pembersihan, dan penggabungan data pariwisata di Bali. Data diperoleh melalui tiga metode, yaitu download dataset, API, dan web scraping.

### 3. Tujuan
- Mengumpulkan data destinasi pariwisata di Bali.
- Memahami karakteristik dan ukuran dataset.
- Memeriksa lisensi serta etika penggunaan data.
- Mengambil data menggunakan API dan web scraping.
- Membersihkan dan menggabungkan data dari beberapa sumber.

### 4. Metode Akuisisi Data
| Metode | Keterangan | Format |
|--------|------------|--------|
| Download | Mengambil dataset pariwisata Bali | CSV / Excel |
| API | Mengambil data cuaca wilayah Bali | JSON |
| Web Scraping | Mengambil informasi pariwisata dari halaman web statis yang diizinkan | HTML / JSON |

### 5. Sumber Data
| No | Sumber | Jenis | URL |
|----|--------|-------|-----|
| 1 | Download - Dataset Pariwisata Bali | CSV | https://www.bps.go.id/id/statistics-table/1/MTk3NSMx/pariwisata |
| 2 | API - Open-Meteo | JSON | https://api.open-meteo.com/v1/forecast?latitude=-8.65&longitude=115.2167&current=temperature_2m,relative_humidity_2m,precipitation,wind_speed_10m |
| 3 | Scraping - Wikipedia Daftar Tempat Wisata di Bali | HTML | https://id.wikipedia.org/wiki/Daftar_tempat_wisata_di_Bali |

### 6. Tahapan Pengerjaan
1. Membaca dataset dan mengidentifikasi karakteristik data.
2. Memeriksa lisensi, PII, dan Data Ethics Checklist.
3. Mengambil data melalui API dengan penanganan status code dan retry.
4. Memeriksa robots.txt dan melakukan web scraping.
5. Membersihkan serta menggabungkan minimal dua sumber data.
6. Membuat dokumentasi provenance dan hash MD5.

### 7. Struktur Repository
- README.md: Penjelasan projek.
- data/raw/: Penyimpanan data asli hasil akuisisi.
- data/processed/: Penyimpanan data hasil pengolahan.
- documentation/: Dokumentasi etika data dan provenance.
- notebook/: Notebook Google Colab berisi seluruh proses pengerjaan.

### 8. Ketentuan Dataset
- Dataset hasil download minimal 100 baris.
- Data hasil API minimal 30 baris.
- Data scraping berasal dari halaman yang mengizinkan pengambilan data.
- Penggabungan menggunakan kunci yang bermakna (Kabupaten / Destinasi).

### 9. Etika Data, Lisensi dan PII
- Lisensi: Data BPS bersifat terbuka untuk keperluan akademik. Data Open-Meteo gratis untuk penggunaan non-komersial. Data Wikipedia berlisensi CC BY-SA.
- PII: Tidak ada data pribadi (nama, NIK, email, nomor HP) dalam dataset ini. Data yang digunakan hanya data agregat destinasi dan cuaca.
- Data Ethics Checklist: Sudah diperiksa, tidak ada data sensitif, tidak melanggar robots.txt, semua sumber disebutkan.

### 10. Provenance dan Hash MD5
| File | Sumber | Tanggal Akuisisi |
|------|--------|------------------|
| data/raw/download.csv | BPS Bali | 25 November 2026 |
| data/raw/api.json | Open-Meteo API | 25 November 2026 |
| data/raw/scraping.html | Wikipedia Bali | 25 November 2026 |

### 11. Tools yang Digunakan
GitHub, Google Colab, Python, Pandas, Requests, BeautifulSoup

### 12. Hasil Akhir
Dataset yang telah dibersihkan dan digabungkan, notebook pengerjaan, Data Ethics Checklist, serta catatan provenance dari setiap sumber data.
