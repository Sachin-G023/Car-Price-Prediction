# Car Price Prediction 🚗📈

## Project Overview

**Project Title**: Car Price Prediction    
**Dataset**: `CarPrice.csv`

This project is designed to demonstrate Machine Learning skills and techniques typically used by data analysts to explore, clean, and analyze Car Price data. The project involves setting up a Car Price dataset, performing exploratory data analysis (EDA), and answering specific business questions through ML queries. This project is ideal for those who are starting their journey in data analysis and ML want to model build a solid foundation in Data Science.

## Objectives

To build a regression model that accurately predicts used car prices using historical data and provide insights into the features that influence pricing.

## Project Structure

### 1. Dataset

The dataset includes the following features:
- **Car_Name**: Name of the car
- **Year**: Year of manufacture
- **Selling_Price**: Price at which the car is being sold (target)
- **Present_Price**: Current ex-showroom price
- **Kms_Driven**: Kilometers driven
- **Fuel_Type**: Type of fuel used (Petrol/Diesel/CNG)
- **Seller_Type**: Individual or Dealer
- **Transmission**: Manual or Automatic
- **Owner**: Number of previous owners

### 2. 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib & Seaborn (for EDA)
- Scikit-learn (ML modeling)
- Jupyter Notebook

### 3. Data Exploration & Cleaning

- Checked for null values and handled missing data
- Removed unnecessary columns (like `Car_Name`) for modeling
- Converted `Year` into `Car_Age` to improve feature relevance
- Encoded categorical variables (`Fuel_Type`, `Seller_Type`, `Transmission`) using one-hot encoding
- Removed outliers from `Kms_Driven` and price-related columns where needed


### 4. 📈 ML Workflow

1. **Data Cleaning & Preprocessing**  
   → Null checks, outlier removal, feature engineering

2. **Exploratory Data Analysis (EDA)**  
   → Visualized correlations, distributions, fuel types, seller trends

3. **Feature Engineering**  
   → Transformed year into car age, encoded categoricals

4. **Model Training**  
   → Linear Regression, Random Forest Regressor

5. **Model Evaluation**  
   → Used R² Score, MAE, and cross-validation

6. **Hyperparameter Tuning**  
   → Used GridSearchCV for optimized performance

7. **Model Saving**  
   → Final model saved using Pickle



### 5. 🚀 Streamlit Web App 

You can deploy the model using [Streamlit]

### 6. Run locally:
```bash
pip install streamlit
streamlit run app.py




## 📊 **Findings**

-Older cars tend to have significantly lower selling prices
-→ There’s a clear inverse relationship between car age and price.

-Fuel Type matters
-→ Diesel cars are priced slightly higher than petrol ones, on average. CNG cars show lower resale prices.

-Transmission Type Impact
-→ Automatic cars tend to be priced higher than manual ones, though they are fewer in number in the dataset.

-Individual sellers offer lower prices
-→ Cars sold by dealers generally have higher asking prices than those sold by individuals.

-Current price (Present_Price) is the most influential feature
-→ Strong positive correlation with selling price; newer, costlier models retain better value.

-Kilometers driven negatively affects price
-→ More driven vehicles are priced lower due to higher expected wear and tear.

-Outliers existed in Kms_Driven and Selling_Price
-→ Some extreme values (e.g., over 5,00,000 km) were removed for better model accuracy.



## 📄 Reports

--Top Features by Importance (Random Forest Regressor):

--Present_Price

--Car_Age

--Kms_Driven

--Fuel_Type_Diesel

--Seller_Type_Individual

--Model Comparison:

| Model                   | R² Score | MAE (Mean Absolute Error) | Notes                       |
| ----------------------- | -------- | ------------------------- | --------------------------- |
| Linear Regression       | 0.86     | 1.21                      | Underfitting observed       |
| Decision Tree Regressor | 0.91     | 0.83                      | Slightly overfitted         |
| **Random Forest**       | **0.98** | **0.72**                  | Best performance (selected) |

--Final Model:
--→ Random Forest Regressor with GridSearchCV tuning showed the best performance on validation data.

--Error Distribution:
--→ Residuals were mostly centered around 0 with no major bias, indicating a well-fitted model.



## Conclusion

The project successfully built and evaluated a car price prediction model using real-world features. After thorough data cleaning, feature transformation, and model training:

The Random Forest model achieved 93% accuracy.

Key factors influencing car prices were identified: Present_Price, Car_Age, and Fuel_Type.

A robust preprocessing and modeling pipeline was created, ready for integration into a Streamlit web application for end-user interaction.

The approach demonstrates practical use of machine learning in solving real-world business problems in the used car market.

## Author - Sachin G.

This project is part of my portfolio, showcasing the SQL skills essential for data analyst roles. If you have any questions, feedback, or would like to collaborate, feel free to get in touch!

Thank you for your support, and I look forward to connecting with you!
