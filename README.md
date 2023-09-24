# Prediksi Waktu  Pesan-Antar Makanan Secara _Online_ - Aldy Muardi
## Domain Proyek
### Latar Belakang

Industri pesan antar makanan telah mengalami pertumbuhan yang signifikan dalam beberapa tahun terakhir, dengan semakin banyaknya pelanggan yang memilih kenyamanan memesan makanan dari restoran dan diantarkan langsung ke rumah mereka. Namun, salah satu tantangan umum yang dihadapi oleh pelanggan dan penyedia layanan pesan-antar makanan adalah ketidakpastian waktu pengantaran. Pelanggan sering mengalami frustrasi dan ketidakpuasan ketika pesanan mereka tertunda atau ketika mereka menerima estimasi waktu pengantaran yang tidak akurat [1].

Masalah ini tidak hanya memengaruhi kepuasan pelanggan tetapi juga berimplikasi pada keseluruhan operasi bisnis penyedia layanan pesan-antar makanan. Prediksi waktu pengantaran yang tidak akurat dapat menyebabkan perencanaan rute dan alokasi pengemudi pengantaran yang tidak efisien, yang mengakibatkan biaya yang lebih tinggi dan pemanfaatan sumber daya yang tidak optimal. Selain itu, persepsi pelanggan terhadap kecepatan pengantaran memainkan peran penting dalam kepuasan dan loyalitas mereka terhadap platform pengantaran makanan tertentu. Oleh karena itu, meningkatkan akurasi prediksi waktu pengantaran dapat secara langsung berdampak pada kepercayaan pelanggan, retensi, dan pertumbuhan bisnis secara keseluruhan.

