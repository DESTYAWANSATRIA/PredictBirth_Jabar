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

| Huruf | Pertanyaan SMART |
|-------|-----------------|
| **S (Specific)** | Kabupaten/kota mana yang memiliki jumlah kelahiran tertinggi dan terendah? |
| **M (Measurable)** | Berapa total jumlah kelahiran per kabupaten/kota dan di seluruh Jawa Barat? |
| **A (Achievable)** | Apakah prediksi jumlah kelahiran dapat dilakukan menggunakan metode regresi linier? |
| **R (Relevant)** | Apa tren jumlah kelahiran berdasarkan data historis dan prediksi model? |
| **T (Time-bound)** | Bagaimana prediksi jumlah kelahiran untuk periode tertentu (misal 2024–2027)? |

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


## Metodologi
1. **Modeling dengan Linear Regression**  
   - Melatih model pada data training menggunakan data dari tahun 2012 - 2022 sebagai data training dan Menggunakan data 2023 sebagai data test.
     hasil training:
     <img width="1489" height="989" alt="Perbandingan Prediksi vs Aktual Jumlah Kelahiran 2023" src="https://github.com/user-attachments/assets/bd221f7b-742a-46d7-bb48-64fa2f594dca" />
   - Mengevaluasi performa model menggunakan **Mean Absolute Error (MAE)** atau **R² Score**

        | Metrik | Nilai |
        |--------|-------|
        | Mean Absolute Error (MAE) | 2,221.79 |
        | Mean Squared Error (MSE) | 13,181,492.38 |
        | Root Mean Squared Error (RMSE) | 3,630.63 |
        | R-squared (R²) | 0.976 |

        **Insight:**  
        - Nilai R² mendekati 1 menunjukkan model regresi linier dapat menjelaskan hampir semua variansi jumlah kelahiran berdasarkan tahun.  
        - MAE dan RMSE menunjukkan rata-rata kesalahan prediksi relatif kecil dibandingkan jumlah kelahiran total, menandakan prediksi model cukup akurat.
  

2. **Prediksi Jumlah Kelahiran Masa Depan 2024 - 2027**
   - Prediksi untuk tahun 2024 menggunakan model linear regression
     <img width="1388" height="989" alt="Total prediksi kelahiran di Jawa Barat pada tahun 2024" src="https://github.com/user-attachments/assets/741f37d5-fd5b-4502-8f7a-966c0556880a" />

   - Prediksi untuk tahun 2025 menggunakan model linear regression
     <img width="1388" height="989" alt="Total prediksi kelahiran di Jawa Barat pada tahun 2025" src="https://github.com/user-attachments/assets/78959ecd-4e0c-4038-b9ba-6a4171857360" />

   - Prediksi untuk tahun 2026 menggunakan model linear regression
     <img width="1388" height="989" alt="hasil prediksi kelahiran ditahun 2026" src="https://github.com/user-attachments/assets/6b22be29-f753-49e4-ae88-1dcfa401d452" />
 - Prediksi untuk tahun 2027 menggunakan model linear regression
   <img width="1388" height="989" alt="Total prediksi kelahiran di Jawa Barat pada tahun 2027" src="https://github.com/user-attachments/assets/e0a9ee2a-2693-432e-9824-b03aeb8c94c0" /> 
 - Perbandingan total prediksi kelahiran di Jawa barat
   <img width="989" height="590" alt="Perbandingan Total Prediksi Kelahiran di Jawa Barat (2024-2027)" src="https://github.com/user-attachments/assets/7a68ba7c-db9c-46da-8d30-e5855b3275f9" />

 - Total Kelahiran di Jawa Barat (2012-2027): Aktual vs. Prediksi
   <img width="1189" height="690" alt="Total Kelahiran di Jawa Barat (2012-2027) Aktual vs  Prediksi" src="https://github.com/user-attachments/assets/e1f6f220-706a-456b-8ae6-2e70e076dd65" />

## Kesimpulan

Berdasarkan hasil eksplorasi data, prediksi menggunakan regresi linier, dan evaluasi model, diperoleh beberapa kesimpulan berikut:

### Kesimpulan SMART

| Huruf | Pertanyaan SMART | Jawaban / Insight dari Proyek |
|-------|-----------------|-------------------------------|
| **S (Specific)** | Kabupaten/kota mana di Jawa Barat yang memiliki jumlah kelahiran tertinggi dan terendah pada 2024–2027? | **Tertinggi:** Kabupaten Bogor (2024: 111,052; 2025: 110,163; 2026: 109,275; 2027: 108,400) <br> **Terendah:** Kota Banjar (2024: 2,552; 2025: 2,538; 2026: 2,523; 2027: 2,510) |
| **M (Measurable)** | Berapa total jumlah kelahiran di Jawa Barat pada periode 2024–2027? | **2024:** 804,016 <br> **2025:** 787,595 <br> **2026:** 771,174 <br> **2027:** 765,000 (estimasi) |
| **A (Achievable)** | Apakah prediksi jumlah kelahiran dapat dilakukan dengan regresi linier? | Ya, model regresi linier terbukti akurat dengan **R² = 0.976**, **MAE = 2,222**, sehingga prediksi per tahun dan per kabupaten/kota dapat diandalkan. |
| **R (Relevant)** | Apa tren utama jumlah kelahiran berdasarkan data historis dan prediksi? | - Tren jumlah kelahiran meningkat hingga 2017–2018, menurun 2019–2020, naik 2021. <br> - Prediksi 2024–2027 menunjukkan **penurunan jumlah total kelahiran sedikit**, tetapi kabupaten/kota tertentu tetap tinggi, seperti Bogor, Bekasi, dan Bandung. |
| **T (Time-bound)** | Bagaimana prediksi jumlah kelahiran di masa depan (2024–2027)? | Prediksi regresi linier per kabupaten/kota: <br> - **2024:** Total 804,016 <br> - **2025:** Total 787,595 <br> - **2026:** Total 771,174 <br> - **2027:** Total ~765,000 <br> Prediksi ini membantu perencanaan jangka menengah untuk **kesehatan ibu & anak, pendidikan, dan infrastruktur publik**. |

### Insight Tambahan
- Kabupaten/kota dengan jumlah kelahiran tinggi (Bogor, Bekasi, Bandung) perlu perhatian lebih pada **layanan publik**, termasuk kesehatan ibu & anak, pendidikan, dan transportasi.  
- Kota/kabupaten dengan jumlah kelahiran rendah (Kota Banjar, Kota Cirebon, Kabupaten Pangandaran) bisa menjadi fokus program peningkatan **kesejahteraan, fasilitas dasar, dan akses layanan publik**.  
- Prediksi regresi linier dapat menjadi acuan **kebijakan pembangunan dan alokasi sumber daya** untuk 4 tahun ke depan (2024–2027).  
- Data ini juga dapat membantu pemerintah dalam **perencanaan strategis jangka menengah** dan evaluasi efektivitas program kesehatan dan pendidikan di tiap kabupaten/kota.  
