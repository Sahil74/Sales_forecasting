# Sales Forecasting

## Project Overview

- This project focuses on building a predictive model to forecast the sales of various products across different stores. 
The data used in this project is from BigMart, consisting of sales data for 1,559 products across 10 stores in different cities 
for the year 2013.

## Objective

The primary objective is to analyze the features of products and stores that impact sales and build a model to predict sales 
for each product at a specific store.

## Dataset

- Source: BigMart Product Data (2013)
- Total Records: 1,559 products
- Features: Product attributes, store details, and sales figures

## Key Columns

- Item_Weight: Represents the weight of the product. Missing values in this column were filled using a mapping of similar products.
- Item_Visibility: A measure of the product's visibility on the shelf. Higher visibility may correlate with higher sales,
                making it an essential feature for analysis.
- Item_MRP: The maximum retail price of the product. This is a significant numerical feature that directly influences sales.
- Outlet_Size: The size of the store (e.g., small, medium, large). Missing values were imputed based on the type of outlet.
- Outlet_Location_Type: Describes the location of the store, such as "Urban," "Suburban," or "Rural." This feature helps understand
                      the impact of store location on sales.
## Steps Involved

### 1. Data Exploration and Preprocessing
- Loaded the dataset using pandas.
Explored the data to understand the distribution and identify missing values.
Performed exploratory data analysis (EDA) to visualize data distributions and relationships.

### 2. Feature Engineering
- Numerical Features: Analyzed and visualized key numerical features such as Item_Weight, Item_Visibility, and Item_MRP.
Categorical Features: Analyzed categorical features like Outlet_Identifier, Outlet_Size, and Item_Type.
Derived Features: Created new features like Item_Type by categorizing Item_Identifier into Food, Drink, and Non-consumable items.
Missing Data Handling: Imputed missing values for Item_Weight using product-specific or category-specific medians. Similarly, imputed Outlet_Size based on Outlet_Type.

### 3. Data Transformation
- Applied One-Hot Encoding to categorical features.
Ensured the same feature set was applied to both training and test datasets.

### 4. Model Training and Evaluation
- Models Used:
Random Forest Regressor
Gradient Boosting Regressor
HistGradient Boosting Regressor
XGBoost Regressor

- Evaluation Metrics:
R² Score
Root Mean Squared Error (RMSE)
Performed cross-validation to evaluate model performance.

### 5. Model Testing
Trained the final model on the entire training dataset.
Made predictions on the test set and evaluated model performance.
