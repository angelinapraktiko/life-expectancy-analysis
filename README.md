# life-expectancy-analysis
Analisis data life expectancy untuk memahami pengaruh faktor kesehatan dan sosial-ekonomi menggunakan EDA, visualisasi, dan korelasi.

---

## Deskripsi

Project ini merupakan analisis data *Life Expectancy* yang mencakup tahap eksplorasi data (EDA), pembersihan data, penanganan missing values, analisis statistik deskriptif, visualisasi data, deteksi outlier, serta analisis korelasi antar variabel.

Dataset ini menggambarkan kondisi kesehatan, sosial, dan ekonomi berbagai negara di dunia.

---

## Tujuan

* Memahami karakteristik dataset Life Expectancy
* Membersihkan dan mempersiapkan data untuk analisis
* Mengidentifikasi faktor yang mempengaruhi umur harapan hidup
* Menemukan hubungan antar variabel kesehatan, ekonomi, dan sosial

---

## Tahapan Analisis

### 1. Exploratory Data Analysis (EDA)

* Dataset terdiri dari **2938 data dan 22 kolom**
* Tidak ditemukan data duplikat
* Ditemukan missing values pada beberapa kolom seperti:

  * GDP
  * Population
  * Alcohol
  * Hepatitis B
  * Schooling

**Insight:**

* Life Expectancy memiliki variasi yang cukup besar antarnegara
* Beberapa variabel memiliki distribusi tidak normal (skewed)


### 2. Data Cleaning

* Imputasi missing values:
  
  * Median per negara (Life Expectancy, Adult Mortality, BMI, dll)
  * Median global (Alcohol, Schooling, dll)
  * Interpolasi (GDP & Population)
* Menghapus kolom dengan missing besar (`Hepatitis B`)
* Mengubah tipe data kategorikal (`Country`, `Status`)


### 3. Statistik Deskriptif

* Menghitung:

  * Mean, median, modus
  * Standar deviasi
  * Range
* Analisis berdasarkan kelompok:

  * Kesehatan
  * Gaya hidup
  * Ekonomi & pendidikan


### 4. Visualisasi Data

* Histogram distribusi variabel numerik
* Bar chart distribusi kategori (Status)
* Pairplot hubungan antar variabel penting

**Insight:**

* Banyak variabel memiliki distribusi **right-skewed**
* Life Expectancy cenderung berdistribusi normal
* Terdapat ketimpangan signifikan antarnegara


### 5. Penanganan Outlier

* Menggunakan metode **IQR (Interquartile Range)**
* Outlier **tidak dihapus** karena merepresentasikan kondisi nyata antarnegara


### 6. Analisis Korelasi

* Menggunakan korelasi Pearson
* Visualisasi heatmap

**Insight:**

* Life Expectancy:

  * Positif dengan: Schooling, GDP, BMI
  * Negatif dengan: Adult Mortality, HIV/AIDS
* Beberapa variabel memiliki korelasi tinggi (redundan)


## Insight Keseluruhan

* Umur harapan hidup meningkat dengan:

  * Pendidikan
  * Kondisi ekonomi
  * Status gizi
* Umur harapan hidup menurun dengan:

  * Tingginya angka kematian
  * Penyakit menular
* Terdapat kesenjangan besar antara negara berkembang dan maju

---

## Tools yang Digunakan

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn


