# UAS_STKI_12757

# Indeks File
1. Dataset Pra Processing: Sentiment
2. Dataset Pasca Processing: sentiment_dataset
3. IPYNB Dataset Preprocessing: Twitter_Dataset_Preprocessing.ipynb
4. IPYNB Modelling dan Evaluasi: STKI_LSTM_Sentiment_Analysis.ipynb

# 1. Dataset
Dataset ini merupakan kumpulan data sentimen pengguna Twitter tentang dua produk smartphone, yaitu Samsung S24 dan Iphone 15. Data sentimen ini diambil dari tweet yang diposting oleh pengguna Twitter dari tanggal 1 Desember 2023 hingga tanggal 17 Januari 2024. Dataset ini hanya berfokus pada tweet yang menggunakan bahasa Indonesia.

Dataset ini terdiri dari tiga kolom, yaitu:

- ID tweet: Kolom ini berisi nomor identifikasi unik untuk setiap tweet.
- Tanggal: Kolom ini berisi tanggal dan waktu ketika tweet diposting.
- Teks tweet: Kolom ini berisi isi teks dari tweet.

Dataset ini diambil menggunakan metode crawling, yaitu proses pengambilan data secara otomatis dari sumber online. Metode crawling ini menggunakan alat snscrape, yaitu sebuah scraper untuk media sosial yang dapat mengambil data tweet berdasarkan kriteria tertentu.

Dataset ini juga telah diolah untuk tujuan analisis sentimen, yaitu proses pengenalan dan ekstraksi opini atau emosi dari teks. Proses pengolahan data ini meliputi langkah-langkah berikut:

- Membuat lowercase: Langkah ini mengubah semua huruf besar menjadi huruf kecil dalam teks tweet, agar tidak ada perbedaan antara kata-kata yang sama dengan kapitalisasi yang berbeda.
- Menghapus karakter yang tidak penting: Langkah ini menghapus karakter yang tidak relevan atau mengganggu dalam teks tweet, seperti tanda baca, simbol, emoji, dll.
- Stopword: Langkah ini menghapus kata-kata yang sering muncul dalam teks, tetapi tidak memiliki makna penting atau informasi yang berguna, seperti “yang”, “dan”, “di”, dll.
- Mencari kata yang paling sering muncul: Langkah ini menghitung frekuensi kemunculan setiap kata dalam teks tweet, dan menampilkan kata-kata yang paling sering muncul dalam bentuk tabel atau grafik.
- Tokenisasi: Langkah ini memecah teks tweet menjadi unit-unit yang lebih kecil, seperti kata, frasa, atau kalimat, yang disebut token. Token ini dapat digunakan sebagai input untuk model analisis sentimen.
- Membuat word cloud: Langkah ini membuat visualisasi teks tweet dalam bentuk awan kata, di mana ukuran kata menunjukkan frekuensi kemunculannya dalam teks. Word cloud ini dapat membantu melihat kata-kata yang paling menonjol atau dominan dalam teks tweet.
- Memberikan skor sentimen: Langkah ini memberikan nilai numerik untuk setiap tweet, yang menunjukkan sentimen atau emosi yang terkandung dalam teks. Skor sentimen ini dapat berupa negatif, positif, netral, atau gabungan, tergantung pada metode atau model yang digunakan.

# 2. Permasalahan dan Tujuan
Eksperimen ini bertujuan untuk mengkaji preferensi konsumen smartphone terhadap dua merek terkemuka, yaitu Samsung dan Apple, yang baru-baru ini meluncurkan produk terbarunya, Samsung S24 dan Iphone 15. Permasalahan yang dihadapi oleh konsumen adalah kesulitan dalam memilih handphone baru yang sesuai dengan kebutuhan dan selera mereka, karena kedua merek tersebut memiliki keunggulan dan kekurangan masing-masing. Dengan menggunakan data dari media sosial Twitter, eksperimen ini akan menganalisis sentimen atau ulasan konsumen terhadap kedua produk tersebut, sehingga dapat memberikan informasi yang berguna bagi konsumen dalam mengambil keputusan berdasarkan data. Selain itu, data ini juga dapat memberikan masukan bagi Samsung dan Apple dalam meningkatkan kualitas produk mereka di masa depan.

# 3. Model
Model LSTM adalah singkatan dari Long Short-Term Memory, yaitu sebuah jenis jaringan saraf berulang (Recurrent Neural Network) yang dapat digunakan untuk memodelkan data berurutan, seperti data waktu (time series). Model LSTM dirancang untuk mengatasi masalah gradien yang menghilang (vanishing gradient) yang sering terjadi pada model RNN biasa, dengan menambahkan sel, pintu masuk, dan pintu keluar tambahan.

