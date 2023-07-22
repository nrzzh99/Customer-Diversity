# Customer-Diversity
Objective : Membuat model clustering untuk melakukan Customer Segmentation dari data kartu kredit dan menaikan insight perusahaan kepada pelanggan kartu kredit

## Latar Belakang Masalah :
Pelanggan kartu kredit berasal dari berbagai latar belakang dan memiliki kebutuhan, preferensi, dan perilaku yang berbeda. Menerapkan pendekatan yang seragam untuk semua pelanggan tidak efisien dan tidak efektif. Oleh karena itu, diperlukan strategi yang lebih terarah untuk memahami karakteristik dan kebutuhan pelanggan secara lebih mendalam. Dengan pemahaman yang lebih baik tentang segmen pelanggan, perusahaan dapat meningkatkan pengalaman pelanggan dan menawarkan solusi yang lebih sesuai

## Data yang Digunakan:
Data dalam proyek ini berasal dari BigQuery dengan Project "ftds-hacktiv8-project". Dataset ini terdiri dari 4475 entri dan 18 kolom. Data mencakup informasi tentang pengguna kartu kredit, seperti nilai pembelian, batas kredit, jumlah pembayaran, dan lain-lain. Data akan digunakan untuk melakukan clustering dan customer segmentation.

## Metode yang Digunakan:
Proyek ini menggunakan metode PCA (Principal Component Analysis) untuk mereduksi dimensi data dan algoritma K-Means Clustering untuk melakukan clustering dan customer segmentation. PCA digunakan untuk mengurangi dimensi data agar lebih efisien dan K-Means digunakan karena efisiensi dan kecepatannya dalam mengelompokkan data dengan banyak entri.

## Customer Segmentation:
Berdasarkan clustering, terdapat 6 cluster pelanggan dengan karakteristik yang berbeda. Setiap cluster memiliki kebutuhan dan perilaku yang berbeda. Dalam setiap cluster, perusahaan dapat memberikan reward atau tawaran yang sesuai untuk mendorong aktivitas pembelian, meningkatkan penggunaan kartu kredit, atau mempertahankan kepercayaan pelanggan.

## Kekurangan Project:
Meskipun hasil clustering telah memberikan insight yang berarti, proyek ini masih perlu ditingkatkan lagi agar model dapat mengelompokkan pelanggan dengan lebih baik. Peningkatan model dapat dilakukan dengan mencoba pendekatan clustering lainnya atau menggunakan lebih banyak fitur dan teknik pengolahan data.
