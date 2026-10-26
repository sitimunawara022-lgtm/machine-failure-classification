# Machine Failure Classification
## Tugas Proyek Artificial Intelligence (AI)

**Klasifikasi Kegagalan Mesin Berbasis Machine Learning**

## 1. Deskripsi Proyek

Proyek ini menerapkan Machine Learning untuk mengklasifikasikan kegagalan mesin (*Machine Failure*) berdasarkan data historis operasional mesin. Penelitian ini membandingkan dua algoritma, yaitu Logistic Regression sebagai model baseline dan Random Forest sebagai model ensemble.

## 2. Tujuan Proyek

Tujuan proyek ini adalah mengetahui kemampuan kedua algoritma dalam membedakan kondisi mesin normal dan kondisi mesin yang mengalami kegagalan. Hasil klasifikasi diharapkan dapat mendukung analisis kondisi mesin dalam penerapan *Predictive Maintenance* di sektor manufaktur.

## 3. Anggota Kelompok

| No | Nama Mahasiswa | NIM | Program Studi |
|---:|---|---|---|
| 1 | Siti Munawara | F1G125018 | Ilmu Komputer |
| 2 | Aghy Hutama Prawira S | F1G125023 | Ilmu Komputer |
| 3 | Mawar Putri Rabia | F1G125062 | Ilmu Komputer |

## 4. Latar Belakang

Mesin merupakan komponen penting dalam proses produksi industri manufaktur. Kegagalan mesin yang terjadi secara mendadak dapat mengganggu proses produksi, meningkatkan biaya perbaikan, dan menurunkan efisiensi operasional.

Data historis operasional mesin dapat digunakan untuk mempelajari pola kegagalan. Dengan memanfaatkan Machine Learning, data tersebut dapat diolah menjadi model klasifikasi yang membantu mengidentifikasi kondisi mesin yang berpotensi mengalami kegagalan.

Proyek ini menggunakan Logistic Regression dan Random Forest untuk membandingkan performa model dalam mendeteksi kegagalan mesin berdasarkan parameter operasionalnya.

## 5. Rumusan Masalah

1. Apakah data historis operasional mesin dapat digunakan untuk mengklasifikasikan kegagalan mesin?
2. Bagaimana perbandingan performa Logistic Regression dan Random Forest dalam mengklasifikasikan kegagalan mesin?

## 6. Tujuan Riset

1. Menerapkan Machine Learning untuk melakukan klasifikasi biner terhadap kegagalan mesin.
2. Membandingkan performa Logistic Regression dan Random Forest berdasarkan metrik evaluasi model.

## 7. Dataset

Dataset yang digunakan adalah **AI4I 2020 Predictive Maintenance Dataset** dari UCI Machine Learning Repository.

Dataset ini terdiri atas 10.000 observasi dan 14 kolom yang mencakup informasi mengenai jenis mesin, kondisi operasional, dan indikator kegagalan mesin.

## 8. Fitur Dataset

| No | Fitur | Keterangan |
|---:|---|---|
| 1 | Type | Jenis mesin |
| 2 | Air Temperature | Suhu udara |
| 3 | Process Temperature | Suhu proses mesin |
| 4 | Rotational Speed | Kecepatan putaran mesin |
| 5 | Torque | Torsi atau gaya putar mesin |
| 6 | Tool Wear | Tingkat keausan alat |
| 7 | Machine Failure | Target klasifikasi kegagalan mesin |

### Target Klasifikasi

| Nilai | Keterangan |
|---:|---|
| 0 | Normal |
| 1 | Failure (Kegagalan) |

## 9. Preprocessing Data

Tahapan preprocessing yang dilakukan dalam proyek ini meliputi:

- **Pemeriksaan Data:** Memeriksa struktur data, tipe data, nilai kosong, dan data duplikat.
- **Penghapusan Identifier:** Menghapus kolom identitas yang tidak digunakan sebagai fitur prediksi.
- **Encoding:** Mengubah fitur kategorikal menjadi format numerik agar dapat diproses oleh model.
- **Pembagian Data:** Membagi dataset menjadi data latih dan data uji.
- **Standardisasi:** Menyamakan skala fitur numerik sesuai kebutuhan algoritma.

