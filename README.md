# 🛍️ Jumia Product Price Prediction & Discount Evaluation

## 📌 Project Overview

This project builds a Machine Learning system to predict product prices from Jumia and evaluate whether the discounted price is reasonable.

The objective is not only to estimate the fair market value of a product but also to determine if the applied discount truly represents a good deal for customers.

---

## 🎯 Objectives

- Predict product prices using machine learning models.
- Compare predicted fair price with the discounted price.
- Evaluate whether the discount is reasonable.
- Provide an interactive price prediction interface.

---

## 📊 Dataset

- **Source:** Scraped from Jumia website  
- **Category:** Shoes products  
- **Key Features:**
  - Brand
  - Main Material
  - Gender
  - Original Price (Preprice)
  - Discount Percentage
  - Final Price

---

## 🧹 Data Preprocessing

The dataset was prepared using the following steps:

- Handling missing values
- Encoding categorical variables (Brand, Material, Gender)
- Feature engineering for better prediction
- Preparing data for training and testing

---

## 📈 Exploratory Data Analysis

Exploratory analysis was performed to understand:

- Price distribution patterns
- Correlation between price, original price, and discount
- Brand popularity and frequency
- Impact of discount percentage on final price

These insights helped improve feature selection and model performance.

## 📊 Data Visualization

To better understand pricing behavior and discount patterns, exploratory data analysis (EDA) was performed using visualizations.

### 🔥 Correlation Heatmap

This heatmap shows the correlation between numerical variables such as:

- `price`
- `preprice`
- `discount`

It helps identify:
- Whether higher original prices receive larger discounts
- The strength of relationship between discount percentage and final price
- Pricing behavior patterns across products

![Correlation Heatmap](images/heatmap.png)

---

### ☁️ Word Cloud of Brands

The Word Cloud visualizes brand frequency in the dataset.

- Larger words represent brands with more products.
- Helps identify dominant brands in the marketplace.
- Provides insight into brand distribution within the dataset.

![Word Cloud of Brands](images/wordcloud.png)


---

## 🤖 Machine Learning Models

The following regression models were implemented:

- **XGBoost Regressor**
- **Random Forest Regressor**
- **Ensemble Model** (Average of XGBoost and Random Forest predictions)

The ensemble approach improves prediction stability and overall performance.

---

## 💡 Discount Evaluation Logic

After predicting the fair product price using the ensemble model:

- If  
  `Predicted Price ≥ Discounted Price`  
  → ✅ The discount is considered reasonable.

- If  
  `Predicted Price < Discounted Price`  
  → ⚠️ The discount may not be sufficient and the product could be overpriced.

This adds a business insight layer beyond traditional price prediction.

---

## 🖥️ How to Run the Project

1. Open the notebook:

