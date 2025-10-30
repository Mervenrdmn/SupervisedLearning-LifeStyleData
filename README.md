# SupervisedLearning-LifeStyleData

## 📌 Project Overview
This project presents a comprehensive regression analysis on a lifestyle dataset containing **20,000 entries** and **54 features** related to health, nutrition, and exercise. The goal is to predict the **number of calories burned per 30 minutes of workout** using personal and behavioral attributes.

## 📊 Dataset
- **Size**: 20,000 rows × 54 columns  
- **Features**: Age, Gender, Workout Type, Diet Type, Body Metrics, Meal Preferences, etc.  
- **Target**: `Burns Calories (per 30 min)`  
- **Source**: *(https://www.kaggle.com/datasets/jockeroika/life-style-data)*

## 🧪 Workflow Summary

### 🔍 Exploratory Data Analysis (EDA)
- Separated numerical and categorical variables
- Visualized distributions and relationships 
- Confirmed no missing or duplicate records

### ⚠️ Outlier Detection
- Applied IQR method to detect and remove extreme values
- Cleaned the target variable for better modeling

### 📊 Correlation Analysis
- Removed highly correlated features (correlation > 0.85) to avoid multicollinearity
- Improved data structure and model efficiency

### 🧮 Encoding & Scaling
- Applied encoding after train-test split to prevent data leakage
- Used binary, one-hot, target mean, and ordinal encoding
- Scaled numerical features with RobustScaler

### 🤖 Model Training & Evaluation
- Trained models: Linear Regression, Lasso, LassoCV, Ridge, RidgeCV, ElasticNet, ElasticNetCV, SVR, K Neighbors Regressor, Decision Tree, Random Forest, Adaboost, Gradient Boosting, XGBoost, LightGBM
- Total models trained: 15
- Evaluated with MAE, RMSE, and R² metrics
- Top performers: XGBoost, LightGBM, KNN (R² > 0.99)
- 
### 🔧 Hyperparameter Tuning
- Applied RandomizedSearchCV with 5-fold cross-validation
- Hyperparameters optimized for 9 selected models:
  Ridge, Lasso, SVR, K Neighbors Regressor, Decision Tree, Adaboost, Gradient Boosting, XGBoost, LightGBM
- Ensured generalizability and improved accuracy
- XGBoost and LightGBM achieved R² scores above 0.99

## 📈 Results & Visuals
- Visual comparison of model performances
- R² score plots for train vs test
- Feature importance and error metrics

## 📁 Project Structure
SupervisedLearning-LifeStyleData/  
│  
├── SupervisedLearning-LifeStyle.ipynb       # Complete analysis, modeling, and visualization workflow  
├── Final_data.csv                           # Original lifestyle dataset (20,000 rows × 54 columns)  
├── model_results.csv                        # Performance metrics of all trained models (15 total)  
├── tuned_model_results.csv                  # Metrics after hyperparameter tuning (9 selected models)  
├── README.md    

## 🛠️ Requirements

The following Python libraries were used in this project:

```txt
pandas  
numpy  
matplotlib  
seaborn  
scikit-learn  
xgboost  
lightgbm
```
