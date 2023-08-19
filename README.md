# **Predict Customer Personality to Boost Marketing Campaign by using Machine Learning**
## Background
Suatu perusahaan dapat berkembang pesat bila mengetahui perilaku kepribadian pelanggannya, sehingga dapat memberikan pelayanan dan manfaat yang lebih baik kepada pelanggan yang berpotensi menjadi pelanggan setia. Perusahaan perlu mengetahui perilaku pelanggan untuk meningkatkan kampanye pemasaran.

## Goal
Tingkatkan kinerja kampanye pemasaran dan targetkan pelanggan yang tepat untuk dapat melakukan transaksi di platform perusahaan.

## Objective

Membuat model prediksi cluster menggunakan unsupervised learning sehingga memudahkan perusahaan dalam mengambil keputusan.

## Data Overview

Dataset berisi 2.240 baris data dan 30 fitur fitur perilaku pelanggan yang melakukan transaksi dan berinteraksi di platform kami.

## Tools
Pada proyek ini saya menggunakan python sebagai bahasa pemrograman; Jupyter sebagai notebook; pandas, numpy, sklearn dan python ke bagian preprocessing dan machine learning; kombinasi matplotlib dan seaborn library untuk menghasilkan visualisasi data.

### Content
## Exploratory Data Analysis
Pada bagian ini terdapat beberapa proses seperti penanganan missing value dengan menggunakan MICE with Light GBM dan penanganan duplikasi data, kemudian seleksi fitur menggunakan metode LRFM (Recency, Frequency, Monetary, Loyality), penanganan outlier dengan Manually Trimmed (menghapus nilai yang sangat jauh di tahun 1893-1900 pada kolom Year Birth, dan menghapus nilai yang sangat tinggi sebesar 666M pada kolom Income), fitur transformasi menggunakan Yeo Johnson Transformation, Normalization dengan Minmaxscaler dan Feature Scalling dengan StandardScaler.

## Data Modeling
Menggunakan K-Means Clustering dengan metode cross-validation elbow pada skor inersia dan silhoutte.

## Customer Personality Analaysis for Marketing Retargeting
Berdasarkan model saya, ada 4 kelompok pelanggan:

 **1. Cluster 0 (Loyal Customer):**
 - Kelompok ini adalah kelompok dengan jumlah pelanggan ketiga terbesar sebanyak 550 orang.
 - Pelanggan di kelompok ini mempunyai rata-rata waktu sejak pembelian terakhir (22 hari), dan rata-rata total pembelian (21 items) itu berarti mereka berbelanja dalam waktu yang dekat, sering berbelanja dan mereka menghabiskan banyak uang di platform kami (sekitar Rp 919k/tahun).
 - Pelanggan dalam kelompok ini kurang dalam merespon kampanye tetapi kelompok ini mengunjungi website cukup sering dengan median sebanyak 5 kali dalam sebulan.
 
 **2. Cluster 1 (Need Attention):**
 - Kelompok ini adalah kelompok dengan jumlah pelanggan terbesar sebanyak 941 orang.
 - Pelanggan di kelompok ini mempunyai rata-rata waktu sejak pembelian terakhir (48 hari), dan rata-rata total pembelian (7 items) itu berarti mereka sudah cukup lama tidak berbelanja, bukan pembeli rutin dan mereka menghabiskan sedikit uang di platform kami (sekitar Rp 79k/tahun).
 - Pelanggan dalam kelompok ini paling sedikit dalam merespon kampanye tetapi kelompok ini mengunjungi website paling sering dengan median sebanyak 7 kali dalam sebulan.
 
**3. Cluster 2 (At Risk):**
 - Kelompok ini adalah kelompok dengan jumlah pelanggan kedua terbesar sebanyak 609 orang.
 - Pelanggan di kelompok ini mempunyai rata-rata waktu sejak pembelian terakhir (73 hari) yang berarti paling lama tidak berbelanja di platform kami dibanding kelompok lainnya, dan rata-rata total pembelian (20 items) itu berarti mereka sering berbelanja dan menghabiskan banyak uang di platform kami (sekitar Rp 930k/tahun).
 - Pelanggan dalam kelompok ini kurang dalam merespon kampanye tetapi kelompok ini mengunjungi website cukup sering dengan median sebanyak 5 kali dalam sebulan.

