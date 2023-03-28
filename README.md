# Brazilian-E-commerce-Public-Dataset-by-Olist-Final-Project

# Customer-Satisfaction-Prediction
Predict customer satisfaction for an e-commerce purchase

# <center>Customer Satisfaction Prediction - Brazillian e-Commerce Public Dataset</center>

## Introduction
E-commerce adalah platform di mana penjual dapat menjual produk dan pelanggan dapat membeli produk. Itu berarti platform e-commerce menghubungkan sejumlah besar penjual ke pelanggan melalui online. Memberikan layanan yang lebih baik kepada pelanggan adalah salah satu kunci utama untuk sukses sebagai penjual e-commerce.
Bagaimana mengukur kebaikan layanan?
Jawabannya adalah: kebaikan suatu layanan didasarkan pada kepuasan pelanggan. Jika pelanggan tidak puas dengan layanan yang diberikan penjual, maka penjual harus fokus pada kualitas layanan untuk menarik pelanggan, sehingga meningkatkan bisnis. Jadi, pada dasarnya umpan balik pelanggan memainkan peran penting dalam bisnis e-commerce.

## Business Problem
Dalam sistem saat ini, platform e-commerce akan mengirimkan email umpan balik kepada pelanggan setelah produk dikirimkan. Pelanggan dapat memberikan penilaian dari 5, juga dapat menuliskan beberapa komentar/ulasan tentang produk yang dibelinya. Dengan menggunakan ulasan dan peringkat ini, platform e-niaga akan menilai produk, yang membantu orang lain mendapatkan wawasan tentang kualitas produk. Namun menurut perspektif penjual, ulasan ini akan memainkan peran penting untuk meningkatkan bisnis. Namun seringkali, pelanggan tidak memberikan peringkat atau ulasan apa pun. Bagaimana cara memprediksi skor ulasan yang dapat diberikan pelanggan? Ini adalah masalah dalam bisnis e-commerce. Juga, masalahnya dapat diperpanjang sebagai "Apakah mungkin untuk memprediksi peringkat ulasan yang dapat diberikan pelanggan sebelum dia benar-benar memberikan peringkat?". Jika masalah ini teratasi, maka dimungkinkan juga untuk memprediksi peringkat yang belum diberikan peringkat oleh pelanggan. Dalam studi kasus ini, tujuan saya adalah mencoba memecahkan masalah ini, yaitu Memprediksi kepuasan pelanggan e-commerce.

## Problem Statement
Dalam menghadapi masalah dunia e-commerce ini, review menjadi tolak ukur penting seorang calon customer untuk membeli suatu barang. menurut artikel dari bigcommerce.com, reviews dapat membantu customer untuk memilih dan melakukan komparasi barang, membangun kepercayaan customer terhadap toko, bahkan meningkatkan penjualan. sedikit review buruk akan menjadi penentu seorang calon customer untuk memutuskan pembelian di suatu toko. Dengan bertambahnya persaingan penjualan, penjual harus melakukan usaha lebih agar barang yang ditawarkan menjadi lebih menarik dan menghasilkan review yang juga baik. faktor penentu seperti jumlah foto, deskripsi barang, lama pengiriman, dan lainnya dapat menjadi faktor penentu review yang diberikan oleh customer.

## Goals
Untuk studi kasus ini, saya mengambil dataset yang diberikan oleh Olist, yang merupakan platform e-commerce di Brazil. Olist menghubungkan bisnis kecil di seluruh Brasil ke pelanggan dengan satu kontrak. Olist telah memberikan lebih dari 100 ribu informasi pesanan yang ditempatkan antara 2016 hingga 2018. Mirip dengan semua platform e-commerce lainnya, Olist juga mengirimkan formulir umpan balik kepada pelanggan setelah perkiraan tanggal pengiriman untuk mendapatkan ulasan dan peringkat. Sekarang, Olist ingin meningkatkan bisnis serta memberikan layanan yang lebih baik kepada pelanggan dengan menggunakan informasi kepuasan pelanggan. Untuk itu perlu memprediksi peringkat ulasan sebelum pengguna memberikan peringkat yang sebenarnya. Jadi, pendekatan saya adalah mengatasi masalah bisnis ini menggunakan ilmu data, yang merupakan cara ilmiah untuk menyelesaikan masalah bisnis ini. Dengan bantuan prediction tool, Olist dapat membantu seller untuk memberikan prediksi review yang diberikan dengan skala 1-5 (1-3 adalah review negatif dan 4-5 adalah review positif) sehingga review yang diberikan customer dapat membantu seller untuk melariskan penjualan. dengan review yang baik, tentunya akan membantu calon pembeli lain yakin untuk membeli pada toko yang memiliki review terbaik.


**CREDITS**:- Kaggle

**Predict Customer satisfaction (0 for negative and 1 for postive) of the purhase from the brazilain e-commerce site Olist.**

## Mapping the real world problem to a Machine Learning Problem
### Type of Machine Learning Problem:

For a given order, we need to predict the customer satisfaction score given its different features like price, item description, on time delivery, delivery status etc. 
The given problem is a **Binary Classification Problem** as it will return the customer review score of an order as either 0 or 1.

#### Performance metric: F1-score
#### Real world/Business Objectives and Constraints
  1. Minimize False positive rate.
  2. No strict latency concerns.
  3. Interpretability is important.

## Data
### Data Overview:
**Source**:- https://www.kaggle.com/olistbr/brazilian-ecommerce

The data is divided in multiple datasets for better understanding and organization. Please refer to the following data schema when working with it:
<img src="https://i.imgur.com/HRhd2Y0.png" />

### Data Description:
* **Customers Dataset**:-
This dataset has information about the customer and its location. Use it to identify unique customers in the orders dataset and to find the orders delivery location.
* **Geolocation Dataset**:-
This dataset has information Brazilian zip codes and its lat/lng coordinates. Use it to plot maps and find distances between sellers and customers.
* **Order Items Dataset**:-
This dataset includes data about the items purchased within each order.
* **Payments Dataset**:-
This dataset includes data about the orders payment options.
* **Order Reviews Dataset**:-
This dataset includes data about the reviews made by the customers.
* **Order Dataset**:-
This is the core dataset. From each order you might find all other information.
* **Products Dataset**:-
This dataset includes data about the products sold by Olist.
* **Sellers Dataset**:-
This dataset includes data about the sellers that fulfilled orders made at Olist. Use it to find the seller location and to identify which seller fulfilled each product.
* **Category Name Translation**:-
Translates the productcategoryname to english.

**Input features**:- order_id,price,freight_value,product_photos_qty,product_weight_g etc.
**Target Variable**:- review_score

We will build various supervised machine learning classification models and see which succeeds in solving the given mapping between the input variables and the review feature in the best way. Let’s see each step in detail.
