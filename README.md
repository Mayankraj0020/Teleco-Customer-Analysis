# Telecom Customer Churn Prediction Using Data Analytics and Machine Learning

## 📌 Project Overview

This project focuses on analyzing telecom customer data and predicting whether a customer is likely to leave the company (Churn) or continue using its services.

The project uses Python, Data Analytics, and Machine Learning techniques to understand customer behavior, explore important patterns, and build predictive models.

It also includes regression analysis to predict monthly customer charges.

## 🎯 Project Objectives

- Analyze telecom customer data using Exploratory Data Analysis (EDA).
- Identify customer churn patterns and trends.
- Understand the relationship between customer attributes and churn.
- Analyze skewness in numerical features.
- Detect potential outliers using the IQR method.
- Predict monthly charges using regression models.
- Build and compare multiple classification models for churn prediction.
- Evaluate model performance using different evaluation metrics.

## 📂 Dataset Information

**Dataset:** IBM Telco Customer Churn Dataset

- Original records: 7,043
- Original features: 21
- Target variable: `Churn`
- Target classes: `Yes` and `No`

The dataset contains customer information such as:

- Gender
- Senior Citizen
- Partner and Dependents
- Tenure
- Phone Service
- Internet Service
- Contract Type
- Payment Method
- Monthly Charges
- Total Charges
- Churn Status

## 🛠️ Technologies and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## ⚙️ Project Workflow

### 1. Data Loading

- Loaded the Telco Customer Churn CSV dataset using Pandas.
- Examined the first and last records.
- Checked dataset dimensions, column names, data types, and statistical summaries.

### 2. Data Cleaning and Preprocessing

- Checked missing values.
- Converted `TotalCharges` into numeric format.
- Replaced invalid or missing `TotalCharges` values with 0.
- Checked and removed duplicate records.
- Dropped the `customerID` column because it is an identifier and not a useful predictive feature.

### 3. Exploratory Data Analysis (EDA)

Performed visual analysis to understand customer behavior using:

- Churn distribution count plot.
- Contract type vs. churn.
- Tenure vs. churn box plot.
- Monthly charges vs. churn box plot.
- Internet service vs. churn.
- Payment method vs. churn.
- Correlation heatmap.

### 4. Skewness Analysis

- Calculated skewness for numerical features.
- Used histograms with KDE curves to understand feature distributions.
- Examined whether numerical data was positively or negatively skewed.

### 5. Outlier Detection

- Used the Interquartile Range (IQR) method.
- Calculated Q1, Q3, IQR, lower bound, and upper bound.
- Identified potential outliers in:
  - Tenure
  - MonthlyCharges
  - TotalCharges
- Used box plots to visualize potential outliers.

**Note:** The project detects and analyzes potential outliers; it does not remove or cap them.

### 6. Regression Models

Regression analysis was performed to predict `MonthlyCharges`.

**Multiple Linear Regression**
- Used multiple customer-related input features.
- Applied Label Encoding to categorical input features.
- Applied StandardScaler to numerical model inputs.
- Evaluated predictions using MAE, MSE, RMSE, and R² Score.

**Polynomial Regression**
- Used `tenure` to predict `MonthlyCharges`.
- Applied PolynomialFeatures with degree 5.
- Trained a Linear Regression model on the transformed features.
- Visualized the actual data and polynomial regression curve.

### 7. Classification Data Preparation

- Selected `Churn` as the target variable.
- Used the remaining customer attributes as input features.
- Applied Label Encoding to categorical features.
- Encoded the target variable:
  - No = 0
  - Yes = 1
- Split the dataset into training and testing sets using an 80:20 ratio.
- Used stratified splitting to maintain class proportions.
- Applied StandardScaler for Logistic Regression and KNN.

### 8. Machine Learning Classification Models

Four classification algorithms were implemented:

1. **Logistic Regression**
   - Used for binary classification of customer churn.

2. **K-Nearest Neighbors (KNN)**
   - Used to classify customers based on their nearest data points.
   - Used 5 neighbors.

3. **Decision Tree**
   - Used tree-based decision rules to predict customer churn.
   - Visualized the trained decision tree.

4. **Random Forest**
   - Used an ensemble of 100 decision trees.
   - Combined predictions using majority voting.
   - Visualized the first tree from the Random Forest model.

### 9. Model Evaluation

All classification models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Classification Report

A comparison table and bar chart were created to compare model performance.

## 📊 Classification Model Results

The following results were obtained from the model comparison:

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 79.84% | 64.06% | 54.81% | 59.08% |
| Random Forest | 79.49% | 64.31% | 51.07% | 56.93% |
| KNN | 74.24% | 51.51% | 50.27% | 50.88% |
| Decision Tree | 72.89% | 48.98% | 51.60% | 50.26% |

### 🏆 Best Performing Model

**Logistic Regression** achieved the best overall performance among the four classification models based on the reported results.

- Accuracy: 79.84%
- Precision: 64.06%
- Recall: 54.81%
- F1 Score: 59.08%

It achieved the highest Accuracy, Recall, and F1 Score among the tested classification models.

Random Forest achieved the highest Precision of 64.31%.

## 📈 Regression Evaluation Metrics

The regression models were evaluated using:

- **MAE:** Mean Absolute Error
- **MSE:** Mean Squared Error
- **RMSE:** Root Mean Squared Error
- **R² Score:** Coefficient of Determination

The actual regression results are generated when the Python script is executed.

## 📁 Project Structure

```text
Telecom-Customer-Churn-Prediction/
│
├── Telecom-Customer-Churn.csv
├── telecom_churn.py
├── README.md
│
└── outputs/
    ├── churn_distribution.png
    ├── correlation_heatmap.png
    ├── confusion_matrix.png
    ├── decision_tree.png
    └── model_comparison.png
```

*The outputs folder is optional. Add the actual generated images if you want to display them in your GitHub repository.*

## ▶️ How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/Telecom-Customer-Churn-Prediction.git
```

### Step 2: Navigate to the Project Folder

```bash
cd Telecom-Customer-Churn-Prediction
```

### Step 3: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Step 4: Add the Dataset

Download the IBM Telco Customer Churn dataset and place the CSV file in your project folder.

Update the dataset path in the Python script:

```python
df = pd.read_csv("Telco-Customer-Churn.csv")
```

### Step 5: Run the Python Script

```bash
python telecom_churn.py
```

## 💡 Key Learning Outcomes

- Practical experience with data cleaning and preprocessing.
- Understanding of Exploratory Data Analysis.
- Analyzing skewness and detecting outliers using IQR.
- Implementing Multiple Linear and Polynomial Regression.
- Understanding supervised machine learning and binary classification.
- Implementing and comparing four classification algorithms.
- Evaluating models using Accuracy, Precision, Recall, and F1 Score.
- Visualizing machine learning results using Matplotlib and Seaborn.

## 🔮 Future Improvements

- Improve churn prediction performance through hyperparameter tuning.
- Explore additional feature engineering techniques.
- Address class imbalance using suitable methods.
- Experiment with additional classification algorithms.
- Develop an interactive dashboard for customer churn analysis.
- Deploy the trained model as a web application.

## 👨‍💻 Author

**Mayank Raj**

B.Tech CSE | Data Science & Machine Learning Enthusiast

[LinkedIn](https://www.linkedin.com/in/mayankraj0020/)

---

⭐ If you find this project useful, feel free to star the repository!
