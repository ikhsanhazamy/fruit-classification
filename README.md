# Klasifikasi Buah: Orange vs Grapefruit

## 1. Deskripsi Dataset
Dataset yang digunakan berasal dari Kaggle:  
https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit  

Dataset ini berisi karakteristik buah citrus dengan dua label:
- Orange (Jeruk)
- Grapefruit (Anggur)

Tujuan dari penelitian ini adalah membangun model klasifikasi untuk menentukan jenis buah berdasarkan fitur yang tersedia.

---

## 2. Tujuan
Membandingkan performa tiga algoritma machine learning:
- Decision Tree
- Naive Bayes
- Support Vector Machine (SVM)

---

## 3. Tahapan Pembuatan Model

### 3.1 Data Understanding
Dilakukan eksplorasi awal dataset menggunakan:
- head()
- info()
- describe()

Hasil:
Dataset terdiri dari fitur numerik sehingga dapat langsung digunakan untuk model klasifikasi.

---

### 3.2 Data Preprocessing
Langkah yang dilakukan:
- Encoding label:
  - orange → 0
  - grapefruit → 1
- Memisahkan fitur (X) dan target (y)
- Normalisasi data menggunakan StandardScaler (untuk SVM)

---

### 3.3 Exploratory Data Analysis (EDA)
Dilakukan analisis:
- Distribusi kelas
- Korelasi antar fitur (heatmap)

Hasil:
Terdapat hubungan antar beberapa fitur yang dapat mempengaruhi performa model, khususnya Naive Bayes.

---

### 3.4 Data Splitting
Dataset dibagi menjadi:
- 80% data training
- 20% data testing

Tujuan:
Menghindari overfitting dan menguji kemampuan generalisasi model.

---

### 3.5 Training Model

#### a. Decision Tree
Model berbasis pohon keputusan.

Kelebihan:
- Mudah dipahami
- Tidak memerlukan scaling

Kekurangan:
- Rentan overfitting

---

#### b. Naive Bayes
Model probabilistik berdasarkan Teorema Bayes.

Kelebihan:
- Cepat
- Sederhana

Kekurangan:
- Mengasumsikan fitur independen

---

#### c. Support Vector Machine (SVM)
Model yang mencari hyperplane optimal untuk memisahkan kelas.

Kelebihan:
- Akurasi tinggi
- Baik untuk data kompleks

Kekurangan:
- Sensitif terhadap scaling

---

### 3.6 Evaluasi Model

Metode evaluasi:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

---

## 4. Hasil Perbandingan Model

Berdasarkan hasil eksperimen:

- Decision Tree:  0.9435
- Naive Bayes:  0.92
- SVM: 0.937

Grafik menunjukkan bahwa seluruh model memiliki performa tinggi, namun terdapat perbedaan akurasi.

---

## 5. Analisis

- Decision Tree memiliki performa baik, namun berpotensi overfitting.
- Naive Bayes memiliki performa paling rendah karena asumsi independensi fitur tidak sepenuhnya terpenuhi.
- SVM memberikan performa terbaik karena mampu memaksimalkan pemisahan antar kelas.

---

## 6. Kesimpulan

Model terbaik dalam penelitian ini adalah **Support Vector Machine (SVM)** karena memiliki akurasi tertinggi dan performa yang paling stabil.

Dataset ini relatif mudah dipelajari karena memiliki pola yang cukup jelas, sehingga ketiga model mampu mencapai akurasi tinggi.

---

## 7. Implementasi

Implementasi dilakukan menggunakan Python dengan library:
- pandas
- scikit-learn
- matplotlib
- seaborn
