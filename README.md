# Interconnect Telecom: Customer Churn Prediction 
### An end-to-end data science project focused on predicting customer churn for Interconnect Telecom using machine learning. This project integrates data preprocessing, exploratory analysis, feature engineering, and advanced classification models to deliver actionable insights and a high-performing churn prediction system.

# 📌 Project Overview
### The primary objective of this project was to classify customers based on their churn status using the enddate field as the target variable. The analysis followed a structured workflow:

 1.Data Acquisition & Exploration
 2.Data Cleaning & Preprocessing
 3.Exploratory Data Analysis (EDA)
 4.Feature Engineering & Transformation
 5.Model Building & Evaluation
 6.Hyperparameter Tuning
7.Final Model Testing & Recommendations
## 🧠 Methodology & Key Findings
## Data Preprocessing & Feature Engineering
### Merged multiple CSV files into a unified dataset.
### Addressed missing values using Simple Imputer and domain-specific logic (e.g., filling totalcharges with 0).
### Standardized column names and corrected data types (totalcharges to float, begindate to datetime).
### Conducted correlation analysis to identify key relationships.
## Notable Correlations
### Positive (0.65): monthlycharges ↔ totalcharges, streamingtv ↔ streamingmovies
### Moderate (0.45): type ↔ totalcharges
### Strong Negative (-0.83): begindate ↔ totalcharges
### Demographic Insight: Fewer senior citizens than non-seniors in the dataset
## 🧪 Modeling Pipeline
### Data Preparation
### Applied One-Hot Encoding to categorical features
### Scaled numeric features using StandardScaler
### Addressed class imbalance (73% loyal, 27% churned) using SMOTE
## Model Development
### Baseline: Logistic Regression (AUC-ROC: 80%, Accuracy: 72%)
### Advanced Models (with Grid Search CV):
### Decision Tree: AUC-ROC 85%, Accuracy 76%
### Random Forest: AUC-ROC 91%, Accuracy 86%
### LightGBM: AUC-ROC 84%, Accuracy 75%
### XGBoost: AUC-ROC 83%, Accuracy 75%
## Final Model Performance
### Random Forest Classifier selected as the best model
### Test Set Results: AUC-ROC 97%, Accuracy 91%
## ⚠️ Challenges Faced
### Inconsistent row counts across data sources
### High volume of missing values
### Class imbalance in churn labels
### Feature scaling inconsistencies
## 💡 Actionable Recommendations
### * Strategic Retention Initiatives
### Use model predictions to proactively engage at-risk customers based on service type, charges, and tenure.

### * Loyalty Incentives
### Reward long-term customers (with earlier begindate) to increase retention and lifetime value.

### * Streaming Service Bundling
### Leverage the strong correlation between streamingtv and streamingmovies to create bundled offers and personalized campaigns.

## 🛠️ Tools & Technologies
* Python: Data processing and modeling
* Pandas, NumPy: Data manipulation
* Scikit-learn: Modeling and evaluation
* XGBoost, LightGBM: Gradient boosting models
* Matplotlib, Seaborn: Visualization
* SMOTE: Class balancing
## 📈 Future Enhancements
* Deploy the model as a web dashboard using Plotly Dash or Streamlit
* Integrate real-time customer data for live predictions
* Explore deep learning models for further performance gains
* Implement explainability tools like SHAP or LIME