![image](https://github.com/aldymuardi/prediksi_waktu_pemesanan_makanan/assets/79571450/5094c547-8aed-45b0-837b-23337dc1cabf)

Gambar 1. Ilustrasi Layanan Pesan-Antar Makanan

Untuk mengatasi tantangan ini, penting untuk mengembangkan model yang dapat secara akurat memprediksi waktu yang dibutuhkan makanan untuk diantarkan dari restoran ke lokasi pelanggan. Dengan memanfaatkan data pengantaran historis dan mempertimbangkan faktor-faktor yang relevan seperti pengalaman mitra pengantaran, peringkat mitra, dan jarak antara restoran dan pelanggan, model ini dapat memberikan perkiraan waktu pengantaran yang lebih andal. Hal ini, pada gilirannya, memungkinkan perencanaan rute yang lebih baik, alokasi sumber daya yang efisien, dan pada akhirnya meningkatkan pengalaman pelanggan secara keseluruhan.

Dengan mengembangkan dan menerapkan model prediktif seperti itu, penyedia layanan pesan-antar makanan dapat meningkatkan kepercayaan pelanggan, meningkatkan tingkat kepuasan, dan mendapatkan keunggulan kompetitif di pasar. Selain itu, mengoptimalkan operasi pengantaran dapat menghasilkan penghematan biaya, peningkatan efisiensi, dan pemanfaatan sumber daya pengantaran yang lebih baik, yang berkontribusi pada pertumbuhan dan kesuksesan bisnis.

## _Business Understanding_
Dalam industri pengantaran makanan yang sangat kompetitif, memberikan pengalaman pengantaran yang lancar dan efisien sangat penting untuk mendapatkan keunggulan kompetitif dan mendorong kepuasan pelanggan. Salah satu aspek penting dari pengalaman ini adalah memprediksi waktu pengantaran pesanan makanan secara akurat. Saat ini, banyak platform pengantaran makanan yang kesulitan dalam memberikan estimasi yang dapat diandalkan, yang menyebabkan ketidakpuasan pelanggan dan masalah kepercayaan.

Kurangnya prediksi waktu pengantaran yang akurat menimbulkan tantangan bagi penyedia layanan pesan antar makanan. Pelanggan sering kali menghadapi ketidakpastian dan ketidaknyamanan ketika mereka tidak yakin kapan pesanan mereka akan tiba. Hal ini dapat mengakibatkan ulasan negatif, penurunan loyalitas pelanggan, dan potensi kehilangan bisnis untuk platform. Di sisi lain, bagi perusahaan pengantaran makanan, estimasi waktu pengantaran yang tidak akurat dapat menyebabkan manajemen logistik yang tidak efisien, alokasi sumber daya yang tidak optimal, dan peningkatan biaya operasional.

Dengan berinvestasi dalam pengembangan dan implementasi sistem prediksi waktu pengantaran yang andal, penyedia layanan pesan-antar makanan dapat meningkatkan reputasi merek mereka, meningkatkan pengalaman pelanggan, dan mencapai pertumbuhan bisnis jangka panjang. Selain itu, ketersediaan estimasi waktu pengantaran yang tepat dapat berkontribusi pada ekosistem pengantaran makanan yang lebih berkelanjutan dan efisien, yang menguntungkan pelanggan dan industri secara keseluruhan.

### _Problem Statment_
1. Bagaimana Mengetahui faktor apa saja yang mempengaruhi waktu pengantaran makanan?
2. Bagaimana cara membuat model prediksi untuk menentukan estimasi waktu pesan-antar makanan?
3. Bagaimana Mengetahui berapa lama waktu rata-rata pesan antar makanan?

### _Goals_
1. Membuat estimasi yang akurat tentang kapan makanan akan tiba, sehingga meningkatkan kepercayaan pelanggan.
2. Melakukan pengantaran lebih cepat dengan melihat data pengantaran sebelumnya dan menentukan atribut yang mempengaruhinya.
3. Merencanakan rute pengantaran dan jadwal pengemudi secara lebih efisien dengan memprediksi berapa banyak pesanan yang akan tiba sehingga penyedia jasa pengantaran dapat menggunakan sumber daya mereka dengan lebih baik.

### _Solution Statement_
Untuk mengatasi tantangan dalam memperkirakan waktu pengantaran makanan, berbagai metode dan teknologi dapat digunakan. Salah satu metode tersebut adalah jaringan saraf _Long Short-Term Memory_ (LSTM) [2]. LSTM adalah jenis _Recurrent Neural Network_ (RNN) yang dirancang khusus untuk menangkap _long-term dependencies_ dan pola dalam data berurutan. Metode ini sangat cocok untuk tugas-tugas yang melibatkan analisis dan prediksi urutan, menjadikannya pilihan yang cocok untuk memodelkan waktu pengiriman makanan.

Dengan memanfaatkan data historis tentang waktu pengiriman, bersama dengan fitur-fitur yang relevan seperti jarak, kondisi lalu lintas, dan volume pesanan, model LSTM dapat mempelajari pola dan korelasi untuk membuat prediksi yang akurat. Prediksi ini kemudian dapat digunakan untuk memberi tahu pelanggan tentang perkiraan waktu kedatangan pesanan mereka, membantu mereka membuat rencana yang sesuai dan mengurangi ketidakpastian.

## _Data Understanding_
Dataset yang digunakan dalam proyek ini merupakan data pesan-antar makanan. Dataset ini dapat diunduh di [Food Delivery Dataset](https://raw.githubusercontent.com/ataislucky/Data-Science/main/dataset/food_delivery.txt)

**#**|**Column**|**Non-Null Count**|**Dtype**
:-----:|:-----:|:-----:|:-----:
0|ID|45593 non-null|object
1|Delivery_person_ID|45593 non-null|object
2|Delivery_person_Age |45593 non-null|int64|
3|Delivery_person_Ratings|45593 non-null|float64
4|Restaurant_latitude |45593 non-null|float64
5|Restaurant_longtitudee|45593 non-null|float64
6|Delivery_location_latitude|45593 non-null|float64
7|Delivery_location_longtitude|45593 non-null|float64
8|Type_of_order|45593 non-null|object|float64
9|Type_of_vehicle|45593 non-null|object
10|Time_taken(min)|45593 non-null|int64

### Berikut Informasi Dataset
* Dataset memiliki format TXT.
* Dataset memiliki 45593 sampel dengan 11 fitur.
* Dataset memiliki 5 fitur bertipe float64, 2 fitur bertipe int64 dan 4 fitur bertipe object.
* Tidak ada _missing value_ dalam dataset.

### Variabel-varibel Dataset
* ID = Nomor ID pemesanan
* Delivery_person_ID = Nomor ID kurir
* Delivery_person_Age = Usia kurir
* Delivery_person_Ratings = Ratings kurir berdasarkan pengiriman sebelumnya
* Restaurant_latitude = Garis lintang restoran
* Restaurant_longtitude = Garis bujur restoran
* Delivery_location_latitude = Garis lintang lokasi pengiriman
* Delivery_location_longtitude = Garis bujur lokasi pengiriman
* Type_of_order = Jenis makanan yang dipesan oleh pelanggan
* Type_of_vehicle = Jenis kendaraan yang digunakan kurir
* Time_taken(min) = Waktu yang dibutuhkan oleh kurir untuk menyelesaikan pesanan

### Langkah-langkah _Data Understanding_
* Mengumpulkan data: Langkah pertama adalah mengumpulkan data yang diperlukan untuk menjalankan model _machine learning_. Data ini bisa berupa data historis, data dari sumber eksternal, atau data yang dihasilkan secara _real-time_.
* Memeriksa dimensi data: Periksa dimensi data untuk memahami struktur dan ukurannya. Data bisa berupa tabel, matriks, atau dataset multidimensi.
* Eksplorasi data: Lakukan eksplorasi data dengan menggunakan berbagai metode statistik dan visualisasi. Analisis ini bertujuan untuk mengenali pola, tren, atau relasi yang ada dalam data. Dengan cara ini, Anda bisa mengetahui apakah ada nilai yang hilang, outlier, atau data yang tidak lengkap.
* Pembersihan data: Identifikasi dan tangani nilai yang hilang atau data yang tidak lengkap. Hal ini bisa dilakukan dengan mengisi nilai yang hilang, menghapus data yang tidak lengkap, atau menggunakan metode penggantian data yang lainnya. Langkah ini juga melibatkan penanganan outlier yang mungkin mempengaruhi analisis atau model yang akan dibangun.
* Normalisasi dan transformasi data: Dalam beberapa kasus, data perlu dinormalisasi atau diubah ke dalam format yang lebih sesuai untuk analisis atau pemodelan. Contohnya, jika data memiliki skala yang berbeda, Anda mungkin perlu menormalkannya agar memiliki skala yang serupa. Juga, terkadang perlu melakukan transformasi pada data untuk mengubah distribusi atau memperjelas hubungan antara variabel.
* Pemilihan fitur (_feature selection_): Jika data memiliki banyak fitur (variabel), perlu dilakukan pemilihan fitur yang paling relevan atau signifikan untuk digunakan dalam model machine learning. Hal ini membantu mengurangi dimensi data dan meningkatkan efisiensi serta interpretabilitas model.
* Split data: Bagi data menjadi set pelatihan (training set) dan set pengujian (_testing set_) atau mungkin juga set validasi. Set pelatihan digunakan untuk melatih model, sedangkan set pengujian digunakan untuk menguji kinerja model pada data yang belum pernah dilihat sebelumnya.
* Analisis korelasi: Analisis korelasi antara fitur atau variabel dalam data untuk memahami hubungan dan interaksi antara mereka. Korelasi dapat membantu mengidentifikasi fitur yang saling terkait dan memahami bagaimana variabel-variabel ini berdampak pada target yang ingin diprediksi.
* Statistik deskriptif: Lakukan analisis statistik deskriptif untuk memahami distribusi, rata-rata, median, dan variabilitas data. Hal ini membantu mengidentifikasi keunikan atau pola yang ada dalam data.
* Visualisasi data: Gunakan teknik visualisasi seperti grafik, histogram, diagram pencar (_scatter plot_), atau heatmap untuk memvisualisasikan data. Visualisasi dapat membantu Anda mendapatkan pemahaman yang lebih baik tentang data, mengidentifikasi anomali, dan menem

### _Data Exploration_
**Analisis Fitur Kategorik**
Analisis ini dilakukan untuk melihat kolerasi antara fitur kategorik dengan fitur target (Time_taken(min)).

* Hubungan antara jarak dan waktu pesan-antar makanan

  ![newplot](https://github.com/aldymuardi/prediksi_waktu_pemesanan_makanan/assets/79571450/ecf63a1d-9fa0-4bb9-ba2c-0b1ffa81c77a)

  Grafik tersebut menunjukkan bahwa ada hubungan yang konsisten antara waktu yang dibutuhkan dan jarak yang ditempuh untuk pengantaran makanan. Artinya, sebagian besar kurir mengantarkan makanan dalam waktu 25-30 menit, terlepas dari jaraknya.

* Hubungan antara usia kurir dan waktu pesan-antar makanan
  
  ![newplot (1)](https://github.com/aldymuardi/prediksi_waktu_pemesanan_makanan/assets/79571450/59d37f85-b4ae-4cd9-a97b-4a49314eeb04)

  Terdapat hubungan linier antara waktu yang dibutuhkan untuk mengantarkan makanan dan usia kurir. Artinya, kurir yang berusia muda membutuhkan waktu yang lebih singkat untuk mengantarkan makanan dibandingkan dengan mitra yang berusia lebih tua.

* Hubungan antara ratings kurir dan waktu pesan-antar makanan
  
  ![newplot (2)](https://github.com/aldymuardi/prediksi_waktu_pemesanan_makanan/assets/79571450/fb89b696-d5da-4b94-95dc-2ba167355974)
  
  Terdapat hubungan _invers linier_ antara waktu yang dibutuhkan untuk mengantarkan makanan dan ratings kurir. Artinya, kurir dengan ratings yang lebih tinggi membutuhkan waktu yang lebih singkat untuk mengantarkan makanan dibandingkan kurir dengan ratings rendah.

* Hubungan antara jenis kendaraan kurir dan waktu pesan-antar makanan
  
  ![newplot (4)](https://github.com/aldymuardi/prediksi_waktu_pemesanan_makanan/assets/79571450/2cd5ae71-309a-4c8d-b782-f614adc5bfc4)

  Grafik tersebut menunjukkan bahwa jenis kendaraan kurir dan jenis makanan yang diantarkan tidak berpengaruh secara signifikan terhadap waktu pengantaran.

Jadi, fitur yang berkontribusi paling besar terhadap waktu pengantaran makanan berdasarkan analisis di atas adalah:
* Jarak antara restauran dan lokasi penganttaran.
* Ratings kurir.
* Usia kurir.

## Data Preparation
### Teknik Data Preparation Yang Dilakukan
* Mengubah [Food Delivery Dataset](https://raw.githubusercontent.com/ataislucky/Data-Science/main/dataset/food_delivery.txt) menjadi dataframe dengan menggunakan pandas.
* Analisis awal untuk membuang variabel yang sangat tidak relevan untuk prediksi data.
* Melakukan _exploratory_ data analysis untuk memahami variabel-variabel yang terdapat dalam dataset.
* Memvisualisasikan data dengan menggunakan boxplot untuk mencari outlier.
* Menggunakan IQR (_Interquartile Range_) untuk mengeliminasi outlier.
* Melakukan univariative analysis untuk memahami sebaran data variabel.
* Melakukan _multivariative analysis_ untuk memahami korelasi variabel kategorikal dan numberikal terhadap variabel price.
* Membuat _correlation matrix_ untuk fitur numerik.
* Mengeliminasi variabel numerik yang memiliki korelasi rendah terhadap variabel price.

### Menghitung Jarak Antara Dua Garis Lintang dan Garis Bujur
Dataset yang digunakan tidak memiliki fitur yang menunjukkan perbedaan antara restoran dan lokasi pengantaran, salah satu fitur yang dimiliki ialah titik lintang dan bujur dari restoran dan lokasi pengantaran, sehingga dapat menggunakan [Haversine formule](https://en.wikipedia.org/wiki/Haversine_formula) untuk menghitung jarak antara dua lokasi berdasarkan garis lintang dan garis bujurnya.
     
    Haversine formule: 
        a = (sin)^2 × (∆lat/2) + cos⁡(lat1) × cos⁡(lat2) × (sin)^2 × (∆lon/2)
        c = 2 × atan2 (√a,√((1-a) ))
        d = R × c
    dimana:
        * lat1 dan lat2 adalah lintang dan bujur dari dua titik
        * ∆lat adalah perbedaan antara garis lintang
        * ∆lon adalah perbedaan antara garis bujur
        * R adalah jari-jari bola
        * d adalah jarak antara dua titik dalam satuan yang sama dengan R

### Splitting Dataset
Membagi dataset biasanya mengacu pada membagi dataset yang diberikan menjadi dua atau lebih subset untuk berbagai tujuan, seperti _train_, _validation_, dan _test_. Pemisahan yang paling umum adalah pemisahan _train-test_, di mana dataset dipartisi menjadi set pelatihan dan set pengujian.

**Train (%)**|**Test (%)**
:-----:|:-----:
80|20

## _Modelling_
Algoritma yang digunakan pada proyek ini adalah _Long Short Term Memory_ (LSTM).

![image](https://github.com/aldymuardi/prediksi_waktu_pemesanan_makanan/assets/79571450/ccdc048a-ad44-4c46-964d-dc81ac9c1fee)

LSTM adalah jenis jaringan saraf tiruan (RNN) yang dirancang khusus untuk menangkap ketergantungan jangka panjang dan pola dalam data berurutan. Jaringan ini sangat cocok untuk tugas-tugas yang melibatkan analisis dan prediksi urutan, menjadikannya pilihan yang cocok untuk memodelkan waktu pengiriman makanan. Dengan memanfaatkan data historis tentang waktu pengiriman, bersama dengan fitur-fitur yang relevan seperti jarak, kondisi lalu lintas, dan volume pesanan, model LSTM dapat mempelajari pola dan korelasi untuk membuat prediksi yang akurat. Prediksi ini kemudian dapat digunakan untuk memberi tahu pelanggan tentang perkiraan waktu kedatangan pesanan mereka, membantu mereka membuat rencana yang sesuai dan mengurangi ketidakpastian.

Jumlah layer yang digunakan sebagai berikut:
**Layer (tipe)**|**Output Shape**|**Param #**
:-----:|:-----:|:-----:
lstm (LSTM)|(None, 3, 128)|66560
lstm_1 (LSTM)|(None, 64)|49408
dense (Dense)|(None, 25)|1625
dense_1 (Dense)|(None, 1)|26

_Omptimizer_: Adam

_Loss Function_: mean_squared_error

_Epoch_: 9 Iterasi

## _Evaluation_
Untuk mengevaluasi kinerja model prediksi pesan-antar makanan, menggunakan metrik evaluasi yang umum digunakan dalam tugas regresi, metrik evaluasi yang digunakan adalah **Mean Squared Error (MSE)** adalah salah satu fungsi kerugian regresi yang paling umum. Dalam Mean Squared Error yang juga dikenal sebagai kerugian L2, untuk menghitung kesalahan dengan mengkuadratkan perbedaan antara nilai prediksi dan nilai aktual dan merata-ratakannya di seluruh kumpulan data. 

![image](https://github.com/aldymuardi/prediksi_waktu_pemesanan_makanan/assets/79571450/3d0d8ece-dc7e-40fb-84a1-8c186cbacddb)

### Menguji Kinerja Model Untuk Memprediksi Waktu Pengantaran Makanan

Hasil yang diberikan adalah prediksi waktu pengiriman untuk pesan-antar makanan berdasarkan model LSTM Neural Network yang telah dilatih dengan menggunakan fitur-fitur input berikut:
* Usia kurir: 25
* Ratings Kurir: 6
* Jarak tempuh: 4

_Output_ dari prediksi ditampilkan sebagai "Prediksi Waktu Pengiriman dalam Menit = [[19.49582]]" yang berarti bahwa model telah memperkirakan bahwa pengiriman makanan akan memakan waktu sekitar 19.5 menit untuk sampai ke tempat tujuan.

### Kesimpulan

Dalam menghadapi tantangan prediksi waktu pesan-antar makanan, jaringan syaraf tiruan LSTM telah diidentifikasi sebagai salah satu metode yang efektif. LSTM mampu memproses data dengan urutan, seperti data waktu, dan memiliki kemampuan untuk mengingat informasi jangka panjang, yang berguna dalam memprediksi waktu pengantaran berdasarkan data historis dan variabel yang relevan.

### Referensi
[1] Amalia, B.S., Retno, Y. and Mayasari, R. (2021) ‘ANALISIS SENTIMEN REVIEW PELANGGAN RESTORAN MENGGUNAKAN ALGORITMA SUPPORT VECTOR MACHINE DAN K-NEAREST NEIGHBOR’, SITEKIN: Jurnal Sains, Teknologi dan Industri, 19(1), pp. 28–34.  

[2] Khiari, J. and Olaverri-Monreal, C. (2020) ‘Boosting algorithms for delivery time prediction in Transportation Logistics’, 2020 International Conference on Data Mining Workshops (ICDMW) [Preprint]. doi:10.1109/icdmw51313.2020.00043.  
