# Project Introduction
Hotel Booking Cancellation adalah dataset dari sebuah hotel di portugal, dimana berisikan informasi mengenai setiap kebutuhan dari sebuah booking, informasi dari data mencakup spesial request, total hari waiting list, tipe kamar, dll. dari data tersebut, kita ingin mencapai tujuan kita, yaitu memprediksi apakah sebuah booking akan berakhir cancel atau tidak. 

## Business Overview
Sebuah hotel di *Portugal* ingin mengetahui apakah sebuah hotel booking akan di *Canceled* atau tidak, Hotel ini ingin mengetahui apakah sebuah **Booking** akan berlanjut atau akan berakhir di *Cancel*, hal ini dapat membantu Hotel untuk mengingkatkan *revenue* karena jika sebuah booking akan berakhir *cancel*, hal itu bisa di alihkan kepada *Customer* yang lebih berpotensi menginap. 

## Tujuan dan Permasalahan 
Permasalahan:
Jika menerima booking secara keseluruhan akan berpotensi adanya customer yang *cancel*, walaupun hal ini tidak memakan biaya, tapi hal ini sangat mempengaruhi hilangnnya potensi *revenue*.

Perusahaan ingin memaksimalkan *revenue* dengan meminimalisirkan potensi *cancel*, hal ini juga dilakukan agar perusahaan akan lebih fokus memperbanyak jumlah penginap semaksimal mungkin.

Tujuan: 
Dari *Problem Statement* diatas, perusahaan ingin bisa memprediksi *behaviour* dari customer, yang berpotensi untuk *cancel* atau yang tetap menginap di hotel tersebut.

tentunya dengan mengetahui faktor apa yang sekiranya mempengaruhi hal ini terjadi, sehingga Hotel bisa lebih terfokus untuk menentukan apakah individu/kelompok mana yang berpotensi melakukan *cancel* atau tidak.

## Analytical Approach

Berdasarkan semua yang tertera diatas, kita mengetahui permasalahan dan memiliki tujuan untuk memprediksi apakah cutomer akan cancel atau tidak, berdasarkan itu sudah jelas bahwa kita akan menghadapi target yang biner, maka analytical approach yang kita gunakan adalah:

1. Model Klassifikasi Biner

Selain itu target dari dataset ini akan didefinisikan sebagai berikut:<br>
**1 : Cancel**<br>
**0 : Tidak Cancel**

## Requirements

Dalam melakukan pemodelan di project ini, bahasa pemrograman yang dibutuhkan adalah python, diikuti dengan framework:

- Scikit-learn (Untuk model tree based, linear model, naive bayes, KNN, ensemble)
- XGBoost & LightGBM 
- Pandas
- Numpy
- Matplotlib & Seaborn (Data Visualization)
- imblearn (Imbalance Dataset)
- Optuna (Hyperparameter Tuning)
- Pickle (Save final model)

## Tahap dari modelling 

### Data Exploration

Disini kita akan melakukan Data Cleaning dan juga EDA, dimana data cleaning akan membersihkan unnecessary data point dan menghilangkan missing value, sedangkan untuk EDA yang dilakukan disini hanyalah simple EDA, tidak terlalu spesifik dan detail, hanya sebagai gambaran besar agar nanti kedepannya kita mengetahui untuk melakukan tindakan apa pada tahap modelling 

### Data Preprocessing

Tentu pada feature yang tersedia dari dataset masih banyak yg berbentuk categorical, oleh karena itu kita melakukan data preprocessing untuk mengubah/mentransformnya menjadi data yang reliable pada saat kita akan melakukan modelling 

### Modelling & Evaluation

Pada tahapan ini, kita akan melakukan modelling, dimana algoritma-algoritma dari model yang terpilih akan dilakukan benchmarking terlebih dahulu pada level training-validation, setelah menghasilkan model yang terbaik, makan akan dilakukan testing pada test set, dan pada tahapan modelling ini, terdapat 2 bagian setelah benchmarking, yaitu:

- Resampling
- Hyperparameter tuning

#### Resampling

Resampling merupakan metode sampling ulang yang dilakukan karena dataset kita memiliki data yang imbalance, oleh karena itu tahapan resampling ini dilakukan dan akan dibandingkan bagaimana bisa menghasilkan performa yang lebih baik 

#### Hyperparameter tuning

Untuk hyperparameter tuning yang digunakan yaitu **Bayesian Optimization**, dimana model akan dituning secara acak pada awal tahapan, lalu dengan menggunakan algoritma Bayesian, adjustment dilakukan secara otomatis, ini merupakan bentuk otomasi dari **RandomizedCV**

### Conclusion & Recommendation

Konklusi diangkat dari hasil model terakhir yang terpilih, dengan menampilkan bagaimana performanya dan sedikit penjelasan mengenai evaluation metricsnya, selain itu, pada tahap konklusi akan ditampilkan secara numerikal untuk melihat perbedaan dengan menggunakan model sebagai company yg data-driven dibandingkan dengan yang tidak menggunakan model (Company yang tidak data-driven), perbandingan akan di tampilkan secara jelas dan menggunakan perbandingan hasil test asli bukan assumsi agar hasil lebih jelas 

Rekomendasi meliputi rekomendasi untuk user, stakeholder, penyedia data dan juga penulis, untuk user dan stake-holder, akan dijelaskan rekomendasi apa yang harus mereka lakukan untuk bisa menggunakan model ini dengan efficient dan effektif, untuk penyedia data rekomendasi yang diberikan yaitu tentang datanya itu sendiri, dari sisi kelengkapan, kebersihan data dan efektifitas datanya, dan untuk penulis sendiri, rekomendasi terkait langkah yang belum bisa dijalankan di project ini. 

### Saving model

Tentunya setelah seluruh analisa dan penjabaran hasil, maka model yang sudah cukup memuaskan perlu di save, agar kedepannya model tersebut bisa di gunakan

# Penutupan 

Terimakasih sudah membaca ReadMe File berikut, file ini mencakup seluruh project yang dikerjakan secara Bigger Point of View saja, untuk mengetahui detail dari project ini bisa di akses di file .ipynb dan untuk melihat performa modelnya dan mencobanya dalam dataset bisa di cek di file .sav

**Thank You!!**
