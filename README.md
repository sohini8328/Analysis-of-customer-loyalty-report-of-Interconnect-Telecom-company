<<<<<<< HEAD

# Interconnect Telecom: Customer Churn Prediction 
### An end-to-end data science project focused on predicting customer churn for Interconnect Telecom using machine learning. This project integrates data preprocessing, exploratory analysis, feature engineering, and advanced classification models to deliver actionable insights and a high-performing churn prediction system.

# 📌 Project Overview
### The primary objective of this project was to classify customers based on their churn status using the enddate field as the target variable. The analysis followed a structured workflow:

### 1.Data Acquisition & Exploration
### 2.Data Cleaning & Preprocessing
### 3.Exploratory Data Analysis (EDA)
### 4.Feature Engineering & Transformation
### 5.Model Building & Evaluation
### 6.Hyperparameter Tuning
### 7.Final Model Testing & Recommendations
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
### Python: Data processing and modeling
### Pandas, NumPy: Data manipulation
### Scikit-learn: Modeling and evaluation
### XGBoost, LightGBM: Gradient boosting models
### Matplotlib, Seaborn: Visualization
### SMOTE: Class balancing
## 📈 Future Enhancements
### Deploy the model as a web dashboard using Plotly Dash or Streamlit
### Integrate real-time customer data for live predictions
### Explore deep learning models for further performance gains
### Implement explainability tools like SHAP or LIME






=======
# Analysis-of-customer-loyalty-report-of-Interconnect-Telecom-company
Analysis of customer loyalty report of Interconnect Telecom company_ Sprint 17 looking at the churn customer data.
## Conclusion
This analysis successfully leveraged data science techniques to reveal critical insights into customer retention and churn prediction for Interconnect Telecom. The primary objective was to classify customers based on their churn status (indicated by the presence or absence of an ‘end date’) using the df['enddate'] variable as the target. The project followed a predefined work plan, encompassing data download, exploration, preprocessing, exploratory data analysis (EDA), feature engineering, scaling, balancing, model building, hyperparameter tuning, model selection, and final testing.
## Methodology and Key Findings:
The process began by downloading and exploring the raw data, noting that different CSV files had varying numbers of rows. This initial exploration identified the need for comprehensive preprocessing.
Data Preprocessing and Feature Engineering:
Data from various data frames was merged into a single data frame. The personal data frame contained most data, but others like phone and contract were missing over 2000 rows. Missing values were addressed primarily using Simple Imputer, which replaced absent entries with the most frequent values in each column. Missing values in the 'total charges' column were specifically handled by filling them with 0. This step was crucial for completing the dataset, stabilizing predictions, and reducing variability. Column names were converted to lowercase to avoid retrieval errors. Data types were adjusted; specifically, 'total charges' were converted to float, and 'begin date' was converted to datetime. A feature correlation analysis was conducted, including a heatmap, to understand variable relationships.
## Key correlations were identified:When Pearson correlation was conducted the results were as follows:
    •	A moderate positive correlation (0.65) exists between ‘monthlycharges’ and ‘totalcharges’ also in  ‘streamingtv’ and ‘streamingmovies’. 
    •	‘Type’ and ‘totalcharges’ showed a weak positive correlation (0.45), indicating that total charges tend to increase as the contract type changes from one year to two years, though not consistently. 
    •	A strong negative correlation (-0.83) was found between ‘begin date’ and total charges, suggesting earlier start dates might correlate with lower total charges.
    •	EDA also revealed that there are fewer senior citizens compared to non-senior citizens in the dataset.
## Data Preparation for Modeling:
Categorical variables were transformed using One-Hot Encoding. This included columns like enddate, type, paperlessbilling, paymentmethod, gender, seniorcitizen, partner, dependents, multiplelines, internetservice, onlinesecurity, onlinebackup, deviceprotection, techsupport, streamingtv, and streamingmovies. Numeric columns such as monthly charges and total charges were scaled using Standard Scaler. This ensured equal contribution from these features, enhancing prediction precision and consistency. The dataset exhibited class imbalance, with 73% of customers still with the company (loyal) and 27% having churned. SMOTE was applied to the training data to address this imbalance by introducing synthetic data points for the minority class, enhancing model fairness and robustness.
## Model Development and Selection:
The dataset was split into training, validation, and testing sets.  Logistic Regression served as the base model. Tested on the validation set, it yielded an AUC-ROC of 80% and an Accuracy of 72%. Hyper parameter tuning using grid search with cross-validation was performed on several advanced models: Random Forest Classifier, Decision Tree Classifier, XGB Classifier, and Light GBM Classifier. 
Performance on the validation set was compared:
    •	Decision Tree Classifier: AUC-ROC 85%, Accuracy 76%.
    •	Random Forest Classifier: AUC-ROC 91%, Accuracy 86%.
    •	LGBM Classifier: AUC-ROC 84%, Accuracy 75%.
    •	XGB Classifier: AUC-ROC 83%, Accuracy 75%. 
Based on validation performance, Random Forest Classifier emerged as the best model.
## Final Model Performance and Excellence:
The chosen Random Forest Classifier was tested on the unseen testing dataset. It achieved a final ROC_AUC score of 97% and an accuracy of 91%. These results demonstrate the model's superior ability to differentiate between loyal and churned customers and highlight its robustness and predictive reliability on new data.
## Difficulties Encountered:
Inconsistent row counts across data frames led to a significant volume of missing values. The data presented a class imbalance between the positive and negative classes (loyal vs. churned customers). Numeric data features were initially on different scales.

## Actionable Recommendations: 
Based on the insights derived from the analysis and the predictive power of the final model, the following strategies are recommended:
      • Strategic Retention Initiatives: Proactively target customers identified by the model as likely to churn. Predictive insights from features like service type, monthly charges, and ‘begindate’ can inform tailored interventions to address specific pain points and improve satisfaction.
      • Loyalty Incentives: Given the negative correlation between ‘begin date’ and total charges, consider introducing reward programs specifically for long-term customers (those with higher ‘begin date’ values) to strengthen their connection with the company and encourage longer tenure.
      • Leveraging Streaming Services: Capitalize on the positive correlation between ‘streamingtv’ and ‘streamingmovies’. Bundle these services or create personalized marketing campaigns around them to enhance customer engagement and drive cross-sell opportunities.
Implementing these strategies, supported by the predictive power of the Random Forest Classifier model, can significantly bolster customer retention rates, refine service delivery, and optimize profitability. Sustained analysis of customer data is essential for ongoing refinement of both the predictive modeling and business strategies to ensure continuous operational improvements.
>>>>>>> 4ab0035dbd439962d85f2d82e92c29442d78cf08