## 10. Algoritma Machine Learning

### 10.1 Logistic Regression

Logistic Regression digunakan sebagai model baseline untuk mengklasifikasikan kegagalan mesin berdasarkan hubungan antara fitur operasional dan target klasifikasi. Algoritma ini relatif sederhana dan efisien, tetapi memiliki keterbatasan dalam menangkap pola hubungan yang kompleks.

### 10.2 Random Forest

Random Forest merupakan algoritma ensemble yang menggabungkan banyak pohon keputusan untuk menghasilkan prediksi. Algoritma ini mampu mempelajari pola yang lebih kompleks dan hubungan nonlinier antarfitur operasional mesin.

## 11. Hasil Perbandingan Model

Evaluasi model dilakukan menggunakan Accuracy, Precision, Recall, dan F1-Score.

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 0.97 | 0.64 | 0.10 | 0.18 |
| Random Forest | 0.98 | 0.88 | 0.53 | 0.66 |

Berdasarkan hasil evaluasi, Random Forest menunjukkan performa yang lebih baik dibandingkan Logistic Regression pada seluruh metrik yang ditampilkan. Random Forest memperoleh Accuracy sebesar 98%, Precision sebesar 88%, Recall sebesar 53%, dan F1-Score sebesar 66%.

Walaupun memiliki performa lebih baik, nilai Recall Random Forest masih menunjukkan bahwa sebagian kasus kegagalan mesin belum berhasil terdeteksi. Oleh karena itu, model masih perlu dikembangkan agar dapat mengenali kegagalan mesin dengan lebih baik.

## 12. Hubungan dengan SDG 9 Target 9.5

Proyek ini berkaitan dengan **Sustainable Development Goal 9 (SDG 9): Industry, Innovation and Infrastructure**, khususnya Target 9.5 yang menekankan penguatan penelitian ilmiah, kemampuan teknologi, dan inovasi industri.

Penerapan Machine Learning untuk klasifikasi kegagalan mesin merupakan salah satu bentuk pemanfaatan teknologi analitik dalam mendukung sektor manufaktur. Dengan menganalisis data historis, model dapat membantu mengidentifikasi pola kegagalan dan mendukung pengambilan keputusan terkait pemeliharaan mesin.

## 13. Teknologi yang Digunakan

| No | Teknologi |
|---:|---|
| 1 | Python |
| 2 | Pandas |
| 3 | NumPy |
| 4 | Scikit-learn |
| 5 | Jupyter Notebook / Google Colab |
| 6 | GitHub |

## 14. Struktur Repository

```text
klasifikasi-kegagalan-mesin/
│
├── Klasifikasi_Kegagalan_Mesin_Machine_Learning.ipynb
├── ai4i2020 (1).csv
├── app.py
└── README.md
```

### Keterangan File

| Nama File | Deskripsi |
|---|---|
| `Klasifikasi_Kegagalan_Mesin_Machine_Learning.ipynb` | Notebook analisis data, preprocessing, pelatihan, dan evaluasi model. |
| `ai4i2020 (1).csv` | Dataset operasional mesin. |
| `app.py` | Implementasi aplikasi prediksi. |
| `README.md` | Dokumentasi proyek. |

## 15. Kesimpulan

Proyek ini menerapkan Machine Learning untuk mengklasifikasikan kegagalan mesin menggunakan algoritma Logistic Regression dan Random Forest. Berdasarkan hasil evaluasi, Random Forest menunjukkan performa yang lebih baik dengan Accuracy sebesar 98% dan F1-Score sebesar 66%.

Meskipun demikian, nilai Recall sebesar 53% menunjukkan bahwa model masih belum berhasil mendeteksi seluruh kasus kegagalan mesin. Pengembangan lebih lanjut diperlukan untuk meningkatkan kemampuan model dalam mengenali kondisi mesin yang berpotensi mengalami kegagalan.

Proyek ini diharapkan dapat menjadi dasar pengembangan sistem Predictive Maintenance untuk mendukung efisiensi operasional industri.

