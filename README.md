# UJIAN TENGAH SEMESTER (UTS)
## DATA ACQUISITION & MANAGEMENT

### Judul Projek
**Akuisisi dan Pengolahan Data Destinasi Pariwisata di Bali**

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
1. Mengumpulkan data destinasi pariwisata di Bali.
2. Memahami karakteristik dan ukuran dataset.
3. Memeriksa lisensi serta etika penggunaan data.
4. Mengambil data menggunakan API dan web scraping.
5. Membersihkan dan menggabungkan data dari beberapa sumber.

### 4. Metode Akuisisi Data

| Metode | Keterangan | Format |
|---|---|---|
| Download | Mengambil dataset pariwisata Bali | CSV/Excel |
| API | Mengambil data cuaca wilayah Bali | JSON |
| Web Scraping | Mengambil informasi pariwisata dari halaman web statis yang diizinkan | HTML/JSON |

### 5. Sumber Data
Sumber data yang digunakan akan dicatat berdasarkan hasil pemeriksaan dan proses akuisisi.

- Dataset: Data destinasi pariwisata Bali.
- API: Open-Meteo.
- Web Scraping: Halaman web statis yang mengizinkan proses scraping.

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
- Process/: Penyimpanan data hasil pengolahan.
- documentation/: Dokumentasi etika data dan provenance.
- Notebook/: Notebook Google Colab berisi seluruh proses pengerjaan.

### 8. Ketentuan Dataset
- Dataset hasil download minimal 100 baris.
- Data hasil API minimal 30 baris.
- Data scraping berasal dari halaman yang mengizinkan pengambilan data.
- Penggabungan menggunakan kunci yang bermakna.

### 9. Tools yang Digunakan
- GitHub
- Google Colab
- Python
- Pandas
- Requests
- BeautifulSoup

### 10. Hasil Akhir
Hasil akhir projek berupa dataset yang telah dibersihkan dan digabungkan, notebook pengerjaan, Data Ethics Checklist, serta catatan provenance dari setiap sumber data.
