# 📦 Proyek Klasifikasi Beras dengan CNN

## 📝 Deskripsi
Proyek ini mengimplementasikan model Convolutional Neural Network (CNN) untuk mengklasifikasikan lima jenis beras berdasarkan gambar. Model ini telah dilatih menggunakan dataset gambar grayscale dari lima kelas:

- **Arborio**
- **Basmati**
- **Ipsala**
- **Jasmine**
- **Karacadag**

Model dilatih dengan akurasi tinggi dan dikonversi ke beberapa format untuk keperluan deployment: **SavedModel**, **TensorFlow Lite**, dan **TensorFlow.js**.

---

## 🧠 Tentang Model

Model CNN dibuat dengan beberapa layer konvolusi, batch normalization, dan dense. Model dilatih menggunakan citra grayscale berukuran 150x150 piksel, serta menggunakan class weighting untuk menangani dataset yang tidak seimbang.

### 🔍 Performa Model:
- **Akurasi Training**: > 95%
- **Akurasi Validasi**: > 95%
- **Callback**: `EarlyStopping` dan `ModelCheckpoint`
- **Jumlah Kelas**: 5 kelas jenis padi

---

## 📁 Struktur Folder
## 🔧 Format Model

- **SavedModel**  
  Format standar TensorFlow untuk deployment server dan kompatibel dengan TensorFlow Serving.

- **TFLite**  
  Format ringan untuk inference di perangkat mobile atau IoT.

- **TensorFlow.js**  
  Format untuk menjalankan model langsung di browser atau aplikasi berbasis JavaScript.

---

## 🧪 Inferensi

### ✅ TensorFlow Lite:
1. Load model `.tflite` menggunakan `tf.lite.Interpreter`
2. Preprocessing gambar (150x150, grayscale, normalisasi)
3. Jalankan inferensi dan tampilkan kelas prediksi

### ✅ SavedModel:
1. Load dengan `tf.keras.models.load_model()`
2. Jalankan `.predict()` untuk inferensi langsung

---

## 📊 Hasil Model

- **Akurasi pelatihan**: ≥ 95%
- **Akurasi validasi**: ≥ 95%
- **Inferensi berhasil**: Ya (dengan TF-Lite & SavedModel)

---
