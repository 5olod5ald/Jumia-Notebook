# 🛍️ Jumia Product Price Prediction & Discount Evaluation

## 📌 Project Overview

This project builds a Machine Learning system to predict product prices from Jumia and evaluate whether the discounted price is reasonable.

The objective is not only to estimate the fair market value of a product but also to determine if the applied discount truly represents a good deal for customers.

This project combines web scraping, data preprocessing, exploratory data analysis, and regression modeling to deliver both technical and business insights.

---

## 🎯 Objectives

- Predict product prices using machine learning models.
- Compare predicted fair price with the discounted price.
- Evaluate whether the discount is reasonable.
- Provide an interactive price prediction interface.
- Extract business insights from pricing behavior.

---

## 📊 Dataset

- **Source:** Scraped from Jumia website  
- **Category:** Shoes products  

### Key Features:
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

These preprocessing steps improved model stability and prediction accuracy.

---

# 📈 Data Visualization

To better understand pricing behavior and discount strategies, exploratory data analysis (EDA) was conducted using visualizations.

These visual insights helped uncover relationships between product features and pricing patterns before building the machine learning models.

---

## 🔥 Correlation Heatmap

The correlation heatmap analyzes the relationships between key numerical variables:

- Final Price
- Original Price (Preprice)
- Discount Percentage

It helps answer important analytical questions:

- Do higher-priced products receive larger discounts?
- How strongly does the discount percentage affect the final price?
- Is original price a strong predictor of final price?

By examining correlation strength, we gain insight into pricing behavior and promotional strategies used in the marketplace.

![Correlation Heatmap]([images/heatmap.png](https://github.com/5olod5ald/Jumia-Notebook/blob/35057e3542e3f8995216bb32d55fa876668fdd72/output1.png))

---

## ☁️ Word Cloud of Brands

The Word Cloud visualizes brand frequency within the dataset.

- Larger brand names represent higher product frequency.
- Highlights dominant brands in the market.
- Helps identify brand concentration and competitive presence.

This provides a quick visual understanding of market dominance and brand distribution.

![Word Cloud of Brands](images/wordcloud.png)

---

## 📌 Key Insights from Visualization

- Original price has a strong influence on final selling price.
- Discount percentage plays a measurable role in pricing adjustments.
- A few brands dominate product listings, indicating potential market concentration.
- Pricing patterns suggest strategic discounting rather than random reductions.

These insights guided feature selection and model development.

---

# 🤖 Machine Learning Models

The following regression models were implemented:

- **XGBoost Regressor**
- **Random Forest Regressor**
- **Ensemble Model** (Average of XGBoost and Random Forest predictions)

The ensemble approach improves prediction stability and overall performance.

---

# 💡 Discount Evaluation Logic

After predicting the fair product price using the ensemble model:

- If  
  **Predicted Price ≥ Discounted Price**  
  → ✅ The discount is considered reasonable.

- If  
  **Predicted Price < Discounted Price**  
  → ⚠️ The discount may not be sufficient and the product could be overpriced.

This adds a business insight layer beyond traditional price prediction.

---

# 🖥️ How to Run the Project

1. Open the notebook:

Notebooks/Notebook_jumia.ipynb


2. Run all cells to:
   - Load and clean the dataset
   - Train machine learning models
   - Generate predictions

3. Use the interactive prediction section to evaluate product pricing.

---

# 📁 Project Structure

Jumia-Notebook/
│
├── Data/
│ └── jumia_shoes_cleaned.csv
│
├── Notebooks/
│ └── Notebook_jumia.ipynb
│
├── images/
│ ├── heatmap.png
│ └── wordcloud.png
│
├── README.md
└── requirements.txt


---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- WordCloud
- Scikit-learn
- XGBoost

---
