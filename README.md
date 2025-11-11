# Klasifikasi-Gambar-Mengunakan-Convolutional-Neural-Network-CNN

# ☕ Analisis Perbandingan Arsitektur CNN untuk Deteksi Karat Daun Kopi

## 📖 Deskripsi Singkat
Proyek ini bertujuan untuk mendeteksi **penyakit karat daun kopi** menggunakan pendekatan **Convolutional Neural Network (CNN)**. Penyakit ini, yang disebabkan oleh jamur *Hemileia vastatrix*, merupakan salah satu faktor utama rendahnya produktivitas kopi di Indonesia. Dengan deteksi otomatis berbasis citra, diharapkan sistem ini dapat membantu petani dalam mengenali penyakit lebih cepat dan akurat.

---

## ⚙️ Masalah
- Produksi kopi Indonesia masih tertinggal karena serangan *karat daun kopi*.
- Penyakit ini bisa menyebabkan kerugian hingga **50% hasil panen**.
- Diperlukan sistem deteksi otomatis berbasis gambar untuk identifikasi dini daun yang terinfeksi.

---

## 🧠 Metode
- Menggunakan **CNN (Convolutional Neural Network)** untuk klasifikasi daun kopi **sehat** dan **terinfeksi**.
- Dataset diambil dari **Kaggle**, berjumlah **1.560 gambar** (769 terinfeksi, 791 sehat).
- Data dibagi menjadi **80% train** dan **20% validation**.
- Diterapkan **augmentasi data** (rotasi, flipping, rescaling, shifting) untuk meningkatkan generalisasi.
- Tiga arsitektur CNN dibandingkan:
  - 🧩 **ResNet101V2**
  - ⚡ **MobileNetV2**
  - 🔗 **DenseNet121**
- Model dikompilasi menggunakan:
  - Optimizer: `Adam`
  - Loss Function: `Binary Crossentropy`
  - Metrics: `Accuracy`, `Precision`, `Recall`, `F1-Score`

---

## 📊 Hasil
| Model | Akurasi Validasi | Precision | Recall | F1-Score |
|--------|------------------|-----------|---------|-----------|
| ResNet101V2 | 89.45% | 0.91 | 0.87 | 0.89 |
| MobileNetV2 | 85.55% | 0.89 | 0.80 | 0.84 |
| **DenseNet121** | **92.19%** | **0.94** | **0.91** | **0.92** |

✅ **DenseNet121** terbukti memiliki performa terbaik dan direkomendasikan untuk implementasi deteksi karat daun kopi.

---

## 🧩 Kesimpulan
Model **DenseNet121** dengan pendekatan **CNN** mampu mendeteksi karat daun kopi dengan akurasi tinggi (**92,19%**).  
Metode ini berpotensi digunakan dalam sistem deteksi otomatis di sektor pertanian untuk meningkatkan produksi dan mendukung kesejahteraan petani kopi.

---

## 👥 Tim Peneliti
- **Muhammad Rayhan Nuansa Adha** – Modelling, Metodologi, Kesimpulan  
- **Nadia Sukesi Sianipar** – Preprocessing, Abstrak, Pendahuluan  
- **Peksyaji** – Evaluasi Model, Hasil dan Diskusi  

---

## 🏫 Universitas Indonesia  
**Program Studi Statistika, Fakultas MIPA**  
Mata Kuliah: *Analisis Data Tidak Terstruktur (SCST603106)*  
Tahun: 2024
