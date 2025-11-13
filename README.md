# JabarBirth-Prediction
**Proyek Prediksi Kelahiran di Jawa Barat**

---

## Latar Belakang

Pertumbuhan penduduk merupakan salah satu indikator penting dalam pembangunan suatu daerah. Jumlah kelahiran menjadi faktor utama yang memengaruhi dinamika pertumbuhan tersebut. Di Provinsi Jawa Barat, yang merupakan provinsi dengan jumlah penduduk terbesar di Indonesia, perubahan angka kelahiran setiap tahunnya memiliki dampak signifikan terhadap berbagai sektor, seperti pendidikan, kesehatan, ekonomi, serta penyediaan infrastruktur publik.

Data dari Badan Pusat Statistik (BPS) menunjukkan bahwa tingkat kelahiran di Jawa Barat cenderung berfluktuasi dari tahun ke tahun. Beberapa kabupaten/kota mengalami peningkatan jumlah kelahiran, sementara daerah lainnya mengalami penurunan. Faktor-faktor yang memengaruhi kondisi ini bisa berasal dari berbagai aspek, antara lain tingkat pendidikan ibu, pendapatan keluarga, ketersediaan fasilitas kesehatan, tingkat urbanisasi, hingga program pemerintah dalam bidang keluarga berencana.

Dalam konteks perencanaan pembangunan daerah, kemampuan untuk **memprediksi jumlah kelahiran di masa depan** menjadi hal yang penting. Prediksi ini dapat membantu pemerintah daerah dalam mengambil keputusan strategis, seperti perencanaan alokasi anggaran untuk pelayanan kesehatan ibu dan anak, pembangunan fasilitas pendidikan, hingga pengendalian laju pertumbuhan penduduk.

Melalui penerapan **metode data mining**, khususnya dengan pendekatan *predictive modeling*, diharapkan dapat diperoleh pola dan tren yang menggambarkan hubungan antara berbagai variabel sosial, ekonomi, dan kesehatan terhadap jumlah kelahiran di Jawa Barat. Analisis ini tidak hanya memberikan gambaran historis, tetapi juga memungkinkan peramalan (*forecasting*) terhadap jumlah kelahiran di tahun-tahun berikutnya.

Dengan demikian, penelitian ini bertujuan untuk **mengeksplorasi data kelahiran di Jawa Barat**, menganalisis faktor-faktor yang memengaruhi, serta membangun model prediksi yang akurat untuk memperkirakan angka kelahiran di masa depan.

---

## Tujuan Proyek

- Memprediksi jumlah kelahiran per kabupaten/kota di Jawa Barat.  
- Mengidentifikasi faktor sosial-ekonomi dan kesehatan yang memengaruhi tingkat kelahiran.  
- Memberikan insight untuk perencanaan pembangunan daerah terkait populasi.

## SMART Questions

| Huruf | Makna | Pertanyaan SMART |
|-------|-------|-----------------|
| **S (Specific)** | Fokus pada masalah yang jelas | Kabupaten atau kota manakah di Jawa Barat yang memiliki **jumlah kelahiran tertinggi dan terendah** dalam lima tahun terakhir? |
| **M (Measurable)** | Bisa diukur dari dataset | Berapa jumlah kelahiran per tahun di setiap kabupaten/kota? <br> Bagaimana distribusi kelahiran berdasarkan **jenis kelamin** dan **status kelahiran**? |
| **A (Achievable)** | Dapat dicapai dengan dataset | Dengan data yang ada, apakah **prediksi jumlah kelahiran per kabupaten/kota** untuk tahun berikutnya bisa dilakukan menggunakan model time series atau regresi sederhana? |
| **R (Relevant)** | Relevan dengan tujuan | Pertanyaan apa yang relevan untuk **memahami tren kelahiran** di Jawa Barat dari 2020–2024 dan distribusinya menurut jenis kelamin/status? |
| **T (Time-bound)** | Terikat waktu | Dalam periode **2020–2024**, bagaimana tren jumlah kelahiran di setiap kabupaten/kota? <br> Prediksi jumlah kelahiran untuk tahun **2025–2027**. |

---

## Dataset

Dataset disimpan di folder `Data/`:

- `Prediksi_Angka_Kelahiran_di_Jawa_Barat.csv` → Data jumlah kelahiran per kabupaten/kota di Jawa Barat (2012–2023), termasuk status kelahiran dan jenis kelamin.

### Contoh Sample Data Per Tahun

| tahun | jumlah_kelahiran |
|-------|-----------------|
| 2012  | 406,544         |
| 2013  | 352,204         |
| 2014  | 333,441         |
| 2015  | 896,063         |
| 2016  | 856,299         |
| 2017  | 917,556         |
| 2018  | 911,763         |
| 2019  | 825,491         |
| 2020  | 789,541         |
| 2021  | 867,490         |
| 2022  | 832,267         |
| 2023  | 820,059         |

### Contoh Sample Data Per Kabupaten/Kota

| nama_kabupaten_kota      | jumlah_kelahiran |
|---------------------------|-----------------|
| KABUPATEN BOGOR           | 1,401,924       |
| KABUPATEN BEKASI           | 788,397        |
| KABUPATEN BANDUNG          | 588,031        |
| KOTA DEPOK                 | 514,713        |
| KOTA BEKASI                | 429,353        |
| …                         | …               |
| KOTA BANJAR                | 20,982         |

### Distribusi Kelahiran Berdasarkan Jenis Kelamin

| jenis_kelamin | jumlah_kelahiran |
|---------------|-----------------|
| LAKI-LAKI     | 4,444,375       |
| PEREMPUAN     | 4,364,343       |

### Distribusi Kelahiran Berdasarkan Status Kelahiran

| status_kelahiran | jumlah_kelahiran |
|-----------------|-----------------|
| HIDUP            | 8,785,303       |
| MATI             | 23,415          |

---


## Eksplorasi Data (EDA)

### Total Kelahiran per Tahun

Line chart tren jumlah kelahiran per tahun:

<img width="790" height="490" alt="Kelahiran pertahun jawa barat" src="https://github.com/user-attachments/assets/d86c01cc-063f-4e67-ace6-73b4d41b10e8" />

**Insight awal:**  
- Terdapat fluktuasi jumlah kelahiran dari tahun ke tahun.  
- Puncak tertinggi terjadi pada 2017–2018.  
- Tren menurun setelah 2018, kemudian naik lagi pada 2021.  

### Total Kelahiran per Kabupaten/Kota

<img width="1189" height="790" alt="Total Kelahiran per KabupatenKota di Jawa Barat" src="https://github.com/user-attachments/assets/13019726-81c6-4f0d-8c24-8accca4e7b79" />

### Distribusi Kelahiran Berdasarkan Jenis Kelamin

<img width="790" height="790" alt="Distribusi Kelahiran berdasarkan Jenis Kelamin" src="https://github.com/user-attachments/assets/e1e0519d-5bea-4619-ac4c-51d3f7d10488" />

- Laki-laki: 4,444,375  
- Perempuan: 4,364,343  

### Distribusi Kelahiran Berdasarkan Status Kelahiran

<img width="790" height="590" alt="Distribusi Kelahiran berdasarkan Status Kelahiran" src="https://github.com/user-attachments/assets/8dd62583-008e-48ba-aa43-9c93f1b3e8f8" />

- Hidup: 8,785,303  
- Mati: 23,415  

---
