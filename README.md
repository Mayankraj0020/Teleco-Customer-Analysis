# Telecom Customer Churn Prediction Using Data Analytics and Machine Learning

## 📌 Project Overview

This project focuses on analysing telecom customer data and predicting customer churn using Data Analytics and Machine Learning techniques.

Customer churn occurs when customers stop using a company's services. The objective of this project is to identify potential churn customers by analysing customer behaviour, service usage, contract details, and billing information.

The project uses the IBM Telco Customer Churn dataset and applies multiple machine learning algorithms to predict whether a customer is likely to leave the service.

## 🎯 Project Objectives

- Analyse telecom customer data to understand customer behaviour.
- Perform data cleaning and preprocessing.
- Identify important factors influencing customer churn.
- Apply Exploratory Data Analysis (EDA) and data visualisation.
- Build regression and classification models.
- Compare machine learning models using evaluation metrics.
- Understand how predictive analytics can support customer retention strategies.

## 📂 Dataset

**Dataset:** IBM Telco Customer Churn Dataset

- Total Records: 7,043 customers
- Total Features: 21 columns
- Target Variable: `Churn`
- Churn Categories: `Yes` and `No`

The dataset contains customer information such as:
- Demographic details
- Tenure
- Internet and phone services
- Contract type
- Payment method
- Monthly charges
- Total charges
- Customer churn status

## 🛠️ Tools & Technologies

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Development Environment:** Spyder
- **Version Control:** Git and GitHub

## ⚙️ Project Workflow

### 1. Data Cleaning and Preprocessing
- Checked missing values and duplicate records.
- Converted `TotalCharges` into numeric format.
- Handled missing values in `TotalCharges`.
- Removed unnecessary `customerID` column.
- Separated numerical and categorical features.

### 2. Exploratory Data Analysis (EDA)

Performed visual analysis to understand customer churn patterns.

Key analysis includes:
- Overall customer churn distribution.
- Contract type vs. churn.
- Tenure vs. churn.
- Monthly charges vs. churn.
- Internet service vs. churn.
- Payment method vs. churn.
- Correlation analysis of numerical features.

### 3. Regression Analysis

Applied regression techniques to explore the relationship between customer tenure and monthly charges.

- Linear Regression
- Polynomial Regression

### 4. Classification Models

Implemented and compared five classification algorithms:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Naive Bayes
4. Decision Tree
5. Random Forest

### 5. Model Evaluation

Evaluated model performance using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Classification Report

## 📊 Model Performance Comparison

The following results were obtained during model evaluation:

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 79.84% | 64.06% | 54.81% | 59.08% |
| KNN | 74.24% | 51.51% | 50.27% | 50.88% |
| Naive Bayes | 74.66% | 51.60% | 73.26% | 60.55% |
| Decision Tree | 73.74% | 50.50% | 54.01% | 52.20% |
| Random Forest | 79.35% | 63.88% | 51.07% | 56.76% |

### Key Findings

- Logistic Regression achieved the highest accuracy of **79.84%**.
- Naive Bayes achieved the highest recall of **73.26%**.
- Naive Bayes also achieved the highest F1 Score of **60.55%**.
- Logistic Regression performed best in terms of overall accuracy and precision.

**Conclusion:** Naive Bayes is a strong choice when identifying as many potential churn customers as possible is the priority, while Logistic Regression performs best in overall accuracy.

## 📁 Project Structure

```text
Telecom-Customer-Churn-Prediction/
│
├── dataset/
│   └── Telco-Customer-Churn.csv
│
├── graphs/
│   ├── churn_distribution.png
│   ├── contract_vs_churn.png
│   ├── tenure_vs_churn.png
│   ├── monthlycharges_vs_churn.png
│   ├── internetservice_vs_churn.png
│   └── model_comparison.png
│
├── Telecom_Customer_Churn.py
│
├── README.md
│
└── requirements.txt
```

*Note: Adjust the folder and file names according to the files you actually upload.*

## ▶️ How to Run the Project

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Step 2: Navigate to the Project Folder

```bash
cd Telecom-Customer-Churn-Prediction
```

### Step 3: Install Required Libraries

```bash
pip install -r requirements.txt
```

### Step 4: Run the Python File

```bash
python Telecom_Customer_Churn.py
```

## 📦 Requirements

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
```

## 🔮 Future Scope

- Improve model performance through hyperparameter tuning.
- Apply advanced ensemble learning techniques.
- Use feature selection to identify the most influential churn factors.
- Develop an interactive dashboard for customer churn analysis.
- Deploy the trained model as a web application.

## 🎓 Academic Information

**Course:** INT234 – Predictive Analytics  
**Institution:** Lovely Professional University (LPU)  
**Project:** Telecom Customer Churn Prediction Using Data Analytics and Machine Learning

## 👨‍💻 Author

**Mayank Raj**  
B.Tech – Computer Science and Engineering  
Lovely Professional University

---

⭐ If you find this project useful, feel free to explore the repository and share your feedback.

**Thank you for visiting!**
