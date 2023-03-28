# Brazilian-E-commerce-Public-Dataset-by-Olist-Final-Project

# Customer-Satisfaction-Prediction
Predict customer satisfaction for an e-commerce purchase

# <center>Customer Satisfaction Prediction - Brazillian e-Commerce Public Dataset</center>

In today's era of internet, every sector is generating a lot of data which cannot be processed and analysed to find meaningful insights by mere humans. So, we take help of computers to find meaningful insights on the data using statiscal methods and machine learning techniques. Today, I am going to take you through a real-world data science problem which I have picked from Kaggle’s open data-set provided by Brazilian e-commerce Olist and will demonstrate my way of solving it. This case study solves everything right from scratch. So, you will get to see each and every phase of how in the real world, a case study is solved. Before I talk about my approach of solving the problem, I shall briefly walk you through the problem statement of the case study in question.

## Problem Statement
This is a Brazilian ecommerce public dataset of orders made at Olist Store. The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers. A geolocation dataset that relates Brazilian zip codes to lat/lng coordinates has also been released.

This dataset was generously provided by Olist, the largest department store in Brazilian marketplaces. Olist connects small businesses from all over Brazil to channels without hassle and with a single contract. Those merchants are able to sell their products through the Olist Store and ship them directly to the customers using Olist logistics partners. See more on the website: www.olist.com
After a customer purchases the product from Olist Store a seller gets notified to fulfill that order. Once the customer receives the product, or the estimated delivery date is due, the customer gets a satisfaction survey by email where he can give a note for the purchase experience and write down some comments.

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
