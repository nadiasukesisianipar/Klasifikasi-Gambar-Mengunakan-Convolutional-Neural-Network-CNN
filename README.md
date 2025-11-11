# ☕ Analisis Perbandingan Arsitektur CNN untuk Deteksi Karat Daun Kopi

## 📖 Deskripsi Singkat
Proyek ini mendeteksi **karat daun kopi** (Hemileia) menggunakan **Convolutional Neural Network (CNN)** untuk membantu deteksi dini kasus infeksi pada daun robusta.

---

## ⚙️ Masalah
- Karat daun mengurangi hasil panen hingga puluhan persen; identifikasi dini diperlukan untuk mitigasi.
- Diperlukan sistem deteksi otomatis berbasis citra agar diagnosis lebih cepat dan konsisten.

---

## 🧠 Metode
- Dataset Kaggle: **1.560 gambar** (769 terinfeksi, 791 sehat).  
- Split: **80% train / 20% validation** (1248 train / 312 val).  
- Augmentasi: rescaling, rotasi, shifting, scaling, horizontal flip.  
- Base models (pretrained ImageNet) diuji: **ResNet101V2, MobileNetV2, DenseNet121**.   
- Evaluasi: Akurasi, Precision, Recall, F1-score.

---

## 📊 Hasil (lengkap — termasuk metrik per kelas)

**Perbandingan metrik :**

| Model | Kelas | Akurasi (val) | Precision | Recall | F1-Score |
|-------|-------|---------------:|----------:|-------:|---------:|
| ResNet101V2 | Sehat | 0.8945 | 0.91 | 0.87 | 0.89 |
| ResNet101V2 | Tidak Sehat | 0.8945 | 0.88 | 0.92 | 0.90 |
| MobileNetV2 | Sehat | 0.8555 | 0.89 | 0.80 | 0.84 |
| MobileNetV2 | Tidak Sehat | 0.8555 | 0.83 | 0.91 | 0.87 |
| DenseNet121 | Sehat | 0.9219 | 0.91 | 0.94 | 0.92 |
| DenseNet121 | Tidak Sehat | 0.9219 | 0.94 | 0.91 | 0.92 |

**Kesimpulan singkat:** DenseNet121 unggul (akurasi validasi **92.19%**) dan menunjukkan metrik precision/recall/F1 lebih baik di kedua kelas, sehingga direkomendasikan untuk implementasi deteksi karat daun kopi.

