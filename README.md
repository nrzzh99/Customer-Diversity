# Customer-Diversity
Objective : Membuat model clustering untuk melakukan Customer Segmentation dari data kartu kredit dan menaikan insight perusahaan kepada pelanggan kartu kredit

Latar Belakang Masalah :
Pelanggan kartu kredit berasal dari berbagai latar belakang dan memiliki kebutuhan, preferensi, dan perilaku yang berbeda. Menerapkan pendekatan yang seragam untuk semua pelanggan tidak efisien dan tidak efektif. Oleh karena itu, diperlukan strategi yang lebih terarah untuk memahami karakteristik dan kebutuhan pelanggan secara lebih mendalam. Dengan pemahaman yang lebih baik tentang segmen pelanggan, perusahaan dapat meningkatkan pengalaman pelanggan dan menawarkan solusi yang lebih sesuai

Data ini berasal dari Bigquery dengan Project ftds-hacktiv8-project
Dataset ini terdiri dari 4475 entri dan 18 kolom
Sebagian besar kolom merupakan tipe data float64, sementara beberapa lainnya merupakan tipe data int64

Metode yg digunakan :
Menggunakan PCA untuk mereduksi dimensi datanya
algoritma yg digunakan adalah K-Means Clustering karena cepat dan efisien untuk digunakan terutama untuk data yg banyak

Kesimpulan EDA :

- dari kolom purchase menunjukkan variasi yang cukup besar dalam jumlah pembelian pelanggan. Minimum nilai pembelian adalah 0, yang menunjukkan bahwa ada pelanggan yang tidak melakukan pembelian sama sekali. Sedangkan nilai maksimum pembelian 49039.57, yang menunjukkan bahwa ada pelanggan yang melakukan pembelian dalam jumlah yang sangat besar.
banyak pelanggan melakukan pembelian dengan nilai rendah atau sedang, dibandingkan dengan pembelian dengan nilai yang sangat tinggi
- mayoritas pelanggan memiliki batas kredit dan jumlah pembelian yang relatif rendah (dalam kisaran 0-20000). Namun, terdapat sejumlah besar data yang terletak di luar kisaran tersebut (outliers), yang menunjukkan adanya sejumlah pelanggan yang melakukan pembelian dalam jumlah yang jauh lebih besar atau memiliki batas kredit yang lebih tinggi.
- mayoritas pelanggan memiliki batas kredit yang relatif rendah (dalam kisaran 150-6000), dengan nilai rata-rata sebesar 4494.02. Namun, terdapat pula sejumlah pelanggan yang memiliki batas kredit yang lebih tinggi, bahkan mencapai nilai tertinggi 30000
- sebagian besar pelanggan melakukan pembayaran dengan jumlah yang relatif kecil dan hanya sedikit pelanggan yang melakukan pembayaran dengan jumlah yang lebih besar
- terdapat beberapa pengguna kartu kredit yang membayar nilai minimum payments dengan jumlah yang sangat besar. Namun, mayoritas pengguna kartu kredit membayar nilai minimum payments pada rentang yang cukup wajar.
- sebagian besar pengguna memiliki tenure selama 12 bulan, sedangkan pengguna dengan tenure kurang dari 12 bulan jauh lebih sedikit.

Cluster 0: Pelanggan dalam cluster ini sering melakukan pembelian secara angsuran. Untuk meningkatkan aktivitas pembelian, perusahaan bisa memberikan reward berupa potongan bunga atau keringanan biaya bunga untuk pembelian secara angsuran.
Cluster 1: Pelanggan dalam cluster ini memiliki pembelian yang tinggi dalam pembelian satu kali (oneoff). Perusahaan bisa memberikan reward berupa diskon atau kupon belanja untuk pembelian satu kali agar dapat mendorong pelanggan untuk melakukan lebih banyak pembelian.
Cluster 2: Pelanggan dalam cluster ini sering melakukan penarikan tunai. Perusahaan bisa memberikan reward berupa keringanan biaya atau potongan bunga untuk transaksi pembelian agar dapat mendorong pelanggan untuk lebih sering melakukan pembelian dengan kartu kredit daripada melakukan penarikan tunai.
Cluster 3: Pelanggan dalam cluster ini memiliki pembelian dan limit kredit yang tinggi. Untuk mempertahankan kepercayaan pelanggan, perusahaan bisa memberikan reward berupa perlindungan asuransi atau keringanan biaya kartu kredit.
Cluster 4: Pelanggan dalam cluster ini sering melakukan penarikan tunai dan pembelian dengan frekuensi rendah. Perusahaan bisa memberikan reward berupa keringanan biaya atau diskon belanja untuk pembelian dengan frekuensi tertentu agar dapat mendorong pelanggan untuk lebih sering menggunakan kartu kredit.
Cluster 5: Pelanggan dalam cluster ini memiliki saldo, pembelian, dan limit kredit yang sangat tinggi, namun jarang melakukan pembayaran penuh dan pembelian secara angsuran. Perusahaan bisa memberikan reward berupa poin reward atau kupon belanja untuk pembayaran penuh atau pembelian secara angsuran untuk mendorong pelanggan agar lebih aktif menggunakan kartu kredit secara optimal.

- masih perlu ditingkatkan lagi modelnya, agar model dapat mengelompokan modelnya dengan baik antara para pengguna kartu kredit bank
- jika membandingkan antara menggunakan 5 komponen ata 2 komponen, tidak terlihat perbedaannya , namun jika dilihat dari silhouette scorenya terdapat perbedaan, untuk pca dengan 5 komponen mendapat score Silhouette Score: 0.393606147927086 sedangkan untuk yg 2 komponen hanya Silhouette Score: 0.3158495200579976
