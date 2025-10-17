# Machine Learning Pertemuan 4–6: Prediksi Kelulusan Mahasiswa

## Tahapan Proyek
### 1. Data Collection & Cleaning
Membaca dataset kelulusan_mahasiswa.csv menggunakan Pandas, menghapus duplikasi, menangani nilai kosong, dan melakukan visualisasi awal menggunakan Seaborn serta Matplotlib untuk mendeteksi outlier.

### 2. Exploratory Data Analysis (EDA)
Melakukan analisis deskriptif dan visualisasi hubungan antar variabel menggunakan histogram, scatter plot, dan heatmap korelasi untuk memahami pola yang memengaruhi kelulusan mahasiswa.

### 3. Feature Engineering
Menambahkan fitur baru seperti Rasio_Absensi dan IPK_x_Study untuk meningkatkan performa model.
Dataset hasil olahan disimpan sebagai processed_kelulusan.csv.

### 4. Dataset Splitting
Membagi dataset menjadi train, validation, dan test set dengan rasio 70/15/15 menggunakan train_test_split secara stratified untuk menjaga distribusi label.

### 5. Model Development
- Baseline Model: Logistic Regression dengan pipeline preprocessing menggunakan SimpleImputer dan StandardScaler.
- Model Alternatif: Random Forest Classifier dengan parameter class_weight="balanced" untuk menangani ketidakseimbangan kelas.

### 6. Model Evaluation & Hyperparameter Tuning
Melakukan validasi silang (StratifiedKFold) dan tuning hyperparameter menggunakan GridSearchCV.
Evaluasi dilakukan dengan metrik F1-score (macro), classification report, dan ROC-AUC curve.

### 7. Feature Importance
Menampilkan peringkat kepentingan fitur (feature importance) dari model Random Forest untuk interpretasi hasil dan pemahaman faktor yang paling memengaruhi kelulusan.

### 8. Model Deployment Preparation
Menyimpan model terbaik ke file rf_model.pkl menggunakan joblib, serta menambahkan contoh prediksi lokal (inference) dengan input fiktif.

### 9. Hasil Akhir
Model Random Forest memberikan performa terbaik dengan nilai F1-score dan ROC-AUC yang tinggi pada data validasi maupun data uji.
Pipeline ini siap digunakan kembali untuk memprediksi kelulusan mahasiswa baru secara otomatis dengan hasil yang cepat dan konsisten.
