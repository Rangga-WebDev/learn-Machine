# 🏠 Mini Project: Prediksi Harga Rumah (Regression)

## 📌 Overview

Mini project ini bertujuan untuk membangun model Machine Learning yang mampu memprediksi harga rumah di California menggunakan dataset California Housing.

Project ini mencakup seluruh tahapan pipeline Machine Learning:

- Pemahaman masalah
- Exploratory Data Analysis (EDA)
- Data preprocessing
- Pelatihan dan perbandingan model
- Hyperparameter tuning
- Evaluasi dan kesimpulan akhir

---

## 🎯 Rumusan Masalah

Tujuan utama dari project ini adalah memprediksi **median harga rumah** berdasarkan beberapa fitur seperti:

- Median Income (Pendapatan rata-rata)
- House Age (Umur rumah)
- Average Rooms (Rata-rata jumlah kamar)
- Population (Populasi area)
- Latitude & Longitude
- dan fitur numerik lainnya

Permasalahan ini termasuk dalam kategori **Supervised Learning – Regression**, karena target berupa nilai kontinu.

---

## 📊 Dataset

- Sumber: `sklearn.datasets.fetch_california_housing()`
- Jumlah Data: 20.640 baris
- Jumlah Fitur: 8 fitur numerik
- Target: Median House Value

Seluruh fitur bersifat numerik sehingga proses preprocessing relatif sederhana.

---

## 🔎 Exploratory Data Analysis (EDA)

### Temuan Utama:

1. Fitur **Median Income (MedInc)** memiliki korelasi paling kuat terhadap harga rumah.
2. Distribusi harga rumah cenderung sedikit skew ke kanan.
3. Beberapa fitur memiliki korelasi sedang satu sama lain.
4. Faktor geografis (latitude dan longitude) mempengaruhi variasi harga.
5. Area dengan pendapatan tinggi cenderung memiliki harga rumah lebih mahal.

Visualisasi yang dilakukan:
- Distribusi target
- Heatmap korelasi
- Scatter plot Income vs Target
- Scatter plot Rooms vs Target
- Scatter plot HouseAge vs Target

---

## ⚙️ Data Preprocessing

Tahapan preprocessing yang dilakukan:

- Split data train-test (80:20)
- Feature scaling menggunakan StandardScaler
- Tidak diperlukan penanganan missing value (dataset bersih)

Scaling dilakukan karena beberapa model regresi sensitif terhadap skala fitur.

---

## 🤖 Model yang Digunakan

Tiga model regresi dibandingkan:

1. **Linear Regression**
2. **Random Forest Regressor**
3. **Gradient Boosting Regressor**

### 📈 Metrik Evaluasi:

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score

---

## 📊 Perbandingan Model

|     Model         |     MAE    |     RMSE |     R²   |
|-------------------|------------|----------|----------|
| Linear Regression |  0.533200  | 0.745581 | 0.575788 |
| Random Forest     |  0.327425  | 0.505143 | 0.805275 |
| Gradient Boosting |  0.371650  | 0.542217 | 0.775643 |

---

## 🔧 Hyperparameter Tuning

Dilakukan tuning menggunakan **GridSearchCV** pada model terbaik (Random Forest).

Parameter yang diuji:
- `n_estimators`
- `max_depth`

Hasil tuning menunjukkan peningkatan performa model.

---

## 🏆 Model Terbaik

Model terbaik pada project ini adalah:

### ✅ Random Forest Regressor

Alasan:
- Nilai R² tertinggi
- RMSE lebih rendah
- Lebih mampu menangkap hubungan non-linear dibanding Linear Regression

---

## 💡 Insight Bisnis

1. Pendapatan wilayah adalah faktor utama dalam menentukan harga rumah.
2. Lokasi geografis sangat mempengaruhi variasi harga.
3. Model ensemble memberikan prediksi yang lebih stabil dan akurat.

---

## 🚀 Pengembangan Selanjutnya

Beberapa kemungkinan pengembangan:

- Feature engineering tambahan
- Menggunakan model boosting lanjutan (XGBoost, LightGBM)
- Cross-validation lebih mendalam
- Optimasi hyperparameter lebih luas

---

## 🛠️ Teknologi yang Digunakan

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab

---

## 👨‍💻 Author

Agung Adi Rangga  
Machine Learning Enthusiast
