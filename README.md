# Machine Learning Pertemuan 4–6: Prediksi Kelulusan Mahasiswa

## Deskripsi Proyek
Repositori ini berisi rangkaian kegiatan praktikum *Machine Learning* dari **Pertemuan 4 hingga Pertemuan 6**, dengan fokus utama pada penerapan algoritma **Random Forest untuk Klasifikasi**.  
Tujuan akhirnya adalah membangun model yang mampu memprediksi status **kelulusan mahasiswa (Lulus / Tidak Lulus)** berdasarkan data tabular seperti IPK, absensi, dan waktu belajar.

---

## Rincian Pertemuan
- **Pertemuan 4:** *Data Preparation* — Pembersihan, transformasi, dan penyimpanan dataset (`kelulusan_mahasiswa.csv` → `processed_kelulusan.csv`).
- **Pertemuan 5:** *Modeling Dasar* — Split data menjadi train/val/test dan membangun model dasar.
- **Pertemuan 6:** *Random Forest untuk Klasifikasi* — Membuat pipeline lengkap, tuning hyperparameter, evaluasi model, dan interpretasi fitur.

---

## Struktur Folder
Machine-Learning-Pertemuan-4-6/
├── data/
│ ├── kelulusan_mahasiswa.csv
│ ├── processed_kelulusan.csv
│ ├── X_train.csv
│ ├── X_val.csv
│ ├── X_test.csv
│ ├── y_train.csv
│ ├── y_val.csv
│ └── y_test.csv
├── notebooks/
│ ├── pertemuan4_data_preparation.ipynb
│ ├── pertemuan5_modeling.ipynb
│ └── pertemuan6_random_forest.ipynb
├── model/
│ └── rf_model.pkl
├── results/
│ ├── roc_test.png
│ ├── pr_test.png
│ └── confusion_matrix.txt
└── README.md

---

## ⚙️ Cara Menjalankan Proyek

Instalasi
Pastikan sudah menginstal **Python ≥ 3.10**.  
Lalu install dependensi:
```bash
pip install -r requirements.txt

**Jalankan Notebook**
Gunakan Jupyter Notebook atau VS Code, lalu buka dan jalankan:
• notebooks/pertemuan4_data_preparation.ipynb
• notebooks/pertemuan5_modeling.ipynb
• notebooks/pertemuan6_random_forest.ipynb

Inference (Prediksi Baru)
Untuk mencoba prediksi model tersimpan:

import joblib, pandas as pd
model = joblib.load("model/rf_model.pkl")
sample = pd.DataFrame([{
    "IPK": 3.4,
    "Jumlah_Absensi": 4,
    "Waktu_Belajar_Jam": 7,
    "Rasio_Absensi": 4/14,
    "IPK_x_Study": 3.4*7
}])
print("Prediksi:", int(model.predict(sample)[0]))

Hasil Evaluasi
| Tahap           | Dataset  | F1-score | ROC-AUC | Catatan                                |
| --------------- | -------- | -------- | ------- | -------------------------------------- |
| **Baseline**    | Validasi | 1.00     | -       | Model awal tanpa tuning                |
| **Tuned Model** | Validasi | 1.00     | -       | Tuning max_depth dan min_samples_split |
| **Final Model** | Test     | 1.00     | 1.00    | Model stabil dan akurat                |

Confusion Matrix:
[[2 0]
 [0 3]]

3 Fitur Teratas (Feature Importance):
1. IPK — Fitur paling dominan, mencerminkan kemampuan akademik.
2. Waktu_Belajar_Jam — Berpengaruh besar terhadap performa.
3. IPK_x_Study — Kombinasi kuat antara IPK dan waktu belajar.

Kesimpulan
Model Random Forest menunjukkan performa sempurna pada dataset ini (F1-score & ROC-AUC = 1.0).
Hal ini menunjukkan:
• Dataset kemungkinan relatif sederhana atau mudah dipisahkan.
• Model mampu menangkap pola dengan sangat baik tanpa overfitting serius.
• Fitur IPK dan waktu belajar merupakan penentu paling kuat dalam klasifikasi kelulusan.

Identitas
Nama: Rafly Sanjaya
Kelas: 05TPLE015 - Machine Learning
Pertemuan: 4–6
