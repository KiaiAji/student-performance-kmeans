# Student Performance Clustering Using K-Means

## Deskripsi Proyek

Proyek ini merupakan implementasi **Machine Learning dengan algoritma K-Means Clustering** untuk mengelompokkan mahasiswa berdasarkan performa akademik dan perilaku kehadiran.

Dataset yang digunakan adalah `student_dropout_behavior_dataset.csv`, yang berisi informasi mengenai nilai kuis, nilai ujian, IPK sebelumnya, dan kehadiran kuliah serta praktikum.

## Tujuan

- Menerapkan algoritma K-Means untuk mengelompokkan mahasiswa.
- Menganalisis pola nilai akademik dan kehadiran mahasiswa.
- Membandingkan karakteristik setiap cluster.
- Memvisualisasikan hasil clustering untuk mempermudah analisis.

## Dataset

Nama dataset: `student_dropout_behavior_dataset.csv`

Dataset memiliki 300 baris dan 16 kolom.

Fitur yang digunakan dalam proses clustering:
- `quiz1_marks`
- `quiz2_marks`
- `quiz3_marks`
- `midterm_marks`
- `final_marks`
- `previous_gpa`
- `lecture_attendance_pct` — persentase kehadiran kuliah yang dihitung dari data asli.
- `lab_attendance_pct` — persentase kehadiran praktikum yang dihitung dari data asli.

Kolom `assignments_submitted` tidak digunakan karena seluruh nilainya kosong. Kolom identitas mahasiswa juga tidak digunakan sebagai fitur clustering.

## Metode

Tahapan analisis yang dilakukan:

1. Membaca dataset menggunakan Pandas.
2. Memeriksa dan menangani nilai yang kosong.
3. Menghitung persentase kehadiran kuliah dan praktikum.
4. Melakukan standardisasi menggunakan `StandardScaler`.
5. Menerapkan K-Means dengan jumlah cluster sebanyak 3.
6. Menganalisis rata-rata fitur pada setiap cluster.
7. Memvisualisasikan cluster menggunakan PCA dan grafik nilai akhir terhadap kehadiran.
8. Menyimpan hasil clustering ke file CSV.

## Teknologi

- Python
- Pandas
- Matplotlib
- Scikit-learn
- K-Means Clustering
- Principal Component Analysis (PCA)

## Struktur Repository

```text
student-performance-kmeans/
├── main.py
├── student_dropout_behavior_dataset.csv
├── requirements.txt
├── README.md
└── hasil_clustering_mahasiswa.csv
```

File hasil clustering akan dibuat setelah program dijalankan. Dataset dapat disertakan sesuai izin distribusi dan ketentuan lisensinya.

## Instalasi

Pastikan Python sudah terpasang, kemudian instal pustaka yang diperlukan:

```bash
pip install pandas scikit-learn matplotlib
```

## Hasil dan Analisis

Hasil clustering membagi mahasiswa menjadi tiga kelompok berdasarkan pola nilai dan kehadiran.

Analisis dilakukan dengan membandingkan rata-rata nilai kuis, ujian, IPK sebelumnya, dan persentase kehadiran setiap cluster. Karakteristik kelompok ditentukan berdasarkan hasil pengolahan data, bukan berdasarkan nomor cluster semata.

## Kesimpulan

K-Means dapat digunakan untuk menemukan kelompok mahasiswa dengan karakteristik akademik dan kehadiran yang berbeda. Hasilnya dapat menjadi analisis awal untuk memahami pola performa mahasiswa.

Clustering tidak secara langsung membuktikan penyebab penurunan prestasi atau risiko putus kuliah. Interpretasi hasil perlu mempertimbangkan karakteristik dataset dan keterbatasan fitur yang tersedia.

## Catatan

Proyek ini dibuat untuk keperluan pembelajaran Machine Learning. Hasil clustering merupakan analisis eksploratif dan tidak seharusnya menjadi satu-satunya dasar pengambilan keputusan akademik.
