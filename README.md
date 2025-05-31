# 🍽️ Piring vs Gelas – Klasifikasi Gambar dengan Transfer Learning

## 📌 Deskripsi Proyek

Model klasifikasi dibangun untuk membedakan dua jenis peralatan makan: Piring dan Gelas. Dengan memanfaatkan model **MobileNetV2** yang telah dilatih sebelumnya (*pretrained*), proyek ini menunjukkan bagaimana transfer learning dapat digunakan untuk tugas klasifikasi dengan dataset terbatas.

## 🛠️ Tools & Library

- Python 3
- Google Colab
- TensorFlow & Keras
- NumPy, Pandas, Matplotlib
- Scikit-learn

## 🧠 Arsitektur Model

- **Base Model**: MobileNetV2 (tanpa top layer, `include_top=False`)
- **Strategi**:
  - Layer pretrained dibekukan (`freeze`)
  - Ditambahkan layer:
    - `GlobalAveragePooling2D`
    - `Dense(64, activation='relu')`
    - `Dense(1, activation='sigmoid')`
- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam
- **Metrics**: Accuracy

## Dataset

- Jumlah total: 200 gambar
- Mobil: 100 gambar
- Motor: 100 gambar
- Sumber: Koleksi pribadi/manual
- Format: JPG/PNG
- Ukuran gambar: Diresize ke (224, 224)
- Split data:
  - 80% training
  - 20% validation

## 🚀 Hasil Pelatihan dan Evaluasi Model 

- Akurasi akhir model: 100% (1.00)
- Model mampu membedakan piring dan gelas dengan baik
- Confusion  Matrix: 

|        | Pred Piring | Pred Gelas |
|--------|-------------|------------|
| Piring | 100         | 0          |
| Gelas  | 0           | 100        |

- Classification Report: Precision, Recall, dan F1-Score di atas 0.95 untuk kedua kelas
- Visualisasi:
  - Kurva akurasi dan loss
    
    ![akurasi](https://github.com/user-attachments/assets/e7d2de00-f010-4311-bb99-4165ddbcbd58)
    ![loss](https://github.com/user-attachments/assets/1d3adf5c-217f-4643-9147-93a84476c655)


## 📁 Struktur File

| Nama File            | Deskripsi                                        |
|----------------------|--------------------------------------------------|
| `piringgelas.ipynb`  | Notebook utama berisi seluruh proses training    |
| `README.md`          | Deskripsi proyek ini                             |
| `dataset/`           | Folder dataset berisi gambar piring & gelas      |
| 'laporan.pdf'        | Laporan lengkap dalam format PDF                 |

## 📚 Refleksi Pribadi

Saya belajar banyak dari proyek ini, mulai dari menyiapkan dataset, menggunakan pretrained model, hingga melakukan evaluasi akurasi. Tantangan terbesar adalah menjaga konsistensi ukuran dan format gambar agar cocok untuk model MobileNetV2. Selain itu, saya jadi lebih memahami alur kerja Deep Learning dari preprocessing hingga prediksi.

## 🔗 Link Terkait

- 📦 GitHub Repository: [https://github.com/shafiiyyaa/pring-vs-gelas](https://github.com/shafiiyyaa/pring-vs-gelas)

---
