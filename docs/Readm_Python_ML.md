# Churn Prediction with Random Forest – Python (Jupyter Notebook)
This documentation helps users understand the `Churn_Prediction.ipynb` notebook, which performs customer churn prediction for INTELEVO Networks using a **Random Forest Classifier**.

## 📁 Script: `Churn_Prediction.ipynb`

The notebook includes the following sections:

### 1. Dataset Extraction
- Imports the final, cleaned dataset (`Final_Customer_Data_Canadian_Cities.csv`) prepared via SQL  
- Displays basic structure, column types, and missing values

### 2. Data Processing and Preparation
- Encodes categorical variables using `get_dummies()`  
- Splits the dataset into features (`X`) and target (`y`)  
- Performs a **train-test split** for model validation

Data Processing Example
```python
# Converting the columns encoding categorical variables to numerical values
label_encoders = {}
for column in columns_to_encode:
    label_encoders[column] = LabelEncoder()
    data[column] = label_encoders[column].fit_transform(data[column])

# Splitting data into features and target (independent and dependent variables)
x = data.drop('Customer_Status', axis = 1)
y = data['Customer_Status']

# Splitting data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(x, y, test_size = 0.2, random_state = 42)
```

### 🌳 3. Training the Random Forest Model
- Initializes and fits a `RandomForestClassifier`  
- Trains the model using the training set  
- Sets parameters like `n_estimators` and `random_state` for reproducibility

![Screenshot 2025-06-16 130623](https://github.com/user-attachments/assets/2b521664-b161-41d4-be8f-2269ae35ba77)

### 4. Evaluating the Random Forest Model
- Evaluates performance using:
  - **Confusion Matrix**
  - **Accuracy Score**
  - **Classification Report** (Precision, Recall, F1 Score)
- Displays model interpretability via **Feature Importance Plot**

![Screenshot 2025-06-16 130804](https://github.com/user-attachments/assets/624ad042-7790-477c-87d4-2c66527c0461)

### 5. Making Predictions Using New Data
- Predicts churn probabilities on the test set  
- Combines predictions with customer info  
- Saves results as `Predicted_Churners.csv` for Power BI integration

## Outputs
- `Predicted_Churners.csv` – At-risk customers predicted by the model  
- `Production_Data.xlsx` – Combined dataset with model scores for dashboarding  


## Key Takeaways
- The model identifies **customers likely to churn** based on contract type, internet services, and billing methods  
- Predictions are used in Power BI to **visualize and prioritize** high-risk customer segments
