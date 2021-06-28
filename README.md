# Customer-Churn-Prediction

Dataset taken from : https://www.kaggle.com/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction

# Define Problems
- Mengetahui penyebab Customers melakukan Churn berdasarkan data yang diperoleh.

# Goals
- Mengetahui apakah Customers mayoritas melakukan Churn atau tidak.
- Mengetahui apakah pemberian Cashback setelah berbelanja efektif untuk menahan Customer Churn atau tidak.
- Mengetahui kebiasaan pelanggan dalam berbelanja melalui E-Commerce.
- Mengetahui apakah E-Commerce sudah memberikan pelayanan yang terbaik kepada Customers.

# Feature Selection
- Churn **(Target)**
- Tenure
- PreferredLoginDevice
- WarehouseToHome
- PreferredPaymentMode
- Gender
- PreferedOrderCat
- SatisfactionScore
- Complain
- OrderAmountHikeFromlastYear
- CouponUsed
- OrderCount
- DaySinceLastOrder
- CashbackAmount

# Conclusion Exploratory Data Analysis
- Customers yang melakukan Churn sebesar 16.83% dari seluruh total Customers.
- Berdasarkan data yang didapatkan, Customers yang melakukan Churn 65.83% menggunakan Mobile Phone, dan 34.17% menggunakan Computer.
- Mayoritas Customers yang melakukan Complain memilih untuk Churn sebesar 53.59%.
- Customers yang melakukan Churn di dominasi oleh Male sebesar 63.29%.
- Customers yang berdomisili di CityTier 1 dan 3 paling banyak melakukan Churn.
- Customers yang melakukan metode pembayaran Debit Card paling banyak melakukan Churn.
- Customers yang lebih tertarik pada Kategori Mobile Phone paling banyak melakukan Churn.
- Pengguna yang menghabiskan waktu 3 jam pada Aplikasi yang paling banyak melakukan Churn.
- Pengguna yang mendaftarkan Devicenya pada Apps, paling banyak melakukan Churn yaitu pada 4 Device.
- Berdasarkan SatisfactionScore Nilai 3 pada kepuasan yang diberikan oleh pelanggan yang paling banyak melakukan Churn.
- Berdasarkan MaritalStatus paling banyak status Single yang melakukan Churn.
- Berdasarkan data yang didapatkan, jumlah Alamat yang didaftarkan 2 dan 3 paling banyak melakukan Churn.
- Berdasarkan OrderAmountHikeFromlastYear kenaikan jumlah order dari tahun yang lalu mempengaruhi Churn pada customers.
- Penggunaan coupon 1 paling banyak yang melakukan Churn.
- Customers yang melakukan OrderCount 1 dan 2 paling banyak melakukan Churn.
- Mayoritas orang yang melakukan churn berkisaran pada orang yang berbelanja setelah 0-3 hari.
- Customers yang mendapatkan Cashback yang kategori high cenderung melakukan Churn.
- Customers yang Tenurenya 0 dan 1 bulan paling banyak melakukan Churn.

# Recommendation Exploratory Data Analysis
- Dikarenakan banyak dari pelanggan yang melakukan Churn pada Tenure nya 0 dan 1 bulan, maka dibuat agar Tenure kepada Customers memberikan benefit yang menarik, seperti iklan barang yang di preferred, diskon/cashback pada barang yang diinginkan, serta berlangganan dalam waktu yang lama lebih murah dibandingkan dengan berlangganan yang hanya 1 bulan.
- Aplikasi pada Mobile Phone dilakukan improvement dari segi tampilan dan performance agar pengguna dapat betah menggunakan Aplikasi E-Commerce.
- Untuk keluhan yang diberikan Customers agar ditanggapi oleh pihak E-Commerce sehingga keluhan yang diberikan oleh Customers dapat menjadi masukkan yang baik bagi E-Commerce.
- Diadakan promo yang menarik bagi Male/Pria agar untuk Gender Pria tidak melakukan Churn.
- Untuk Customer yang berlangganan Tenure dibawah 3 bulan tidak akan mendapatkan Coupon Cashback untuk menghindari adanya pemanfaatan promo cashback saja / Fraud.
- Pada E-Commerce untuk kategori Mobile Phone dilakukan improvement, dikarenakan banyak Customers yang Prefer terhadap kategori Mobile Phone melakukan Churn.

# Conclusion Machine Learning
- Model Machine Learning yang terbaik menggunakan Algoritma Decision Tree Classifier dengan hasil Recall (Training) yaitu 0.853562 dan Recall (Testing) yaitu 0.805263, dengan nilai False Negatif 37, False Positif 72, yang dilakukan Fine Tuning dengan parameter sebagai berikut :
    - class_weight = 0 : 0.365, 1 : 0.635
    - max_depth = None
    - max_features = None
    - min_samples_leaf = 3
    - min_samples_split = 23

# Recommendation Machine Learning
- Untuk False Negatif (Aktual Churn, Prediksi Tidak Churn) : Secara general dilakukan Optimize dan Improvement dari E-Commerce untuk menarik pelanggan, sehingga walau diprediksi Tidak Churn tetapi Aktualnya Churn dapat berpotensi untuk kembali menggunakan E-Commerce ini. Seperti pada Recommendation Exploratory Data Analysis kami.
- Untuk False Positif (Aktual Tidak Churn, Prediksi Churn) : Adain event undian untuk Free Tenure selama 3 bulan bagi Customers yang beruntung, tetapi saat undian berlangsung Free Tenure ini ditujukan kepada Customers yang False Positif, sehingga akan memberikan chance dia tetap stay selama prediksi kita Churn.
