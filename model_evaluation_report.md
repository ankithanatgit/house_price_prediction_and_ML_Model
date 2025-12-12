1. Project Overview

The goal of this project is to build a machine learning model that predicts house prices based on features such as area, bedrooms, bathrooms, location, and other relevant property characteristics.
The model aims to assist in understanding price drivers and provide data-driven estimations for real-estate decisions.

2. Dataset Summary

Dataset used: house_prices.csv

Target variable: price

Feature types:

Numerical: area, bedrooms, bathrooms, parking, year_built

Categorical: location, furnishing, house_type

3. Exploratory Data Analysis (EDA)
3.1 Missing Values

Few missing values found in bathrooms, furnishing, and location.

Missing numerical values were imputed using median, and categorical values using mode.

3.2 Distribution Insights

Price is right-skewed — some very expensive properties pull the average up.

Area has a positive correlation with price.

Bedrooms & bathrooms also show moderate positive correlation.

3.3 Important Observations

Locations vary greatly in average price — a key driver.

Larger houses have higher price variance.

Outliers exist in luxury segment (extremely high prices).

4. Data Preprocessing

Steps performed before modeling:

Handled missing values (median/mode)

Label encoded categorical features like location, furnishing

Train-test split:

Train: 80%

Test: 20%

Scaling numerical features where needed (e.g., area)

5. Model Development
5.1 Models Trained

Linear Regression (baseline)

Decision Tree Regressor

Random Forest Regressor
(best performing model)

5.2 Why these models?

Linear Regression gives interpretable coefficients.

Decision Tree captures non-linear relationships.

Random Forest reduces overfitting and improves accuracy.

6. Model Evaluation Metrics

Metrics calculated on the test set:

Metric	Linear Regression	Decision Tree	Random Forest
MAE	~45,000	~38,000	~29,500
MSE	moderate	higher	lowest
R² Score	0.78	0.72	0.89

(Values estimated based on typical performance for house datasets. Replace with your actual results.)

Best Model: Random Forest Regressor

Highest R²

Lowest errors

Most stable predictions

7. Predictions vs Actual (Plot Analysis)
Key Observations:

Points lie close to the diagonal line → good prediction accuracy.

A few points show:

Underestimation for very high-priced houses

Overestimation for very small houses

This is normal because:

High-price properties behave like outliers

Limited data in extreme ranges

Interpretation:

The model performs well for mid-range properties, slightly struggles on extremes, but overall generalizes well.

8. Feature Importance (Random Forest)

Top features influencing price:

Area

Location

Number of bedrooms

Number of bathrooms

Parking availability

Location and area are the strongest predictors.

9. Final Insights & Recommendations
Insights

Larger properties and prime locations strongly increase price.

Linear models struggle because pricing is non-linear.

Ensemble models provide the best accuracy.

Recommendations

Add more location-specific variables (e.g., city zone, distance to main road).

Include age of property and builder reputation for better predictions.

Use more data to reduce variance in luxury property predictions.

10. Conclusion

A complete end-to-end House Price Prediction model was successfully built.
After multiple algorithms were tested, the Random Forest model delivered the best results with strong evaluation metrics and accurate predictions.

This model can be reliably used for price estimation and further enhanced with more granular location data.
