# 🫁 Pneumonia Classification using EfficientNetB0

## 🚀 Ringkasan Proyek
Proyek ini membangun model klasifikasi pneumonia berbasis citra **Chest X-ray** menggunakan arsitektur **EfficientNetB0** dengan pendekatan *transfer learning*. Model bertujuan untuk mengklasifikasikan citra ke dalam dua kelas: **Pneumonia** dan **Normal**.

---

## 📌 Informasi Umum
- **Task** : Binary Image Classification  
- **Domain** : Medical Imaging  
- **Model** : EfficientNetB0 (Pretrained ImageNet)  
- **Framework** : TensorFlow & Keras  
- **Environment** : Google Colab  
- **Output** : Model klasifikasi pneumonia  

---

## 📂 Struktur Dataset
Dataset disusun mengikuti standar Keras ImageDataGenerator:

```
pneumonia/
│
├── train/
│   ├── NORMAL/
│   └── PNEUMONIA/
│
└── test/
    ├── NORMAL/
    └── PNEUMONIA/
```

> Folder tidak relevan seperti `__MACOSX` dibersihkan sebelum training untuk mencegah error.

---

## 🔍 Data Preparation
Langkah preprocessing meliputi:
- Ekstraksi dataset dari file `.zip`
- Pembersihan folder tidak valid
- Validasi struktur direktori
- Pengecekan jumlah data per kelas

Hal ini penting untuk mencegah **data leakage**, terutama pada domain medis.

---

## 🧠 Arsitektur Model
Model menggunakan **EfficientNetB0** sebagai backbone dengan konfigurasi berikut:

1. EfficientNetB0 (`include_top=False`)
2. Global Average Pooling
3. Dense Layer
4. Output layer dengan **sigmoid activation**

Model dirancang untuk **binary classification**.

---

## ⚙️ Konfigurasi Training
- **Input Size** : 224 × 224  
- **Loss Function** : Binary Crossentropy  
- **Optimizer** : Adam  
- **Metrics** : Accuracy  
- **Output Activation** : Sigmoid  

---

## 📊 Evaluasi
Evaluasi model dilakukan menggunakan data test terpisah untuk mengukur performa generalisasi. Model menghasilkan probabilitas prediksi:
- `0` → Normal  
- `1` → Pneumonia  

---

## 💾 Penyimpanan Model
Model dapat disimpan menggunakan:
```python
model.save("pneumonia_efficientnetb0.h5")
```

---

## ▶️ Cara Menjalankan
1. Upload dataset ke Google Drive
2. Mount Google Drive di Colab
3. Jalankan notebook dari awal hingga akhir
4. Training dan evaluasi model
5. Simpan model hasil training

---

## 🛠️ Teknologi
- Python  
- TensorFlow / Keras  
- EfficientNet  
- NumPy  
- Matplotlib  

---

## ✨ Pengembangan Lanjutan
Beberapa pengembangan yang dapat dilakukan:
- Fine-tuning EfficientNet
- Data augmentation
- Confusion Matrix & Classification Report
- Grad-CAM untuk interpretabilitas

---

## 👤 Author
**Chris**  
Computer Vision & Deep Learning
