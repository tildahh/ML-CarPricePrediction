# 🚗 ML-CarPricePrediction

## 📌 Overview
A data-driven project analyzing 426,000+ used cars to predict prices and optimize dealership inventory decisions. Using advanced regression techniques and the CRISP-DM framework, we achieved 77% prediction accuracy while uncovering key market insights.

![Kurt](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/kurt.jpeg)

## 🎯 Business Understanding
### Problem Statement
Used car dealerships face significant challenges in:
- Determining optimal pricing strategies
- Managing inventory efficiently
- Understanding market value drivers
- Maintaining competitive advantage

### Project Goals
1. Develop an accurate price prediction model
2. Identify key price influencing factors
3. Provide actionable insights for inventory optimization

## 🔍 Methodology: CRISP-DM Framework
![CrispDM](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/crisp.png)

Following the CRISP-DM methodology, we systematically:
1. Understood business objectives
2. Analyzed data characteristics
3. Prepared data for modeling
4. Developed predictive models
5. Evaluated performance
6. Deployed insights

## 📊 Key Insights & Visualizations
### 1. Market Distribution
![Car_Manufacturers](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/cars_by_make.png)
*Analysis of market share by manufacturer reveals dominant players and niche segments.*

### 2. Price Variations by Manufacturer
![Car Manufacturer vs. Price](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/1.png)
*Key Finding: Premium brands (Ferrari, Aston Martin, Tesla) command significantly higher prices, indicating luxury market opportunities.*

### 3. Feature Correlations
![Feature Correlation with Price](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/2.png)
*Heat map revealing strongest price predictors and interrelationships between features.*

### 4. Condition Impact
![Price vs Condition](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/price_vs_condition.png)
*Clear relationship between vehicle condition and market value, guiding quality standards.*

### 5. Age-Price Relationship
![Price vs. Year](https://github.com/tildahh/ML-CarPricePrediction/blob/main/images/3.png)
*Strong correlation between vehicle age and price, informing inventory age management.*

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


## 🛠️ Technical Implementation

### Data Processing Pipeline
```python
Pipeline(steps=[
    ('preprocessor', ColumnTransformer([
        ('nom', OneHotEncoder(drop='first', handle_unknown='ignore'),
         ['manufacturer', 'fuel', 'transmission', 'drive', 'type', 'paint_color']),
        ('ord', OrdinalEncoder(), ['condition']),
        ('num', StandardScaler(), ['year', 'cylinders', 'odometer'])
    ])),
    ('model', RandomForestRegressor(max_features='sqrt', n_estimators=200))
])
```

### Model Performance Comparison
| Model | MAE | RMSE | R² Score |
|-------|-----|------|----------|
| Linear Regression | 0.378 | 0.516 | 0.509 |
| Ridge Regression | 0.378 | 0.516 | 0.509 |
| Random Forest | 0.378 | 0.516 | 0.769 |

## 💡 Strategic Recommendations

### 1. Inventory Optimization
- Focus on newer vehicles (< 5 years old)
- Maintain diverse brand portfolio with emphasis on high-margin segments
- Implement condition-based acquisition strategy

### 2. Pricing Strategy
- Develop dynamic pricing models based on:
  - Vehicle age and mileage
  - Brand value positioning
  - Market demand patterns
  - Seasonal trends

### 3. Quality Management
- Establish condition assessment standards
- Prioritize reconditioning for high-ROI vehicles
- Monitor condition-price relationships

[Link to notebook](https://github.com/tildahh/ML-CarPricePrediction/blob/main/prompt_II.ipynb)
---
*This project demonstrates the power of data-driven decision-making in the competitive used car market. For questions or collaborations, please [reach out](https://www.linkedin.com/in/sara-orona/).*
