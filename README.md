# Olist-E-Commerce-Exploratory-Analysis

This repository contains all Python scripts, data cleaning steps, and exploratory analyses performed as part of Achievement 6: Advanced Analytics & Dashboard Design. The curated results are presented in an interactive Tableau dashboard.

---

## 📌 Project Description

This project was developed as part of *Achievement 6: Advanced Analytics & Dashboard Design*. The goal was to analyze the **Olist Brazilian E-Commerce Dataset (2016–2018)** and explore factors affecting **shipping costs**, customer distribution, and logistics challenges in Brazilian e-commerce.

The analysis was conducted in **Python** (exploratory, regression, clustering, and geospatial analysis) and the results were curated into an **interactive Tableau dashboard**. The dashboard tells the story of how product attributes (weight, size), geography, and customer behavior impact freight pricing and delivery performance.

---

## 📊 Data Source

The dataset is publicly available on [Kaggle: Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce).

It contains \~100,000 orders placed between 2016 and 2018 and is divided into 9 related tables:

* **Orders** – order status, timestamps, estimated vs. actual delivery dates
* **Order Items** – product ID, seller ID, price, freight value, quantity
* **Payments** – payment method, installments, amount paid
* **Customers** – anonymized customer IDs, zip code prefixes, city/state
* **Sellers** – seller IDs, location (zip, city, state)
* **Products** – product category, weight, dimensions
* **Reviews** – customer ratings (1–5), comments, review timestamps
* **Geolocation** – zip code prefixes mapped to latitude/longitude
* **Category Translations** – product categories (Portuguese → English)

These tables can be connected using `order_id`, `customer_id`, `product_id`, and `seller_id`.

**Additional source:**

* **Geospatial shapefile:** Brazil states boundaries for mapping customer and seller distribution

---

## 🔍 Research Questions

The project focused on answering the following questions:

1. **Customer Distribution**

   * Where are customers located in Brazil?
   * Which regions generate the most e-commerce orders?
   * How does this concentration affect logistics and costs?

2. **Shipping Costs**

   * Do **weight** and **size** explain variation in freight prices?
   * Does paying more for shipping result in **faster delivery**?

3. **Business Implications**

   * What can e-commerce businesses learn to **optimize logistics**?
   * Which regions or product categories need special strategies to reduce costs?

---

## 🧹 Cleaning Procedures (Exercise 6.1)

Data cleaning was performed in Python for each table. The main steps included:

* **Column checks** – renaming columns for clarity and ensuring consistent naming conventions
* **Data types** – verifying and converting data types (e.g., timestamps, numeric fields)
* **Categorical variables** – counting values to check distributions and anomalies
* **Missing values** – identifying and handling missing data appropriately
* **Duplicate rows** – checking for and removing duplicates
* **ID uniqueness** – ensuring keys like `order_id` and `customer_id` are unique
* **New columns** – creating additional columns where useful (e.g., delivery duration)
* **Basic statistics** – using `.describe()` to summarize distributions and detect irregularities
* **Merging** – integrating the **Category Translation** dataset into the Products dataset for English category names

---

## 🛠️ Methods & Techniques

**Exploratory Analysis:** Scatterplots, correlations, descriptive statistics

**Geospatial Analysis:** Choropleth maps of customer distribution across Brazil

**Regression Analysis:** Testing linear relationships between shipping cost and weight/size

**Cluster Analysis:** K-means to segment parcels into natural groups

**Dashboard Design:** Curated results presented in Tableau

---

## 📈 Key Insights

* **Geography:** Customers are heavily concentrated in the Southeast, especially São Paulo.

* **Costs:** Weight and size are strong cost drivers but explain <40% of variation.

* **Clusters:** Three parcel groups emerged (small/light, medium, large/heavy).

* **Delivery times:** Similar across clusters (~23–25 days), so cost is driven mainly by product attributes, not speed.

---

## 🚀 Recommendations & Next Steps

**Expand Regionally:** Strengthen seller presence outside the Southeast to reduce long-distance costs.

**Analyze Product Categories:** Identify cost drivers by category (e.g., electronics vs. furniture).

**Refine Clustering:** Test additional clusters.

**Add Distance Metrics:** Incorporate delivery distance and route data for stronger models.

---

## 📊 Tableau Dashboard

The final interactive dashboard is published here: 👉 [Tableau Dashboard Link](https://public.tableau.com/app/profile/habibe.zare.haghighi/viz/OlistE-CommerceStoryboard/OlistE-Commerce)

*Note: The dashboard includes only selected results that best tell the story of shipping costs in Brazil. Additional analyses are available in this repository.*

---
