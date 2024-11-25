# 🚗 ML-CarPricePrediction
![Kurt](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/kurt.jpeg)

This project explores a dataset containing details on over 426,000 used cars with the goal of identifying factors that significantly impact car prices using various regression techniques. The model considers multiple features including manufacturer, fuel type, transmission, mileage, and condition to provide accurate price predictions, achieving an R² score of 0.77 with the best performing model.

## CRISP-DM Framework 
Utilizing the CRISP-DM methodology, this analysis aims to equip used car dealerships with data-driven insights to optimize their inventories based on consumer preferences and market trends.

![CrispDM](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/crisp.png)

### 🎯 Business Problem
The used car market lacks standardized pricing mechanisms, making it challenging for both buyers and sellers to determine fair market values. This project aims to:

* Create an accurate price prediction model for used cars
* Identify key factors influencing car prices
* Provide data-driven insights for market participants

### 📈 Results & Impact
The goal was to identify factors that affect the price of used cars to help a used car dealership optimize inventory.

* Achieved 77% accuracy in price predictions
* Identified key price influencing factors:
  * Newer vehicles tend to have higher prices.
  * Lower mileage correlates with higher pricing.
  * Some brands and models are more favorable in retaining value.
  * Cars in better condition command higher prices.
* Successfully captured non-linear relationships in the data
* Model performance validated through cross-validation

## Visualizations
To support our findings, we have included a series of visualizations that illustrate the key factors affecting used car prices:
1. **Number of Cars by Make in Dataset**:
![Car_Manufacturers](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/cars_by_make.png)

2.  **Boxplot - Car Manufacturer vs. Price**:
![Car Manufacturer vs. Price](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/1.png)
This boxplot indicates the variance in prices across different car manufacturers, highlighting the brands that command higher prices in the used car market. Ferrari, Aston Martin and Tesla are the most expesive brands.

3. **Heatmap - Feature Correlation with Price**:
![Feature Correlation with Price](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/2.png)
The heatmap shows how different features correlate with the price of used cars, guiding dealers on what features contribute most to a car’s value.

4. **Price vs Condition**:
![Price vs Condition](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/price_vs_condition.png)

5. **Scatter Plot - Price vs. Year**:
![Price vs. Year](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/3.png)
A scatter plot that showcases the relationship between the car’s price and its year, clearly showing that newer cars tend to fetch higher prices.

### 🛠️ Technical Approach
## Data Processing & Feature Engineering
- Implemented comprehensive preprocessing pipeline using scikit-learn
- Features included: manufacturer, fuel type, transmission, drive type, condition, year, cylinders, odometer
- Applied various encoding techniques:
  - OneHotEncoder for categorical variables
  - OrdinalEncoder for ordinal features (condition ratings)
  - StandardScaler for numerical features

## Models Developed & Evaluated
1. Baseline Linear Regression
  - Initial model to establish baseline performance
  - MAE: 0.378, RMSE: 0.516, R² Score: 0.509
2. Ridge Regression
  - Implemented L2 regularization
  - MAE: 0.378, RMSE: 0.516, R² Score: 0.509
3. Random Forest Regressor (Best Performing)
  - Hyperparameters:
    - n_estimators: 200
    - max_features: 'sqrt'
- Final R² Score: 0.769

## Key Recommendations
* Prioritize newer, low-mileage cars in inventory.
* Adjust stock levels based on brand and model insights.
* Implement a dynamic pricing model based on our findings.

## Conclusion
This project provides valuable insights into the used car market, assisting dealers in making informed decisions to optimize their inventory and improve profitability. The analysis demonstrates the power of data-driven decision-making in a competitive market.

[Link to notebook](https://github.com/tildahh/ML-CarPricePrediction/blob/main/prompt_II.ipynb)
