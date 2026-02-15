# Jumia Product Price Prediction & Price Evaluation

This project focuses on predicting product prices from Jumia and evaluating if the discounted price is reasonable. It includes data scraping, cleaning, visualization, and building predictive models.

## Project Overview

**Data Source:** Scraped from Jumia website.

**Data Cleaning:**
- Handled missing values
- Encoded categorical variables (Brand, Material, Gender)
- Created additional features for better prediction

## Data Visualization

Explored distributions of product prices and analyzed relationships between features and prices using plots.

### Correlation Heatmap
Shows correlation strength between numeric variables (`price`, `preprice`, `discount`). Helps understand if expensive products get bigger discounts.

![Correlation Heatmap](images/output1.png)

### Word Cloud of Brands
Shows the most popular brands visually (bigger word = more products). Helps quickly identify brand popularity.

![Word Cloud of Brands](images/output2.png)

## Machine Learning Models

- **XGBoost Regressor**
- **Random Forest Regressor**
- **Ensemble Model:** Average of XGBoost and Random Forest predictions

## Price Evaluation

The models not only predict the product price but also evaluate if the discounted price is reasonable:

- If `Final Ensemble Prediction >= Discounted Price`: ✅ Discount is good and price is reasonable.
- If `Final Ensemble Prediction < Discounted Price`: ⚠️ Discount is not enough and price is high.

## How to Use

Open the Jupyter Notebook (`Notbook.ipynb`) to see the full workflow:

- Data scraping
- Cleaning and preprocessing
- Visualization
- Model training

Use the **Prediction Section** to input product details and get predicted prices and evaluation:

```python
brand = input("Brand: ")
material = input("Main Material: ")
gender = input("Gender: ")
preprice = float(input("Original price (preprice): "))
discount = float(input("Discount %: "))

xgb_p, rf_p, final_p = predict_price(brand, material, gender, preprice, discount)

print("XGBoost Prediction:", round(xgb_p, 2))
print("RandomForest Prediction:", round(rf_p, 2))
print("Ensemble Prediction:", round(final_p, 2))

discounted_price = preprice * (1 - discount/100)
if final_p >= discounted_price:
    print("✅ Discounted price is reasonable")
else:
    print("⚠️ Discounted price is too high")
