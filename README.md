# Analisis Wisatawan Mancanegara ke Bali 2025

## Data Diri
- **Nama:** Maria Indriani Lelu
- **NIM:** 2501010335
- **Kelas:** F
- **Mata Kuliah:** Data Acquisition & Management
- **Topik:** Wisatawan Mancanegara ke Bali 2025

## Sumber Data & Provenance
| Jenis Akuisisi | Nama Berkas Raw | URL Sumber | Tanggal Akses | Lisensi | MD5 Hash |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Download | `data/raw/[nama_berkas_download]` | [URL sumber resmi] | [YYYY-MM-DD] | [Lisensi sumber] | `[md5_asli_berkas]` |
| API | `data/raw/[nama_berkas_api.json]` | [URL endpoint / dokumentasi API] | [YYYY-MM-DD] | [Lisensi / ketentuan API] | `[md5_asli_berkas]` |
| Scraping | `data/raw/[nama_berkas_scraping]` | [URL halaman statis target] | [YYYY-MM-DD] | [Lisensi / ketentuan halaman] | `[md5_asli_berkas]` |

## Keterangan Kepatuhan & Etika Data
- **Pemeriksaan `robots.txt`:** [Catat hasil pengecekan `robots.txt` halaman target scraping serta bukti kepatuhannya]
- **Teknis Akuisisi:** Seluruh request memakai `timeout`, `User-Agent` berisi email kampus sendiri, jeda antar-request, dan kredensial/API key disimpan terpisah di luar notebook.
- **Data Ethics Checklist (9 Butir):** [Tersedia lengkap beserta bukti pada notebook / dokumen checklist, termasuk identifikasi PII/quasi-identifier dan lisensi sumber]
- **Konsistensi Data & Penggabungan:** Angka pada dataset dan hasil penggabungan (`merge` dengan `validate`) mengacu langsung ke sumber resmi tanpa angka perkiraan atau duplikasi yang tidak diharapkan.

## Struktur Berkas & Folder
- `data/raw/` : Berkas mentah asli (Download CSV/Excel, API JSON, Scraping JSON/HTML) tanpa perubahan.
- `Proces/` : Hasil pembersihan/normalisasi (CSV bersih, JSON, HTML) serta berkas hasil gabungan beserta metadata.
- `[nama_notebook].ipynb` : Notebook lengkap pengerjaan Soal 1–5 dengan seluruh sel sudah dijalankan.
- `catatan_provenance.csv` : Catatan provenance lengkap untuk seluruh sumber data.
```[cite: 1, 2, 3, 4, 5]

Silakan masukkan **3 URL sumber** (download, API, scraping) dan **nama berkas mentah** yang kamu pakai sekarang, agar bagian tabel keterangannya langsung terisi pas untuk datamu.
