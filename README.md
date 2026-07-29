# Klasifikasi Citra Bunga dengan Multi-Layer Perceptron (MLP)

Proyek Ujian Akhir Semester (UAS) mata kuliah **Pengolahan Citra Digital**.

Sistem ini melakukan klasifikasi citra bunga menggunakan algoritma **Multi-Layer Perceptron (MLP)** untuk mengenali jenis bunga berdasarkan pola visual dari gambar.

---

## Identitas Mahasiswa

| Keterangan | Detail |
|------------|--------|
| **Nama** | Nur Alfitrah |
| **NIM** | 24146074 |
| **Mata Kuliah** | Pengolahan Citra Digital |
| **Tahun Ajaran** | Genap 2025/2026 |
| **Program Studi** | Sistem Informasi |
| **Universitas** | Universitas Abulyatama Aceh |

---

# Tentang Proyek

Proyek ini membangun sebuah sistem **Machine Learning** yang mampu melakukan klasifikasi terhadap citra bunga secara otomatis menggunakan metode **Multi-Layer Perceptron (MLP)**.

Tahapan yang dilakukan dalam proyek ini meliputi proses membaca dataset citra bunga, melakukan preprocessing citra, mengubah gambar menjadi data yang dapat diproses oleh komputer, melakukan pelatihan model MLP, serta melakukan evaluasi terhadap hasil klasifikasi.

Seluruh proses implementasi terdapat pada notebook:

```
UAS_PCD_NUR_ALFITRAH_24146074.ipynb
```

---

# Dataset

Dataset yang digunakan berupa kumpulan citra bunga yang terdapat pada folder:

```
dataset/flowers/
```

Dataset terdiri dari beberapa kelas bunga yang digunakan sebagai data pelatihan dan pengujian model.

Struktur folder dataset:

```
dataset/
└── flowers/
    ├── daisy/
    ├── dandelion/
    ├── roses/
    ├── sunflowers/
    └── tulips/
```

Setiap folder berisi kumpulan gambar bunga sesuai dengan kategori masing-masing.

---

# Alur Kerja Sistem (Pipeline)

Tahapan proses klasifikasi citra bunga:

## 1. Eksplorasi Dataset

Melakukan pemeriksaan awal terhadap dataset seperti:
- Membaca jumlah data gambar.
- Melihat distribusi kelas bunga.
- Menampilkan contoh citra.

## 2. Preprocessing Citra

Tahap preprocessing dilakukan agar gambar dapat diproses oleh model MLP.

Proses yang dilakukan:

- Mengubah ukuran gambar (*resize*) agar memiliki ukuran yang sama.
- Mengubah format warna citra.
- Melakukan normalisasi nilai piksel agar berada pada rentang tertentu.

## 3. Ekstraksi Fitur

Citra yang awalnya berbentuk 3 dimensi diubah menjadi bentuk vektor 1 dimensi (*flatten*) karena algoritma MLP membutuhkan data input berupa array numerik.

## 4. Encoding Label

Label atau nama kelas bunga diubah menjadi bentuk angka sehingga dapat dipahami oleh model.

## 5. Pembagian Data

Dataset dibagi menjadi:

- Data training untuk melatih model.
- Data testing untuk menguji kemampuan model.

## 6. Training Model MLP

Model dilatih menggunakan algoritma:

```
Multi-Layer Perceptron (MLP)
```

Model mempelajari pola dari citra bunga berdasarkan data training.

## 7. Evaluasi Model

Evaluasi dilakukan menggunakan:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

# Konfigurasi Model

Model menggunakan algoritma MLP dengan konfigurasi:

```python
MLPClassifier(
    hidden_layer_sizes=(256,128),
    activation="relu",
    solver="adam",
    max_iter=100,
    random_state=24146074
)
```

Keterangan:

- Hidden layer terdiri dari 2 lapisan.
- Fungsi aktivasi menggunakan ReLU.
- Optimasi menggunakan Adam.
- Random state menggunakan NIM agar hasil dapat direproduksi.

---

# Hasil

Model yang telah dibuat digunakan untuk melakukan klasifikasi citra bunga berdasarkan dataset yang tersedia.

Hasil pengujian menunjukkan bahwa model mampu mengenali pola citra bunga dan melakukan prediksi terhadap data baru.

Evaluasi model meliputi:

- Nilai akurasi klasifikasi.
- Performa setiap kelas bunga.
- Hasil prediksi gambar.

Contoh hasil evaluasi:

| Evaluasi | Hasil |
|----------|-------|
| Accuracy | Berdasarkan hasil pengujian model |
| Precision | Berdasarkan klasifikasi setiap kelas |
| Recall | Berdasarkan klasifikasi setiap kelas |
| F1-Score | Berdasarkan klasifikasi setiap kelas |

---

# Struktur Repository

```
UAS_PCD_NUR_ALFITRAH_24146074/

│
├── dataset/
│   └── flowers/
│       ├── daisy/
│       ├── dandelion/
│       ├── roses/
│       ├── sunflowers/
│       └── tulips/
│
├── UAS_PCD_NUR_ALFITRAH_24146074.ipynb
│
└── README.md
```

---

# Cara Menjalankan Program

1. Install library yang dibutuhkan:

```bash
pip install numpy pandas matplotlib opencv-python scikit-learn
```

2. Pastikan folder dataset berada sejajar dengan notebook.

3. Buka file:

```
UAS_PCD_NUR_ALFITRAH_24146074.ipynb
```

menggunakan:

- Jupyter Notebook
- JupyterLab
- Visual Studio Code

4. Jalankan seluruh cell secara berurutan.

---

# Library yang Digunakan

| Library | Fungsi |
|---------|--------|
| OpenCV | Membaca dan melakukan preprocessing citra |
| NumPy | Operasi array dan numerik |
| Pandas | Pengolahan data |
| Matplotlib | Visualisasi data |
| Scikit-learn | Pembuatan model MLP dan evaluasi |

---

# Saran Pengembangan

Beberapa pengembangan yang dapat dilakukan:

- Menggunakan metode ekstraksi fitur yang lebih baik.
- Menambahkan augmentasi data.
- Melakukan optimasi parameter model.
- Membandingkan MLP dengan metode Deep Learning seperti CNN.
- Menggunakan dataset yang lebih besar untuk meningkatkan akurasi.

---

# Lisensi dan Catatan

Project ini dibuat untuk memenuhi tugas **Ujian Akhir Semester (UAS) Pengolahan Citra Digital**.

Dataset dan program digunakan hanya untuk kepentingan akademik dan pembelajaran mengenai penerapan Machine Learning dalam klasifikasi citra.
