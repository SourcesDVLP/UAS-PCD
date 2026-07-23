# UAS Pengolahan Citra Digital (SIF202) — Klasifikasi Citra Bunga dengan MLP

**Nama Lengkap:** Ferdinan Mahrus
**NIM:** 24146086
**Mata Kuliah:** Pengolahan Citra Digital (SIF202)
**Tahun Ajaran:** Genap 2025/2026
**Dosen Pengampu:** Teuku Rizky Noviandy, S.Kom., M.Kom.

## Deskripsi Proyek
Repository ini berisi penyelesaian tugas UAS berupa model klasifikasi citra menggunakan algoritma
**Multi-Layer Perceptron (MLP)** pada dataset [Flowers Recognition](https://www.kaggle.com/datasets/alxmamaev/flowers-recognition)
dari Kaggle, yang terdiri dari 5 kelas: `daisy`, `dandelion`, `rose`, `sunflower`, `tulip`.

## Isi Repository
- `UAS_Pengolahan_Citra_Digital_24146086.ipynb` — source code lengkap (preprocessing, ekstraksi fitur, training MLP, evaluasi, visualisasi 25 prediksi)
- `Laporan_UAS_PCD_24146086.pdf` — laporan ilmiah
- `README.md` — file ini

## Cara Menjalankan
1. Unduh dataset dari Kaggle: https://www.kaggle.com/datasets/alxmamaev/flowers-recognition
2. Ekstrak dataset sehingga strukturnya menjadi:
   ```
   ./flowers/
       daisy/
       dandelion/
       rose/
       sunflower/
       tulip/
   ```
3. Install dependency yang dibutuhkan:
   ```
   pip install numpy pandas matplotlib opencv-python scikit-image scikit-learn
   ```
4. Jalankan seluruh sel pada `UAS_Pengolahan_Citra_Digital_24146086.ipynb` secara berurutan.

## Metodologi Singkat
- **Preprocessing:** resize 64x64, konversi BGR→RGB, normalisasi piksel
- **Ekstraksi fitur:** color histogram (96 fitur) + HOG (Histogram of Oriented Gradients)
- **Split data:** 80% train / 20% test, `random_state = 24146086`
- **Model:** `MLPClassifier` (scikit-learn), hidden layers (256, 128), aktivasi ReLU, optimizer Adam
- **Evaluasi:** `classification_report` (precision, recall, F1-score), confusion matrix, visualisasi 25 prediksi