**4. Cluster 3 (Potential Loyalist):**
 - Kelompok ini adalah kelompok dengan jumlah pelanggan terkecil sebanyak 136 orang.
 - Pelanggan di kelompok ini mempunyai rata-rata waktu sejak pembelian terakhir (48 hari), dan rata-rata total pembelian (21 items) itu berarti mereka sering berbelanja dan menghabiskan paling banyak uang di platform kami (sekitar Rp 1.5jt/tahun) dibanding kelompok lain.
 - Pelanggan dalam kelompok ini yang paling banyak merespon kampanye yaitu sebanyak 2 kali tetapi kelompok ini mengunjungi website hanya 3 kali dalam sebulan.

## Business Recommendation 
 **1. Loyal Customer:**

 - **Pertahankan Keterlibatan:** Lanjutkan komunikasi secara teratur melalui kampanye pemasaran yang relevan dan menarik.
 - **Penawaran Khusus:** Berikan penawaran eksklusif atau diskon kepada pelanggan sebagai hadiah atas keterlibatan mereka.
 - **Program Hadiah:** Pertimbangkan untuk memperkenalkan program hadiah yang menawarkan insentif untuk partisipasi aktif dan pembelian.
 
**2. Need Attention Customer:**

 - **Reaktivasi:** Kirim tawaran menarik atau diskon untuk mendorong pelanggan berbelanja kembali.
 - **Penawaran Khusus:** Berikan penawaran khusus atau diskon terbatas untuk merangsang pembelian lebih lanjut.
 - **Konten Edukatif:** Kirim konten yang memberikan informasi berharga tentang produk atau metode penggunaan untuk meningkatkan minat dan keterlibatan.
 
 **3.  At Risk Customer:**

 - **Kampanye Personalisasi:** Upayakan untuk mengirimkan kampanye yang lebih relevan dan menarik kepada pelanggan dalam kelompok ini.
 - **Penawaran Eksklusif:** Berikan penawaran eksklusif atau diskon khusus kepada pelanggan dalam kelompok ini. Ini dapat menjadi insentif tambahan bagi mereka untuk berbelanja kembali meskipun jarang menerima kampanye pemasaran.
 - **Program Loyalitas:** Ajak mereka untuk bergabung dalam program loyalitas yang menawarkan manfaat eksklusif bagi pelanggan setia.
 - **Eksperimen dengan Media dan Saluran Berbeda:** Cobalah menguji kampanye melalui media atau saluran yang berbeda. Beberapa pelanggan mungkin merespons lebih baik jika kampanye disampaikan melalui email, SMS, media sosial, atau periklanan online. Eksperimen ini dapat membantu kami menemukan saluran komunikasi yang paling efektif untuk kelompok ini.
 
 **4. Potential Loyalist Customer:**

 - **Kampanye Personalisasi:** Tingkatkan upaya untuk mengirim kampanye pemasaran yang lebih personal dan relevan kepada pelanggan dalam klaster ini.
 - **Penawaran Diskon:** Berikan penawaran khusus atau diskon kepada pelanggan untuk mendorong pembelian lebih lanjut.
 - **Program Loyalitas:** Ajak pelanggan untuk bergabung dengan program loyalitas yang menawarkan insentif tambahan untuk pembelian tinggi.
 - **Pemberitahuan Produk Baru:** Informasikan mereka tentang produk-produk baru yang sejalan dengan minat dan preferensi mereka.
 
## Potential Impact
Jika kita bisa memprioritaskan pada semua kelompok dan mereka tidak beralih (churn), kita masih memiliki potensi GMV sekitar Rp 1,3 miliar/tahun

• Loyal Customer = IDR 505jt/tahun
• Need Attention Customer = IDR 74jt/tahun
• At Risk Customer = IDR 566jt/tahun
• Potential Loyalist Customer= IDR 208jt/tahun
