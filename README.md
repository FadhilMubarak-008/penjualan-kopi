# Analisis Penjualan Kopi

## Project Overview

Project ini bertujuan untuk menganalisis data penjualan kopi guna memahami pola penjualan, performa produk, serta perilaku pembelian pelanggan. Analisis ini diharapkan dapat memberikan insight yang dapat membantu pengambilan keputusan bisnis berbasis data.

---

## Deskripsi Dataset

Dataset terdiri dari 6 kolom utama:

* `date` → tanggal transaksi
* `datetime` → waktu transaksi detail
* `cash_type` → metode pembayaran
* `card` → ID pelanggan
* `money` → jumlah pembayaran
* `coffee_name` → jenis produk kopi

Jumlah data: **3636 baris**

---

## Data Cleaning

Beberapa langkah preprocessing yang dilakukan:

* Tidak ditemukan data duplikat
* Missing value terdapat pada kolom `card`

  * Tidak dianggap kritis karena analisis berfokus pada penjualan, bukan customer profiling
* Konversi kolom `date` menjadi format datetime

---

## Exploratory Data Analysis (EDA)

### 1. Analisis Distribusi Harga

Statistik deskriptif pada kolom `money` menunjukkan:

* Rata-rata: 31.74
* Median: 32.82
* Minimum: 18.12
* Maksimum: 40.00
* Standar deviasi: 4.91

**Insight:**

* Harga produk relatif stabil
* Tidak terdapat outlier ekstrem
* Rentang harga mencerminkan variasi produk dari basic hingga premium

---

### 2. Analisis Tren Penjualan Harian

Dilakukan agregasi total revenue per hari.

**Insight:**

* Penjualan menunjukkan fluktuasi yang cukup tinggi
* Tidak terdapat tren naik/turun yang konsisten
* Mengindikasikan permintaan yang tidak stabil dan kemungkinan dipengaruhi faktor eksternal

---

### 3. Analisis Revenue per Produk

Dilakukan agregasi total revenue berdasarkan jenis kopi.

**Insight:**

* Latte berkontribusi cukup besar terhadap total revenue

Hipotesis:

* Karna Latte Produk berbasis susu, cenderung memberikan nilai transaksi lebih tinggi karna rasanya yang manis

---

### 4. Analisis Jumlah Transaksi per Produk

Menghitung frekuensi transaksi/pembelian setiap produk.

**Insight:**

* Americano memiliki jumlah transaksi tertinggi

Hipotesis:

* Karena harga produk yang sangat terjangkau, customer cendrung lebih memilih produk tersebut

---

## Insights Utama

1. **Perbedaan Peran Produk**

   * Americano → volume driver (sering dibeli)
   * Latte → revenue driver (nilai tinggi)

2. **Strategi Pricing Stabil**

   * Variasi harga relatif kecil

3. **Fluktuasi Penjualan Tinggi**

   * Tidak ada pola tren yang stabil

---

## Tools yang digunakan

* Python
* Pandas
* Matplotlib

---

## Penutup

Analisis menunjukkan bahwa meskipun dataset sederhana, terdapat insight yang cukup baik terkait peran produk, stabilitas harga, serta dinamika penjualan. Dengan pendekatan analisis yang tepat, data ini dapat digunakan untuk mendukung strategi bisnis yang lebih efektif.

---

## 📎 Future Work

* Analisis berdasarkan waktu (jam, weekday vs weekend)
* Customer segmentation (menggunakan kolom `card`)
* Analisis metode pembayaran
* Penggunaan moving average untuk melihat tren jangka panjang

---
