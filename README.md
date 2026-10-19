# Student Performance Clustering Using K-Means

## Deskripsi Proyek

Proyek ini merupakan implementasi Machine Learning menggunakan algoritma **K-Means Clustering** untuk mengelompokkan mahasiswa berdasarkan performa akademik dan perilaku kehadiran.

Dataset yang digunakan adalah `student_dropout_behavior_dataset.csv`, yang berisi data nilai kuis, ujian tengah semester, ujian akhir, IPK sebelumnya, serta kehadiran kuliah dan praktikum.

Proyek ini dibuat untuk memenuhi tugas mata kuliah Machine Learning.

## Tujuan

- Menerapkan algoritma K-Means Clustering pada data mahasiswa.
- Mengelompokkan mahasiswa menjadi tiga cluster.
- Menganalisis pola performa akademik dan kehadiran.
- Memvisualisasikan hasil clustering.
- Menyimpan hasil pengelompokan dalam file CSV.

## Dataset

Nama file: `student_dropout_behavior_dataset.csv`

Dataset terdiri dari 300 baris dan 16 kolom.

Fitur yang digunakan:
- `quiz1_marks`: nilai kuis 1.
- `quiz2_marks`: nilai kuis 2.
- `quiz3_marks`: nilai kuis 3.
- `midterm_marks`: nilai ujian tengah semester.
- `final_marks`: nilai ujian akhir.
- `previous_gpa`: IPK sebelumnya.
- `lecture_attendance_pct`: persentase kehadiran kuliah.
- `lab_attendance_pct`: persentase kehadiran praktikum.

Kolom `assignments_submitted` tidak digunakan karena seluruh nilainya kosong. Kolom identitas mahasiswa juga tidak digunakan dalam proses clustering.

## Algoritma dan Metode

Algoritma yang digunakan adalah **K-Means**, salah satu metode Unsupervised Learning.

Tahapan pengolahan data:

1. Membaca dataset menggunakan Pandas.
2. Memeriksa nilai kosong.
3. Menghitung persentase kehadiran kuliah dan praktikum.
4. Memilih fitur yang relevan untuk clustering.
5. Melakukan standardisasi menggunakan `StandardScaler`.
6. Menerapkan K-Means dengan `n_clusters=3`.
7. Menganalisis jumlah dan rata-rata fitur setiap cluster.
8. Memvisualisasikan hasil clustering menggunakan PCA dan scatter plot.
9. Menyimpan hasil ke file CSV.

## Teknologi yang Digunakan

- Python
- Pandas
- Matplotlib
- Scikit-learn
- K-Means Clustering
- Principal Component Analysis (PCA)
- Google Colab / Jupyter Notebook

## Struktur Repository

```text
student-performance-kmeans/
├── README.md
├── requirements.txt
├── student_dropout_behavior_dataset.csv
├── student_performance_kmeans.ipynb
└── hasil_clustering_mahasiswa.csv
```

## Instalasi

Pastikan Python sudah terpasang. Instal library yang diperlukan menggunakan perintah berikut:

```bash
pip install -r requirements.txt
```

Isi file `requirements.txt`:

```text
pandas
scikit-learn
matplotlib
```

## Cara Menjalankan

1. Buka file `student_performance_kmeans.ipynb` di Google Colab atau Jupyter Notebook.
2. Pastikan dataset `student_dropout_behavior_dataset.csv` tersedia.
3. Jalankan setiap cell secara berurutan dari atas ke bawah.
4. Periksa ringkasan jumlah mahasiswa dan rata-rata fitur setiap cluster.
5. Amati grafik hasil clustering.
6. Unduh atau periksa file `hasil_clustering_mahasiswa.csv` yang dihasilkan.

## Hasil Clustering

Berdasarkan pengujian pada dataset, K-Means menghasilkan tiga cluster dengan pembagian berikut:

| Cluster | Jumlah Mahasiswa |
|---|---:|
| Cluster 0 | 80 |
| Cluster 1 | 114 |
| Cluster 2 | 106 |
| **Total** | **300** |

Karakteristik cluster dianalisis dengan membandingkan rata-rata nilai akademik, IPK sebelumnya, serta persentase kehadiran kuliah dan praktikum.

Nomor cluster hanya merupakan label kelompok yang dihasilkan algoritma. Penamaan kelompok berdasarkan tingkat performa harus ditentukan setelah mengevaluasi karakteristik masing-masing cluster.

## Kesimpulan

Algoritma K-Means dapat digunakan untuk mengelompokkan mahasiswa berdasarkan kemiripan karakteristik akademik dan kehadiran. Hasil clustering membantu mengidentifikasi pola yang berbeda di antara kelompok mahasiswa.

Analisis ini bersifat eksploratif. Hasil clustering tidak secara langsung membuktikan penyebab penurunan prestasi atau risiko putus kuliah.
