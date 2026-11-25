# UTS Data Acquisition & Management — Kelas F

**Nama:** Maria Indriani Lelu
**NIM:** 2501010335
**Prodi:** Informatika - INSTIKI

### Deskripsi
Projek akuisisi dan pengolahan data pariwisata Bali dari 3 sumber: download, API, dan scraping.

### Sumber Data
| Metode | Sumber | File |
|---|---|---|
| Download | BPS Provinsi Bali | `data/raw/download.csv` |
| API | Open-Meteo Denpasar | `data/raw/api.json` |
| Scraping | Wikipedia Daftar Tempat Wisata di Bali | `data/raw/scraping.html` |

### Isi Dataset
- **Download:** 132 baris (12 bulan x 11 negara)
- **API:** 11 baris harian (tanggal 1 tiap bulan, Jan-Okt 2025) Denpasar
- **Scraping:** 10 baris, nama + kabupaten saja
- **Gabung:** Pakai kunci `Bulan`

### Total BPS
Jan 529897, Feb 450697, Mar 470851, Apr 591221, Mei 602213, Jun 637868, Jul 697107, Agu 682866, Sep 635149, Okt 594853, Nov 483364, Des 572668. Total 2025: 6948754.

### Keterbatasan
BPS tidak sediakan CSV per negara per bulan. Total per bulan di file ini ASLI dari BPS. Rincian per negara adalah estimasi dari share BPS.

Wikipedia tidak sediakan angka kunjungan, jadi scraping tidak ada kolom kunjungan.

Data API hanya 11 hari sampel, bukan hourly setahun penuh.

### Etika Data
- Lisensi: BPS terbuka akademik, Open-Meteo non-komersial, Wikipedia CC BY-SA.
- PII: Tidak ada data pribadi.
- Robots.txt Wikipedia sudah dicek dan diizinkan.
- API Key: Tidak ada.

### Struktur Folder
- `data/raw/` - data asli
- `Proses/` - data bersih + gabungan
- `catatan_provenance.csv` - provenance + MD5
- `notebook/` - Colab