Model LSTM dapat digunakan untuk berbagai macam tujuan, seperti prediksi, klasifikasi, generasi teks, analisis sentimen, dan lain-lain. Dalam penelitian yang Anda sebutkan, model LSTM digunakan untuk melakukan analisis sentimen pada data tweet yang berbahasa Indonesia. Analisis sentimen adalah proses mengenali dan mengekstraksi opini atau emosi dari teks.

Model LSTM dapat belajar dari data tweet yang berisi sentimen positif, negatif, atau netral, dan kemudian memberikan skor sentimen untuk setiap tweet. Skor sentimen ini dapat digunakan untuk mengetahui preferensi atau kepuasan konsumen terhadap produk tertentu, seperti Samsung S24 atau Iphone 15. Model LSTM juga dapat mengolah data tweet yang memiliki fitur beragam, seperti bahasa, panjang, tanda baca, emoji, dan lain lain.

# 4. Alur Tahapan Eksperimen
Eksperimen Anda terdiri dari dua tahap utama, yaitu persiapan data dan pembuatan model. Tahap persiapan data meliputi proses pengambilan, penggabungan, pemilihan, pembersihan, dan penilaian data sentimen dari tweet pengguna Twitter tentang produk Samsung S24 dan Iphone 15. Tahap pembuatan model meliputi proses pembuatan, pelatihan, pengujian, dan evaluasi model LSTM untuk melakukan analisis sentimen pada data tweet yang telah diproses.

Tahap persiapan data memiliki langkah-langkah sebagai berikut:

- Menggali data sentimen Samsung dan Apple dari Twitter dengan tools crawl. Tools crawl adalah alat untuk mengambil data secara otomatis dari sumber online, seperti media sosial. Tools crawl yang digunakan adalah snscrape, yang dapat mengambil data tweet berdasarkan kriteria tertentu, seperti kata kunci, tanggal, bahasa, dll.
- Menyatukan kedua file dataset dari masing masing merek. File dataset yang dihasilkan dari proses crawling berisi data tweet tentang Samsung S24 dan Iphone 15 secara terpisah. Untuk memudahkan analisis, kedua file dataset tersebut disatukan menjadi satu file dataset yang berisi data tweet tentang kedua produk tersebut.
- Hanya mengambil data tweet yang menggunakan bahasa indonesia dan menghapus sisanya. Karena eksperimen ini hanya berfokus pada data tweet yang berbahasa Indonesia, maka data tweet yang menggunakan bahasa lain dihapus dari file dataset yang digabungkan. Hal ini dilakukan untuk menghindari kesalahan atau kebingungan dalam analisis sentimen.
- Hanya mengambil kolom data id, tanggal, dan teks tweets dan menghapus sisanya. File dataset yang digabungkan berisi beberapa kolom data, seperti id tweet, tanggal, teks tweet, bahasa, lokasi, dll. Namun, hanya kolom data id, tanggal, dan teks tweet yang dibutuhkan untuk analisis sentimen, sehingga kolom data lainnya dihapus dari file dataset.
- Mengubah semua huruf menjadi huruf kecil, tidak ada huruf kapital di dataset. Langkah ini dilakukan untuk menghilangkan perbedaan antara kata-kata yang sama dengan kapitalisasi yang berbeda, seperti “Samsung” dan “samsung”. Hal ini dapat mempengaruhi hasil analisis sentimen, karena kata-kata yang sama dapat dianggap sebagai kata-kata yang berbeda jika memiliki huruf besar atau kecil yang berbeda.
- Menghapus karakter seperti titik, koma, kutip, dan lainnya. Langkah ini dilakukan untuk menghapus karakter yang tidak relevan atau mengganggu dalam teks tweet, seperti tanda baca, simbol, emoji, dll. Hal ini dapat mempengaruhi hasil analisis sentimen, karena karakter tersebut dapat menyebabkan kesalahan atau kebingungan dalam pemrosesan teks.
- Memberikan stopword untuk setiap kata. Stopword adalah kata-kata yang sering muncul dalam teks, tetapi tidak memiliki makna penting atau informasi yang berguna, seperti “yang”, “dan”, “di”, dll. Langkah ini dilakukan untuk menghapus stopword dari teks tweet, agar hanya menyisakan kata-kata yang relevan atau bermakna untuk analisis sentimen.
- Mencari kata yang paling sering muncul. Langkah ini dilakukan untuk menghitung frekuensi kemunculan setiap kata dalam teks tweet, dan menampilkan kata-kata yang paling sering muncul dalam bentuk tabel atau grafik. Hal ini dapat membantu melihat kata-kata yang paling menonjol atau dominan dalam teks tweet, yang dapat mengindikasikan sentimen atau opini pengguna.
- Membuat tokenisasi. Langkah ini dilakukan untuk memecah teks tweet menjadi unit-unit yang lebih kecil, seperti kata, frasa, atau kalimat, yang disebut token. Token ini dapat digunakan sebagai input untuk model analisis sentimen, karena model tersebut dapat belajar dari pola atau hubungan antara token-token tersebut.
- Membuat word cloud untuk representasi frekuesni setiap kata. Langkah ini dilakukan untuk membuat visualisasi teks tweet dalam bentuk awan kata, di mana ukuran kata menunjukkan frekuensi kemunculannya dalam teks. Word cloud ini dapat membantu melihat kata-kata yang paling menonjol atau dominan dalam teks tweet, yang dapat mengindikasikan sentimen atau opini pengguna.
- Memberikan 4 skor sentimen (positif, negatif, netral, gabungan) kepada data. Langkah ini dilakukan untuk memberikan nilai numerik untuk setiap teks tweet, yang menunjukkan sentimen atau emosi yang terkandung dalam teks. Skor sentimen ini dapat berupa negatif, positif, netral, atau gabungan, tergantung pada metode atau model yang digunakan. Skor sentimen ini dapat digunakan sebagai target atau label untuk model analisis sentimen.

