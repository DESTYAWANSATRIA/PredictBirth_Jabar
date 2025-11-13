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

## Eksplorasi Data (EDA)

### Total Kelahiran per Tahun

Line chart tren jumlah kelahiran per tahun:

<img width="790" height="490" alt="Kelahiran pertahun jawa barat" src="https://github.com/user-attachments/assets/d86c01cc-063f-4e67-ace6-73b4d41b10e8" />

**Insight awal:**  
- Terdapat fluktuasi jumlah kelahiran dari tahun ke tahun.  
- Puncak tertinggi terjadi pada 2017–2018.  
- Tren menurun setelah 2018, kemudian naik lagi pada 2021.  

