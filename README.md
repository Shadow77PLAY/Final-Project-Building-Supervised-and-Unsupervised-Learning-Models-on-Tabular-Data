# 📊 End-to-End Data Science Project: Bank Transactions Clustering & Classification

## 📌 1. Project Overview & Business Objective
Proyek ini bertujuan untuk menganalisis perilaku transaksi nasabah bank menggunakan pendekatan komprehensif Machine Learning. Proyek ini diselesaikan dalam dua tahapan besar:
1. **Unsupervised Learning (Clustering):** Melakukan segmentasi nasabah bank berdasarkan pola dan karakteristik perilaku transaksi mereka.
2. **Supervised Learning (Klasifikasi):** Membangun model prediktif yang dapat mengklasifikasikan nasabah baru secara otomatis ke dalam segmen yang sesuai berdasarkan data historis.

Manfaat bisnis dari proyek ini adalah membantu pihak manajemen bank dalam merancang strategi pemasaran yang personal (*targeted marketing*), meningkatkan retensi nasabah, serta mendukung pengambilan keputusan berbasis data.

---

## 📂 2. Repository Structure
Untuk memastikan kode rapi, modular, dan memenuhi standar industri, repositori ini diorganisasikan sebagai berikut:

* `[Klasifikasi]_Submission_Akhir_BMLP_Yosia_Azriel_Saputra.ipynb` : Proses eksperimen, pelatihan, dan evaluasi model Supervised Learning.
* `[Clustering]_Submission_Akhir_BMLP_Yosia_Azriel_Saputra.ipynb`  : Proses segmentasi, reduksi dimensi, dan analisis Unsupervised Learning.
* `data_clustering.csv`                     : Dataset perilaku transaksi hasil pelabelan dari tahap clustering.
* `data_clustering_inverse.csv`             : Dataset inversi yang digunakan untuk analisis fitur kembali.
* `decision_tree_model.h5`                  : Artefak model klasifikasi dasar menggunakan Decision Tree.
* `explore_random_forest_classification.h5` : Eksperimen model lanjutan menggunakan Random Forest.
* `tuning_classification.h5`                : Model Random Forest terbaik setelah melalui proses Hyperparameter Tuning.
* `model_clustering.h5`                     : Hasil penyimpanan model clustering yang siap digunakan.
* `PCA_model_clustering.h5`                 : Artefak model Principal Component Analysis untuk reduksi dimensi.

---

## 🛠️ 3. Methodology & Technical Workflow

### 🎯 A. Unsupervised Learning: Clustering & PCA
1. **Dimensionality Reduction:** Menggunakan **PCA (Principal Component Analysis)** untuk mereduksi dimensi fitur transaksi yang kompleks guna menghilangkan *noise* dan mempercepat komputasi model.
2. **Clustering Analysis:** Menerapkan algoritma clustering pada data hasil reduksi PCA untuk mengelompokkan nasabah ke dalam kelompok yang homogen.

### 🌲 B. Supervised Learning: Klasifikasi
1. **Model Baseline:** Membangun arsitektur dasar menggunakan algoritma **Decision Tree** untuk klasifikasi awal segmen nasabah.
2. **Advanced Modeling & Tuning:** Melakukan eksplorasi menggunakan **Random Forest** untuk meningkatkan performa akurasi.
3. **Hyperparameter Tuning:** Mengoptimalkan parameter model (seperti *max_depth*, *n_estimators*) menggunakan GridSearch/RandomizedSearch guna menghasilkan model terbaik yang siap rilis (*production-ready*).

---

## 📈 4. Model Evaluation & Results

### 📊 Evaluasi Model Klasifikasi Nasabah

| Model Architecture | Accuracy | Status |
| :--- | :---: | :--- |
| Decision Tree (Baseline) | ~82.3% | Baseline Model |
| Random Forest (Explore) | ~87.5% | Improved Model |
| **Random Forest (Tuned)** | **92.19%** | **Production Ready (Best)** |

### 🎯 Hasil Clustering & PCA
* **PCA Explained Variance:** Komponen utama PCA berhasil mempertahankan mayoritas informasi penting dari keseluruhan fitur asli secara efisien.
* **Clustering Insight:** Data nasabah berhasil dikelompokkan secara optimal ke dalam **3 Klaster Utama**:

---

## 🚀 5. How to Run This Project
Ikuti langkah berikut untuk menjalankan proyek ini di komputer lokal Anda:

1. Clone repositori ini:
   ```bash
   git clone https://github.com/Shadow77PLAY/Final-Project-Building-Supervised-and-Unsupervised-Learning-Models-on-Tabular-Data.git
   cd Final-Project-Building-Supervised-and-Unsupervised-Learning-Models-on-Tabular-Data
   ```
2. Pastikan dependensi utama sudah terinstal di komputer Anda:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn yellowbrick joblib
   ```
3. Buka notebook menggunakan Jupyter untuk melihat visualisasi data:
   ```bash
   jupyter notebook
   ```
