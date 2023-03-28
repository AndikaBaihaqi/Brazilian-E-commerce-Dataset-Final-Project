# Brazilian-E-commerce-Public-Dataset-by-Olist-Final-Project

# Customer-Satisfaction-Prediction


## Introduction
E-commerce adalah platform dimana penjual dapat menjual produk dan pelanggan dapat membeli produk. Itu berarti platform e-commerce menghubungkan sejumlah besar penjual ke pelanggan melalui online. Memberikan layanan yang lebih baik kepada pelanggan adalah salah satu kunci utama untuk sukses sebagai penjual e-commerce.
Bagaimana mengukur kebaikan layanan?
Jawabannya adalah: rating suatu layanan didasarkan pada kepuasan pelanggan. Jika pelanggan tidak puas dengan layanan yang diberikan penjual, maka penjual harus fokus pada kualitas layanan untuk menarik pelanggan, sehingga meningkatkan bisnis. Jadi, pada dasarnya umpan balik pelanggan memiliki peran penting dalam bisnis e-commerce.

## Problem Statement
Review menjadi tolak ukur penting seorang calon customer untuk membeli suatu barang. menurut artikel dari bigcommerce.com, reviews dapat membantu customer untuk memilih dan melakukan komparasi barang, membangun kepercayaan customer terhadap toko, bahkan meningkatkan penjualan. sedikit review buruk akan menjadi penentu seorang calon customer untuk memutuskan pembelian di suatu toko. Dengan bertambahnya persaingan penjualan, penjual harus melakukan usaha lebih agar barang yang ditawarkan menjadi lebih menarik dan menghasilkan review yang juga baik. faktor penentu seperti jumlah foto, deskripsi barang, lama pengiriman, dan lainnya dapat menjadi faktor penentu review yang diberikan oleh customer.

## Goals
Merumuskan cara untuk meningkatkan suatu bisnis serta memberikan layanan yang lebih baik kepada pelanggan dengan menggunakan informasi kepuasan pelanggan pada platform e-commerce. Untuk itu perlu memprediksi peringkat ulasan sebelum pengguna memberikan peringkat yang sebenarnya.  Dengan bantuan prediction tool, Olist dapat membantu seller untuk memberikan prediksi review yang diberikan dengan skala 1-5 sehingga review yang diberikan customer dapat membantu seller untuk meningkatkan penjualan dengan review yang baik, tentunya akan membantu calon pembeli lain yakin untuk membeli pada toko yang memiliki review terbaik.

## Analytic Approach
Membangun prediksi "tool" dan menganalisis dataset yang diberikan dengan mengklasifikasikan review score kedalam review negatif atau review positif, yang nantinya berguna untuk membantu seller meningkatkan penjualan dengan review yang baik, tentunya akan membantu calon pembeli yakin untuk membeli pada toko yang memiliki review terbaik.


**Prediksi kepuasan pelanggan (0 untuk negatif dan 1 untuk positif) dari pembelian dari situs e-commerce brazilian Olist.**

## ML formulation of business problem:
Untuk pesanan tertentu, kita perlu memprediksi skor kepuasan pelanggan mengingat fitur-fiturnya yang berbeda seperti harga, deskripsi barang, pengiriman tepat waktu, status pengiriman, dll. Masalah yang diberikan adalah **Masalah Klasifikasi Biner** karena masalah tersebut akan mengembalikan skor ulasan pelanggan atas pesanan sebagai 0 atau 1.


## Data
### Data Overview:
**Sumber**:- https://www.kaggle.com/olistbr/brazilian-ecommerce

<img src="https://i.imgur.com/HRhd2Y0.png" />

### Data Description:
* **Customers Dataset**:-
Dataset ini memiliki informasi tentang pelanggan dan lokasinya. Gunakan untuk mengidentifikasi pelanggan unik dalam kumpulan data pesanan dan untuk menemukan lokasi pengiriman pesanan.
* **Geolocation Dataset**:-
Kumpulan data ini memiliki informasi kode pos Brasil dan koordinat lintang/bujurnya. Gunakan untuk memplot peta dan menemukan jarak antara penjual dan pelanggan.
* **Order Items Dataset**:-
Kumpulan data ini mencakup data tentang item yang dibeli dalam setiap pesanan.
* **Payments Dataset**:-
Kumpulan data ini mencakup data tentang opsi pembayaran pesanan.
* **Order Reviews Dataset**:-
Kumpulan data ini mencakup data tentang ulasan yang dibuat oleh pelanggan.
* **Order Dataset**:-
Ini adalah kumpulan data inti. Dari setiap pesanan Anda mungkin menemukan semua informasi lainnya.
* **Products Dataset**:-
Kumpulan data ini mencakup data tentang produk yang dijual oleh Olist.
* **Sellers Dataset**:-
Kumpulan data ini mencakup data tentang penjual yang memenuhi pesanan yang dibuat di Olist. Gunakan untuk menemukan lokasi penjual dan untuk mengidentifikasi penjual mana yang memenuhi setiap produk.
* **Category Name Translation**:-
Terjemahan dari nama kategori produk ke bahasa Inggris.

**Input features**:- price,freight_value,product_photos_qty etc.
**Target Variable**:- review_score
