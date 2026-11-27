# Analisis Wisatawan Mancanegara ke Bali 2025

## Data Diri
- **Nama:** Maria Indriani Lelu
- **NIM:** 2501010335
- **Kelas:** F
- **Mata Kuliah:** Data Acquisition & Management
- **Topik:** Wisatawan Mancanegara ke Bali 2025

## Sumber Data & Provenance
| Jenis Akuisisi | Nama Berkas Raw | URL Sumber | Tanggal Akses | Lisensi | MD5 Hash |
| :--- | :--- | :--- | :---: | :--- | :--- |
| Download | `data/raw/Jumlah Kunjungan Wisatawan Mancanegara per bulan Menurut Paspor yang Dipegang , 2026.csv` | https://www.bps.go.id/id/statistics-table/2/MTQ3MCMy/kunjungan-wisatawan-mancanegara-per-bulan-menurut-kebangsaan-kunjungan-.html | 2026-11-27 | Data publik resmi BPS | `a3bc7f1e998338342527fa6d7d443320` |
| API | `data/raw/api_cuaca_denpasar_bali.json` | https://open-meteo.com/ | 2026-11-27 | API publik terbuka (Open-Meteo) | `afc65cd73109e054068a4221fa914765` |
| Scraping | `data/raw/scraping_katalog_referensi.csv` | https://books.toscrape.com/ | 2026-11-27 | Publik / diizinkan `robots.txt` | `69e10b241e6bfeb94e941674be5c7c9c` |

## Keterangan Kepatuhan & Etika Data
- **Pemeriksaan `robots.txt`:** `robots.txt` pada situs target scraping telah diperiksa sebelum pengambilan data dan dinyatakan diizinkan (`True`).
- **Teknis Akuisisi:** Seluruh request memakai `timeout`, header `User-Agent` berisi kontak email, jeda antar-request, dan tanpa penyimpanan kredensial sensitif di dalam kode.
- **Data Ethics Checklist (9 Butir):** Seluruh 9 butir etika data telah diperiksa dan dicatat pada `Proces/data_ethics_checklist.csv` serta notebook, termasuk verifikasi data publik non-PII, lisensi sumber, dan integritas hash MD5.
- **Konsistensi Data & Penggabungan:** Angka pada dataset dan hasil penggabungan (`merge` dengan `validate`) mengacu langsung ke sumber resmi (`248x14` untuk Download, `168x4` untuk API, dan `120x6` untuk Scraping) tanpa angka perkiraan atau duplikasi yang tidak diharapkan.

## Struktur Berkas & Folder
- `data/raw/` : Berkas mentah asli (Download CSV/Excel, API JSON, Scraping JSON/HTML) tanpa perubahan.
- `Proces/` : Hasil pembersihan/normalisasi (CSV bersih, JSON, HTML) serta berkas hasil gabungan beserta metadata.
- `UTS_Data_Acquisition_Pariwisata_Bali.ipynb` : Notebook lengkap pengerjaan akuisisi data dengan seluruh sel sudah dijalankan.
- `catatan_provenance.csv` : Catatan provenance lengkap untuk seluruh sumber data.
