# Proyek Prediksi Produksi Jahe Provinsi Sulawesi Tengah (2018–2025)

Proyek ini merupakan implementasi pemodelan statistik dan *Machine Learning* sederhana menggunakan algoritma **Regresi Linear Sederhana (Simple Linear Regression)**. Tujuan utama dari proyek ini adalah untuk menganalisis tren historis serta memprediksi total produksi tanaman jahe berdasarkan luas lahan panen di wilayah Provinsi Sulawesi Tengah.

## Identitas Mahasiswa
* **Nama:** Nazwa Alifiah Bustaman
* **NIM:** F5512520050
* **Kelas:** TI - B
* **Program Studi:** S1 - Teknik Informatika
* **Mata Kuliah:** Statistika dan Probabilitas

---

## Ringkasan Dataset
* **Sumber Data:** Badan Pusat Statistik (BPS) Provinsi Sulawesi Tengah.
* **Rentang Waktu:** 2018 – 2025 (8 Tahun).
* **Jumlah Sampel:** 104 baris data (Hasil *data stacking* dari 13 Kabupaten/Kota × 8 Tahun pengamatan).
* **Variabel Model:**
  * **Variabel $X$ (Independen):** Luas Panen Jahe (Hektar)
  * **Variabel $Y$ (Dependen):** Total Produksi Jahe (Kilogram)

---

## Hasil Pemodelan Matematika
Berdasarkan analisis regresi yang dilakukan melalui Microsoft Excel dan divalidasi menggunakan Python (Jupyter Notebook), didapatkan formula inti model sebagai berikut:

$$Y = 0.3349X + 22814$$

* **Koefisien Determinasi ($R^2$):** $0.1476$ ($14.76\%$). Luas lahan panen memengaruhi volume produksi jahe sebesar $14.76\%$, sedangkan $85.24\%$ sisanya dipengaruhi oleh faktor eksternal lain di luar jangkauan model (seperti cuaca, hama, varietas bibit, dan intensitas pupuk).

---

## Teknologi & Library yang Digunakan
Proyek ini dikembangkan menggunakan bahasa pemrograman **Python 3.13** di lingkungan **Jupyter Notebook (VS Code)** dengan beberapa pustaka pendukung:
* **Pandas**: Digunakan untuk membaca dataset dari file Excel dan melakukan pra-pemrosesan data (*data cleaning* & *stripping*).
* **Matplotlib**: Digunakan untuk memvisualisasikan grafik *scatter plot* data riil beserta garis tren regresi linier.
* **NumPy**: Digunakan untuk manipulasi array matematika saat menggambar garis prediksi.
* **Openpyxl**: Digunakan sebagai *engine* pendukung Pandas untuk membaca berkas berekstensi `.xlsx`.

---

## Struktur Berkas dalam Repositori
* `Data_Jahe_Sulteng.xlsx` : Berkas dataset mentah dan grafik regresi versi Microsoft Excel.
* `Prediksi_Jahe_Sulteng.ipynb` : Berkas kode sumber utama interaktif (*source code*) berbasis Jupyter Notebook yang terbagi menjadi 3 tahapan (Load Data, Visualisasi Grafik, dan Mesin Inferensi Prediksi otomatis).