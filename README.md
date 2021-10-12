# KnightsOfData_JC_DS_VL_01_FinalProject

# :tropical_fish:Churn Prediction and Analysis:fish:
![churnfish](https://github.com/PurwadhikaDev/KnightsOfData_JC_DS_VL_01_FinalProject/blob/master/images/churnFish.png)
Customer churn mengacu pada hilangnya klien atau pelanggan yang sudah ada.<br>
Dari analysis ini, kita bisa mengidentifikasi user yang cenderung akan berhenti menggunakan aplikasi ecommerce dan meninggalkan perusahaan.

# whats the problem? :thinking:
### Define Problem
Identifikasi pengguna berhenti menggunakan ecommerce 'ijo' ditandai dengan tidak adanya transaksi dalam kurun waktu tertentu, atau akun tersebut tidur (dormant account).

1. Salah satu dampak dari persaingan di dunia ecommerce adalah churn, sebuah kondisi dimana user berpindah dari satu ecommerce ke ecommerce yang lain.
2. Semakin tinggi churn rate, semakin kecil revenue yang akan perusahaan raih di masa mendatang.
3. Biaya untuk memperoleh user baru cukup besar, namun jauh lebih besar biaya kehilangan user karena kita kehilangan bisnis sama sekali,
ditambah lagi user yang kecewa akan bercerita kepada banyak orang yang memengaruhi orang lain untuk tidak menggunakan layanan dari perusahaan kita.

### Objective
Apakah ada Faktor penting yang paling berpotensi membuat customer menjadi churn.

# why the problem is important to solve? :hushed:
**Mengapa itu penting?**<br>
Bisnis sering kali harus berinvestasi dalam jumlah besar untuk menarik user baru, jadi setiap kali user keluar, itu berarti kerugian investasi yang signifikan.
Mampu memprediksi kapan user kemungkinan akan pergi dan menawarkan mereka program yang sesuai untuk tetap tinggal di aplikasi kita itu merupakan penghematan besar bagi bisnis.

# what is the goal/target of solving the problem?
### Goals :sunglasses:
* Tujuan utamanya adalah untuk memperluas cakupan user dan mendapatkan lebih banyak loyalitas user.
* Serta untuk berhasil di pasar ini terletak pada user itu sendiri,
maka kita harus berusaha untuk memuaskan setiap user dengan karakteristiknya masing-masing, serta menurunkan resiko churn untuk user lainnya di waktu yang akan datang.

# Data Source
[ECommerce Dataset](https://www.kaggle.com/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction)

# Formulation:writing_hand:
* Data
  * Pada kasus ini yang ingin diprediksi adalah customer yang kemungkinan akan churn, serta berhenti menggunakan layanan dari aplikasi ecommerce.
  * Customer yang kemungkinan akan churn dapat diprediksi berdasarkan data demografis user, perilaku user dalam bertransaksi, serta data lain yang mendukung.
* ML Objective : objective dari ML ini adalah memaksimalkan revenue dari perusahaan, serta meminimalkan resiko churn untuk user lainnya di waktu yang akan datang.
* Action : yang akan dilakukan setelah hasil prediksi diperoleh adalah menawarkan user yang teridentifikasi churn dengan program package promo yang sesuai untuk mereka.
* Value : hasil yang ingin dicapai dari penggunaan model machine learning ini adalah meningkatnya revenue dari perusahaan dan meminimalisir kehilangan user dalam aplikasi kita.

# Conclusion EDA
![EDA](https://github.com/PurwadhikaDev/KnightsOfData_JC_DS_VL_01_FinalProject/blob/master/images/edaChurn.png)
* Dari hasil observasi, customer yang churn sekitar 16%, sedangkan yang tidak churn sekitar 83%.
* Semakin lama Tenur, maka kemungkinan untuk Churn berkurang. Pengguna baru memiliki kecenderungan untuk Churn lebih besar. Pengguna dengan Tenure 1 tahun memiliki kecenderungan Churn hampir 20% di banding pengguna di tahun ke 2 yang kurang dari 10%.
* Persentase Churn pelanggan complain 30%.
* Semakin tinggi cashback yang didapatkan, semakin rendah persentase Churn. Terdapat peningkatan Churn signifikan pada pelanggan yang mendapatkan Cashback 221-231 dollar.
* Semakin lama pengguna tidak melakukan pemesanan, maka tingkat Churn semakin rendah.
* Satisfaction Score 5 adalah yang paling banyak Churn pada tahun pertama. Satisfaction Score 5 memiliki kecenderungan Churn paling banyak yaitu sekitar lebih dari 20%.<br>
_Ternyata ~65% Pengguna yang memberikan nilai Satisfaction Score 5, Churned pada Bulan ke 0 dan ~60% pada Bulan ke 1._<br>
Meskipun memberikan Satisfaction Score 5, user dengan Cashback terendah USD 110 - 111 memiliki tingkat Churn 100%.
* Tingkat presentase Churn pada jarak Warehouse ke rumah ada di sekitar 15% - 20%.<br>
Terjadi kenaikan signifikan pada jarak 15km, 19km, dan juga 31km. Semakin jauh jarak rumah ke gudang, potensi churn semakin meningkat.

# Conclusion Model
### Feature Importance
![feature importance](https://github.com/PurwadhikaDev/KnightsOfData_JC_DS_VL_01_FinalProject/blob/master/images/Feature%20Importance.png)
### Explain the model's predictions using SHAP
![shapValue](https://github.com/PurwadhikaDev/KnightsOfData_JC_DS_VL_01_FinalProject/blob/master/images/SHAPchurn.png)
1. _Tenure_
Semakin singkat berlangganan potensi churn semakin meningkat
2. _Complain_
Semakin banyak complain potensi churn semakin meningkat
3. _NumberOfAddress_
Semakin banyak jumlah alamat yang terdaftar potensi churn semakin meningkat
4. _CashbackAmount_
Semakin sedikit jumlah Cashback yang didapat potensi churn semakin meningkat
5. _DaySinceLastOrder_
Semakin singkat interval pemesanan, potensi churn semakin meningkat
6. _SatisfactionScore_
Semakin tinggi nilai kepuasan, potensi churn semakin meningkat
7. _NumberOfDeviceRegistered_
Semakin banyak jumlah device yang terdaftar, potensi churn semakin meningkat
8. _WarehouseToHome_
Semakin jauh jarak dari gudang ke rumah, , potensi churn semakin meningkat

# Recommendation
* Untuk pengguna dengan masa tenure 0-1 bulan, diberikan insentif (bisa berupa package promo cashback), untuk mencegah potensi churn terhadap Pengguna baru.
* Diperlukan perbaikan secara fungsi(aplikasi) maupun feedback pelayanan(service) yang lebih responsif terhadap komplain dari user, untuk mencegah pengguna akan churn.
* Memberikan notifikasi pengingat (reminder) yang bisa digabungkan dengan program insentif untuk pengguna yang telah melakukan pemesanan agar akun pengguna kembali aktif dan tidak churn.
* Memberikan insentif berupa pengurangan biaya ongkos kirim kepada pelanggan yang memiliki jarak yang jauh terhadap gudang, bisa dengan melakukan kerja sama dengan pihak jasa pengantar (kurir) untuk meringankan cost dari perusahaan.
* Pengguna baru yang memberikan nilai Satisfaction Score 5 diberikan notifikasi email untuk aktif kembali dengan isi email berupa visual grafis marketing ajakan untuk kembali aktif menggunakan aplikasi.
