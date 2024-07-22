# Penerapan Model Jaringan Saraf Konvolusi untuk Klasifikasi Penyakit Daun Jagung

## 1. Judul / Topik
**Penerapan Model Jaringan Saraf Konvolusi untuk Klasifikasi Penyakit Daun Jagung Menggunakan Dataset Penyakit Daun Jagung**

## 2. Masalah dan Tujuan Penelitian

### a. Masalah dan Tujuan

**Masalah:**
Penyakit pada daun jagung dapat menyebabkan kerugian signifikan dalam produksi pertanian. Identifikasi dan klasifikasi penyakit daun jagung yang cepat dan akurat dapat membantu petani dan peneliti dalam pengelolaan penyakit dan pengambilan keputusan yang lebih baik. Dengan kemajuan teknologi komputer dan pembelajaran mesin, ada peluang untuk mengembangkan model otomatis yang dapat mengidentifikasi penyakit daun jagung dari gambar dengan akurasi tinggi.

**Tujuan:**
- Mengembangkan model Jaringan Saraf Konvolusi (CNN) untuk mengklasifikasikan gambar daun jagung ke dalam beberapa kategori penyakit.
- Meningkatkan akurasi klasifikasi penyakit daun jagung dengan menerapkan teknik augmentasi data dan arsitektur model CNN yang efektif.

### b. Model yang Dipakai

**Arsitektur Model CNN:**

- **Preprocessing Layers:** Resize dan Rescale untuk mengubah ukuran gambar dan menormalkan nilai piksel.
- **Data Augmentation:** Random Flip dan Random Rotation untuk meningkatkan keberagaman data pelatihan.
- **Convolutional Layers:** Menggunakan beberapa lapisan Conv2D diikuti dengan MaxPooling2D untuk mengekstraksi fitur dari gambar.
- **Fully Connected Layers:** Lapisan Flatten diikuti dengan Dense Layers untuk klasifikasi akhir.

![image](https://github.com/user-attachments/assets/2493130c-b7ce-47bb-bee7-e7d42184b63d)

## 3. Dataset

**Dataset yang Digunakan:**
- **Nama Dataset:** Corn or Maize Leaf Disease Dataset
- **Sumber:** [Kaggle - Corn or Maize Leaf Disease Dataset](https://www.kaggle.com/datasets/smaranjitghose/corn-or-maize-leaf-disease-dataset?resource=download)

**Exploratory Data Analysis (EDA):**

1. **Pemeriksaan Data:** Memeriksa struktur data dan distribusi kelas menggunakan teknik visualisasi.
2. **Preprocessing:** Resize gambar ke 256x256 piksel dan rescale nilai piksel untuk normalisasi.
3. **Pengorganisasian Dataset:** Pembagian dataset menjadi data pelatihan, validasi, dan pengujian dengan proporsi 80%, 10%, dan 10%.
4. **Feature Extraction:** Menggunakan teknik augmentasi data untuk meningkatkan variasi dalam dataset pelatihan dan memaksimalkan performa model.

## 4. Proses Learning/Modeling

**Arsitektur Model:**

1. **Preprocessing Layers:** Resize dan Rescale gambar.
2. **Data Augmentation:** Teknik augmentasi seperti Random Flip dan Random Rotation.
3. **Convolutional Layers:** Konvolusi dengan 32, 64, dan 64 filter, serta MaxPooling untuk ekstraksi fitur.
4. **Fully Connected Layers:** Lapisan Flatten diikuti dengan Dense Layers untuk klasifikasi akhir.

**Proses Training:**

- **Optimizer:** Adam
- **Loss Function:** SparseCategoricalCrossentropy
- **Metrics:** Accuracy
- **Epochs:** 30
- **Batch Size:** 32

**Proses Evaluasi:** Pengujian model pada dataset pengujian untuk mengukur akurasi dan loss.

## 5. Hasil Uji Performa

- **Akurasi Keseluruhan:** 90.42%
- **Loss Keseluruhan:** 0.2200

**Kinerja Model:**

| Kelas            | Precision | Recall | F1-Score | Support |
|------------------|-----------|--------|----------|---------|
| Blight           | 21%       | 20%    | 20%      | 121     |
| Common Rust      | 26%       | 26%    | 26%      | 133     |
| Gray Leaf Spot   | 14%       | 16%    | 15%      | 63      |
| Healthy          | 25%       | 26%    | 26%      | 131     |
| **Rata-Rata**    | 22%       | 22%    | 22%      | 448     |

**Akurasi per Kelas:**

- **Blight:** 33.88%
- **Common Rust:** 36.09%
- **Gray Leaf Spot:** 19.05%
- **Healthy:** 34.35%

## 6. Kesimpulan

Model Jaringan Saraf Konvolusi yang diterapkan dalam penelitian ini menunjukkan akurasi keseluruhan yang baik sebesar 90.42% pada dataset pengujian. Namun, akurasi per kelas menunjukkan variasi yang signifikan, dengan beberapa kelas memiliki akurasi yang lebih rendah, khususnya kelas Gray Leaf Spot.

**Kesimpulan:**
- **Efektivitas Model:** Model CNN menunjukkan potensi yang baik untuk klasifikasi penyakit daun jagung dengan akurasi keseluruhan yang tinggi, tetapi memerlukan peningkatan lebih lanjut untuk meningkatkan akurasi pada kelas dengan performa rendah.
- **Tindakan Selanjutnya:** Perlu dilakukan tuning hyperparameter lebih lanjut, eksplorasi arsitektur model yang lebih kompleks, dan evaluasi teknik augmentasi data tambahan untuk meningkatkan akurasi klasifikasi di setiap kelas.
- **Rekomendasi:** Pertimbangkan penggunaan teknik augmentasi data yang lebih canggih dan kumpulkan lebih banyak data pelatihan untuk meningkatkan performa model pada semua kelas.

Dengan demikian, penelitian ini memberikan dasar yang kuat untuk aplikasi model CNN dalam pengidentifikasian penyakit daun jagung dan menunjukkan arah untuk penelitian lebih lanjut untuk perbaikan model.
