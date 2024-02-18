# Bank-Marketing-Campaign

# Contents
Business Problem Understanding
Data Understanding
Data Preprocessing
Modeling
Conclusion
Recommendation

# Business Problem Understanding
# Context
Dalam pasar yang semakin kompetitif di sektor perbankan, bank menghadapi tantangan besar dalam mempertahankan nasabah deposito berjangka yang sudah ada dan menarik nasabah baru untuk memperoleh suku bunga deposito yang tinggi. Sementara persaingan antar bank terus meningkat, bank juga harus menjaga keuntungan dan pertumbuhan portofolio mereka. Salah satu cara untuk mendapatkan pelanggan baru adalah dengan melakukan *Marketing Campaign.

Bank melakukan Marketing Campaign melalui panggilan telepon dimana hasilnya dalam bentuk dataset. Tujuannya di sini adalah untuk menerapkan Machine Learning untuk menganalisis dataset dan menemukan strategi paling efektif yang akan membantu bank dalam campaign berikutnya untuk membujuk lebih banyak nasabah agar berlangganan deposito berjangka. Oleh karena itu, Bank ingin mengetahui nasabah mana saja yang tertarik deposit dan tidak agar Marketing Campaign ini bisa langsung ditujukkan ke target market secara langsung dan efisien.

Target: 
0 : Tidak menaruh deposit
1 : Menaruh deposit

# Problem Statement
Profitabilitas bank bergantung pada deposito jangka panjang. Untuk mempermudah dan efisiensi biaya maupun waktu dari Marketing Campaign diperlukan sebuah sistem untuk memprediksi nasabah mana saja yang tertarik atau tidak tertarik dengan produk deposito. Sehingga pendekatan dan tujuan campaign tersebut bisa langsung dirasakan dan sesuai dengan nasabah yang potensial untuk melakukan deposito.

# Goals
Bank mendapatkan customer yang ingin melakukan deposit dengan memaksimalkan marketing campaign. Salah satu langkah yang diperlukan adalah mengurangi cost pulsa untuk menelepon semua nasabah dan meningkatkan efisiensi waktu agar telemarketing tidak perlu menghubungi semua nasabah. Caranya adalah dengan mengidentifikasi nasabah dengan kriteria dan target yang sesuai agar dapat melalukan deposit. Oleh karena itu, dengan bantuan Machine Learning dibuatkan suatu sistem untuk melakukan prediksi dengan data yang tersedia, mengidentifikasi nasabah yang potensial dan tidak potensial untuk melakukan deposito.

# Analytic Approach
Jadi, yang perlu kita lakukan adalah menganalisis data untuk dapat menemukan pola dari fitur-fitur yang ada, yang membedakan kandidat nasabah yang potensial untuk deposito atau tidak.

Selanjutnya, dilanjutkan dengan membangun model klasifikasi yang akan membantu bank untuk dapat memprediksi probabilitas seorang kandidat nasabah yang akan/ingin melakukan deposit atau tidak.

# Metric Evaluation
Type 1 error (False Positive) akan menunjukkan pemborosan waktu dan biaya campaign untuk nasabah yang sebenarnya tidak berpotensi menaruh deposit, dan Type 2 error (False Negative) menunjukkan kehilangan nasabah potensial. Metrik yang tepat untuk model machine learning keadaan ini adalah F1 score.

F1 score cocok digunakan dalam situasi untuk mencapai keseimbangan antara presisi dan recall, terutama ketika kelas-kelas dalam data tidak seimbang. Dalam case ini, Kita ingin menghindari kedua jenis kesalahan, baik False Positive maupun False Negative. F1 score memberikan ukuran kinerja yang baik karena memperhitungkan kedua jenis kesalahan tersebut.

Dengan demikian, dalam kasus ini, Kita ingin memaksimalkan F1 score untuk memastikan bahwa model memiliki presisi yang tinggi dalam mengidentifikasi calon nasabah yang berpotensi menaruh deposit, sambil meminimalkan jumlah calon nasabah potensial yang terlewatkan (False Negative) dan menghindari pengeluaran yang tidak perlu pada calon nasabah yang sebenarnya tidak potensial (False Positive).

# Data Understanding
Dataset: https://drive.google.com/drive/folders/13lrEDlKfnTPNREfGLBaYGYf8dSjHBzfW

Terdapat 11 kolom dan 7813 baris dari dataset tersebut.

**Attribute Information**:
age	:	Umur nasabah
job	:	Pekerjaan nasabah
balance	:	Jumlah uang pada rekening nasabah
housing	: Apakah nasabah memiliki cicilan rumah
loan	:	Apakah nasabah memiliki hutang
contact	:	Alat komunikasi yang digunakan oleh telemarketimg untuk menghubungi
month	:	Bulan terakhir nasabah dihubungi oleh telemarketing
campaign	:	Jumlah kontak yang dilakukan selama kampanye
pdays	:	Jumlah hari sejak hari terakhir nasabah dihubungi oleh telemarketing
poutcome	:	Hasil dari kampanye sebelumnya
deposit	:	Apakah customer melakukan deposit atau tidak

# Conclusion
Model terbaik yang dipilih adalah model XGBoost dengan melihat f1 score paling tinggi. Model ini dapat mengurangi 57% kandidat nasabah tidak potensial untuk tidak di approach melalui campaign, dan model ini dapat memprediksi 42% kandidat nasabah yang tertarik. (berdasarkan recall) 

Tanpa model, perusahaan akan melakukan kampanye terhadap 1563 kandidat nasabah yang mana tidak semuanya adalah kandidat nasabah potensial untuk menaruh deposit. Dengan bantuan model ini, tim marketing campaign dapat berkurang jumlah approaching untuk campaign dimana yang tadinya approach 1563 nasabah menjadi 747 nasabah. Sehingga model ini dapat meningkatkan efisiensi bagi bank baik dari segi biaya maupun waktu.
