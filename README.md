# Walmart Store Sales Prediction

## Project Overview
This project aims to predict the weekly sales of Walmart stores using historical sales data and various features such as store number, holiday flag, temperature, fuel price, Consumer Price Index (CPI), and unemployment rate. The goal is to build a machine learning model that accurately forecasts weekly sales to aid in business planning and decision-making.

## Data Preprocessing

- Missing Values: Handled missing values using SimpleImputer for both categorical and numerical features.
- Date Handling: Converted the 'Date' column to datetime format and extracted additional features such as year, month, day, and day of the week.
- Outlier Removal: Identified and removed outliers in the numerical columns to improve model performance.

## Exploratory Data Analysis (EDA)

- Data Visualization: Created boxplots to visualize the distribution of Temperature, Fuel Price, CPI, and Unemployment.
- Sales Trends:
- Yearly Sales: Observed a slight decrease in sales from 2010 to 2012.
- Monthly Sales: Highest sales recorded in February.
- Day of the Month Sales: Spikes in sales around the 12th of each month.
- Day of the Week Sales: Majority of sales occur on Fridays.
- Store Sales: Notable disparities in sales between different stores.
- Correlation Analysis: Analyzed pairwise correlations and a heatmap to identify relationships between features. CPI and temperature showed negative correlations with weekly sales.


## Model Building
Used multiple linear regression to predict weekly sales. The features used in the model are:

- Store
- Holiday_Flag
- Temperature
- Fuel_Price
- CPI
- Months
- Year
- Day
- Day_of_week

## Addressing Overfitting

To prevent overfitting, we applied the following techniques:

- Cross-Validation: Used k-fold cross-validation to ensure the model generalizes well to unseen data.
- Regularization: Applied Ridge Regression (L2 regularization) to penalize large coefficients and reduce model complexity.
- Feature Selection: Selected the most relevant features based on correlation analysis and domain knowledge to avoid overfitting from irrelevant features.
- Hyperparameter Tuning: Used GridSearchCV to find the optimal hyperparameters for the model, balancing bias and variance.

## Results
After preprocessing the data and training the model, we evaluated its performance using metrics such as R² score, mean absolute error (MAE), and mean squared error (MSE).

- R² Score: 
- Mean Absolute Error (MAE): 
- Mean Squared Error (MSE):

## Conclusion
The model provides a good baseline for predicting weekly sales at Walmart stores. By analyzing various features and their impact on sales, we can derive actionable insights to optimize store operations and marketing strategies.

Project Files
Data: The dataset used for this project is located in the data folder.
Notebook: The Jupyter Notebook containing the entire analysis and model building process is in the notebooks folder.
Scripts: The scripts for data preprocessing, model training, and evaluation are available in the scripts folder.
Results: Visualizations and results are stored in the results folder.
