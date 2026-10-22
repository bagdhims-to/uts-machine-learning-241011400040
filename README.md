# UTS Machine Learning

## Identitas
- Nama: Dhimas Baga Yulistyana
- NIM: 241011400040
- Kelas: Reg B

## Deskripsi
Tugas ini menerapkan Linear Regression untuk memperkirakan penjualan berdasarkan biaya iklan dan Logistic Regression untuk mengklasifikasikan email spam berdasarkan jumlah link dan kata promosi.

Model dan metrik utama diimplementasikan menggunakan NumPy. Evaluasi dilakukan pada data testing dengan `RANDOM_STATE = 40`.

## Ringkasan Hasil

### Linear Regression
| Metrik data testing | Hasil |
|---|---:|
| MAE | 8.2791 juta Rp |
| RMSE | 10.3049 juta Rp |
| R2 | 0.7008 |

Model menjelaskan sekitar 70.08% variasi penjualan pada data testing. Prediksi memiliki RMSE sekitar 10.30 juta rupiah.

### Logistic Regression
Pada threshold default `0.5`:

| Metrik data testing | Hasil |
|---|---:|
| Accuracy | 0.8667 |
| Precision | 0.9000 |
| Recall | 0.9000 |
| F1-score | 0.9000 |
| Confusion matrix | `[[4, 1], [1, 9]]` |

Confusion matrix menggunakan urutan `[[TN, FP], [FN, TP]]`.

Threshold pilihan untuk prediksi email baru adalah `0.7`. Pada data testing, threshold ini menghasilkan precision `1.0000`, recall `0.7000`, dan confusion matrix `[[5, 0], [3, 7]]`. Threshold yang lebih tinggi mengurangi false positive pada sampel testing ini, tetapi lebih banyak spam terlewat sebagai false negative.

## File
- `tugas_UTS.ipynb`: notebook pengerjaan dan visualisasi.
- `Ads_Data.csv`: dataset biaya iklan dan penjualan.
- `Email_Data.csv`: dataset klasifikasi email spam.

Hasil metrik berasal dari split testing pada notebook. Karena ukuran data testing kecil, hasil dapat berubah jika pembagian data atau konfigurasi model berubah.