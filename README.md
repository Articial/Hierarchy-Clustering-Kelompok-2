# **Segmentasi Pasar Mobil BMW Menggunakan Metode Hierarchical Clustering**

## **Deskripsi Proyek**

Proyek ini bertujuan untuk melakukan analisis segmentasi pasar mobil BMW menggunakan metode **Hierarchical Clustering** berdasarkan tiga variabel utama: **tahun produksi**, **harga**, dan **ukuran mesin (sebagai proksi performa mesin)**. Dataset yang digunakan adalah **BMW Worldwide Sales Records (2010-2024)**, yang diperoleh dari platform Kaggle.

Hasil dari segmentasi ini diharapkan dapat memberikan wawasan tentang bagaimana BMW dapat lebih memahami pasar mobil mereka dan merancang strategi pemasaran yang lebih efektif berdasarkan karakteristik produk dan preferensi konsumen.

## **Tujuan**

* Menganalisis segmentasi mobil BMW dengan menggunakan metode **Hierarchical Clustering**.
* Mengidentifikasi jumlah kluster optimal yang dapat merepresentasikan segmen pasar mobil BMW.
* Memberikan interpretasi tentang karakteristik masing-masing kluster dan bagaimana hasil tersebut dapat digunakan untuk mendukung keputusan bisnis.

## **Fitur dan Variabel Utama**

* **Year**: Tahun produksi model mobil.
* **Price_USD**: Harga mobil dalam USD.
* **Engine_Size_L**: Ukuran mesin dalam liter (sebagai proksi untuk performa mesin).
* **Mileage_KM**: Jarak tempuh mobil (km).
* **Sales_Volume**: Volume penjualan mobil.

## **Metodologi**

Proyek ini menggunakan teknik **Hierarchical Clustering** untuk mengelompokkan mobil BMW berdasarkan kemiripan dalam hal harga, tahun produksi, dan ukuran mesin. Algoritma yang digunakan adalah **Agglomerative Hierarchical Clustering** dengan metode **Ward's linkage**, yang bertujuan untuk meminimalkan peningkatan varians antar kluster saat penggabungan.

### **Tahapan Analisis:**

1. **Pengumpulan Data**: Mengunduh dataset dari Kaggle.
2. **Pra-pemrosesan Data**: Membersihkan data, menghilangkan nilai yang hilang, dan melakukan normalisasi untuk memastikan skala variabel yang seragam.
3. **Clustering**: Menghitung jarak antar data, membuat linkage matrix, dan membangun dendrogram untuk menentukan jumlah kluster optimal.
4. **Evaluasi Model**: Menggunakan **Silhouette Score** untuk mengevaluasi sejauh mana kluster yang terbentuk saling terpisah dengan baik.
5. **Interpretasi dan Implikasi Bisnis**: Menginterpretasikan karakteristik tiap kluster untuk merumuskan strategi pemasaran yang tepat.

## **Struktur File**

```
/Segmentasi_Pasar_BMW/
│
├── README.md                # File ini
├── BMW_Segmentasi.ipynb     # Jupyter Notebook yang berisi kode analisis
└── data/
    └── bmw_sales_data.csv   # Dataset yang digunakan (dataset CSV)
```

## **Persyaratan**

Untuk menjalankan Jupyter Notebook ini, Anda memerlukan beberapa **perpustakaan Python** berikut:

* **pandas**: Untuk manipulasi dan analisis data.
* **numpy**: Untuk perhitungan numerik.
* **matplotlib**: Untuk visualisasi data.
* **seaborn**: Untuk visualisasi grafik statistik.
* **scipy**: Untuk perhitungan linkage matrix dan clustering.
* **scikit-learn**: Untuk evaluasi model dan validasi metrik.

### **Instalasi**

Untuk menginstal dependensi yang diperlukan, Anda bisa menggunakan **pip** atau **conda**. Berikut adalah cara untuk menginstal semua dependensi yang diperlukan menggunakan **pip**:

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn
```

Atau, jika Anda menggunakan **Anaconda**:

```bash
conda install pandas numpy matplotlib seaborn scipy scikit-learn
```

## **Instruksi Penggunaan**

1. **Unduh atau Kloning Repository**:
   Untuk mulai bekerja dengan file ini, Anda dapat mengunduh atau mengkloning repository ini ke mesin lokal Anda.

   ```bash
   git clone https://github.com/username/repository-name.git
   ```

2. **Jalankan Jupyter Notebook**:
   Setelah mengunduh file dan menginstal dependensi yang diperlukan, buka terminal dan navigasikan ke direktori tempat file berada, kemudian jalankan Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

3. **Eksekusi Notebook**:
   Buka file `BMW_Segmentasi.ipynb` dalam Jupyter Notebook, dan jalankan setiap sel untuk melakukan analisis. Anda dapat melihat visualisasi dendrogram, interpretasi kluster, dan hasil analisis lainnya sepanjang notebook.

4. **Hasil Analisis**:
   Setelah menjalankan notebook, Anda akan melihat hasil segmentasi mobil BMW dalam bentuk **5 kluster** yang masing-masing mewakili segmen pasar dengan karakteristik yang berbeda. Anda juga akan mendapatkan rekomendasi strategis untuk pemasaran, harga, dan diferensiasi produk berdasarkan hasil analisis kluster.

## **Referensi**

1. Kaggle. (2024). BMW Worldwide Sales Records (2010-2024). Retrieved from [https://www.kaggle.com/code/mohamedzayton/used-car-data-set-bmw](https://www.kaggle.com/code/mohamedzayton/used-car-data-set-bmw)
2. Ward, J. H. (1963). Hierarchical Grouping to Optimize an Objective Function. *Journal of the American Statistical Association*, 58(301), 236-244.
3. Han, J., Kamber, M., & Pei, J. (2012). *Data Mining: Concepts and Techniques* (3rd ed.). Elsevier.

## **Lisensi**

Proyek ini dilisensikan di bawah [Lisensi MIT](https://opensource.org/licenses/MIT).
