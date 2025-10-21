# 🧠 Machine Learning: Prediksi Kelulusan Mahasiswa

**Nama:** Rafly Sanjaya  
**Kelas:** 05TPLE015 - Machine Learning  

---

## 🚀 Jalankan di Google Colab

| Pertemuan | Notebook | Link Colab |
|------------|-----------|-------------|
| 4 | Data Preparation | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rafly-sanjaya/machine_learning/blob/main/pertemuan4_data_preparation.ipynb) |
| 5 | Modeling (Logistic Regression) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rafly-sanjaya/machine_learning/blob/main/pertemuan5_modeling.ipynb) |
| 6 | Random Forest | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rafly-sanjaya/machine_learning/blob/main/pertemuan6_random_forest.ipynb) |
| 7 | Artificial Neural Network (ANN) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rafly-sanjaya/machine_learning/blob/main/pertemuan7_ann.ipynb) |

---

## 📊 Deskripsi Proyek
Proyek ini bertujuan untuk memprediksi **kelulusan mahasiswa** berdasarkan faktor akademik dan perilaku belajar menggunakan berbagai algoritma Machine Learning.

### 🔹 Tahapan Proyek
1. **Data Preparation**  
   Membersihkan dataset `kelulusan_mahasiswa.csv`, menghapus duplikasi, menangani missing value, dan melakukan visualisasi awal.
2. **Modeling**  
   Membangun model baseline (Logistic Regression) dan model alternatif (Random Forest, ANN).
3. **Evaluation**  
   Menggunakan metrik F1-score, precision, recall, ROC-AUC, confusion matrix, dan grafik ROC/PR.
4. **Feature Importance & Interpretasi**  
   Mengidentifikasi fitur yang paling berpengaruh terhadap prediksi kelulusan.
5. **Deployment Preparation**  
   Menyimpan model terbaik ke file `rf_model.pkl` dan menambahkan contoh prediksi.
6. **Artificial Neural Network (Pertemuan 7)**
   - Implementasi model **ANN** untuk klasifikasi kelulusan.
   - Evaluasi performa model dan visualisasi loss serta akurasi pada data uji.

---

## 📁 File di Repositori
- `Laporan` : Laporan pertemuan 4-7.
- `processed_kelulusan.csv` : Dataset hasil preprocessing dan feature engineering.
- `X_train.csv`, `X_val.csv`, `X_test.csv` : Data fitur hasil pembagian dataset.
- `y_train.csv`, `y_val.csv`, `y_test.csv` : Label kelulusan hasil pembagian dataset.
- `kelulusan_mahasiswa.csv` → Dataset utama  
- `pertemuan4_data_preparation.ipynb`: Tahapan pembersihan dan pembagian data.  
- `pertemuan5_modeling.ipynb`: Model baseline Logistic Regression.
- `pertemuan6_random_forest.ipynb`: Model Random Forest dan evaluasi.
- `pertemuan7_ann.ipynb` : Model Artificial Neural Network (ANN).
- `learning_curve.png` : Grafik learning curve hasil pelatihan model.
- `rf_model.pkl` → Model hasil pelatihan  
- `roc_curve.png`, `confusion_matrix.png` → Hasil evaluasi model  

---

## 🧾 Cara Menjalankan di Colab
1. Klik tombol “Open in Colab” di atas.
2. Setelah notebook terbuka di Colab, klik **Runtime → Run all** untuk menjalankan semua sel. 

---

📌 **Catatan:**  
Gunakan `random_state=42` agar hasil model tetap konsisten setiap dijalankan ulang.
