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
- **Data Ethics Checklist (9 Butir):** Seluruh 9 butir etika data telah diperiksa dan dicatat pada `data_ethics_checklist.csv` di root repository serta di dalam notebook, termasuk verifikasi data publik non-PII, lisensi sumber, dan integritas hash MD5.
- **Konsistensi Data & Penggabungan:** Ukuran data mentah mengacu ke sumber aslinya (`248x14` untuk Download, `168x4` untuk API, dan `120x6` untuk Scraping), sedangkan hasil penggabungan akhir (`merge` dengan `validate="one_to_one"` pada kunci `bulan` 1-12) tersimpan di `Proces/gabungan.csv` berukuran `12x5` dengan `0` duplikasi baris.

## Struktur Berkas & Folder
- `data/raw/` : Berkas mentah asli (Download CSV, API JSON, dan Scraping CSV) tanpa perubahan.
- `Proces/` : Hasil pembersihan/normalisasi (`csv_bersih.csv`, `data_json.json`, `data_html.html`) serta berkas hasil gabungan (`gabungan.csv`) beserta metadata (`metadata_gabungan.json`).
- `UTS_Data_Acquisition_Pariwisata_Bali.ipynb` : Notebook lengkap pengerjaan akuisisi, pembersihan, dan penggabungan data.
- `catatan_provenance.csv` : Catatan provenance lengkap untuk seluruh sumber data.
- `data_ethics_checklist.csv` : Daftar periksa 9 butir etika data.
```[cite: 2]

### Hal yang Sudah Kuubah di Draf Ini
* Lokasi `data_ethics_checklist.csv` diubah dari `Proces/data_ethics_checklist.csv` menjadi di *root* repository (`data_ethics_checklist.csv`) dan ditambahkan ke daftar *Struktur Berkas & Folder*[cite: 2].
* Keterangan konsistensi & penggabungan dipisah jelas antara ukuran data mentah (`248x14`, `168x4`, `120x6`) dan hasil gabungan akhir (`12x5` pada kunci `bulan` dengan `one_to_one` dan `0` duplikat)[cite: 2].
* Format berkas pada *Struktur Berkas & Folder* disesuaikan dengan berkas yang benar-benar ada (`Download CSV`, `API JSON`, `Scraping CSV`, serta isi folder `Proces/`)[cite: 2].

Setelah kamu *copas* dan *commit* perubahan `README.md` ini di GitHub, repository-mu sudah konsisten[cite: 2]. Ada lagi yang ingin kamu pastikan sebelum dikirim?
