# Kelompok 10 Project UAS Pembelajaran Mesin Dasar (Machine Learning)
1. Muhammad Ariq Hibatullah (23031554064)
2. Firdaini Azmi (23031554071)
3. Reva Deshinta Isyana (23031554153)

# Judul
Klasifikasi Bahan Makanan Berbasis Citra Gambar Menggunakan SVM serta Estimasi Nilai Gizi dan Rekomendasinya berdasarkan Angka Kecukupan Gizi

# Latar Belakang
Pola makan yang seimbang adalah salah satu faktor penting dalam menjaga kesehatan tubuh. Asupan makanan yang masuk ke dalam tubuh harus sesuai dengan jumlah kebutuhan gizi sehari-hari. Untuk memudahkan penerapan pola makan seimbang, digunakan pemanfaatan teknologi sekarang berupa Machine Learning. Akan dibuat sistem untuk menghitung estimasi gizi dari foto dan memberikan rekomendasi makanan.

# Rumusan Masalah
1. Bagaimana cara mengklasifikasikan jenis bahan makanan berdasarkan citra secara otomatis menggunakan metode SVM ?
2. Bagaimana cara sistem menghitung kandungan gizi dari bahan makanan yang diinputkan?
3. Bagaimana sistem dapat memberikan rekomendasi makanan tambahan berdasarkan input pengguna?

# Tujuan
1. Mengklasifikasi jenis bahan makanan berdasarkan citra menggunakan metode SVM
2. Menghitung kandungan gizi dari makanan yang diinputkan oleh pengguna.
3. Menyediakan rekomendasi makanan tambahan untuk membantu pengguna mendapatkan menu makanan dengan gizi yang seimbang.

# Metode
Support Vector Machine (SVM)

# Dataset
Dataset yang digunakan pada project ini ada dua, dataset citra yang berisi foto bahan makanan dan juga dataset tabular yang berisi data nilai gizi yang terkandung dalam bahan makanan tersebut. 
Pada dataset citra, kami menyediakan setidaknya 982 foto multi label untuk semua label bahan makanannya, yaitu nasi, telur, ayam, timun, selada, tomat, ayam, dan ikan. Dari kumpulan foto itu akan disediakan kondisi bahan makanan yang beragam, misal seperti kondisi bahan makanan disaat kondisi utuh, kondisi dimasak, atau bahkan kondisi dipotong. Foto-foto tersebut dikumpulkan dari beberapa sumber, mulai dari mengambil dari dataset yang sudah ada, dan juga mengumpulkan fotonya menggunakan scraping pada Google Image dan Unsplash.
Pada dataset kandungan gizi, terdapat data kandungan karbohidrat, protein, lemak, kalori, dan energi pada setiap bahan makanan yang nantinya akan digunakan untuk klasifikasi. Data gizi diperoleh dari scraping dari website yang menyediakan informasi gizi suatu bahan makanan yaitu fatsecret.

# Langkah-langkah
1. Exploratory Data Analysis (EDA)
2. Pre-processing
3. Ekstraksi fitur
4. Normalisasi
5. Modeling
6. Deployment

# Hasil dan Analisis
1. Prediksi Makanan dan Kandungan Gizinya
   Model yang telah dibuat menghasilkan output berupa klasifikasi label makanan yang telah diinputkan oleh pengguna. Model akan menampilkan gambar inputan pengguna, label prediksi dengan berat sajian, dan perkiraan total nilai gizi dari hasil klasifikasi inputan gambar dari pengguna. Model juga akan menampilkan chart rincian kalori dari label makanan yang terprediksi
2. Kebutuhan Angka Kecukupan Gizi (AKG)
   Sistem juga akan menampilkan jumlah Angka Kecukupan Gizi (AKG) dari pengguna, dimana terdapat bullet chart yang menampilkan nilai AKG yang dibutuhkan yaitu 1841 kkal serta nilai AKG yang baru terpenuhi yaitu 338 kkal. Nilai AKG yang baru terpenuhi diambil dari nilai gizi dari gambar yang pengguna inputkan sedangkan kebutuhan nilai AKG diambil dari inputan data pengguna seperti jenis kelamin, umur, tinggi badan, berat badan, dan intensitas olahraga setiap individu.
3. Rekomendasi Makanan Berdasarkan AKG
   Rekomendasi makanan akan otomatis ditampilkan oleh sistem yang didasarkan pada nilai kebutuhan AKG setiap individu dengan toleransi sudah memenuhi setidaknya 80% dari angka tersebut, sistem akan merekomendasikan makanan yang ada pada dataset ‘Nilai Gizi’ yang memenuhi kriteria AKG. Terdapat hasil rekomendasi kombinasi makanan yang dibutuhkan pengguna untuk dapat mencukupi nilai AKG nya dalam satu hari, serta nilai gizi dan total asupan yang akan didapatkan jika mengonsumsi makanan yang telah direkomendasikan. Rekomendasi dilengkapi bar chart yang menampilkan informasi nilai dari setiap gizi yang diperlukan dalam satu hari oleh pengguna.

# Kesimpulan
Model klasifikasi multi-label yang dibangun dengan kombinasi ekstraksi fitur yaitu Color histogram spasial, Histogram of Oriented Gradients (HOG), Local Binary Pattern (LBP), dan Gray Level Co-occurrence Matrix (GLCM) yang menggunakan algoritma SVM, berhasil mendeteksi jenis makanan dari citra dengan tingkat Hamming Accuracy sebesar 73,03% dan nilai AUC untuk setiap label diatas 0,6.
