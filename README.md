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
| Download | Mengambil data wisatawan mancanegara Bali | CSV |
| API | Mengambil data cuaca wilayah Bali (hourly) | JSON |
| Web Scraping | Mengambil informasi pariwisata dari halaman web statis yang diizinkan | HTML |

### 5. Sumber Data
| No | Sumber | Jenis | URL | Tanggal Akuisisi |
|----|--------|-------|-----|------------------|
| 1 | Download - Estimasi dari share BPS Provinsi Bali 2025 | CSV | https://www.bps.go.id/id/statistics-table/1/MTk3NSMx/pariwisata | 25 November 2026 |
| 2 | API - Open-Meteo | JSON | https://api.open-meteo.com/v1/forecast?latitude=-8.65&longitude=115.2167&hourly=temperature_2m,relative_humidity_2m,precipitation,wind_speed_10m | 25 November 2026 |
| 3 | Scraping - Wikipedia Daftar Tempat Wisata di Bali | HTML | https://id.wikipedia.org/wiki/Daftar_tempat_wisata_di_Bali | 25 November 2026 |

### 6. Tahapan Pengerjaan
1. Membaca dataset dan mengidentifikasi karakteristik data.
2. Memeriksa lisensi, PII, dan Data Ethics Checklist.
3. Mengambil data melalui API dengan penanganan status code dan retry.
4. Memeriksa robots.txt dan melakukan web scraping.
5. Membersihkan serta menggabungkan minimal dua sumber data.
6. Membuat dokumentasi provenance dan hash MD5.

### 7. Struktur Repository
- README.md: Penjelasan projek.
- Data/Raw/: Penyimpanan data asli hasil akuisisi.
- Process/: Penyimpanan data hasil pengolahan.
    - download_bersih.csv
    - api_bersih.json
    - scraping_bersih.html
    - data_gabungan.csv
- documentation/: Dokumentasi etika data dan provenance.
- notebook/: Notebook Google Colab berisi seluruh proses pengerjaan.

### 8. Ketentuan Dataset
- Dataset hasil download: 120 baris (12 bulan x 10 negara), sudah memenuhi minimal 100 baris.
- Data hasil API: 72 baris (3 hari x 24 jam hourly), sudah memenuhi minimal 30 baris.
- Data scraping berasal dari halaman Wikipedia yang mengizinkan pengambilan data.
- Penggabungan menggunakan kunci yang bermakna: bulan.

### 9. Etika Data, Lisensi dan PII
- Lisensi: Data BPS bersifat terbuka untuk keperluan akademik. Data Open-Meteo gratis untuk penggunaan non-komersial. Data Wikipedia berlisensi CC BY-SA.
- PII: Tidak ada data pribadi (nama, NIK, email, nomor HP) dalam dataset ini. Data yang digunakan hanya data agregat destinasi dan cuaca.
- API Key: Tidak ada API key yang disimpan di notebook. Semua request menggunakan User-Agent dengan email kampus dan timeout.

### 10. Data Ethics Checklist (9 Butir)
1. Lisensi: Semua sumber sudah diperiksa lisensinya - DIPATUHI
2. PII: Tidak ada data pribadi dalam dataset - AMAN
3. Quasi-identifier: Kombinasi tahun + bulan + negara tidak dapat mengidentifikasi individu - AMAN
4. Robots.txt: Wikipedia diizinkan, sudah dicek di https://id.wikipedia.org/robots.txt - DIPATUHI
5. Terms of Service: Tidak melanggar ToS ketiga sumber - DIPATUHI
6. Bias: Data download adalah estimasi, bias sudah dicatat di keterbatasan - DICATAT
7. Dampak: Tidak ada dampak negatif ke individu atau kelompok - AMAN
8. Atribusi: Semua sumber disebutkan di tabel Sumber Data - DIPATUHI
9. Keamanan Penyimpanan: File disimpan di Github, tidak ada API key, tidak ada data sensitif - AMAN

### 11. Keterbatasan Data - WAJIB DIBACA
Data download BUKAN angka resmi BPS per negara per bulan. Data ini adalah estimasi dari share resmi BPS 2025 (Australia 23.4%, India 8.2%, China 7.7%) dikali total bulanan, untuk keperluan latihan pembersihan dan penggabungan data. Data asli BPS Juli 2025 yang terverifikasi: Australia 161.051, China 59.651, India 45.288, Prancis 38.460, Korea Selatan 38.275.

### 12. Provenance dan Hash MD5
| File | Sumber | Tanggal Akuisisi | MD5 |
|------|--------|------------------|-----|
| Data/Raw/download.csv | Estimasi share BPS Bali | 25 November 2026 | [ISI MD5 DARI COLAB] |
| Data/Raw/api.json | Open-Meteo API | 25 November 2026 | [ISI MD5 DARI COLAB] |
| Data/Raw/scraping.html | Wikipedia Bali | 25 November 2026 | [ISI MD5 DARI COLAB] |

Cara hitung MD5 di Colab:
```python
import hashlib
for f in ['download.csv','api.json','scraping.html']:
    print(f, hashlib.md5(open(f,'rb').read()).hexdigest())