Tahap pembuatan model memiliki langkah-langkah sebagai berikut:
- Data Preparation: Mengimpor modul-modul yang dibutuhkan untuk melakukan analisis sentimen, seperti numpy, pandas, seaborn, matplotlib, nltk, keras, dan tensorflow. Membaca dataset sentimen yang berisi tweet, nilai negatif, netral, positif, dan gabungan. Menerapkan lemmatization pada tweet untuk mengubah kata-kata menjadi bentuk dasarnya.
- Modelling: Membuat model sequential dengan lapisan embedding, convolution, max pooling, bidirectional LSTM, LSTM, GRU, simple RNN, dan dense. Mengkompilasi model dengan optimizer adam, loss mean squared error, dan metrik mean absolute error. Melatih model dengan data training dan validasi, menggunakan early stopping untuk menghindari overfitting.
- Prediksi Komputasi: Memprediksi nilai sentimen untuk data training dan data uji menggunakan model yang telah dilatih.
- Analisis Sentimen Metriks: Menghitung dan memvisualisasikan metrik evaluasi untuk setiap jenis sentimen, seperti R2, rmse, dan MAE. Membuat scatter plot antara nilai aktual dan prediksi untuk data training dan data uji.
- Menginput hyper parameter: Menentukan nilai-nilai untuk parameter seperti panjang maksimum urutan, jumlah kata maksimum, dimensi embedding, dan filter konvolusi.
- Membuat arsitektur model: Membangun model sekuensial dengan lapisan embedding, konvolusi, max pooling, LSTM, GRU, RNN, dan dense.
- Melatih model dengan epochs 100 dan batch size 50: Menggunakan optimizer adam, loss mean squared error, dan metrik mean absolute error. Menggunakan early stopping untuk menghindari overfitting.
- Membuat loss function: Menggambarkan kurva loss dan mean absolute error untuk data latih dan validasi.
- Membuat prediksi komputasi: Menghasilkan nilai-nilai prediksi untuk sentimen negatif, netral, positif, dan gabungan dari data latih dan uji.
- Membuat analisis sentimen metriks: Menghitung dan membandingkan nilai-nilai R2, rmse, dan MAE untuk sentimen negatif antara data latih dan uji. Menggambarkan scatter plot untuk menunjukkan hubungan antara nilai aktual dan prediksi.
- Membuat evaluasi netral: Mengulangi langkah sebelumnya untuk sentimen netral.
- Membuat evaluasi positif: Mengulangi langkah sebelumnya untuk sentimen positif.
- Membuat evaluasi gabungan: Mengulangi langkah sebelumnya untuk sentimen gabungan.

# 5. Link presentasi
https://youtu.be/fLCYga9WMA4?si=kwnzwUxRWidsfiIV
