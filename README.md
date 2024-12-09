# AIML-Practical-App2
## What Drives the Price of a Car?

## 1.	Introduction
This report summarizes results from an in-depth analysis of what determines used car prices with the use of machine learning models to predict and gauge pricing trends. The analysis focuses on the needs of used car dealers by trying to optimize their inventory strategy through understanding price determinants. Using data science techniques, this project identifies key insights and actionable recommendations to be used in decision-making.

## 2.	Dataset Overview
The dataset includes 18 columns with detailed information about vehicles:
Key Features:

•	id: Unique vehicle identifier.

•	price: Vehicle price (target variable).

•	year: Manufacture year.

•	manufacturer: Vehicle brand (e.g., Ford, Toyota).

•	condition: Vehicle condition (e.g., excellent, good).

•	fuel: Fuel type (e.g., gas, diesel, electric).

•	transmission: Type of transmission (automatic, manual).

•	odometer: Distance traveled by the vehicle in miles.

•	title_status: Ownership status (e.g., clean, salvage).

## 3.	Data Preprocessing

To ensure the quality and usability of the data, the following preprocessing steps were performed:

3.1.	Handling Missing Values:
•	Missing data in key columns, such as price and year, was removed to maintain dataset integrity.

3.2.	Outlier Removal:
•	Extreme outliers in price and mileage were excluded to avoid skewed predictions.

3.3.	Feature Transformation:
•	Categorical variables, such as manufacturer and condition, were encoded using techniques like one-hot encoding for model compatibility.

3.4.	Data Splitting:
•	The dataset was split into training and testing sets (e.g., 80% training and 20% testing) to validate model performance.

## 4.	EDA (Exploratory Data Analysis)
Key insights from the exploratory analysis include:

4.1.	Price Distribution:
•	Prices exhibited a positively skewed distribution with a few high-value outliers, confirming the need for log transformations in modeling.

4.2.	Feature Correlations:
•	Strong correlations were observed between year and price, indicating newer cars tend to be priced higher.

4.3.	Category Trends:
•	Certain manufacturers (e.g., tesla,	aston-martin) showed higher average prices, likely due to brand reliability and market demand.
•	Vehicle condition and title status significantly impacted pricing, with "excellent" and "" vehicles commanding premium prices.

## 5.	Model Development
Multiple machine learning models were implemented to predict used car prices like RandomForrest, XGBoost, AdaBoost, LinearRegression etc. The key models include:

5.1.	Linear Regression:

•	A basic model to establish a baseline.

•	Performance:
  
      o	MSLE: 0.8220
      o	Root MSLE: 0.9067
      o	R² Score: 0.0065 (0.65%)

•	Insights: Linear Regression struggled to capture the complex relationships in the data, highlighting the need for advanced models.

5.2.	Ridge Regression:

•	Incorporated regularization to address overfitting.

•	Performance:

      o	MSLE: 0.8221
      o	Root MSLE: 0.9067
      o	R² Score: 0.0065 (0.65%)
      
•	Insights: Performance was nearly identical to Linear Regression, indicating limited effectiveness.

5.3.	AdaBoost Regressor:

•	A powerful ensemble model leveraging weak learners for better predictions.

•	Performance:

      o	MSLE: 0.0186
      o	Root MSLE: 0.1363
      o	R² Score: 0.9861 (98.61%)

•	Insights: AdaBoost significantly outperformed all other models, demonstrating its ability to capture complex, nonlinear relationships.

## The best alternative to predict the prices for used cars is AdaBoost Regressor, a report reveals. The method can better explain pricing variability and is more accurate, which is a plus when dealing with used car salesmen.

