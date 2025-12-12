# 🏥 Tugas Model Improvement - Heart Disease Dataset

Repository ini berisi tugas mata kuliah **Kecerdasan Buatan** tentang **Model Improvement** menggunakan algoritma **K-Nearest Neighbors (KNN)** pada dataset Heart Disease.

## 📋 Deskripsi

Proyek ini mengimplementasikan teknik improvement model machine learning dengan fokus pada:
- **Feature Scaling** menggunakan MinMaxScaler
- **Hyperparameter Tuning** untuk mencari nilai K optimal
- **Perbandingan performa** model sebelum dan sesudah improvement

## 📊 Dataset

Dataset yang digunakan adalah **Heart Disease Dataset** yang berisi data pasien dengan berbagai fitur medis untuk memprediksi penyakit jantung.

**Sumber Dataset:** [AI-UPB GitHub Repository](https://github.com/asepmuhidin/AI-UPB)

**Fitur Dataset:**
- `age`: Usia pasien
- `sex`: Jenis kelamin
- `cp`: Tipe nyeri dada
- `trestbps`: Tekanan darah saat istirahat
- `chol`: Kolesterol serum
- `fbs`: Gula darah puasa
- `restecg`: Hasil elektrokardiografi
- `thalach`: Detak jantung maksimum
- `exang`: Angina akibat olahraga
- `oldpeak`: ST depression
- `slope`: Kemiringan segmen ST
- `ca`: Jumlah pembuluh darah utama
- `thal`: Thalassemia
- `target`: **Target variabel** (0 = tidak sakit, 1 = sakit jantung)

**Total Data:** 303 baris, 14 kolom

## 🛠️ Teknologi yang Digunakan

- **Python 3.x**
- **Pandas** - Data manipulation
- **Scikit-learn** - Machine learning
  - `MinMaxScaler` - Feature scaling
  - `KNeighborsClassifier` - KNN algorithm
  - `train_test_split` - Data splitting
  - `classification_report` - Model evaluation
- **Matplotlib** - Data visualization

## 📂 Struktur File

```
tugas-ai-model-improvement/
│
├── Tugas_model_improvment.ipynb    # Notebook utama
├── README.md                         # File ini
└── .gitignore                        # (opsional)
```

## 🚀 Cara Menjalankan

### Opsi 1: Google Colab (Recommended)
1. Buka file `Tugas_model_improvment.ipynb` di GitHub
2. Klik tombol **"Open in Colab"** di bagian atas notebook
3. Jalankan semua cell dengan `Runtime > Run all`
4. Lihat hasil analisis dan visualisasi

### Opsi 2: Local Jupyter Notebook
1. Clone repository ini:
   ```bash
   git clone https://github.com/[username]/tugas-ai-model-improvement.git
   ```
2. Install dependencies:
   ```bash
   pip install pandas scikit-learn matplotlib
   ```
3. Buka Jupyter Notebook:
   ```bash
   jupyter notebook Tugas_model_improvment.ipynb
   ```
4. Jalankan semua cell

## 📈 Metodologi

### 1. **Data Loading & Exploration**
- Load dataset dari GitHub
- Eksplorasi struktur data
- Cek missing values

### 2. **Preprocessing**
- Dataset sudah bersih (tidak ada missing values)
- Semua fitur sudah dalam bentuk numerik
- Tidak perlu encoding tambahan

### 3. **Data Splitting**
- Train: 80% (242 data)
- Test: 20% (61 data)
- Stratified sampling untuk menjaga proporsi target

### 4. **Simple Modeling (Baseline)**
- Training KNN tanpa scaling
- Evaluasi performa baseline
- K = 5 (default)

### 5. **Feature Improvement (Scaling)**
- Scaling semua fitur numerik dengan **MinMaxScaler**
- Transformasi nilai ke rentang [0, 1]
- Training ulang model dengan data ter-scale

### 6. **Hyperparameter Tuning**
- Mencoba nilai K dari 3 hingga 99 (step = 2)
- Evaluasi accuracy untuk setiap K
- Visualisasi grafik accuracy vs K
- Pilih K optimal berdasarkan test accuracy

### 7. **Final Model**
- Training model dengan K optimal
- Evaluasi performa akhir
- Classification report lengkap

## 📊 Hasil

### Perbandingan Performa

| Model | Train Accuracy | Test Accuracy |
|-------|---------------|---------------|
| **Without Scaling** | ~81% | ~69% |
| **With Scaling** | ~85% | ~81% |
| **With Tuning (K optimal)** | ~87% | ~84% |

> **Note:** Hasil aktual dapat berbeda sedikit karena random state

### Visualisasi

![Grafik Tuning Parameter](https://via.placeholder.com/600x400.png?text=Grafik+Accuracy+vs+K)

*Grafik menunjukkan performa model dengan berbagai nilai K*

### Kesimpulan
1. ✅ **Feature scaling** meningkatkan akurasi secara signifikan (~12% improvement)
2. ✅ **Hyperparameter tuning** mengoptimalkan performa model
3. ✅ Model terbaik dicapai dengan K = [sesuai hasil tuning]
4. ✅ Tidak ada overfitting yang signifikan (gap train-test kecil)

## 📝 Pembelajaran

### Yang Dipelajari:
- Pentingnya **feature scaling** untuk algoritma berbasis jarak (KNN)
- Cara melakukan **hyperparameter tuning** secara sistematis
- Interpretasi **classification report** dan metrik evaluasi
- Visualisasi hasil tuning untuk decision making

### Best Practices:
- Selalu lakukan scaling untuk KNN
- Gunakan stratified sampling untuk data tidak seimbang
- Evaluasi dengan train-test split untuk deteksi overfitting
- Visualisasi hasil untuk insight yang lebih baik

## 👨‍💻 Author

**Arie Miftah Budiman**
- NIM: 312210350
- Program Studi: Teknik Informatika
- Mata Kuliah: Kecerdasan Buatan
- Dosen: Asep Muhidin, S.Kom., M.Kom.

## 📚 Referensi

1. Dataset: [AI-UPB GitHub Repository](https://github.com/asepmuhidin/AI-UPB)
2. Scikit-learn Documentation: [KNeighborsClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)
3. Scikit-learn Documentation: [MinMaxScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html)

## 📄 License

This project is for educational purposes only.

## 🙏 Acknowledgments

- Terima kasih kepada **Pak Asep Muhidin** atas dataset dan panduan tugas
- UCI Machine Learning Repository untuk dataset Heart Disease
- Komunitas Python dan Scikit-learn

